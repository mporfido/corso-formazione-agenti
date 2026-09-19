# Struttura del corso — quaderno di regia

**Nome:** Dalla IA generativa alla IA agentica

**Pubblico:** docenti di scuola superiore, non tecnici

**Durata:** 13 ore, organizzate in 13 moduli autonomi da un'ora (pause comprese). Le ore 1-3
formano il primo incontro, in presenza; le altre si aggregano quando ci sarà il calendario.

**Programma di riferimento:** [scaletta-corso-13-ore.md](scaletta-corso-13-ore.md). Lì c'è il
*cosa* — argomenti e obiettivo di ogni ora — e non si modifica da qui. Questo file raccoglie
il *come*: fonti, materiale da riusare, demo, laboratori, materiali da preparare, questioni
aperte.

**Convenzione per i riferimenti:** `[[concetti/…]]`, `[[tecniche/…]]` ecc. sono pagine di
`wiki-ia-agenti/wiki/`; `did:nome-pagina` sono pagine di `wiki-didattica-scuola/pagine/`.

## Scelte di impianto

- **Un deck per ora**: `slides/ora-01.html` … `ora-13.html`, stile Manuale. Gli argomenti della
  scaletta sono i punti chiave delle slide.
- **Agnostico rispetto al prodotto**: si impara l'impalcatura, non lo strumento. Il file-guida
  canonico è `AGENTS.md`; `CLAUDE.md` e `GEMINI.md` sono solo rimandi. Molti docenti partono
  dai piani gratuiti (Codex, Antigravity); Claude Code richiede un abbonamento.
- **Il confronto tra piattaforme** non è un modulo: compare nelle ore 2, 4, 6, 10 e 12 come
  *scheda piattaforma* a quattro righe — concetto stabile · nome nel prodotto · piano gratuito
  o a pagamento · stato alla data della lezione. Stessa grafica in tutti i deck.
- **Sicurezza applicata** non è un modulo: è un filo che attraversa le ore 1, 3, 4, 5, 7, 9,
  10 e 13 (vedi scaletta). Linee guida MIM 2025 e AI Act entrano nelle ore 7 e 9.
- **Fuori programma, per ora:** MCP. Il loop engineering (stadio 4 dei paradigmi) si nomina
  soltanto.
- **Il filo del giudizio quadrimestrale** resta, in via provvisoria: le demo sulla
  `cartella-di-prova/` compaiono nelle ore 1, 3, 4 e 7. Non convince del tutto: se si trovano
  esempi migliori, si sostituiscono.
- **Il perno delle demo non è l'errore di calcolo.** I modelli attuali gestiscono bene assenti,
  virgola decimale e separatori. Le demo si reggono sui due fallimenti che non dipendono dalla
  bravura del modello: **l'ambiguità** (decide al posto vostro ciò che nei dati non c'è, e non
  ve lo dice) e **l'invenzione** (riempie i vuoti quando un'informazione manca).

## Materiali condivisi

| Materiale | Dove | Ore |
|---|---|---|
| Classe inventata: Matematica 3ª B, 21 studenti, fine gennaio 2026 | `cartella-di-prova/` | 1-4, 7-10 |
| Prompt, numeri di controllo, note per chi conduce | `LABORATORIO.md` | tutte |
| Slide del vecchio Modulo 1, da smontare | `slides/modulo-1.html` | 1-3 |
| Profilo disciplinare d'esempio (Italiano e Storia) | `materiali/ora-04-profilo-esempio/` | 4 |
| Wiki navigabile come esempio vivo di knowledge base | `wiki-didattica-scuola/` | 5 |
| Repository barebones per le lezioni interattive | Geode (`C:\Users\mikil\Documents\Repository\geode`) | 11-13 |

## Quadro d'insieme

| Ora | Titolo | Demo e laboratorio | Stato slide |
|---|---|---|---|
| 1 | Dal chatbot all'agente | Chat vs agente dal vivo · giudizio a mani nude · matrice dei casi d'uso | bozza: `slides/ora-01.html` |
| 2 | Orientarsi negli ambienti agentici | Aprire la cartella, fiducia, contatori, Markdown | bozza: `slides/ora-02.html` |
| 3 | Il primo workflow controllato | Brief in quattro righe · piano · modifica di un file | bozza: `slides/ora-03.html` |
| 4 | Context engineering e memoria permanente | Scelta silenziosa · invenzione con e senza `AGENTS.md` · profilo disciplinare | bozza: `slides/ora-04.html` |
| 5 | Knowledge base: file, wiki e RAG | Navigare una LLM wiki · l'agente monta la wiki dal testo di Karpathy | bozza: `slides/ora-05.html` |
| 6 | Usare e comprendere le skill | Skill `teach` · adattare una skill | da fare |
| 7 | Creare skill fondate sulla pedagogia | Griglia a 4 indicatori · skill verifica/rubrica | da fare |
| 8 | Dalla programmazione al calendario | Skill calendario dall'anno scolastico | da fare |
| 9 | Dal registro alle prossime lezioni | PDF fittizio del registro · riallineare il piano | da fare |
| 10 | Più agenti per produrre e controllare | Quattro ruoli su un materiale · il revisore | da fare |
| 11 | Progettare una lezione interattiva | Scheda di progetto prima della tecnica | da fare |
| 12 | Laboratorio su Geode | Lezione interattiva funzionante | da fare |
| 13 | Laboratorio aperto e pubblicazione | Checklist · GitHub Pages | da fare |

---

## Ora 1 — Dal chatbot all'agente

**Fonti wiki:** [[concetti/agente-llm]], [[tecniche/tool-use]], [[concetti/harness-engineering]],
[[concetti/permessi-agente]], [[concetti/verifica-agenti]].

**Da riusare da `modulo-1.html`:** continuità con il corso «Docente 4.0» e i tre nodi rimasti
aperti (slide 2-3); «la stessa domanda, due risposte diverse», chat vs agente in quattro punti,
il loop, «l'agente non agisce: scrive», l'harness (slide 6-10). Obiettivi e mappa (4-5) vanno
riscritti per un'ora sola.

**Da adeguare:** la scaletta usa un ciclo a quattro fasi, *osserva · pianifica · agisce ·
verifica*; le slide attuali ne hanno tre (osserva–pensa–agisci). La quarta fase, la verifica,
serve anche a introdurre la responsabilità umana.

**Da costruire:**
- apertura con raccolta dei casi d'uso dei partecipanti (cartoncini o modulo);
- demo dal vivo della differenza chat/agente sulla stessa richiesta: «quante insufficienze ci
  sono state in 3ªB a gennaio?». Non «nell'ultimo mese»: i voti finiscono a gennaio 2026 e
  la risposta dipenderebbe dalla data del giorno (LABORATORIO § Ora 1);
- strumenti, memoria, autonomia e supervisione: la scala di autonomia come idea, i dettagli
  pratici nelle ore 2-3;
- limiti, allucinazioni e responsabilità: prima comparsa dell'**invenzione**, con il giudizio
  chiesto a mani nude (LABORATORIO § Ora 1);
- chiusura sull'obiettivo dell'ora: una matrice per classificare i casi d'uso raccolti in
  apertura. Assi proposti: *il risultato è verificabile?* · *l'azione è reversibile?* ·
  *ci sono di mezzo dati personali?*

**Laboratorio:** i partecipanti collocano i propri casi d'uso nella matrice (10′). Nessun
account richiesto in quest'ora.

**Materiali da preparare:** modulo per i casi d'uso; matrice stampabile; piano B della demo
(screenshot o registrazione) se la rete non collabora.

**Aperto:** con quale piattaforma fare la demo dal vivo.

## Ora 2 — Orientarsi negli ambienti agentici

**Fonti wiki:** [[framework/claude-code]], [[framework/codex]], [[framework/antigravity]],
[[confronti/claude-code-vs-codex-vs-antigravity]] (attenzione: tutte le fonti di confronto
sono dello stesso autore), [[tecniche/scelta-del-modello]].

**Da riusare da `modulo-1.html`:** il progetto è una cartella, «ti fidi di questa cartella?»,
scegliere il modello, i due contatori (slide 14-16 e 18); l'addendum su Python (slide 21).

**Da rifare:** la slide «I tre nomi che sentirete» (13) diventa la prima *scheda piattaforma*.
Oggi indica `CLAUDE.md` come file-guida di Claude Code e rimanda al «Modulo 4»: va riallineata
ad `AGENTS.md` e alla nuova numerazione. I giudizi «forte su / debole su» vengono da una fonte
sola: tenerli come opinione dichiarata o toglierli.

**Da costruire:**
- sondaggio iniziale su competenze, rapporto con la riga di comando, uso attuale dell'IA;
- panoramica grafica: screenshot aggiornati delle tre interfacce, con le stesse zone indicate
  (conversazione, file, modello, modalità, contatori);
- account, quote gratuite, abbonamenti: una scheda per piattaforma, datata;
- file e cartelle per chi non ci ha mai pensato: percorsi, estensioni (nascoste di default su
  Windows), perché il testo semplice (`.md`, `.csv`) funziona meglio di `.docx` per un agente;
- Markdown essenziale: titoli, elenchi, grassetto, tabelle, link — visti in sorgente e in
  anteprima;
- formazione dei gruppi per piattaforma.

**Laboratorio:** aprire `cartella-di-prova/` nell'ambiente scelto, rispondere alla domanda di
fiducia, farsi descrivere la cartella senza toccare niente, aprire il file-guida che ha letto
da solo, leggere i due contatori (LABORATORIO § Ora 2).

**Materiali da preparare:** sondaggio; screenshot; checklist dei prerequisiti; archivio zip di
`cartella-di-prova/`.

**Aperto:** installare **Git** già qui, insieme a Python, oppure all'ora 11? Serve a Geode e,
per chi vuole, a backup e reversibilità nell'ora 3.

## Ora 3 — Il primo workflow controllato

**Fonti wiki:** [[concetti/prompt-engineering]], [[tecniche/plan-mode]],
[[concetti/permessi-agente]], [[tecniche/versionamento-git-agenti]],
[[concetti/verifica-agenti]], [[tecniche/workflow-progetto-agentico]].

**Da riusare:**
- da `modulo-1.html`: le modalità, da manuale ad autonoma (slide 17); il laboratorio
  (slide 19), esercizi 2 e 3;
- dal vecchio Modulo 2, blocco A: l'anatomia della richiesta. Qui si riduce alle quattro voci
  della scaletta — **obiettivo · contesto · vincoli · criterio di completamento** — che
  diventano il *brief in quattro righe*. Few-shot («ecco un giudizio che ho già scritto io») e
  parole-guida ([[concetti/in-context-learning]], [[tecniche/leading-words]]) sono uscite
  dalle slide e stanno in fondo alla consegna.

**Da costruire:**
- pianificare prima di eseguire: il piano come documento da leggere e correggere;
- osservare le azioni mentre avvengono: cosa guardare nel log dell'agente;
- verificare il risultato contro il criterio di completamento scritto *prima*;
- permessi, backup, reversibilità: copia della cartella prima di lavorare, cosa è
  irreversibile (cancellare, sovrascrivere, inviare, pubblicare), punti di ripristino delle
  piattaforme. Git come rete di sicurezza, nominato ma non insegnato.

**Il nodo dell'ora:** il primo impianto teneva i corsisti in ascolto per una trentina di
minuti prima del laboratorio, faceva la dimostrazione in chat sul giudizio e poi passava
alla modalità piano dentro l'agente senza dichiarare il cambio di ambiente. Deciso
(17/09/2026): **si prova prima e si impara dopo**.

- **Primo tentativo (10 min):** copia di sicurezza, poi «sistema questa scheda» e basta, in
  modalità manuale. I corsisti producono loro il «prima».
- **Raccolta (8 min):** si mettono in fila i guai usciti dai gruppi. Conduzione in
  `demo/ora-03-conduzione-primo-tentativo.md`.
- **Workflow (17 min):** brief, criterio, reti di sicurezza, piano, modalità, lettura delle
  modifiche, verifica. Ogni pezzo risponde a un guaio appena visto.
- **Secondo tentativo (20 min):** stesso compito dalla copia intatta, con tutti e cinque i
  passi, e confronto fra i due risultati.

Il prima/dopo del formatore sul giudizio quadrimestrale **è uscito dalle slide**: il
confronto lo fanno i corsisti sui propri due tentativi. Il prompt resta in
`LABORATORIO.md § Ora 3` per chi conduce. La versione precedente del deck è conservata in
`slides/ora-03-OLD.html`.

**Laboratorio (piccoli gruppi):** in due parti — «sistema questa scheda» → raccolta →
brief scritto → piano → approvazione → esecuzione → verifica e confronto, sulla scheda
`05-materiali/scheda-recupero-equazioni.md` (LABORATORIO § Ora 3).

**Materiali da preparare:** cartoncino «brief in quattro righe».

**Aperto:** il primo tentativo regge solo se l'agente fa davvero qualche danno. Sui modelli
più recenti può chiedere chiarimenti e restare nei refusi: va provato sui tre prodotti prima
della lezione, e la conduzione prevede il ripiego.

## Ora 4 — Context engineering e memoria permanente

**Fonti wiki:** [[concetti/context-engineering]], [[concetti/context-rot]],
[[tecniche/compaction]], [[concetti/memoria-agenti]], [[concetti/harness-engineering]],
[[sintesi/evoluzione-paradigmi-prompting]], [[tecniche/workflow-progetto-agentico]],
[[tecniche/potatura-skill]].

**Da riusare:**
- da `modulo-1.html`: quattro stadi uno dentro l'altro, il contesto come risorsa finita
  (slide 11-12);
- dal vecchio blocco B: cos'è il contesto (richiesta + file letti + conversazione); tre modi di
  darlo (incollare, allegare, far leggere la cartella); context rot, con degrado marcato oltre
  ~200k token; compaction lossy, «una sessione, un compito»; «selezionare *è* il lavoro».
  La **scelta silenziosa** sulla media di Caruso (4,9 · 5,0 · 5,25);
- dal vecchio blocco C: l'**invenzione** sui 21 giudizi, con e senza `AGENTS.md`;
  `AGENTS.md` proiettato riga per riga; la mappa, non il territorio (sotto le ~250 righe,
  dettagli in file separati); portabilità con i rimandi `CLAUDE.md` e `GEMINI.md`; il file non
  si scrive a mano; le regole nascono dalle correzioni; il test di cancellazione;
- dal vecchio Test 5: la nota sul PDP che finisce, o no, nella comunicazione alle famiglie.

**Da costruire:** il **profilo disciplinare del docente**, cioè un file-guida personale a mappa
(materia, classi, stile, convenzioni di valutazione) con i dettagli in file separati. Si crea
facendosi intervistare dall'agente. Nel contesto permanente nessun dato personale di studenti.

**Il nodo dell'ora:** il vecchio Modulo 2 occupava quattro ore; qui ce n'è una. Deciso
(14/09/2026):
- scelta silenziosa, vuoto riempito e comunicazione alle famiglie come tre **demo condotte
  dal formatore**, circa 15 minuti in tutto (copioni in `demo/ora-04-demo-*.md`);
- laboratorio sul **profilo disciplinare**, 20 minuti, in una cartella nuova
  (`consegne/ora-04-lab-profilo.md`);
- «la regola che manca» come esercizio facoltativo da fare a casa, in fondo alla consegna.

**Scheda piattaforma (la terza):** dove ciascuna legge il file-guida, il file-guida per tutte
le cartelle, la memoria automatica. Del vecchio Modulo 4 restano `MEMORY.md`, le lezioni
imparate e `plan.md` come cenno (slide 12).

**Profilo d'esempio:** `materiali/ora-04-profilo-esempio/`, una docente inventata di Italiano
e Storia in un istituto tecnico — `AGENTS.md` a mappa, rimandi `CLAUDE.md` e `GEMINI.md`, tre
file di dettaglio in `profilo/`. Mostrato nella slide 15; si distribuisce come zip su
Classroom per chi non arriva in fondo al laboratorio. La sua `valutazione.md` fissa la media
del quadrimestre: è la risposta alla scelta silenziosa.

**Materiali da preparare:** lo zip `ora-04-profilo-esempio.zip` per Classroom.

## Ora 5 — Knowledge base: file, wiki e RAG

**Fonti wiki:** `wiki-ia-agenti/llm-wiki.md` (l'idea di wiki mantenuta dall'LLM, già
confrontata con NotebookLM), [[concetti/rag]], [[concetti/in-context-learning]],
[[tecniche/artefatti-per-revisione-umana]].

**Da riusare dal vecchio blocco D:** cosa rende un file leggibile da un agente — una riga, un
caso; intestazioni esplicite; valori da un elenco chiuso; convenzioni dichiarate una volta.

**Da costruire:**
- raccolta e selezione delle fonti;
- indice, collegamenti, approfondimento progressivo;
- `wiki-didattica-scuola` come esempio vivo: `index.md` → pagina → fonte, e l'agente che la
  percorre per rispondere;
- file navigabili contro RAG: chi sceglie cosa leggere, cosa si accumula, cosa si perde;
  NotebookLM solo con screenshot;
- qualità delle fonti, citazioni, copyright. Domanda di controllo: una domanda la cui risposta
  *non* è nelle fonti.

**Laboratorio:** il corsista **non decide la struttura**. Consegna all'agente il testo di
Karpathy che descrive il modello e gli dice su quale argomento lavorare; l'agente crea le
cartelle, scrive il file-guida con le convenzioni e le operazioni, e prepara indice e
registro. Poi si ingeriscono tre-cinque fonti proprie e si chiude con la domanda di
controllo. È qui che si vede la potenza dell'agente: una descrizione dettagliata scritta da
qualcun altro basta a montare un sistema intero.

Il testo da consegnare è il gist di Andrej Karpathy, in `wiki-ia-agenti/llm-wiki.md` anche in
copia locale:
`https://gist.githubusercontent.com/karpathy/442a6bf555914893e9891c11519de94f/raw/ac46de1ad27f92b28ac95459c782c07f6b8c964a/llm-wiki.md`
(URL verificato il 19/09/2026; il gist va ricontrollato prima della lezione perché il
riferimento punta a una revisione precisa).

**Materiali — tutti pronti (19/09/2026):**
- `consegne/ora-05-lab-knowledge-base.md`, la consegna per Classroom;
- la sezione «Ora 5» di `LABORATORIO.md`: demo, laboratorio e note di conduzione;
- `slides/img/ora-05-notebooklm.png`, lo screenshot con tre zone numerate nella slide 11;
- `materiali/ora-05-fonti-esempio.zip` per chi arriva senza materiale. Tre documenti
  pubblici (Linee guida MIM sull'IA 2025, Raccomandazione UE competenze chiave 2018,
  Raccomandazione UE EQF 2008) in una cartella `fonti/`, più un `LEGGIMI.md`. Soltanto
  documenti istituzionali, per non distribuire materiale di terzi;
- `materiali/ora-05-llm-wiki/`, il piano B se un prodotto non apre gli URL: copia locale del
  testo di Karpathy e istruzioni per usarlo dalla cartella.

**Aperto:** la licenza del gist di Karpathy. Non ne dichiara una, quindi la copia locale
resta un piano B da passare in aula. Da chiarire prima di caricarla su Classroom.

**Deciso (19/09/2026):** il pacchetto di fonti d'esempio è di **didattica trasversale**
(valutazione, UdA, Linee guida MIM), così serve a qualunque materia. La demo si appoggia a
`wiki-didattica-scuola`: domanda su BICS e CALP, percorso `index.md` → `pagine/bics-e-calp.md`
→ `fonti/2024 CLIL/`.

## Ora 6 — Usare e comprendere le skill

**Fonti wiki:** [[concetti/agent-skills]], [[framework/mattpocock-skills]],
[[framework/superpowers]], [[tecniche/potatura-skill]]; did:scaffolding, did:lev-vygotskij
(zona di sviluppo prossimale).

**Da costruire:**
- istruzione permanente contro skill: sempre caricata contro caricata quando serve;
- anatomia: `SKILL.md` con nome e descrizione, corpo, file di riferimento;
- attivazione: dalla descrizione o su richiesta; confini e criteri di applicazione;
- installare o adattare una skill esistente;
- la skill `teach`: missione, memoria dell'apprendimento, ZPD, recupero attivo, lezioni HTML;
- impieghi con gli studenti: solo come suggestione;
- scheda piattaforma: dove stanno le skill. Geode ne è un esempio pronto: il vero contenuto in
  `.agents/skills/`, i rimandi in `.claude/skills/` — lo stesso schema di `AGENTS.md` e
  `CLAUDE.md`.

**Laboratorio:** installare `teach` chiedendolo all'agente con il link a GitHub; scoprire in
quale cartella è finita; leggerne il sorgente e verificare che non si attivi da sola; usarla
su un argomento personale. L'adattamento alla propria materia è compito a casa facoltativo.
Consegna: `consegne/ora-06-lab-installare-skill.md`. Nessuna demo.

**Materiali da preparare:** fatto — `materiali/ora-06-skill-teach/` (copia locale della
skill con `LICENSE` e `LEGGIMI.md`, più lo zip per Classroom). Serve solo da piano B se
l'agente non arriva in rete. Le skill da smontare in aula sono quelle di Geode, mostrate
nelle slide 8 e 10.

**Aperto:** la skill `teach` non è ancora nella wiki (la pagina `mattpocock-skills` non la
cita): da ingerire. Anche la scheda piattaforma della slide 10 è da ingerire in wiki: i
percorsi delle skill nei tre prodotti non ci sono.

**Chiuso:**
- licenza del repository verificata — MIT, Matt Pocock 2026. La ridistribuzione è
  consentita portandosi dietro la nota di copyright, che è nel pacchetto;
- percorsi delle skill verificati sulla documentazione ufficiale il 19/09/2026. Progetto:
  `.claude/skills/` in Claude Code, `.agents/skills/` sia in Codex sia in Antigravity.
  Globali: `~/.claude/skills/`, `~/.agents/skills/`, `~/.gemini/config/skills/` (in
  Antigravity l'IDE e la CLI hanno percorsi propri, ma `config/` vale per tutte);
- attivazione automatica: si spegne con `disable-model-invocation` in Claude Code e con
  `allow_implicit_invocation: false` in `agents/openai.yaml` per Codex. **In Antigravity non
  si può spegnere**: il frontmatter accetta solo `name` e `description`. La prova del passo
  2 del laboratorio quindi lì si rovescia — previsto nella slide 7 e in `LABORATORIO.md`.

## Ora 7 — Creare skill fondate sulla pedagogia

**Fonti wiki:** did:obiettivo-di-apprendimento, did:tassonomia-di-bloom,
did:progettazione-a-ritroso, did:unita-di-apprendimento-uda, did:rubrica-di-valutazione,
did:livelli-di-padronanza, did:competenza, did:sintesi-uda-a-caccia-di-spot;
[[tecniche/workflow-progetto-agentico]] (l'intervista), [[tecniche/llm-come-giudice]],
[[concetti/verifica-agenti]].

**Da riusare dal vecchio blocco D:**
- «una struttura è un prompt che scrivete una volta sola»;
- la griglia a quattro indicatori contro il voto unico, e la domanda impossibile senza
  struttura (LABORATORIO § Ora 7);
- le strutture che i docenti già usano: rubrica (dimensione → criterio → livello →
  descrittore, livelli A/B/C/D della C.M. 3/2015), piano di lavoro UdA a cinque colonne, verbi
  di Bloom come elenco chiuso;
- l'errore vero trovato in un documento didattico reale: livelli «C. Iniziale – D. Base»
  invertiti.

**Da costruire:**
- l'intervista che rende esplicita una procedura docente;
- coerenza obiettivi → attività → valutazione; descrittori osservabili;
- revisione umana delle decisioni valutative. Qui entrano le Linee guida MIM del 09/08/2025 e
  l'AI Act, che classifica la valutazione degli apprendimenti come uso ad alto rischio.

**Laboratorio:** dall'intervista a una skill che genera verifica e rubrica coerenti con gli
obiettivi dichiarati.

**Materiali da preparare:** ingerire le Linee guida MIM, che stanno in
`wiki-didattica-scuola/fonti/` ma non sono state ingerite; reperire una fonte affidabile
sull'AI Act, oggi assente.

## Ora 8 — Dalla programmazione al calendario delle lezioni

**Fonti wiki:** [[tecniche/plan-mode]], [[tecniche/artefatti-per-revisione-umana]],
[[tecniche/workflow-progetto-agentico]]; did:unita-di-apprendimento-uda,
did:modelli-progettuali.

**Dati:** `cartella-di-prova/02-programmazione/programmazione-annuale.md` (99 ore, unità
U0-U7 con ore previste, tre ore settimanali il lunedì, mercoledì e venerdì).

**Da costruire:**
- prerequisiti, vincoli, festività, ore effettivamente disponibili;
- sequenza delle unità e milestone (verifiche);
- margini di recupero; ipotesi mancanti dichiarate dall'agente e non riempite in silenzio (è
  l'**ambiguità** dell'ora 4 che torna);
- output strutturato e modificabile: una tabella (data · unità · argomento · tipo di ora) più
  una vista HTML per la revisione;
- prima versione della skill `calendario-lezioni`.

**Materiali da preparare:** calendario scolastico 2025/26 fittizio ma plausibile (inizio e
fine lezioni, festività, sospensioni, un'uscita didattica) da aggiungere in
`cartella-di-prova/`; un calendario già pronto per chi non arriva in fondo, che serve all'ora 9.

## Ora 9 — Dal registro alle prossime lezioni

**Fonti wiki:** [[concetti/verifica-agenti]], [[tecniche/artefatti-per-revisione-umana]].

**Dati:** il calendario pianificato dell'ora 8 per l'intero anno; il **PDF fittizio** del
registro, da generare a partire da `02-programmazione/argomenti-svolti.md`. Il diario ha già
gli ingredienti giusti: verifiche spostate di giorno, fasci di rette fatti «per cenni»,
interrogazioni del secondo giro da completare, prova di recupero a metà febbraio.

**Da costruire:**
- dati sintetici e minimizzazione: dal registro vero si esporta solo ciò che serve
  (argomenti), non assenze, note o voti;
- confronto pianificato/svolto: ritardi, anticipi, argomenti incompleti;
- proposta motivata delle lezioni successive, con le incertezze dichiarate;
- l'approvazione resta al docente. Richiamo a MIM e AI Act (vedi ora 7).

**Laboratorio:** secondo passaggio del workflow — una skill che aggiorna il piano.

**Materiali da preparare:** il PDF del registro, con un'impaginazione generica da registro
elettronico, non riconducibile a un fornitore reale.

## Ora 10 — Più agenti per produrre e controllare materiali

**Fonti wiki:** [[tecniche/orchestrazione-multi-agente]], [[concetti/verifica-agenti]],
[[tecniche/llm-come-giudice]], [[concetti/permessi-agente]], [[concetti/loop-engineering]]
(solo nominato).

**Da costruire:**
- quando dividere e quando no;
- i quattro ruoli: ricercatore, progettista didattico, autore, revisore;
- in parallelo o in sequenza; contesto isolato e sintesi del coordinatore;
- fonti discordanti: chi decide;
- costi: più agenti consumano più quota;
- scheda piattaforma: sub-agenti e agenti in parallelo nei tre prodotti, con i nomi alla data.

**Demo candidata:** una scheda di recupero sull'indicatore più debole della verifica 2,
prodotta dai quattro ruoli. Per far lavorare il revisore si può piantare un'incoerenza in
`04-valutazioni/voti-scritti.csv` (vedi Stato delle prove).

## Ora 11 — Progettare una lezione interattiva

**Fonti:** [math-rocks](https://github.com/mporfido/math-rocks) come esempio avanzato; Geode —
`README.md`, `docs/MARKDOWN_SYNTAX.md`, `docs/COMPONENTI.md`, `docs/GRAFICI.md`, il corso
`content/benvenuto/`; did:scaffolding, did:obiettivo-di-apprendimento.

**Da costruire:**
- motore, configurazione e contenuti. In Geode: *engine* (`parser/`, `routes/`, `templates/`,
  `static/components/`) · configurazione (`site.yaml`, `static/theme.css`) · contenuti
  (`content/`, lezioni in Markdown);
- le interazioni disponibili, messe in fila con quelle della scaletta (risposta aperta, scelta
  multipla, slider, contenuti progressivi, grafici, animazioni p5.js);
- prima l'obiettivo pedagogico, poi la soluzione tecnica;
- esempi per area disciplinare (vedi la scaletta, «Esempi interdisciplinari»).

**Laboratorio:** scheda di progetto su carta — obiettivo, sequenza di passi, interazione
scelta, criterio di riuscita — prima di aprire l'agente.

**Materiali da preparare:** scheda di progetto; un esempio per ciascuna area disciplinare.

## Ora 12 — Laboratorio sul repository barebones

**Riferimento:** Geode. Le skill incluse accompagnano tutto il flusso: `inizia`, `nuovo-corso`,
`bozza-lezione`, `app-interattiva`, `nuovo-componente`, `salva`, `pubblica`.

**Da costruire:** scaricare e aprire; leggere istruzioni e skill; generare o adattare i
contenuti; anteprima HTML; correggere dialogando con l'agente; confronto tra piattaforme (scheda
piattaforma).

**Aperto:**
- Geode non è ancora pubblicato su GitHub: va fatto prima dell'ora 12;
- l'onboarding è pensato e testato con Claude Code, che non ha piano gratuito. Va provato su
  Codex e Antigravity;
- prerequisiti: Python e Git; l'account GitHub serve solo per pubblicare;
- per chi non usa Git: download come zip.

## Ora 13 — Laboratorio aperto, revisione e pubblicazione facoltativa

**Da costruire:**
- scelta libera fra lezione interattiva, calendario, knowledge base, verifica, rubrica o
  skill;
- checklist di revisione: correttezza, pedagogia, privacy, copyright, accessibilità;
- dimostrazione della pubblicazione su GitHub Pages con il flusso già pronto in Geode (skill
  `pubblica`, workflow `.github/workflows/pages.yml`);
- conservazione del progetto per il lavoro futuro.

**Materiali da preparare:** la checklist, stampabile.

**Aperto:** la scaletta nomina anche Netlify. Tenerlo come semplice citazione o toglierlo.

---

## Stato delle prove

- ✅ Verificato: sui conti l'agente **non** sbaglia (assenti, virgola decimale, separatori)
- ✅ Verificato: il dataset è coerente ovunque — date, griglie e totali coincidono. Il
  12/09/2026 le date degli orali sono state riallineate al diario: prima cadevano anche di
  sabato, di domenica e durante le vacanze
- ⬜ Da provare: la demo chat/agente sulle insufficienze di gennaio, sulla piattaforma scelta
  per l'ora 1 (numeri giusti: 9 voti, 8 studenti)
- ⬜ **Da provare per forza:** il primo tentativo dell'ora 3 («sistema questa scheda»), nei tre
  prodotti. L'intera ora regge su quello che l'agente combina qui. Che cosa fa della regola di
  consegna e di «x2» → «x²»; se riempie la tabella con le soluzioni; se invece chiede
  chiarimenti e non fa danni. I guai che escono davvero vanno riportati nella colonna destra
  della slide 4 e nella tabella di `demo/ora-03-conduzione-primo-tentativo.md`
- ⬜ Da provare: la divergenza della scelta silenziosa su due sessioni diverse (ora 4)
- ⬜ Da provare: il grado di invenzione sui 21 giudizi, con e senza `AGENTS.md` (ora 4). Con
  la memoria automatica spenta: quella di Claude Code è attiva di default e può portarsi
  dietro qualcosa fra le due sessioni
- ⬜ Da provare: se la nota sul PDP finisce nella comunicazione alle famiglie senza
  `AGENTS.md` (ora 4)
- ⬜ Da ricontrollare la settimana della lezione: la scheda piattaforma dell'ora 4. In
  particolare la memoria automatica di Antigravity: le fonti trovate il 14/09/2026 non sono
  concordi
- ⬜ Da decidere: se piantare un'incoerenza in `voti-scritti.csv` per il revisore (ora 10)
- ⬜ **Da provare per forza:** il prompt del laboratorio dell'ora 5 nei tre prodotti. Il
  laboratorio regge sul fatto che l'agente sappia **aprire un URL**: va verificato se Codex,
  Claude Code e Antigravity lo fanno con le impostazioni predefinite dei piani gratuiti, e
  che cosa chiedono all'utente prima di farlo. Se uno dei tre non ci arriva, serve il testo
  di Karpathy anche come file da scaricare da Classroom
- ⬜ Da provare: quanto divergono fra loro le strutture che i tre prodotti generano dallo
  stesso testo (ora 5). Se divergono molto, è un buon momento per parlarne in aula
- ⬜ Da provare: l'onboarding di Geode su Codex e Antigravity (ora 12)
- ✅ Fatto: gli screenshot delle tre app (12/09/2026) in `slides/img/`, slide 6-8 dell'ora 2.
  Da rifare se cambia l'interfaccia
- ⬜ Da ricontrollare la settimana della lezione: le due schede piattaforma dell'ora 2 (fonti di
  luglio–agosto 2026). In particolare, dove si legge il consumo in Claude Code
- ⬜ Da preparare: calendario scolastico e PDF fittizio del registro (ore 8-9)
- ⬜ Da ingerire: skill `teach`, Linee guida MIM, una fonte sull'AI Act (ore 6, 7, 9)

I prompt esatti, i numeri di controllo e le note per chi conduce stanno in `LABORATORIO.md`.
