# cyber-resilience

cyber-resilience e' un progetto che si propone di creare un framework di riferimento per la gestione della sicurezza e della cyber-resilienza a livello di azienda, codice e infrastruttura. Il progetto e' composto dai seguenti elementi:

- Principi: definizione di principi generali per la gestione della sicurezza e della cyber-resilienza
- Struttura: definizione di una struttura per la gestione della sicurezza e della cyber-resilienza
- Cyber-resilienza per l'azienda: definizione di linee guida per la gestione della sicurezza e della cyber-resilienza a livello di azienda
- Cyber-resilienza per il codice: definizione di linee guida per la gestione della sicurezza e della cyber-resilienza a livello di codice
- Cyber-resilienza per l'infrastruttura: definizione di linee guida per la gestione della sicurezza e della cyber-resilienza a livello di infrastruttura

Il progetto si propone di raccogliere e organizzare informazioni su come garantire la sicurezza e la protezione dei dati, delle infrastrutture e delle applicazioni dalle minacce cibernetiche.

## Principi

- [ ] Zero trust
- [ ] Least privilege
- [ ] Keep it simple
- [ ] Clean code
- [ ] Automated procedures
- [ ] Continuous improvements

## Struttura

### Design

- [ ] Threat Modeling
- [ ] Design dell'infrastruttura
- [ ] Design dei servizi
- [ ] Scelta degli standards di sicurezza
- [ ] Definizione di una classe/livello di rischio per ogni componente

### Sviluppo

- [ ] Sviluppo dell'infrastruttura
  - [ ] Hardening dell'infrastruttura
- [ ] Sviluppo del codice
  - [ ] Leggibilità del codice
    - [ ] Scelta della tecnologia di formattazione
    - [ ] Definire una formattazione condivisa
  - [ ] Verifica degli errori (linting)
    - [ ] Scelta della tecnologia di linting
    - [ ] Definire le regole di linting condivise
  - [ ] Logging
    - [ ] Definire un formato e livelli di log condivisi
    - [ ] Definire linee guida per l'integrazione dei log
    - [ ] Utilizzo di log strutturati
  - [ ] Evitare patterns non sicuri
  - [ ] Evitare secret nel codice
  - [ ] Gestione degli errori
  - [ ] Manutenzione del codice
  - [ ] Gestire gli avvisi di linting e compilazione
  - [ ] Utilizzare sistemi di autenticazione ed autorizzazione affidabili
  - [ ] Utilizzare standard di cifratura forte consolidati
  - [ ] Test di unità
    - [ ] Definire Test Coverage minima
  - [ ] Test di integrazione
  - [ ] Test E2E
  - [ ] Test di performance
  - [ ] Test di sicurezza
  - [ ] Test di configurazione
  - [ ] Effettuare Code Review

### Verifica

- [ ] Verifica del codice
  - [ ] Detection delle vulnerabilità del codice
    - [ ] Software Composition Analysis (SCA): analisi sulla composizione
      - [ ] Verifica di vulnerabilità conosciute nelle dipendenze
      - [ ] Generazione di report e SBOM (Software Bill of Materials)
        - [ ] SPDX (Linux Foundation)
        - [ ] DependencyTrack (OWASP Foundation)
  - [ ] Static Application Security Testing (SAST): analisi del codice sorgente
    - [ ] Linters e validatori
    - [ ] Analisi del codice per identificare pattern con possibili vulnerabilità
    - [ ] Identificazione di secret nel codice o risorse correlate
  - [ ] Dynamic Application Security Testing (DAST): analisi sul codice compilato
- [ ] Verifica dei container
  - [ ] Detection delle "poisoned images"
  - [ ] Detection delle vulnerabilità delle immagini container
  - [ ] Verifica di integrità delle immagini container
- [ ] Verifica dell'infrastruttura
  - [ ] Verifica degli errori di configurazione
  - [ ] Verifica delle vulnerabilità server e network
- [ ] Automazione
  - [ ] Fase di Sviluppo
    - [ ] IDE Security plugins
    - [ ] Pre-commit hooks
  - [ ] Fase di CI
    - [ ] Esecuzione test (Unità, Integrazione, E2E, Performance, Sicurezza, Configurazione)
    - [ ] Verifica vulnerabilità supply chain
  - [ ] Fase operativa
    - [ ] Continuous monitoring
      - [ ] Dynamic application security testing
      - [ ] Cloud configuration validation
      - [ ] Infrastructure scanning
    - [ ] Threat intelligence
    - [ ] Penetration testing
    - [ ] Blameless postmortems

## Policy Aziendale

- [ ] Acceptable Use Policy (AUP)
- [ ] Information Security Policy (ISP)
- [ ] Non-Disclosure Agreement (NDA)

- [ ] Gestione degli accessi fisici in azienda
  - [ ] Registro accessi in azienda
  - [ ] Area sicura per l’attesa degli ospiti
- [ ] Gestione e messa in sicurezza degli strumenti aziendali
- [ ] Cifratura e messa in sicurezza dei dati aziendali
- [ ] Cifratura del volume del pc di lavoro
- [ ] Utilizzo di antivirus
- [ ] Utilizzo di firewall software
- [ ] Gestione della postazione di lavoro ed delle informazioni esposte
- [ ] Autenticazione a due fattori
- [ ] Divieto di utilizzo di dispositivi di archiviazione digitale non facenti parte degli asset
- [ ] Utilizzo solo di dispositi di archiviazione con cifratura forte
- [ ] Utilizzo di accesso biometrico, token con chiave privata, o password sicure

## References

- [ ] Vulnerability Database
  - [ ] CVE
  - [ ] OSV
  - [ ] Go Vulnerability Database
  - [ ] GitHub Advisory Database
    - [ ] NPM audit
- [ ] Standard Awareness
  - [ ] OWASP Top 10
  - [ ] OWASP IoT Top 10
- [ ] Frameworks
  - [ ] CSA IoT Security Controls Framework
  - [ ] ISO 27001
- [ ] Laws
  - [ ] Cyber Resilience Act
  - [ ] NIS 2

## Note

- [ ] Strumenti e linee guida per
  - [ ] Sviluppo
  - [ ] Test
  - [ ] Continuous integration
  - [ ] Deployment
  - [ ] Monitoraggio
  - [ ] Responsità agli incidenti

- [ ] Utilizzo di approcci e tecnologie standard, conosciute, consolidate e mantenute.
- [ ] In fase di progettazione, dare attenzione a consumi e performance
