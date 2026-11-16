# Taste Skill CN

**让中文成为设计的起点。**

给 Claude Code、Codex 等支持 Agent Skills 的编程助手使用的中文网页审美技能。把文章、活动介绍和产品说明，做成适合中文阅读、有自己气质的网页。

Chinese-first web design skill for AI coding agents: typography, content-led storytelling, and art direction in everyday language.

[安装](#安装) · [看示例](preview/index.html) · [我们新增了什么](#我们新增了什么) · [与-taste-skill-的关系](#与-taste-skill-的关系)

## 不会说设计术语，也能说清想要什么

你可以直接这样说：

> 用 taste-skill-cn 把这篇文章做成网页，像一本安静的杂志。保留论证和引用，手机上读起来舒服。

> 用 taste-skill-cn 做读书会介绍页，像一张展览说明。时间地点没确定，标出来，不要编造。

> 用 taste-skill-cn 改这个中文产品页。像一份清楚的说明书，让人先看懂它能做什么。

## 我们新增了什么

| 能力 | 具体改变 |
|---|---|
| 中文先行 | 先看真实标题字数与语义停顿，再定字号和宽度；不用英文占位决定布局 |
| 内容叙事 | 把原文映射成读者问题，保留事实、论证与引用，不把长文压成卖点卡片 |
| 三种日常风格 | 杂志、展签、说明书；改变信息结构和视觉重心，远不止换色 |
| 中文排版底座 | 局部生效的 CSS，中文回退字体、阅读宽度与行距，不依赖在线字库 |
| 如实交付 | 区分静态检查与实际预览，说明待确认素材和没有接通的功能 |

中文网页不必都是米白底、宋体和红印章。工具可以清楚，展览可以大胆，文章可以安静。风格来自内容。

## 安装

需要支持 Agent Skills 的编程助手。技能本身不要求运行脚本、不需要额外 API Key，也不会自动安装依赖。模型服务仍使用你原有的账号与配置。

```bash
npx skills add batespaige357-tech/taste-skill-cn --skill taste-skill-cn
```

没有 Node.js 或不想运行安装命令，也可以下载本仓库，把 **`skills/taste-skill-cn` 整个文件夹**复制到助手支持的技能目录。例如：

- Codex：`~/.codex/skills/taste-skill-cn/`
- Claude Code：`~/.claude/skills/taste-skill-cn/`

重新打开会话，在 Codex 中可输入 `$taste-skill-cn`，或直接说明要用这个技能。其他工具的技能目录与调用方式以其当前说明为准。

## 看示例

下载后直接用浏览器打开 **[preview/index.html](preview/index.html)**，无需安装、联网或编译。

同一份“把周末留给一本书”的虚构读书会材料，可以切换三种表达：

| 杂志 | 展签 | 说明书 |
|---|---|---|
| 观点与阅读节奏 | 主题与活动事实 | 步骤与参与准备 |
| 阅读主栏与边注 | 大标题与事实栏 | 清晰的步骤结构 |

示例还提供“常见模板”对照，用来解释我们的设计选择。**它是手工编写的演示，不是模型测试成绩，也不是与原项目的性能比较。** 原始需求见 [examples/brief.md](examples/brief.md)。

## 如何工作

1. 从你给的内容判断受众、主题和读者下一步。
2. 沿用现有品牌，或建议一个能解释清楚的视觉方向；需要比较时给三种。
3. 先组织内容，再实现页面；尊重已有框架和修改范围。
4. 检查中文排版、操作和内容真实性，说明检查范围。

可以创建网页，也可以只审查或局部修改。用户未要求编译时不主动运行 build；不会因为调用技能就擅自发布网站。

## 与 Taste Skill 的关系

本项目受 [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill) 启发，是**独立维护、非官方**的中文方向社区项目。

我们借鉴它“让设计判断成为可执行约束”的思路；本版技能正文、中文参考、CSS 与演示重新编写，没有打包上游的代码、照片、商标图或脚本，也不需要原技能作为运行依赖。

| Taste Skill（本次参考版本） | Taste Skill CN v0.1.0 |
|---|---|
| 公司网站的完整系统、素材与浏览器检查工具 | 中文排版、内容转网页和可解释的风格选择 |
| 有自己的整屏布局和动效规则 | 按内容长度安排页面，不强制整屏或动效 |
| 自带 Node 与浏览器工作流 | 轻量指令、参考与可选 CSS，使用助手已有能力 |

这是方向比较，不代表质量排名。来源、参考提交与许可证说明见 [ATTRIBUTION.md](ATTRIBUTION.md)。

## 目录

```text
skills/taste-skill-cn/
  SKILL.md                    技能入口
  agents/openai.yaml          Codex 展示信息
  references/                 中文排版、叙事、风格与检查表
  assets/typography.css       可选、局部生效的排版底座
preview/index.html            无依赖交互示例
examples/brief.md             演示需求与观察说明
```

## 版本与参与

当前是 **v0.1.0**。格式与文件检查不能证明生成质量；字体在 Windows、macOS 和 Linux 上也会不同，仍需在目标环境预览。

欢迎提交带截图的中文排版问题：原始需求、助手名称、页面宽度、预期与实际效果。请移除个人信息和密钥。我们尤其关注长标题、中英混排、长文阅读和真实活动页面。

如果这个方向对你有用，欢迎 Star；更欢迎带着一个具体页面来讨论。

MIT License · [LICENSE](LICENSE)
