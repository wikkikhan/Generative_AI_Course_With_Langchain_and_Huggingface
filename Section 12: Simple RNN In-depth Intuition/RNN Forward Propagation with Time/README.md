# 🔄 RNN Forward Propagation with Time

Forward propagation in RNN happens **sequentially over time steps**.

---

## ⏳ What is Time Step?

Each position in a sequence is called a **time step (t)**

Example:
"I love AI" → 3 time steps

---

## 🔁 Forward Flow

At each time step:

1. Take input (xₜ)
2. Combine with previous hidden state (hₜ₋₁)
3. Compute new hidden state (hₜ)
4. Generate output (yₜ)

---

## 🧠 Formula

Hidden State:
hₜ = tanh(W·xₜ + U·hₜ₋₁)

Output:
yₜ = V·hₜ

---

## 🔗 Chain Structure

h₀ → h₁ → h₂ → h₃ → ... → hₜ

Each state depends on previous state

---

## 📊 Step-by-Step Example

Sentence: "AI is powerful"

| Time Step | Input | Hidden State | Output |
|----------|------|-------------|--------|
| t=1 | AI | h₁ | y₁ |
| t=2 | is | h₂ | y₂ |
| t=3 | powerful | h₃ | y₃ |

---

## 🔥 Key Insight

- Information flows **left → right**
- Earlier inputs influence later outputs

---

## ⚠️ Limitation

Long sequences may cause:
- Weak memory of earlier inputs

---

## 📈 Summary

- Processes input sequentially
- Uses previous hidden state
- Builds contextual understanding over time
