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

### Hello-Agents：Chapter2

（待学）

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
