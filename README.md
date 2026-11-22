# Mist Dossier｜雾中卷宗

**A research-first true-crime storytelling skill.**  
一套面向真实案件研究与叙事的 Agent Skill：先核查，再讲述；尊重事实，控制剧透，让案件成为一个值得慢慢听完的故事。

[简体中文](#简体中文) · [English](#english)

## 简体中文

### 这是什么？

「雾中卷宗」帮助 AI 助手筛选、调查并讲述真实刑事案件，尤其关注未解案件与冷门已破案件。它把资料核查、证据分级、叙事节奏和防剧透规则放进同一套工作流程。

它的核心原则是：**讲给人听的故事，不是案件调查报告。**

### 设计原则

- **先筛选，再开讲：** 候选案件必须有足够可靠、相互独立的来源，以及能支撑持续叙述的事实骨架。
- **全球视野：** 不限国家、地区或资料语言；尽可能查找案件发生地的当地来源。
- **事实优先：** 区分已证实事实、官方说法、证人陈述、媒体报道、争议与推测。
- **严格防剧透：** 在适当节点前不揭晓凶手或结局，也不通过语气暗示用户猜测是否正确。
- **尊重真实的人：** 不猎奇、不渲染无必要的血腥细节，不把受害者和家属的痛苦当作娱乐素材。
- **睡前叙事节奏：** 从具体的人和生活场景进入，逐步交代背景；不把讲述变成课堂、播客播报或案情简报。
- **宁缺毋滥：** 资料不足就换案，不用猜测填补空白。

### 仓库内容

```text
mist-dossier/
├── SKILL.md       # 完整技能说明与运行规范
├── README.md      # 项目介绍与使用说明
├── CHANGELOG.md   # 版本记录
└── LICENSE        # MIT License
```

### 使用方法

本项目遵循开放的 [Agent Skills 规范](https://agentskills.io/specification)。将仓库根目录作为一个 Skill 文件夹使用，或把 `SKILL.md` 放入你所使用的 Agent 产品支持的 skills 目录中。不同产品的安装位置和加载方式可能不同，请以对应产品的文档为准。

默认会话控制暗号为：

- 启动：整条消息恰好为 `🥱😶‍🌫️`
- 结束：整条消息恰好为 `😶‍🌫️😶‍🌫️`

这两个暗号只是默认配置，可以按使用者习惯修改。提及暗号本身不会触发模式切换。

### 重要限制

Skill 能约束助手如何研究和呈现信息，但不能保证所有部署环境中的绝对防剧透。若使用场景要求参与者无法提前读取结论，必须把完整研究底稿保存在参与者无权访问的独立存储中，并通过受控服务逐段提供内容。拥有服务器、数据库或日志完整权限的人仍可能读取相关信息。

本 Skill 要求尽可能使用可靠公开资料。若来源无法访问、证据互相冲突或事实无法确认，助手应明确说明限制，而不是假装完成核查。

## English

### What is Mist Dossier?

Mist Dossier is an Agent Skill for researching and narrating real-world criminal cases, with a preference for unresolved cases and lesser-known solved cases. It combines case-selection standards, source verification, evidence distinctions, spoiler control, continuity, and a calm conversational storytelling style.

Its guiding principle is simple: **tell a true story, not a case report.**

### Core features

- Research cases before recommending them; reject thin or rumor-driven candidates.
- Search globally and prioritize reliable local-language sources where possible.
- Distinguish established facts, official statements, witness accounts, reporting, disputed claims, and speculation.
- Preserve the reveal until the appropriate point in the narrative.
- Treat victims, families, witnesses, and suspects as real people.
- Tell the story gradually, without sensationalism or report-like information dumps.
- Be willing to change cases when the available evidence cannot support a responsible account.

### Installation

Use this repository as a skill folder, or copy `SKILL.md` into the skills directory supported by your agent. Installation paths and skill-loading behavior vary by product; consult the documentation for your agent.

### Spoiler and research limitations

A prompt or skill file alone cannot guarantee absolute spoiler secrecy. Deployments that require answer secrecy should keep the full research dossier in storage inaccessible to ordinary participants and release only the current segment through a controlled service. Public-source access and verification may also vary; the skill instructs the assistant to disclose uncertainty rather than invent missing facts.

## License

Released under the [MIT License](LICENSE).
