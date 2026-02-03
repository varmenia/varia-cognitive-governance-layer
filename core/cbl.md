# IBC — Interpretation Bias Control

L’**Interpretation Bias Control (IBC)** è il secondo modulo del CGL e ha il compito di controllare, limitare e rendere trasparenti le inferenze del modello.

---

## Obiettivo
Ridurre le assunzioni arbitrarie e mantenere l’output aderente ai dati forniti dall’utente.

---

## Funzioni principali

- identificazione delle inferenze non autorizzate  
- richiesta di conferma esplicita prima di procedere  
- blocco delle deduzioni non supportate  
- tracciamento delle assunzioni fatte dal modello  

---

## Struttura del modulo

1. **Inference Scan**  
   Analisi delle deduzioni implicite generate dal modello.

2. **Bias Detection**  
   Individuazione di assunzioni non supportate dai dati.

3. **User Confirmation Gate**  
   Il modello deve chiedere conferma prima di procedere.

4. **Inference Log**  
   Produzione di un registro delle inferenze autorizzate e bloccate.

---

## Output previsto

- elenco delle assunzioni verificate  
- elenco delle assunzioni bloccate  
- richieste di chiarimento se necessario  

---

## Regole operative

- nessuna inferenza può essere introdotta senza conferma  
- ogni assunzione deve essere esplicitata  
- il modello deve fermarsi se il dato è insufficiente  

---

## Note
IBC opera dopo CBL e prima di EAL.  
Se IBC rileva inferenze non autorizzate, il processo deve essere interrotto.
