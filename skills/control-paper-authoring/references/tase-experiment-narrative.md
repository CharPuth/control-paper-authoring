# 仿真与实验叙事：TASE 实例

适用：控制与机器人论文的仿真、实物验证、机制消融和现场演示。与 `paper-structure-and-patterns.md` 第 7–8 节配合使用。这里补充如何组织证据，不替代控制语义、统计口径和作者事实。

## 依据及适用范围

2026-10-13 对下列 11 篇 TASE 机器人论文的验证章节进行了定向阅读，并以 1 篇直升机控制论文作补充。主要选取 2024–2026 卷年或在线发表的工作；卷年与首次在线年份可能不同。这是便于核查的写作样本，不是对全刊的随机抽样或期刊强制规则。公开录用稿与出版版在分页和文字上可能有差异，复查时以所列版本为准。

样本同时包含仿真与实物分章、合并验证章、先列实验再独立分析结果、仿真案例研究。常见做法是在结果附近给出具体解释；部分实验主要依靠曲线中的行为，部分依靠数值比较。同一篇论文可混用。独立 Discussion、小节总结、逐项报数均不是统一要求。发表过的论文也可能冗长或有过度解释；只借鉴有用的组织方式，不复制其措辞或未经核实的因果判断。

## 先确定每项实验回答什么

在写作前，用内部简表关联：作者确认的目的 → 改变的因素 → 对照的作用 → 可观察证据 → 支持的结论。缺少某项实验时，不把这张表转化为强制补实验清单。

| 实验职责 | 正文应回答 | 常用证据 |
| --- | --- | --- |
| 标称性能参照 | 基本任务能否完成；与常用控制器在这一条件下表现如何 | 主要通道响应、稳态偏差、少量误差指标 |
| 增广或模块贡献 | 在已确认的共同设置下，加入该部分带来什么变化 | 基准版本与增广版本的响应及指标 |
| 跨工作点比较 | 固定哪些设计参数后，在哪些目标值范围内仍有收益 | 配对结果、跨工作点汇总及分布 |
| 指令切换 | 目标变化怎样影响被调节量及耦合通道；何时恢复 | 双通道时序、关键过渡段及相应误差 |
| 饱和等机制试验 | 特定机制在何时起作用；内部状态呈现什么差异 | 残差、参数历史、边界驻留或更新活动；任务误差作为背景 |
| 现场运行 | 在已测环境和任务中是否实现预期行为 | 实测曲线与场景对应、任务完成情况，必要时补关键指标 |

不同对照承担不同职责。独立调参的 PID 与所提控制器比较，主要提供外部性能参照；共享基准结构的有无增广比较，才支持增广项的作用。二者不能互相替代。

标称场景中对照表现接近，是有效结果。直接陈述响应和差异，再将后续实验转向真正需要区分的条件。不要在正文替对照方法辩解；也不要把“表现接近”升级成统计等效或把作者确认的良好调参升级成全局最优。

## 章节与段落怎样安排

**章节开头**交代任务、主要对照、共享设置、测量及评价口径。具体试验只补新增条件。必要的评价窗、重置规则、控制器差异和统计量含义应就近明确；完整配置可交给表格，正文无需反复复述。

**结果段落**应让读者看清条件、观察、证据和含义。可从关键现象起笔，再给数字和解释；也可先给决定性的数值，再解释对应曲线。不要求固定句数或固定顺序，不让每段都以 “To verify…” 开头、以 “These results demonstrate…” 结尾。

局部解释回答“该现象说明这个方法在本项任务中做到了什么”。只有方法结构和实验对照共同支持时才写机制或因果。若结果足够直接，观察本身即可收束，无需额外补一句“验证了有效性”。

**章节结尾**仅在多项结果需要建立新的联系时简短综合。没有新信息时可直接进入下一章。独立 Discussion 用于真正需要跨试验解释的机制、权衡或适用条件，不机械追加一段泛化局限或再抄一遍指标。

**全文结论**回到方法贡献和实验共同支持的能力。不同试验支持不同主张，不能把某项标称比较、单次现场运行或参数曲线扩大为所有条件下的性能保证。

## 图、表、正文的分工

- 图展示时间过程、配对变化、空间行为与分布；表提供精确汇总；正文指出值得读者关注的变化及其研究含义。
- 正文只选择能改变判断的数值，例如主要效应量、关键阈值、发生时间或必要反例。没有固定的数字配额；避免逐行翻译表格。
- 主要问题是瞬态或内部机制时，可少报数，多解释有图可查的变化。不能用“曲线较好”代替对象、时段和行为。
- 单次代表曲线指标、重复试验指标均值、试验间标准差、时序信号标准差是不同统计量。保持实际口径，不将“代表试验值 ± 重复试验标准差”润色成“均值 ± 标准差”。
- 未定义综合指标时，以各相关通道的响应和指标解释协调跟踪表现，不编造“总体 RMSE”或隐藏不一致的指标方向。

## 消融与约束机制的特殊检查

同时开关多个部件，只能直接支持这组部件的合并作用。应准确说明对照变化，不能把它写成各部件的独立贡献。

投影已使两组参数有界时，参数有界本身不能证明残差补偿有效。可比较参数是否持续增长、是否长时间停留在边界、以及累计变化是否趋于平缓。参数冻结、总变差变平和参数收敛也不是同一个命题。

存在执行器饱和时，区分跟踪结果与自适应机制结果。若实验目的为抑制无法实现的控制需求引起的无效学习，应优先解释参数及残差证据。不能把“补偿无法恢复丢失的执行能力”写成“饱和时任何控制器都不可能改善任何性能指标”这种过强命题；观测到的指标差异仍保留其真实含义。

没有对照的现场试验可以支持特定任务下的实际运行表现；算法优越性应由已有比较试验支持。结论写到已有证据覆盖的范围即可，无需在正文反复提示缺少其他实验。

## 可核查实例

下列页码是链接 PDF 的从 1 开始的文件页码。每行只归纳结构和证据用法，不评价整篇论文的科学质量。

| 论文、TASE 年份与来源 | 所读位置与可借鉴之处 |
| --- | --- |
| Salt Ducaju 等，2025，Model-Based Predictive Impedance Variation for Obstacle Avoidance in Safe Human–Robot Collaboration；[全文](https://lucris.lub.lu.se/ws/portalfiles/portal/206302831/TASE_FINAL.pdf)，DOI 10.1109/TASE.2024.3508718 | V–VII，PDF 8–14 页（含封面）；先解释避障和恢复轨迹，再用 MAE 与偏离时长量化预测作用；仿真与实物分章。 |
| Franceschi 等，2024，Human–Robot Role Arbitration via Differential Game Theory；[全文](https://iris.unibs.it/bitstream/11379/590854/1/HumanRobot_Role_Arbitration_via_Differential_Game_Theory%20%281%29.pdf)，DOI 10.1109/TASE.2023.3320708 | III–IV，PDF 9–14 页；实验设置与结果分章，按三个任务解释角色分配行为，再综合力指标；保留不同场景下方法表现相近的结果。 |
| Zhang 等，2024，Adaptive Safety-Critical Control With Uncertainty Estimation for Human–Robot Collaboration；[全文](https://pureadmin.qub.ac.uk/ws/portalfiles/portal/522513053/Zhang_2023_IEEE_TASE.pdf)，DOI 10.1109/TASE.2023.3320873 | X，PDF 9–13 页（含封面）；仅仿真，静态与动态障碍场景中结合消融、误差、运动量和安全距离解释模块作用。 |
| Chen 等，2025 在线录用，Actuator Fault Estimation for a Class of Euler-Lagrange Systems Using Super-Twisting Observers；[录用稿](https://discovery.ucl.ac.uk/id/eprint/10213132/)，DOI 10.1109/TASE.2025.3604035 | IV-C/D，PDF 8–10 页；仅仿真，依无故障、单故障、多故障、比较组织；用收敛时间解释估计器与更新律关系。 |
| Lee 等，2025，QP Chaser: Polynomial Trajectory Generation for Autonomous Aerial Tracking；[录用稿全文](https://arxiv.org/pdf/2302.14273)，[期刊记录](https://pure.seoultech.ac.kr/en/publications/qp-chaser-polynomial-trajectory-generation-for-autonomous-aerial/)，DOI 10.1109/TASE.2025.3629046 | VI-F、VII，PDF 11–16 页；规划器基准测试后做完整追踪验证；大表保留全部指标，正文主要解释遮挡、碰撞与计算时间。所读版本标注 2025 年 10 月录用。 |
| Liu 等，2026，HEIGHT: Heterogeneous Interaction Graph Transformer for Robot Navigation in Crowded and Constrained Environments；[全文](https://www.joydeepb.com/Publications/arxiv2025_height.pdf)，DOI 10.1109/TASE.2025.3646588 | V–VII，PDF 7–15 页；仿真按研究问题和消融组织；实物分受控比较与现场运行，后者主要解释场景行为。 |
| Chen 等，2026，SLEI3D: Simultaneous Exploration and Inspection via Heterogeneous Fleets Under Limited Communication；[录用稿全文](https://mengguo.github.io/personal_site/papers/pdf/chen2025simul.pdf)，DOI 10.1109/TASE.2025.3643166 | V，PDF 10–19 页；模块、系统比较、扩展、复杂度、实物顺次组织；F 为实物，尽管章标题为 Numerical Experiments。时间线较长，不宜原样套用到短篇控制实验。 |
| Ma 等，2025，An End-to-End Deep Reinforcement Learning Based Modular Task Allocation Framework for Autonomous Mobile Systems；[全文](https://discovery.ucl.ac.uk/10187647/1/An_End-to-End_Deep_Reinforcement_Learning_Based_Modular_Task_Allocation_Framework_for_Autonomous_Mobile_Systems.pdf)，DOI 10.1109/TASE.2024.3367237 | V–VI，PDF 6–13 页；仿真含比较、消融及 Summary，实物侧重任务执行；存在章节小结不意味着其他稿件也必须添加。 |
| Wang 等，2025，Vision-Based Automatic Control of a Surgical Robot for Posterior Segment Ophthalmic Surgery；[全文](https://discovery.ucl.ac.uk/10195794/1/TASE_Vision-Based_Automatic_Control_of_a_Surgical_Robot_for_Posterior_Segment_Ophthalmic_Surgery.pdf)，DOI 10.1109/TASE.2024.3438452 | V，PDF 7–11 页；感知、轨迹处理、坐标关系、整机控制、通信逐项验证；模块结果就近解释。 |
| Yao 等，2025，Sim2Real Learning With Domain Randomization for Autonomous Guidewire Navigation in Robotic-Assisted Endovascular Procedures；[全文](https://rasevents.org/uploads/documents/pdfviewer/5a/af/208178-5269.pdf)，DOI 10.1109/TASE.2025.3555559 | IV–V，PDF 7–11 页；数值比较较密集，按仿真和部署解释差异，再独立讨论。表格逐项复述较多，不作为压缩正文的范本。 |
| Wang 等，2026，TDN-PPO: An Automatic Control Framework of a Surgical Robot for Posterior Segment Ophthalmic Surgery；[出版版入口](https://discovery.ucl.ac.uk/id/eprint/10222653/)，DOI 10.1109/TASE.2026.3671981 | V–VI，PDF 7–11 页；由检测精度到仿真控制、实物控制和时延；技术数值在对应小节解释，结论重复数字较多，不必效仿。 |

补充控制案例：Zhao 等，2024 卷年、2022 首次在线，Reinforcement Learning Control for a 2-DOF Helicopter With State Constraints: Theory and Experiments，DOI 10.1109/TASE.2022.3215738；[全文](https://his.pusan.ac.kr/sites/cogno/2024/2024_260.pdf)，IV，PDF 6–9 页。以响应曲线解释稳态接近、瞬态差异和约束作用，说明少报数也可形成局部分析。其平台是控制试验台，单列为补充，不计入 11 篇机器人主体样本。
