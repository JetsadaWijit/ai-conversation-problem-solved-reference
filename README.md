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
