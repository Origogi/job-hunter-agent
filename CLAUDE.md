# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a job hunting agent application built with CrewAI, a framework for orchestrating autonomous AI agents. The project uses Python 3.9+ and is managed with `uv` for dependency management.

## Key Dependencies

- **crewai[tools]** (>=0.5.0): Core framework for building AI agent workflows
- **firecrawl-py** (>=4.6.0): Web scraping tool for gathering job listings and company data
- **python-dotenv** (>=1.2.1): Environment variable management for API keys

## Development Commands

### Setup
```bash
# Install dependencies using uv
uv sync

# Activate virtual environment
source .venv/bin/activate  # On macOS/Linux
```

### Running the Application
```bash
# Run the main application
python main.py

# Or using uv
uv run main.py
```

## Architecture Notes

This project is in early development. The main.py currently contains a placeholder entry point. When implementing agents:

- CrewAI agents will be the primary abstraction for job hunting tasks (searching, analyzing, applying)
- Firecrawl will be used for web scraping job boards and company websites
- Environment variables should be stored in a .env file (not committed to git)
- The typical CrewAI pattern involves defining Agents, Tasks, and Crews to orchestrate workflows
