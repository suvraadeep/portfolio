---
title: "NewsAgent"
excerpt: "This project implements an AI-powered news aggregation system using LangGraph and Groq's 70B-parameter LLM. It automates real-time news discovery from global sources (BBC, TechCrunch, Financial Post), performs intelligent web scraping, and generates TL;DR summaries with source attribution. Designed for analysts tracking geopolitical events, market movements, and emerging tech trends."
collection: portfolio
---

🔗 **Notebook Link:** [NewsAgent](https://www.kaggle.com/code/suvroo/newsagent)  



## Tech Stack  
- **Core Framework**: LangGraph (Stateful Workflow Orchestration)  
- **LLM Provider**: Groq (Llama-3.3-70B)  
- **News APIs**: NewsAPI, Google News, BBC News  
- **Web Scraping**: BeautifulSoup + Custom Extraction Pipeline  
- **Analysis Tools**: PyDantic (Data Modeling), Regex (Pattern Matching)  


## Key Features  
1. **Adaptive News Discovery**  
   - Auto-generates optimal NewsAPI parameters (date ranges, sources, keywords)  
   - Fallback searches with expanded parameters when initial results are sparse  

2. **Intelligent Filtering**  
   ```python  
   def select_top_urls(state):  
       """LLM-powered relevance ranking of 100+ articles"""  
       # Uses query context to filter non-relevant content  
       return top_3_articles  
   ```

3. **Parallel Processing**  
   - Concurrent summarization of 5+ articles using async/await  
   - Maintains source attribution and publication dates  

4. **Enterprise-Grade Output**  
   ```markdown  
   ## Foxconn EV Market Expansion [^1]  
   * Investing $1.3B in auto-tech acquisitions  
   * Targeting 40% global EV production share  
   [^1]: Financial Post | 2024-12-13  
   ```

---

## Workflow Architecture  
```mermaid  
graph TD  
    A[Generate API Params] --> B[Fetch Metadata]  
    B --> C{Enough Articles?}  
    C -->|Yes| D[Scrape Full Text]  
    C -->|No| A  
    D --> E[LLM Relevance Filter]  
    E --> F[Parallel Summarization]  
    F --> G[Format Results]  
```








