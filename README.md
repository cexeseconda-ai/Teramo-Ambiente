# Giro · Raccolta differenziata Teramo

Applicazione web mobile first, statica: HTML, CSS e JavaScript senza dipendenze o compilazione.

## Pubblicazione su GitHub Pages

1. Crea un repository su GitHub.
2. Estrai questo ZIP e carica **il contenuto** della cartella `giro-teramo` nella radice del repository: `index.html`, `app.js`, `data.js`, `.nojekyll` e questo README.
3. In **Settings → Pages → Build and deployment**, scegli **Deploy from a branch**.
4. Seleziona il branch `main` e la cartella `/ (root)`, quindi Save.
5. GitHub mostrerà il link del sito quando la pubblicazione sarà completata.

## Avvio locale

Nella cartella del progetto esegui:

```sh
python3 -m http.server 8000
```

Apri http://localhost:8000 nel browser. Non servono npm, chiavi API o un backend.

## File

- `index.html`: struttura e stile responsive.
- `app.js`: navigazione, calendario, ricerca, preferenze locali ed esportazione ICS.
- `data.js`: date delle raccolte 2026 per città/San Nicolò, zona A e zona B.
- `.nojekyll`: permette la pubblicazione statica diretta con GitHub Pages.

## Dati e limiti

Progetto indipendente, non affiliato a Teramo Ambiente. Fonte: https://www.differenziatateramo.it/index.php?id=64

I dati sono una fotografia dei calendari ufficiali 2026 consultati il 3 novembre 2026; non si aggiornano automaticamente. Verificare eventuali avvisi del gestore. Per gli anni successivi occorre aggiornare dati e logica del calendario (attualmente fissata al 2026).

Le preferenze e i ritiri segnati sono salvati in localStorage nel browser. Nessun account e nessuna sincronizzazione fra dispositivi.

L'esportazione `.ics` include le esposizioni dei prossimi 30 giorni, alle 20:00 della sera precedente al ritiro. Il file deve essere importato nel calendario del telefono; gli avvisi dipendono dalle impostazioni di quel calendario. Non sono implementate notifiche push.

## Verifica

Controllata la sintassi JavaScript e la presenza di 365 date per ciascuna zona. Alcune date di novembre sono state confrontate con i calendari ufficiali. La verifica visiva e funzionale in browser non è stata completata nell'ambiente di creazione.
