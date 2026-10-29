# 通用写作习惯正反例

案例按句法和文风组织，不按论文章节组织。E 表示语法/搭配问题，T 表示术语/修饰关系问题，P 表示可选优化。
原稿案例来自用户论文《Adaptive Speed and Depth Tracking for Hybrid Aerial–Aquatic Vehicle Surface Planing》（2026402288.pdf）；页码是 PDF 物理页码。

作者要求保留原稿作为正反面教材。推荐写法中补全的试验场景、信号名称、指标和范围依赖原稿上下文，不能仅凭所列孤立原句推出，也不能套到其他论文。将“明确修饰对象、保持比较平行”等语言经验迁移到新稿；方法名、数字、参数设置和操作流程保留在本案例中。

## 01 修饰范围（T）

原稿第 1 页，案例 M02。

- 原句：Design parameters tuned at a nominal condition remain fixed during the operating-grid and command-switching tests.
- 表达问题：a nominal condition 与 remain fixed 的作用范围不够直观；分别说明整定场景和固定范围。
- 推荐写法：Design parameters are tuned separately for nominal simulation and pool tracking, then held fixed within each test series.
- 写作规则：separately 修饰整定动作，within 修饰固定参数的使用范围。

## 02 主语与动作（P）

原稿第 1 页，案例 M04。

- 原句：The 25-point simulation grid and pool speed-command changes then evaluate coordinated tracking with the respective design parameters retained.
- 表达问题：grid 和 command changes 是测试设置；以 We 为主语更便于组织评价动作、对象和场景。
- 推荐写法：We then evaluate coordinated tracking over a 25-point simulation grid and during speed-command changes in the pool, while retaining the design parameters tuned for each setting.
- 写作规则：over 引出覆盖范围，during 引出过程；并列成分采用相同句法层级。

## 03 代词先行词（P）

原稿第 2 页，案例 M05。

- 原句：Thus, h = h0 at rest, and a negative ∆hcmd specifies a position above it.
- 表达问题：it 的先行词不够直观；重复 reference level 可减少回读。
- 推荐写法：Thus, h = h0 at rest, and a negative ∆hcmd specifies a position above the stationary reference level.
- 写作规则：技术写作可以重复关键名词，清楚的指代比刻意避免重复更重要。

## 04 明确名词修饰关系（P）

原稿第 2 页，案例 M09。

- 原句：Regressors use SI units, and the learning rates have the corresponding units.
- 表达问题：regressors 与 corresponding units 较笼统；components 和 parameter-update law 能明确修饰关系。
- 推荐写法：The regressor components are expressed in SI units, and the learning rates carry the units required by the parameter-update law.
- 写作规则：expressed in 用于单位表达；carry the units required by ... 用于说明量纲关系。

## 05 并列动作（P）

原稿第 3 页，案例 M11。

- 原句：It limits and integrates the update rates, projects the estimates, and computes the current virtual inputs using (13).
- 表达问题：连续动作可保留并列结构，并将 limits、rates 和 estimates 分别配给相应动词。
- 推荐写法：The controller applies the update-rate limits, integrates the resulting rates, projects the parameter estimates, and computes the current virtual inputs using (13).
- 写作规则：并列动词采用相同形式，动作顺序按原句排列。

## 06 both 的指代（P）

原稿第 3 页，案例 M13。

- 原句：Both settings use the same control equations; initial estimates are specified below.
- 表达问题：Both settings 的指代需要回查；直接写 Simulation and pool experiments 更易读。
- 推荐写法：Simulation and pool experiments use the same control equations; their initial estimates are specified below.
- 写作规则：用具体对象替代 both settings；same 后紧接要比较的对象。

## 07 修饰层次（P）

原稿第 4 页，案例 M15。

- 原句：Both error terms have equal weights.
- 表达问题：error terms 可以进一步明确为 squared normalized RMSE terms。
- 推荐写法：The squared normalized RMSE terms are weighted equally.
- 写作规则：weighted equally 是权重说明的常用搭配；修饰词按运算层次组织。

## 08 比较对象平行（E）

原稿第 5 页，案例 M16。

- 原句：At Vd = 1.5 m/s and hd = 0.24 m, with h0 = 0.33 m, we compare ADaST with updating only θ̂ or only λ̂ in both channels.
- 表达问题：比较两侧分别为控制器名称和 updating 动作；改成控制器与 variants 后结构平行。
- 推荐写法：At Vd = 1.5 m/s, hd = 0.24 m, and h0 = 0.33 m, we compare ADaST with two variants that update only θ̂ or only λ̂, respectively, in both channels.
- 写作规则：compare A with B 的两侧采用同类语法对象；分别对应时可用 respectively。

## 09 术语一致性（T）

原稿第 6 页，案例 M19。

- 原句：With PID gains suitably tuned for this nominal task, PID and ADaST achieve similar mean tracking errors.
- 表达问题：mean tracking errors 与图表术语不够统一；使用 mean RMSE values 可直接对应指标名称。
- 推荐写法：With PID gains tuned for this nominal task, PID and ADaST achieve similar mean RMSE values in both channels.
- 写作规则：统一正文与图表的指标名称；in both channels 说明描述对象。

## 10 图表句宾语（P）

原稿第 6 页，案例 M20。

- 原句：Fig. 9 shows both trials from initialization to stopping, with the command change at time zero.
- 表达问题：shows both trials 的宾语较泛；明确展示的是 parameter estimates，并写出试验名称。
- 推荐写法：Fig. 9 shows the ADaST parameter estimates for the plotted E2a and E2b trials from initialization to stopping, with the command change at time zero.
- 写作规则：图表句常以 Fig. X 为主语；shows 后写图中展示的量。

## 11 背景与主句的信息顺序（P）

原稿第 6 页，案例 M21。

- 原句：Relative to each command scale, the lower mean J reflects improved coordinated tracking in these trials, with the design parameters retained from E1.
- 表达问题：尺度、指标和参数设置挤在同一句里；可以先交代设置，再陈述指标结果。
- 推荐写法：With the E1 design parameters unchanged, ADaST achieves a lower mean J in both E2 cases under the channel normalization in (22).
- 写作规则：with 短语提供背景，主句突出方法和指标。

## 12 完整名词与拆句（T）

原稿第 7 页，案例 M23。

- 原句：ADaST reduces mean and maximum simulation RMSE and pool-test depth deviations while maintaining speed tracking, with fixed parameters within each test setting.
- 表达问题：fixed parameters 的中心词较宽；明确 design parameters，并将较长句拆成结果与设置两句。
- 推荐写法：Relative to PID, ADaST reduces the mean and maximum per-condition RMSE across the 25 simulated operating points and the mean depth RMSE in both pool speed-command-change tests. The controller design parameters remain fixed within the simulation series and within the pool-experiment series.
- 写作规则：relative to 引出比较对象，across 引出工况范围；固定对象用完整名词短语。

## 13 减少名词化

以下为自编语言示例。

- 原句：The estimation of the disturbance is carried out by the observer.
- 推荐写法：The observer estimates the disturbance.
- 写作规则：把 estimation is carried out 改成 estimates，缩短主谓结构。

## 14 主动与被动均可

以下为自编语言示例。

- 原句：The control input is computed using (12).
- 推荐写法：保留原句；若需要突出作者动作，也可写 We compute the control input using (12).
- 写作规则：语态按信息重点选择，不强制一律改为主动句。

## 15 公式后的符号解释

以下为自编语言示例。

- 原句：u = −Ke. Here, K is the feedback gain.
- 推荐写法：u = −Ke, where K is the feedback gain.
- 写作规则：按本技能统一约定，公式后的符号解释必须用小写 where 接续同一句，并调整公式末尾标点；此处不保留独立 Here 句。

## 16 过去操作与当前图表

以下为自编语言示例。

- 原句：We conducted five trials. Fig. 3 showed the mean response.
- 推荐写法：We conducted five trials. Fig. 3 shows the mean response.
- 写作规则：已完成的操作用过去时，读者当前可见的图表可用现在时。

## 17 压缩图表套话

以下为自编语言示例。

- 原句：It can be clearly seen from Fig. 3 that the response has oscillations.
- 推荐写法：Fig. 3 shows oscillations in the response.
- 写作规则：用图表作主语，直接连接显示内容。

## 18 区分起点、终点与变化量

以下为自编语言示例，必须先区分终值与下降量。

- 已知起点为 0.10 m、终值为 0.08 m：The mean error decreases from 0.10 m to 0.08 m.
- 同一变化也可写：The mean error decreases by 0.02 m, from 0.10 m to 0.08 m.
- 若下降量为 0.08 m：The mean error decreases from 0.10 m by 0.08 m. 此时终值为 0.02 m，这句话本身没有语法错误。
- 写作规则：to 后接终值，by 后接变化量，不能在没有给定目标含义时直接互换。本例替代此前将 by 直接改成 to 的教学。

## 自然表达的保留

### K02，原稿第 2 页

- 原句：The combined virtual control input vector is defined as
- 保留理由：is defined as 是公式前常用定义句式，相邻定义句可以重复。
- 不推荐的编辑：为避免重复改成 is elegantly manifested as。

### K03，原稿第 2 页

- 原句：We use the following regressor functions:
- 保留理由：use 简洁自然；following 放在名词前，引出后续公式或列表。
- 不推荐的编辑：用 utilize 或 employ 机械替换每个 use。

### K06，原稿第 3 页

- 原句：The reference-model states are not reset at E2 command changes.
- 保留理由：not reset 直接说明初始化行为，否定句也是正常的技术说明句式。
- 不推荐的编辑：为统一肯定句写成 remain in a non-reinitialized state。

### K08，原稿第 7 页

- 原句：Time zero marks the command change. Colored vertical dotted lines mark stopping times; faded post-stop samples are excluded from RMSE.
- 保留理由：图注分别交代时间原点、线型和样本范围；marks 和 are excluded from 各有明确对象。
- 不推荐的编辑：把短句合成多个 which 串联的长句。
