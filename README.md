# 🚀 AI Email Triage Engine

An intelligent email processing system that simulates how AI agents can classify, prioritize, and respond to emails in real-world scenarios.

---

## 💡 Problem Statement

Modern inboxes are overwhelmed with spam, urgent messages, and routine communication.

This project builds an **AI-powered email assistant** that:

* Detects spam
* Assigns priority
* Suggests responses

---

## 🧠 What Makes This Project Unique

Unlike basic ML models, this system is built as a:

👉 **Custom evaluation environment (RL-style)**

* Multi-task setup (3 tasks)
* Reward-based scoring
* Structured agent interaction
* Real-time LLM integration

---

## ⚙️ System Design

### 🔹 Environment Layer

* Simulates email scenarios
* Tracks state, steps, and rewards

### 🔹 Task & Grading Layer

* Custom scoring logic
* Partial rewards (not binary)
* Realistic evaluation

### 🔹 Inference Layer

* OpenAI-powered reasoning
* Handles API failures gracefully

---

## 🛠️ Tech Stack

* Python
* OpenAI API
* FastAPI
* Docker
* Hugging Face Spaces

---

## 📊 Sample Run

```bash
[START] task=email env=openenv model=gpt-4.1-mini
[STEP] step=1 reward=0.60 done=false
[STEP] step=2 reward=0.85 done=false
[STEP] step=3 reward=0.92 done=true
[END] success=true score=0.92
```

---
## DEMO 

<img width="852" height="441" alt="image" src="https://github.com/user-attachments/assets/4385cbfa-3483-4ee2-b605-dc19c007e409" />
This system simulates an AI agent that processes emails using a custom environment 
and evaluates actions through a reward-based mechanism.

## 🎯 Key Highlights

* Multi-task AI environment
* Robust error handling
* Reward shaping logic
* Clean modular architecture

---

## 📈 Learnings

* Designing agent-based systems
* Debugging real-world AI pipelines
* Handling API instability
* Building evaluation frameworks

---

## 🚀 Future Scope

* UI dashboard
* Larger dataset
* Fine-tuned models
* Real-time deployment

---

## 👩‍💻 Author

Ambika Bansal
