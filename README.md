# Cognitive Governance Layer — VarIA Framework  
Un framework open source per progettare prompt affidabili, modulari e controllabili in contesti professionali.

---

## Obiettivo

Il Cognitive Governance Layer (CGL) è un framework progettato per migliorare l’affidabilità dei modelli linguistici attraverso tre principi fondamentali:

- Cognitive Load Balancing (CBL): strutturazione del ragionamento in fasi sequenziali  
- Interpretation Bias Control (IBC): riduzione delle inferenze non autorizzate  
- Error Anticipation Layer (EAL): controllo qualità pre‑output  

Il framework è pensato per:

- AI designer  
- Prompt engineer  
- Workflow architect  
- Team enterprise  
- Automazioni e agenti AI  

---

## Architettura del Framework

### 1. Cognitive Load Balancing (CBL)
Struttura il task in fasi distinte per evitare:

- mescolanza dei passaggi  
- ragionamento caotico  
- sintesi premature  

Linee guida:

- 3–7 fasi  
- ogni fase rappresenta un obiettivo atomico  
- definire cosa fare e cosa non fare  
- output intermedio verificabile  

---

### 2. Interpretation Bias Control (IBC)
Controlla l’interpretazione dell’input per ridurre:

- inferenze non richieste  
- assunzioni implicite  
- completamenti automatici  

Linee guida:

- specificare la fonte dei dati  
- impostare Strictness: Alto, Medio o Basso  
- elencare assunzioni vietate  
- definire fallback per ambiguità  

---

### 3. Error Anticipation Layer (EAL)
Introduce un quality gate pre‑output che intercetta:

- incoerenze  
- omissioni critiche  
- rischi logici  
- assunzioni non autorizzate  

Linee guida:

- definire 3–5 checkpoint  
- stabilire se bloccare l’output su errori critici  
- definire formato della segnalazione  

---

## Parametri di Configurazione

```yaml
IBC_Strictness: Alto | Medio | Basso
EAL_Strictness: Alto | Medio | Basso
Thought_Process_Visibility: Nascosto | Visibile
Phase_Limit: 3 | 5 | 7

### Nota sul parametro `Thought_Process_Visibility`

Questo parametro controlla se il modello deve mostrare o nascondere il proprio ragionamento interno (chain‑of‑thought).  
Nel Cognitive Governance Layer, il valore predefinito è **Nascosto**, perché:

- il ragionamento interno può contenere passaggi non verificati  
- aumenta il rumore cognitivo e riduce la chiarezza dell’output  
- può introdurre bias o inferenze non autorizzate  
- non è destinato all’utente finale in contesti professionali  

Impostare `Visibile` è utile solo in fase di sviluppo, audit o debugging, quando è necessario analizzare:

- la scomposizione del task (CBL)  
- le interpretazioni controllate (IBC)  
- i checkpoint del quality gate (EAL)  

In produzione, si raccomanda di mantenere `Thought_Process_Visibility: Nascosto` per garantire output puliti, sintetici e controllabili.

---

## Esempio di Prompt CGL

Di seguito un esempio completo di prompt costruito secondo il Cognitive Governance Layer.

### Input Declaration
L’utente fornisce:  
- una descrizione testuale di un processo aziendale  
L’utente NON fornisce:  
- dati quantitativi  
- metriche di performance  
- diagrammi tecnici  

Vincoli:  
- linguaggio professionale  
- output sintetico  

---

### Task Decomposition (CBL)
1. Analizzare il processo descritto  
2. Identificare inefficienze o punti critici  
3. Proporre miglioramenti operativi  
4. Applicare IBC per evitare assunzioni non autorizzate  
5. Applicare EAL per verificare coerenza e completezza  
6. Restituire una sintesi strutturata  

---

### Interpretation Bias Control (IBC)
- Strictness: Alto  
- Assunzioni vietate: dati non forniti, numeri inventati, organigrammi non citati  
- Fonti autorizzate: solo testo dell’utente  
- Gestione ambiguità: chiedere chiarimento o proporre alternative  

---

### Error Anticipation Layer (EAL)
Checklist:  
- L’output rispetta i vincoli?  
- Ci sono inferenze non autorizzate?  
- Le fasi CBL sono state rispettate?  
- La sintesi è coerente con l’input?  

Criteri di blocco:  
- presenza di dati inventati  
- violazione delle assunzioni vietate  

---

### Output Format
- Titolo  
- Analisi del processo  
- Criticità individuate  
- Proposte di miglioramento  
- Note operative  

/varia-cognitive-governance-layer
│
├── /core
│     ├── cgl-schema.md
│     ├── cbl.md
│     ├── ibc.md
│     ├── eal.md
│
├── /examples
│     ├── business-analysis.md
│     ├── educational.md
│     ├── automation.md
│
├── /templates
│     ├── cgl-prompt-template.md
│     ├── audit-checklist.md
│
└── README.md




# Cognitive Governance Layer — VarIA Framework
*A modular open‑source framework for designing reliable, controllable, and enterprise‑grade prompts.*

## Purpose
The Cognitive Governance Layer (CGL) is a framework designed to increase the reliability of language models through three core principles:

- **Cognitive Load Balancing (CBL):** structured, sequential reasoning  
- **Interpretation Bias Control (IBC):** reduction of unauthorized inferences  
- **Error Anticipation Layer (EAL):** pre‑output quality control  

The framework is intended for:

- AI designers  
- Prompt engineers  
- Workflow architects  
- Enterprise teams  
- Automation systems and AI agents  

---

# Framework Architecture

## 1. Cognitive Load Balancing (CBL)
Structures the task into distinct phases to prevent:

- mixed reasoning steps  
- chaotic thought processes  
- premature synthesis  

**Guidelines:**

- 3–7 phases  
- each phase represents a single atomic objective  
- define what to do and what *not* to do  
- produce verifiable intermediate outputs  

---

## 2. Interpretation Bias Control (IBC)
Controls input interpretation to reduce:

- unsolicited inferences  
- implicit assumptions  
- automatic completions  

**Guidelines:**

- specify the source of truth  
- set Strictness: High, Medium, or Low  
- list forbidden assumptions  
- define fallback behavior for ambiguity  

---

## 3. Error Anticipation Layer (EAL)
Adds a pre‑output quality gate that detects:

- inconsistencies  
- critical omissions  
- logical risks  
- unauthorized assumptions  

**Guidelines:**

- define 3–5 checkpoints  
- decide whether to block output on critical errors  
- define the reporting format  

---

# Configuration Parameters

- **IBC_Strictness:** High | Medium | Low  
- **EAL_Strictness:** High | Medium | Low  
- **Thought_Process_Visibility:** Hidden | Visible  
- **Phase_Limit:** 3 | 5 | 7  

### Note on `Thought_Process_Visibility`
This parameter controls whether the model should reveal or hide its internal reasoning (chain‑of‑thought).

Default in CGL: **Hidden**, because:

- internal reasoning may contain unverified steps  
- it increases cognitive noise  
- it may introduce bias or unauthorized inferences  
- it is not intended for end‑users in professional contexts  

Use **Visible** only during development, auditing, or debugging to inspect:

- task decomposition (CBL)  
- controlled interpretations (IBC)  
- quality checkpoints (EAL)  

In production, keep it **Hidden** to ensure clean, controlled outputs.

---

# Example — CGL Prompt

## Input Declaration
The user provides:  
- a textual description of a business process  

The user does *not* provide:  
- quantitative data  
- performance metrics  
- technical diagrams  

Constraints:  
- professional tone  
- concise output  

---

## Task Decomposition (CBL)

1. Analyze the described process  
2. Identify inefficiencies or critical points  
3. Propose operational improvements  
4. Apply IBC to avoid unauthorized assumptions  
5. Apply EAL to verify coherence and completeness  
6. Deliver a structured synthesis  

---

## Interpretation Bias Control (IBC)

- **Strictness:** High  
- **Forbidden assumptions:** invented data, numbers, org charts not provided  
- **Authorized sources:** user text only  
- **Ambiguity handling:** ask for clarification or offer alternatives  

---

## Error Anticipation Layer (EAL)

**Checklist:**  
- Does the output respect the constraints?  
- Are there unauthorized inferences?  
- Were the CBL phases followed?  
- Is the synthesis consistent with the input?  

**Blocking criteria:**  
- invented data  
- violation of forbidden assumptions  

---

## Output Format

- Title  
- Process analysis  
- Identified issues  
- Improvement proposals  
- Operational notes  

---

# Repository Structure

