# CodexCompany Workflow

一个面向 Codex 的产品与工程工作流 Skill。把 CodexCompany 日常使用的任务接续、经理协调、专业技能路由、实现和验收整理成一个可移植的包。适用于独立开发者、小团队和需要跨会话交付软件的人。

## 能做什么

| 场景 | 工作方式 |
| --- | --- |
| 新 App 或产品 | 从问题验证、首版范围和状态数据，到设计、纵向切片、实现、验收、发布准备和反馈。 |
| 已有功能或 Bug | 复用当前规则与技术栈，沿受影响的路径补规格、修复和回归。 |
| 文案或间距微改 | 改动目标位置并直接查看实际结果。 |
| 自主迭代或复杂需求 | 经理组织体验、工程和独立 QA，记录分歧、取舍与复测结果。 |
| 换会话继续任务 | 从当前项目的权威状态与交接继续，保留最新纠正、文件归属与证据范围。 |

## 安装

在要使用的项目根目录运行。若目标目录已有同名 Skill，请先检查其版本。

~~~sh
mkdir -p .agents/skills
git clone https://github.com/kyox215/codexcompany-workflow.git .agents/skills/codexcompany-workflow
~~~

如果下载的是 ZIP，将解压后包含 `SKILL.md` 和 `references/` 的文件夹命名为 `codexcompany-workflow`，放到项目的 `.agents/skills/`。想在本机各项目使用时，可选择放到 `~/.agents/skills/`。安装后在 Codex 的 Skill 列表中确认可见，必要时重启 Codex。 [OpenAI Docs](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## 第一次使用

在 Codex 的 Skill 选择器中选择 **codexcompany-workflow**。支持 `$` 提及的客户端可直接输入 `$codexcompany-workflow`，再补一句你要完成的事。

~~~text
$codexcompany-workflow 给现有记录列表加一个状态筛选。沿用现有数据接口与设计。
完成实现，验证筛选、清空、空结果和失败重试，交付一个本地候选。
~~~

~~~text
$codexcompany-workflow 继续任务 42。先核对项目交接和最新纠正，沿现有候选处理未完成项。
~~~

想将这套流程作为项目默认方法时，可在该项目的 `AGENTS.md` 添加一句。

> 多步骤交付和任务接续按 codexcompany-workflow 选取步骤。复杂任务按授权安排独立验收，普通问答和微改走短流程。

## 包内入口

- [SKILL.md](SKILL.md) 根据任务大小决定下一步。
- [产品交付十阶段](references/delivery.md) 定义每一步的结果和通过条件。
- [协作与验收](references/operations.md) 明确经理、专业岗位、桌面排队与独立复测。
- [接续与记忆](references/continuation.md) 处理项目归属、当前决定、任务接续与留档。
- [技能路由](references/routing.md) 按平台和步骤选择已有专业能力。
- [可复制模板](references/templates.md) 包含规格、页面、状态数据、切片、派工、验收、发布和交接。

本包是 CodexCompany 截至 2026-11-03 的工作方法公开版。使用现有项目目录和任务系统即可运行；没有专用台账时，可用项目文档保存简明接续记录。原公司任务库、内部运行工具、项目数据和第三方技能分别维护。专业技能和子代理是可选能力，依赖独立 QA 的结论仍需要独立证据。

## License

[MIT](LICENSE)
