# 检索策略文档

**系统综述标题：** 直接血管内治疗与桥接治疗（静脉溶栓联合血管内治疗）用于急性大血管闭塞缺血性卒中的系统综述与 Meta 分析

**方案版本：** 1.0

**检索策略版本：** 1.0

**文档日期：** 2026年2月26日

**检索执行状态：** 待执行（本文档为预检索策略，须经信息学专家 PRESS 同行评审后方可执行）

---

## 目录

1. [检索概述](#1-检索概述)
2. [概念组分解与检索词汇表](#2-概念组分解与检索词汇表)
3. [各数据库完整检索式](#3-各数据库完整检索式)
4. [已知关键试验补充检索](#4-已知关键试验补充检索)
5. [补充检索策略](#5-补充检索策略)
6. [检索结果管理](#6-检索结果管理)
7. [检索策略验证](#7-检索策略验证)

---

## 1. 检索概述

### 1.1 研究问题

在急性大血管闭塞（Large Vessel Occlusion, LVO）缺血性卒中成年患者中，直接血管内治疗（Direct EVT，不予前置静脉溶栓）与桥接治疗（Bridging Therapy，静脉溶栓 [alteplase 或 tenecteplase] 联合 EVT）相比，在90天功能独立（mRS 0–2）、全因死亡率、症状性颅内出血（sICH）及成功再通率（mTICI 2b–3）方面是否不劣于或优于后者？

### 1.2 PICO 框架摘要

| PICO 要素 | 定义 |
|-----------|------|
| **P（人群）** | 急性 LVO 缺血性卒中成年患者（年龄 ≥18岁），经影像证实存在 ICA 末段、MCA M1/M2 段、基底动脉或椎动脉颅内段闭塞 |
| **I（干预）** | 直接血管内治疗（Direct EVT）：机械取栓或其他血管内再通治疗，不预先给予静脉溶栓药物 |
| **C（对照）** | 桥接治疗（Bridging Therapy）：静脉注射 alteplase（0.9 mg/kg）或 tenecteplase（0.25 mg/kg 或 0.4 mg/kg）后进行 EVT |
| **O（结局）** | 主要：90天 mRS 0–2；次要：90天全因死亡率、sICH 发生率、mTICI 2b–3 再通率 |
| **S（研究设计）** | 随机对照试验（RCT），含优效性及非劣效性设计 |

### 1.3 检索时间范围

**起始日期：** 2000年1月1日

**截止日期：** 检索执行当日（滚动更新，无终止限制）

**选择理由：** 虽然经皮血管内治疗技术在2015年后经多项里程碑式 RCT（MR CLEAN、ESCAPE、EXTEND-IA 等）确立其有效性，但将检索起始日期定为2000年1月1日可确保完整覆盖所有早期可行性研究及先驱性试验，体现系统综述的最大敏感性原则。

### 1.4 语言限制

**无语言限制。** 所有语种的相关文献均予以检索和保留，非英文文献将借助翻译工具（DeepL、Google Translate）或双语研究人员进行筛选与数据提取。

### 1.5 研究设计限制

本检索策略应用经过验证的 RCT 方法学过滤器，以提高检索精确性，同时保留高敏感度。具体过滤器见第3节各数据库检索式。

### 1.6 覆盖数据库列表

| 序号 | 数据库 | 访问平台 | 受控词表 |
|------|--------|----------|----------|
| 1 | PubMed/MEDLINE | NLM (pubmed.ncbi.nlm.nih.gov) | MeSH (Medical Subject Headings) |
| 2 | Embase | Elsevier Embase.com 或 Ovid 平台 | Emtree |
| 3 | Cochrane Central Register of Controlled Trials (CENTRAL) | Cochrane Library (cochranelibrary.com) | MeSH（Cochrane 版本） |
| 4 | Web of Science Core Collection | Clarivate Analytics | 无受控词，纯自由词 |
| 5 | ClinicalTrials.gov | NIH/NLM (clinicaltrials.gov) | 结构化字段检索 |
| 补充 | WHO ICTRP | apps.who.int/trialsearch | 自由词 |

---

## 2. 概念组分解与检索词汇表

本检索策略将研究问题分解为四个核心概念组（Concept Blocks）。在每个数据库的检索式中，**同一概念组内的检索词使用 OR 连接，不同概念组之间使用 AND 连接**。

> **设计说明：** 干预（Direct EVT）与对照（桥接治疗）共享相同的医学概念词汇（血管内治疗和溶栓治疗），因此不单独设立"干预 vs. 对照"概念组，而是将 EVT 相关词汇设为概念组2，溶栓相关词汇设为概念组3，通过概念组2 AND 概念组3 的逻辑交集自动锁定比较两种策略组合的研究。区分直接 EVT 与桥接治疗的核心是研究在文题摘要中同时提及两者，而非依赖单一词汇。RCT 限定通过概念组4实现。

---

### 2.1 概念组1：人群 — 急性大血管闭塞缺血性卒中

#### MeSH 术语（PubMed 用）

| MeSH 术语 | 说明 |
|-----------|------|
| `Brain Ischemia`[MeSH] | 脑缺血（上位词，爆炸检索可涵盖缺血性卒中相关词条） |
| `Stroke`[MeSH] | 卒中（含缺血性和出血性，通过自由词限定缺血性） |
| `Ischemic Stroke`[MeSH] | 缺血性卒中（2018年起的 MeSH 独立词条） |
| `Cerebral Infarction`[MeSH] | 脑梗死 |
| `Arterial Occlusive Diseases`[MeSH] | 动脉闭塞性疾病 |
| `Carotid Artery, Internal`[MeSH] | 颈内动脉（LVO 涉及血管之一） |
| `Middle Cerebral Artery`[MeSH] | 大脑中动脉 |
| `Basilar Artery`[MeSH] | 基底动脉 |
| `Vertebral Artery`[MeSH] | 椎动脉 |

> **注意：** `Ischemic Stroke`[MeSH] 于2018年正式加入 MeSH 词表，检索时建议与 `Stroke`[MeSH] 并用以确保对2018年前文献的覆盖。

#### Emtree 术语（Embase 用）

| Emtree 术语 | 说明 |
|-------------|------|
| `ischemic stroke`/exp | 缺血性卒中（爆炸检索） |
| `brain ischemia`/exp | 脑缺血（爆炸检索） |
| `cerebrovascular accident`/exp | 脑血管意外 |
| `cerebral artery occlusion`/exp | 脑动脉闭塞 |
| `internal carotid artery occlusion`/exp | 颈内动脉闭塞 |
| `middle cerebral artery occlusion`/exp | 大脑中动脉闭塞 |
| `basilar artery occlusion`/exp | 基底动脉闭塞 |
| `large vessel occlusion`/exp（若可用） | 大血管闭塞 |

> **注意：** Emtree 中 `large vessel occlusion` 作为独立词条的可用性视版本而定，建议同时使用自由词补充。

#### 自由词同义词（含缩写、拼写变体、截词符）

```
"large vessel occlusion"
"large-vessel occlusion"
"large artery occlusion"
"large-artery occlusion"
LVO
"proximal occlusion"
"proximal vessel occlusion"
"acute ischemic stroke"
"acute ischaemic stroke"
"acute cerebral ischemia"
"acute cerebral ischaemia"
"acute cerebral infarction"
"acute brain ischemia"
"acute brain ischaemia"
"anterior circulation stroke"
"posterior circulation stroke"
"internal carotid artery occlusion"
ICA occlusion
"middle cerebral artery occlusion"
"MCA occlusion"
"MCA-M1 occlusion"
"M1 occlusion"
"basilar artery occlusion"
"vertebrobasilar occlusion"
"tandem occlusion"
```

**截词和通配符说明：**
- `isch*mic` 可同时涵盖 ischemic / ischaemic（注意：部分数据库通配符语法不同）
- 在 PubMed 中使用 `[tiab]` 字段限制标题/摘要检索

---

### 2.2 概念组2：干预/对照核心 — 血管内治疗 / 机械取栓

#### MeSH 术语（PubMed 用）

| MeSH 术语 | 说明 |
|-----------|------|
| `Thrombectomy`[MeSH] | 血栓切除术 / 取栓术 |
| `Endovascular Procedures`[MeSH] | 血管内操作（上位词，爆炸检索） |
| `Mechanical Thrombolysis`[MeSH] | 机械溶栓（含机械取栓） |
| `Stents`[MeSH] | 支架（涵盖支架取栓器相关词条，慎用） |

> **注意：** `Mechanical Thrombectomy` 尚未在 MeSH 中作为独立词条存在（截至2025年），建议以 `Thrombectomy`[MeSH] 配合自由词 `mechanical thrombectomy` 共同检索。

#### Emtree 术语（Embase 用）

| Emtree 术语 | 说明 |
|-------------|------|
| `thrombectomy`/exp | 取栓术（爆炸检索） |
| `mechanical thrombectomy`/exp | 机械取栓（若作为独立 Emtree 词条可用） |
| `endovascular surgery`/exp | 血管内手术（爆炸） |
| `endovascular treatment`/exp | 血管内治疗 |
| `stent retriever`/exp | 支架取栓器（若可用） |
| `cerebrovascular thrombolysis`/exp | 脑血管溶栓术（含机械方式） |

#### 自由词同义词

```
"endovascular treatment"
"endovascular therapy"
"endovascular intervention"
"endovascular procedure"
EVT
"mechanical thrombectomy"
MT
"mechanical recanalization"
thrombectomy
"intra-arterial treatment"
"intra-arterial therapy"
"intraarterial treatment"
"intraarterial therapy"
"intra-arterial thrombectomy"
"stent retriever"
"stent-retriever"
"stent retriever thrombectomy"
"contact aspiration"
"aspiration thrombectomy"
ADAPT
"direct aspiration"
"direct aspiration first pass"
DAPT
"combined approach"
"Solitaire"
"Trevo"
"balloon guide catheter"
BGC
"catheter-based thrombectomy"
"neurothrombectomy"
"cerebral thrombectomy"
"clot retrieval"
"clot removal"
"recanalization"
"revascularization"
```

---

### 2.3 概念组3：溶栓治疗 — 静脉溶栓 / alteplase / tenecteplase / 桥接治疗

#### MeSH 术语（PubMed 用）

| MeSH 术语 | 说明 |
|-----------|------|
| `Thrombolytic Therapy`[MeSH] | 溶栓治疗（上位词，爆炸检索） |
| `Tissue Plasminogen Activator`[MeSH] | 组织型纤溶酶原激活剂（alteplase 的 MeSH 词条） |
| `Fibrinolytic Agents`[MeSH] | 纤溶药物（上位词） |
| `Streptokinase`[MeSH] | 链激酶（保留以覆盖历史文献，但与本题关联性低） |

> **注意：** Tenecteplase 的 MeSH 词条为 `Tenecteplase`（2019年后加入），亦可通过 `Tissue Plasminogen Activator`[MeSH] 的爆炸检索覆盖，但建议同时使用自由词 `tenecteplase` 单独列出。

#### Emtree 术语（Embase 用）

| Emtree 术语 | 说明 |
|-------------|------|
| `alteplase`/exp | 阿替普酶（爆炸检索） |
| `tenecteplase`/exp | 替奈普酶（爆炸检索） |
| `thrombolysis`/exp | 溶栓（爆炸检索） |
| `thrombolytic therapy`/exp | 溶栓治疗（爆炸检索） |
| `tissue plasminogen activator`/exp | 组织型纤溶酶原激活剂 |
| `fibrinolytic agent`/exp | 纤溶药物 |
| `recombinant tissue plasminogen activator`/exp | 重组 tPA |
| `intravenous thrombolysis`/exp（若可用） | 静脉溶栓 |

#### 自由词同义词

```
"intravenous thrombolysis"
"IV thrombolysis"
"intravenous thrombolytic"
"IV thrombolytic"
"intravenous fibrinolysis"
"systemic thrombolysis"
"systemic fibrinolysis"
"intravenous alteplase"
"IV alteplase"
alteplase
"rt-PA"
rtPA
"recombinant tPA"
"recombinant tissue plasminogen activator"
"tissue plasminogen activator"
tPA
"t-PA"
"Actilyse"
"Activase"
"intravenous tenecteplase"
"IV tenecteplase"
tenecteplase
TNK
"TNK-tPA"
TNKase
"bridging therapy"
"bridging treatment"
"bridging strategy"
"drip and ship"
"drip-and-ship"
"combined treatment"
"combined therapy"
"thrombolysis plus thrombectomy"
"IVT plus EVT"
"IVT+EVT"
"tPA plus thrombectomy"
"alteplase plus thrombectomy"
```

---

### 2.4 概念组4：研究设计 — RCT 限定

#### MeSH 术语（PubMed 用）

| MeSH 术语 | 说明 |
|-----------|------|
| `Randomized Controlled Trial`[pt] | 随机对照试验（出版物类型字段） |
| `Randomized Controlled Trials as Topic`[MeSH] | 作为研究主题的 RCT |
| `Random Allocation`[MeSH] | 随机分配 |
| `Clinical Trial`[pt] | 临床试验（出版物类型，较宽泛） |

> **说明：** 使用 `[pt]`（Publication Type）字段标签比 `[MeSH]` 更精确，可直接过滤出版物类型。

#### Emtree 术语（Embase 用）

| Emtree 术语 | 说明 |
|-------------|------|
| `randomized controlled trial`/exp | 随机对照试验（爆炸检索） |
| `random allocation`/exp | 随机分配 |
| `clinical trial`/exp | 临床试验（较宽泛） |

#### 自由词同义词

```
"randomized controlled trial"
"randomised controlled trial"
"randomized clinical trial"
"randomised clinical trial"
"randomized trial"
"randomised trial"
"RCT"
"randomly assigned"
"randomly allocated"
"random assignment"
"random allocation"
"random*" (截词，配合字段限定)
"non-inferiority trial"
"non-inferiority study"
"non-inferiority randomized"
"superiority trial"
"double-blind"
"single-blind"
"open-label randomized"
```

---

### 2.5 布尔逻辑组合说明

**最终组合逻辑：**

```
(概念组1：人群) AND (概念组2：EVT) AND (概念组3：溶栓) AND (概念组4：RCT)
```

**逻辑依据：**
- 概念组1 AND 概念组2：确保文献同时涉及 LVO 卒中人群和血管内治疗
- AND 概念组3：进一步限定为同时涉及溶栓治疗（无论是桥接还是对照组）的研究，自然排除仅描述机械取栓无溶栓比较的研究
- AND 概念组4：限定为随机对照试验

**敏感性保障：**
由于本综述的核心比较是"有溶栓 vs. 无溶栓"，检索策略通过要求文献同时包含 EVT 词汇和溶栓词汇来实现，而非依赖"直接 EVT"或"桥接治疗"等概念词组（这类词组的 MeSH 覆盖尚不完善），从而最大化检索敏感度。

---

## 3. 各数据库完整检索式

---

### 3.1 PubMed/MEDLINE

**平台：** https://pubmed.ncbi.nlm.nih.gov/

**检索日期：** [待填写，格式：YYYY-MM-DD]

**检索结果数：** [待填写]

**语法说明：**
- `[MeSH]`：MeSH 受控词（爆炸检索，默认包含下位词）
- `[MeSH:NoExp]`：MeSH 受控词，不爆炸
- `[tiab]`：标题/摘要字段（Title/Abstract）
- `[pt]`：出版物类型字段（Publication Type）
- `*`：截词符（在 PubMed 中置于词根末尾）
- 布尔运算符（AND, OR, NOT）须大写

```
#1  "Brain Ischemia"[MeSH] OR "Stroke"[MeSH] OR "Ischemic Stroke"[MeSH] OR "Cerebral Infarction"[MeSH]

#2  "large vessel occlusion"[tiab] OR "large-vessel occlusion"[tiab] OR "large artery occlusion"[tiab] OR "large-artery occlusion"[tiab] OR "proximal occlusion"[tiab] OR "proximal vessel occlusion"[tiab] OR LVO[tiab]

#3  "acute ischemic stroke"[tiab] OR "acute ischaemic stroke"[tiab] OR "acute cerebral ischemia"[tiab] OR "acute cerebral ischaemia"[tiab] OR "acute cerebral infarction"[tiab] OR "acute brain ischemia"[tiab] OR "acute brain ischaemia"[tiab]

#4  "internal carotid artery occlusion"[tiab] OR "ICA occlusion"[tiab] OR "middle cerebral artery occlusion"[tiab] OR "MCA occlusion"[tiab] OR "MCA-M1"[tiab] OR "M1 occlusion"[tiab] OR "basilar artery occlusion"[tiab] OR "vertebrobasilar occlusion"[tiab] OR "tandem occlusion"[tiab] OR "anterior circulation stroke"[tiab] OR "posterior circulation stroke"[tiab]

#5  "Carotid Artery, Internal"[MeSH] OR "Middle Cerebral Artery"[MeSH] OR "Basilar Artery"[MeSH] OR "Vertebral Artery"[MeSH] OR "Arterial Occlusive Diseases"[MeSH]

#6  #1 OR #2 OR #3 OR #4 OR #5

#7  "Thrombectomy"[MeSH] OR "Endovascular Procedures"[MeSH] OR "Mechanical Thrombolysis"[MeSH]

#8  "endovascular treatment"[tiab] OR "endovascular therapy"[tiab] OR "endovascular intervention"[tiab] OR "endovascular procedure"[tiab] OR EVT[tiab]

#9  "mechanical thrombectomy"[tiab] OR "mechanical recanalization"[tiab] OR thrombectomy[tiab] OR "intra-arterial treatment"[tiab] OR "intra-arterial therapy"[tiab] OR "intraarterial treatment"[tiab] OR "intraarterial therapy"[tiab]

#10 "stent retriever"[tiab] OR "stent-retriever"[tiab] OR "contact aspiration"[tiab] OR "aspiration thrombectomy"[tiab] OR ADAPT[tiab] OR "direct aspiration"[tiab] OR "clot retrieval"[tiab] OR "clot removal"[tiab]

#11 recanalization[tiab] OR revascularization[tiab] OR "neurothrombectomy"[tiab] OR "cerebral thrombectomy"[tiab]

#12 #7 OR #8 OR #9 OR #10 OR #11

#13 "Thrombolytic Therapy"[MeSH] OR "Tissue Plasminogen Activator"[MeSH] OR "Fibrinolytic Agents"[MeSH] OR "Tenecteplase"[MeSH]

#14 "intravenous thrombolysis"[tiab] OR "IV thrombolysis"[tiab] OR "intravenous thrombolytic"[tiab] OR "IV thrombolytic"[tiab] OR "intravenous fibrinolysis"[tiab] OR "systemic thrombolysis"[tiab]

#15 alteplase[tiab] OR "rt-PA"[tiab] OR rtPA[tiab] OR "recombinant tPA"[tiab] OR "recombinant tissue plasminogen activator"[tiab] OR "tissue plasminogen activator"[tiab] OR tPA[tiab] OR "t-PA"[tiab] OR Actilyse[tiab] OR Activase[tiab]

#16 tenecteplase[tiab] OR TNK[tiab] OR "TNK-tPA"[tiab] OR TNKase[tiab]

#17 "bridging therapy"[tiab] OR "bridging treatment"[tiab] OR "bridging strategy"[tiab] OR "drip and ship"[tiab] OR "drip-and-ship"[tiab] OR "combined treatment"[tiab] OR "combined therapy"[tiab]

#18 "thrombolysis plus thrombectomy"[tiab] OR "IVT plus EVT"[tiab] OR "tPA plus thrombectomy"[tiab] OR "alteplase plus thrombectomy"[tiab] OR "tenecteplase plus thrombectomy"[tiab]

#19 #13 OR #14 OR #15 OR #16 OR #17 OR #18

#20 "Randomized Controlled Trial"[pt] OR "Randomized Controlled Trials as Topic"[MeSH] OR "Random Allocation"[MeSH]

#21 "randomized controlled trial"[tiab] OR "randomised controlled trial"[tiab] OR "randomized clinical trial"[tiab] OR "randomised clinical trial"[tiab] OR "randomized trial"[tiab] OR "randomised trial"[tiab] OR RCT[tiab]

#22 "randomly assigned"[tiab] OR "randomly allocated"[tiab] OR "random assignment"[tiab] OR "random allocation"[tiab] OR "randomly randomized"[tiab] OR "non-inferiority trial"[tiab] OR "non-inferiority randomized"[tiab]

#23 random*[tiab]

#24 #20 OR #21 OR #22 OR #23

#25 #6 AND #12 AND #19 AND #24

#26 (#25) AND ("2000/01/01"[PDAT] : "3000/12/31"[PDAT])
```

**最终检索式（第 #26 行）为完整策略，结合日期过滤。**

**注：** 若检索结果数量过大（>10,000），建议先在不加 RCT 过滤（不含 #24）的情况下评估结果规模，然后加入 #24 层。日期范围写法 `"3000/12/31"[PDAT]` 为 PubMed 惯用写法，代表无终止日期。

---

### 3.2 Embase（Ovid 平台）

**平台：** Ovid Embase（https://ovidsp.ovid.com/）

**检索日期：** [待填写，格式：YYYY-MM-DD]

**检索结果数：** [待填写]

**语法说明：**
- `/exp`：Emtree 受控词爆炸检索（exploded，包含下位词）
- `/de`：Emtree 受控词精确检索（不爆炸）
- `.ti,ab,kw.`：标题、摘要、关键词字段
- `adj3`：邻近运算符（两词之间最多间隔3个词）
- `*`：截词符
- `1 AND 2`：集合运算

```
1   ischemic stroke/exp OR brain ischemia/exp OR cerebrovascular accident/exp OR cerebral infarction/exp

2   cerebral artery occlusion/exp OR internal carotid artery occlusion/exp OR middle cerebral artery occlusion/exp OR basilar artery occlusion/exp

3   (large vessel occlusion OR large-vessel occlusion OR large artery occlusion OR large-artery occlusion OR proximal occlusion OR LVO).ti,ab,kw.

4   (acute ischemic stroke OR acute ischaemic stroke OR acute cerebral ischemia OR acute cerebral ischaemia OR acute cerebral infarction).ti,ab,kw.

5   (internal carotid artery occlusion OR ICA occlusion OR middle cerebral artery occlusion OR MCA occlusion OR MCA-M1 OR M1 occlusion OR basilar artery occlusion OR vertebrobasilar occlusion OR tandem occlusion).ti,ab,kw.

6   1 OR 2 OR 3 OR 4 OR 5

7   thrombectomy/exp OR endovascular surgery/exp OR endovascular treatment/exp

8   (endovascular treatment OR endovascular therapy OR endovascular intervention OR endovascular procedure OR EVT).ti,ab,kw.

9   (mechanical thrombectomy OR mechanical recanalization OR thrombectomy OR intra-arterial treatment OR intra-arterial therapy OR intraarterial treatment).ti,ab,kw.

10  (stent retriever OR stent-retriever OR contact aspiration OR aspiration thrombectomy OR ADAPT OR direct aspiration).ti,ab,kw.

11  (recanalization OR revascularization OR clot retrieval OR clot removal OR neurothrombectomy).ti,ab,kw.

12  7 OR 8 OR 9 OR 10 OR 11

13  alteplase/exp OR tenecteplase/exp OR thrombolytic therapy/exp OR tissue plasminogen activator/exp OR fibrinolytic agent/exp

14  (intravenous thrombolysis OR IV thrombolysis OR intravenous thrombolytic OR IV thrombolytic OR intravenous fibrinolysis OR systemic thrombolysis).ti,ab,kw.

15  (alteplase OR rt-PA OR rtPA OR recombinant tPA OR recombinant tissue plasminogen activator OR tissue plasminogen activator OR tPA OR t-PA OR Actilyse OR Activase).ti,ab,kw.

16  (tenecteplase OR TNK OR TNK-tPA OR TNKase).ti,ab,kw.

17  (bridging therapy OR bridging treatment OR bridging strategy OR drip and ship OR drip-and-ship OR combined treatment OR combined therapy).ti,ab,kw.

18  (thrombolysis plus thrombectomy OR IVT plus EVT OR tPA plus thrombectomy OR alteplase plus thrombectomy OR tenecteplase plus thrombectomy).ti,ab,kw.

19  13 OR 14 OR 15 OR 16 OR 17 OR 18

20  randomized controlled trial/exp OR random allocation/exp OR clinical trial/exp

21  (randomized controlled trial OR randomised controlled trial OR randomized clinical trial OR randomised clinical trial OR randomized trial OR randomised trial OR RCT).ti,ab,kw.

22  (randomly assigned OR randomly allocated OR random assignment OR random allocation OR non-inferiority trial OR non-inferiority randomized).ti,ab,kw.

23  random*.ti,ab.

24  20 OR 21 OR 22 OR 23

25  6 AND 12 AND 19 AND 24

26  limit 25 to yr="2000 -"
```

**可选 — 去除 MEDLINE 重复（Embase-only 过滤）：**

若需单独获取 Embase 独有文献以避免与 PubMed 重复导入，可在最后添加：

```
27  25 AND [embase]/lim NOT [medline]/lim
```

> **说明：** 若使用文献管理软件（Endnote/Zotero）在导入后进行去重，则步骤27非必须，保留完整集合（步骤26）即可。

---

### 3.3 Cochrane Central Register of Controlled Trials (CENTRAL)

**平台：** Cochrane Library（https://www.cochranelibrary.com/）

**检索日期：** [待填写，格式：YYYY-MM-DD]

**检索结果数：** [待填写]

**语法说明：**
- `MeSH descriptor: [term] explode all trees`：MeSH 爆炸检索
- `[mh]`：MeSH 字段
- `[ti,ab,kw]` 或 `"term":ti,ab,kw`：标题、摘要、关键词字段
- `AND`, `OR`, `NOT`：布尔运算符（不区分大小写）
- Cochrane Library 的 CENTRAL 数据库本身已限定为对照试验，通常无需额外 RCT 过滤；但为确保完整性仍建议保留。

**Cochrane Library 高级检索界面检索式（可整段复制）：**

```
#1 MeSH descriptor: [Brain Ischemia] explode all trees
#2 MeSH descriptor: [Stroke] explode all trees
#3 MeSH descriptor: [Ischemic Stroke] explode all trees
#4 MeSH descriptor: [Cerebral Infarction] explode all trees
#5 MeSH descriptor: [Middle Cerebral Artery] explode all trees
#6 MeSH descriptor: [Basilar Artery] explode all trees
#7 MeSH descriptor: [Carotid Artery, Internal] explode all trees
#8 ("large vessel occlusion" OR "large-vessel occlusion" OR "large artery occlusion" OR LVO OR "proximal occlusion"):ti,ab,kw
#9 ("acute ischemic stroke" OR "acute ischaemic stroke" OR "acute cerebral ischemia" OR "acute cerebral ischaemia" OR "acute cerebral infarction"):ti,ab,kw
#10 ("internal carotid artery occlusion" OR "ICA occlusion" OR "middle cerebral artery occlusion" OR "MCA occlusion" OR "MCA-M1" OR "M1 occlusion" OR "basilar artery occlusion" OR "vertebrobasilar occlusion" OR "tandem occlusion"):ti,ab,kw
#11 #1 OR #2 OR #3 OR #4 OR #5 OR #6 OR #7 OR #8 OR #9 OR #10

#12 MeSH descriptor: [Thrombectomy] explode all trees
#13 MeSH descriptor: [Endovascular Procedures] explode all trees
#14 MeSH descriptor: [Mechanical Thrombolysis] explode all trees
#15 ("endovascular treatment" OR "endovascular therapy" OR "endovascular intervention" OR EVT OR "mechanical thrombectomy" OR thrombectomy):ti,ab,kw
#16 ("intra-arterial treatment" OR "intra-arterial therapy" OR "intraarterial treatment" OR "stent retriever" OR "contact aspiration" OR "aspiration thrombectomy" OR ADAPT):ti,ab,kw
#17 (recanalization OR revascularization OR "clot retrieval" OR "clot removal"):ti,ab,kw
#18 #12 OR #13 OR #14 OR #15 OR #16 OR #17

#19 MeSH descriptor: [Thrombolytic Therapy] explode all trees
#20 MeSH descriptor: [Tissue Plasminogen Activator] explode all trees
#21 MeSH descriptor: [Tenecteplase] explode all trees
#22 MeSH descriptor: [Fibrinolytic Agents] explode all trees
#23 ("intravenous thrombolysis" OR "IV thrombolysis" OR "intravenous thrombolytic" OR "systemic thrombolysis"):ti,ab,kw
#24 (alteplase OR "rt-PA" OR rtPA OR "recombinant tPA" OR "tissue plasminogen activator" OR tPA OR "t-PA" OR Actilyse OR Activase):ti,ab,kw
#25 (tenecteplase OR TNK OR "TNK-tPA" OR TNKase):ti,ab,kw
#26 ("bridging therapy" OR "bridging treatment" OR "bridging strategy" OR "drip and ship" OR "drip-and-ship"):ti,ab,kw
#27 ("combined treatment" OR "combined therapy" OR "thrombolysis plus thrombectomy" OR "IVT plus EVT" OR "tPA plus thrombectomy"):ti,ab,kw
#28 #19 OR #20 OR #21 OR #22 OR #23 OR #24 OR #25 OR #26 OR #27

#29 MeSH descriptor: [Randomized Controlled Trial] explode all trees
#30 MeSH descriptor: [Random Allocation] explode all trees
#31 (random* OR "randomized controlled trial" OR "randomised controlled trial" OR RCT):ti,ab,kw
#32 #29 OR #30 OR #31

#33 #11 AND #18 AND #28
#34 #33 AND #32
#35 #34 with Publication Year from 2000 to 9999
```

> **说明：** CENTRAL 本身收录的绝大多数记录已为对照试验，步骤 #32 主要用于排除少数混入的非试验文献（如综述）。若在 Cochrane Library 内仅检索 CENTRAL（而非同时检索 Cochrane Reviews），步骤 #32 可酌情简化，保留 #33 AND 日期限制即可。

---

### 3.4 Web of Science（Core Collection）

**平台：** Clarivate Web of Science（https://www.webofscience.com/）

**检索日期：** [待填写，格式：YYYY-MM-DD]

**检索结果数：** [待填写]

**数据库范围：** Science Citation Index Expanded (SCI-EXPANDED), Social Sciences Citation Index (SSCI), Emerging Sources Citation Index (ESCI)

**语法说明：**
- `TS=`：Topic 字段（标题 + 摘要 + 关键词 + Keywords Plus）
- `TI=`：标题字段
- `*`：截词符（置于词根末尾）
- `$`：单字符通配符
- 双引号 `"..."` 表示短语检索
- `AND`, `OR`, `NOT`：布尔运算符（大写）
- Web of Science 无受控词表，仅使用自由词

```
#1  TS=("large vessel occlusion" OR "large-vessel occlusion" OR "large artery occlusion" OR "proximal occlusion" OR "LVO")

#2  TS=("acute ischemic stroke" OR "acute ischaemic stroke" OR "acute cerebral ischemia" OR "acute cerebral ischaemia" OR "acute cerebral infarction" OR "brain ischemia" OR "brain ischaemia" OR "cerebral infarction")

#3  TS=("internal carotid artery occlusion" OR "ICA occlusion" OR "middle cerebral artery occlusion" OR "MCA occlusion" OR "MCA-M1" OR "M1 occlusion" OR "basilar artery occlusion" OR "vertebrobasilar occlusion" OR "tandem occlusion")

#4  #1 OR #2 OR #3

#5  TS=("endovascular treatment" OR "endovascular therapy" OR "endovascular intervention" OR "EVT" OR "mechanical thrombectomy" OR "thrombectomy")

#6  TS=("intra-arterial treatment" OR "intra-arterial therapy" OR "intraarterial treatment" OR "intraarterial therapy" OR "stent retriever" OR "stent-retriever")

#7  TS=("contact aspiration" OR "aspiration thrombectomy" OR "ADAPT" OR "direct aspiration" OR "recanalization" OR "revascularization" OR "clot retrieval")

#8  #5 OR #6 OR #7

#9  TS=("intravenous thrombolysis" OR "IV thrombolysis" OR "intravenous thrombolytic" OR "systemic thrombolysis" OR "intravenous fibrinolysis")

#10 TS=(alteplase OR "rt-PA" OR "rtPA" OR "recombinant tPA" OR "tissue plasminogen activator" OR "tPA" OR "t-PA" OR "Actilyse" OR "Activase")

#11 TS=(tenecteplase OR "TNK" OR "TNK-tPA" OR "TNKase")

#12 TS=("bridging therapy" OR "bridging treatment" OR "bridging strategy" OR "drip and ship" OR "drip-and-ship" OR "combined treatment" OR "combined therapy")

#13 TS=("thrombolysis plus thrombectomy" OR "IVT plus EVT" OR "tPA plus thrombectomy" OR "alteplase plus thrombectomy" OR "tenecteplase plus thrombectomy")

#14 #9 OR #10 OR #11 OR #12 OR #13

#15 TS=("randomized controlled trial" OR "randomised controlled trial" OR "randomized clinical trial" OR "randomised clinical trial" OR "randomized trial" OR "randomised trial" OR "RCT")

#16 TS=("randomly assigned" OR "randomly allocated" OR "random assignment" OR "random allocation" OR "non-inferiority trial" OR "non-inferiority randomized")

#17 TS=(random*)

#18 #15 OR #16 OR #17

#19 #4 AND #8 AND #14 AND #18

#20 #19 AND PY=(2000-2026)
```

> **说明：** PY=(2000-2026) 中的2026应在执行检索时更新为当年年份。TS= 字段同时检索标题、摘要、关键词及 Keywords Plus，敏感性高。

---

### 3.5 ClinicalTrials.gov

**平台：** https://clinicaltrials.gov/

**检索日期：** [待填写]

**说明：** ClinicalTrials.gov 的高级检索功能支持按条件（Condition）、干预措施（Intervention）、研究类型（Study Type）等字段进行结构化检索。此数据库检索的主要目的是发现：（1）已注册但结果尚未发表于期刊的完整试验；（2）正在进行中的相关试验；（3）已完成但尚未发表的试验（用于发表偏倚评估）。

#### 高级检索字段填写建议

**检索方法一：基本字段组合**

| 字段 | 填写内容 |
|------|----------|
| **Conditions or disease** | `ischemic stroke` OR `large vessel occlusion` OR `stroke` |
| **Intervention/treatment** | `thrombectomy` OR `endovascular` OR `alteplase` OR `tenecteplase` |
| **Study type** | 选择 `Interventional studies (clinical trials)` |
| **Study phase** | Phase 2, Phase 3, Phase 4（可多选） |
| **Date range (First Posted)** | 2000-01-01 至今 |

**检索方法二：自由词全文检索（Other terms 字段）**

在 "Other terms" 字段输入以下检索式（支持布尔逻辑）：

```
(thrombectomy OR endovascular) AND (alteplase OR tenecteplase OR thrombolysis) AND (stroke OR "large vessel occlusion")
```

#### 补充：直接检索已知试验注册号

以下是已知核心 RCT 的注册编号，可直接在 ClinicalTrials.gov 检索：

| 试验名称 | 注册号 |
|----------|--------|
| DIRECT-MT | NCT03469206 |
| DEVT | NCT03864211 |
| MR CLEAN-NO IV | NCT03321006 |
| SKIP | NCT02930083 |
| SWIFT DIRECT | NCT03192332 |
| DIRECT-SAFE | NCT03494920 |
| MR CLEAN-LATE | NCT03781219 |
| BAOCHE | NCT02737189 |

**检索执行建议：**
1. 在高级检索界面分别执行方法一和方法二
2. 单独检索上述注册号
3. 将结果导出为 CSV 格式并保存

---

## 4. 已知关键试验补充检索

除上述系统性数据库检索外，以下已知相关 RCT 须单独进行精确名称检索，以验证系统检索的完整性（敏感度验证的一部分，见第7节）。

### 4.1 核心比较性 RCT（直接 EVT vs. 桥接治疗）

| 试验名称 | 国家/地区 | 发表年份 | 主要期刊 | 检索关键词（建议） |
|----------|-----------|----------|----------|-------------------|
| **DIRECT-MT** | 中国 | 2020 | NEJM | "DIRECT-MT" OR "direct-mt trial" |
| **DEVT** | 中国 | 2021 | JAMA | "DEVT" OR "DEVT trial" |
| **MR CLEAN-NO IV** | 荷兰 | 2021 | NEJM | "MR CLEAN-NO IV" OR "MRCLEAN-NOIV" OR "MR CLEAN NO IV" |
| **SKIP** | 日本 | 2021 | JAMA | "SKIP trial" OR "SKIP randomized" |
| **SWIFT DIRECT** | 欧洲/加拿大 | 2022 | Lancet | "SWIFT DIRECT" OR "SWIFTDIRECT" |
| **DIRECT-SAFE** | 澳大利亚/中国 | 2022 | Lancet Neurology | "DIRECT-SAFE" OR "DIRECT SAFE trial" |

### 4.2 相关背景 RCT（用于参考文献追溯）

| 试验名称 | 说明 |
|----------|------|
| **MR CLEAN** | 2015年奠基性 EVT vs. 标准治疗 RCT |
| **ESCAPE** | 2015年奠基性 RCT |
| **EXTEND-IA** | 2015年奠基性 RCT |
| **SWIFT PRIME** | 2015年奠基性 RCT |
| **DAWN** | 延伸时间窗 RCT（NEJM 2018） |
| **DEFUSE 3** | 延伸时间窗 RCT（NEJM 2018） |
| **ESCAPE-NA1** | Tenecteplase vs. alteplase 背景下的 EVT RCT |
| **BAOCHE** | 后循环 LVO（基底动脉闭塞）RCT |
| **ATTENTION** | 基底动脉闭塞 RCT（NEJM 2022） |

**补充检索执行方法：**

在 PubMed 中，将上述试验名称作为标题词检索：

```
"DIRECT-MT"[tiab] OR "DEVT"[tiab] OR "MR CLEAN-NO IV"[tiab] OR "SKIP trial"[tiab] OR "SWIFT DIRECT"[tiab] OR "DIRECT-SAFE"[tiab]
```

若上述任一已知试验未被主体系统检索策略（第3节）检索到，须记录遗漏原因，并相应扩展检索词汇。

---

## 5. 补充检索策略

### 5.1 参考文献追溯（Backward Citation Tracking）

**目的：** 通过阅读所有纳入研究的参考文献列表，发现可能未被数据库检索覆盖的相关研究。

**执行方法：**
- 对所有经全文筛选纳入的 RCT，人工检查其"参考文献"或"Introduction / Background"部分引用的相关 RCT
- 对以下已发表系统综述/Meta 分析的参考文献进行手工检索：
  - Katsanos et al. 及同期关于直接 EVT vs. 桥接治疗的 Meta 分析（2021–2023年）
  - Cochrane 卒中组已发表的相关综述
- 记录通过此途径发现的新文献数量

### 5.2 引文追踪（Forward Citation Tracking）

**目的：** 通过追踪核心纳入研究的引用，发现更新的相关研究或仍在进行中的后续试验。

**执行方法：**

1. **Google Scholar 引文追踪：**
   - 对每篇核心 RCT 在 Google Scholar 中搜索"被引用"列表
   - 重点关注发表年份晚于原始文献的引用文献

2. **Web of Science Cited Reference Search：**
   - 在 Web of Science 中使用 "Cited Reference Search" 功能
   - 以 DIRECT-MT（Yang 2020, NEJM）、DEVT（Zi 2021, JAMA）、MR CLEAN-NO IV（LeCouffe 2021, NEJM）等核心试验为种子文献
   - 检索其所有引用记录，筛选相关 RCT

3. **Scopus Citation Tracking（可选）：**
   - 在 Scopus 中使用 "Cited by" 功能进行补充

### 5.3 临床试验注册库检索

#### 5.3.1 WHO 国际临床试验注册平台（ICTRP）

**平台：** https://www.who.int/clinical-trials-registry-platform

**检索词：**

```
Condition: "ischemic stroke" OR "large vessel occlusion"
Intervention: "thrombectomy" OR "endovascular" OR "alteplase" OR "tenecteplase"
```

**执行步骤：**
1. 访问 WHO ICTRP 搜索门户（https://trialsearch.who.int/）
2. 在 "Title" 字段输入：`thrombectomy AND (alteplase OR tenecteplase OR thrombolysis)`
3. 在 "Condition" 字段输入：`ischemic stroke`
4. 选择 "Interventional" 研究类型
5. 导出结果

#### 5.3.2 其他注册库

| 注册库 | 网址 | 检索建议 |
|--------|------|----------|
| EU Clinical Trials Register（EudraCT/CTIS） | https://www.clinicaltrialsregister.eu/ | 关键词：`large vessel occlusion` + `thrombectomy` |
| ISRCTN Registry | https://www.isrctn.com/ | 关键词：`stroke` + `thrombectomy` + `alteplase` |
| Chinese Clinical Trial Registry（ChiCTR） | https://www.chictr.org.cn/ | 关键词：大血管闭塞 / 机械取栓 / 直接取栓 / 桥接治疗 |
| UMIN Clinical Trials Registry（日本） | https://www.umin.ac.jp/ctr/ | 检索 SKIP 试验注册及相关日本研究 |

### 5.4 灰色文献检索

#### 5.4.1 会议摘要

以下学术会议的年会摘要集应予以检索，以发现尚未正式发表的试验结果：

| 学术组织 | 会议名称 | 检索方式 |
|----------|----------|----------|
| American Heart Association / American Stroke Association (AHA/ASA) | International Stroke Conference (ISC) | 检索摘要集数据库（Stroke 杂志补充刊） |
| European Stroke Organisation (ESO) | European Stroke Organisation Conference (ESOC) | 检索 ESO 官网摘要数据库及 European Stroke Journal |
| Society of NeuroInterventional Surgery (SNIS) | SNIS Annual Meeting | 检索 Journal of NeuroInterventional Surgery 摘要刊 |
| World Stroke Congress (WSC) | 世界卒中大会 | 检索 International Journal of Stroke 摘要刊 |

**检索关键词：** `direct EVT` OR `direct thrombectomy` OR `bridging therapy` OR `large vessel occlusion` AND `randomized`

#### 5.4.2 预印本服务器

| 平台 | 网址 | 检索建议 |
|------|------|----------|
| medRxiv | https://www.medrxiv.org/ | 关键词：`large vessel occlusion thrombectomy alteplase` |
| bioRxiv | https://www.biorxiv.org/ | 关键词：同上（神经科学相关预印本） |
| SSRN (Health Sciences) | https://ssrn.com/ | 关键词：`direct EVT bridging stroke` |

> **注意：** 预印本尚未经过同行评审，若发现相关预印本，需追踪其正式发表状态。根据本方案纳入标准（I5），仅纳入已发表于同行评审期刊的完整研究报告；但预印本可用于联系作者获取完整数据。

#### 5.4.3 学位论文（可选）

- **ProQuest Dissertations & Theses Global：** 检索关键词 `large vessel occlusion` AND `endovascular`
- **DART-Europe：** 欧洲博士论文数据库

### 5.5 重要期刊手工检索

以下期刊为本领域最重要的发表平台，建议对2019年至检索执行日的全部目录（Table of Contents）进行手工浏览或检索，以捕捉数据库索引延迟的文献：

| 期刊名称 | 关注重点 |
|----------|----------|
| New England Journal of Medicine (NEJM) | 奠基性卒中试验（如 DIRECT-MT、MR CLEAN-NO IV 均发表于此） |
| The Lancet Neurology | DIRECT-SAFE 等重要 RCT |
| The Lancet | SWIFT DIRECT 等重要 RCT |
| JAMA (Journal of the American Medical Association) | DEVT、SKIP 等重要 RCT |
| Stroke (AHA/ASA 官方期刊) | 大量卒中领域 RCT 和 Meta 分析 |
| JAMA Neurology | 神经病学专科 RCT |
| Neurology | 综合性神经病学期刊 |
| Journal of NeuroInterventional Surgery (JNIS) | 神经介入专科期刊，技术性 RCT |
| European Stroke Journal | 欧洲卒中组织官方期刊 |
| International Journal of Stroke | 世界卒中组织官方期刊 |

**手工检索方法：** 访问上述期刊官方网站，使用站内检索功能，关键词为 `large vessel occlusion` 和/或 `direct thrombectomy` 和/或 `bridging therapy`，或浏览目录页。

### 5.6 专家与作者联系

**目的：** 获取正在进行中或已完成但尚未发表的相关 RCT 数据。

**执行方法：**
1. 联系上述核心 RCT（DIRECT-MT、DEVT、MR CLEAN-NO IV、SKIP、SWIFT DIRECT、DIRECT-SAFE）的通讯作者，询问是否有更新数据或相关尚未发表的研究
2. 通过领域专家（神经介入治疗组专家、卒中指南制定委员会成员）询问是否知晓尚未发表的相关试验
3. 联系 Cochrane Stroke Group 确认是否有相关已注册的 Cochrane 综述

---

## 6. 检索结果管理

### 6.1 文献导入与去重流程

**步骤一：导入**
1. 将各数据库检索结果分别以 RIS 或 BibTeX 格式导出
2. 导入文献管理软件（推荐 **Zotero** 或 **Endnote 21**）
3. 各数据库结果分别建立独立分类夹（Collection），保留原始检索信息

**步骤二：自动去重**
1. 使用 Zotero 内置去重功能（Edit > Find Duplicates）或 Endnote 的 Find Duplicates 功能进行初步自动去重
2. 推荐同时使用 **ASySD（Automated Systematic Search Deduplicator）** 工具（https://estech.shinyapps.io/asyssd/）进行专门针对系统综述的自动去重，其算法针对文献管理场景优化

**步骤三：手动核查**
1. 对自动去重的结果进行人工审核
2. 重点核查：同一试验的多份报告（如主结局报告 vs. 亚组报告 vs. 长期随访报告）
3. 保留最完整或最新的报告版本，其他版本标记为"重复发表—已排除"并保存

**步骤四：导入筛选平台**
将去重后的文献列表导入系统综述管理平台（推荐 **Covidence**，https://www.covidence.org/；或 **Rayyan**，https://www.rayyan.ai/）进行双人独立筛选。

### 6.2 各数据库检索结果记录模板

在执行检索后，请填写以下记录表，用于 PRISMA 2020 流程图和方法学报告：

| 数据库 | 检索日期 | 检索结果数（原始） | 去重前合计 | 去重后合计 | 检索人员签名 |
|--------|----------|-------------------|------------|------------|-------------|
| PubMed/MEDLINE | | | | | |
| Embase | | | | | |
| Cochrane CENTRAL | | | | | |
| Web of Science | | | | | |
| ClinicalTrials.gov | | | | | |
| WHO ICTRP | | | | | |
| 补充检索（手工/灰色）| | | | | |
| **合计** | | | | | |

**去重统计记录：**

| 项目 | 数量 |
|------|------|
| 数据库检索合计（去重前）| |
| 自动去重删除 | |
| 手动去重删除 | |
| 去重后剩余（进入初筛）| |
| 其他来源补充文献 | |
| 进入初筛总计 | |

---

## 7. 检索策略验证

### 7.1 敏感度验证——已知核心 RCT 回检测试

**原则：** 检索策略的最低验证标准是，所有已知符合纳入标准的核心 RCT 均应被该策略检索到。若任何一项已知核心 RCT 未被检索到，须分析遗漏原因并修订检索策略，直至所有核心文献均可被覆盖。

**验证步骤：**

1. 对以下6项核心 RCT，逐一在 PubMed 中检索其 PMID（PubMed 文章编号）
2. 确认该 PMID 是否被第3.1节的完整检索式检索结果所包含
3. 记录验证结果

| 核心 RCT | 第一作者（年份） | PMID | 被 PubMed 检索式覆盖？ | 被 Embase 检索式覆盖？ | 备注 |
|----------|-----------------|------|----------------------|----------------------|------|
| DIRECT-MT | Yang (2020) | 32369035 | [ ] 是 [ ] 否 | [ ] 是 [ ] 否 | |
| DEVT | Zi (2021) | 33464336 | [ ] 是 [ ] 否 | [ ] 是 [ ] 否 | |
| MR CLEAN-NO IV | LeCouffe (2021) | 34758259 | [ ] 是 [ ] 否 | [ ] 是 [ ] 否 | |
| SKIP | Suzuki (2021) | 33464337 | [ ] 是 [ ] 否 | [ ] 是 [ ] 否 | |
| SWIFT DIRECT | Aamodt (2023) | — | [ ] 是 [ ] 否 | [ ] 是 [ ] 否 | 注：原引用的 Nogueira 2022 文献需核实准确 PMID |
| DIRECT-SAFE | Mitchell (2022) | 34863371 | [ ] 是 [ ] 否 | [ ] 是 [ ] 否 | |

**验证方法（PubMed 示例）：**

```
在 PubMed 高级检索中，将第3.1节的完整检索式（#26行）作为检索集合S，
然后检索：S AND 32369035[uid]
若结果数 = 1，则该文献被覆盖；若结果数 = 0，则遗漏。
或：将检索结果导出为 PubMed ID 列表，逐一核对。
```

### 7.2 检索策略同行评审（PRESS 清单）

根据 Cochrane 手册及系统综述方法学最佳实践，建议在正式执行检索前，由**具有医学信息学（Medical Librarianship / Information Specialist）专业背景的独立人员**，使用 **PRESS（Peer Review of Electronic Search Strategies）清单**对本检索策略进行同行评审。

**PRESS 2015 清单核查项目：**

| 评审维度 | 评审要点 | 状态 |
|----------|----------|------|
| 1. 翻译（Translation） | PICO 元素是否全面转化为检索词汇？ | [ ] 待评审 |
| 2. 布尔运算符（Boolean Logic） | AND/OR 使用是否正确？括号逻辑是否准确？ | [ ] 待评审 |
| 3. 主题词（Subject Headings） | MeSH 和 Emtree 术语选择是否恰当？爆炸检索是否合理？ | [ ] 待评审 |
| 4. 自由词（Text Words） | 同义词、拼写变体、截词符是否全面？ | [ ] 待评审 |
| 5. 语法和拼写（Syntax/Spelling） | 是否存在语法错误或拼写错误？ | [ ] 待评审 |
| 6. 范围（Limits/Filters） | 过滤器选择是否合理？是否引入不必要限制？ | [ ] 待评审 |

**PRESS 评审流程：**
1. 将本文档发送给信息学专家
2. 信息学专家独立复查检索式，记录问题
3. 与信息学专家讨论修订意见
4. 根据评审意见修订检索策略
5. 在发表文章中报告 PRESS 评审已完成，并致谢信息学专家

**参考文献：** McGowan J, Sampson M, Salzwedel DM, Cogo E, Foerster V, Lefebvre C. PRESS Peer Review of Electronic Search Strategies: 2015 Guideline Statement. *J Clin Epidemiol*. 2016;75:40–46.

### 7.3 检索更新计划

**建议：** 系统综述通常需要在投稿前进行检索更新。若从首次检索到论文投稿间隔超过6个月，建议执行更新检索，并筛选新增文献。具体更新策略：

1. 重新运行相同的检索式，限制日期范围为上次检索日期至今
2. 对新增文献按相同流程进行双人筛选
3. 在方法学部分报告更新检索的日期和结果

---

## 附录：检索策略汇总表

| 数据库 | 概念组1（人群） | 概念组2（EVT） | 概念组3（溶栓）| 概念组4（RCT）| 日期过滤 | 组合逻辑 |
|--------|----------------|---------------|----------------|---------------|----------|----------|
| PubMed | #1–#5 → #6 | #7–#11 → #12 | #13–#18 → #19 | #20–#23 → #24 | 2000– | #6 AND #12 AND #19 AND #24 |
| Embase (Ovid) | 1–5 → 6 | 7–11 → 12 | 13–18 → 19 | 20–23 → 24 | yr="2000-" | 6 AND 12 AND 19 AND 24 |
| Cochrane CENTRAL | #1–#10 → #11 | #12–#17 → #18 | #19–#27 → #28 | #29–#31 → #32 | 2000–9999 | #11 AND #18 AND #28（AND #32 可选）|
| Web of Science | #1–#3 → #4 | #5–#7 → #8 | #9–#13 → #14 | #15–#17 → #18 | PY=2000–2026 | #4 AND #8 AND #14 AND #18 |
| ClinicalTrials.gov | Condition 字段 | Intervention 字段 | Intervention 字段 | Study Type = Interventional | 2000– | 字段组合 |

---

*本检索策略文档版本1.0，起草日期：2026年2月26日。本文档须在正式检索执行前经信息学专家 PRESS 同行评审，且在检索执行后填写检索日期和结果数量。任何对检索策略的修订须记录修订内容、日期和理由。*
