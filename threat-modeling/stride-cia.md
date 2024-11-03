# Modello STRIDE e CIA

Questa guida offre una panoramica del modello **STRIDE** e della triade di sicurezza **Confidentiality, Integrity, and Availability (CIA)**. STRIDE è un framework che aiuta a identificare e categorizzare le minacce di sicurezza durante la progettazione del sistema, mentre la triade CIA rappresenta i principali obiettivi della sicurezza informatica.

---

## Il Modello STRIDE

**STRIDE** è un modello sviluppato da Microsoft per classificare le minacce di sicurezza in sei categorie principali. Ogni categoria corrisponde a una diversa tipologia di minaccia che può colpire un sistema informatico.

| Minaccia                       | Descrizione                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------|
| **S - Spoofing**               | Impersonificazione di un’entità legittima per ottenere accesso non autorizzato.     |
| **T - Tampering**              | Modifica o alterazione non autorizzata dei dati o del sistema.                      |
| **R - Repudiation**            | Rifiuto da parte di un utente di aver eseguito un'azione o una transazione.         |
| **I - Information Disclosure** | Accesso non autorizzato a informazioni sensibili.                                   |
| **D - Denial of Service**      | Tentativo di rendere un sistema o servizio indisponibile agli utenti legittimi.     |
| **E - Elevation of Privilege** | Acquisizione di privilegi più alti per eseguire azioni non autorizzate nel sistema. |

### Applicazione del Modello STRIDE

1. **Identificazione delle Superfici di Attacco**: individua i punti di contatto tra il sistema e gli attori esterni, come interfacce di rete o endpoint API.
2. **Categorizzazione delle Minacce**: associa ogni minaccia identificata a una categoria STRIDE per determinarne l'impatto potenziale.
3. **Mitigazione e Contromisure**: stabilisci le contromisure necessarie per ciascuna minaccia, con particolare attenzione agli obiettivi di sicurezza del sistema.

---

## Triade di Sicurezza: Confidentiality, Integrity, and Availability (CIA)

La triade **Confidentiality, Integrity, and Availability (CIA)** rappresenta i tre principali obiettivi della sicurezza informatica. Ogni obiettivo corrisponde a un aspetto fondamentale per la protezione delle informazioni e delle risorse del sistema.

### Confidentiality (Riservatezza)

- **Descrizione**: Garantisce che i dati siano accessibili solo a chi è autorizzato.
- **Esempi di Misure di Protezione**: Crittografia, controllo degli accessi e gestione delle identità.

### Integrity (Integrità)

- **Descrizione**: Assicura che i dati e le risorse non siano alterati o manipolati da entità non autorizzate.
- **Esempi di Misure di Protezione**: Hashing, firma digitale e sistemi di controllo delle versioni.

### Availability (Disponibilità)

- **Descrizione**: Assicura che i servizi e i dati siano disponibili per gli utenti legittimi quando richiesto.
- **Esempi di Misure di Protezione**: Ridondanza del sistema, gestione delle risorse e prevenzione DDoS.

---

## Impatto del Modello STRIDE sulla CIA

Ogni categoria di minaccia di STRIDE può compromettere uno o più aspetti della CIA. La seguente tabella descrive come ciascuna minaccia influisce sulla riservatezza, integrità o disponibilità.

| Minaccia                   | Impatto sulla CIA                                                                                                                                                                                   |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Spoofing**               | Compromette la **Confidentiality** e l'**Integrity**: gli attori non autorizzati possono impersonare utenti legittimi e accedere a dati riservati o alterare dati.                                  |
| **Tampering**              | Compromette l'**Integrity**: manipola dati o configurazioni del sistema, mettendo a rischio l'affidabilità delle informazioni.                                                                      |
| **Repudiation**            | Compromette la **Confidentiality** e l'**Integrity**: un utente potrebbe negare di aver eseguito azioni, rendendo difficile mantenere la tracciabilità.                                             |
| **Information Disclosure** | Compromette la **Confidentiality**: permette l'accesso non autorizzato a dati sensibili, causando perdite di dati riservati.                                                                        |
| **Denial of Service**      | Compromette la **Availability**: rende il sistema o i servizi inaccessibili, impattando negativamente sull'operatività.                                                                             |
| **Elevation of Privilege** | Compromette la **Confidentiality**, l'**Integrity** e la **Availability**: un attore non autorizzato ottiene accessi privilegiati, con possibilità di accesso, modifica o blocco di dati e servizi. |

---

## Procedura per Applicare STRIDE e CIA nella Progettazione Sicura

1. **Analizza le Superfici di Attacco**: per ciascun punto di interazione, valuta se ci sono rischi di spoofing, tampering o altre minacce STRIDE.
2. **Determina l'Impatto sulla CIA**: per ogni minaccia STRIDE, valuta l'impatto su Confidentiality, Integrity e Availability.
3. **Definisci le Contromisure**: applica controlli di sicurezza specifici per ciascun tipo di minaccia, con focus su riservatezza, integrità e disponibilità.

> **Nota**: Utilizzare STRIDE e CIA consente di avere una visione completa e sistematica dei rischi di sicurezza, assicurando una copertura delle vulnerabilità nella progettazione del sistema.

---

## Risorse Utili

- [OWASP Threat Modeling](https://owasp.org/www-project-threat-modeling/)
- [Microsoft STRIDE Threat Modeling](https://docs.microsoft.com/en-us/azure/security/develop/threat-modeling-tool)
- [NIST Framework for Improving Critical Infrastructure Cybersecurity](https://www.nist.gov/cyberframework)

---
