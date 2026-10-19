# humanizer-zh

面向中文内容的“去 AI 味”Agent Skill。

它会识别中文文本中的空泛升华、模板连接词、商业黑话、机械排比、伪金句、聊天机器人残留，以及公众号、小红书、短视频和商业汇报中常见的平台模板腔。改写时会锁定事实、数字、日期、引文、链接和作者立场，不用“编细节”的方式假装真人。

## 与上游版本的关系

本项目基于 [blader/humanizer](https://github.com/blader/humanizer) v2.9.1 的核心原则重新设计：

- 保留事实，不按原文句式机械改写
- 不新增来源中不存在的信息
- 支持使用本人旧文校准声线
- 避免把单个词语或标点误判成 AI 写作

中文增强版另外加入 36 组中文模式，覆盖中文商业黑话、宏大开场、强行升华、公众号模板、小红书复制腔、短视频悬念流水线和商业汇报闭环腔。

这不是 AI 检测器，也不承诺绕过任何检测系统。它只负责改善表达。

## 安装

这是一个以 `SKILL.md` 为入口的通用 Agent Skill，不依赖脚本、API、MCP 或环境变量。

下载源码：

```bash
git clone https://github.com/syw2039/humanizer-zh.git
```

将整个 `humanizer-zh` 目录放入所用 Agent 的 Skills 目录，或通过该工具提供的本地 Skill 导入功能安装。安装后应保持 `SKILL.md` 位于目录根部。

也可以在 GitHub 页面点击 **Code → Download ZIP**，解压后安装。不同 Agent 的 Skills 目录和导入方式可能不同，请以对应工具的文档为准。

## 使用方法

直接改写：

```text
请使用 humanizer-zh 修改下面这段文字。
保留所有事实和数字，改得自然一点，不要新增信息。

【粘贴原文】
```

审校并说明：

```text
请使用 humanizer-zh 的审校模式。
先指出最明显的 AI 模板腔，再给我可以直接发布的终稿。

【粘贴原文】
```

匹配个人文风：

```text
请使用 humanizer-zh 匹配我的写作习惯。

这是我以前写的两段文字：
【本人旧文】

这是需要改写的内容：
【目标文本】
```

## 适用内容

- 公众号文章
- 小红书文案
- 短视频口播稿
- 商业计划、方案和汇报
- 邮件、通知和工作总结
- 技术文档与产品说明
- 个人文章和评论

## 项目结构

```text
humanizer-zh/
├── SKILL.md
├── README.md
├── LICENSE
├── NOTICE
├── agents/
│   └── openai.yaml
├── examples/
│   ├── before.md
│   └── after.md
└── references/
    └── chinese-ai-patterns.md
```

## License

MIT。上游版权和许可信息见 [LICENSE](LICENSE) 与 [NOTICE](NOTICE)。
