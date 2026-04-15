# 🔁 Simple RNN Backward Propagation (BPTT)

Backward propagation in RNN is called:

👉 **Backpropagation Through Time (BPTT)**

---

## 🧠 What Happens?

- Errors are calculated at each time step
- Gradients are propagated **backwards through time**

---

## 🔄 Process

1. Compute loss at each time step
2. Calculate gradients
3. Propagate errors backward:
   hₜ → hₜ₋₁ → hₜ₋₂ → ...

---

## ⛓️ Chain Rule

Gradients are computed using chain rule:

∂L/∂W = Σ (∂L/∂hₜ × ∂hₜ/∂W)

---

## ⚠️ Key Challenge

Repeated multiplication causes:

- Gradients become very small → **Vanishing Gradient**
- Gradients become very large → **Exploding Gradient**

---

## 📉 Why It’s Hard?

Because:
- Same weights are reused at every time step
- Long sequences increase complexity

---

## 🔥 Visualization Idea

Backward flow:
t₃ → t₂ → t₁ → t₀

---

## 🛠️ Solutions

- Gradient Clipping (for exploding gradient)
- LSTM / GRU (for vanishing gradient)

---

## 📈 Summary

- Uses Backpropagation Through Time
- Updates weights based on sequence errors
- Suffers from gradient problems
