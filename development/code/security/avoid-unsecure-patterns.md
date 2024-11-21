
# Guida alla Sicurezza per Evitare Pattern Non Sicuri nello Sviluppo del Codice

Nel processo di sviluppo software, è essenziale adottare pratiche che evitino l’uso di pattern di codice non sicuri, che possono introdurre vulnerabilità e aumentare il rischio di attacchi. Identificare e prevenire questi pattern riduce il rischio di esposizione a minacce comuni come SQL injection, Cross-Site Scripting (XSS), e accessi non autorizzati ai dati. Questa guida evidenzia le pratiche consigliate per scrivere codice sicuro.

## Principi di Base per Evitare Pattern Non Sicuri

- **Convalidare e sanificare tutti gli input**: Non fidarsi mai degli input esterni. Tutti i dati provenienti da fonti esterne (utente, API, file) devono essere convalidati e sanificati per garantire che non contengano caratteri o dati potenzialmente dannosi.
- **Utilizzare tecniche di coding sicure**: Adottare standard di codifica sicuri e utilizzare costrutti linguistici che prevengono pattern di codice rischiosi.
- **Minimizzare l’uso di costrutti pericolosi**: Evitare l’uso di comandi come `eval`, che possono esporre il codice ad attacchi di injection.
- **Gestire correttamente le eccezioni**: Errori non gestiti possono esporre informazioni sensibili. Ogni eccezione dovrebbe essere catturata e gestita in modo sicuro.

## Pattern di Codice da Evitare e Alternative Sicure

### 1. **Injection (SQL, Command, LDAP)**

Le vulnerabilità di injection si verificano quando un'applicazione permette a un utente di inserire comandi o query direttamente nel sistema.

- **Evitare**: String concatenation per le query SQL o comandi di sistema.
- **Alternativa sicura**: Utilizzare query parametrizzate o ORM (Object-Relational Mapping) per l’accesso ai dati. Ad esempio:

#### Golang

```go
// Insecure
query := "SELECT * FROM users WHERE username = '" + username + "'"
db.Query(query)

// Secure
query := "SELECT * FROM users WHERE username = ?"
db.Query(query, username)
```

#### Node.js

```javascript
// Insecure
db.query("SELECT * FROM users WHERE username = '" + username + "'");

// Secure
db.query("SELECT * FROM users WHERE username = ?", [username]);
```

### 2. **Uso di `eval` e Esecuzione di Codice Dinamico**

L'uso di `eval` o esecuzione di codice dinamico può aprire le porte a exploit e attacchi di injection.

- **Evitare**: Utilizzare `eval` per eseguire codice dinamico.
- **Alternativa sicura**: Rimuovere l'uso di `eval` o sostituirlo con metodi più sicuri, come funzioni specifiche che non eseguono codice arbitrario.

#### Golang

```go
// Insecure
evalCode := fmt.Sprintf("executeCommand('%s')", userInput)
exec.Command("sh", "-c", evalCode).Run()

// Secure
if userInput == "allowedCommand" {
    executeCommand(userInput)
}
```

#### Node.js

```javascript
// Insecure
eval("executeCommand('" + userInput + "')");

// Secure
if (allowedCommands.includes(userInput)) {
    executeCommand(userInput);
}
```

### 3. **Hardcoded Credentials**

Hardcodare credenziali (password, token, chiavi API) nel codice rappresenta un grave rischio di sicurezza.

- **Evitare**: Inserire credenziali direttamente nel codice.
- **Alternativa sicura**: Utilizzare variabili di ambiente o servizi di gestione delle credenziali (come AWS Secrets Manager o HashiCorp Vault).

#### Golang

```go
// Insecure
const password = "mysecretpassword"

// Secure
password := os.Getenv("PASSWORD")
```

#### Node.js

```javascript
// Insecure
const PASSWORD = "mysecretpassword";

// Secure
const PASSWORD = process.env.PASSWORD;
```

### 4. **Gestione Inadeguata delle Eccezioni**

Lasciare eccezioni non gestite o esporre dettagli tecnici sugli errori può rivelare informazioni sensibili.

- **Evitare**: Mostrare dettagli di errore agli utenti finali o non gestire le eccezioni.
- **Alternativa sicura**: Gestire le eccezioni con messaggi generici e registrare i dettagli in modo sicuro.

#### Golang

```go
// Insecure
fmt.Println("Error:", err)

// Secure
if err != nil {
    log.Println("An error occurred")
}
```

#### Node.js

```javascript
// Insecure
console.log("Error:", err);

// Secure
if (err) {
    console.error("An error occurred");
}
```
