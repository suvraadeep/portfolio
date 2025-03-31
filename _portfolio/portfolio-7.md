---
title: "Agentic Hedge Fund for Stock Analysis"
excerpt: "This project implements a Financial Assistant using LangChain, LangGraph, and Groq APIs to process user queries related to stock prices, income statements, company financials, and markdown reports. The assistant leverages structured workflows, APIs, and LLMs to fetch, analyze, and present financial data efficiently."
collection: portfolio
---

🔗 **Notebook Link:** [Agentic Hedge Fund for Stock Analysis](https://www.kaggle.com/code/suvroo/agentic-hedge-fund-for-stock-analysis)  


### Key Features:
1. **Dynamic Query Routing**: Categorizes user requests into predefined routes such as `income_statement`, `company_financials`, `stock_price`, `report`, or `chat`.
2. **Symbol Extraction**: Extracts stock symbols (e.g., `AAPL` for Apple) using Groq-powered LLMs.
3. **Financial Data Retrieval**: Fetches real-time stock prices, income statements, and company financials using Financial Modeling Prep API.
4. **Markdown Report Generation**: Generates detailed markdown reports summarizing financial data for companies.
5. **Workflow Automation**: Implements structured workflows via LangGraph to dynamically route queries based on user intent.


### Example Workflow:
#### Query: *"Tell me about Uber?"*
1. **Categorization**: Recognized as a `report` request.
2. **Symbol Extraction**: Extracted symbol `UBER`.
3. **Data Retrieval**:
   - Fetched company overview, income statement, and stock price.
4. **Report Generation**:
   - Compiled markdown report summarizing Uber's financial data.

#### Query: *"What is Nvidia's stock price?"*
1. **Categorization**: Recognized as a `stock_price` request.
2. **Symbol Extraction**: Extracted symbol `NVDA`.
3. **Data Retrieval**:
   - Fetched Nvidia's current price ($142.44), volume (183M), EPS (2.54), and PE ratio (56.08).

### Technologies Used:
- **LangChain & LangGraph**: For building workflows and integrating LLMs.
- **Groq API**: For high-performance inference with large models.
- **Financial Modeling Prep API**: To fetch real-time financial data.
- **Python & Pydantic**: For data modeling and validation.








