
# Guida per la Creazione e il Mantenimento di un Threat Model

Questa guida descrive il concetto di **threat modeling** e fornisce istruzioni per la creazione e il mantenimento di un modello di minaccia, fondamentale per migliorare la sicurezza di applicazioni e sistemi.

---

## Cos'è un Threat Model?

Un **threat model** è un'analisi strutturata dei potenziali rischi di sicurezza associati a un sistema o applicazione. Serve a identificare e classificare le minacce, a valutare i rischi e a definire contromisure adeguate. Il threat modeling è una pratica continua che evolve con il sistema e le minacce emergenti.

### Obiettivi del Threat Modeling

- **Identificare le Superfici di Attacco**: Rilevare i punti vulnerabili in cui un sistema può essere esposto a potenziali attacchi.
- **Valutare i Rischi**: Classificare le minacce in base alla probabilità e all'impatto per prioritizzare le azioni.
- **Implementare Contromisure**: Definire e applicare misure per mitigare i rischi identificati.
- **Ridurre i Costi**: Identificare le vulnerabilità durante la fase di progettazione per ridurre i costi di risoluzione delle problematiche di sicurezza.

---

## Passi per Creare un Threat Model

### 1. Definire i Confini e lo Scopo del Sistema

- **Descrivere il Sistema**: Fornire una panoramica dell’architettura e delle funzionalità del sistema.
- **Identificare i Confini del Sistema**: Distinguere i componenti inclusi e quelli esclusi dall’analisi.
- **Definire gli Obiettivi di Sicurezza**: Stabilire i requisiti di sicurezza principali (es. integrità dei dati, disponibilità dei servizi, protezione della privacy).

### 2. Creare un Diagramma del Sistema

Un diagramma di sistema aiuta a visualizzare i flussi di dati, i componenti principali e i punti di ingresso.

- **Diagramma di Flusso dei Dati (DFD)**: Mostra il percorso dei dati attraverso il sistema e identifica le interazioni tra i componenti.
- **Identificare le Superfici di Attacco**: Annotare i punti in cui il sistema interagisce con attori esterni, come API, interfacce utente o connessioni di rete.

### 3. Identificare le Minacce

Utilizzare il framework **STRIDE** per analizzare le minacce potenziali sulle superfici di attacco identificate:

- **Spoofing (S)**: Impersonificazione di un'entità legittima
- **Tampering (T)**: Manomissione dei dati
- **Repudiation (R)**: Impossibilità di tracciare le attività degli utenti
- **Information Disclosure (I)**: Divulgazione non autorizzata di informazioni
- **Denial of Service (D)**: Interruzione del servizio
- **Elevation of Privilege (E)**: Ottenimento di privilegi non autorizzati

> **Suggerimento**: Per ogni superficie di attacco, documenta le minacce usando una tabella:

| Componente | Superficie di Attacco | Minaccia                    | Categoria STRIDE | Descrizione                                     |
|------------|-----------------------|-----------------------------|------------------|-------------------------------------------------|
| API        | Endpoint `/login`     | Forzatura delle credenziali | Spoofing         | Attacco brute-force per accesso non autorizzato |

### 4. Valutare il Livello di Rischio

Per ogni minaccia, valuta il livello di rischio in base a **probabilità** e **impatto**. Utilizza una classificazione con lettere per assegnare priorità ai rischi in modo chiaro e uniforme.

#### Classificazione del Threat Risk Level

Assegna un livello di rischio alla minaccia considerando la probabilità di manifestazione e l'impatto che avrebbe. Usa una scala da **A** a **E**:

- **A** - Rischio molto elevato: priorità critica, richiede immediato intervento.
- **B** - Rischio elevato: alta priorità, mitigare con azioni a breve termine.
- **C** - Rischio moderato: attenzione moderata, valutare azioni correttive.
- **D** - Rischio basso: rischio gestibile, monitorare e valutare la mitigazione.
- **E** - Rischio molto basso: rischio trascurabile, può non richiedere intervento.

#### Classificazione del Business Risk Level

Valuta il rischio anche in termini di impatto sul business, così da comprenderne le conseguenze più ampie e allineare le priorità di sicurezza alle esigenze aziendali.

- **A** - Rischio critico per il business: impatto significativo, azione immediata necessaria.
- **B** - Rischio alto per il business: impatto rilevante, intervento a breve termine.
- **C** - Rischio moderato per il business: monitoraggio e azioni correttive se possibile.
- **D** - Rischio basso per il business: intervento minimo, monitoraggio periodico.
- **E** - Rischio trascurabile per il business: nessuna azione immediata richiesta.

#### Esempio di Tabella di Valutazione del Rischio

Utilizza una tabella per documentare le minacce e il loro livello di rischio, sia a livello di threat che di business.

| Minaccia                                       | Probabilità | Impatto  | Threat Risk Level | Business Risk Level | Note                                    |
|------------------------------------------------|-------------|----------|-------------------|---------------------|-----------------------------------------|
| Forzatura delle credenziali su API di login    | Alta        | Elevato  | A                 | B                   | Richiede limiti di login e monitoraggio |
| Esposizione di dati sensibili                  | Media       | Critico  | B                 | A                   | Implementare crittografia e logging     |
| Interruzione del servizio tramite attacco DDoS | Bassa       | Moderato | C                 | C                   | Configurare protezione DDoS             |

### 5. Definire le Contromisure

Per ogni minaccia prioritaria, definisci le contromisure che riducono la probabilità o l’impatto.

| Minaccia | Contromisura | Descrizione | Stato (In corso, Completa, Pianificata) |
|----------|--------------|-------------|-----------------------------------------|
| ...      | ...          | ...         | ...                                     |

---

## Mantenimento del Threat Model

Il threat model deve essere aggiornato regolarmente per adattarsi ai cambiamenti nel sistema e alle nuove minacce.

### 1. Monitoraggio e Logging

- **Monitoraggio Attivo**: Configura allarmi per rilevare attività sospette.
- **Conservazione dei Log**: Mantieni log dettagliati per consentire l'analisi retrospettiva e la risposta agli incidenti.

### 2. Test e Verifica

- **Penetration Testing**: Effettua test di penetrazione per verificare la sicurezza delle contromisure implementate.
- **Code Review**: Esegui revisioni periodiche del codice per individuare vulnerabilità.

### 3. Revisione Periodica

- **Piano di Revisione**: Effettua una revisione del threat model a intervalli regolari (es. trimestrale, semestrale) o a seguito di modifiche significative del sistema.
- **Documentazione delle Modifiche**: Tieni traccia delle modifiche per garantire la trasparenza e mantenere una storia del modello.

---

## Documentazione e Condivisione

1. **Archiviazione Centrale**: Mantieni il threat model in un repository condiviso accessibile a tutto il team.
2. **Condivisione delle Modifiche**: Notifica i membri del team quando il modello viene aggiornato, soprattutto se ci sono nuove minacce o contromisure.

---

> **Nota**: Il threat model è un documento dinamico che evolve con il sistema e deve essere gestito come parte integrante dello sviluppo software sicuro.

---

## Risorse Utili

- [OWASP Threat Modeling Cheat Sheet](https://owasp.org/www-project-cheat-sheets/cheatsheets/Threat_Modeling_Cheat_Sheet.html)
- [NIST SP 800-30 Guide for Conducting Risk Assessments](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final)
- [Microsoft STRIDE Threat Modeling](https://docs.microsoft.com/en-us/azure/security/develop/threat-modeling-tool)

---
