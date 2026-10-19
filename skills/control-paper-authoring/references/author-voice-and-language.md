# 作者视角与自然表达

适用于初稿、翻译和语言修改。下面的例句是原创编辑示例，不是某篇IEEE论文的逐字引文，也不代表示例中的方法已经在当前研究中实施。

## 1. 去AI味的目标是消除具体表达问题

把“有AI味”拆成可处理的问题：角色错误、无实际对象的辩解、条件堆叠、空泛评价、生僻修饰、压缩过度、指代不明、逻辑跳步、机械重复或聊天残留。不要用词汇黑名单代替判断。

同一句式重复不一定有问题。两个并列定义都用 `is defined as` 很自然；两个不同结论都用“充分展现了卓越的……”则可能掩盖本应不同的证据。

## 2. 作者身份：描述研究，不解释自己正在写论文

投稿正文写已经完成的方法和观察到的结果，不写编辑过程或假想审稿对话。

| 需要处理的表达 | 具体问题 | 有依据时的处理 |
| --- | --- | --- |
| `To avoid giving the impression that the baseline was poorly tuned, ...` | 向假想审稿人辩解，没有提供调参事实 | `The controllers are tuned for tracking at the nominal operating point.` |
| `It is important to clarify that our method is not intended to ...` | 以澄清和否定代替任务定义 | 直接写控制器调节的变量和研究工况 |
| `Its equivalence to the theoretical formulation awaits run-configuration confirmation.` | 把内部核查状态写进正文 | 作者已确认一致时，写已确认的实现；确有矛盾时，在正文外解决，不捏造一致性 |
| `As requested, the previous controller output is used ...` | 回复作者的语气 | `The regressor uses the controller output from the previous sampling instant.` |
| `The results appear to suggest that our approach may be effective.` | 多层虚弱限定，没有指出结果 | 据已提供统计量写明哪个指标在什么条件下较低 |
| `This paper successfully resolves all concerns about ...` | 预判审稿结论，并扩大研究范围 | 删除审稿评价，陈述实际完成的工作 |

`we`、被动句、`the controller` 和 `the results` 都可用于作者叙事。选择由本句重点决定，不按固定比例轮换。

必要条件不是“防御性写作”。例如 `under the stated assumptions`、`near the nominal operating point`、`in the tested conditions` 若限制了定理或实验结论，就应保留在相关主张旁，而不是为显得有信心而删除。

## 3. 区分有用对比与无对象的辩论

看到 `not ... but ...`、`rather than`、“不是……而是……”时，先问：两项是否都是读者需要区分的真实概念？

- 可保留：`The local model uses virtual control inputs rather than actuator-input increments.` 前提是模型确实如此，而且建模变量的差异属于研究动机。
- 应改写：`This is not just another controller, but a fundamentally different paradigm.` 没有可识别的比较内容，只有自我评价。
- 可直接陈述：`The controller uses the previous output to construct the regressor.` 通常不必补上“而不是未经确认的实际作用力”。
- 必须说明：若两个误差定义、坐标系或评价窗口容易混淆，明确区别属于必要技术说明，不应被去AI味规则删除。

不为论文虚构对手，不预测审稿人会问什么；用方法说明和证据回答真实问题。

## 4. 常见词、准确术语、完整关系

替换的理由是语义更清楚，不是字母更少。以下为语境建议，而非全局替换表。

| 待判断的表达 | 通常更清楚的写法 | 注意事项 |
| --- | --- | --- |
| `utilize`, `leverage` | `use` | 固定术语或引用题名不机械替换 |
| `ameliorate tracking deviations` | `reduce tracking error` | 保留误差类型与统计量 |
| `facilitate superior tracking capability` | `improve tracking`，或报告具体误差 | 无证据时不补写“improve” |
| `operational regimes` | `operating conditions` | 不同物理模式确实称为regime时可保留 |
| `seamless integration` | 指明哪个输出接入哪个输入 | 不凭空承诺无修改、低成本或容易部署 |
| `a comprehensive and robust framework` | 直接命名控制器、估计器或算法 | 技术性的鲁棒性质仍使用准确术语 |
| `force-level` 等自造层级名称 | 定义实际变量和接口 | 已有研究采用并清楚定义该术语时不一概禁止 |
| `hardware` 表示试验 | `experiments`、`pool experiments`、`bench tests` | 硬件、处理器、传感器和hardware-in-the-loop仍正常使用hardware |
| `hydrodynamic loads` 与 `hydrodynamic forces` 混用 | 按量的定义统一 | 载荷可能包含力矩；不能把六维力/力矩量缩成三维力 |

保留专业读者熟悉的词，如 `regressor`、`reference model`、`projection operator`、`asymptotic stability`。不要把 `input effectiveness` 模糊改成“control ability”，也不要把 `matched uncertainty` 简化成所有未知扰动。

同一个数学对象用同一个术语。不要为了避免重复，将控制器交替叫作 `framework`、`mechanism`、`paradigm` 和 `scheme`。

## 5. 防止“看似专业却没有说清”的压缩

每个短语都应能还原成具体关系：谁使用什么，计算什么，作用于哪个变量，在什么条件下产生哪个结果。不能还原时，优先展开句子，而不是再造一个缩写。

| 原表达 | 问题 | 条件成立时的改写 |
| --- | --- | --- |
| `Together with the moments, they form ...` | 代词与组合后的对象都不明确 | `The virtual control input vector is defined as ...` |
| `Adaptation acts on the commands.` | 动作和信号不清楚 | `The adaptive outer loop updates the virtual control inputs.` |
| `The force drives depth.` | 把动力学关系压成不准确的直觉描述 | `The vertical virtual input is the control input of the local depth model.` |
| `The controller addresses the acceleration produced by its force commands.` | 暗示了未定义的补偿对象或反馈关系 | 根据实际模型写估计哪些项、调整哪个输出；若研究仅补偿变化水动力，就只陈述这一点 |
| `The method ensures cross-condition adaptability.` | “确保”暗含保证，跨工况能力未定义 | 写固定哪些设计参数、测试哪些工况，以及对应的跟踪结果 |

`they form` 是正常英语，不是禁用语。只有指代不清、定义不明确或不符合当前段落结构时才改。

## 6. 中文：展开动作，减少强凑的名词短语

中文学术表达不应模仿宣传标题。连续的“面向、基于、多维、协同、赋能、闭环、一体化”若没有明确对象，会把简单关系写得难以理解。

| 原表达 | 较清楚的表达 | 保留的含义 |
| --- | --- | --- |
| 面向多工况载荷变化的控制能力增强实现 | 控制器补偿不同工况下变化的水动力，以改善跟踪性能 | 工况、补偿对象和目的 |
| 基于前序输出信息的回归构建机制 | 使用上一采样周期的控制器输出构造回归向量 | 采样时序与操作 |
| 速度深度协同跟踪性能提升验证 | 通过试验比较速度和深度的跟踪误差 | 两个通道与评价方式 |
| 多源异构扰动适应性强化 | 明确实际估计或补偿了哪些扰动；材料未给出时先询问 | 不用新词填补机制缺项 |
| 实现对深度变化率测量信息的滑窗求导处理 | 对测得的深度进行滑动窗口求导，得到深度变化率估计 | 输入、操作和输出 |
| 具有良好跨工况适用性的高性能控制策略 | 据数据写明参数是否重新整定、误差如何变化 | 不把评价形容词当作证据 |

改写时遵守这些判断：

- 修饰语应说明真实限制、对象或差异；只增加气势的定语删除。
- 前置定语过长时，改为“对象＋动作＋条件”的句子，或拆成定义与用途两句。
- 能用“测量、估计、计算、更新、补偿、比较、降低”准确描述时，不再叠加“实现……的……化”。
- “自适应控制”“模型预测控制”“输入到状态稳定性”等约定俗成术语不拆散；较长术语本身不是问题。
- 翻译前先还原中文关系，再用英文功能句式表达，不逐字翻译堆叠定语。
- 保持正式文体，不靠语气词、俚语、故意不对称或语法错误制造“活人感”。

## 7. 灵活性来自信息重心，不来自随机变化

定义时可以连续使用被动句；实现过程适合用控制器作主语；结果比较适合把统计量放到主语位置。转折只在实际有转折时出现，因果词只在逻辑成立时出现。

可以保留：`The state error is defined as ... The parameter error is defined as ...`

无需保留：每段都先写 `It is worth noting that`，再重复图中已有事实，最后用 `These findings underscore ...` 升华。

一句话同时容纳坐标定义、估计过程、补偿效果和实验意义时，应分开。两项确有紧密依赖关系时，也不必为了追求短句把它们拆散。没有统一句长、被动语态比例或同义词配额。

## 8. 精简式交稿判断

依次问：本句有新的有效信息吗？对象与动作明确吗？读者需要猜测术语含义吗？它在解释方法还是在替作者辩护？删掉某个限定会改变科学主张吗？

只改识别出的表达问题。不把所有句子重新写一遍，不将任何一次局部偏好升级为永久禁词。
