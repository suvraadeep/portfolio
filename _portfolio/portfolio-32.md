---
title: "Code Quality Intelligence Agent"
excerpt: "An AI-powered code analysis system that combines static analysis, semantic search (RAG), and LLM reasoning to detect vulnerabilities, improve code quality, and provide actionable insights across large codebases."
collection: portfolio
---

🔗 **GitHub Repo:** [Code Quality Intelligence Agent](https://github.com/suvraadeep/Code-Quality-Intelligence-Agent)  


### Key Features:
1. **AI-Augmented Static Analysis**: Combines Bandit, Radon, and Semgrep with LLM-based reasoning for deeper insights.
2. **RAG-Based Code Understanding**: Semantic search over code using vector databases (FAISS/ChromaDB).
3. **Multi-Language Support**: Analyzes 13+ programming languages across local and GitHub repositories.
4. **Conversational Code Assistant**: Chatbot interface for context-aware code queries and explanations.
5. **Multi-Format Reporting**: Generates Console, JSON, and Markdown reports with actionable recommendations. :contentReference[oaicite:0]{index=0}  


### Example Workflow:
#### Input: *Analyze a GitHub repository*
1. **File Processing**:
   - Clones repo and detects programming languages.
2. **Static + AI Analysis**:
   - Runs Bandit, Radon, Semgrep + LLM reasoning.
3. **RAG Indexing**:
   - Builds semantic search index over codebase.
4. **Output**:
   - Generates detailed reports + enables interactive chat.

#### Scenario: *Ask "Where are security vulnerabilities?"*
1. **Context Retrieval**:
   - Fetches relevant code chunks via RAG.
2. **LLM Reasoning**:
   - Explains vulnerabilities with suggestions.
3. **Response**:
   - Provides actionable fixes with code references.


### Technologies Used:
- **Python & LangChain**: Core orchestration and LLM pipelines.
- **Groq API (DeepSeek LLM)**: High-performance inference.
- **FAISS / ChromaDB**: Vector database for semantic search.
- **Bandit, Radon, Semgrep**: Static code analysis tools.
- **Streamlit**: Web-based dashboard interface.
- **GitPython**: Repository cloning and management.
