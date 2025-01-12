# Crawler

Questo notebook contiene codice per eseguire il crawling di Wikipedia e indicizzarne il contenuto utilizzando Redis.

## Caratteristiche

Il notebook fornisce le seguenti funzionalità:

1. **Estrae il contenuto da una pagina di Wikipedia:** utilizza la libreria `BeautifulSoup` per estrarre il contenuto della pagina HTML di una pagina di Wikipedia.
2. **Cerca i link in una pagina di Wikipedia:** Cerca tutti i link in una pagina di Wikipedia e li filtra per includere solo i link validi alle altre pagine di Wikipedia.
3. **Cerca parole in una pagina di Wikipedia:** estrae le parole dal contenuto della pagina e le pulisce rimuovendo la punteggiatura e convertendole in minuscolo.
4. **Indicizza le parole in Redis:** memorizza le parole e il loro conteggio per ogni pagina di Wikipedia in un database Redis. Utilizza una pipeline Redis per migliorare le prestazioni.
5. **Esegue il crawling di Wikipedia utilizzando l'algoritmo BFS:** implementa un web crawler che utilizza l'algoritmo Breadth-First Search (BFS) per esplorare Wikipedia e indicizzare più pagine.
6. **Esegue il crawling persistente:** memorizza la coda di crawling e l'insieme di URL visitati in Redis per consentire il crawling persistente in più sessioni.
7. **Identifica le parole di arresto:** analizza l'indice per identificare le parole più frequenti, che possono essere considerate parole di arresto.
8. **Genera un grafico Zipf:** crea un grafico Zipf per visualizzare la distribuzione della frequenza delle parole nell'indice.

## Utilizzo

Per utilizzare il notebook, è necessario disporre di Redis installato ed eseguito. È possibile installare Redis utilizzando pip install redis. È possibile avviare il server Redis eseguendo redis-server.

Una volta installato ed eseguito Redis, è possibile eseguire le celle nel notebook per eseguire il crawling di Wikipedia e indicizzarne il contenuto.

## Note

Il notebook utilizza la libreria WikiFetcher per limitare la velocità delle richieste a Wikipedia ed evitare di essere bloccato.
Il notebook utilizza la libreria redis per interagire con il database Redis.
Il notebook contiene un'implementazione dell'algoritmo BFS per eseguire il crawling di Wikipedia.
