# AI-Based Summary Evaluation System (Agentic AI)

An autonomous AI evaluator built to grade student-written lecture summaries by comparing them against original transcripts using LLMs and logic-based NLP.

## 🚀 Key Features
- [cite_start]**End-to-End Automation:** Takes a ZIP file containing a lecture transcript (.docx) and student summaries (.xlsx) and processes them fully.
- [cite_start]**High-Power LLM Reasoning:** Uses the **Groq API with LLaMA 3.1 (405B)** to evaluate summaries against the actual transcript.
- [cite_start]**Intelligent Scoring:** Automatically scores summaries out of 10 based on Coverage, Clarity, Coherence, and Completeness[cite: 2, 21].
- [cite_start]**Teacher-Like Feedback:** Generates 2-3 sentence written explanations for every score[cite: 6, 24].
- [cite_start]**Statistical Normalization:** Automatically adjusts class scores if the mean falls below a predefined threshold.
- [cite_start]**Automated Reporting:** Exports results (Email, Name, Score, Explanation) directly to a formatted Excel file[cite: 31, 33].
- [cite_start]**Scalability:** Successfully evaluated **82 students** in a single execution.

## 🛠️ Tech Stack
- [cite_start]**Language/Environment:** Python (Google Colab).
- [cite_start]**AI Model:** Groq API + LLaMA 3.1-405B (State-of-the-art LLM).
- [cite_start]**Document Processing:** `python-docx` for transcript parsing.
- [cite_start]**Data Engineering:** `pandas` & `openpyxl` for data handling and automated Excel exports.
- [cite_start]**Pipeline:** Custom text preprocessing and ZIP file handling modules.

## 📊 Evaluation Logic
The system simulates an **Agentic AI pipeline** that autonomously reads, reasons, and evaluates text based on the following criteria:

| Parameter | Weight | Description |
| :--- | :--- | :--- |
| **Coverage** | 3.0 | [cite_start]Accuracy in capturing key lecture arguments[cite: 21]. |
| **Length** | 2.5 | [cite_start]Optimal summary-to-transcript ratio. |
| **Clarity** | 2.0 | [cite_start]Language structure and clear expression[cite: 21]. |
| **Coherence** | 1.5 | [cite_start]Logical flow between sentences and ideas[cite: 21]. |
| **Completeness**| 1.0 | [cite_start]Inclusion of final conclusions and examples[cite: 21]. |
