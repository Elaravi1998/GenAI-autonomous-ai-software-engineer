# 🤖 Autonomous AI Software Engineer

> 🧠 An advanced agentic AI system that analyzes software-engineering tasks, understands a repository, creates an implementation plan, proposes code changes, validates them with tests, performs AI-assisted review, and routes risky actions through human approval.

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://www.python.org/)
[![AI Agents](https://img.shields.io/badge/AI-Agents-purple)](#-architecture)
[![MCP](https://img.shields.io/badge/MCP-Ready-green)](#-mcp-integration)
[![RAG](https://img.shields.io/badge/Code-RAG-orange)](#-code-rag)

## 🚀 Project Overview

The **Autonomous AI Software Engineer** is a portfolio-grade GenAI project exploring how an AI agent can assist developers across the software-development lifecycle.

```text
🎫 Issue / Request
       ↓
🧭 Planner Agent
       ↓
🗂️ Repository Analyzer
       ↓
✍️ Code Generation Agent
       ↓
🧪 Test Agent
       ↓
🔎 Critic Agent
       ↓
🛡️ Human Approval Gate
       ↓
🐙 Git / GitHub / MCP
```

The included notebook is a reproducible local prototype. Production extensions can connect GitHub, MCP, sandboxed execution, real test runners, and an LLM.

## 🎯 Objectives

- 🤖 Build an agentic software-engineering workflow
- 🧠 Practice multi-step task planning
- 🗂️ Analyze repositories and dependencies
- ✍️ Generate structured code-change proposals
- 🧪 Automatically validate generated changes
- 🔎 Review patches for correctness and security risks
- 🛡️ Keep humans in control of high-impact actions
- 📊 Measure agent quality and reliability

## ✨ Key Features

### 🧭 Intelligent Task Routing
Classifies requests into feature development, bug fixing, testing, or refactoring.

### 🗂️ Repository Analysis
Inspects project files and basic structure to provide context.

### 🧠 Planning Agent
Converts a natural-language issue into verifiable implementation steps.

### ✍️ Code Agent
Produces a structured patch proposal instead of blindly editing production code.

### 🧪 Test Agent
Runs validation checks and reports pass/fail results.

### 🔎 Critic Agent
Reviews changes for correctness, maintainability, security risks, missing tests, and regressions.

### 🛡️ Human-in-the-Loop
Commits, pull requests, deployments, deletion, and production access should require explicit approval.

## 🏗️ Architecture

```text
Developer
   │
   ▼
🧭 Planner
   │
   ▼
🗂️ Repository Context
   │
   ▼
✍️ Coding Agent
   │
   ▼
🧪 Test Agent
   │
   ▼
🔎 Critic
   │
   ▼
🛡️ Approval
   │
   ▼
🐙 GitHub / MCP
```

## 🧰 Technology Stack

| Area | Technology |
|---|---|
| 🐍 Language | Python |
| 🧠 LLM | OpenAI-compatible APIs / OpenRouter |
| 🤖 Agents | Custom orchestration, LangGraph-ready |
| 🔌 Tools | MCP-ready |
| 🧠 Code RAG | Vector database integration planned |
| 🧪 Testing | pytest / project-specific runners |
| 🔍 Quality | Ruff / ESLint / mypy / Semgrep |
| 🐙 Version Control | Git + GitHub |
| 🌐 UI | Streamlit / React planned |

## 📁 Project Structure

```text
autonomous-ai-software-engineer/
├── 📓 Autonomous_AI_Software_Engineer.ipynb
├── 📄 README.md
├── 📄 requirements.txt
├── 📄 .env.example
├── 📄 .gitignore
├── 🤖 agents/
├── 🔌 tools/
├── 🧠 rag/
├── 🧪 tests/
└── 📁 docs/
```

## ⚙️ Installation

```bash
git clone https://github.com/YOUR_USERNAME/autonomous-ai-software-engineer.git
cd autonomous-ai-software-engineer

python -m venv .venv

# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
```

## 📓 Run the Notebook

```bash
pip install jupyter
jupyter notebook
```

Open:

```text
Autonomous_AI_Software_Engineer.ipynb
```

The notebook's core workflow does not require a paid LLM API.

## 🤖 Optional LLM Integration

```env
OPENAI_API_KEY=your_api_key
OPENAI_MODEL=your_model
```

⚠️ Never commit API keys. Add `.env` to `.gitignore`.

## 🔄 Agent Workflow

1. 🎫 Developer submits an issue
2. 🧭 Planner decomposes the request
3. 🗂️ Repository agent retrieves relevant context
4. ✍️ Coding agent creates a patch
5. 🧪 Test agent validates it
6. 🔎 Critic agent reviews it
7. 🛡️ Human approves or rejects
8. 🐙 GitHub agent can create a branch/commit/PR in the production version

## 🧠 Code RAG

For large repositories:

```text
Repository
   ↓
Code Parser
   ↓
Chunking
   ↓
Embeddings
   ↓
Vector Database
   ↓
Semantic Retrieval
   ↓
Relevant Code Context
   ↓
LLM
```

This avoids sending the entire codebase to the model.

## 🔌 MCP Integration

A future version can expose engineering capabilities through Model Context Protocol:

```text
🤖 AI Engineer
      ↓
🔌 MCP Client
 ┌────┼──────────────┐
 ↓    ↓              ↓
📁 FS 🐙 GitHub     🧪 Tests
```

Potential tools:

- `read_file`
- `search_code`
- `list_files`
- `run_tests`
- `git_diff`
- `create_branch`
- `create_commit`
- `create_pull_request`

## 🧪 Evaluation Metrics

| Metric | Description |
|---|---|
| 🎯 Task Success | Did the agent solve the issue? |
| 🧪 Test Pass Rate | How often changes pass tests |
| 🔁 Repair Rate | Ability to repair failed changes |
| 🧠 Planning Quality | Quality of task decomposition |
| 🛡️ Safety Rate | Avoidance of unauthorized actions |
| ⏱️ Latency | Time to complete an engineering task |
| 💰 Cost | Token/API/tool cost |
| 👨‍💻 PR Acceptance | Developer acceptance rate |

## 🛡️ Security & Responsible AI

Production deployments should:

- 🔐 Protect API keys and credentials
- 🧱 Run generated code in a sandbox
- ⏱️ Apply execution timeouts
- 💾 Restrict filesystem access
- 🌐 Restrict network access
- 🛡️ Require approval before deployment
- 🧪 Run static/security analysis
- 👀 Log agent actions and tool calls
- 🚫 Block destructive commands by default
- 🔑 Use least-privilege GitHub tokens

## 🗺️ Roadmap

- [x] 🧭 Task routing
- [x] 🗂️ Repository analysis
- [x] 🧠 Planning agent
- [x] ✍️ Patch generation
- [x] 🧪 Validation agent
- [x] 🔎 Critic agent
- [x] 🛡️ Human approval gate
- [ ] 🐙 GitHub Issues integration
- [ ] 🔀 Automatic branch creation
- [ ] 🔄 Pull Request generation
- [ ] 🧠 Code RAG
- [ ] 🔌 MCP integration
- [ ] 🧪 Sandboxed execution
- [ ] 🔁 Automatic test-failure repair
- [ ] 📊 Agent evaluation dashboard
- [ ] 🤖 LangGraph multi-agent workflow
- [ ] 🌐 Web interface

## 💼 Resume Description

> Built an autonomous AI software-engineering system that analyzes developer tasks and repositories, generates implementation plans and code patches, validates changes through automated tests, performs AI-assisted code review, and uses human approval gates for safe Git/GitHub workflows.

## 🏷️ Recommended GitHub Topics

```text
ai, artificial-intelligence, generative-ai, agentic-ai, ai-agents,
llm, langgraph, langchain, mcp, code-generation, coding-agent,
software-engineering, developer-tools, rag, github, python, automation
```

## 🌟 Project Highlights

- 🤖 Autonomous software-engineering workflow
- 🧠 Agentic task planning
- 🗂️ Repository-aware reasoning
- ✍️ AI code generation
- 🧪 Automated validation
- 🔎 AI-assisted code review
- 🔌 MCP-ready architecture
- 🧠 Code-RAG ready
- 🛡️ Human-in-the-loop safety
- 📊 Evaluation-driven development

## 🎓 Learning Outcomes

You will practice:

- Agent orchestration
- Tool calling
- Repository-aware LLM systems
- Code generation
- Code RAG
- Automated testing agents
- AI code review
- MCP architecture
- Human-in-the-loop workflows
- Agent evaluation
- AI security
- Production GenAI architecture

## 🔮 Future Vision

```text
🎫 Read Issue
   ↓
🧠 Understand Requirements
   ↓
🔍 Explore Codebase
   ↓
📝 Create Plan
   ↓
💻 Implement Changes
   ↓
🧪 Run Tests
   ↓
🔧 Repair Failures
   ↓
🔎 Review Code
   ↓
🛡️ Request Approval
   ↓
🐙 Create Pull Request
   ↓
📊 Report Results
```

## ⭐ Support

If this project helps you learn **Agentic AI, GenAI, MCP, RAG, and autonomous software engineering**, consider giving the repository a ⭐.

---

### 👨‍💻 Built for AI Engineering & GenAI Portfolio Development

🤖 Agentic AI • 🧠 LLMs • 🔌 MCP • 🗂️ Code RAG • 🧪 Testing • 🛡️ AI Safety
