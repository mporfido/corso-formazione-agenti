# Scaletta del corso - 13 ore

## Stato e struttura

Questa e la programmazione di riferimento del corso. Le 13 ore sono organizzate come
moduli autonomi da un'ora, pause comprese, in modo da poter definire successivamente il
numero e la durata degli incontri.

I moduli 1-3 costituiscono il primo incontro di tre ore, in presenza. Gli altri moduli
possono essere aggregati quando sara disponibile il calendario definitivo.

Indicazione temporale flessibile: ogni modulo prevede circa 50-55 minuti di attivita e
5-10 minuti di pausa, transizione o recupero tecnico. Quando piu moduli sono consecutivi,
i minuti possono essere accumulati in una pausa unica.

## Programma ora per ora

### Ora 1 - Dal chatbot all'agente

**Argomenti**

- Apertura, aspettative e raccolta dei casi d'uso dei partecipanti.
- Dimostrazione concreta della differenza tra chatbot e agente.
- Ciclo osserva, pianifica, agisce e verifica.
- Strumenti, memoria, autonomia e supervisione.
- Limiti, allucinazioni e responsabilita umana.

**Obiettivo**

Riconoscere che cosa rende agentico un sistema e distinguere le attivita professionali
adatte all'automazione da quelle che richiedono un controllo umano stretto.

### Ora 2 - Orientarsi negli ambienti agentici

**Argomenti**

- Sondaggio iniziale sulle competenze e sul rapporto con la riga di comando.
- Panoramica grafica di Codex, Claude Code e Antigravity.
- Account, quote gratuite, abbonamenti e vincoli pratici.
- Cartelle, file, estensioni, percorsi e Markdown essenziale.
- Formazione di eventuali gruppi in base alla piattaforma scelta.

**Obiettivo**

Aprire un ambiente agentico e acquisire il modello mentale dell'agente che opera in una
cartella di progetto.

### Ora 3 - Il primo workflow controllato

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

### Ora 4 - Context engineering e memoria permanente

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

### Ora 5 - Knowledge base: file, wiki e RAG

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

### Ora 6 - Usare e comprendere le skill

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

### Ora 7 - Creare skill fondate sulla pedagogia

**Argomenti**

- Intervista per rendere esplicita una procedura docente.
- Obiettivi di apprendimento e Tassonomia di Bloom.
- Progettazione a ritroso, Unita di Apprendimento e compito autentico.
- Generazione di verifiche, criteri e rubriche.
- Descrittori osservabili e coerenza tra obiettivi, attivita e valutazione.
- Revisione umana delle decisioni valutative.

**Obiettivo**

Trasformare una pratica professionale in una procedura agentica ripetibile, fondata su
obiettivi e criteri pedagogici espliciti.

### Ora 8 - Dalla programmazione al calendario delle lezioni

**Argomenti**

- Analisi della programmazione annuale.
- Prerequisiti, vincoli, festivita e ore disponibili.
- Sequenziamento delle unita e milestone.
- Margini di recupero e gestione delle ipotesi mancanti.
- Definizione di un output strutturato e modificabile.
- Prima versione della skill per il calendario delle lezioni.

**Obiettivo**

Generare un calendario didattico motivato e modificabile a partire dalla programmazione
del docente.

### Ora 9 - Dal registro alle prossime lezioni

**Argomenti**

- Uso esclusivo di una classe inventata e di dati sintetici.
- Lettura del PDF fittizio esportato dal registro elettronico.
- Confronto tra calendario pianificato e argomenti svolti.
- Individuazione di ritardi, anticipi e argomenti incompleti.
- Proposta motivata delle lezioni successive.
- Incertezze, minimizzazione dei dati e approvazione del docente.

**Obiettivo**

Costruire un secondo passaggio del workflow che aggiorni il piano sulla base dello stato
reale senza delegare all'agente la decisione finale.

### Ora 10 - Piu agenti per produrre e controllare materiali

**Argomenti**

- Quando conviene dividere un lavoro e quando non conviene.
- Ruoli: ricercatore, progettista didattico, autore e revisore.
- Lavoro parallelo e lavoro sequenziale.
- Isolamento del contesto e sintesi del coordinatore.
- Controllo delle fonti e risoluzione dei risultati discordanti.
- Costi, quote e confronto operativo tra le piattaforme.

**Obiettivo**

Scomporre un compito complesso e coordinare piu agenti per ottenere un materiale unico,
coerente e verificato.

### Ora 11 - Progettare una lezione interattiva

**Argomenti**

- `math-rocks` come esempio avanzato e il repository barebones come punto di partenza.
- Distinzione tra motore, configurazione e contenuti.
- Corso e lezioni descritti mediante Markdown.
- Esercizi, scelte multiple, slider, contenuti progressivi e visualizzazioni.
- Definizione dell'obiettivo pedagogico prima della soluzione tecnica.
- Esempi per materie scientifiche, umanistiche, linguistiche e tecniche.

**Obiettivo**

Progettare una breve attivita interattiva pertinente alla propria disciplina prima di
affidarne la realizzazione all'agente.

### Ora 12 - Laboratorio sul repository barebones

**Argomenti**

- Download e apertura del repository distribuito tramite GitHub.
- Lettura delle istruzioni e delle skill incluse.
- Generazione o adattamento dei contenuti.
- Anteprima HTML e controllo dell'interattivita.
- Correzione tramite dialogo con l'agente.
- Personalizzazione disciplinare e confronto tra piattaforme.

**Obiettivo**

Produrre una lezione interattiva funzionante senza dover conoscere i dettagli tecnici
del motore.

### Ora 13 - Laboratorio aperto, revisione e pubblicazione facoltativa

**Argomenti**

- Scelta libera di un'attivita utile al partecipante.
- Prosecuzione di una lezione interattiva oppure lavoro su calendario, knowledge base,
  verifica, rubrica o skill.
- Confronto informale tra gruppi e piattaforme.
- Checklist di correttezza, pedagogia, privacy, copyright e accessibilita.
- Dimostrazione della pubblicazione su GitHub Pages o Netlify.
- Pubblicazione facoltativa e conservazione del progetto per il lavoro futuro.

**Obiettivo**

Applicare il metodo a un'esigenza professionale reale e consolidare un progetto o un
workflow riutilizzabile, senza trasformare l'attivita in una prova finale.

## Fili conduttori

### Sicurezza applicata

- Ora 1: limiti, allucinazioni e responsabilita.
- Ora 3: permessi, backup e azioni distruttive.
- Ora 4: dati personali e contesto permanente.
- Ora 5: fonti, citazioni e copyright.
- Ora 7: valutazione assistita e responsabilita del docente.
- Ora 9: dati sintetici, minimizzazione e controllo umano.
- Ora 10: permessi e controllo dei sub-agenti.
- Ora 13: verifica prima della pubblicazione.

### Confronto tra piattaforme

Il confronto tra Codex, Claude Code e Antigravity non costituisce un modulo separato.
Viene inserito nei momenti in cui emergono differenze rilevanti:

- ora 2: accesso, interfaccia e configurazione;
- ora 4: file guida e memoria di progetto;
- ora 6: collocazione e attivazione delle skill;
- ora 10: agenti paralleli e coordinamento;
- ora 12: esperienza pratica nello stesso tipo di progetto.

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
- [skill teach](https://github.com/mattpocock/skills/tree/main/skills/productivity/teach)
- [OECD Digital Education Outlook 2026](https://www.oecd.org/en/publications/oecd-digital-education-outlook-2026_062a7394-en.html)
- `C:\Users\mikil\Progetti\wiki-ia-agenti`
- `C:\Users\mikil\Progetti\wiki-didattica-scuola`

