# 🧠 Cognitive Governance Layer (CGL)
> **VarIA Framework v2.0**
> Un framework open source per progettare prompt affidabili, modulari e controllabili in contesti professionali.

---

## 🎯 Obiettivo / Purpose

Il **Cognitive Governance Layer (CGL)** è un framework progettato per migliorare l’affidabilità dei modelli linguistici attraverso tre principi fondamentali:

* **Cognitive Load Balancing (CBL)**: Strutturazione del ragionamento in fasi sequenziali.
* **Interpretation Bias Control (IBC)**: Riduzione delle inferenze non autorizzate.
* **Error Anticipation Layer (EAL)**: Controllo qualità pre‑output.

---

## 🧩 Architettura del Framework

### 1️⃣ CBL - Cognitive Load Balancing
Struttura il task in fasi distinte (3–7 fasi) per evitare ragionamenti caotici e sintesi premature. Ogni fase deve avere un obiettivo atomico e un output verificabile.

### 2️⃣ IBC - Interpretation Bias Control
Controlla l’interpretazione dell’input. Riduce assunzioni implicite e completamenti automatici specificando la fonte dei dati e impostando livelli di *Strictness* (Alto/Medio/Basso).

### 3️⃣ EAL - Error Anticipation Layer
Un "Quality Gate" pre-output. Introduce 3-5 checkpoint per intercettare incoerenze, omissioni o rischi logici prima che l'utente veda la risposta.

---

## ⚙️ Parametri di Configurazione

| Parametro | Valori Disponibili | Default |
| :--- | :--- | :--- |
| `IBC_Strictness` | Alto \| Medio \| Basso | Alto |
| `EAL_Strictness` | Alto \| Medio \| Basso | Medio |
| `Thought_Process_Visibility` | Nascosto \| Visibile | **Nascosto** |
| `Phase_Limit` | 3 \| 5 \| 7 | 5 |

> **Nota su `Thought_Process_Visibility`**: In produzione, mantenere **Nascosto** per garantire output puliti e professionali. Usare **Visibile** solo per audit e debugging.

---
---

## 📞 Contatti & Social

* **💻 GitHub**: [varmenia/varia-cognitive-governance-layer](https://github.com/varmenia/varia-cognitive-governance-layer)
* **👔 LinkedIn**: [Viviana Armenia](http://www.linkedin.com/in/viviana-armenia)

## 📂 Struttura Repository
```text
/core         -> Documentazione approfondita moduli
/examples     -> Casi d'uso (Business, Education, Automation)
/templates    -> Prompt pronti all'uso
