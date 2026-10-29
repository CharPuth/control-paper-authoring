# 按语言功能选择通用句式

按句子要完成的动作查找，不按章节套用。方括号是待填内容，只用当前材料替换；不需要的句型跳过。原稿中的控制架构、参数、评价协议和实验场景不随句型迁入新论文。词义与搭配由当前领域 M05 提供；独立使用时可按需结合 control-paper-vocabulary。

以下为迁移、抽象和去重后的编辑句型，不是每条都有独立频次统计的文献原句。[来源记录](sources.md)区分观察、归纳和个人约定。

## 定义对象、描述模型与关系

- `Consider [system or problem].`
- `Let [symbol] denote [quantity].`
- `[Quantity] is defined as [expression].`
- `The dynamics of [system] are described by [equation].`
- `The components of [vector] are [meanings], respectively.`
- `[Transformation] maps [object] from [source representation] to [target representation].`

先命名被定义或描述的对象。公式后的符号解释按 [公式与自然语言](writing-rules.md#11-公式与自然语言)使用小写 `where`。

## 陈述假设、近似与适用条件

- `For [conditions], [quantity] is assumed to be [property].`
- `Neglecting [specified terms], [equation] reduces to [equation].`
- `Near [operating point], the dynamics are approximated by [equation].`
- `Under Assumptions [identifiers], [stated result] holds.`

assumed、approximated 和 defined 分别表达假设、近似和定义，不能仅为换词而互换。条件修饰实际依赖它的结论。

## 表达目标、设计选择与部件作用

- `The objective is to [task] while satisfying [requirement].`
- `We choose [design quantity] as [expression].`
- `[Gain or parameter] is selected to satisfy [condition].`
- `[Component] computes [output] from [inputs].`
- `[Term] compensates for [effect], while [other term] accounts for [other factor].`
- `[Variable] is updated according to [equation].`

选择了一个设计量与推导出一个结果是不同动作。组件名称及输入输出按当前研究填写，不预设内外环、分配器或自适应结构。

## 衔接运算、推导与论证

- `Substituting [expression] into [equation] gives [result].`
- `Rearranging [equation] yields [expression].`
- `Collecting the terms associated with [quantity] gives [relation].`
- `It follows from [relation or lemma] that [conclusion].`
- `Consider the Lyapunov function [expression].`
- `Differentiating [function] along the system trajectories gives [expression].`

写出真正执行的运算；不把含糊的“经过一些操作”自行补成某次具体代入。Lyapunov 句式只适用于材料已有相应论证的情况，不要求其他论文增加这一方法。

## 描述实现、初始化与时序

- `[Algorithm] is implemented on [platform].`
- `At [event], [state or variable] is initialized to [value].`
- `At sampling instant [index], [component] uses [available signals] to compute [quantity].`
- `[Operation] is performed before [dependent operation].`
- `[Stored quantity] is updated after [operation].`

这些句型用于表达已有操作，不规定重置策略、采样延迟、估计方法或积分与投影顺序。需要表达“不重置”时，直接用 `is not reset` 即可。

## 表达评价、比较与观测

- `We evaluate [property] over [conditions] using [metric].`
- `[Method] is compared with [baseline] under [conditions].`
- `Each [condition] was tested in [number] trials.`
- `[Metric] is evaluated over [defined interval or sample set].`
- `Table [identifier] reports [statistic] of [quantity] across [groups].`
- `At [condition], [method] reduces [metric] by [amount] relative to [baseline].`
- `As [variable] changes, [metric] changes from [initial value] to [final value].`
- `The [response] settles within [reported interval].`

统计对象、比较对象和条件就近说明，不预设 RMSE、试验截止事件或必须共用参数。涉及变化量与终值时，按词汇技能中的 from/to/by 教学例区分。

## 解释联系与承接已有内容

- `Using [previously introduced model or result], we [next action].`
- `The resulting [output] is passed to [next component].`
- `[Observation] is consistent with [interpretation].`
- `The results indicate [behavior] over [conditions].`
- `[Observed difference] is largest at [condition], where [specific observation].`

用句子交代实际依赖或联系，避免重复标题、泛泛评价和为了过渡补写原文没有的解释。上述功能可以出现在不同章节，不构成章节内容或顺序要求。
