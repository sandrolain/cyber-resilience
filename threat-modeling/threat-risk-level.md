# Linee Guida per la Classificazione del Rischio dei Threat

### Obiettivo

Questa linea guida fornisce un metodo standard per classificare i livelli di rischio associati a potenziali minacce (threat) su servizi software. L’obiettivo è consentire agli ingegneri di valutare e gestire il rischio in modo uniforme, tenendo in considerazione i fattori di probabilità e impatto.

---

### Definizione delle Variabili di Rischio

Per una valutazione precisa del rischio, consideriamo due variabili principali:

- **Probabilità (P)**: misura la possibilità che una minaccia si verifichi. La probabilità è classificata su una scala di 5 livelli:
  - **1**: Molto improbabile
  - **2**: Improbabile
  - **3**: Possibile
  - **4**: Probabile
  - **5**: Molto probabile

- **Impatto (I)**: misura la gravità delle conseguenze della minaccia sul servizio. Anche l’impatto è valutato su una scala di 5 livelli:
  - **1**: Minimo
  - **2**: Limitato
  - **3**: Moderato
  - **4**: Grave
  - **5**: Catastrofico

> **Nota**: La scala dei livelli per probabilità e impatto può essere adattata a specifici criteri aziendali, se necessario.

---

### Calcolo del Livello di Rischio

Il **livello di rischio** viene calcolato moltiplicando la probabilità (P) per l’impatto (I):

\[
\text{Rischio} = P \times I
\]

Questo valore può variare da un minimo di 1 (basso rischio) a un massimo di 25 (rischio molto alto).

---

### Classificazione Alfabetica dei Livelli di Rischio

Per rendere più intuitiva la priorità e urgenza di intervento, il livello di rischio viene suddiviso in cinque categorie alfabetiche. La tabella seguente specifica i livelli di rischio:

| Rischio (P × I) | Livello di Rischio | Classificazione | Descrizione                                               |
|-----------------|--------------------|-----------------|-----------------------------------------------------------|
| 1 - 5           | Molto Basso        | **E**           | Rischio trascurabile; nessuna azione immediata richiesta  |
| 6 - 10          | Basso              | **D**           | Rischio moderato; monitorare e valutare azioni correttive |
| 11 - 15         | Medio              | **C**           | Rischio considerevole; interventi raccomandati            |
| 16 - 20         | Alto               | **B**           | Rischio significativo; pianificare azioni di mitigazione  |
| 21 - 25         | Molto Alto         | **A**           | Rischio critico; azione immediata necessaria              |

---

### Esempio di Applicazione

Consideriamo una minaccia con:

- **Probabilità (P)** = 4 (Probabile)
- **Impatto (I)** = 5 (Catastrofico)

Il livello di rischio è calcolato come:

\[
\text{Rischio} = 4 \times 5 = 20
\]

Questo punteggio corrisponde alla **classificazione B** (Alto rischio), richiedendo la pianificazione di azioni di mitigazione.

---

### Azioni Raccomandate in Base alla Classificazione

| Classificazione     | Azione Raccomandata                                                                    |
|---------------------|----------------------------------------------------------------------------------------|
| **A (Molto Alto)**  | Attivare contromisure immediate. Informare i responsabili e monitorare costantemente.  |
| **B (Alto)**        | Pianificare e implementare azioni di mitigazione. Monitorare regolarmente l'efficacia. |
| **C (Medio)**       | Valutare e implementare azioni correttive. Monitorare periodicamente.                  |
| **D (Basso)**       | Monitorare la minaccia e valutare periodicamente se sia necessaria un’azione.          |
| **E (Molto Basso)** | Nessuna azione immediata richiesta; mantenere un monitoraggio generale.                |

---

### Vantaggi dell'Approccio Proposto

- **Uniformità e Chiarezza**: Una scala standardizzata facilita la comprensione e la comparabilità dei rischi.
- **Scala Alfabetica Intuitiva**: L’uso di lettere rende facile la comunicazione del livello di priorità e urgenza.
- **Flessibilità Operativa**: La matrice può essere personalizzata secondo le esigenze specifiche del team e del contesto aziendale.

---

> **Nota Importante**: Questa linea guida deve essere aggiornata periodicamente per riflettere eventuali cambiamenti nel contesto aziendale o nella tolleranza al rischio.

---
