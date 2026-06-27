# ad-compliance-cn

中文广告合规审查 AI Agent Skill。

依据《中华人民共和国广告法》（2021修正）、《互联网广告管理办法》（2023·总局第72号令）、《医疗广告管理办法》（2007施行）、《医疗广告认定指南》（2025年公告第29号）、《中华人民共和国反不正当竞争法》（2025修订）、《广告法适用问题执法指南（一）（二）》等法规，对商业广告内容进行系统性合规审查。

## 安装

```bash
npx skills add chaihongjun/ad-compliance-cn
```

安装后 skill 位于对应 Agent 的 skill 目录中。支持 Claude Code、Cursor、Codex、GitHub Copilot、OpenCode、Gemini CLI 等。

### 静默安装

```bash
npx skills add chaihongjun/ad-compliance-cn --yes --global
```

## 触发语

> "帮我看下这个广告合不合法"、"广告法审查"、"广告文案合规"、"医疗广告合规"、"ad compliance review"、"广告内容审核"、"广告法合规审查"、"广告法"

触发后执行 12 步审查流程（Step 0 四性前置判断 → Step 1-11 逐级审查），最终输出结构化合规报告。

## 文件结构

- `SKILL.md` — 主技能文件，12 步审查流程 + 违规定级 + 罚款速查 + 报告模板
- `references/` — 8 份法规原文：
  - 广告法（74 条）
  - 互联网广告管理办法（32 条）
  - 医疗广告管理办法（23 条）
  - 医疗广告认定指南（12 条 + 解读）
  - 反不正当竞争法（40 条，2025 修订）
  - 执法指南（一）：广告四性判断
  - 执法指南（二）：管辖规则

## License

MIT
