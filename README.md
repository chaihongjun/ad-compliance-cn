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
npx skills add chaihongjun/ad-compliance-cn --yes
```

## 触发语

> "帮我看下这个广告合不合法"、"广告法审查"、"广告文案合规"、"医疗广告合规"、"ad compliance review"、"广告内容审核"、"广告法合规审查"、"广告法"

支持纯文本和含图片的广告审查。图片审查由用户提供画面描述或直接提交图片，重点检查画面禁用元素、嵌入文字、暗示误导、比较诋毁、包装混淆及医疗广告画面限制。

触发后执行 13 步审查流程（Step 0 四性前置判断 → Step 1-12 逐级审查），最终输出结构化合规报告。

## 文件结构

- `SKILL.md` — 主技能文件，13 步审查流程（含图片视觉审查）
- `references/` — 参考文档：
  - 法规原文（8 份）：
    - 广告法（74 条）
    - 互联网广告管理办法（32 条）
    - 医疗广告管理办法（23 条）
    - 医疗广告认定指南（12 条）
    - 认定指南解读
    - 反不正当竞争法（40 条，2025 修订）
    - 执法指南（一）：广告四性判断
    - 执法指南（二）：管辖规则
  - [案例演示](references/CASES.md) — 3 个完整审查案例
  - [常见疑问解答](references/FAQ.md) — 10 条 FAQ
  - [审查报告模板](references/REPORT_TEMPLATE.md) — 输出格式规范
  - [易错点清单](references/GOTCHAS.md) — 8 条常见非直觉陷阱
  - [审查辅助参考](references/GUIDANCE.md) — 边界模糊引导 + 罚款速查表

## License

MIT
