# 来源与迁移记录

仅在询问来源、维护或扩充语料时读取。普通润色不需要重新联网检索。

## 来源类别与范围

- **文献观察**：在实际阅读的论文部分中见到的表达，保留出处与阅读范围。
- **编辑归纳**：17 类通用规则、自编正反例及语言功能句型。它们用于解释选择，不意味着每条都是经过频次统计的期刊规范。
- **原稿教学**：作者要求保留的《Adaptive Speed and Depth Tracking for Hybrid Aerial–Aquatic Vehicle Surface Planing》（2026402288.pdf）片段，见 [正反面案例](style-examples.md)。保留原稿方法名、数字和场景以便理解修改；不将其设置作为下一篇论文的默认内容。
- **个人约定**：公式后解释使用小写 `where`，于 2026-10-29 再次明确为必须采用的形式。它不是 IEEE 对所有作者的强制规则。

新教材的共同语料记录为 2022—2026 年 20 篇摘要、3193 个英文词法单元，另抽读 6 篇正文，覆盖 T-RO、TASE、RA-L、IROS、TAC、Automatica。样本偏向 MPC、学习控制、导航与编队，不是全领域频率研究。文献清单与词形统计说明统一保存在配套词汇技能的 [语料与来源](../../control-paper-vocabulary/references/sources.md)。单独安装本技能时，该来源链接可缺失，不影响已有规则与案例的使用；不自动安装配套技能。

## 从旧 ieee-control-writing 保留的来源

旧技能由以下两篇 TAC 论文的选定部分及编辑归纳形成；迁移时保留出处，不沿用其场景作为通用技术要求。

### R1：定义对象与控制量

T. E. Gibson, Z. Qu, A. M. Annaswamy, and E. Lavretsky, “Adaptive Output Feedback Based on Closed-Loop Reference Models,” IEEE Transactions on Automatic Control, 60(10), 2728–2733, 2015. DOI: 10.1109/TAC.2015.2405295.

[作者全文](https://stuff.mit.edu/people/tgibson/papers/teg_tac_2015.pdf)。旧记录阅读 II、V 节；短语 “The reference system is defined as” 展示先命名对象再引出方程的写法。迁移的是定义与模型描述的表达功能，不是该文的参考模型架构。

### R2：动力学与误差表述

R. Kamalapurkar, B. Reish, G. Chowdhary, and W. E. Dixon, “Concurrent Learning for Parameter Estimation Using Dynamic State-Derivative Estimators,” IEEE Transactions on Automatic Control, 62(7), 3594–3601, 2017. DOI: 10.1109/TAC.2017.2671343.

[作者实验室全文](https://ncr.mae.ufl.edu/papers/TAC17.pdf)。旧记录阅读 II、IV、V 节；短语 “The dynamics of the model are described by” 展示给出被建模对象后连接方程。迁移的条件、推导和实现句式为编辑归纳，不宣称全部逐字出现在该文。

## 本次迁移

2026-10-29：M04 改由本技能承担，去重后保留定义、假设/近似、设计选择、运算/论证、实现/时序、评价/比较、解释/承接七类句式。旧版按章节组织的句式不再独立保留；语言功能已覆盖的部分并入相应类别，章节安排仍由总技能的 M01 负责。旧版完整文本可从仓库历史追溯。

本次是已读材料与既有指南的迁移，未新增大规模语料研究。以后扩充需记录实际阅读的章节和版本，区分摘要观察、正文观察及编辑建议；抽取表达功能并自编示例，不复制长段落。来源文献不自动进入被润色论文的参考文献表。
