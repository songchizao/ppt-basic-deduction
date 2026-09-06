# PPT基本演绎法（ppt-basic-deduction）

一个面向 AI Agent（Kimi/Claude Code/workbuddy等）的可复用 Skill：**把 PPT 内容经过学习后写成一篇 Markdown 笔记。核心立场：笔记是对知识的重新表达，不是对幻灯片的逐页转录。**

将 PPT/幻灯片内容转化为一篇"理解型" Markdown 笔记。当用户提供 PPT、PPTX、PDF 课件、幻灯片截图或导出的讲义，并要求做笔记、整理、总结、消化、复盘、转 Markdown、输出学习笔记时使用本 skill。产出不是 PPT 的镜像摘要，而是一位聪明人学完后独立写出的重构笔记：第三方（人或者AI）仅凭该笔记即可完整、准确地讲解原 PPT 的全部要点与逻辑。方法论融合费曼学习法、渐进式总结、知识解构与重构；PPT 中的图片/框架图/拓扑图/逻辑图一律用 Mermaid、表格、ASCII 图或结构化文字原生还原，笔记中禁止出现页码、文件名、"幻灯片/第X页"等任何出处元数据。

## 核心特性

- **理解型重构，拒绝转录**：拆掉 PPT 的原始页序结构，按认知逻辑重新组织，用费曼学习法写作——术语就地通俗解释、凡因果必写"为什么"、写作中暴露并消灭理解盲区。
- **渐进式总结**：一句话总览 → 要点速览 → 分层展开正文 → 可选附录，读者可停在任意一层。
- **图表原生还原**：PPT 中的流程图、架构图、拓扑图、逻辑图一律用 Mermaid / Markdown 表格 / ASCII 图 / 结构化文字还原，禁止图片引用与截图。
- **零元数据**：笔记中不出现页码、文件名、"幻灯片"、"第 X 页"等任何出处标记。
- **批判性收尾**：笔记最后一章《作者的构思与不足》——还原原作者的构思逻辑（目标受众、叙事策略、取舍逻辑），并逐类排查其不足：客观限制、认知盲区、有意隐藏（每条判断附依据，推测明确标注）。

## 方法论

费曼学习法（用通俗语言讲清概念并自检理解盲区）× 渐进式总结（由详到略分层提炼）× 知识解构与重构（拆解原结构后按理解重新组织）。

## 安装

### 方式一：作为 Kimi Work / Claude Code 兼容 Skill

将 `ppt-basic-deduction/` 目录复制到 Skills 目录：

- Kimi Work：`%APPDATA%\kimi-desktop\daimon-share\daimon\skills\`
- Claude Code 用户级：`~/.claude/skills/` 或 `~/.config/agents/skills/`
- 项目级：`<项目>/.agents/skills/`

### 方式二：导入 .skill 分发包

`ppt-basic-deduction.skill` 是 zip 格式的分发包（见 Releases），解压后按方式一放置即可。

## 使用

向 Agent 提供 PPT / PPTX / PDF 课件 / 幻灯片截图，并说"用 PPT基本演绎法整理成笔记"即可触发。输出为单个自包含的 `.md` 文件。

## 目录结构

```
ppt-basic-deduction/
├── SKILL.md                      # Skill 主文件：铁律、六步工作流、图表还原规则、自检清单
└── references/
    └── output-template.md        # 输出结构模板 + 好/坏写法范例 + 收尾章节范例
```

## License

MIT
