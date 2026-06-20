# Communicative Agents for Software Development

<p align="center">
  <img src='./misc/logo1.png' width=550>
</p>

<p align="center">
    【English | <a href="readme/README-Chinese.md">Chinese</a> | <a href="readme/README-Japanese.md">Japanese</a> | <a href="readme/README-Korean.md">Korean</a> | <a href="readme/README-Filipino.md">Filipino</a> | <a href="readme/README-French.md">French</a> | <a href="readme/README-Slovak.md">Slovak</a> | <a href="readme/README-Portuguese.md">Portuguese</a> | <a href="readme/README-Spanish.md">Spanish</a> | <a href="readme/README-Dutch.md">Dutch</a> | <a href="readme/README-Hindi.md">Hindi"】
</p>
<p align="center">
    【📚 <a href="wiki.md">Wiki</a> | 🚀 <a href="wiki.md#local-demo">Local Demo</a> | 👥 <a href="Contribution.md">Community Built Software</a> | 🔧 <a href="wiki.md#customization">Customization</a>】
</p>

## Overview

**ChatDev** is a **virtual software company** operated by **intelligent agents** in different roles: CEO, CPO, CTO, programmer, reviewer, tester, and art designer. These agents collaborate through specialized functional seminars — designing, coding, testing, and documenting — to "revolutionize the digital world through programming."

ChatDev provides an **easy-to-use**, **highly customizable**, and **extendable** LLM-based framework for studying collective intelligence in software development.

<p align="center">
  <img src='./misc/company.png' width=600>
</p>

## What's New (2025-2026)

- **Multi-Model Support**: Run with GPT-4o, Claude 3.5 Sonnet, Gemini 1.5 Pro, Llama 3.1 405B, Qwen 2.5, DeepSeek-V3, or local models via Ollama
- **OpenAI Agents SDK Integration**: Leverage OpenAI's latest agent orchestration framework (2025)
- **MCP (Model Context Protocol)**: Tool-use protocol for standardized agent-tool communication
- **Docker Sandbox Execution**: Isolated code execution environments for safer generation
- **Incremental Development**: Build upon existing codebases with `--config "incremental" --path "[dir]"`
- **Enhanced Code Quality**: Ruff linting, mypy type checking, and pytest integration in generated code
- **Multi-Language Output**: Generate Python, JavaScript, TypeScript, Java, Go, Rust codebases
- **GitHub Copilot Integration**: Enhanced Git mode with automated PR creation
- **LangGraph Workflows**: Complex agent orchestration with state management
- **Vision Capabilities**: Image analysis and UI generation with GPT-4V / Claude 3.5 Vision

## Architecture

```
┌─────────────────────────────────────────────────────┐
│                    ChatDev Agent System               │
├──────────────┬──────────────┬───────────────────────┤
│   CEO Agent  │  CTO Agent   │   Programmer Agent    │
├──────────────┼──────────────┼───────────────────────┤
│ Reviewer     │  Tester      │   Art Designer        │
├──────────────┴──────────────┴───────────────────────┤
│              ChatChain Orchestration Layer            │
├─────────────────────────────────────────────────────┤
│  LLM Backend (OpenAI / Anthropic / Local via Ollama) │
└─────────────────────────────────────────────────────┘
```

## What Can ChatDev Do?

![intro](misc/intro.png)

https://github.com/OpenBMB/ChatDev/assets/11889052/80d01d2f-677b-4399-ad8b-f7af9bb62b72

## Quickstart

### Web Interface

Access the web demo: https://chatdev.modelbest.cn/

### Terminal

```bash
# Clone the repository
git clone https://github.com/OpenBMB/ChatDev.git
cd ChatDev

# Setup environment (Python 3.10+)
conda create -n ChatDev python=3.10 -y
conda activate ChatDev

# Install dependencies
pip install -r requirements.txt

# Set API key (supports multiple providers)
export OPENAI_API_KEY="your_api_key"

# Build software
python3 run.py --task "create a calculator app" --name "Calculator"

# Run generated software
cd WareHouse/Calculator_DefaultOrganization_timestamp
python3 main.py
```

### Docker

```bash
docker build -t chatdev .
docker run -e OPENAI_API_KEY="your_key" chatdev --task "create a todo app" --name "TodoApp"
```

### Using Local Models (Ollama)

```bash
# Install Ollama and pull a model
ollama pull llama3.1

# Run ChatDev with local model
export OPENAI_API_KEY="ollama"
export OPENAI_API_BASE="http://localhost:11434/v1"
python3 run.py --task "build a web scraper" --name "WebScraper" --model "llama3.1"
```

## Advanced Configuration

| Parameter | Description | Default |
|-----------|-------------|---------|
| `--task` | Description of software to build | Required |
| `--name` | Project name | Required |
| `--org` | Organization name | DefaultOrganization |
| `--config` | ChatChain configuration | Default |
| `--model` | LLM model to use | gpt-3.5-turbo |
| `--config "incremental"` | Build on existing code | - |
| `--config "Human"` | Human-in-the-loop mode | - |
| `--config "Art"` | Enable image generation | - |
| `"git_management"` | Git version control | False |

See [Wiki](wiki.md) for full configuration reference.

## Community Built Software

See contributed software in [Contribution.md](Contribution.md).

## Related Research (2025-2026)

- **OpenAI Agents SDK** (2025): Agent orchestration framework for tool-use and multi-step reasoning
- **MCP Protocol** (2025): Anthropic's Model Context Protocol for standardized tool integration
- **AutoGen** (2024-2025): Microsoft's multi-agent conversation framework
- **CrewAI** (2024-2025): Role-based AI agent orchestration
- **LangGraph** (2024-2025): Stateful agent workflows with cycles and persistence
- **Devin** (2024): AI software engineer paradigm
- **SWE-bench** (2024-2025): Benchmark for AI coding agents

## Contributors

<a href="https://github.com/OpenBMB/ChatDev/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=OpenBMB/ChatDev" />
</a>

## Citation

```bibtex
@misc{qian2023communicative,
      title={Communicative Agents for Software Development},
      author={Chen Qian and Xin Cong and Wei Liu and Cheng Yang and Weize Chen and Yusheng Su and Yufan Dang and Jiahao Li and Juyuan Xu and Dahai Li and Zhiyuan Liu and Maosong Sun},
      year={2023},
      eprint={2307.07924},
      archivePrefix={arXiv},
      primaryClass={cs.SE}
}
```

## License

- **Source Code**: Apache 2.0 License
- **Data**: CC BY-NC 4.0 (non-commercial use only)

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=openbmb/chatdev&type=Date)](https://star-history.com/#openbmb/chatdev&Date)

## Contact

[chatdev.openbmb@outlook.com](mailto:chatdev.openbmb@outlook.com)

## Acknowledgments

<a href="http://nlp.csai.tsinghua.edu.cn/"><img src="misc/thunlp.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://modelbest.cn/"><img src="misc/modelbest.png" height=50pt></a>&nbsp;&nbsp;
<a href="https://github.com/OpenBMB/AgentVerse/"><img src="misc/agentverse.png" height=50pt></a>
