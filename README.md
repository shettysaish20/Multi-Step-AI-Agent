# 🤖 Multi-Step AI Agent System

![Python Version](https://img.shields.io/badge/python-3.12+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

A sophisticated, multi-agent AI system designed to understand complex user queries, formulate a dynamic execution plan, and achieve goals through iterative, tool-assisted steps.

---

## ✨ Key Features

-   🧠 **Autonomous Task Planning:** Dynamically creates a Directed Acyclic Graph (DAG) of tasks to solve complex problems.
-   🤖 **Specialized Agent Team:** Utilizes a variety of agents, each with a specific role:
    -   `PlannerAgent`: Creates the initial plan.
    -   `CoderAgent`: Generates and executes code.
    -   `RetrieverAgent`: Fetches information from the web or local files.
    -   `FormatterAgent`: Structures and formats output.
    -   And more...
-   🔄 **Iterative Self-Correction:** Agents can call themselves (`call_self`) to refine their work, handle sequential tasks, or build on previous results.
-   🛠️ **Extensible Tool System:** Integrates with external tools and APIs through a Model Context Protocol (MCP), allowing agents to perform actions like web searches, file operations, and data analysis.
-   📊 **Rich Terminal UI:** Provides a detailed, real-time view of the execution graph, agent logs, and final results directly in the terminal.
-   💾 **Persistent Session Memory:** Saves session history and summaries, allowing the system to learn from past interactions.

---

## 📂 Project Structure

The project is organized into distinct modules, each handling a core aspect of the agent system:

```
AI-Agent-V1/
├── 📄 main.py                  # Main entry point for the application
├── 📄 pyproject.toml           # Project dependencies and configuration
├── 📄 queries.md               # Sample queries for testing
├── 📁 action/                  # Handles code execution and sandboxing
├── 📁 agentLoop/               # Core logic for the agent execution flow
│   ├── 📄 agents.py             # Agent execution logic
│   ├── 📄 flow.py               # Main execution DAG controller
│   ├── 📄 planner.py            # Logic for the planning agent
│   └── 📄 visualizer.py         # Renders the execution graph in the terminal
├── 📁 browserMCP/              # Tools for browser interaction
├── 📁 config/                  # Agent and model configuration files
├── 📁 mcp_servers/             # External tool servers (MCP)
├── 📁 memory/                  # Manages session history and memory
├── 📁 prompts/                 # Prompt templates for each agent
└── 📁 utils/                   # Utility functions and helpers
```

---

## 🚀 Getting Started

### Prerequisites

-   Python 3.12+
-   `pip` for package management

### Installation

1.  **Clone the repository:**
    ```bash
    git clone <your-repo-url>
    cd AI-Agent-V1
    ```

2.  **Install dependencies:**
    The project uses `pyproject.toml` to manage dependencies. Install them using pip:
    ```bash
    pip install .
    ```
    *(If you use `uv`, you can run `uv pip install -e .`)*

### Running the Agent

Execute the `main.py` script to start the interactive agent session:

```bash
python main.py
```

You will be prompted to enter your query, and the agent system will take it from there!


