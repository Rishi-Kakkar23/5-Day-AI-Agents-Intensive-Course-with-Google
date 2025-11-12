# 🚀 5-Day AI Agents Intensive Course with Google

Welcome to the **5-Day AI Agents Intensive Course**! This comprehensive course teaches you how to build sophisticated AI agents using Google's **Agent Development Kit (ADK)** and the **Gemini API**.

## 📚 Course Overview

This hands-on course guides you through building AI agents from basic concepts to advanced multi-agent systems. Each day focuses on specific aspects of agent development with practical Jupyter notebooks and exercises.

### What You'll Learn

- ✅ Build AI agents that can take actions using tools like Google Search
- ✅ Design and orchestrate multi-agent systems with different workflow patterns
- ✅ Create custom tools and integrate with external APIs
- ✅ Manage agent sessions and implement persistent memory
- ✅ Apply best practices for production-ready agent applications

## 🗓️ Course Structure

### Day 1: Foundations - Agents & Architectures
**Topics Covered:**
- From Prompt to Action: Building your first AI agent
- Agent architectures and workflow patterns
- Multi-agent systems and orchestration
- Sequential, Parallel, and Loop workflow patterns

**Notebooks:**
- [`day-1a-from-prompt-to-action.ipynb`](Day%201/day-1a-from-prompt-to-action.ipynb) - Introduction to AI agents and ADK basics
- [`day-1b-agent-architectures.ipynb`](Day%201/day-1b-agent-architectures.ipynb) - Multi-agent systems and coordination

### Day 2: Tools & Interoperability
**Topics Covered:**
- Understanding agent tools and their importance
- Creating custom function tools
- Building agent tools (using agents as tools)
- Code execution with BuiltInCodeExecutor
- Tool types: Function Tools, Agent Tools, MCP Tools, OpenAPI Tools

**Notebooks:**
- [`day-2a-agent-tools.ipynb`](Day%202/day-2a-agent-tools.ipynb) - Building custom tools
- [`day-2b-agent-tools-best-practices.ipynb`](Day%202/day-2b-agent-tools-best-practices.ipynb) - Advanced tool patterns

### Day 3: Context Engineering & Memory
**Topics Covered:**
- Session management and stateful agents
- Persistent sessions with DatabaseSessionService
- Context compaction and management
- Session state and cross-session data sharing
- Long-term memory systems

**Notebooks:**
- [`day-3a-agent-sessions.ipynb`](Day%203/day-3a-agent-sessions.ipynb) - Session management
- [`day-3b-agent-memory.ipynb`](Day%203/day-3b-agent-memory.ipynb) - Memory systems

## 🛠️ Prerequisites

### Required Tools
- Python 3.11 or higher
- [Google AI Studio API Key](https://aistudio.google.com/app/api-keys)
- Jupyter Notebook or Kaggle account

### Installation

To run the notebooks locally, install the Agent Development Kit:

```bash
pip install google-adk
```

## 🚀 Getting Started

### Option 1: Run on Kaggle (Recommended for Beginners)
1. Visit the [Kaggle 5-day Agents course](https://www.kaggle.com/)
2. Verify your account with a phone number
3. Click "Copy and Edit" on any notebook
4. Add your `GOOGLE_API_KEY` to Kaggle Secrets
5. Run cells in order from top to bottom

### Option 2: Run Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/Rishi-Kakkar23/5-Day-AI-Agents-Intensive-Course-with-Google.git
   cd 5-Day-AI-Agents-Intensive-Course-with-Google
   ```

2. Install dependencies:
   ```bash
   pip install google-adk
   ```

3. Set up your API key:
   ```bash
   export GOOGLE_API_KEY="your-api-key-here"
   ```

4. Launch Jupyter:
   ```bash
   jupyter notebook
   ```

5. Open any notebook from the Day folders and start learning!

## 📖 Reading Materials

The [`Reading material`](Reading%20material/) folder contains supplementary PDFs covering:
- Agent Tools & Interoperability with Model Context Protocol (MCP)
- Context Engineering: Sessions & Memory
- Day 1 course materials

## 🎯 Key Concepts

### Agent Development Kit (ADK)
ADK is Google's flexible and modular open-source framework for building and deploying AI agents. It's optimized for Gemini models but is model-agnostic and compatible with other frameworks.

**Available SDKs:** Python, Go, Java

### Core Components
- **Agents**: AI entities that can reason and take actions
- **Tools**: Functions and services that agents can use
- **Sessions**: Containers for conversation history
- **Memory**: Long-term storage for agent knowledge
- **Runners**: Orchestrators that manage agent execution

### Agent Patterns
1. **Sequential Agents**: Execute tasks in a fixed, linear order
2. **Parallel Agents**: Run independent tasks concurrently
3. **Loop Agents**: Iterate and refine outputs through feedback cycles
4. **LLM Orchestrator**: Let the model dynamically decide workflow

## 💡 Example: Your First Agent

```python
from google.adk.agents import Agent
from google.adk.runners import InMemoryRunner
from google.adk.tools import google_search

# Create an agent with Google Search capability
agent = Agent(
    name="helpful_assistant",
    model="gemini-2.5-flash-lite",
    description="A simple agent that can answer questions",
    instruction="You are a helpful assistant. Use Google Search for current info.",
    tools=[google_search],
)

# Run the agent
runner = InMemoryRunner(agent=agent)
response = await runner.run_debug("What's the weather today?")
```

## 🤝 Contributing

This course is designed for learning purposes. Feel free to:
- Report issues or bugs
- Suggest improvements
- Share your learning experiences

## 📝 License

Copyright 2025 Google LLC. Licensed under the Apache License, Version 2.0.

See the LICENSE file or visit: https://www.apache.org/licenses/LICENSE-2.0

## 🔗 Useful Resources

- [ADK Official Documentation](https://google.github.io/adk-docs/)
- [ADK Python Quickstart](https://google.github.io/adk-docs/get-started/python/)
- [Gemini API Documentation](https://ai.google.dev/gemini-api/docs)
- [Google AI Studio](https://aistudio.google.com/)
- [Kaggle Discord](https://discord.com/invite/kaggle) - Get help and connect with other learners

## ⚠️ Important Notes

- **No Submission Required**: These notebooks are for hands-on practice and learning only
- **API Costs**: Be mindful of API usage; use the Gemini API responsibly
- **Rate Limits**: Avoid running all cells at once to prevent hitting QPM limits
- **Secrets Security**: Never share your API keys or authentication tokens

## 🎓 Course Credits

Created by Google AI team with contributions from:
- [Kristopher Overholt](https://linkedin.com/in/koverholt)
- [Laxmi Harikumar](https://www.linkedin.com/in/laxmi-harikumar/)
- [Sampath M](https://www.linkedin.com/in/msampathkumar/)

---

**Ready to build your first AI agent? Start with Day 1! 🚀**
