# M05 常用词汇与使用场景 / Vocabulary and usage

按实际概念选词，同一对象保持同一术语。以下是编辑归纳与控制领域用语建议，不是大样本词频排名；[来源范围](source-basis.md)保留在独立记录中。

## 功能动词与搭配

| 功能 | 常用表达 | 使用边界 |
| --- | --- | --- |
| 定义与记号 | define; denote; is defined as | 数学定义或符号约定，不代替观察和推导 |
| 描述系统 | is described by; is given by | 说明模型或已有关系，先命名对象 |
| 假设与近似 | assume; is assumed to; approximate | 保留真实假设、近似条件，不写成恒等 |
| 设计选择 | choose; select; is selected as | 主动设计的量，不等同最优性 |
| 推导与计算 | derive; obtain; compute; yield | 有对应步骤、计算或关系支持 |
| 实现动作 | measure; estimate; update; store | 测量、估计、更新和存储分别对应实际操作 |
| 补偿作用 | compensate for; account for | 指明实际建模或处理的对象，不泛指“强鲁棒” |
| 跟踪与调节 | track a reference; regulate a variable | 目标、受控变量和误差定义一致 |
| 实验观察 | shows; is lower than; decreases | 报告实际现象，明确指标与条件 |
| 解释 | indicates; is consistent with | 解释的强度服从证据，不能自动升级为因果 |
| 保证性质 | ensures; guarantees; converges | 需要对应理论结果与条件；设计目标不等于证明 |

## 易混概念

| 表达 | 对应场景 | 不可混用 |
| --- | --- | --- |
| speed / velocity | 速度大小 / 速度向量或明确分量 | 图上标量不能无依据改成向量含义 |
| hydrodynamic loads / forces | 载荷可含力矩 / 力 | 六维力与力矩量不能缩为三维力 |
| command / applied input / measurement | 指令 / 实际施加输入 / 测量 | 按真实信号链区分 |
| design parameters / parameter estimates | 设计设置 / 在线估计量 | 固定设计参数不等于冻结自适应 |
| reference model / command | 期望动态模型 / 目标指令 | 对应的状态与误差不能混称 |
| operating conditions / regimes | 一般工况 / 有定义的物理模式 | regime 有明确含义时保留 |
| mean / maximum per-condition RMSE | 跨试验均值 / 工况级最大指标 | 不等于平均轨迹误差或最大瞬时误差 |
| hardware / experiments | 物理组件、处理器或硬件在环 / 试验活动 | 试验可具体写 pool experiments、flight tests、bench tests，但场景必须真实 |

保留 regressor、input effectiveness、matched uncertainty、projection operator、controllability、asymptotic stability 等准确术语。force command 是否合适取决于真实接口，不全局禁用。

## 消除空泛与装饰性用词

| 待判断表达 | 语义吻合时采用 | 不能增加的含义 |
| --- | --- | --- |
| utilize; leverage | use | 不机械改题名或固定用语 |
| ameliorate tracking deviations | reduce tracking error | 保留误差类型与统计量 |
| facilitate improved tracking | improve tracking，或具体动作 | 没有结果依据不添加 improve |
| seamless integration | 指明输出接入哪个输入 | 不补造低成本、无修改或易部署保证 |
| comprehensive validation | 写实际测试项目 | 不暗示验证穷尽全部情况 |
| superior performance | 写明确比较及条件 | 范围收缩按主入口的作者确认规则处理 |
| framework / mechanism / scheme | 据实际对象写 controller、estimator、algorithm 等 | 不为避免重复轮换名称 |
| force-level 等自造层级名称 | 定义实际变量和接口 | 已有清楚定义的术语可保留 |

robust 的技术含义可以保留；泛泛的“鲁棒、卓越、全面”不能替代证据。更短的词若丢失专业概念，就不是更好的选择。长短句和标点由 M03 管理，具体句式由 M04 管理。
