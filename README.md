# ChatBot

Un'applicazione di chat intelligente che offre un'interfaccia intuitiva per conversazioni multiple con un assistente AI. Il progetto è strutturato con un backend Python Flask per la gestione delle conversazioni e un frontend Angular per l'interfaccia utente.

## Caratteristiche Principali

- 💬 Gestione di conversazioni multiple
- 🔄 Sistema di sessioni per utenti
- 🔒 Autenticazione tramite API key
- 📝 Storico completo delle conversazioni
- 🤖 Integrazione con modello AI locale
- 🎯 Supporto per embeddings

## Struttura del Backend

Il backend è sviluppato in Python utilizzando Flask e offre le seguenti API:

- Gestione Sessioni (`/api/session`)
- Gestione Conversazioni (`/api/conversation`)
- Gestione Messaggi (`/api/message`)
- Elaborazione Domande (`/api/question`)

## Tecnologie Utilizzate

### Backend
- Python
- Flask
- CORS
- Sistema di embedding personalizzato
- Modello LLM locale
- PostgreSQL con pgvector

### Frontend
- Angular
- TypeScript
- Angular Material
- Nginx

## Architettura Docker

Il progetto è completamente containerizzato e utilizza tre servizi principali:

### App Service
- Backend Python Flask
- Integrazione con Ollama per il modello AI
- Espone la porta 5001

### Database Service
- PostgreSQL con estensione pgvector per gestione embeddings
- Costruito con supporto personalizzato per vettori
- Espone la porta 54321

### Frontend Service
- Build multi-stage per l'applicazione Angular
- Servito tramite Nginx
- Espone la porta 4200

## Avvio dell'Applicazione

L'intero stack applicativo può essere avviato con un singolo comando:

```bash
docker-compose up --build
```

L'applicazione sarà accessibile all'indirizzo `http://localhost:4200`

## API Key

L'applicazione richiede un'API key per l'autenticazione. L'API key predefinita è configurata nel backend.
