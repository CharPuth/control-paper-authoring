# control：控制与机器人论文

读者默认具有控制基础，专业术语准确、对象与关系清楚。下表中的文件路径均相对于本配置文件。每个模块有唯一主规则，跨模块引用通过此表解析。

| 模块 | 主规则文件 | 配套 skill 与读取条件 |
| --- | --- | --- |
| M01 章节安排 | [structure.md](../modules/structure.md) | 默认内置；只有用户明确要求其他文风时才另行适配 |
| M02 作者叙事 | [author-voice.md](../modules/author-voice.md) | 中文 anti-defensive-writing；英文 anti-defensive-writing-en，动笔前按目标语言读取 |
| M03 自然表达 | [natural-language.md](../modules/natural-language.md) | 中文 humanizer-zh；英文 humanizer，按语言整理任务读取 |
| M04 句式与写作习惯 | [control-paper-writing-style](../../control-paper-writing-style/SKILL.md) | 英文句子起草或修改；规则、语言功能句式、原稿教材按需读取 |
| M05 词汇用法 | [control-paper-vocabulary](../../control-paper-vocabulary/SKILL.md) | 英文用词、翻译或词汇教学；51 组场景词汇和正反例按需读取 |
| M06 技术与证据 | [evidence.md](../modules/evidence.md) | 默认内置；特定统计或核验需求可按 M08 选工具 |
| M07 实验叙事 | [experiments.md](../modules/experiments.md) | 默认内置；TASE 来源记录按需查阅 |
| M08 图表与交付 | [delivery.md](../modules/delivery.md) | 检索、引用、绘图、模板及文档工具按实际产物选择 |
| M09 排版 | [layout.md](../modules/layout.md) | 采用实际期刊模板；编译与页面渲染使用宿主可用工具 |

本配置的 M01、M04、M05、M06、M07 含控制领域规则；新领域逐项选择保留或替换。M02、M03 的作者叙事与文风适配可复用；M08、M09 的具体模板、排版要求与工具仍需匹配目标领域。

M04、M05 均为替换后的主规则提供者，不再调用旧 ieee-control-writing。两者接收当前文字或研究材料，默认返回可用正文；要求教学时给出原句、改写及语言理由。公式后解释必须使用小写 where；保留原稿正反面教材的上下文，但不将案例中的实现或试验设置作为新论文默认要求。已有主入口和 M02 等的任务边界继续适用，两者不重新启动整篇论文流程。缺少提供者时报告缺失，继续独立部分，不自动安装。

尚无额外扩展 skill。新增补充或替换提供者时，按维护约定登记角色、路径、触发条件与冲突处理；不把新技能正文粘贴进主入口。
