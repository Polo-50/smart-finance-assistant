--------------------------------------------------------------------------------------------------------------------------------------------------------------------------
***README***
This project is a web-based finance assistant that helps users understand their spending, get financial advice, chat with an AI coach, and plan savings goals — all in one system.

It is built using six main components:


**1. Transaction Loader (transaction_loader.py)**

- Loads and cleans bank transaction CSV files
- Fixes messy data (currency symbols, negative values, missing rows)
- Standardises categories (e.g. groceries → Food)
- Removes invalid or corrupted entries
- Outputs clean data for analysis


**2. Spending Analysis (spending_analysis.py)**

- Groups spending by category
- Calculates total spending and percentages
- Separates spending and refunds
- Detects unusual spending patterns (e.g. high rent or food spending)
- Generates a summary report with insights

**3. Recommendations Engine (recommendations.py)**

- Converts spending data into financial advice
- Suggests ways to save money
- Gives practical tips (subscriptions, budgeting, grocery savings)
- Provides quick actions users can apply immediately

**4. Finance Chatbot — “Morgan” (finance_chatbot.py)**

- AI chatbot for personal finance questions
- Uses spending data for personalised answers
- Remembers conversation history
- Runs in Google Colab with a simple chat UI
- Can also be used in code without UI

**5. Financial RAG System (financial_rag.py)**

- Answers questions using uploaded financial documents
- Splits documents into text chunks
- Uses TF-IDF + cosine similarity to find relevant information
- Sends only relevant context to the AI to reduce hallucinations


**6. Web Dashboard (smart_finance_ui.py)**

- Built using Gradio
- Combines all features into one interface with 3 tabs:

Tab 1: Data Dashboard
- Upload CSV file
- View spending summary and charts

Tab 2: Chat Coach
- Chat with AI finance assistant
- Ask questions like “How can I save money?”

Tab 3: Savings Calculator
- Calculate time to reach savings goals
- Uses compound interest formula

 **How to Run**

1. Open the project in Google Colab
2. Install dependencies:
   pip install openai scikit-learn gradio pandas --quiet

3. Run all files in order
4. Launch dashboard:
   python smart_finance_ui.py
   Open the link provided

Optional:
- FinancialRAG().ask("your question") for document Q&A
- launch_finance_chat() for chatbot UI

 Summary Table

transaction_loader.py   → Cleans transaction data
spending_analysis.py     → Analyses spending patterns
recommendations.py       → Gives saving tips
finance_chatbot.py       → AI chatbot (Penny)
financial_rag.py         → Document-based Q&A system
smart_finance_ui.py      → Full Gradio dashboard


 Tools Used

- OpenAI-compatible LLM (Ollama / gemma3:4b)
- pandas (data handling)
- scikit-learn (TF-IDF search)
- Gradio (web UI)
- ipywidgets (Colab chat interface)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------
MIT License — free to use and modify.
