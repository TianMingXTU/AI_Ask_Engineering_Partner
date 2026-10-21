# 公开工程实践与方法依据

## 方法与限制

本次优先核对公开的**一手**工程实践资料：OpenAI 工程案例、Google Engineering Practices、Microsoft Engineering Fundamentals、Martin Fowler 的重构/TDD 说明、OWASP 安全实践、Anthropic Skills 文档与 DORA 指标。公开文档体现各机构公开主张，**不能推定每个大厂团队或某位资深开发者都按同一流程工作**，也不代表获得其官方认可。用户自定义的 Ask 模式、人工审批、逐文件代码交付是**本协作协议**，不是这些机构的统一规则。

## 事实来源与采纳范围

1. OpenAI《How OpenAI Uses Codex to Accelerate Engineering》：对较大任务先以 Ask Mode 形成计划并补足上下文。本文只采纳计划/执行分离，不照搬其随后切换 Code Mode 的流程。https://openai.com/business/guides-and-resources/how-openai-uses-codex/
2. OpenAI《Rethinking skills and prompts for GPT-6 Astra》（2026-09-11）：重新审视冗长指令与 Skill 描述，减少常驻上下文。采纳精简 Prompt、任务触发 Skill 的方向。https://developers.openai.com/blog/rethinking-skills-and-prompts-for-gpt-6-astra
3. Anthropic《Agent Skills Overview》与《Equipping agents for the real world with Agent Skills》：Skill frontmatter（name/description）、加载主体及按需读取参考资源的渐进加载架构。按目录构建，是否自动加载取决于工具。https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview ; https://www.anthropic.com/research/equipping-agents-for-the-real-world-with-agent-skills
4. Google《What to look for in a code review》：设计、正确性、复杂度、测试、命名与注释；拒绝为未知需求过度泛化；评论解释为什么。https://google.github.io/eng-practices/review/reviewer/looking-for.html
5. Google《Small CLs》：自包含的小变更便于审查和回滚；自包含并不意味着每个 PR 只能一文件，通常需要配套测试。https://google.github.io/eng-practices/review/developer/small-cls.html
6. Microsoft《Engineering Fundamentals: Pull Requests》和《Reviewer Guidance》：审查业务正确性、测试和可读性，并利用自动化验证；避免范围外意见拖住当前 PR。https://microsoft.github.io/code-with-engineering-playbook/code-reviews/pull-requests/ ; https://microsoft.github.io/code-with-engineering-playbook/code-reviews/process-guidance/reviewer-guidance/
7. Martin Fowler《Refactoring》与《Test Driven Development》（2023-12-11）：将重构拆为行为保持的小步骤；TDD 采用测试—实现—重构的循环。本协议建议按适合任务的风险使用，而非机械要求所有代码都 TDD。https://martinfowler.com/books/refactoring.html ; https://martinfowler.com/bliki/TestDrivenDevelopment.html
8. OWASP《Secure Code Review》与《Secure Coding Practices》：风险驱动的安全审查、输入验证、鉴权、秘密管理、信任边界与依赖供应链。https://owasp.github.io/DevSecOpsGuideline/2-Process/2-2-Develop/2-2-3-Secure-Code-Review/ ; https://owasp.github.io/www-project-secure-coding-practices-quick-reference-guide/stable-en/02-checklist/
9. DORA《Software Delivery Performance Metrics》：交付既要快也要稳，不能只用代码产出量或 PR 数量评价工程表现。本协议只引用其理念，不自行宣称改善了 DORA 指标。https://dora.dev/guides/dora-metrics/

## 在本协作协议中的应用

- 小幅、可审查且自洽的改动有助于审查质量；对话每轮一个文件是开发者自己的人工审核约定，而非公司统一规定。
- 对中等及高风险工作先确定接口契约、验收和风险；常规小问题直接解决。
- 审查聚焦正确性、安全、数据一致性、测试和可维护性，降低纯风格争执。
- 系统提示词保持长期行为约束，专业详细工作流程通过独立 Skill 和 references 按需加载。
- 编程能力训练强调检索、独立输入、真实编译调试、针对性反馈、延迟再现和变式迁移。训练层级与提示阶梯是本协作协议的设计，并不声称是上述企业的统一制度。

## 适用边界

这些链接均为公开工程文档或工程实践分享，不能推断所有资深程序员、所有团队都执行相同程序；也不构成某公司的官方认可。如何分配 AI 与人类的编码工作须服从组织政策与项目风险。独立编程成长效果需要通过真实任务、测试记录和重复练习检验，目前没有受控实证能够保证某个固定训练量的结果。
