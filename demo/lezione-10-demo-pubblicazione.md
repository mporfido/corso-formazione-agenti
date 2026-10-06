# Lezione 10 · Demo — La pubblicazione, passo per passo

> Conduce il formatore · circa 5 minuti · slide 11 di `slides/lezione-10.html`

Si guarda la skill `pubblica` di Geode lavorare su un sito di prova. Il messaggio è uno
solo: **l'agente fa i passaggi tecnici, ma si ferma dove serve una vostra decisione, e il
sito che nasce è pubblico.**

## Prima della lezione

- [ ] Un sito Geode di prova, **senza alcun contenuto riservato**, con una lezione vera,
      salvato. Se c'è lavoro non salvato, la demo mostra anche il passo 2.
- [ ] Un account GitHub **di servizio per la demo**, se non volete lasciare tracce del
      personale. Il nome utente finirà nell'indirizzo mostrato in aula.
- [ ] Nome ed email dei salvataggi del sito di prova controllati: finiranno nella storia
      pubblica.
- [ ] `gh` installato **ma non autenticato**, così si vede l'accesso (`gh auth logout` prima di
      cominciare). Il browser pronto per l'accesso.
- [ ] Il nome del repository di prova deciso e libero (per esempio `demo-lezione-10`).
- [ ] **Riserva** se la rete non va: tre screenshot già fatti (richiesta di accesso, consenso
      sul nome, sito online), o un sito già pubblicato da mostrare.
- [ ] Dopo la lezione: cancellare il repository di prova. Serve il permesso `delete_repo`
      (`gh auth refresh -s delete_repo`), oppure si fa dal sito di GitHub (Settings, in fondo
      alla pagina del repository).

## Passi

1. **Si dice «voglio pubblicare il sito»** nell'assistente, aperto sul sito di prova. Si legge
   a voce la prima risposta dell'agente.
2. **Salvataggio.** Se c'è lavoro non salvato, propone di salvarlo. Mostrare che lo chiede.
3. **Accesso.** L'agente verifica `gh` e fa partire (o chiede di far partire) l'accesso con
   `gh auth login -s workflow`. Si mostra il browser: la richiesta di autorizzazione, leggendo
   che cosa chiede. **Fermarsi sul permesso `workflow`**: serve perché il sito contiene i file
   che lo pubblicano; se manca, il caricamento viene rifiutato.
4. **Corsi dimostrativi.** L'agente chiede se `benvenuto`, `esempio-matematica` ed `esempi`
   devono andare online. Rispondere di toglierli e far notare che li elimina e ricompila il
   sito.
5. **Nome e consenso.** Propone un nome e l'indirizzo `https://<utente>.github.io/<nome>/`,
   dichiara che il sito sarà **pubblico** e chiede il sì. Fermarsi e chiedere in aula: «che
   cosa potrebbe esserci di sbagliato in un sito pubblico?» (dati di studenti, brani copiati,
   un'email personale nella storia). Poi dire sì.
6. **Online.** Creazione del repository e attivazione di Pages. Dopo circa due minuti si apre
   il link. Se non è ancora pronto, usare l'attesa per dire che ogni modifica futura passa da
   «aggiorna il sito».

## Che cosa deve succedere

- I corsisti vedono che l'agente **si ferma** in tre punti (accesso, corsi dimostrativi,
  consenso sul nome) e non pubblica da solo.
- Qualcuno chiede se il sito si può nascondere: no, su Pages gratuito non c'è un sito
  privato. Chi non vuole pubblicare resta in locale.

## Se qualcosa va storto

- **Il caricamento è rifiutato per `workflow`.** È il guaio previsto, e mostrarlo è utile:
  `gh auth refresh -h github.com -s workflow`, conferma nel browser, si ripete.
- **La rete blocca GitHub.** Piano B: gli screenshot, o il sito già pubblicato.
- **Il sito non compare dopo 3-4 minuti.** Chiedere all'agente di guardare l'ultima esecuzione
  (`gh run list`); l'errore tipico è una lezione che non compila. Nel frattempo, andare avanti
  con la slide successiva.
- **L'agente non chiede il consenso.** Fermarlo e dirlo ad alta voce: è la regola della slide.
