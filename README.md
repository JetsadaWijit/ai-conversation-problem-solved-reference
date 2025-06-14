# 🧠 AI Text Classifier with Web Search (PyTorch)

This project is a simple AI model built using PyTorch that classifies input text into one of four categories:

- 💬 **Conversation** – Explains what happened  
- ❗ **Problem** – Identifies an issue  
- ✅ **Solved** – Describes the solution  
- 🔗 **Reference** – Provides a helpful link (with live web search)

The model also performs a web search automatically when the response is classified as a reference.

---

## 📂 Project Structure

```bash
.
├── createAi.py     # Train and save the model
├── usageAi.py      # Load and use the model
├── ai_model.pt     # Trained model (generated after training)
├── word2idx.pt     # Word index map (used during inference)
└── README.md       # You're reading this
```

## 🏗️ How to Use

1. 🚀 Train the Model Run this to train and save the model:

```bash
python createAi.py
```

2. 🤖 Use the Model Run the usage script and enter your question:

```bash
python usageAi.py
```
It will classify your input and, if the class is `reference`, perform a live Google search to retrieve the first useful link.

| Label           | Description                        |
| --------------- | ---------------------------------- |
| 💬 conversation | General explanation of a situation |
| ❗ problem       | Declares a specific issue          |
| ✅ solved        | Describes the solution             |
| 🔗 reference    | Suggests external resources        |

## 🌐 Dependencies
Install required packages:

```bash
pip install torch requests beautifulsoup4
```

## 📌 Notes

- Model uses a basic tokenizer (space split) and padded input of length 10.

- You can easily swap in a more powerful tokenizer or expand the dataset.

- Web search scrapes Google using `requests` + `BeautifulSoup`.

## 🛠️ Future Improvements

- Use transformer-based models (e.g., BERT)

- Train on larger, labeled datasets

- Support multi-label classification
