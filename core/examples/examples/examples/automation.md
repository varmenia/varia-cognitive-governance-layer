# Esempio — Automation Workflow

Questo esempio mostra come applicare il CGL a un compito di automazione: generare un workflow chiaro e verificabile.

---

## Task
Creare un workflow automatizzato per inviare una notifica quando arriva un nuovo lead.

---

## Applicazione del CGL

### 1. CBL — Strutturazione del ragionamento
1. Identificare la fonte del lead  
2. Definire i trigger  
3. Definire i dati necessari  
4. Definire il canale di notifica  
5. Definire le condizioni di invio  
6. Definire i fallback  

---

### 2. IBC — Controllo delle inferenze
- Assunzioni autorizzate:  
  - il lead contiene almeno nome e email  
- Assunzioni bloccate:  
  - struttura del CRM non dichiarata  
- Richieste di chiarimento:  
  - canale preferito (email, Slack, webhook)  

---

### 3. EAL — Controllo qualità
- Verifica che il workflow sia completo  
- Controllo che non ci siano passaggi mancanti  
- Identificazione di potenziali errori di trigger  

---

## Output finale
Un workflow chiaro, verificabile e pronto per essere implementato in un sistema di automazione.
