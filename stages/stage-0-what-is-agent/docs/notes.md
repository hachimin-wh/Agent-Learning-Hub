# Stage 0: Understand What An Agent Is

## Checklist

- [ ] 区分 chatbot、workflow、agent、multi-agent
- [x] 理解 agent 的基本循环：observe -> think -> act -> observe
- [ ] 明白什么时候不该用 agent：任务可预测、流程稳定、普通脚本能解决时，agent 反而增加不确定性
- [ ] 读完 Anthropic: Building effective agents
- [ ] 读完 OpenAI: A practical guide to building agents

## 核心要点

### Hello-Agents：Chapter1（初识智能体）
1. Agent 循环是**感知 -> 思考 -> 行动 -> 再感知**，适用于传统 agent（规则匹配、搜索算法、贝叶斯推断）和现代 LLM agent。
2. React 是实现 Agent 循环的具体工程范式，**思考(Thought) -> 行动(Action) -> 观察(Observation)** ，其中“思考”由 LLM 完成，“行动”是由 LLM 输出的格式化工具调用，“观察”作为工具调用结果反馈给下一轮循环。
```python
    while(flag < n) {
        thought = llm.generate(system_prompt, history, available_tools) 
        observation = available_tools[thought.tool_name](**kwarg)
        history.append(observation)
    }
```

### Hello-Agents：Chapter2（智能体发展史）

第二章的主线是**知识来源的变化**：从人写规则，到从数据中学，到从交互中学，再到预训练模型配合记忆 / 规划 / 工具。

1. **知识来源的演变**。符号主义靠专家把知识写成规则，联结主义从数据中学参数，强化学习从环境奖励中学策略。三者解决的问题不同：规则可解释但难穷举，参数能泛化但难解释，强化学习能学长期决策但交互成本高。
2. **早期系统的价值与局限**。专家系统、ELIZA、SHRDLU 都证明：在封闭域内，规则系统可以表现出看似智能的行为——推理、对话、规划。但搬到开放世界，知识无法穷举，状态变化难以显式维护，输入稍超预设系统就失效。
3. **预训练 LLM 补上了通用起点**。预训练让模型从海量数据中获得了广泛的语言和世界知识，新任务可以通过上下文示例或微调快速适配，不必从零开始。但预训练模型的知识可能错误或过时，所以它不能单独做 Agent 的全部。
4. **现代 Agent 是三条线索的汇合**。LLM 负责理解开放指令和规划（承接联结主义），工具接口显式约束"能做什么、怎么执行"（承接符号主义的动作规则），反馈循环根据 Observation 调整下一步（承接智能体与环境的交互思想）。这个结构正好接上第一章的 Agent 循环：感知 → 思考 → 行动 → 再感知。

### Anthropic：Building effective agents

（待读）

### OpenAI：A practical guide to building agents

（待读）

## 概念辨析
- chatbot 是什么？
- workflow 是什么？
- agent 是什么？
- multi-agent 是什么？

## 阶段产出：我的场景为什么需要 agent，而不是普通 workflow？

> 按 README 要求写一页短笔记。建议覆盖：场景描述、为什么 workflow 不够、引入 agent 带来的新问题（不确定性、成本、评测难度）、结论。

（待写）
