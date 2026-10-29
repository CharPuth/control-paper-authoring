# 语料与来源

本 Skill 由本次控制与机器人论文写作教材整理，词汇规则结合样本用法与语言编辑归纳。场景补充词不等于摘要高频词排名。

2026-10-29 迁移说明：在原 48 组之外，从旧 ieee-control-writing 保留 choose/select、measure/store、regulate/track 三组及尚未重复覆盖的用词区分，合计 51 组。这些补充属于编辑归纳，不加入下列 20 篇摘要的频次统计。旧技能两篇 TAC 来源在配套写作习惯技能的 [来源记录](../../control-paper-writing-style/references/sources.md) 中保留；该链接只用于溯源，不是独立使用本词库的必需依赖。

原稿教学例来自作者提供的 2026402288.pdf，按作者要求保留在 [论文原句案例](manuscript-examples.md)，不计入 20 篇摘要统计。公式后用小写 where 属于作者文风约定，不是从词频推导出的规范。本次迁移没有新增大规模检索。

语料：2022—2026 五个自然年，检索截至 2026-10-29。T-RO 4 篇、TASE 4 篇、RA-L 3 篇、IROS 3 篇、TAC 3 篇、Automatica 3 篇。IROS 为会议。
统计使用 20 篇摘要，共 3193 个英文词法单元；另抽读 6 篇正文。样本按主题选取，词形统计未做词性标注，不能作为全领域排名。

摘要中的篇章覆盖：use 14/20，propose 13/20，show 与 demonstrate 各 8/20，achieve 与 introduce 各 7/20。其余词按场景保留，不按这一小样本排除。

# 文献使用示例

下面只摘录极短词组，其余为写作功能分析。教学例句不是这些文献原句。

S02，T-RO 2024：摘要同时承担方法介绍、动力学形式化和硬件验证。其用词随动作切换，不能把一段中所有动词统一成 propose。来源：https://arxiv.org/abs/2107.05616

S05，TASE 2025：摘要的 “computed by solving” 区分了控制输入的计算和优化问题的求解；“validated through numerical simulations” 明确验证方式。来源：https://iris.uniroma1.it/retrieve/c680db9e-a68e-4c8f-8943-c5a42cc80962/Menegatti_Tractable-Data-Driven_2025.pdf

S09，RA-L 2023：摘要用 show 引出控制器组合的收敛性质，用 validate 描述仿真和实物验证。两者取决于该句的任务，不能规定 show 只讲实验事实。来源：https://ieeexplore.ieee.org/abstract/document/10255119

S15，TAC 2022：摘要中的 “We prove that our MPC scheme” 对应有条件的闭环性质；正文推导中的 “this yields” 对应公式衔接。这种结构将条件、数学结论和运算步骤分别表达。来源：https://arxiv.org/abs/2105.08567

S19，Automatica 2023：摘要使用 “is demonstrated under assumptions”，其对象是参数收敛。demonstrate 并不是“仅限实验”的标签。来源：https://arxiv.org/abs/2211.09275

S20，Automatica 2024：account for 对应把感知不确定性和控制动作对感知质量的影响纳入方法；establish 对应约束满足和稳定性质。来源：https://www.sciencedirect.com/science/article/pii/S000510982300585X

S04，T-RO 2026，提前在线于 2025：正文中的 “To quantify the robustness of these policies” 后接实际扰动参数变化、部署方式和成功率定义。可借鉴 quantify + 性质，以及随后交代指标的段落安排。来源：https://rpg.ifi.uzh.ch/docs/TRO25_ACMPC_Romero.pdf

## 文献列表

S01 T-RO 2022 — A Comparative Study of Nonlinear MPC and Differential-Flatness-Based Control for Quadrotor Agile Flight. DOI: 10.1109/TRO.2022.3177279. https://arxiv.org/abs/2109.01365
S02 T-RO 2024 — Fast Contact-Implicit Model Predictive Control. DOI: 10.1109/TRO.2024.3351554. https://arxiv.org/abs/2107.05616
S03 T-RO 2025 — Structure-Exploiting Sequential Quadratic Programming for Model-Predictive Control. DOI: 10.1109/TRO.2025.3595674. https://ieeexplore.ieee.org/document/11112619/
S04 T-RO 2026（2025 提前在线）— Actor-Critic Model Predictive Control: Differentiable Optimization Meets Reinforcement Learning for Agile Flight. DOI: 10.1109/TRO.2025.3644945. https://rpg.ifi.uzh.ch/docs/TRO25_ACMPC_Romero.pdf
S05 TASE 2025（2024 提前在线）— Tractable Data-Driven Model Predictive Control Using One-Step Neural Networks Predictors. DOI: 10.1109/TASE.2024.3453668. https://iris.uniroma1.it/retrieve/c680db9e-a68e-4c8f-8943-c5a42cc80962/Menegatti_Tractable-Data-Driven_2025.pdf
S06 TASE 2025（DOI 为 2024）— Learning Control Affine Neural NARX Models for Internal Model Control Design. DOI: 10.1109/TASE.2024.3479321. https://arxiv.org/abs/2402.05607 。本次计数采用 arXiv v2 摘要，该预印本版本的题名与发表题名不同。
S07 TASE 2025（2024 提前在线）— Data-Efficient Learning Control of Continuum Robots in Constrained Environments. DOI: 10.1109/TASE.2024.3357816. https://scholars.cityu.edu.hk/en/publications/data-efficient-learning-control-of-continuum-robots-in-constraine/
S08 TASE 2026（2025 提前在线）— Event-Triggered Safety Control Strategy in Learning-Based Model Predictive Control of Partially Unknown Nonlinear System. DOI: 10.1109/TASE.2025.3633240. https://doi.org/10.1109/TASE.2025.3633240
S09 RA-L 2023 — Combined Leaderless Control of Translational, Shape-Preserving, and Affine Multirobot Formations. DOI: 10.1109/LRA.2023.3316889. https://ieeexplore.ieee.org/abstract/document/10255119
S10 RA-L 2026 — Learning Context-Aware Neural ODE Dynamics for Adaptive Robotic Control. DOI: 10.1109/LRA.2026.3701574. https://research.aalto.fi/en/publications/learning-context-aware-neural-ode-dynamics-for-adaptive-robotic-c/
S11 RA-L 2026 — Smooth Feedback Motion Planning With Reduced Curvature. DOI: 10.1109/LRA.2026.3682600. https://oulurepo.oulu.fi/bitstream/handle/10024/61724/nbnfioulu-202604132573.pdf?sequence=1
S12 IROS 2022 — Learning Enabled Fast Planning and Control in Dynamic Environments with Intermittent Information. DOI: 10.1109/IROS47612.2022.9981508. https://ieeexplore.ieee.org/document/9981508/
S13 IROS 2024 — Neural Control Barrier Functions for Safe Navigation. 录用信息见 arXiv Comments：https://arxiv.org/abs/2407.19907
S14 IROS 2025 — Disturbance Observer-based Control Barrier Functions with Residual Model Learning for Safe Reinforcement Learning. https://publications.ri.cmu.edu/disturbance-observer-based-control-barrier-functions-with-residual-model-learning-for-safe-reinforcement-learning-2
S15 TAC 2022 — Linear Tracking MPC for Nonlinear Systems Part II: The Data-Driven Case. DOI: 10.1109/TAC.2022.3166851. https://arxiv.org/abs/2105.08567
S16 TAC 2023（2022 提前在线）— Bridging Direct and Indirect Data-Driven Control Formulations via Regularizations and Relaxations. DOI: 10.1109/TAC.2022.3148374. https://ieeexplore.ieee.org/document/9705109/
S17 TAC 2023（2022 提前在线）— On a Stochastic Fundamental Lemma and Its Use for Data-Driven Optimal Control. DOI: 10.1109/TAC.2022.3232442. https://arxiv.org/abs/2111.13636
S18 Automatica 2022 — Data-driven control via Petersen’s lemma. DOI: 10.1016/j.automatica.2022.110537. https://pure.rug.nl/ws/portalfiles/portal/236636177/1_s2.0_S0005109822003983_main.pdf
S19 Automatica 2023 — Robust adaptive model predictive control with persistent excitation conditions. DOI: 10.1016/j.automatica.2023.110959. https://arxiv.org/abs/2211.09275
S20 Automatica 2024（DOI 为 2023）— Perception-aware model predictive control for constrained control in unknown environments. DOI: 10.1016/j.automatica.2023.111418. https://www.sciencedirect.com/science/article/pii/S000510982300585X
