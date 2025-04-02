
# 🧠 Codebrain

> The Thinking Engine Behind Every Line of Code

**Codebrain** is a brain-inspired multi-agent AI system that solves Python coding interview problems through cognitive simulation. It integrates:
- ✅ LangChain agents for reasoning
- ✅ A knowledge graph memory (Neo4j) for long-term learning
- ✅ Structured output parsing for explainability
- ✅ Dynamic code generation with LLMs

---


## 🚀 Features

- 🧠 **Multi-Agent Architecture**  
  Modeled after human cognitive faculties: Sense, Memory, Intellect, Action, and Ego.

- 📘 **Knowledge Graph Memory**  
  Uses Neo4j to store problems, strategies, concepts, and code interlinked as nodes.

- 🧩 **Modular Strategy Planning**  
  Generates multiple strategy paths and synthesizes Python implementations dynamically.

- 🔁 **Self-Learning Engine**  
  Reinforces and expands its knowledge graph with every new problem.

---

## 📦 Installation

```bash
git clone https://github.com/mindverse-computing/codebrain.git
cd codebrain
pip install -r requirements.txt
```

Then configure your `.env` file:

```bash
cp .env.example .env
```

Add the following keys:

```
OPENAI_API_KEY=your_openai_key
NEO4J_URI=bolt://localhost:7687
NEO4J_USER=neo4j
NEO4J_PASSWORD=yourpassword
```

---

## 🧪 Usage Example

```bash
python examples/solve_problem.py
```

Input:
```
Find the longest increasing subsequence in an array.
```

Output:
- Problem Introduction
- Strategy Options
- Code for Each Strategy
- Selected Best Solution
- Stored to Knowledge Graph

---

## 🧠 Architecture Overview

```mermaid
graph TD
  A[User Query] --> S[Sense Agent]
  S --> I[Intellect Agent]
  I -- YES --> M[Memory Agent]
  M <--> G[Knowledge Graph]
  M --> E[Ego Agent]
  I -- NO --> O[Orchestrator Agent]
  O --> A1[Action Agent 1]
  O --> A2[Action Agent 2]
  O --> A3[Action Agent 3]
  A1 <--> R1[Rection Agent 1]
  A2 <--> R2[Rection Agent 2]
  A3 <--> R3[Rection Agent 3]
  R1 --> AA[Assembler Agent]
  R2 --> AA[Assembler Agent]
  R3 --> AA[Assembler Agent]
  AA --> E[Ego Agent]
  E --> G[Knowledge Graph]
  E --> U[Response User]

  %% Styling green paths (YES path)
  linkStyle 2 stroke:green,stroke-width:2px      %% I --> M
  linkStyle 3 stroke:green,stroke-width:2px      %% M <--> G (first half)
  linkStyle 4 stroke:green,stroke-width:2px      %% M --> E

  %% Styling red paths (NO path)
  linkStyle 5 stroke:red,stroke-width:2px        %% I --> O
  linkStyle 6 stroke:red,stroke-width:2px        %% O --> A1
  linkStyle 7 stroke:red,stroke-width:2px        %% O --> A2
  linkStyle 8 stroke:red,stroke-width:2px        %% O --> A3
  linkStyle 9 stroke:red,stroke-width:2px        %% A1 <--> R1
  linkStyle 10 stroke:red,stroke-width:2px       %% A2 <--> R2
  linkStyle 11 stroke:red,stroke-width:2px       %% A3 <--> R3
  linkStyle 12 stroke:red,stroke-width:2px       %% R1 --> AA
  linkStyle 13 stroke:red,stroke-width:2px       %% R2 --> AA
  linkStyle 14 stroke:red,stroke-width:2px       %% R3 --> AA
  linkStyle 15 stroke:red,stroke-width:2px       %% AA --> E
  linkStyle 16 stroke:red,stroke-width:2px       %% E --> G
  linkStyle 17 stroke:red,stroke-width:2px       %% E --> U
```



---

## 📚 Directory Guide

| Folder       | Purpose                          |
|--------------|----------------------------------|
| `agentome/`  | Agent classes & orchestration    |
| `examples/`  | CLI and problem input            |
| `notebooks/` | Jupyter walkthrough     

### Files

```
codebrain/
│
├── README.md                   # Project introduction and usage guide
├── requirements.txt            # Python dependencies
├── .env.example                # Sample env file with API keys
├── .gitignore                  # Ignored files
│
├── agentome/
│   ├── __init__.py
│   ├── base.py                 # Base Agent class
│   ├── sense_agent.py          # Problem comprehension
│   ├── memory_agent.py         # Graph-based memory access
│   ├── intellect_agent.py      # Strategy generation
│   ├── action_agent.py         # Strategy-to-code agent
│   ├── ego_agent.py            # Evaluation & output assembly
│   ├── knowledge_graph.py      # Neo4j connector and logic
│   └── system.py               # Orchestration of agents
│
├── examples/
│   ├── solve_problem.py        # Sample usage script
│   └── problems.txt            # Sample problems for input
│
└── notebooks/
    └── demo.ipynb              # Jupyter notebook walkthrough


```         

---

## 🛠️ Tech Stack

- [LangChain](https://github.com/hwchase17/langchain)
- [Neo4j](https://neo4j.com/)
- [OpenAI GPT-4](https://platform.openai.com/)
- [Python 3.9+](https://www.python.org/)

---

## 📈 Future Directions

- ✅ LangGraph integration for visual state workflows
- ✅ Curriculum Agent for guided learning
- ✅ UI for interactive graph-based reasoning
- ✅ Auto-evaluator with test case verification

---

## 🤝 Contributing

Pull requests are welcome! For major changes, open an issue first.

---

## 📄 License

MIT © 2025 Mindverse Computing

---

## 🌐 Project Status

Actively developed. Reach out to `@mindverse` to collaborate! 

-------

# Join Us

Join our slack channel: [bit.ly/mc-slack](bit.ly/mc-slack)
