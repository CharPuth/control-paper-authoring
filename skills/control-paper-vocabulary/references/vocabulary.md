# 控制论文常用词汇与使用场景

按研究动作选择词组。01–09 为问题和方案，10–16 为建模和定义，17–25 为推导和性质，26–34 为计算和实现，35–48 为评价和结果；49–51 为旧技能迁入的设计选择、测量/存储与调节表达。
以下正例为语言教学示例。通用正反例见 [contrastive-examples.md](contrastive-examples.md)，论文原句正反例见 [manuscript-examples.md](manuscript-examples.md)。

## 01 address — address a problem/challenge/limitation；处理明确问题，不自动意味着彻底解决。

- 使用场景：陈述所处理的研究问题。
- 正例：We address trajectory tracking under bounded input disturbances.
- 搭配提示：address 为及物动词，直接接 problem / challenge，不接 to。

## 02 consider / study / investigate — consider a system/problem；study a property；investigate the effect of X on Y。

- 使用场景：引入研究对象或考察某因素的影响。
- 正例：We investigate the effect of sensor delay on tracking accuracy.
- 搭配提示：consider 引入研究对象；investigate the effect of X on Y 用于研究因素影响。

## 03 propose — propose a controller/method/framework/algorithm；提出本文方案。

- 使用场景：介绍所提出的控制器或算法。
- 正例：We propose an observer-based controller for flexible manipulators.
- 搭配提示：propose 后常接 controller / method / algorithm；性质常与 analyze / establish 搭配。

## 04 present — present an approach/analysis/comparison/result；介绍本文内容或工作。

- 使用场景：介绍方法、分析或比较内容。
- 正例：This paper presents an experimental comparison of two tracking controllers.
- 搭配提示：present 后可接 approach、analysis、comparison 或 results，适合介绍论文内容。

## 05 introduce — introduce a variable/constraint/mechanism/formulation；把新对象纳入叙事或方案。

- 使用场景：引入变量、约束或机制。
- 正例：We introduce a slack variable to relax the terminal constraint.
- 搭配提示：introduce 常接 variable、constraint、mechanism，表示把某对象引入当前表述。

## 06 develop / design / synthesize — develop a framework；design a controller；synthesize a controller from LMIs/data。

- 使用场景：描述控制器设计或构造性求解。
- 正例：We synthesize a state-feedback controller by solving a semidefinite program.
- 搭配提示：design 常接 controller；synthesize 常与构造性求解过程同句。

## 07 extend / generalize — extend a method to a new system class；generalize a result。

- 使用场景：描述方法适用对象或结果的扩展。
- 正例：We extend the formulation to systems with bounded disturbances.
- 搭配提示：extend A to B 表示拓展应用范围；generalize a result 表示推广结果。

## 08 combine / integrate / incorporate — combine A with B；integrate A into B；incorporate constraints into a formulation。

- 使用场景：说明模块组合与因素纳入。
- 正例：The formulation incorporates actuator limits into the optimization problem.
- 搭配提示：combine A with B；integrate A into B；incorporate A into B。

## 09 enable / allow — enable a capability；enable the robot to perform a task；allow for model updates。

- 使用场景：描述某机制使一项操作得以进行。
- 正例：The reduced model enables online trajectory optimization.
- 搭配提示：enable + 对象 + to do；allow for + 名词；allow + 对象 + to do。

## 10 define / denote — define a quantity as；a symbol denotes an object。

- 使用场景：定义量、符号及其含义。
- 正例：The tracking error is defined as e = y − r, where r denotes the reference output.
- 搭配提示：define A as B；A is defined as B；符号解释常用 denotes。

## 11 model / describe / represent — model A as B；the dynamics are described by；represent a set using inequalities。

- 使用场景：描述动力学模型或集合表示。
- 正例：The actuator dynamics are modeled as a first-order system.
- 搭配提示：model A as B；描述方程常用 be described by，描述集合常用 represent。

## 12 formulate / cast — formulate a task as an optimization problem；cast constraints as LMIs。

- 使用场景：把任务写成数学或优化问题。
- 正例：We formulate trajectory tracking as a constrained optimal control problem.
- 搭配提示：formulate a task as a problem；cast a problem into a form，宾语通常为问题或任务。

## 13 assume / suppose / let — assume a physical/mathematical condition；let 引入对象；suppose 用于论证。

- 使用场景：引入假设、条件或符号。
- 正例：We assume that the disturbance is bounded by a known constant.
- 搭配提示：assume that 接条件从句；let 引入符号；under Assumption X 引出条件。

## 14 satisfy / fulfill — a signal satisfies a bound；a model satisfies an assumption；fulfill requirements。

- 使用场景：描述信号或模型满足的条件。
- 正例：The initial state satisfies x₀ ∈ X.
- 搭配提示：系统、变量或信号作主语时可用 satisfy；算法施加条件时可用 impose。

## 15 account for / capture — account for a factor in a model/design；capture dominant dynamics。

- 使用场景：说明模型所考虑的因素或描述的动态。
- 正例：The prediction model accounts for actuator lag.
- 搭配提示：account for 接所考虑的因素；capture 常接 dynamics / behavior。

## 16 estimate / identify / approximate — estimate a state/disturbance；identify model parameters；approximate a function。

- 使用场景：描述状态估计、参数辨识或函数近似。
- 正例：The observer estimates the external torque from encoder measurements.
- 搭配提示：estimate 常接 state / disturbance；identify 常接 parameters；approximate 常接 function。

## 17 derive — derive error dynamics/a bound/a condition/an update law from given relations。

- 使用场景：由已有关系推导公式或条件。
- 正例：We derive the error dynamics by substituting the control law into the plant model.
- 搭配提示：derive A from B；derive A by substituting ...，写明推导对象。

## 18 obtain / yield / give — obtain a result；an operation yields/gives a result。

- 使用场景：衔接计算操作及其结果。
- 正例：Substituting (4) into (7) yields the closed-loop error dynamics.
- 搭配提示：以操作为主语用 yields / gives，以作者为主语用 obtain，按句法选择。

## 19 rewrite / rearrange / substitute — rewrite an equation；rearrange terms；substitute A into B。

- 使用场景：说明公式变形与代入步骤。
- 正例：Rearranging (8) gives an upper bound on the tracking error.
- 搭配提示：substitute A into B；rearrange terms；rewrite an expression as ...。

## 20 follow / imply — it follows from A that B；A implies B。

- 使用场景：衔接引理、公式及其后续结论。
- 正例：It follows from Lemma 1 that the feasible set is forward invariant.
- 搭配提示：It follows from A that B；A implies that B，两者均可用于公式衔接。

## 21 bound / upper-bound / lower-bound — bound the error；upper-bound the residual term。

- 使用场景：描述某个量的上界、下界或范围。
- 正例：The residual term is bounded by ε on the operating domain.
- 搭配提示：be bounded by 后接界；on / over 后接定义域；within 后可接范围。

## 22 prove / establish / show — prove a theorem/that-clause；establish stability/a sufficient condition；show that。

- 使用场景：陈述数学论证及性质。
- 正例：Under Assumptions 1–3, we prove local exponential stability of the equilibrium.
- 搭配提示：prove 后接 theorem 或 that 从句；establish 后接 stability / conditions；show that 用途较广。

## 23 ensure / guarantee — ensure feasibility/stability/constraint satisfaction，在给定条件下成立。

- 使用场景：描述条件与可行性或约束满足的关系。
- 正例：The terminal condition ensures recursive feasibility under Assumption 2.
- 搭配提示：ensure / guarantee 后常接 feasibility、stability、constraint satisfaction；句首可用 under 引出条件。

## 24 stabilize / converge / remain — stabilize an equilibrium；the error converges to zero/a neighborhood；signals remain bounded。

- 使用场景：描述平衡点稳定、响应趋近或信号有界。
- 正例：The tracking error converges to a neighborhood of the origin.
- 搭配提示：converge to zero / a neighborhood；remain bounded；stabilize an equilibrium。

## 25 characterize — characterize a set/relationship/region of attraction。

- 使用场景：描述集合、结构或关系。
- 正例：Theorem 2 characterizes the set of admissible initial states.
- 搭配提示：characterize 常接 set、relationship、region，用于描述结构或范围。

## 26 compute / calculate / evaluate — compute a gradient/control input；calculate a metric；evaluate a function at x。

- 使用场景：计算数值量、输入或函数值。
- 正例：At each sampling instant, we compute the control input from the estimated state.
- 搭配提示：compute 后接量；evaluate a function at x 表示在指定点求值。

## 27 solve / minimize / optimize — solve a QP；minimize a cost；optimize a trajectory subject to constraints。

- 使用场景：求解方程、优化问题或代价函数。
- 正例：We solve the quadratic program at each sampling instant.
- 搭配提示：solve a problem / equation；minimize a cost；compute the resulting input。

## 28 enforce / impose / constrain — enforce bounds；impose a terminal condition；constrain inputs to a set。

- 使用场景：说明输入约束与可行集合。
- 正例：We impose box constraints on the actuator commands.
- 搭配提示：impose constraints on inputs；constrain inputs to a set；enforce bounds。

## 29 update / adapt / tune — update an estimate；adapt parameters online；tune controller gains。

- 使用场景：描述参数整定和在线更新。
- 正例：The parameter estimate is updated using the latest measurements.
- 搭配提示：tune gains；update estimates；adapt parameters，按宾语选择。

## 30 implement / deploy / apply — implement an algorithm on hardware；deploy a policy on a robot；apply a method to a system。

- 使用场景：描述算法实现、部署和应用。
- 正例：The controller is implemented on the onboard computer.
- 搭配提示：implement on a computer；deploy on a robot；apply a method to a system。

## 31 use / employ — use an observer；employ a solver，两者均可。

- 使用场景：交代所用工具、模型或求解器。
- 正例：We use a low-pass filter to attenuate measurement noise.
- 搭配提示：use 和 employ 均可；use 通常更简洁，不需要全篇替换。

## 32 generate / produce / track — generate a reference trajectory；produce a control command；track a reference。

- 使用场景：描述参考生成、指令输出和轨迹跟踪。
- 正例：The planner generates a reference trajectory, which the controller tracks.
- 搭配提示：generate a trajectory；produce a command；track a reference，分别描述生成与跟踪。

## 33 compensate for / reject / attenuate / suppress — compensate for a modeled effect；reject a disturbance；attenuate noise；suppress oscillations。

- 使用场景：描述补偿、扰动抑制或噪声衰减。
- 正例：The feedback term attenuates the effect of measurement noise on the control input.
- 搭配提示：compensate for 中 for 不省略；attenuate noise、suppress oscillations 是常见搭配。

## 34 exploit / reduce — exploit sparsity/structure；reduce computational cost。

- 使用场景：说明如何利用结构或降低计算量。
- 正例：The solver exploits the block structure of the Hessian.
- 搭配提示：exploit 后接具体结构；reduce 后接成本、时间或误差等量。

## 35 evaluate / assess — evaluate performance；assess sensitivity/robustness under specified tests。

- 使用场景：介绍性能评价对象及指标。
- 正例：We evaluate tracking accuracy using the root-mean-square error.
- 搭配提示：evaluate / assess 后接性能对象；using 引出指标，under 引出条件。

## 36 compare / benchmark — compare A with B in terms of a metric；benchmark A against named baselines。

- 使用场景：比较控制器或基线方法。
- 正例：We compare the controller with two baselines under the same input limits.
- 搭配提示：compare A with B；benchmark A against B；in terms of 引出指标。

## 37 test / conduct / perform — test a controller；conduct experiments；perform an ablation study。

- 使用场景：说明试验、实验和分析操作。
- 正例：We conduct experiments with three payload masses.
- 搭配提示：conduct experiments；perform an analysis / ablation study；test a controller。

## 38 demonstrate / validate / verify — demonstrate a capability；validate an approach through experiments；verify a condition/property against a stated criterion。

- 使用场景：描述能力展示、方法验证或性质检查。
- 正例：Hardware experiments demonstrate the controller’s ability to recover after the applied push.
- 搭配提示：demonstrate a capability；validate an approach；verify a condition，按句子任务和宾语选择。

## 39 quantify — quantify an effect using a metric。

- 使用场景：用指标表达某个效应或性质。
- 正例：We quantify disturbance sensitivity using the peak tracking error after the applied pulse.
- 搭配提示：quantify X using Y，Y 通常是指标或量化方式。

## 40 show / report / summarize — a figure shows；a table reports numerical values；a table summarizes comparisons。

- 使用场景：引出图表内容、数值及比较结果。
- 正例：Table II reports the median solve time for each controller.
- 搭配提示：图常用 shows；表常用 reports / summarizes；公式句用 yields / implies 等衔接。

## 41 observe — observe a trend/behavior/phenomenon。

- 使用场景：报告响应趋势或观察现象。
- 正例：We observe larger tracking errors as the communication delay increases.
- 搭配提示：observe 后接 trend、behavior 或 that 从句，适合引出观测描述。

## 42 indicate / suggest — results indicate that ...；results suggest that ...。

- 使用场景：接续结果描述并引出解释。
- 正例：The ablation results suggest that the observer contributes to disturbance rejection.
- 搭配提示：indicate / suggest 后接 that 从句；也可用 indicating / suggesting 接续前句结果。

## 43 exhibit — a system/response exhibits oscillations, overshoot or a specified property。

- 使用场景：描述系统或响应呈现的行为。
- 正例：The baseline response exhibits sustained oscillations.
- 搭配提示：响应或系统作主语时用 exhibits；图表作主语时通常用 shows。

## 44 achieve / attain — achieve a success rate/tracking accuracy/target performance。

- 使用场景：报告达到的指标或目标水平。
- 正例：The controller achieves a mean tracking error of [value] under [condition].
- 搭配提示：achieve 后常接 performance、accuracy 或指标值；attain 常接目标水平。

## 45 reduce / improve / outperform — reduce an error；improve accuracy；outperform a named baseline on a named metric。

- 使用场景：描述误差、计算时间或精度的比较。
- 正例：The proposed method reduces the mean solve time relative to [baseline].
- 搭配提示：reduce an error；improve accuracy；outperform a baseline in terms of a metric。

## 46 preserve / retain / maintain — preserve a mathematical property；retain a model feature；maintain performance/feasibility。

- 使用场景：描述保留的属性、参数或持续表现。
- 正例：The reformulation preserves the feasible set.
- 搭配提示：preserve a property；retain parameters；maintain performance，注意各自宾语。

## 47 attribute / explain / result in — attribute an observed change to a mechanism；explain a trend；A results in B。

- 使用场景：解释现象及其相互关系。
- 正例：The additional optimization step increases the computation time.
- 搭配提示：attribute A to B；A results in B；explain a trend，方向和介词不同。

## 48 support / corroborate — results support a conclusion；results corroborate a finding。

- 使用场景：表达结果对某个解释或结论的支持。
- 正例：The hardware results support the applicability of the method to the tested platform.
- 搭配提示：support / corroborate 后常接 finding、interpretation 或 conclusion。

## 49 choose / select — choose a control input；select a gain to satisfy a condition。

- 使用场景：表达主动设计或选取的量。
- 正例：The gain is selected to satisfy [condition].
- 搭配提示：choose A as B；select A to satisfy B。选择设计量不等同于推导结果，也不自动表示求得最优解。

## 50 measure / store — measure a quantity using a sensor；store a value for a later operation。

- 使用场景：描述测量与存储动作。
- 正例：The sensor measures [quantity]. The controller stores [value] for [subsequent operation].
- 搭配提示：measure 接被测量，store 接所存值；估计用 estimate，不把这三种动作当作同义词轮换。

## 51 regulate / track — regulate a variable to a setpoint；track a reference trajectory。

- 使用场景：说明调节目标或跟踪目标。
- 正例：The controller regulates [variable] to [setpoint].
- 搭配提示：regulate 与 track 根据任务和目标选择，不能为了增加变化而替换论文已经定义的任务名称。

# 易混表达

1. derive / compute / solve
derive 接公式、关系或条件，compute 接数值量或控制输入，solve 接方程或优化问题。常见句式：We compute the control input by solving the optimization problem.

2. propose / present / develop / use
propose 用于提出方案，present 用于介绍内容，develop 用于说明形成的方法或系统，use 用于交代采用的工具。按当前句子的动作选择。

3. show / demonstrate / validate / verify
show 常用于图表描述或 that 从句；demonstrate 常接能力或效果；validate 常接方法；verify 常接性质或条件。它们不是固定的一一对应翻译。

4. accuracy / precision / robustness / stability
这些名词有不同技术含义，正文用词与所在章节和指标名称保持一致。避免将所有性能描述都写成 performance。

5. mean error / mean RMSE / maximum RMSE
mean error 的中心词是 error，mean RMSE 的中心词是 RMSE。涉及多次试验或多个工况时，可用 across trials / across operating conditions 写明汇总维度。

6. fixed / same / both / this
这些词依赖修饰对象或先行词。优先写 fixed design parameters、the same control equations、both channels；距离较远时重复具体名词。

7. 信号与专业名词的范围
`command / applied input / measurement` 分别指指令、实际施加输入和测量；`design parameters / parameter estimates` 分别指设计参数和估计量；`reference model / command` 不自动表示同一对象。按材料中已经定义的对象选词，不触发额外的实现审查。

`speed / velocity` 按速度大小、向量或明确分量的含义选用；`loads / forces` 按作者定义区分载荷内容，不能在包含力矩时只写力。`operating conditions / regimes` 依一般工况或有定义的模式选择。`hardware` 指具体物理实现相关对象，实验活动使用 `experiments / tests` 并按实际场景说明，不能把所有实验机械改成 hardware。

准确的专业词，如 regressor、input effectiveness、matched uncertainty、projection operator、controllability、asymptotic stability，在相应语境保留。词库不是封闭白名单；装饰性用词的处理由总技能 M03 负责，已有自然表达无需换词。
