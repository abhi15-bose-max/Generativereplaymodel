# Generativereplaymodel
# 🧠 Generative Replay: Teaching Neural Networks to Dream and Remember

Can a neural network **replay past memories by dreaming them up**?

This project implements and compares **Generative Replay (GR)** with standard **Continual Learning** techniques. It simulates a scenario where a model must learn sequentially from multiple tasks **without forgetting** earlier ones — known as **catastrophic forgetting**.

---

## 🧠 What is Generative Replay?

Instead of storing past data, a model trains a **generator** to recreate synthetic examples from previous tasks. When learning a new task, the main classifier is trained using:

- **Real data** from the current task
- **Generated data** from old tasks

> Like a brain dreaming of past experiences while learning new ones.

---

## 🔁 Core Components

- **Main Classifier:** \( f_\theta \)
- **Generator:** \( G_\phi(z, y) \), where \( z \sim \mathcal{N}(0, I) \), \( y \) is the class label

