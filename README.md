#  AI Web Agent


An advanced **AI Web Scraper & Agent** capable of navigating websites, extracting structured data, and performing autonomous research. This project leverages **Firecrawl** for high-fidelity scraping and **LangGraph** to orchestrate intelligent workflows, allowing the agent to "think" as it browses.

---

## 🚀 Key Features

- **🕷️ Intelligent Crawling**: Uses **Firecrawl** to turn any website into LLM-ready markdown, handling dynamic content and infinite scrolls.
- **🧠 State-Based Orchestration**: Built with **LangGraph** to manage the agent's state, memory, and decision-making loops.
- **🔍 Deep Research**: Can autonomously navigate through links to gather comprehensive information on a given topic.
- **📝 Structured Extraction**: Converts unstructured web data into clean, structured formats (JSON/Markdown) for downstream analysis.
- **🛡️ Robust Error Handling**: Includes retry logic and validation to ensure reliable data collection.

---

## 🛠️ Tech Stack

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Language** | Python 3.10+ | Core logic |
| **Orchestration** | LangGraph | State machine for agent workflows |
| **Scraping** | Firecrawl | Web scraping & content extraction API |
| **LLM** | OpenAI (GPT-4o) | Decision making and data processing |
| **Framework** | LangChain | Tool definitions and LLM chains |

---

## 🏁 Getting Started

Follow these steps to set up the Web Agent locally.

### 1. Clone the Repository
```bash
git clone [https://github.com/TanishqMishra12/Web-Agent.git](https://github.com/TanishqMishra12/Web-Agent.git)
cd Web-Agent

```

### 2. Create a Virtual Environment

```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

```

### 3. Install Dependencies

```bash
pip install -r requirements.txt

```

*(If `requirements.txt` is missing, install the core packages manually: `pip install langgraph langchain-openai firecrawl-py python-dotenv`)*

### 4. Configuration

Create a `.env` file in the root directory and add your API keys:

```env
OPENAI_API_KEY=sk-...
FIRECRAWL_API_KEY=fc-...
# TAVILY_API_KEY=tv-... (If using Tavily for search)

```

---

## 🏃‍♂️ Usage

To run the agent, simply execute the main script:

```bash
python main.py

```

*(Note: Replace `main.py` with your specific entry file if different, e.g., `agent.py` or `graph.py`)*

### Example Workflow

1. **Input**: You provide a URL or a research topic.
2. **Plan**: The agent decides which pages to visit.
3. **Scrape**: Firecrawl extracts the content.
4. **Refine**: The LLM analyzes the content and decides if more info is needed.
5. **Output**: Returns a summarized report or structured data.

---

## 📂 Project Structure

```text
Web-Agent/
├── agent.py            # Main agent logic and graph definition
├── tools.py            # Firecrawl and search tool definitions
├── state.py            # LangGraph state schema
├── .env                # Environment variables (API keys)
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation

```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request 

