# cyber-resilience

cyber-resilience e' un progetto che si propone di creare un framework di riferimento per la gestione della sicurezza e della cyber-resilienza a livello di azienda, codice e infrastruttura. Il progetto e' composto dai seguenti elementi:

- Principi: definizione di principi generali per la gestione della sicurezza e della cyber-resilienza
- Struttura: definizione di una struttura per la gestione della sicurezza e della cyber-resilienza
- Cyber-resilienza per l'azienda: definizione di linee guida per la gestione della sicurezza e della cyber-resilienza a livello di azienda
- Cyber-resilienza per il codice: definizione di linee guida per la gestione della sicurezza e della cyber-resilienza a livello di codice
- Cyber-resilienza per l'infrastruttura: definizione di linee guida per la gestione della sicurezza e della cyber-resilienza a livello di infrastruttura

Il progetto si propone di raccogliere e organizzare informazioni su come garantire la sicurezza e la protezione dei dati, delle infrastrutture e delle applicazioni dalle minacce cibernetiche.

## Documenti

### Principi fondamentali

- [Clean Code](priciples/clean-code.md)
- [Continuous Improvement](priciples/continuous-improvement.md)
- [Security by Design](priciples/security-by-design.md)
- [Zero Trust](priciples/zero-trust.md)

---

## Checklist integrazione

### Principi

- [x] Zero trust
- [x] Least privilege
- [x] Keep it simple
- [x] Clean code
- [x] Automated procedures
- [x] Continuous improvements
- [x] Security by design
  - [x] Shift left security
  - [x] Secure by design
  - [x] Security as code

### Struttura

#### Design

- [x] Threat Modeling
  - [x] STRIDE
  - [x] CIA: Confidentiality, Integrity, and Availability
  - [x] Definizione di una classe/livello di rischio per ogni componente
- [ ] Design dell'infrastruttura
  - [x] IaC
- [ ] Design dei servizi
- [ ] Scelta degli standards di sicurezza

#### Sviluppo

- [ ] Sviluppo dell'infrastruttura
  - [ ] Hardening dell'infrastruttura
  - [ ] IaC
- [ ] Sviluppo del codice
  - [ ] Leggibilità del codice
    - [x] Scelta della tecnologia di formattazione
    - [x] Definire una formattazione condivisa
  - [ ] Verifica degli errori (linting)
    - [x] Scelta della tecnologia di linting
    - [x] Definire le regole di linting condivise
  - [x] Logging
    - [x] Definire un formato e livelli di log condivisi
    - [x] Definire linee guida per l'integrazione dei log
    - [x] Utilizzo di log strutturati
  - [x] Scelta delle dipendenze
    - [x] Valutazione della licenza
    - [x] Valutazione della sicurezza
  - [ ] Evitare patterns non sicuri
  - [ ] Evitare secret nel codice
  - [x] Gestione degli errori
  - [x] Manutenzione del codice
  - [ ] Gestire gli avvisi di linting e compilazione
  - [ ] Utilizzare sistemi di autenticazione ed autorizzazione affidabili
  - [ ] Utilizzare standard di cifratura forte consolidati
  - [ ] Test di unità
    - [ ] Scelta di un framwork di test
    - [ ] Definire Test Coverage minima
  - [ ] Test di integrazione
  - [ ] Test E2E
  - [ ] Test di performance
  - [ ] Test di sicurezza
  - [ ] Test di configurazione
  - [ ] Effettuare Code Review
  - [ ] Source Version Control
  - [ ] Utilizzare un template per nuovi progetti

#### Verifica

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

### Response

- [ ] Incident Response
  - [ ] Incident Response Automation
- [ ] Management of Threats

### Policy Aziendale

- [ ] Acceptable Use Policy (AUP)
- [ ] Information Security Policy (ISP)
- [ ] Non-Disclosure Agreement (NDA)

- [ ] Gestione degli accessi fisici in azienda
  - [ ] Registro accessi in azienda
  - [ ] Area sicura per l’attesa degli ospiti
- [ ] Gestione e messa in sicurezza degli asset aziendali
  - [ ] Labels e classificazione
  - [ ] Manutenzione
  - [ ] Utilizzo solo per il fine previsto (divieto  per usi privati)
  - [ ] Distruzione a fine vita
- [ ] Cifratura e messa in sicurezza dei dati aziendali
- [ ] Cifratura del volume del pc di lavoro
- [ ] Utilizzo di antivirus
- [ ] Utilizzo di firewall software
- [ ] Gestione della postazione di lavoro ed delle informazioni esposte
- [ ] Autenticazione a due fattori
- [ ] Divieto di utilizzo di dispositivi di archiviazione digitale non facenti parte degli asset
- [ ] Utilizzo solo di dispositi di archiviazione con cifratura forte
- [ ] Utilizzo di accesso biometrico, token con chiave privata, o password sicure

### References

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

### Note

- [ ] Strumenti e linee guida per
  - [ ] Sviluppo
  - [ ] Test
  - [ ] Continuous integration
  - [ ] Deployment
  - [ ] Monitoraggio
  - [ ] Responsità agli incidenti

- [ ] Utilizzo di approcci e tecnologie standard, conosciute, consolidate e mantenute.
- [ ] In fase di progettazione, dare attenzione a consumi e performance
