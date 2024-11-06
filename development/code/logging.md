
# Guida alla Gestione dei Log per la Cyber Sicurezza

Questa guida fornisce le best practice per la gestione dei log da una prospettiva di sicurezza. I log rappresentano una fonte critica di informazioni durante le attività di monitoraggio, troubleshooting, e analisi di eventi di sicurezza. Di seguito, vengono descritti alcuni aspetti fondamentali per stabilire un formato e livelli di log condivisi, linee guida per l'integrazione e la formattazione dei log, e l'adozione di log strutturati.

---

## Definire un Formato e Livelli di Log Condivisi

Per un logging efficace, è essenziale che tutti i componenti di un'applicazione adottino un formato e una struttura di livelli di log condivisi. Questa coerenza permette di aggregare i log in modo standard, facilitando la ricerca e l'analisi dei dati di sicurezza. I livelli consigliati per una configurazione orientata alla cyber sicurezza sono:

1. **TRACE**: Usato per informazioni estremamente dettagliate, principalmente durante il debug.
2. **DEBUG**: Contiene dettagli utili per la diagnosi di problemi non critici. Consigliato solo in ambienti di sviluppo.
3. **INFO**: Fornisce informazioni generali sullo stato dell’applicazione. Include informazioni che possano essere utili al monitoraggio continuo del sistema.
4. **WARNING**: Segnala eventi inattesi ma non critici, che potrebbero tuttavia richiedere attenzione.
5. **ERROR**: Usato per errori che richiedono una revisione immediata da parte di un operatore.
6. **FATAL**: Registra errori gravi che provocano l'interruzione del sistema o di uno dei suoi componenti principali.

Esempio in **Golang** con `slog`:

```go
import (
  "log/slog"
)

func main() {
  logger := slog.New(slog.HandlerOptions{Level: slog.LevelInfo})
  
  logger.Info("Applicazione avviata")
  logger.Warn("Tentativo di accesso non autorizzato", slog.String("utente", "anonimo"))
  logger.Error("Impossibile connettersi al database", slog.String("errore", "connessione rifiutata"))
}
```

Esempio in **Node.js** con `pino`:

```javascript
const pino = require('pino');
const logger = pino({ level: 'info' });

logger.info("Applicazione avviata");
logger.warn("Tentativo di accesso non autorizzato", { utente: "anonimo" });
logger.error("Impossibile connettersi al database", { errore: "connessione rifiutata" });
```

---

## Linee Guida per l'Integrazione e la Formattazione dei Log

Per mantenere i log utili e interpretabili, è importante seguire alcune linee guida:

- **Utilizzare un formato timestamp coerente**: Aggiungere il timestamp in formato ISO 8601 per una migliore leggibilità e per facilitare l'analisi temporale degli eventi.
- **Usare contesto esplicito nei log**: Ogni log dovrebbe includere informazioni contestuali come ID utente, ID richiesta, e endpoint coinvolto, dove possibile.
- **Evitare informazioni sensibili**: Mai loggare dati sensibili, come password, dati di autenticazione, e altre informazioni personali. Mascherare o rimuovere completamente queste informazioni.
- **Separare i log in base al livello di sicurezza**: Creare canali di log separati per attività sensibili. Ad esempio, le richieste di autenticazione e accesso possono essere registrate in un file separato.

Esempio di log con timestamp e contesto in **Golang**:

```go
  logger.Info("Richiesta autenticazione utente",
    slog.String("utente", "anonimo"),
    slog.String("endpoint", "/login"),
    slog.String("timestamp", time.Now().Format(time.RFC3339)))
```

Esempio in **Node.js**:

```javascript
  logger.info("Richiesta autenticazione utente", {
    utente: "anonimo",
    endpoint: "/login",
    timestamp: new Date().toISOString()
});
```

---

## Utilizzo di Log Strutturati

I log strutturati sono essenziali per una gestione efficace dei dati di log, consentendo l'analisi automatizzata e l'elaborazione su larga scala. Utilizzare log strutturati migliora la capacità di ricerca e filtraggio dei log, facilitando l'identificazione rapida di eventi di sicurezza.

In pratica, i log strutturati utilizzano chiavi e valori JSON o altri formati strutturati per memorizzare ogni elemento del log. La struttura JSON consente di inviare i log a sistemi di aggregazione e analisi con il minimo sforzo di trasformazione.

Esempio in **Golang** con `slog`:

```go
logger := slog.New(slog.HandlerOptions{Level: slog.LevelInfo})

logger.Info("Evento di accesso", slog.String("utente", "user123"), slog.String("azione", "login"), slog.Int("tentativi", 3))
```

Esempio in **Node.js** con `pino`:

```javascript
logger.info({
    utente: "user123",
    azione: "login",
    tentativi: 3
}, "Evento di accesso");
```

---

Seguendo queste linee guida, è possibile creare una pipeline di logging sicura e strutturata che consente un monitoraggio accurato e una gestione efficiente degli eventi di sicurezza. Le pratiche descritte aiutano a mantenere i log leggibili, sicuri e utili per rilevare e rispondere prontamente agli incidenti di sicurezza.
