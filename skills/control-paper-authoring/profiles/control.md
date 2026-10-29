# control：控制与机器人论文

读者默认具有控制基础，专业术语准确、对象与关系清楚。下表中的文件路径均相对于本配置文件。每个模块有唯一主规则，跨模块引用通过此表解析。

| 模块 | 主规则文件 | 配套 skill 与读取条件 |
| --- | --- | --- |
| M01 章节安排 | [structure.md](../modules/structure.md) | 默认内置；只有用户明确要求其他文风时才另行适配 |
| M02 作者叙事 | [author-voice.md](../modules/author-voice.md) | 中文 anti-defensive-writing；英文 anti-defensive-writing-en，动笔前按目标语言读取 |
| M03 自然表达 | [natural-language.md](../modules/natural-language.md) | 中文 humanizer-zh；英文 humanizer，按语言整理任务读取 |
| M04 常用句式 | [ieee-control-writing](../../ieee-control-writing/SKILL.md) | 按段落功能选其参考文件 |
| M05 词汇用法 | [vocabulary-and-usage.md](../../ieee-control-writing/references/vocabulary-and-usage.md) | 术语和搭配需要时读取；通过 M04 进入时也复用同一文件 |
| M06 技术与证据 | [evidence.md](../modules/evidence.md) | 默认内置；特定统计或核验需求可按 M08 选工具 |
| M07 实验叙事 | [experiments.md](../modules/experiments.md) | 默认内置；TASE 来源记录按需查阅 |
| M08 图表与交付 | [delivery.md](../modules/delivery.md) | 检索、引用、绘图、模板及文档工具按实际产物选择 |

本配置的 M01、M04、M05、M06、M07 含控制领域规则；新领域逐项选择保留或替换。M02、M03 的作者叙事与文风适配可复用；M08 的具体模板与工具仍需匹配目标领域。

尚无额外扩展 skill。新增补充或替换提供者时，按维护约定登记角色、路径、触发条件与冲突处理；不把新技能正文粘贴进主入口。
