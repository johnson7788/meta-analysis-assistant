# Meta 分析写作助手

## 简介

Claude Code 插件，通过 6 个专业 Agent 协作，帮助医学研究者完成 Meta 分析全流程——从研究方案制定到论文撰写。

目标用户为有医学背景的专业研究者和临床医生，熟悉 Meta 分析方法学，需要高效的写作与分析辅助工具。

## 安装

1. 将整个 `meta-analysis-assistant` 目录复制到 Claude Code 插件目录：

```bash
cp -r meta-analysis-assistant ~/.claude/plugins/
```

2. 重新启动 Claude Code，插件将自动加载。

3. 在 Claude Code 中输入 `/meta-analysis` 验证插件是否生效。

## 插件结构

```
meta-analysis-assistant/
├── .claude-plugin/
│   └── plugin.json                          # 插件清单文件
├── commands/
│   └── meta-analysis.md                     # /meta-analysis 命令定义
├── agents/
│   ├── protocol-designer.md                 # Agent 1: 研究方案设计
│   ├── search-strategist.md                 # Agent 2: 检索策略
│   ├── study-screener.md                    # Agent 3: 文献筛选
│   ├── data-extractor.md                    # Agent 4: 数据提取与质量评估
│   ├── statistician.md                      # Agent 5: 统计分析
│   └── manuscript-writer.md                 # Agent 6: 论文撰写
├── skills/
│   └── meta-analysis-methodology/
│       ├── SKILL.md                         # 方法学知识库 Skill 定义
│       └── references/
│           ├── prisma-2020.md               # PRISMA 2020 声明
│           ├── cochrane-handbook.md         # Cochrane 系统评价手册
│           ├── grade-framework.md           # GRADE 证据分级框架
│           ├── rob2-tool.md                 # RoB 2 偏倚风险评估工具
│           ├── nos-scale.md                 # Newcastle-Ottawa 量表
│           └── statistical-methods.md       # 统计方法参考
└── README.md                                # 本文件
```

## 使用方法

### 启动完整流程

在 Claude Code 中输入：

```
/meta-analysis
```

不带参数时，命令将启动完整的 Meta 分析流程引导。系统会先询问当前进度，然后按顺序触发 6 个 Agent，依次完成从研究方案制定到论文撰写的全部阶段：

```
protocol-designer → search-strategist → study-screener → data-extractor → statistician → manuscript-writer
```

每个 Agent 启动时会自动读取前序 Agent 的输出文件，确保信息传递连贯。

### 跳转到指定阶段

如果你已经完成了部分工作，可以通过参数直接跳转到指定阶段：

| 参数 | 说明 | 触发的 Agent |
|------|------|-------------|
| `protocol` | 制定研究方案（PICO、纳排标准） | protocol-designer |
| `search` | 设计检索策略（数据库、检索词） | search-strategist |
| `screen` | 辅助文献筛选（PRISMA 流程图） | study-screener |
| `extract` | 数据提取与质量评估 | data-extractor |
| `stats` | 统计分析（生成 R 代码） | statistician |
| `write` | 论文撰写（各章节、PRISMA 声明） | manuscript-writer |

示例：

```
/meta-analysis stats
```

上述命令将直接启动统计分析阶段。

### 自动触发

当对话涉及 Meta 分析相关话题时，相应的 Agent 和 Skill 会自动激活。例如：

- 讨论 PICO 框架或纳入排除标准时，protocol-designer 会自动参与
- 讨论检索策略或 MeSH 词时，search-strategist 会自动参与
- 讨论异质性、效应量、森林图等统计话题时，statistician 会自动参与
- 讨论 PRISMA、偏倚评估、GRADE 分级等方法学话题时，meta-analysis-methodology Skill 会自动提供参考

## Agent 说明

| Agent | 职责 | 模型 | 主要输出文件 |
|-------|------|------|-------------|
| protocol-designer | 引导明确研究问题（PICO/PICOS），制定纳入/排除标准，生成研究方案 | sonnet | `protocol.md` |
| search-strategist | 构建检索词，为不同数据库生成检索式（PubMed、Embase、Cochrane 等） | sonnet | `search-strategy.md` |
| study-screener | 设计筛选表格，制定筛选决策规则，记录筛选过程和排除原因 | sonnet | `screening-log.md`、`prisma-flow-data.md` |
| data-extractor | 设计数据提取表，选择质量评估工具（RoB 2 / NOS / QUADAS-2），引导偏倚评估 | sonnet | `data-extraction.md`、`quality-assessment.md` |
| statistician | 选择效应量与合成模型，生成 R 代码，异质性检验，亚组分析，发表偏倚检测 | opus | `analysis.R`、`statistical-results.md` |
| manuscript-writer | 撰写结构化论文（标题、摘要、引言、方法、结果、讨论），生成 PRISMA checklist | opus | `manuscript.md`、`prisma-checklist.md` |

## 输出文件

所有输出文件统一生成在用户项目的工作目录下：

| 文件 | 生成阶段 | 说明 |
|------|---------|------|
| `protocol.md` | 研究方案 | 包含 PICO 框架、纳入/排除标准、研究类型、PROSPERO 注册建议 |
| `search-strategy.md` | 检索策略 | 各数据库检索式、MeSH 词与自由词组合、布尔逻辑、补充检索建议 |
| `screening-log.md` | 文献筛选 | 筛选表格模板、决策规则、筛选记录及排除原因 |
| `prisma-flow-data.md` | 文献筛选 | PRISMA 流程图所需数据（各阶段文献数量） |
| `data-extraction.md` | 数据提取 | 数据提取表（研究特征、结局指标、效应量） |
| `quality-assessment.md` | 质量评估 | 偏倚风险评估结果和证据质量评估摘要 |
| `analysis.R` | 统计分析 | 完整 R 分析脚本（Meta 分析、森林图、漏斗图、敏感性分析） |
| `statistical-results.md` | 统计分析 | 统计结果解读（效应量、异质性、亚组分析、发表偏倚） |
| `manuscript.md` | 论文撰写 | 完整论文稿件（标题、摘要、引言、方法、结果、讨论） |
| `prisma-checklist.md` | 论文撰写 | PRISMA 2020 checklist（27 条逐项对照） |

## 依赖

统计分析阶段（statistician Agent）需要以下环境：

- **R 语言环境**（用于运行生成的统计分析代码）
- **R 包**：
  - `metafor` -- Meta 分析核心计算
  - `meta` -- Meta 分析辅助函数
  - `dmetar` -- 额外诊断与分析工具
  - `forestplot` -- 森林图绘制

安装 R 包：

```r
install.packages(c("metafor", "meta", "forestplot"))

# dmetar 需要从 GitHub 安装
if (!require("remotes")) install.packages("remotes")
remotes::install_github("MathiasHarworker/dmetar")
```

> 注意：如果不需要运行统计代码，仅生成 R 脚本则不需要安装以上依赖。

## 方法学参考

`skills/meta-analysis-methodology/` 目录下的 Skill 提供方法学知识库，在对话涉及相关话题时自动激活。参考文件说明如下：

| 文件 | 内容说明 |
|------|---------|
| `prisma-2020.md` | PRISMA 2020 声明 27 条 checklist 项目及流程图模板，用于规范系统评价的报告 |
| `cochrane-handbook.md` | Cochrane 系统评价手册核心要点，涵盖系统评价各阶段的方法学指导 |
| `grade-framework.md` | GRADE 证据分级框架，包括证据质量的升级和降级因素判定标准 |
| `rob2-tool.md` | RoB 2（Risk of Bias 2）偏倚风险评估工具，包含五个评估域及判定规则 |
| `nos-scale.md` | Newcastle-Ottawa Scale 量表，用于观察性研究的质量评分标准 |
| `statistical-methods.md` | 统计方法参考，包括效应量公式、模型选择决策树、异质性检验指标 |

## 许可

本插件供个人学术研究使用。
