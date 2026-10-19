# Control Paper Authoring｜控制论文作者写作

**简体中文** | [English](README_EN.md)

面向控制与机器人研究的论文写作技能合集。以 `control-paper-authoring` 为入口，按任务组织中英文起草、润色、翻译、篇幅压缩和实验叙事，将控制领域的句式、作者视角与自然表达结合起来，同时保留方法、公式、数据和结论成立的条件。

导航：[快速开始](#快速开始) · [功能](#能完成哪些工作) · [技能分工](#六个技能如何分工) · [参考文件](#什么时候读取哪些参考文件) · [可选能力](#可选能力与外部依赖) · [安装](#安装) · [使用示例](#使用示例) · [常见问题](#常见问题) · [来源与许可](#来源与许可)

## 快速开始

1. 下载本仓库，将 `skills/` 中的**六个技能目录一起安装**到支持本地技能的 AI 工具中。Codex 的具体步骤见下方“安装”。
2. 提供要修改的正文或研究材料，说明目标语言、任务范围和不能改动的内容。
3. 指定主入口，例如：

```text
请使用 $control-paper-authoring 润色附件中的英文控制论文。
本轮只修改语言，保留方法、公式、数据、引用和结论范围。
使用作者视角和控制领域常见表达。返回修改后的正文，
并在正文外列出有代表性的修改前后对照。
```

在支持 `@` 选择技能的界面中，选择对应技能即可；自然语言指定 `control-paper-authoring` 也能明确意图。不同工具的触发语法由其宿主决定。

## 能完成哪些工作

| 工作 | 输入 | 处理重点 |
| --- | --- | --- |
| 从研究材料起草 | 已确认的方法、公式、图表、结果和目标刊会 | 建立“问题—方法—证据”的主线，形成摘要、引言、方法、实验和结论 |
| 中英文润色 | 已有段落或完整稿件 | 修正含糊指代、堆叠定语、空泛修饰、回复式语气和不自然的专业表达 |
| 中英文翻译 | 原文、术语约定和目标语言 | 保留技术含义与符号关系，按目标语言的学术习惯组织句子 |
| 压缩篇幅与重组 | 原稿、篇幅目标和允许改动的范围 | 删除重复内容，调整论证顺序，保留必要定义、证据和条件 |
| 组织仿真与实验 | 已有试验目的、设置、对照、曲线和统计结果 | 区分标称参照、模块贡献、跨工作点、指令切换、约束机制和现场运行的论证职责 |
| 图表文字与交稿整理 | 图表、说明文字、引用和实际投稿要求 | 明确图表与正文的分工，统一符号、单位、统计口径和必要读图信息 |

本项目尤其关注控制论文容易写错的技术关系：控制器输出与实际施加输入、参考模型误差与指令误差、设计目的与已经证明的性质、参数有界与参数收敛、单次记录与重复试验统计。语言修改应保持这些区别。

英文公式后紧接符号、参数或条件解释时，主技能采用小写 `where`，并同步处理公式末尾标点。这是本技能的写作约定，适用范围是公式后的解释，不构成对 `here` 其他用法的禁令，也不宣称是 TASE 的强制规定。

## 六个技能如何分工

| 技能 | 职责 | 主入口何时读取 |
| --- | --- | --- |
| [`control-paper-authoring`](skills/control-paper-authoring/SKILL.md) | 确定任务范围，组织作者叙事，约束技术含义，选择配套规则和参考文件 | 控制与机器人论文的起草、修改、翻译或结构组织 |
| [`ieee-control-writing`](skills/ieee-control-writing/SKILL.md) | 按定义、假设、推导、设计、实现、比较和解释选择英文句式 | 英文起草或改写 |
| [`anti-defensive-writing`](skills/anti-defensive-writing/SKILL.md) | 围绕真实贡献组织中文叙事，减少无必要的自我削弱和过程汇报 | 中文起草或改写 |
| [`anti-defensive-writing-en`](skills/anti-defensive-writing-en/SKILL.md) | 对应的英文作者叙事规则 | 英文起草或改写；`ieee-control-writing` 也引用它 |
| [`humanizer`](skills/humanizer/SKILL.md) | 识别英文模板化表达、空泛修饰和聊天残留，保留原有事实与文风 | 英文起草或改写 |
| [`humanizer-zh`](skills/humanizer-zh/SKILL.md) | 识别中文模板腔、定语堆叠、生造短语和不自然表达 | 中文起草或改写 |

完整工作流从主入口开始。这样，语言规则始终受研究事实、专业语义和结论范围的约束。可以单独使用某个配套技能，但单独调用不会自动获得主技能的全部控制论文规则。

### “调用”具体意味着什么

这些技能主要由 Markdown 指令和参考材料组成。主技能要求 AI 根据任务读取相应文件，再将其规则用于当前写作。“调用其他技能”指的是读取并遵循这些技能的指令，并非运行一个自动调度所有模块的程序。

一次完整任务通常按以下逻辑展开：

1. **确定范围。** 区分只改语言、翻译、从材料起草、实质重组和图表排版。已有稿件的“润色”默认只改语言。
2. **固定事实。** 从材料与作者确认中提取方法、符号、设置、结果、统计口径和不可变更项；真实矛盾集中放在正文之外解决。
3. **选择语言分支。** 中文读取中文去防御性写作和中文 humanizer；英文读取英文去防御性写作、IEEE 控制句式和英文 humanizer。混合任务主要按投稿正文的目标语言选择。
4. **读取当前任务需要的指南。** 改一句话通常只需要语言规则；组织实验章节则需要结构、证据和实验叙事指南。
5. **形成或修改正文。** 以作者身份陈述方法、结果和含义。专业术语、公式、研究事实及必要条件优先于通用文风规则。
6. **检查并交付。** 检查论证主线、术语句式和技术含义；按用户要求交付正文、文件或修改对照。报告实际完成的检查。

同一上下文已经完整读取的技能无需重复读取。是否自动触发技能、能否读写文件、是否能联网或编译，取决于运行它的 AI 工具及用户授权。

## 什么时候读取哪些参考文件

### 主技能的六份指南

以下文件位于 `skills/control-paper-authoring/references/`。

| 文件 | 读取条件 | 主要内容 |
| --- | --- | --- |
| [`author-voice-and-language.md`](skills/control-paper-authoring/references/author-voice-and-language.md) | 去 AI 味、作者视角、中英文语言修改 | 作者身份、清楚的对象与动作、常见术语、自然句式和语言自检 |
| [`paper-structure-and-patterns.md`](skills/control-paper-authoring/references/paper-structure-and-patterns.md) | 新写摘要至结论，或经授权重组章节 | 各章节的功能和可选句式；完整实验章节进一步指向 TASE 实验叙事指南 |
| [`tase-experiment-narrative.md`](skills/control-paper-authoring/references/tase-experiment-narrative.md) | 组织仿真与实验、选择正文数据、解释消融和比较结果 | 各组试验的职责，局部解释与章节总结，图表分工，以及可核查的 TASE 论文实例 |
| [`control-semantics-and-evidence.md`](skills/control-paper-authoring/references/control-semantics-and-evidence.md) | 处理模型、实现、实验事实或比较结论 | 输入与误差定义、时序与统计口径、机制归因、主张与证据的对应关系 |
| [`figures-tables-and-delivery.md`](skills/control-paper-authoring/references/figures-tables-and-delivery.md) | 图表、数值格式、参考文献、匿名和交稿 | 图表说明、指标显示、实际模板要求和交付前核对 |
| [`revision-lessons.md`](skills/control-paper-authoring/references/revision-lessons.md) | 判断历史改稿经验能否泛化，或维护本技能 | 区分可复用的写作原则与某篇论文的局部偏好 |

### IEEE 英文句式的五份指南

以下文件位于 `skills/ieee-control-writing/references/`。按当前段落的功能选择，无需每次全部读取。

| 文件 | 读取条件 |
| --- | --- |
| [`model-and-control-patterns.md`](skills/ieee-control-writing/references/model-and-control-patterns.md) | 符号、动力学、控制器设计、公式和离散实现 |
| [`experiments-and-results.md`](skills/ieee-control-writing/references/experiments-and-results.md) | 实验设置、比较、指标、结果和图注 |
| [`manuscript-sections.md`](skills/ieee-control-writing/references/manuscript-sections.md) | 摘要、引言、相关工作、贡献、讨论和结论 |
| [`natural-style-and-editing.md`](skills/ieee-control-writing/references/natural-style-and-editing.md) | 常见词语、自然句式、修改示例和语言检查 |
| [`source-basis.md`](skills/ieee-control-writing/references/source-basis.md) | 核查句式来源、了解语料范围或扩展参考论文 |

`humanizer-zh` 在完整改写或审校时还会读取 [`chinese-ai-patterns.md`](skills/humanizer-zh/references/chinese-ai-patterns.md)；短句轻改可使用其 `SKILL.md` 中的核心规则。英文 `humanizer` 的主要规则集中在自己的 `SKILL.md` 中。

## 可选能力与外部依赖

六个核心技能均随仓库提供。下面这些技能仅在任务需要且运行环境已经具备时使用，不属于本仓库的固定安装依赖。

| 任务 | 主技能提到的可选技能或能力 | 作用 |
| --- | --- | --- |
| 检索与参考文献修订 | `research-lookup`、`citation-management`、`nature-ref-verifier` | 搜索文献、管理或核验书目信息 |
| 明确要求 Nature 文风 | `nature-polishing`、`nature-writing` | 辅助相应文风和结构组织，继续保留控制领域准确术语 |
| 绘图、模板与文件交付 | `scientific-visualization`、`venue-templates`、`pdf:pdf` 等 | 依据实际产物调用绘图、排版、PDF 等工具 |

普通语言修改不需要为此安装一整套科研工具。缺少可选技能时，主技能要求说明实际可用范围，并继续完成不依赖它的工作。

写作规则本身无需 Python、Node.js 或本项目专用 API 密钥。运行 AI 仍需要宿主模型；编辑 Word、编译 LaTeX、重绘图片和检索文献则需要宿主提供对应能力。本仓库不附带论文、实验数据、绘图环境或编译器。

## 仓库结构

```text
control-paper-authoring/
├── README.md
├── README_EN.md
├── LICENSE
├── THIRD_PARTY_NOTICES.md
├── .gitattributes
├── .gitignore
└── skills/
    ├── control-paper-authoring/
    │   ├── SKILL.md
    │   ├── agents/openai.yaml
    │   └── references/                 # 六份主技能指南
    ├── ieee-control-writing/
    │   ├── SKILL.md
    │   ├── agents/openai.yaml
    │   └── references/                 # 五份英文句式指南
    ├── anti-defensive-writing/
    │   ├── SKILL.md
    │   └── LICENSE
    ├── anti-defensive-writing-en/
    │   ├── SKILL.md
    │   └── LICENSE
    ├── humanizer/
    │   ├── SKILL.md
    │   ├── README.md
    │   ├── LICENSE
    │   ├── agents/openai.yaml
    │   ├── scripts/validate-package.py
    │   └── …                          # 保留的上游维护及插件文件
    └── humanizer-zh/
        ├── SKILL.md
        ├── README.md
        ├── LICENSE
        ├── NOTICE
        ├── agents/openai.yaml
        ├── references/chinese-ai-patterns.md
        └── examples/                  # 中文修改前后示例
```

`SKILL.md` 定义技能何时适用、怎样处理任务；`references/` 存放按需读取的详细规则；`agents/openai.yaml` 提供界面显示名称、简介和默认调用提示。目录中保留的第三方插件文件属于相应组件，不代表整个合集已经注册为插件。

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

## 使用示例

### 1. 中文润色

```text
请使用 control-paper-authoring 修改下面的中文控制论文段落。
本轮只改语言：减少空泛修饰、定语堆叠和回复式语气，
保留事实、公式、数据、引用和必要条件。
输出可直接用于论文的正文，修改说明另列。
```

### 2. 英文翻译

```text
请使用 control-paper-authoring，将以下中文方法章节翻译成英文。
目标是控制领域期刊论文。保持符号、控制器结构和离散实现次序不变。
固定术语：参考模型为 reference model；控制分配为 control allocation。
公式后的符号解释使用 where，并检查公式与解释从句的标点。
```

### 3. 根据研究材料起草

```text
请使用 control-paper-authoring，根据附件中的方法、公式和试验结果，
起草英文摘要及引言。目标刊会和篇幅要求见附件说明。
先明确研究问题、核心方法和最主要的实验证据，再组织正文。
只使用材料中已有或我明确确认的研究事实；关键缺项集中列在正文之外。
```

### 4. 组织实验章节

```text
请使用 control-paper-authoring 重组现有仿真与实验章节。
读取 TASE 实验叙事指南，明确各项试验的论证职责，
说明正文应该选择哪些关键数据，以及如何联系曲线和机制解释。
保留现有实验编号、原始结果、统计口径和必要条件。
不要把没有完成的实验写入正文。
```

### 5. 压缩篇幅

```text
请使用 control-paper-authoring 压缩附件中的引言和讨论，
目标减少约 20% 的文字。允许合并重复论点和调整句序，
保留研究问题、方法区别、关键证据、引用关系及影响结论成立的条件。
先给压缩后的正文，再说明主要删减内容。
```

### 6. 修改文件并交付

```text
请使用 control-paper-authoring 修改指定的 LaTeX 主稿。
本轮只修改摘要和结论，不改图表、公式、数值与实验编号。
保持现有文件结构。若运行环境支持编译，修改后编译并检查日志；
报告实际完成的检查及输出文件位置。
```

文件编辑、编译和版式检查由宿主工具执行。若需要这些操作，应在请求中明确交付方式，并提供必要的源文件。

## 输入材料与输出方式

开始任务时，优先提供会改变写法的信息：目标语言、目标刊会、当前文本或研究材料、允许改动的范围、必须保留的内容，以及希望返回正文还是直接编辑文件。已有对话里明确过的信息无需重复确认。

任务可以交付：

- 可直接使用的论文正文；
- 指定文件中的修改；
- 按“位置、原句、具体问题、新句”组织的修改对照；
- 放在正文之外的少量关键缺项或事实冲突。

主技能采用研究作者视角。内部待办、改稿过程和 AI 核查说明与投稿正文分开；必要的科学假设、不利结果和适用范围保留在对应的方法与结果表述中。

## 使用边界

本项目提供写作流程和编辑参考。IEEE 句式指南依据代表性论文及编辑归纳，TASE 指南依据定向阅读的实例；它们不构成 IEEE 或 TASE 的官方语言规范。

研究事实和技术含义始终优先。去防御性写作规则用于突出已经成立的贡献，不能据此隐藏影响核心结论的数据、限制或反例；去 AI 味规则也不能替换准确术语、添加事实或改变结论。

论文能否录用取决于研究质量、证据和刊会要求。本项目不提供录用保证，也不以通过 AI 检测作为效果承诺。

## 常见问题

**为什么需要安装六个目录？** 主技能按语言读取配套技能，相关路径跨越同级目录。完整安装保留原有功能；只复制主技能会缺少相应规则。

**每次都会读取所有文件吗？** 不会。语言分支决定配套技能，具体任务决定参考文件。已经在当前上下文完整读取的文件无需再次读取。

**必须安装 Nature、文献检索或绘图技能吗？** 普通论文语言修改不需要。只有任务需要相应能力时才按需使用。

**只修改语言时会改方法或数据吗？** 主技能要求锁定科学含义和结果。发现真实矛盾时应在正文外提出，不能通过润色自行补齐研究事实。

**英文公式后的 Here 都要替换吗？** 规则针对紧接公式的符号、参数或条件解释，并要求调整句法与标点。它不扩展到其他语境中的 `here` 或 `hereafter`。

**怎样更新？** 下载新版后比较六个目录，保留自己的改动，再更新完整合集。尽量避免混用不同版本的主技能与配套参考文件。

## 来源与许可

本项目的原创内容采用 [MIT 许可证](LICENSE)。第三方组件继续遵循各自保留的许可和版权声明。

第三方组件的作者、来源和许可证见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。各组件中的原始 `LICENSE` 与 `NOTICE` 随文件保留。研究论文的署名与来源见相应参考指南；引用论文的权利不因本仓库的代码或文档许可而改变。
