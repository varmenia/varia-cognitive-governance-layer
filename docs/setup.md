# 📖 Documentazione Tecnica

Questa sezione approfondisce i tre layer che compongono il **Cognitive Governance Layer (CGL)**.

---

## 🛡️ IBC (Interpretation Bias Control)
Il modulo IBC è il guardiano dell'accuratezza. Il suo compito è impedire che l'IA "immagini" dettagli non presenti nell'input.

### Livelli di Strictness
* **Alto**: L'IA rifiuta qualsiasi inferenza. Se un dato manca, deve dichiararlo.
* **Medio**: L'IA può fare deduzioni logiche basilari, ma deve segnalarle.
* **Basso**: L'IA agisce in modalità creativa (non raccomandato per uso enterprise).

---

## 🧩 CBL (Cognitive Load Balancing)
Suddividere un compito complesso in step atomici riduce drasticamente il degrado delle performance dei modelli.

### Linee Guida per la Decomposizione
1. **Analisi**: Identificazione delle entità nell'input.
2. **Elaborazione**: Applicazione delle regole di business.
3. **Validazione**: Controllo interno dei risultati.
4. **Sintesi**: Formattazione dell'output finale.

---

## 🚦 EAL (Error Anticipation Layer)
L'ultimo filtro prima dell'utente finale. Funziona come una checklist interna che l'IA deve validare.

* **Checkpoint logici**: Verifica che la conclusione sia supportata dalle premesse.
* **Vincoli di formato**: Assicura che l'output rispetti lo schema richiesto (JSON, Tabella, Report).
* **Criteri di blocco**: Se l'EAL rileva un'allucinazione critica, il framework blocca la generazione.
