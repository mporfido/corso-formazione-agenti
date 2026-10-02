# Scaletta del corso - 10 lezioni

## Stato e struttura

Questa e la programmazione di riferimento del corso. Le 10 lezioni sono
autonome, da un'ora ciascuna, pause comprese, in modo da poter definire successivamente il
numero e la durata degli incontri.

Le lezioni 1-3 costituiscono il primo incontro di tre ore, in presenza. Le altre lezioni
possono essere aggregate quando sara disponibile il calendario definitivo.

Indicazione temporale flessibile: ogni lezione prevede circa 50-55 minuti di attivita e
5-10 minuti di pausa, transizione o recupero tecnico. Quando piu lezioni sono consecutive,
i minuti possono essere accumulati in una pausa unica.

## Programma lezione per lezione

### Lezione 1 - Dal chatbot all'agente

**Argomenti**

- Apertura, aspettative e raccolta dei casi d'uso dei partecipanti.
- Dimostrazione concreta della differenza tra chatbot e agente.
- Ciclo osserva, pianifica, agisce e verifica.
- Strumenti, memoria, autonomia e supervisione.
- Limiti, allucinazioni e responsabilita umana.

**Obiettivo**

Riconoscere che cosa rende agentico un sistema e distinguere le attivita professionali
adatte all'automazione da quelle che richiedono un controllo umano stretto.

### Lezione 2 - Orientarsi negli ambienti agentici

**Argomenti**

- Sondaggio iniziale sulle competenze e sul rapporto con la riga di comando.
- Panoramica grafica di Codex, Claude Code e Antigravity.
- Account, quote gratuite, abbonamenti e vincoli pratici.
- Cartelle, file, estensioni, percorsi e Markdown essenziale.
- Formazione di eventuali gruppi in base alla piattaforma scelta.

**Obiettivo**

Aprire un ambiente agentico e acquisire il modello mentale dell'agente che opera in una
cartella di progetto.

### Lezione 3 - Il primo workflow controllato

**Argomenti**

- Obiettivo, contesto, vincoli e criterio di completamento.
- Pianificazione prima dell'esecuzione.
- Lettura e modifica dei file da parte dell'agente.
- Osservazione delle azioni e verifica del risultato.
- Permessi, backup, reversibilita e azioni distruttive.
- Primo esercizio guidato in piccoli gruppi.

**Obiettivo**

Portare a termine un piccolo compito agentico mantenendo controllo, tracciabilita e
possibilita di correzione.

### Lezione 4 - Context engineering e memoria permanente

**Argomenti**

- Limiti della conversazione e della finestra di contesto.
- Contesto utile, rumore e degrado delle prestazioni.
- Istruzioni permanenti e file guida: `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`.
- Struttura a mappa con dettagli conservati in file separati.
- Creazione di un primo profilo disciplinare del docente.
- Esclusione dei dati personali dal contesto permanente.

**Obiettivo**

Costruire un contesto permanente, sintetico e riutilizzabile, riducendo la necessita di
ripetere istruzioni a ogni conversazione.

### Lezione 5 - Knowledge base: file, wiki e RAG

**Argomenti**

- Raccolta, selezione e organizzazione delle fonti.
- Indice, collegamenti e approfondimento progressivo.
- LLM wiki come knowledge base navigabile dall'agente.
- Differenza concettuale tra consultazione dei file e RAG.
- NotebookLM come esempio di sistema RAG, senza laboratorio dedicato.
- Qualita delle fonti, citazioni, allucinazioni e copyright.

**Obiettivo**

Organizzare una piccola knowledge base disciplinare e scegliere consapevolmente quando
usare file navigabili dall'agente o un sistema RAG.

### Lezione 6 - Usare e comprendere le skill

**Argomenti**

- Istruzione permanente e skill specializzata.
- Anatomia essenziale di una skill e materiali di riferimento.
- Attivazione, confini e criteri di applicazione.
- Installazione o adattamento di una skill esistente.
- La skill `teach` come esempio: missione, memoria dell'apprendimento, zona di sviluppo
  prossimale, recupero attivo e lezioni HTML.
- Possibili impieghi futuri con gli studenti, presentati soltanto come suggestione.

**Obiettivo**

Comprendere quando una procedura merita di diventare una skill e saper adattare una
procedura esistente senza partire da zero.

### Lezione 7 - Creare skill fondate sulla pedagogia

**Argomenti**

- Procedura svolta passo passo con l'agente, corretta dal docente e distillata in skill
  dopo la verifica del risultato: le correzioni diventano regole.
- Obiettivi di apprendimento e Tassonomia di Bloom.
- Progettazione a ritroso, Unita di Apprendimento e compito autentico.
- Generazione di verifiche, criteri e rubriche.
- Descrittori osservabili e coerenza tra obiettivi, attivita e valutazione.
- Revisione umana delle decisioni valutative.

**Obiettivo**

Trasformare una pratica professionale in una procedura agentica ripetibile, fondata su
obiettivi e criteri pedagogici espliciti.

### Lezione 8 - Come funziona math-rocks

**Argomenti**

- `math-rocks` come esempio avanzato: che cosa fa una lezione interattiva e che cosa vede
  lo studente.
- Distinzione tra motore, configurazione e contenuti: il motore non si tocca, il sito del
  docente sta in `content/`, `site.yaml` e nel tema grafico.
- Corso, lezioni e passi descritti in Markdown: domande aperte, scelte multiple, slider,
  contenuti che si rivelano a obiettivi completati, formule, grafici e animazioni.
- Dal testo al sito: anteprima in locale, compilazione, pubblicazione come sito statico;
  che cosa viene salvato nel browser dello studente e quali servizi esterni sono coinvolti.
- Il minimo di Python: a che cosa serve in questo progetto, che cosa lascia fare
  all'agente, come riconoscere un errore di installazione.
- Il minimo di Git e GitHub: repository, salvataggio come fotografia del lavoro, copia
  propria e copia pubblica, differenza tra Git (sul computer) e GitHub (online).
- Definire l'obiettivo pedagogico di una breve attivita interattiva prima di pensare alla
  soluzione tecnica; esempi per materie scientifiche, umanistiche, linguistiche e tecniche.

**Obiettivo**

Capire quali parti del progetto spettano al docente e quali al motore, e arrivare alla
lezione 9 con il computer pronto e con l'idea di una breve attivita da realizzare.

### Lezione 9 - Creare la propria istanza di Geode

**Argomenti**

- Verifica dei prerequisiti: Python, Git e l'assistente scelto.
- Copia indipendente del repository barebones `Geode` in una cartella vuota, con storia
  propria e senza collegamenti per pubblicare nel progetto originale.
- Lettura guidata delle istruzioni (`AGENTS.md`) e delle skill incluse.
- Onboarding con la skill di avvio: nome del sito, materia, veste grafica scelta su
  un'anteprima.
- Prima lezione della propria disciplina a partire dalla scheda di progetto; anteprima
  locale e controllo dell'interattivita.
- Correzione tramite dialogo con l'agente e salvataggio del lavoro con Git.
- Confronto tra piattaforme: onboarding con Claude Desktop, Codex e Antigravity.

**Obiettivo**

Ottenere un'istanza propria e funzionante, con almeno una lezione della propria disciplina
visibile in anteprima, senza dover conoscere i dettagli tecnici del motore.

### Lezione 10 - Personalizzare e pubblicare

**Argomenti**

- Personalizzazione di aspetto, testi e contenuti del sito.
- Prosecuzione libera del lavoro: nuove lezioni, uso di propri appunti e documenti come
  fonte, nuovi componenti interattivi.
- Checklist di correttezza disciplinare, pedagogia, privacy, copyright e accessibilita.
- Pubblicazione su GitHub Pages: account GitHub, GitHub CLI, accesso dal browser e
  permessi richiesti; un sito pubblicato e pubblico per natura.
- Aggiornamenti successivi del sito e del motore; conservazione del progetto per il lavoro
  futuro.
- Chiusura del corso: che cosa portarsi a casa e da dove ripartire.

**Obiettivo**

Completare, controllare e se si vuole pubblicare un'attivita interattiva della propria
disciplina, e portare a casa un progetto riutilizzabile, senza trasformare l'attivita in
una prova finale.

## Fili conduttori

### Sicurezza applicata

- Lezione 1: limiti, allucinazioni e responsabilita.
- Lezione 3: permessi, backup e azioni distruttive.
- Lezione 4: dati personali e contesto permanente.
- Lezione 5: fonti, citazioni e copyright.
- Lezione 7: valutazione assistita e responsabilita del docente.
- Lezione 8: servizi esterni e dati degli studenti in un sito pubblicato.
- Lezione 9: comandi eseguiti dall'agente, dipendenze installate e salvataggi con Git.
- Lezione 10: verifica prima della pubblicazione e permessi concessi a GitHub.

### Confronto tra piattaforme

Il confronto tra Codex, Claude Code e Antigravity non costituisce un modulo separato.
Viene inserito nei momenti in cui emergono differenze rilevanti:

- lezione 2: accesso, interfaccia e configurazione;
- lezione 4: file guida e memoria di progetto;
- lezione 6: collocazione e attivazione delle skill;
- lezione 9: onboarding dello stesso progetto con Claude Desktop, Codex e Antigravity.

Ogni scheda deve distinguere tra concetto stabile, nome usato dal prodotto, disponibilita
nel piano gratuito o a pagamento e stato della funzionalita alla data della lezione.

## Esempi interdisciplinari per il laboratorio

- Materie umanistiche: analisi guidata di un testo, timeline, confronto tra fonti,
  percorso a diramazioni e comprensione linguistica.
- Materie scientifiche: grafici dinamici, slider, simulazioni e sequenze
  previsione-osservazione-spiegazione.
- Materie tecniche: procedure operative, troubleshooting, scelte guidate e simulazione
  di processi.
- Lingue: cloze, scelte multiple, scaffolding lessicale e feedback progressivo.
- Diritto ed economia: analisi di casi, classificazioni, scenari decisionali e lettura
  di dati.

## Riferimenti principali

- [math-rocks](https://github.com/mporfido/math-rocks)
- [Geode](https://github.com/mporfido/geode), il repository barebones delle lezioni 8-10
- [skill teach](https://github.com/mattpocock/skills/tree/main/skills/productivity/teach)
- [OECD Digital Education Outlook 2026](https://www.oecd.org/en/publications/oecd-digital-education-outlook-2026_062a7394-en.html)
- `C:\Users\mikil\Progetti\wiki-ia-agenti`
- `C:\Users\mikil\Progetti\wiki-didattica-scuola`

