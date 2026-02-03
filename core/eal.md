# EAL — Error Anticipation Layer

L’**Error Anticipation Layer (EAL)** è il terzo modulo del CGL e ha il compito di eseguire un controllo qualità prima dell’output finale.

---

## Obiettivo
Individuare errori logici, incoerenze, omissioni e punti critici prima che il modello produca la risposta definitiva.

---

## Funzioni principali

- verifica della coerenza interna del ragionamento  
- identificazione di errori logici o contraddizioni  
- segnalazione di punti ambigui o incompleti  
- richiesta di chiarimenti all’utente se necessario  

---

## Struttura del modulo

1. **Consistency Check**  
   Controllo della coerenza tra le fasi precedenti.

2. **Logic Scan**  
   Individuazione di errori logici, salti o deduzioni non supportate.

3. **Critical Points Detection**  
   Evidenziazione di parti incomplete o rischiose.

4. **User Clarification Gate**  
   Se qualcosa non è chiaro, il modello deve fermarsi e chiedere.

---

## Output previsto

- elenco degli errori potenziali  
- note operative per correggerli  
- eventuali richieste di chiarimento  
- conferma che l’output è pronto  

---

## Regole operative

- nessun output finale se esistono errori critici  
- ogni criticità deve essere esplicitata  
- il modello deve fermarsi in caso di dubbio  

---

## Note
EAL è l’ultimo livello del CGL.  
Se supera il controllo, il modello può produrre l’output finale.
