# 论文结构与功能句式

用于从研究材料形成初稿，或在作者授权后重组章节。所有句式都是可选的编辑框架，方括号是本参考文件的教学占位符，不应直接出现在交付的投稿正文中。

## 1. 主线先于章节

先明确四件事：实际任务；工况变化造成的控制困难；方法改变了哪一部分；哪个结果支持其价值。它们应构成因果清楚的论证，而不是背景词汇、组件名称和指标的拼接。

例如，研究问题可能是工作点和目标指令变化时两个通道的协同跟踪；一次切换中的单通道改善是证据之一，不应把整篇论文改写成只解决该通道的保持问题。

贡献应说明结构或机制带来的能力。不要仅把参考模型、回归项、投影算子和分配器列成四个“贡献”。已有的内环或分配器可作为接口背景，不能因为在框图中出现就宣称为本文新方法。

## 2. 摘要：问题、动作、主要证据

采用合适篇幅回答：控制对象面对什么变化；本文设计什么；它如何处理该变化；试验给出什么主要结果。省去实现流水账和与主张无关的防御性话语。

可用句式：

```text
Changes in [operating condition] alter [physical quantity] and affect [task].
We develop a [controller] for [controlled variables / task].
The controller estimates [specified terms] and updates [specified inputs].
The controller design parameters remain fixed across [specified tests].
Compared with [baseline], the method reduces mean [metric] from [A] to [B]
under [condition].
```

从实验结论中选择最重要的证据，不把所有数字抄入摘要。控制器简称若使用，应在首次出现时给出一致的全称；不要单独使用读者还不了解的C1/C2编号。

## 3. 引言：从实际任务与现实意义展开

按“实际任务与现实意义 → 相关研究及已有成果 → 尚存问题与本文研究问题 → 本文方法与验证安排”的顺序组织。每个环节可按材料分成一段或多段，段数与篇幅由研究内容和投稿要求决定。

### 3.1 实际任务与现实意义

开篇说明研究对象面向哪些实际任务、这些任务为何值得研究，以及该类系统能够提供什么相关能力。先建立应用价值和研究背景，再逐步进入具体技术问题。

以水空航行器论文为例，可从有依据的应用需求切入，说明其跨介质能力如何服务这些任务，再引出相关平台与控制研究。具体应用领域、功能和优势以作者材料及文献为依据。“受到关注”或“成为研究热点”可以在文献支持时使用，并紧接具体能力与现实意义。将这一展开方式迁移到其他平台时，替换任务、对象和能力，不沿用水空航行器的具体背景。

```text
[Application task] requires [documented capability] under [conditions].
[Platform class] supports [application] through [documented capability].
The ability to [capability] is relevant to [specific practical need].
```

### 3.2 相关研究与已有成果

接着介绍已有研究做了什么、实现了什么，以及与本文任务的关系。按相关的研究方向或技术路径组织文献，可由平台和系统研究逐步过渡到与本稿直接相关的控制方法。每组文献应有共同主题，说明代表性工作的对象、方法、能力或结果。

已有平台设计、感知或姿态控制成果应准确引用，区分本稿采用的已有基础与本稿新增贡献。介绍机构、运动模式和执行器接口时，选择有助于理解应用能力或后续研究问题的信息。

```text
[Authors] developed [platform or method] for [task].
The system in [citation] achieves [documented capability] using [approach].
For [related control task], [authors] proposed [method] to address [effect].
These studies establish [supported capability] under [reported conditions].
```

### 3.3 尚存问题与本文研究问题

在已有成果的基础上，指出目标任务或工况中仍需解决的具体问题，并将其收束为本文的研究问题。说明问题发生在什么条件下、影响哪个对象或性能，以及为什么已有研究尚未充分解决这一需求。控制难点在这里结合物理机制、模型关系和文献证据具体展开。

文献中的限制应有相应来源；材料尚不足以支持整个领域的研究空白时，明确本文需要处理的设计问题。避免把每篇文献都写成“存在不足”，也不要凭空使用“现有方法均无法……”或“首次解决……”。

```text
Under [target condition], [supported unresolved issue] remains.
Changes in [physical quantity] affect [controlled behavior] during [operation].
The resulting problem is to [control objective] while [design requirement].
```

### 3.4 本文方法与验证安排

最后围绕刚提出的研究问题引出本文方法，说明方法的主要思路及其针对的问题，再概括有证据支持的贡献与验证安排。交代仿真、实物试验或其他已完成验证分别考察什么；保留到方法章和实验章再展开的实现细节。贡献的数量与验证类型由实际研究决定，章节安排按需要简述。

```text
To address [research problem], we develop [method] that [key action].
The method accounts for [specified effects] through [supported mechanism].
We evaluate [property] in [simulation study] and examine [capability]
in [experimental study].
```

平台实物图、结构图应在解释相应对象的正文中被引用；有图注和标签并不等于正文已经引用。上述句式为可选框架，具体研究事实、引用及验证范围均由当前材料确定。

## 4. 定义、假设与模型

| 语义操作 | 常用英文句式 | 中文对应 |
| --- | --- | --- |
| 定义变量 | `Let x denote ...` / `The state vector is defined as ...` | 令x表示…… / 状态向量定义为…… |
| 描述模型 | `The system dynamics are given by ...` | 系统动力学方程为…… |
| 解释符号 | `where M is ... and d denotes ...` | 其中，M为……，d表示…… |
| 提出假设 | `We assume that ...` / `... is assumed to be ...` | 假设…… |
| 给出局部条件 | `Near [operating point], ...` / `Under [conditions], ...` | 在……附近 / 在……条件下 |
| 区分模型职责 | `The simulation uses [full model]. The controller uses [local model].` | 仿真采用……；控制器采用…… |

先命名对象再给公式。不要在一个含糊的 `they form` 后突然引入读者尚不知道用途的向量。真实假设与人为设计选择分开写；不是所有“选取”都叫假设，也不是所有建模近似都能写成等式恒成立。

## 5. 控制器设计与推导

```text
The reference model is selected as ...
The tracking error is defined as ...
Substituting [expression] into [equation] gives ...
We obtain P by solving ...
The control input is computed as ...
The estimate is projected onto [specified set].
```

`is selected as` 对应设计，`is defined as` 对应定义，`is obtained from` 对应已有推导或计算。不要为了句式多样性混淆三者。

`ensures`、`guarantees` 和 `is stable` 需要相应数学依据及条件。只有仿真和实物结果时，写测试中的实际行为，不把实验轨迹当成稳定性定理。

## 6. 实现：写出信号和时序

```text
At sampling instant k, the controller uses [available quantities] to
construct [regressor / estimate].
The derivative is estimated from [measurements] using [specified method].
The reference-model states are initialized to [confirmed values].
The estimates are reset at the start of each independent trial.
The reference-model states are not reset at command changes.
The current output is stored for the next sampling instant.
```

上述操作仅在实际实现吻合时使用。不要把例句中的重置规则、求导方法或操作顺序自动移入另一篇论文。

对于多步实现，用两三句说清必要顺序即可。完整逐行伪代码只有在任务需要时提供；实现说明也不应退化为版本追溯日志。

## 7. 实验：每一组承担一个论证职责

| 试验类型 | 主要职责 | 推荐写法与边界 |
| --- | --- | --- |
| 标称仿真 | 展示基本响应与合理的性能参照 | 同时报告任务涉及的主要通道；客观说明调参，不为对照方法辩解 |
| 标称实物试验 | 展示架构在实际系统中的运行及比较结果 | 写实际测量、初始化和评价方式，不以hardware含糊代称试验 |
| 工作点网格 | 检验既定设计参数下跨工况跟踪 | 明确哪些设置固定，并报告工况间变化，不直接外推到任意环境 |
| 指令切换 | 检验目标变化后的跟踪与通道间影响 | 明确改变一个还是多个指令，区分参考曲线与统计汇总 |
| 消融或机制比较 | 支持性能来自某个设计因素 | 只有实际存在该实验时才安排，不能从对比结果中虚构机制验证 |

这些是职责类型，不是必须新增的实验清单。保留作者当前实验编号与主体结构，除非其明确要求重组。

涉及完整实验章节时，继续读取 [仿真与实验叙事：TASE 实例](tase-experiment-narrative.md)。其中说明图、表、正文的分工，局部解释与章节总结的位置，以及标称比较、消融和现场演示的不同证据作用。这些是基于已读论文归纳的写作选择，不是期刊强制格式，也不是每段必须套用的句子顺序。

```text
We compare [method] with [baselines] under [conditions].
The controllers are tuned for [nominal task].
The controller design parameters remain unchanged across [test set].
Figure [reference] shows representative trials.
Table [reference] reports the mean and standard deviation of [trial metric].
The mean [channel] RMSE is lower than that of [baseline] in [conditions].
Across the tested operating points, ...
```

不要把 `well tuned` 写成 `optimally tuned`，也不要虚构“相同带宽”“充分优化”来制造公平性。提供实际采用的设置和一致条件即可。

## 8. 讨论混合结果

让最强、最相关的优势成为重点，保留读者判断比较所需的数据。某指标并非全面领先时，不用一句笼统的 `outperforms in all channels` 覆盖事实。

若已确认两个控制器的速度误差都满足任务标准，而主要收益在深度通道，可以写：

```text
Both controllers keep mean speed RMSE below [documented threshold].
The proposed method reduces mean depth RMSE during [specified changes].
```

这里的阈值必须有数据或任务要求支持，不能为了淡化差异临时挑选。没有定义综合指标时，不把这种结果改称“总体误差更低”；没有统计检验时，不用 `statistically significant`。`similar`、`comparable` 也不能替代未经建立的等效性结论。

## 9. 结论：留下研究记忆点

```text
We developed [method] for [task].
The method [principal action] while retaining [existing interface, if relevant].
With [confirmed settings], the tests show [main supported result].
```

不新增结果、保证或审稿式评价。与核心结论无关的未来工作不必机械添加；真正限制结论的条件应在相应模型或结果处准确陈述，不能在全文中隐藏，再把删除结论中的局限段误称为扬长避短。
