# CGL Prompt Template (English Version)
Framework for designing reliable, modular, and verifiable prompts.

---

## 1. CBL — Cognitive Breakdown Layer
Break down the task into clear and verifiable steps.

1. Main objective:
2. Sub‑objectives:
3. Constraints:
4. Required data:
5. Expected output:
6. Quality criteria:

---

## 2. IBC — Inference Boundary Check
Define what the model is allowed and not allowed to assume.

### Allowed assumptions:
- 

### Forbidden assumptions:
- 

### Information the model must not invent:
- 

---

## 3. KFG — Knowledge Formatting Grid
Define the exact structure of the output.

Possible formats:
- Numbered list
- Table
- JSON
- Sectioned schema
- Textual diagram

Required format:

---

## 4. QV — Quality Validation
Criteria to verify that the output is correct.

- Completeness:
- Adherence to constraints:
- Absence of hallucinations:
- Internal coherence:
- Compliance with the required format:

---

## 5. RAG (optional) — External Context
Add any external documents or contextual information here.

---

## 6. Final Instruction to the Model
Write the operational instruction:

**Use the CBL, IBC, KFG, and QV layers to generate the required output, strictly respecting constraints and format.**
