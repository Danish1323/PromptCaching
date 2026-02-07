# LiteLLM Prompt Caching & Simulated RAG Demo

## Overview

This project demonstrates how to use **LiteLLM** to interact with modern language models while analyzing token usage, cost, and the powerful impact of **prompt caching**.

It walks through:

* Making basic LLM calls
* Tracking token consumption
* Understanding cost behavior
* Simulating Retrieval-Augmented Generation (RAG)
* Observing how cached prompts dramatically reduce API expenses

The notebook is intentionally educational and highlights practical considerations developers often overlook when building LLM-powered systems.

---

## Key Concepts Demonstrated

### ✅ LiteLLM Integration

Provides a unified interface to call multiple model providers without rewriting application logic.

### ✅ Token & Cost Inspection

Each request logs usage so you can clearly see how prompt size affects pricing.

### ✅ Simulated RAG

Instead of building a full vector database, the notebook injects external context (Hamlet text) directly into the prompt to demonstrate why retrieval systems matter.

### ✅ Prompt Caching

Repeated calls with identical context show a massive drop in cost — an important optimization for production AI systems.

---

## Project Structure

```
.
├── project.ipynb
├── hamlet.txt
├── .env (NOT committed)
└── README.md
```

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd <repo-name>
```

---

### 2. Install Dependencies

```bash
pip install litellm python-dotenv openai
```

---

### 3. Add Your API Key

Create a `.env` file:

```
OPENAI_API_KEY=your_key_here
```

⚠️ **Never commit this file.**
Add `.env` to `.gitignore`.

---

### 4. Run the Notebook

```bash
jupyter notebook
```

Open the notebook and execute cells sequentially.

---

## How Others Can Use This Project

This repository is useful for:

* Developers learning how LLM pricing works
* Engineers exploring prompt optimization
* Students studying modern AI tooling
* Builders planning production AI systems
* Anyone curious about prompt caching

You can easily modify the notebook to:

* Test different models
* Compare providers
* Measure cost differences
* Experiment with larger context windows

---

## Security Notes

This repository **does NOT contain any API keys**.

If you fork or reuse this project:

✔ Use environment variables
✔ Never hardcode secrets
✔ Rotate keys if accidentally exposed

---

## Why This Project Matters

Many LLM tutorials focus only on generating responses.

This project focuses on something equally important:

**Understanding cost and efficiency.**

When building real-world AI applications, optimizing token usage can reduce infrastructure expenses by orders of magnitude.

Prompt caching is one of the simplest — yet most overlooked — techniques to achieve that.

---

## Future Improvements (Optional Ideas)

* Replace simulated RAG with a vector database
* Add embeddings search
* Build a small chat interface
* Benchmark multiple models
* Visualize token cost trends

---

If you found this helpful, consider starring the repo ⭐
