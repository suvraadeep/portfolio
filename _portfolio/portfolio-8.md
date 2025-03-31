---
title: "Quant agent- PhiData"
excerpt: "This project implements a multi-agent financial analysis system combining real-time market data, news sentiment analysis, and quantitative modeling to deliver institutional-grade stock evaluations. The agent team leverages Groq's ultra-fast LLM inference and specialized tools for comprehensive analysis."
collection: portfolio
---

🔗 **Notebook Link:** [Quant agent- PhiData](https://www.kaggle.com/code/suvroo/quant-agent-phidata)  



### Key Features:  
- **Sentiment Analysis**: News scraping with Google Search + sentiment scoring (1-10)  
- **Fundamental Analysis**: Financial statements, ratios, analyst recommendations via YFinance  
- **Quantitative Modeling**: Python-driven DCF analysis and market positioning comparisons  
- **Executive Synthesis**: Unified BUY/SELL recommendations with risk assessment  

## Tech Stack  
- **Groq Cloud**: Ultra-fast LLM inference (70B parameter models)  
- **Phi**: Agent orchestration framework  
- **YFinance**: Real-time market data integration  
- **Google Search API**: News/article retrieval  
- **Python Tools**: Quantitative analysis libraries  

### Core Capabilities  
1. **Multi-Agent Architecture**
   ```markdown  
   | Agent Type | Specialization | Tools Used |  
   |-----------|----------------|------------|  
   | Sentiment Analyst | News scoring | Google Search, NLP |  
   | Financial Analyst | Fundamental metrics | YFinance API |  
   | Quant Analyst | DCF modeling | Python/pandas |  
   | Executive Agent | Risk-weighted synthesis | Data aggregation |  
   ```
   
2. **Analysis Workflows**  
   - Comparable Companies Analysis (Public Comps)  
   - Discounted Cash Flow Modeling (DCF)  
   - News Sentiment Heatmapping  
   - Technical/Fundamental Convergence Scoring  

3. **Output Formats**  
   ```markdown  
   ## CALM Intrinsic Value Analysis [^1]  
   | Metric | Value |  
   |--------|-------|  
   | Current Price | $57.32 |  
   | DCF Fair Value | $64.15 |  
   | Margin of Safety | +12.3% |  
   [^1]: Based on 2023-2025 EBITDA projections from YFinance  

   **Recommendation**: BUY (Consensus Score: 8.2/10)  
   ```

**Output Framework**:  
1. Market Share Analysis (YFinance data)  
2. Patent Activity Comparison (Google Scholar scraping)  
3. Gross Margin Trend Analysis (5Y historicals)  
4. Sentiment Correlation: News vs Stock Performance  
5. Consolidated STRONG BUY Recommendation  









