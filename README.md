# 🧭 Murshid — LLM Application Engineering

<div align="center">

[![SDAIA](https://img.shields.io/badge/SDAIA-Training_Program-006C67?style=for-the-badge)](https://sdaia.gov.sa/)
![Course](https://img.shields.io/badge/Course-SDA--AIE--213-6254A4?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-2E8B57?style=for-the-badge)

### Building Reliable, Tool-Augmented LLM Applications

**A bilingual public-service assistant developed through four cumulative engineering labs and four practical homework assignments.**

**[Main Repository](https://github.com/WesalFadhl/Murshid-Wesal-Mashael) · [Complete Labs Notebook](Murshid_Labs_1-4.ipynb) · [SDAIA](https://sdaia.gov.sa/)**

</div>

---

## 📌 Project Overview

**Murshid** is a bilingual (Arabic–English) public-service assistant developed as part of the **LLM Application Engineering (SDA-AIE-213)** training program at the Saudi Data & Artificial Intelligence Authority (SDAIA).

The project demonstrates the engineering lifecycle of an LLM-based application, progressing from structured response generation to controlled tool interactions, safety validation, systematic evaluation, and performance optimization.

Rather than focusing solely on text generation, Murshid emphasizes **reliability, traceability, privacy, controlled execution, and measurable system behavior**.

The implementation was developed incrementally in one cumulative notebook, supported by four independent homework assignments.

## 🎯 Project Objectives

- Develop a bilingual assistant capable of handling public-service inquiries.
- Design consistent, structured responses with clear output contracts.
- Implement controlled tool calling for application-status requests.
- Enforce input validation, authorization checks, and output validation.
- Evaluate successful and rejected requests through reproducible golden tests.
- Optimize application performance through selective caching.
- Measure model behavior, latency, token usage, and evaluation outcomes.
- Document limitations and responsible deployment considerations.

## 🛠️ Technologies & Tools

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

| Category | Technologies |
|---|---|
| Programming Language | Python 3 |
| Development Environment | Google Colab |
| Local Language Model | `google/flan-t5-small` |
| Model Libraries | Hugging Face Transformers, PyTorch |
| Data & Reporting | JSON |
| Testing | Python Assertions, Mock Testing, Golden Test Suites |
| Performance | Latency Measurement, Caching, Metrics Collection |
| Version Control | Git & GitHub |

---

## 📚 Core Labs — Development Journey

All four labs were implemented cumulatively in **[`Murshid_Labs_1-4.ipynb`](Murshid_Labs_1-4.ipynb)**.

### Day 1 — LLM Application Foundations

**Focus:** Building a bilingual assistant with structured outputs.

- Implemented Arabic and English public-service FAQ responses.
- Developed a simulated model client.
- Introduced structured response formatting.
- Added trace identifiers and latency tracking.
- Recorded baseline execution results.

**Deliverable:** `baseline_results.json`

### Day 2 — Tool Calling & Structured Workflows

**Focus:** Connecting the assistant to controlled application workflows.

- Implemented ticket-reference extraction and validation.
- Developed synthetic application-status lookup.
- Added request routing and structured result codes.
- Enforced authorization and access-control checks.
- Tested clarification and unsupported-action scenarios.

**Deliverable:** `day2_results.json`

### Day 3 — Guardrails & Golden Test Evaluation

**Focus:** Validating system behavior and handling unsafe or invalid requests.

- Implemented input and output validation.
- Examined instruction-injection attempts.
- Enforced response-schema requirements.
- Created and executed ten predefined golden test cases.
- Evaluated successful responses, clarification requests, and expected refusals.

**Result: 10/10 golden tests passed in mock mode.**

**Deliverable:** `day3_results.json`

### Day 4 — Measurement, Caching & Optimization

**Focus:** Improving efficiency while maintaining consistent application behavior.

- Implemented selective caching for eligible public FAQ requests.
- Introduced cache expiration and version-aware cache keys.
- Compared execution behavior with and without caching.
- Collected latency, cache-hit, and mock-call metrics.
- Conducted regression testing after optimization.
- Generated final evaluation reports and synthetic-data artifacts.

**Deliverables:** `day4_results.json`, `final_report.json`, `metrics.json`, and `synthetic_data.json`

### Lab Completion Summary

| Day | Main Topic | Status |
|---|---|---|
| 01 | LLM Application Foundations | ✅ Completed |
| 02 | Tool Calling & Structured Workflows | ✅ Completed |
| 03 | Guardrails & Golden Testing | ✅ Completed |
| 04 | Measurement & Caching | ✅ Completed |

---

## 🧪 Optional Homework Assignments

Each homework assignment was implemented in a separate notebook to explore additional engineering concepts without modifying the cumulative core project.

| Day | Homework | Implementation | Outcome |
|---|---|---|---|
| 01 | Real Model Demonstration | Local inference using `google/flan-t5-small` | Successful model response |
| 02 | Structured Tool Dispatcher | Tool-call validation and routing | **7/7 tests passed** |
| 03 | Error Handling & Input Validation | Intentional `ValueError` rejection and correction | **3/3 errors caught** |
| 04 | Real Model Evaluation | Token counting, latency measurement, keyword checks, and manual review | **3/3 keyword hits** |

All homework notebooks and supporting results are stored in the [`homework/`](homework/) directory.

---

## 📊 Evaluation Results

### Overall Results

| Evaluation | Result |
|---|---|
| Day 2 Homework | **7/7 tests passed** |
| Day 3 Golden Test Suite | **10/10 tests passed** |
| Day 3 Mock Pass Rate | **100%** |
| Day 3 Homework | **3/3 intentional errors caught** |
| Day 4 Homework Keyword Hits | **3/3** |
| Day 4 Homework Keyword Hit Rate | **100%** |
| Day 4 Homework External Inference API Calls | **0** |

### Day 3 — Golden Test Suite

The golden test suite covered ten predefined cases, including bilingual FAQs, authorized status retrieval, missing references, out-of-scope inquiries, access denial, instruction-injection attempts, and invalid outputs.

**Execution mode:** Mock

**Results:** 10 passed / 10 total

**Pass rate:** 100%

These results demonstrate correct behavior for the supplied deterministic test cases, including appropriate refusal paths.

### Day 4 — Real Model Evaluation

The final homework evaluated `google/flan-t5-small` using three synthetic application-status questions.

| Test Case | Generated Answer | Input Tokens | Output Tokens* | Inference Time |
|---|---|---:|---:|---:|
| E01 | Use its reference number | 34 | 6 | 0.362 s |
| E02 | Reference number | 36 | 4 | 0.172 s |
| E03 | Use its reference number | 37 | 6 | 0.178 s |

*Output token counts include special tokens.*

**Model Configuration:**
- Sampling: Disabled
- Beam Search: 1 beam
- Maximum New Tokens: 48
- External Inference API Calls: 0

**Manual Review:** All three generated responses were consistent with the supplied reference context.

**Evaluation Limitation:** Keyword matching is a proxy indicator, not a measure of general semantic accuracy. Results from three synthetic questions cannot establish overall model reliability.

---

## 📁 Repository Structure

```text
Murshid-Wesal-Mashael/
│
├── README.md
├── Murshid_Labs_1-4.ipynb
│
├── baseline_results.json
├── day2_results.json
├── day3_results.json
├── day4_results.json
├── final_report.json
├── metrics.json
├── synthetic_data.json
│
└── homework/
    ├── Homework1.ipynb
    ├── Homework day2_tools.ipynb
    ├── Homework3.ipynb
    ├── Homework4.ipynb
    ├── evaluation_result.json
    └── Additional homework result files
```

The main notebook contains the complete four-day implementation, while the homework directory contains independent experiments and their supporting evidence.

---

## 🔐 Reliability & Responsible AI Considerations

Murshid incorporates several engineering practices designed to improve application reliability:

**1. Structured Outputs**

Consistent response formats support predictable application behavior and validation.

**2. Controlled Tool Execution**

Tool interactions are restricted through routing logic, input validation, and authorization checks.

**3. Input & Output Guardrails**

Invalid requests and malformed responses are identified through explicit validation rules.

**4. Privacy-Aware Monitoring**

Performance metrics are collected without logging raw questions, private references, record ownership, or generated answer content.

**5. Selective Caching**

Caching is limited to eligible public FAQ responses. Private application-status results are excluded.

**6. Regression Testing**

Previously defined test cases are used to verify that optimization changes do not unintentionally alter expected behavior.

### Limitations

- Core lab evaluations use synthetic records and deterministic mock behavior.
- Keyword-based guardrails are insufficient for production-level security.
- The golden test suite covers a limited set of predefined scenarios.
- Real-model evaluation uses only three synthetic questions.
- Additional security, privacy, and reliability testing would be necessary before production deployment.

---

## 💡 Learning Outcomes

Through the four cumulative labs and independent homework assignments, we developed practical skills across the LLM application engineering lifecycle.

**Key competencies gained:**

- Designing bilingual AI application workflows.
- Implementing structured model interactions.
- Integrating tools with controlled routing and authorization.
- Applying validation and instruction-injection checks.
- Developing reproducible evaluation suites.
- Measuring latency and token usage.
- Implementing caching and performance monitoring.
- Evaluating real local language models.
- Documenting technical results and system limitations.

The project reinforced that **reliable AI application engineering extends beyond generating responses; it requires validation, controlled execution, measurable performance, and systematic evaluation.**

---

## 👩🏻‍💻 Contributors

**Wesal Al-Numani**

**Mashael Al-Mufleh**

---

## 🏛️ Training Information & Acknowledgments

**Program:** LLM Application Engineering (SDA-AIE-213)

**Organization:** [Saudi Data & Artificial Intelligence Authority (SDAIA)](https://sdaia.gov.sa/)

**Instructor:** Meaad Al-Marri

**Original Course Repository:** [Murshid — LLM Application Engineering](https://github.com/almiyead-rgb/murshid-llm-application-engineering-sda-aie-213)

We sincerely appreciate SDAIA and our instructor for providing the opportunity to gain practical experience in LLM application engineering through structured, hands-on learning.

---

<div align="center">

### ✅ Project Completed

**4 Core Labs · 4 Homework Assignments · Real Model Evaluation**

*Developed as part of the SDAIA LLM Application Engineering training program.*

</div>
