# Learning Progress

> 打勾规则：完成一项在这里打勾，不改 README.md。状态：`未开始` / `进行中` / `完成`。
> 学习过程与产出在各 stage 目录自表达：`stages/<stage>/docs/`（笔记、翻译、产出）、`stages/<stage>/code/`（练习脚本）。

## Learning Todo List

### Stage 0: Understand What An Agent Is — 进行中

- [ ] 区分 chatbot、workflow、agent、multi-agent
- [ ] 理解 agent 的基本循环：observe -> think -> act -> observe
- [ ] 明白什么时候不该用 agent：任务可预测、流程稳定、普通脚本能解决时，agent 反而增加不确定性
- [ ] 读完 Anthropic: Building effective agents
- [ ] 读完 OpenAI: A practical guide to building agents

### Stage 1: Build A Minimal Agent Loop

- [ ] 会用一个 LLM API 完成普通对话
- [ ] 会让模型输出结构化 JSON
- [ ] 会定义一个工具函数（search、calculator、read_file）
- [ ] 会解析模型的 tool call / function call
- [ ] 会执行工具，并把工具结果喂回模型
- [ ] 会给 agent loop 加最大步数、超时和错误处理

### Stage 2: Learn Tool Use, RAG, And Memory

- [ ] 会做检索增强生成：chunk、embed、retrieve、answer with citations
- [ ] 会把搜索、数据库、文件、浏览器、代码执行接成工具
- [ ] 会区分短期上下文、会话记忆、长期记忆
- [ ] 会处理工具失败、空结果、重复调用、幻觉引用
- [ ] 会让 agent 在回答里给出来源或证据

### Stage 3: Study One Modern Agent Harness

- [ ] 读懂一个 agent harness 的目录结构
- [ ] 找出它的 agent loop、tool registry、permission gate、session store、context compaction
- [ ] 跑通它的最小示例，并加一个自己的工具
- [ ] 观察一次完整 trace，解释每一步为什么发生
- [ ] 把同一个任务分别用「裸 agent loop」和「harness」实现，对比差异

### Stage 4: Multi-Agent Is Coordination, Not Magic

- [ ] 理解 planner / executor / reviewer / critic / router 等常见角色
- [ ] 学会用 supervisor 或 graph 管理多 agent
- [ ] 会定义每个 agent 的职责边界、输入输出 schema、停止条件
- [ ] 会处理循环、争论、任务漂移、上下文膨胀
- [ ] 会判断什么时候单 agent 更好

### Stage 5: Learn Skills, Protocols, And Capability Packaging

- [ ] 理解 Skill / Tool / Prompt / MCP 的区别
- [ ] 阅读 Claude Code Skills 的文件结构和触发机制
- [ ] 阅读 OpenClaw Skills 的加载、作用域和安全边界
- [ ] 写一个最小 SKILL.md（name、description、何时使用、步骤、验收标准）
- [ ] 给 skill 加一个脚本或模板文件
- [ ] 给 skill 写一个 smoke test

### Stage 6: Browser And Computer-Use Agents

- [ ] 理解 browser agent 和普通 API tool 的区别
- [ ] 会用 Playwright 或 browser-use 做网页观察和点击
- [ ] 会给浏览器操作加安全限制
- [ ] 会处理页面变化、弹窗、加载失败、元素定位失败
- [ ] 会记录截图、DOM、动作日志，方便复盘

### Stage 7: Evaluation, Observability, And Safety

- [ ] 为 agent 准备固定测试集，而不是只看 demo
- [ ] 记录成功率、失败原因、工具调用次数、成本、延迟
- [ ] 会看 trace，定位失败发生在 prompt、工具、检索、模型还是状态管理
- [ ] 给危险工具加人工确认
- [ ] 了解 prompt injection、data exfiltration、tool abuse 等风险
- [ ] 会用回归测试防止能力退化

### Stage 8: Ship A Real Agent

- [ ] 有明确用户、明确任务、明确成功标准
- [ ] 有日志、trace、错误重试、超时、成本上限
- [ ] 有权限边界和人工确认机制
- [ ] 有部署方式：CLI、Web app、Slack bot、GitHub Action 或后台任务
- [ ] 有 README：怎么运行、怎么配置 key、怎么扩展工具、有哪些限制

## Project Ladder

| Level | Project | 状态 |
| --- | --- | --- |
| 1 | Calculator Agent | 未开始 |
| 2 | Web Research Agent | 未开始 |
| 3 | PDF QA Agent | 未开始 |
| 4 | Coding Review Agent | 未开始 |
| 5 | Browser Agent | 未开始 |
| 6 | Claude Code-like Nano Agent | 未开始 |
| 7 | OpenClaw-like Gateway | 未开始 |
| 8 | Reusable Skill Pack | 未开始 |
| 9 | Multi-Agent Writer | 未开始 |
| 10 | Personal Agent | 未开始 |
| 11 | Production Harness | 未开始 |
