<div align="center">

# Taste Skill CN

### 让 AI 写中文网页，也懂中文的美。

**把文章、活动介绍和产品说明，做成有自己气质的网页。**

不懂设计术语也能用。告诉 AI：像一本杂志、像一张展签，或像一份清楚的说明书。

[![MIT License](https://img.shields.io/badge/license-MIT-235B4B?style=flat-square)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent_Skill-Claude_Code_%C2%B7_Codex-252B29?style=flat-square)](skills/taste-skill-cn/SKILL.md)
[![Chinese First](https://img.shields.io/badge/Chinese-first-155E63?style=flat-square)](#我们做了哪些不同)

[立即安装](#一行安装) · [风格方向](#三种风格方向) · [中文能力](#我们做了哪些不同) · [来源与致谢](#来源与致谢)

</div>

## 一行安装

```bash
npx skills add batespaige357-tech/taste-skill-cn --skill taste-skill-cn
```

然后对你的 AI 说：

```text
用 taste-skill-cn 把我的中文内容做成网页。
像一本杂志，保留原文的表达，手机上读起来舒服。
```

支持读取 Agent Skills 的编程助手。技能本身不需要额外 API Key、不运行安装脚本；模型服务沿用你的账号配置。

<details>
<summary>手动安装与调用方式</summary>

下载仓库，将 **`skills/taste-skill-cn` 整个文件夹**复制到助手的技能目录，例如：

- Codex：`~/.codex/skills/taste-skill-cn/`
- Claude Code：`~/.claude/skills/taste-skill-cn/`

重新打开会话。Codex 中可使用 `$taste-skill-cn`；其他工具的目录与调用方式以其说明为准。

</details>

## 三种风格方向

用日常语言描述偏好，让内容决定视觉结构。

| 方向 | 视觉重点 | 适合的内容 |
|---|---|---|
| 像一本杂志 | 观点、阅读节奏与连续正文 | 文章、专栏、访谈、作品集 |
| 像一张展签 | 主题、留白与关键信息 | 展览、活动、文化空间 |
| 像一份说明书 | 步骤、证据与行动入口 | 工具、产品、服务与指南 |

## 我们做了哪些不同

**中文不是英文模板的替换文本。**

| 你可能遇到的问题 | Taste Skill CN 的处理方式 |
|---|---|
| 中文标题一放进去，换行就碎了 | 先看真实字数、语义停顿和手机宽度，再决定排版 |
| 每段内容都被装进同一种卡片 | 按读者的问题组织页面，长文章保留连续阅读 |
| 一说“高级”，就变成米白底、宋体、红印章 | 从内容与品牌选方向，中文也可以清楚、冷静、大胆 |
| 不懂网格、字体配对等设计词 | 用“杂志／展签／说明书”等日常语言表达偏好 |
| 日期、地址、评价被 AI 补出来了 | 保留事实来源，缺的信息标记待确认 |

可用于新建网页、局部改版，也可以只做中文页面审美评审。沿用项目已有框架与品牌，不扩大修改范围。

## 来源与致谢

受 **[Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill)** 启发，独立维护、非官方。感谢原项目把网页设计判断转化为可执行规则的思路。

本版技能正文、中文排版参考、内容叙事方法和 CSS 重新编写；没有打包上游代码、摄影或视觉标识，也不依赖安装原技能。

我们的方向是**中文内容与阅读体验**：不强制整屏区块，不要求每页动效，按内容长度安排结构。`cn` 表示中文设计方向，不表示官方翻译。

[来源与参考提交](ATTRIBUTION.md) · [上游 MIT 许可](licenses/taste-skill-MIT.txt) · [本项目 MIT 许可](LICENSE)

<details>
<summary>项目结构与验证范围</summary>

```text
skills/taste-skill-cn/
  SKILL.md                    技能入口
  agents/openai.yaml          Codex 展示信息
  references/                 中文排版、叙事、风格与检查表
  assets/typography.css       可选、局部生效的排版底座
```

当前技能版本 **v0.1.0**。技能格式、UTF-8 与本地链接已检查。

尚未完成真实助手的端到端安装、生成质量测评、手机与读屏验收。实际效果受模型、输入内容和项目环境影响。未运行前端编译。[验证记录](VALIDATION.md)

</details>

---

<div align="center">

**如果你也想让 AI 写出更懂中文的网页，点个 Star，关注后续更新。**

也欢迎带一个具体页面来：[提交排版问题](https://github.com/batespaige357-tech/taste-skill-cn/issues) · [查看版本](https://github.com/batespaige357-tech/taste-skill-cn/releases)

<sub>提交截图前，请移除个人信息与密钥。</sub>

</div>
