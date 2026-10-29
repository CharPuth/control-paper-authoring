# TASE 实验叙事的来源记录

只在核查来源或扩充写作样本时读取。组织规则由当前领域配置的 M07 维护。以下为原技能保留的定向阅读记录，本次模块化没有重新核验这些论文。

## 依据及适用范围


2026-10-13 对下列 11 篇 TASE 机器人论文的验证章节进行了定向阅读，并以 1 篇直升机控制论文作补充。主要选取 2024–2026 卷年或在线发表的工作；卷年与首次在线年份可能不同。这是便于核查的写作样本，不是对全刊的随机抽样或期刊强制规则。公开录用稿与出版版在分页和文字上可能有差异，复查时以所列版本为准。

样本同时包含仿真与实物分章、合并验证章、先列实验再独立分析结果、仿真案例研究。常见做法是在结果附近给出具体解释；部分实验主要依靠曲线中的行为，部分依靠数值比较。同一篇论文可混用。独立 Discussion、小节总结、逐项报数均不是统一要求。发表过的论文也可能冗长或有过度解释；只借鉴有用的组织方式，不复制其措辞或未经核实的因果判断。


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
