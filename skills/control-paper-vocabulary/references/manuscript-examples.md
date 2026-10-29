# 论文原句用词案例

来源：用户论文《Adaptive Speed and Depth Tracking for Hybrid Aerial–Aquatic Vehicle Surface Planing》，文件名 2026402288.pdf。页码为 PDF 物理页码。
原句保留原文，合并排版换行；数学符号采用可读的线性形式。推荐写法是编辑示例。E 为语法/搭配问题，T 为术语或修饰关系问题，P 为可选优化；K 为应保留表达。
按动词、M 编号、K 编号或词库编号查找。

这些原稿正反面教材按作者要求保留。推荐写法中补全的仿真/水池场景、指标名称、参数与范围使用原稿上下文；教学时说明这些前提，不能把补全内容解释成仅凭孤立原句就能推出。新论文复用语言功能和搭配，不继承本案例的方法名、数字或试验设置；无需因阅读案例而核查当前论文的控制器实现。

## M01 couple 与具体技术关系（P）

位置：第 1 页。词库编号：15、47。

- 原句：During planing, vehicle speed affects the hydrodynamic forces, which in turn affect vehicle motion.
- 表达问题：两个 affect 和宽泛的 vehicle motion 使首句较绕；可以直接写出速度与深度的关系。
- 推荐写法：Speed-dependent hydrodynamic forces couple speed and depth during surface planing.
- 场景句式：A couples B and C.
- 使用提示：couple 直接接两个相互关联的量，适合用作问题背景句的核心动词。

## M02 retain / keep fixed 的作用范围（T）

位置：第 1 页。词库编号：29、46。

- 原句：Design parameters tuned at a nominal condition remain fixed during the operating-grid and command-switching tests.
- 表达问题：a nominal condition 与 remain fixed 的作用范围不够直观；分别说明整定场景和固定范围。
- 推荐写法：Design parameters are tuned separately for nominal simulation and pool tracking, then held fixed within each test series.
- 场景句式：Parameters are tuned separately for A and B, then held fixed within each series.
- 使用提示：separately 修饰整定动作，within 修饰固定参数的使用范围。

## M03 tune 与笼统的程度副词（P）

位置：第 1 页。词库编号：29、36。

- 原句：PID is suitably tuned for these nominal tasks.
- 表达问题：suitably 较泛；明确 gains 为 tune 的宾语，搭配更具体。
- 推荐写法：The PID gains are tuned for the nominal simulation and pool-tracking tasks.
- 场景句式：tune controller gains for a task
- 使用提示：tune gains 比 tune a controller 更具体；for 后接任务。

## M04 evaluate 的主语与实验对象（P）

位置：第 1 页。词库编号：35、37。

- 原句：The 25-point simulation grid and pool speed-command changes then evaluate coordinated tracking with the respective design parameters retained.
- 表达问题：grid 和 command changes 是测试设置；以 We 为主语更便于组织评价动作、对象和场景。
- 推荐写法：We then evaluate coordinated tracking over a 25-point simulation grid and during speed-command changes in the pool, while retaining the design parameters tuned for each setting.
- 场景句式：We evaluate performance over a grid and during command changes.
- 使用提示：over 引出覆盖范围，during 引出过程；并列成分采用相同句法层级。

## M05 define / specify 的参考对象（P）

位置：第 2 页。词库编号：10、11。

- 原句：Thus, h = h0 at rest, and a negative ∆hcmd specifies a position above it.
- 表达问题：it 的先行词不够直观；重复 reference level 可减少回读。
- 推荐写法：Thus, h = h0 at rest, and a negative ∆hcmd specifies a position above the stationary reference level.
- 场景句式：specify a position above the reference level
- 使用提示：技术写作可以重复关键名词，清楚的指代比刻意避免重复更重要。

## M06 align 与坐标轴描述（P）

位置：第 2 页。词库编号：11。

- 原句：These inputs are expressed in the level, yaw-aligned frame {H}: xH follows the horizontal heading and zH points downward.
- 表达问题：描述坐标轴方向时，is aligned with 比 follows 更直接。
- 推荐写法：These inputs are expressed in the level, yaw-aligned frame {H}, whose xH-axis is aligned with the horizontal heading and whose zH-axis points downward.
- 场景句式：The x-axis is aligned with the heading.
- 使用提示：be aligned with 表示方向一致，point downward 表示指向。

## M07 terminate / satisfy 的算法条件（P）

位置：第 2 页。词库编号：14、27。

- 原句：Iterations stop when the allocation error meets its tolerance or the maximum iteration count is reached.
- 表达问题：meets its tolerance 可以改成更明确的误差范围表达。
- 推荐写法：The iterations terminate when the allocation error falls within the specified tolerance or the maximum number of iterations is reached.
- 场景句式：Iterations terminate when the error falls within the tolerance.
- 使用提示：terminate when 介绍终止条件；fall within / remain within 与 tolerance 搭配。

## M08 send / apply 与控制接口（P）

位置：第 2 页。词库编号：30、32。

- 原句：The current solution is sent to the actuators.
- 表达问题：solution 在此较抽象；直接写 actuator inputs 能让接口描述更清楚。
- 推荐写法：The actuator inputs from the final iteration are sent to the actuators.
- 场景句式：The actuator inputs from the final iteration are sent to the actuators.
- 使用提示：from the final iteration 紧接被修饰的输入；sent to 表示发送对象。

## M09 express 与量纲说明（P）

位置：第 2 页。词库编号：10、29。

- 原句：Regressors use SI units, and the learning rates have the corresponding units.
- 表达问题：regressors 与 corresponding units 较笼统；components 和 parameter-update law 能明确修饰关系。
- 推荐写法：The regressor components are expressed in SI units, and the learning rates carry the units required by the parameter-update law.
- 场景句式：Quantities are expressed in SI units.
- 使用提示：expressed in 用于单位表达；carry the units required by ... 用于说明量纲关系。

## M10 compute 与代数操作（P）

位置：第 3 页。词库编号：18、26。

- 原句：The controller subtracts this term from the baseline virtual input and divides by the input-effectiveness estimate:
- 表达问题：this term 和省略的被除对象增加回读；compute 加 by 短语可以直接组织计算步骤。
- 推荐写法：The controller computes Fi by subtracting θ̂iᵀφi from Fb,i and dividing the difference by λ̂i:
- 场景句式：compute an input by subtracting A from B and dividing the difference by C
- 使用提示：subtract A from B 表示 B−A；the difference 承接前一个运算结果。

## M11 limit / integrate / project 的顺序（P）

位置：第 3 页。词库编号：26、29、30。

- 原句：It limits and integrates the update rates, projects the estimates, and computes the current virtual inputs using (13).
- 表达问题：连续动作可保留并列结构，并将 limits、rates 和 estimates 分别配给相应动词。
- 推荐写法：The controller applies the update-rate limits, integrates the resulting rates, projects the parameter estimates, and computes the current virtual inputs using (13).
- 场景句式：apply limits → integrate rates → project estimates → compute inputs
- 使用提示：并列动词采用相同形式，动作顺序按原句排列。

## M12 imply 与有条件的有界性（P）

位置：第 3 页。词库编号：20、21、24。

- 原句：Thus, bounded commands and measured states give bounded virtual inputs at every sample.
- 表达问题：give 是可用表达；以公式为主语、implies that 为谓语，公式与后句衔接更直接。
- 推荐写法：For bounded commands and measured states, (18) implies that the virtual inputs remain bounded at every sampling instant.
- 场景句式：For ..., (18) implies that ...
- 使用提示：条件置于句首，公式编号作主语，that 从句写结果。

## M13 use 与 settings 的指代（P）

位置：第 3 页。词库编号：31、46。

- 原句：Both settings use the same control equations; initial estimates are specified below.
- 表达问题：Both settings 的指代需要回查；直接写 Simulation and pool experiments 更易读。
- 推荐写法：Simulation and pool experiments use the same control equations; their initial estimates are specified below.
- 场景句式：A and B use the same control equations.
- 使用提示：用具体对象替代 both settings；same 后紧接要比较的对象。

## M14 report 与统计对象（P）

位置：第 4 页。词库编号：39、40。

- 原句：S2 statistics summarize the RMSE at 25 operating conditions.
- 表达问题：summarize 后没有写明统计项；report the mean and maximum 的宾语更具体。
- 推荐写法：For S2, we report the mean and maximum of the RMSE values across the 25 operating conditions.
- 场景句式：report the mean and maximum of ... across ...
- 使用提示：of 引出被汇总的量，across 引出汇总维度。

## M15 weight 与归一化指标（P）

位置：第 4 页。词库编号：39。

- 原句：Both error terms have equal weights.
- 表达问题：error terms 可以进一步明确为 squared normalized RMSE terms。
- 推荐写法：The squared normalized RMSE terms are weighted equally.
- 场景句式：The squared normalized terms are weighted equally.
- 使用提示：weighted equally 是权重说明的常用搭配；修饰词按运算层次组织。

## M16 compare A with B 的对象平行（E）

位置：第 5 页。词库编号：36、37。

- 原句：At Vd = 1.5 m/s and hd = 0.24 m, with h0 = 0.33 m, we compare ADaST with updating only θ̂ or only λ̂ in both channels.
- 表达问题：比较两侧分别为控制器名称和 updating 动作；改成控制器与 variants 后结构平行。
- 推荐写法：At Vd = 1.5 m/s, hd = 0.24 m, and h0 = 0.33 m, we compare ADaST with two variants that update only θ̂ or only λ̂, respectively, in both channels.
- 场景句式：compare a controller with two variants that ...
- 使用提示：compare A with B 的两侧采用同类语法对象；分别对应时可用 respectively。

## M17 approach 与响应对象（P）

位置：第 5 页。词库编号：24、41。

- 原句：Both tracking responses approach their commands more slowly.
- 表达问题：tracking responses 较抽象；直接用 speed and depth 作主语更简洁。
- 推荐写法：Speed and depth approach their commanded values more slowly.
- 场景句式：A approaches its commanded value.
- 使用提示：approach 直接接宾语；commanded value 适合描述响应趋近的目标。

## M18 remain 与 residual tracking error（T）

位置：第 5 页。词库编号：24、41。

- 原句：The input-effectiveness estimates reach their lower bounds, but speed retains a visible offset; the depth offset is much smaller.
- 表达问题：visible offset 和 much smaller 较依赖读图；分别写两个通道的响应更容易理解。
- 推荐写法：The input-effectiveness estimates reach their lower bounds, but a residual speed-tracking error remains. The depth response stays close to its commanded value.
- 场景句式：A residual tracking error remains.
- 使用提示：residual error 作主语，remains 作谓语；不同物理量可分别成句描述。

## M19 mean error 与 mean RMSE（T）

位置：第 6 页。词库编号：35、36、44。

- 原句：With PID gains suitably tuned for this nominal task, PID and ADaST achieve similar mean tracking errors.
- 表达问题：mean tracking errors 与图表术语不够统一；使用 mean RMSE values 可直接对应指标名称。
- 推荐写法：With PID gains tuned for this nominal task, PID and ADaST achieve similar mean RMSE values in both channels.
- 场景句式：achieve similar mean RMSE values in both channels
- 使用提示：统一正文与图表的指标名称；in both channels 说明描述对象。

## M20 show 的对象与 both 的指代（P）

位置：第 6 页。词库编号：40、41。

- 原句：Fig. 9 shows both trials from initialization to stopping, with the command change at time zero.
- 表达问题：shows both trials 的宾语较泛；明确展示的是 parameter estimates，并写出试验名称。
- 推荐写法：Fig. 9 shows the ADaST parameter estimates for the plotted E2a and E2b trials from initialization to stopping, with the command change at time zero.
- 场景句式：A figure shows parameter estimates for the plotted trials.
- 使用提示：图表句常以 Fig. X 为主语；shows 后写图中展示的量。

## M21 reflect / achieve 与联合指标范围（P）

位置：第 6 页。词库编号：39、44、45。

- 原句：Relative to each command scale, the lower mean J reflects improved coordinated tracking in these trials, with the design parameters retained from E1.
- 表达问题：尺度、指标和参数设置挤在同一句里；可以先交代设置，再陈述指标结果。
- 推荐写法：With the E1 design parameters unchanged, ADaST achieves a lower mean J in both E2 cases under the channel normalization in (22).
- 场景句式：With ... unchanged, the method achieves a lower mean J.
- 使用提示：with 短语提供背景，主句突出方法和指标。

## M22 achieve / yield 与条件限定（P）

位置：第 1 页。词库编号：44、45。

- 原句：Both controllers keep mean speed RMSE below 0.25 m/s.
- 表达问题：结果句补上 In this test，可让工况指代就近明确。
- 推荐写法：In this speed-increase test, both controllers achieve a mean speed RMSE below 0.25 m/s.
- 场景句式：In this test, both controllers achieve a mean RMSE below ...
- 使用提示：条件短语放在句首，指标和阈值放在句末。

## M23 fixed parameters 与比较范围（T）

位置：第 7 页。词库编号：29、39、45、46。

- 原句：ADaST reduces mean and maximum simulation RMSE and pool-test depth deviations while maintaining speed tracking, with fixed parameters within each test setting.
- 表达问题：fixed parameters 的中心词较宽；明确 design parameters，并将较长句拆成结果与设置两句。
- 推荐写法：Relative to PID, ADaST reduces the mean and maximum per-condition RMSE across the 25 simulated operating points and the mean depth RMSE in both pool speed-command-change tests. The controller design parameters remain fixed within the simulation series and within the pool-experiment series.
- 场景句式：Relative to B, A reduces [metric] across [conditions].
- 使用提示：relative to 引出比较对象，across 引出工况范围；固定对象用完整名词短语。

## M24 update 与 nominalization（P）

位置：第 1 页。词库编号：29、30。

- 原句：Adaptive compensation and input-effectiveness estimation are performed in the outer loops, before nonlinear allocation.
- 表达问题：are performed 是泛化动作；以 outer loops 为主语、update 为谓语，句子更直接。
- 推荐写法：The outer loops update the adaptive compensation parameters and input-effectiveness estimates before nonlinear control allocation.
- 场景句式：The outer loops update parameters before control allocation.
- 使用提示：模块可以作主语；update 与 parameters / estimates 搭配。

## K01 保留案例

位置：第 1 页。

- 正例：We develop an Adaptive Depth and Speed Tracking (ADaST) controller for a hybrid aerial–aquatic vehicle (HAAV).
- 保留理由：develop a controller 是介绍控制器的常用搭配，当前句式已经简洁。
- 不推荐的编辑：仅为换词而将 develop 改成 present，再堆叠多个评价形容词。

## K02 保留案例

位置：第 2 页。

- 正例：The combined virtual control input vector is defined as
- 保留理由：is defined as 是公式前常用定义句式，相邻定义句可以重复。
- 不推荐的编辑：为避免重复改成 is elegantly manifested as。

## K03 保留案例

位置：第 2 页。

- 正例：We use the following regressor functions:
- 保留理由：use 简洁自然；following 放在名词前，引出后续公式或列表。
- 不推荐的编辑：用 utilize 或 employ 机械替换每个 use。

## K04 保留案例

位置：第 2 页。

- 正例：In the pool experiments, we compute ḣ̂ by differentiating motion-capture depth measurements over a sliding window of 10 samples.
- 保留理由：compute + 估计量，by + 计算方式，over + 窗口，句子组织清楚。
- 不推荐的编辑：改成 The computational acquisition of ... is performed，增加名词化结构。

## K05 保留案例

位置：第 2 页。

- 正例：The constant term accounts for trim forces.
- 保留理由：accounts for + 因素，主语与宾语具体，句子短而完整。
- 不推荐的编辑：写成 accounts trim forces，漏掉介词 for。

## K06 保留案例

位置：第 3 页。

- 正例：The reference-model states are not reset at E2 command changes.
- 保留理由：not reset 直接说明初始化行为，否定句也是正常的技术说明句式。
- 不推荐的编辑：为统一肯定句写成 remain in a non-reinitialized state。

## K07 保留案例

位置：第 6 页。

- 正例：Both intervals span zero, indicating no statistically significant difference in mean J between the two controllers given five trials per controller and condition.
- 保留理由：indicating 引出对前句的解释，given 引出条件；此处教学的是衔接方式。
- 不推荐的编辑：改成 which indicates which means，使从句层层嵌套。

## K08 保留案例

位置：第 7 页。

- 正例：Time zero marks the command change. Colored vertical dotted lines mark stopping times; faded post-stop samples are excluded from RMSE.
- 保留理由：图注分别交代时间原点、线型和样本范围；marks 和 are excluded from 各有明确对象。
- 不推荐的编辑：把短句合成多个 which 串联的长句。
