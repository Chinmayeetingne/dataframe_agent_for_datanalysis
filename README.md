# 📊 DataFrame Agent for Data Analysis

This project demonstrates how to build an AI-powered data analysis assistant using **LangChain**, **LLaMA (via Groq API)**, and **pandas**. The assistant can answer natural language questions, perform analysis, and even generate charts or code based on a given dataset.

---

## 🚀 Features

- 🔎 Ask questions about your dataset using natural language  
- 🤖 Powered by LLaMA-3 via **Groq API** for blazing-fast LLM inference  
- 📈 Auto-generates code and executes Python commands to analyze data  
- 📊 Supports plotting graphs using matplotlib  
- 🧠 Maintains conversational context for deeper insights  

---

## 📦 Requirements

Make sure you have the following installed:

```bash
pip install pandas matplotlib langchain groq
```

> You also need a `.env` file with your Groq API key:

```env
GROQ_API_KEY=your_groq_api_key_here
```

---

## 📁 How It Works

1. **Load a dataset** (e.g., Titanic CSV from URL or local file)
2. **Set up a LangChain agent** using the `create_pandas_dataframe_agent` function
3. **Ask questions** like:
   - “What is the average age of passengers?”
   - “Create a histogram of the Fare column”
   - “Show me the survival rate by gender”
4. The agent runs the code and displays the results, including plots

---

## 🧪 Example Usage

```python
agent.run("Plot a histogram of the Age column")
```

```python
agent.run("Which class had the highest survival rate?")
```

---

## ⚠️ Known Issues

- If you see `ValueError: An output parsing error occurred`, try setting:
  
  ```python
  handle_parsing_errors=True
  ```

- Graphs may not display in environments without display support. Make sure you're using Jupyter Notebook or VS Code.

---

## 📌 TODO

- [ ] Add support for uploading custom datasets via UI
- [ ] Enable CSV upload via web app
- [ ] Extend to multi-modal data

---

## 🧠 Credits

- Built using [LangChain](https://www.langchain.com/)
- LLaMA model via [Groq API](https://console.groq.com/)
- Inspired by LangChain agents for pandas
