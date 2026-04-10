# AI-Based Summary Evaluation System (Agentic AI)

An autonomous AI evaluator built to grade student-written lecture summaries by comparing them against original transcripts using LLMs and logic-based NLP.

## 🚀 Key Features
- **End-to-End Automation:** Takes a ZIP file containing a lecture transcript (.docx) and student summaries (.xlsx) and processes them fully.
- **High-Power LLM Reasoning:** Uses the **Groq API with LLaMA 3.1 (405B)** to evaluate summaries against the actual transcript.
- **Intelligent Scoring:** Automatically scores summaries out of 10 based on Coverage, Clarity, Coherence, and Completeness[cite: 2, 21].
- **Teacher-Like Feedback:** Generates 2-3 sentence written explanations for every score.
- **Statistical Normalization:** Automatically adjusts class scores if the mean falls below a predefined threshold.
- **Automated Reporting:** Exports results (Email, Name, Score, Explanation) directly to a formatted Excel file.
- **Scalability:** Successfully evaluated **82 students** in a single execution.

## 🛠️ Tech Stack
- **Language/Environment:** Python (Google Colab).
- **AI Model:** Groq API + LLaMA 3.1-405B (State-of-the-art LLM).
- **Document Processing:** `python-docx` for transcript parsing.
- **Data Engineering:** `pandas` & `openpyxl` for data handling and automated Excel exports.
- **Pipeline:** Custom text preprocessing and ZIP file handling modules.

## 📊 Evaluation Logic
The system simulates an **Agentic AI pipeline** that autonomously reads, reasons, and evaluates text based on the following criteria:

| Parameter | Weight | Description |
| :--- | :--- | :--- |
| **Coverage** | 3.0 | Accuracy in capturing key lecture arguments. |
| **Length** | 2.5 | Optimal summary-to-transcript ratio. |
| **Clarity** | 2.0 | Language structure and clear expression. |
| **Coherence** | 1.5 | Logical flow between sentences and ideas. |
| **Completeness**| 1.0 | Inclusion of final conclusions and examples. |
