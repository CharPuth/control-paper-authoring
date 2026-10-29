# 控制论文通用写作规则

以下规则适用于句子及相邻句子，不分章节，不安排文章内容或章节结构。

## 1. 研究动作与主语

用主语明确动作承担者：`We design ...`、`The controller computes ...`、`The observer estimates ...`、`Fig. 3 shows ...`。系统、方法、图表或数学关系可以作主语。测试网格或参数变化是场景时，用 `We evaluate ... over ... / during ...` 更容易组织句子。

## 2. 动词与宾语

动词根据宾语选择：计算输入用 `compute the input`，求解问题用 `solve the problem`，推导关系用 `derive the relation`，趋近指令值用 `approach the commanded value`。避免用 `perform` 或 `conduct` 包裹本可直接作谓语的动作。

## 3. 主动句与被动句

`We compute the control input using (12).` 强调动作。`The control input is computed using (12).` 强调对象。两者都自然。已知动作承担者时，可以用被动句维持话题连续；不逐句强制改为主动句。

## 4. 减少名词化

`The estimation of the disturbance is carried out by the observer.` 可写为 `The observer estimates the disturbance.` 使用动词代替 `the computation / estimation / evaluation of ... is performed`。技术名称中的名词保留，例如 `control allocation`、`state estimation`。

## 5. 术语一致性与必要重复

同一变量、信号、参数和指标保持同一名称，不轮换同义词。`command-tracking error` 与 `model-tracking error`、`design parameters` 与 `parameter estimates` 分别指不同对象。定义句的 `is defined as` 可以重复，公式前后的同一术语也可以重复。

## 6. 指代与修饰对象

`this`、`it`、`both`、`same`、`fixed` 的对象应容易识别。先行词距离较远或存在多个候选时，重复具体名词：`both channels`、`the same control equations`、`fixed design parameters`。避免只写 `these settings` 或 `the above method` 而让读者回查。

## 7. 条件、方式与范围

条件常由 `under`、`for`、`when` 引出；方式常用 `by`、`using`；覆盖范围常用 `over`、`across`。让修饰语紧邻对象：`Parameters are tuned separately for A and B and held fixed within each series.` 句首条件短语后用逗号衔接主句。

## 8. 比较结构

比较同类对象：`The error is smaller than that of the baseline.`、`We compare the controller with two variants.` 对比多个动作时使用平行语法形式。`outperform` 直接接宾语，不接 `than`；`compared with`、`relative to` 或 `in terms of` 分别交代对象和指标。

## 9. 并列动作

算法操作序列使用平行谓语，例如 `reads the measurements, updates the estimates, and computes the input`。多个动词共有主语时通常不必重复主语。若动作宾语不同，分别写出对象，减少笼统的 `this` 或 `it`。示例只演示语法，实际操作及顺序采用当前材料的内容。

## 10. 统计量与单位的写法

统一正文与图表的指标名称。`mean error`、`mean RMSE`、`maximum RMSE` 的中心词不同；可用 `across trials` 或 `across operating conditions` 说明汇总维度。`from A to B` 写起点和终点，`by A` 写变化量。`a mean RMSE of ...` 和 `an RMSE below ...` 分别表示数值与阈值。

## 11. 公式与自然语言

将公式作为句子组成部分处理标点。公式后紧接符号、参数或条件解释时，必须用小写 `where` 接续同一句；公式末尾通常用逗号，不保留句号后再接小写 `where`，也不在 `where` 后机械加逗号。不另起 `Here` 句承担这一作用。这是作者确认的统一文风约定，不是 IEEE 强制语法规则；其他语境中的 here 不受此约束。定义、代入、变形和推导的可选句型见按需读取的 [通用句式](sentence-patterns.md)。

```text
The dynamics are given by
[equation],
where [symbol] denotes [quantity].
```

## 12. 图表引导句

用 `Fig. X shows [quantity or trend]`、`Table X reports [metric]`、`Table X summarizes [comparison]`。图表句的宾语写所展示的量，避免只写 `shows both trials` 等宽泛对象。`It can be clearly seen from ...` 通常可以改为图表作主语。

## 13. 时态

当前方法、数学关系和图表描述常用一般现在时：`The controller computes ...`、`Fig. 3 shows ...`。已完成的具体操作可用过去时：`We recorded the response at 100 Hz.` 时态由动作的时间含义决定，不要求整篇只有一个时态。

## 14. 连接词与解释句

根据关系使用 `because / since`、`therefore / thus`、`whereas / while`、`for example`。`indicating` 或 `suggesting` 可接续前句结果。避免每句都用 `Furthermore`、`Moreover`、`In addition` 开头；同一话题自然延续时可以不用连接副词。

## 15. 信息顺序与长句

主句先表达核心动作，条件、方式和结果围绕该动作排列。一个句子同时包含设置、指标定义、比较和解释时，可以拆为两个句子。拆句后仍使用具体名词承接话题，不把每个短句都写成孤立声明。

## 16. 修饰词与简洁度

优先使用具体对象、动作和指标。`very`、`fully`、`excellent`、`remarkable` 等泛化程度词常可删除。`robust control`、`adaptive control`、`optimal control` 等术语中的形容词按术语保留。`use`、`show`、`obtain`、`return` 都是自然的学术表达。

## 17. 相邻句子的衔接

让前句已经引入的对象成为后句容易识别的话题，避免连续引入不相关主语。一个自然段围绕同一局部问题展开；调整仅限句间衔接和冗余，不使用章节功能模板。

## 语言检查

检查动作是否具体、搭配是否自然、术语是否统一、指代是否明确、比较是否平行、修饰位置是否合适、时态是否协调、公式与图表句是否顺畅。普通润色只输出改写；用户需要时再解释关键修改。
