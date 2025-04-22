# 🧠 Offline LLM-Powered Automated Workflow Generator

## 📌 Problem Statement

The objective of this project is to design and implement an **automated workflow generation system** using **offline Large Language Models (LLMs)** to ensure **privacy**, **security**, and **cost-effectiveness**, while outputting results in a **standardized JSON format** for seamless integration with other systems.

---

## 🎯 Objectives and Approach

### ✅ Step 1: Transition to Offline Models

#### Overview:
To enhance **data privacy** and **security**, this step shifts from online LLMs to **offline alternatives** using [Ollama](https://ollama.com/).

#### 🔧 Tools:
- **Ollama**: Manages local LLMs for offline use.
- **Models Used**:
  - **Llama2**: Versatile, well-balanced model.
  - **Mistral**: Lightweight and low-latency model.

#### ✅ Advantages:
- ✅ Full data privacy (no external API calls)
- ✅ Enhanced system security
- ✅ Cost savings (no recurring cloud usage fees)

#### ⚠️ Limitations:
- ❌ No access to real-time data
- ❌ Static knowledge (trained only on fixed data)

---

### ✅ Step 2: Standardized JSON Output

This project uses LLMs to **automatically generate structured JSON workflows**. These workflows are consistent and integration-ready.

---

## 🧩 Components & Functionalities

### 1. 🛠 Core Functions

#### `generate_workflow()`
- Creates a JSON configuration
- Includes metadata, OCR settings, email/SLA configs, and flow blocks

#### `get_workflow_arguments(workflow_type)`
- Uses Llama2 or Mistral to generate workflow parameters
- Has a fallback mechanism to defaults if LLM fails

#### `create_workflow_from_type()`
- Bridges argument generation and workflow creation
- Validates inputs and ensures correct structure

---

### 2. 🧑‍💻 User Interface

#### `get_user_workflow()`
- Captures workflow type input from user

#### `generate_workflow_from_user_input()`
- Full pipeline:
  - Get input → Generate args → Build JSON → Save to file

---

## 📈 Performance Metrics

| Model    | Avg JSON Generation Time |
|----------|--------------------------|
| Llama2   | 1 min 33 sec              |
| Mistral  | 2 min 7 sec               |

Both models deliver reliable performance and robust output.

---

## 🔗 Reference

📘 Ollama Integration Example in Jupyter Notebook:  
[GitHub Notebook Link](https://github.com/RamiKrispin/ollama-poc/blob/main/ollama-poc.ipynb)

---

## 📂 Output

- The final output is a **JSON configuration file** with a standardized structure for downstream use.
- System ensures **error handling** and **format compliance**.

---
