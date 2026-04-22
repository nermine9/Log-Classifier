# Log-Classifier
Hybrid log classification using Regex, ML and LLM


##  Problem Statement

Modern software systems generate massive volumes of logs every second. These logs are critical for monitoring system health, detecting failures, and ensuring security. However, manually analyzing logs is time-consuming, error-prone, and not scalable.

This project aims to build an **automated log classification system** that categorizes log messages into predefined classes using a **hybrid approach combining Regex, Machine Learning, and Large Language Models (LLMs)**.

---

##  Who uses this system?

This system is designed for:

* **DevOps Engineers** → monitor system health and detect failures quickly
* **SRE (Site Reliability Engineers)** → ensure system reliability and reduce downtime
* **Security Teams** → detect suspicious activities and potential attacks
* **Backend Engineers** → debug and understand system behavior

---

##  Target Categories

The classifier will predict the following 5 categories:

* `ERROR` → system failures, crashes, exceptions
* `WARNING` → potential issues or deprecated usage
* `INFO` → general system information
* `SECURITY` → authentication issues, attacks, unauthorized access
* `NETWORK` → connectivity issues, timeouts, network failures

---

##  Success Criteria

The system will be considered successful if it meets the following goals:

* **Accuracy > 90%** → high-quality predictions
* **Latency < 500 ms per log** → fast response time
* **LLM usage < 20%** → optimized cost and efficiency
* **Robust architecture** → scalable and maintainable system

---

## Architecture Overview (Hybrid Cascade)

The system uses a **multi-stage classification pipeline**:

1. **Regex Classifier (Fast & deterministic)**

   * Handles simple and obvious patterns
   * Very fast and cost-free

2. **Machine Learning Model (TF-IDF + Logistic Regression)**

   * Handles most standard cases
   * Learns from labeled data

3. **LLM Classifier (Fallback for complex cases)**

   * Used only when previous methods are uncertain
   * Handles ambiguous or rare logs

###  Flow:

```
Log Input
   ↓
Regex → if confident → return label
   ↓
ML Model → if confident → return label
   ↓
LLM → final fallback
```

---


##  Tech Stack

* Python (pandas, scikit-learn, Numpy)
* Regex (rule-based classification)
* LLM API (Gemini / DeepSeek / OpenAI)
* FastAPI (API deployment)
* Streamlit

---

##  Concepts Covered

* Text Classification (NLP)
* TF-IDF Vectorization
* Logistic Regression
* Regex pattern matching
* Prompt Engineering
* Hybrid AI systems (rule-based + ML + LLM)
* API development (FastAPI)

---

##  Goal of the Project

This project is designed to demonstrate:

* End-to-end ML system design
* Practical use of hybrid AI approaches
* Trade-offs between **accuracy, latency, and cost**
* Production-ready thinking (API + deployment)

-

🚧 Work in progress — currently in setup and data exploration phase.
