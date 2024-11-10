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

## Principi Generali di Sicurezza

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

## Design e Pianificazione

### Threat Modeling e Classificazione Rischi

- [x] Threat Modeling
  - [x] STRIDE
  - [x] CIA: Confidentiality, Integrity, and Availability
  - [x] Definizione di una classe/livello di rischio per ogni componente
  - [ ] Approccio basato sulla probabilità e sull'impatto del rischio

### Sicurezza dell'Infrastruttura

- [ ] Design dell'infrastruttura
  - [x] Infrastructure as Code (IaC)
  - [ ] Segmentazione e isolamento dei network
- [ ] Design dei servizi
  - [ ] Impostazione di criteri di accesso e permessi
  - [ ] Definizione di Service Level Agreements (SLA) e obiettivi di uptime
- [ ] Scelta degli standard di sicurezza

## Sviluppo Sicuro

### Infrastruttura

- [ ] Hardening dell'infrastruttura
  - [ ] Configurazione sicura dei server, firewall e database
  - [ ] Abilitazione del logging e auditing per il monitoraggio
- [ ] IaC
  - [ ] Verifica di sicurezza per gli script IaC

### Codice

- [ ] Sviluppo del codice sicuro
  - [ ] Leggibilità del codice
    - [x] Scelta della tecnologia di formattazione
    - [x] Definire una formattazione condivisa
  - [x] Verifica degli errori (linting)
    - [x] Scelta della tecnologia di linting
    - [x] Definire le regole di linting condivise
  - [x] Logging
    - [x] Definire formato e livelli di log condivisi
    - [x] Definire linee guida per l'integrazione dei log
    - [x] Utilizzo di log strutturati
  - [x] Gestione delle dipendenze
    - [x] Valutazione della licenza
    - [x] Valutazione della sicurezza
  - [ ] Evitare patterns non sicuri
  - [x] Gestione degli errori
  - [x] Manutenzione del codice
  - [x] Gestione degli avvisi di linting e compilazione
  - [x] Autenticazione e autorizzazione affidabili
  - [x] Cifratura forte consolidata
  - [ ] Test di sicurezza e qualità
    - [x] Test di unità
      - [x] Scelta del framework di test
      - [x] Definire la Test Coverage minima
    - [x] Test di integrazione
    - [x] Test End-to-End (E2E)
    - [ ] Test di performance
    - [ ] Test di sicurezza
    - [ ] Test di configurazione
  - [x] Source Version Control
    - [x] Evitare secret nel codice
    - [x] Effettuare Code Review
  - [x] Utilizzo di template per nuovi progetti

## Verifica e Test

### Codice e Dipendenze

- [ ] Verifica del codice
  - [ ] Vulnerabilità del codice
    - [ ] Software Composition Analysis (SCA)
      - [ ] Verifica vulnerabilità note nelle dipendenze
      - [ ] Generazione report e SBOM (Software Bill of Materials)
        - [ ] SPDX (Linux Foundation)
        - [ ] DependencyTrack (OWASP Foundation)
  - [ ] Static Application Security Testing (SAST)
    - [ ] Linters e validatori
    - [ ] Identificazione pattern vulnerabili
    - [ ] Rilevazione di secret nel codice
  - [ ] Dynamic Application Security Testing (DAST)

### Container e Infrastruttura

- [ ] Verifica dei container
  - [ ] Rilevazione di immagini container compromesse
  - [ ] Verifica vulnerabilità e integrità delle immagini container
- [ ] Verifica dell'infrastruttura
  - [ ] Verifica configurazioni errate
  - [ ] Verifica vulnerabilità server e network

### Automazione e Continuous Testing

- [ ] Automazione
  - [ ] Fase di sviluppo
    - [ ] Security plugins per IDE
    - [ ] Pre-commit hooks
  - [ ] Fase di CI
    - [ ] Esecuzione test (Unità, Integrazione, E2E, Performance, Sicurezza, Configurazione)
    - [ ] Verifica vulnerabilità supply chain
  - [ ] Fase operativa
    - [ ] Continuous monitoring
      - [ ] Dynamic application security testing
      - [ ] Cloud configuration validation
      - [ ] Infrastructure scanning
    - [ ] Threat intelligence
    - [ ] Penetration testing
    - [ ] Blameless postmortems

## Risposta e Gestione delle Minacce

- [ ] Incident Response
  - [ ] Automazione nella risposta agli incidenti
  - [ ] Definizione e test di piani di risposta agli incidenti
- [ ] Management of Threats
  - [ ] Monitoraggio attivo e continuo delle minacce
  - [ ] Reporting periodico sulle minacce

## Politiche e Sicurezza Fisica

### Policy Aziendali

- [x] Acceptable Use Policy (AUP)
- [x] Information Security Policy (ISP)
- [x] Non-Disclosure Agreement (NDA)

### Gestione Accessi Fisici e Sicurezza degli Asset

- [x] Accessi fisici
  - [x] Registro accessi in azienda
  - [x] Area sicura per ospiti
- [x] Gestione e sicurezza degli asset
  - [x] Etichettatura e classificazione
  - [x] Manutenzione
  - [x] Uso limitato a scopi aziendali
  - [x] Distruzione sicura a fine vita

### Protezione delle Informazioni e Sicurezza dei Dispositivi

- [x] Cifratura dei volumi sui PC aziendali
- [x] Utilizzo di antivirus e firewall
- [x] Gestione della postazione di lavoro
- [ ] Autenticazione a due fattori
- [x] Divieto di dispositivi di archiviazione non autorizzati
- [x] Uso di dispositivi con cifratura
- [x] Autenticazione biometrica, token o password sicure

## Riferimenti e Standard di Sicurezza

### Vulnerability Database

- [ ] CVE
- [ ] OSV
- [ ] Go Vulnerability Database
- [ ] GitHub Advisory Database
  - [ ] NPM audit

### Standard e Framework

- [ ] OWASP Top 10
- [ ] OWASP IoT Top 10
- [ ] CSA IoT Security Controls Framework
- [ ] ISO 27001

### Normative

- [ ] Cyber Resilience Act
- [ ] NIS 2

## Note Aggiuntive

- [ ] Linee guida per
  - [ ] Sviluppo
  - [ ] Test
  - [ ] Continuous integration
  - [ ] Deployment
  - [ ] Monitoraggio
  - [ ] Gestione degli incidenti

- [ ] Utilizzo di tecnologie standard, affidabili e mantenute
- [ ] Ottimizzazione delle performance e dei consumi in fase di progettazione
