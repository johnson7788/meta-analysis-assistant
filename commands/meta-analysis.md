---
description: 启动 Meta 分析写作助手，引导完成从研究方案到论文撰写的全流程
argument-hint: [protocol|search|screen|extract|stats|write]
allowed-tools: [Read, Write, Edit, Glob, Grep, Bash, WebSearch, WebFetch]
---

# Meta 分析写作助手

用户调用参数为：$ARGUMENTS

---

## 工作流程

### 无参数：完整流程引导

如果 `$ARGUMENTS` 为空，执行以下操作：

1. **检查当前工作目录中的已有文件**，判断项目进度：
   - `protocol.md` — 研究方案
   - `search-strategy.md` — 检索策略
   - `screening-log.md` — 文献筛选记录
   - `data-extraction.md` — 数据提取表
   - `statistical-results.md` — 统计分析结果
   - `manuscript.md` — 论文手稿

   使用 Glob 扫描工作目录中的这些文件。向用户展示各阶段完成情况的摘要。

2. **询问用户**：是从头开始，还是从某个特定阶段继续。

3. **按顺序引导用户完成以下 6 个阶段**，每个阶段完成后确认用户满意再进入下一阶段：

| 阶段 | 名称 | 触发的 Agent | 主要输出文件 |
|------|------|-------------|-------------|
| Stage 1 | 研究方案 | `protocol-designer` | `protocol.md` |
| Stage 2 | 检索策略 | `search-strategist` | `search-strategy.md` |
| Stage 3 | 文献筛选 | `study-screener` | `screening-log.md` |
| Stage 4 | 数据提取 | `data-extractor` | `data-extraction.md` |
| Stage 5 | 统计分析 | `statistician` | `statistical-results.md` |
| Stage 6 | 论文撰写 | `manuscript-writer` | `manuscript.md` |

每个阶段：
- 简要说明该阶段完成的任务和所需输入。
- 触发对应的 Agent 执行工作。
- Agent 完成后，将输出展示给用户审阅。
- 询问："对本阶段的结果满意吗？可以进入下一阶段，或者修改当前结果。"
- 仅在用户明确确认后才进入下一阶段。

---

### 带参数：跳转到指定阶段

如果 `$ARGUMENTS` 不为空，将参数映射到对应的 Agent：

| 参数 | 目标 Agent | 说明 |
|------|-----------|------|
| `protocol` | `protocol-designer` | 跳转到研究方案设计阶段 |
| `search` | `search-strategist` | 跳转到检索策略制定阶段 |
| `screen` | `study-screener` | 跳转到文献筛选阶段 |
| `extract` | `data-extractor` | 跳转到数据提取阶段 |
| `stats` | `statistician` | 跳转到统计分析阶段 |
| `write` | `manuscript-writer` | 跳转到论文撰写阶段 |

**前置依赖检查：** 在执行请求的阶段之前，验证前序阶段的必需文件是否存在。依赖链如下：

- `search` 需要：`protocol.md`
- `screen` 需要：`protocol.md`、`search-strategy.md`
- `extract` 需要：`protocol.md`、`search-strategy.md`、`screening-log.md`
- `stats` 需要：`data-extraction.md`
- `write` 需要：`protocol.md`、`statistical-results.md`

如果任何前置文件缺失，**明确警告用户**：

> ⚠️ 缺少前置文件：`<缺失文件>` 尚未生成。建议先完成对应阶段，或提供已有数据文件后再继续。

然后询问用户是否要：
1. 先完成缺失的前置阶段
2. 跳过检查，强制继续（可能导致输出质量下降）

---

## 输出文件一览

以下是整个 Meta 分析流程中产生的全部输出文件：

| 文件名 | 来源 Agent | 说明 |
|--------|-----------|------|
| `protocol.md` | `protocol-designer` | PRISMA-P 规范的研究方案，包含 PICOS 框架、纳入排除标准 |
| `search-strategy.md` | `search-strategist` | 多数据库检索策略，含检索词、布尔逻辑组合 |
| `screening-log.md` | `study-screener` | 文献筛选记录，含标题摘要筛选与全文筛选结果 |
| `prisma-flowchart.md` | `study-screener` | PRISMA 流程图数据（纳入/排除各阶段文献数量） |
| `data-extraction.md` | `data-extractor` | 结构化数据提取表（研究特征、结局指标、效应量） |
| `rob-assessment.md` | `data-extractor` | 偏倚风险评估结果（基于 RoB 2 或 NOS 等工具） |
| `statistical-results.md` | `statistician` | 统计分析结果，含合并效应量、异质性检验、亚组分析 |
| `analysis.py` | `statistician` | 完整 Python 分析脚本（含森林图、漏斗图） |
| `manuscript.md` | `manuscript-writer` | 完整论文手稿（PRISMA 2020 声明格式） |

---

## 注意事项

- **逐步确认**：每个阶段完成后，必须确认用户对结果满意，才能进入下一阶段。
- **允许回退**：用户可以随时回到之前的阶段进行修改。修改后应检查后续阶段是否需要同步更新。
- **保持一致性**：跨文件的关键信息（如 PICOS 定义、纳入标准、统计方法）必须保持一致。当某阶段产出更新时，提醒用户检查关联文件。
- **鼓励参与**：在关键决策点（如纳入排除标准制定、统计模型选择、敏感性分析方案）主动征求用户意见，而非自动决定。
- **透明沟通**：对每一步的方法选择给出理由，让用户理解"为什么这样做"。
- **质量把控**：在流程推进中自动检查常见问题（如检索策略覆盖度、数据提取完整性、统计假设合理性）。
