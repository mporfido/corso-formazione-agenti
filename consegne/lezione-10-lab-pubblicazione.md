# Lezione 10 · Laboratorio — Rifinire, controllare, se volete pubblicare

> Al computer · da soli · 20 minuti · serve il sito della lezione 9

## Cosa facciamo e perché

Oggi si chiude il lavoro. Rifinite la vostra lezione, la passate a una **checklist di
revisione** e, **solo se volete**, mettete il sito online. Non è una prova finale: l'attività è
vostra e la giudicate voi.

**Un sito pubblicato è pubblico.** GitHub Pages gratuito non ha siti privati: chiunque abbia il
link può aprirlo, e il progetto su GitHub, con i file delle lezioni e la storia dei salvataggi,
si può leggere. Chi non pubblica non ha perso niente: il percorso A basta a raggiungere
l'obiettivo dell'ora.

**Nessun dato di studenti**, nemmeno negli esempi.

## Prima di cominciare

- Il sito della lezione 9 si apre in anteprima (`localhost:5000`) e il lavoro è salvato.
- **Solo per il percorso B:** un account GitHub (gratuito, su github.com). Il nome utente
  comparirà nell'indirizzo del sito.

## Percorso A · per tutti

### 1 · Rifinire · 5 minuti

Cambiate almeno una cosa, chiedendola all'agente. Ad esempio:

- l'aspetto: «rendi i colori più caldi», «prova il tema salvia»;
- un testo: sottotitolo del sito, footer, una spiegazione;
- un contenuto: un passo in più, o una nuova lezione da un vostro appunto («leggi
  `appunti/…` e proponimi la scaletta di una lezione fedele a quel testo»).

**Salvate prima di un cambiamento grande** («salva il lavoro»): se non vi convince si torna indietro.

### 2 · La checklist · 8 minuti

Prima rilettura, fatta dall'agente:

```
Rileggi la lezione «…» con questa checklist: correttezza disciplinare, pedagogia, privacy,
copyright, accessibilità. Elenca i problemi che trovi, con il passo e il motivo.
Non correggere niente: decido io.
```

Poi verificate **voi** ogni punto, e anche quelli che l'agente non ha segnalato:

| Controllo | Domande |
|---|---|
| **Correttezza** | Fatti e numeri sono veri, controllati su una vostra fonte? La risposta segnata come giusta lo è? Niente esempi o citazioni inventati? |
| **Pedagogia** | La sequenza raggiunge l'obiettivo della scheda? Gli errori proposti sono quelli tipici degli studenti? Il feedback spiega il perché? Non è una prova? |
| **Privacy** | Nessun dato di studenti, nessun materiale riservato della scuola? Nome ed email dei salvataggi: sapete quali avete impostato? |
| **Copyright** | Testi e immagini sono vostri o con licenza? Fonti nominate? Nessun brano copiato dal manuale? |
| **Accessibilità** | Contrasto sufficiente? Ogni immagine ha un testo alternativo? Si usa con la sola tastiera (Tab, Invio)? Il colore non è l'unico segnale? |

Infine **provate la lezione da studenti**, dall'inizio alla fine, con almeno una risposta
sbagliata. Correggete quello che trovate: dialogando con l'agente, indicando il passo e il
motivo, oppure a mano nel file.

### 3 · Salvare · 2 minuti

Scrivete: **«Salva il lavoro».** Controllate che la frase del salvataggio dica quello che avete fatto.

Se non volete pubblicare, **avete finito**: passate a «Per chi finisce prima».

## Percorso B · se volete pubblicare · 5 minuti

Fatelo solo se la checklist è passata, avete l'account e siete convinti. Scrivete:

```
Voglio pubblicare il sito.
```

L'agente segue la skill `pubblica`. **Leggete ogni richiesta prima di rispondere.** Si ferma in
questi punti:

1. **Strumenti e accesso.** Se manca GitHub CLI (`gh`), guida l'installazione. Poi vi chiede di
   accedere: si apre il browser, o compare un codice da inserire in una pagina. Il comando è
   `gh auth login -s workflow`. Il permesso **`workflow`** è indispensabile: senza, GitHub rifiuta
   i file che pubblicano il sito. Leggete che cosa autorizzate: è un permesso dato a un
   programma sul vostro account.
2. **Corsi dimostrativi.** Vi chiede se `benvenuto`, `esempio-matematica` ed `esempi` devono andare
   online. Di solito si tolgono: al sito vostro interessa il lavoro vostro.
3. **Nome e consenso.** Propone un nome (ad esempio `lezioni-rossi`) e vi mostra l'indirizzo
   `https://<utente>.github.io/<nome>/`. Vi chiede il **sì esplicito**, perché il sito sarà pubblico.
   **Se non lo chiede, fermatelo.**
4. **Online.** Crea il progetto su GitHub, attiva Pages e, dopo circa due minuti, vi dà il link.

Aprite il link. Se il sito non compare subito, aspettate un minuto: l'agente può controllare la
pubblicazione e dirvi che cosa è successo.

## Da controllare alla fine

- Avete cambiato almeno una cosa e provato la lezione da studenti?
- Avete passato i cinque controlli, e verificato voi i punti segnalati dall'agente?
- Il lavoro è salvato, con una frase che lo descrive?
- Se avete pubblicato: il sito si apre dal link, e sapete che chiunque può leggerlo?
- Sapete dove sta la cartella del progetto e come riprenderla?

## Se qualcosa non va

| Che cosa succede | Che cosa fare |
|---|---|
| Il caricamento è rifiutato: «without `workflow` scope» | Manca il permesso. `gh auth refresh -h github.com -s workflow`, conferma nel browser, poi si ripete. Se il progetto online è già nato vuoto, non va ricreato |
| Il caricamento è rifiutato per autenticazione | `gh auth login -s workflow`, poi `gh auth status` per controllare |
| Il sito non compare dopo qualche minuto | Chiedete all'agente di guardare l'ultima esecuzione. L'errore tipico è una lezione che non compila: si riproduce in locale e si corregge |
| Errore 409 su Pages («già attivo») | Va bene così, non serve altro |
| GitHub non risponde | Può essere la rete della scuola. Provate un'altra rete (hotspot del telefono) e ditelo all'agente |

## Dopo, a casa

- **Aggiornare il sito:** scrivete «aggiorna il sito». Prima si salva, poi l'agente lo manda online;
  dopo circa un minuto il sito è aggiornato. I progressi degli studenti restano, a patto di non
  cambiare mai la sigla dei progressi in `site.yaml`.
- **Aggiornare la piattaforma:** «aggiorna la piattaforma» porta le novità di Geode senza
  toccare corsi e lezioni. Salvate prima; l'agente vi mostra che cosa cambierebbe e chiede il
  vostro ok.
- **Conservare il progetto:** la cartella è il progetto. Tenetene una copia su un altro
  supporto. Per riprenderlo, riapritela nell'assistente: l'agente rilegge `AGENTS.md` e le skill.

## Per chi finisce prima

Aggiungete una seconda lezione dalle vostre note, o un'**interazione nuova** (uno slider,
un contenuto che si rivela dopo la risposta). Poi ripassate la checklist solo sulle parti nuove.
