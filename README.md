# Banking-Agent-POC: AI-Powered Loan Underwriting System

An automated, local Proof-of-Concept (POC) for an AI-powered loan origination and underwriting system. Built with Streamlit, Pandas, Plotly, and LangChain, the application processes loan application parameters, generates credit scores and risk ratings, recommends interest terms, compiles amortization tables, and uses a local LLaMA 3 model to generate executive committee summaries.

---

## Underwriting Workflow

```
Customer Input (main.py Form)
      │
      ▼
Calculate Credit Score & Risk Rating (utils.py)
      │
      ▼
Determine Loan Offer & Amortization (utils.py)
      │
      ▼
Inference: Generate Committee Summary (agent.py via Ollama LLaMA 3)
      │
      ▼
Render Dashboard (main.py) & Compile PDF Proposal (utils.py)
```

---

## Key Features

- **Automated Credit Scoring**: Evaluates creditworthiness and risk profiles based on age, income, and debt ratios.
- **AI Loan Committee Summaries**: Utilizes a local LLaMA 3 model to write concise, professional loan summaries for internal bank committee reviews.
- **Amortization Engine**: Computes monthly schedules, tracking principal, interest, and remaining balances over the tenure.
- **Plotly Visualizations**: Renders interactive charts showing the reduction in loan balance over time.
- **PDF Proposal Generator**: Generates and compiles a downloadable PDF loan proposal containing complete terms and approval status.
- **Zero Cloud Dependencies**: Powered by local LLMs via Ollama, ensuring customer application details remain private.

---

## Tech Stack

- **Frontend UI**: Streamlit
- **Agentic Orchestration**: LangChain
- **Language Model**: LLaMA 3 (via local Ollama engine)
- **Data Manipulation**: Pandas
- **Data Visualization**: Plotly
- **PDF Compilation**: ReportLab (via utils)
- **Development Language**: Python (v3.9+)

---

## Project Structure

```
Banking-Agent-POC/
├── main.py              # Streamlit dashboard layout and submission handler
├── agent.py             # LangChain LLaMA 3 model setup and summary prompt logic
├── utils.py             # Math engines (amortization, risk rules) and PDF compiler
├── requirements.txt     # Python dependency configuration
└── assets/              # Static assets and animation JSONs
```

---

## Setup & Running Locally

### Prerequisites
- Python 3.9 or higher
- [Ollama](https://ollama.com) installed and running locally

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/programmingxpert/Banking-Agent-POC.git
   cd Banking-Agent-POC
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Pull the LLaMA 3 Model**
   Verify that Ollama is running and download the model:
   ```bash
   ollama pull llama3
   ```

4. **Launch Application**
   ```bash
   streamlit run main.py
   ```
   *Note: Access the application in your browser at `http://localhost:8501`.*

---

## Author

**Satya**  
GitHub: [programmingxpert](https://github.com/programmingxpert/)
