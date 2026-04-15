# 🔁 Simple RNN – In-Depth Intuition

Recurrent Neural Networks (RNNs) are designed to handle **sequential data** by maintaining a memory of previous inputs.

---

## 🧠 Why RNN?

Traditional Neural Networks (ANNs):
- Cannot handle sequence dependency
- Treat each input independently

RNN solves this by:
👉 Using **previous information (memory)** to influence current output

---

## 🔄 Core Idea

At each time step:
- Input = current data + previous hidden state
- Output depends on both

---

## 📦 Basic Components

- **Input (xₜ)** → Current word/input
- **Hidden State (hₜ)** → Memory
- **Weights (W, U, V)** → Learnable parameters
- **Activation Function** → Usually tanh or ReLU

---

## 🔁 How Memory Works

RNN keeps updating hidden state:

hₜ = f(W·xₜ + U·hₜ₋₁)

👉 This allows the network to "remember" previous inputs

---

## 📌 Example

Sentence:
"I love AI"

RNN processes:
- "I" → memory updated
- "love" → uses previous memory
- "AI" → understands context

---

## ⚠️ Key Insight

RNN doesn’t process all data at once — it processes **step by step (time-based)**.

---

## 🎯 Use Cases

- Language Modeling
- Text Generation
- Speech Recognition
- Time Series Prediction

---

## 📈 Summary

- RNN introduces **memory**
- Works well with **sequence data**
- Foundation for advanced models like **LSTM & GRU**
