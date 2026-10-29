# Control Paper Authoring｜控制论文作者写作

简体中文 | [English](README_EN.md)

用于中英文控制与机器人论文的起草、润色、翻译、压缩和实验组织。六个可安装 skill 按九个写作模块协作，通过领域配置选择规则。当前提供控制领域配置；新增领域可绑定其他 skill，无需覆盖原有控制规则。

[主入口](skills/control-paper-authoring/SKILL.md) · [领域配置](skills/control-paper-authoring/profiles/index.md) · [改动日志](skills/control-paper-authoring/CHANGELOG.md) · [维护与扩展](skills/control-paper-authoring/references/maintenance.md) · [模块化审计](AUDIT_20261029.md)

## 快速使用

安装 `skills/` 下全部六个同级目录，提供正文或研究材料、目标语言、任务范围和必须保留的内容。例如：

```text
请使用 $control-paper-authoring 润色附件中的英文控制论文。
本轮只改语言，保留方法、公式、数据和引用，使用 control 配置。
重点处理 M03 自然表达和 M05 词汇用法。
如果主张范围明显超过材料，可以收缩到有据可依的范围并列出修改；
存在科学含义不确定，或不利结果影响核心结论时，先询问我。
```

用户可以按模块指定工作，模块名称不要求精确记忆。已有作者确认无需反复提供。调用语法、文件编辑和编译能力取决于宿主工具。

## 九个模块怎样分工

模块 ID 表示稳定的职责；真正读取哪个文件由[当前领域配置](skills/control-paper-authoring/profiles/control.md)决定。

| 模块 | 功能与输入 | control 配置中的提供者 |
| --- | --- | --- |
| M01 章节安排 | 从问题、方法和证据安排摘要至结论，或按要求压缩重组 | [structure.md](skills/control-paper-authoring/modules/structure.md) |
| M02 作者叙事 | 围绕真实优势组织内容，决定叙述重点与结果取舍 | [author-voice.md](skills/control-paper-authoring/modules/author-voice.md)，调用中/英文 anti-defensive-writing |
| M03 去 AI 味 | 处理含糊、空泛、堆叠、重复和聊天残留 | [natural-language.md](skills/control-paper-authoring/modules/natural-language.md)，调用对应语言的 humanizer |
| M04 常用句式 | 按定义、假设、推导、设计、实现、观察等功能选择表达 | [ieee-control-writing](skills/ieee-control-writing/SKILL.md) 及三份句式库 |
| M05 词汇与用法 | 术语、动词搭配、易混概念和语境替换 | [vocabulary-and-usage.md](skills/ieee-control-writing/references/vocabulary-and-usage.md) |
| M06 技术与证据 | 保留模型、信号、时序、评价窗口、统计对象和主张含义 | [evidence.md](skills/control-paper-authoring/modules/evidence.md) |
| M07 实验叙事 | 为已有验证分配职责，组织比较、消融、曲线与数字 | [experiments.md](skills/control-paper-authoring/modules/experiments.md) |
| M08 图表与交付 | 图注、表注、显示精度、引用、模板选择、匿名和文件核对 | [delivery.md](skills/control-paper-authoring/modules/delivery.md) |
| M09 排版 | 定义顺序、图表邻近与排列、统一间距、留白、双栏对齐和成稿检查 | [layout.md](skills/control-paper-authoring/modules/layout.md) |

词汇模块提供常用表达及场景，没有大样本词频统计，不声称是“高频词排名”。示例中的平台、方法、数据和实验流程不能自动带入当前论文。

## 一次任务会读取什么

主入口先确定任务范围和领域，再根据触发条件读取模块；模块间请求也通过当前领域配置解析，不固定跳回控制领域。

- 所有论文写作在动笔前通过 M02 读取目标语言的去防御性写作 skill。
- 起草或重组章节读取 M01；语言整理读取 M03。M03 用嵌入模式调用 Humanizer，只交付终稿，用户要求时再给分析。
- 英文句式按 M04 选择 `model-and-control-patterns.md`、`experiments-and-results.md` 或 `manuscript-sections.md`；词义和搭配读取 M05。
- 技术歧义、统计或主张问题读取 M06；组织实验读取 M07；实际图表、文献或文件交付读取 M08；图表位置、间距与页面布局读取 M09。
- [TASE 来源记录](skills/control-paper-authoring/references/tase-source-notes.md)、[IEEE 来源记录](skills/ieee-control-writing/references/source-basis.md)、维护文档和日志只在核查或维护时读取。

已经完整读取的同一版本无需重读。新增文件不会因放进目录就自动生效。“调用 skill”是读取并采用其指令；这里没有自动执行所有模块的调度程序。

## 已统一的写作规则

引言按实际任务与现实意义、相关研究与已有成果、尚存问题与本文研究问题、本文方法与验证安排展开，段数随内容安排。

英文公式后的符号、参数或条件解释用小写 `where`，与公式构成同一句并调整标点。这是本项目约定，不是 IEEE 强制要求。正文解释尽量不用破折号，保留数值范围、数学符号和固定术语所需连接号。

以真实优势组织论文，不主动罗列缺点，无关弱项可省略。影响核心结论或关键比较的不利结果先询问作者，确认定位与主张后再处理；不通过隐瞒关键事实制造支持。明确的过度范围可收缩并说明改动，存在不确定性时先问作者。

第三方 skill 原件保持完整，M02、M03 明确学术适配规则。技术术语、研究事实、必要条件和实际模板优先于通用文风建议；新冲突不能按文件加载顺序擅自覆盖。

排版模块按以下优先级执行：定义先于使用 → 靠近首次正文引用 → 同侧连续图表尽量同类相邻 → 按首次引用顺序排列 → 页首先于页尾 → 内部间距按期刊规范全文统一 → 消除明显留白 → 双栏图表下边界尽量对齐。图表与首次引用最多相邻页，中间不得隔一整页；补充内容须有材料依据并与论证有关。完整要求及冲突处理见 [M09](skills/control-paper-authoring/modules/layout.md)。

## 六个安装目录

| 目录 | 作用 |
| --- | --- |
| `control-paper-authoring` | 主入口、模块、领域配置、维护约定和日志 |
| `ieee-control-writing` | 控制英文句式、词汇与来源 |
| `anti-defensive-writing` | 中文作者叙事的配套技能 |
| `anti-defensive-writing-en` | 英文作者叙事的配套技能 |
| `humanizer` | 英文自然表达，保留原插件元数据和维护资料 |
| `humanizer-zh` | 中文自然表达、按需参考和修改示例 |

单独使用配套技能不会自动获得主入口的全部模块规则。完整流程从 `control-paper-authoring` 开始。

```text
skills/control-paper-authoring/
├── SKILL.md
├── CHANGELOG.md
├── profiles/        # 索引与各领域的模块绑定
├── modules/         # 当前内置模块与第三方适配
├── references/      # 维护约定、来源记录
└── agents/          # 界面元数据

skills/ieee-control-writing/
├── SKILL.md
├── references/      # 三份句式库、词汇模块、来源记录
└── agents/
```

## 按模块修改与扩展

修改现有规则时，指出模块与预期变化即可，例如：

```text
请只修改 control 配置的 M01 引言组织规则，保留其他模块。
先检查与配套 skill 的冲突，冲突向我确认；更新日志和中英文说明。
```

排版可以单独指定：

```text
请按 control 配置的 M09 调整论文排版，严格按模块的优先级处理。
使用期刊模板，修改后编译并检查全部页面；需要补充正文时使用已有材料。
```

已有新 skill 时，优先让模块引用它，而不是复制全文：

```text
我提供了一个新的专业词汇 skill。请读取它，作为 control 配置
的 M05 提供者；保留尚适用的独有规则，向我确认冲突，并记录变更。
```

扩展到其他领域时，新建领域配置并显式绑定九个模块。例如可复用 M02、M03，选择新领域的章节、句式、词汇和证据提供者；原 `control` 配置保持独立。新模块间也通过配置查找规则。只替换词汇不一定完成领域适配，实验与证据标准可能也需替换。

每个模块只有一个主规则提供者，可登记有明确触发条件的扩展。登记信息包括路径、适用语言、输入输出、补充或替换关系及冲突处理。完整步骤和接入字段见[维护约定](skills/control-paper-authoring/references/maintenance.md)。后续实际改动记录到[日志](skills/control-paper-authoring/CHANGELOG.md)。

## 可选外部能力

文献检索、引用核验、绘图、模板和 Word/PDF/LaTeX 交付由 M08 按任务选择宿主已有工具；对应 skill 如 `research-lookup`、`citation-management`、`nature-ref-verifier`、`scientific-visualization`、`venue-templates` 不随本包提供。明确要求 Nature 文风时可适配 `nature-writing` 或 `nature-polishing`，须先核对其与当前模块的关系，不直接覆盖控制规则。

写作指令本身无需 Python、Node.js 或专用 API 密钥。运行 AI、编辑文件、编译和联网依赖宿主。缺少可选能力时说明范围并继续独立部分，不自动安装，也不声称做过未执行的检查。

## 安装


### Codex：手动安装完整合集

1. 在 GitHub 仓库页面选择 **Code → Download ZIP**，并解压；也可以克隆仓库。
2. 将仓库 `skills/` 下的六个目录复制到用户技能目录 `~/.agents/skills/`。Windows 中通常为 `C:\Users\你的用户名\.agents\skills\`。
3. 保持六个目录同级。目标目录已有同名技能时，先比较或备份已有版本，再更新。
4. 在技能选择器或新对话中调用 `control-paper-authoring`。没有出现时，检查目录层级并重启 Codex。

正确的安装结果：

```text
~/.agents/skills/
├── control-paper-authoring/SKILL.md
├── ieee-control-writing/SKILL.md
├── anti-defensive-writing/SKILL.md
├── anti-defensive-writing-en/SKILL.md
├── humanizer/SKILL.md
└── humanizer-zh/SKILL.md
```

将整个仓库目录放进技能目录，会多出一层 `skills/`，与本合集的安装结构不符。主技能通过 `../技能名/SKILL.md` 读取配套技能，因此六个目录的同级关系需要保留。

只希望在某个代码仓库内使用时，可以安装到该仓库的 `.agents/skills/`。Codex 的本地技能位置、自动发现和调用方式见 [OpenAI 官方技能文档](https://learn.chatgpt.com/docs/build-skills)。

### Codex：让安装器处理

将当前 GitHub 仓库链接提供给 Codex，并明确要求安装全部六个技能：

```text
请使用 $skill-installer，从我提供的仓库链接安装 skills/ 下的六个技能：
control-paper-authoring、ieee-control-writing、anti-defensive-writing、
anti-defensive-writing-en、humanizer、humanizer-zh。
保持六个目录同级。如果已有同名技能，先比较版本并保留本地修改。
```

### 其他 AI 工具

将六个目录放到该工具支持的本地技能位置，保持目录关系，并使用其对应的调用语法。普通聊天界面只有在能够读取完整规则及所需参考文件时，才具备执行这套流程的材料；上传 ZIP 是否会安装技能，需要以该平台的实际能力为准。


## 交付、来源与许可

提供可用正文或指定文件中的修改；用户要求时附“位置、原句、具体问题、新句”。内部待办和事实冲突不混入投稿正文。只报告实际完成的检查，论文语言修改不自动触发重跑研究实验。

指南属于编辑归纳，不是 IEEE/TASE 官方写作标准，不保证录用或通过 AI 检测。原创部分采用 [MIT](LICENSE)，第三方保持原有版权与许可，详见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。
