# AI Ask Engineering Partner

这是面向真实企业软件开发和个人工程成长的 Ask 模式协作规范。开发者保有设计、编码、代码应用、测试及提交的决定权；AI 扮演具备独立判断能力的工程师同事、审查者和有节制的教练。

## 目录

```text
AI_Ask_Engineering_Partner/
├── SYSTEM_PROMPT.md
├── README.md
├── RESEARCH_NOTES.md
├── TASK_EXAMPLES.md
└── skills/
    ├── ask-development/
    │   ├── SKILL.md
    │   └── references/
    ├── ask-debug-review/
    │   ├── SKILL.md
    │   └── references/
    ├── ask-engineering-growth/
    │   ├── SKILL.md
    │   └── references/
    └── ask-coding-practice/
        ├── SKILL.md
        └── references/
```

## 直接使用

1. 将 `SYSTEM_PROMPT.md` 全文配置为支持系统指令的客户端的常驻提示词。
2. 支持 Skills 的环境中，将四个 Skill 目录整体安装至该客户端指定目录。保留 references 文件，不要只复制 SKILL.md。不同平台的自动触发实现有所区别，应以实际结果验证。
3. 普通 Chat/IDE Ask 环境若无技能加载能力，将当前任务对应的 SKILL.md 及必要的 references 内容附在会话中。纯文本文件不会自动成为模型已知上下文。
4. 仓库语言版本、技术栈、构建步骤、代码规范和数据安全要求由项目文件（如 AGENTS.md、README）及团队制度说明，避免塞入通用系统提示词。

## 工作中的默认分工

日常任务使用“一起做”：AI 提供必要背景与评审，人负责真实关键判断和一段核心逻辑编码。紧急任务说“赶进度”；专项练习说“我先写”；需要立即答案则明确说“直接给答案”。

一次一文件约束只涉及对话中的代码交付，不等同于 Git 变更范围。AI 未运行测试时，必须写明“待验证”。避免将 AI 生成或人工复制直接记为功能完成。

## 能力培养原则

高频语法需要亲手写，设计能力需要亲自做取舍，调试能力需要实际收集证据，架构能力需要理解依赖与演进成本。练习应包括尝试、反馈、修正和过一段时间后不看答案的迁移任务。训练量依据工作负荷调整，不盲目追求时长或行数。

可在 `TASK_EXAMPLES.md` 中选择一个真实场景检查 AI 是否遵守协作协议。`RESEARCH_NOTES.md` 列出公开规范与适用边界；企业制度优先。
