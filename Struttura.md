# Struttura del corso — quaderno di regia

**Nome:** Dalla IA generativa alla IA agentica

**Pubblico:** docenti di scuola superiore, non tecnici

**Durata:** 10 ore, organizzate in 10 lezioni autonome da un'ora (pause comprese). Le lezioni 1-3
formano il primo incontro, in presenza; le altre si aggregano quando ci sarà il calendario.

**Programma di riferimento:** [scaletta-corso-10-ore.md](scaletta-corso-10-ore.md). Lì c'è il
*cosa* — argomenti e obiettivo di ogni ora — e non si modifica da qui. Questo file raccoglie
il *come*: fonti, materiale da riusare, demo, laboratori, materiali da preparare, questioni
aperte.

**Convenzione per i riferimenti:** `[[concetti/…]]`, `[[tecniche/…]]` ecc. sono pagine di
`wiki-ia-agenti/wiki/`; `did:nome-pagina` sono pagine di `wiki-didattica-scuola/pagine/`.

## Scelte di impianto

- **Un deck per lezione**: `slides/lezione-01.html` … `lezione-10.html`, stile Manuale. Gli argomenti della
  scaletta sono i punti chiave delle slide.
- **Agnostico rispetto al prodotto**: si impara l'impalcatura, non lo strumento. Il file-guida
  canonico è `AGENTS.md`; `CLAUDE.md` e `GEMINI.md` sono solo rimandi. Molti docenti partono
  dai piani gratuiti (Codex, Antigravity); Claude Code richiede un abbonamento.
- **Il confronto tra piattaforme** non è un modulo: compare nelle lezioni 2, 4, 6 e 12 come
  *scheda piattaforma* a quattro righe — concetto stabile · nome nel prodotto · piano gratuito
  o a pagamento · stato alla data della lezione. Stessa grafica in tutti i deck.
- **Sicurezza applicata** non è un modulo: è un filo che attraversa le lezioni 1, 3, 4, 5, 7,
  8, 9 e 10 (vedi scaletta). Linee guida MIM 2025 e AI Act entrano nella lezione 7.
- **Fuori programma, per ora:** MCP. Il loop engineering (stadio 4 dei paradigmi) si nomina
  soltanto.
- **Il filo del giudizio quadrimestrale** resta, in via provvisoria: le demo sulla
  `cartella-di-prova/` compaiono nelle lezioni 1, 3, 4 e 7. Non convince del tutto: se si trovano
  esempi migliori, si sostituiscono.
- **Il perno delle demo non è l'errore di calcolo.** I modelli attuali gestiscono bene assenti,
  virgola decimale e separatori. Le demo si reggono sui due fallimenti che non dipendono dalla
  bravura del modello: **l'ambiguità** (decide al posto vostro ciò che nei dati non c'è, e non
  ve lo dice) e **l'invenzione** (riempie i vuoti quando un'informazione manca).

## Materiali condivisi

| Materiale | Dove | Lezioni |
|---|---|---|
| Classe inventata: Matematica 3ª B, 21 studenti, fine gennaio 2026 | `cartella-di-prova/` | 1-4, 7 |
| Prompt, numeri di controllo, note per chi conduce | `LABORATORIO.md` | tutte |
| Profilo disciplinare d'esempio (Italiano e Storia) | `materiali/lezione-04-profilo-esempio/` | 4 |
| Wiki navigabile come esempio vivo di knowledge base | `wiki-didattica-scuola/` | 5 |
| Repository barebones per le lezioni interattive | Geode (`C:\Users\mikil\Documents\Repository\geode`, <https://github.com/mporfido/geode>) | 8-10 |

## Quadro d'insieme

| Lezione | Titolo | Demo e laboratorio | Stato slide |
|---|---|---|---|
| 1 | Dal chatbot all'agente | Chat vs agente dal vivo · giudizio a mani nude · matrice dei casi d'uso | bozza: `slides/lezione-01.html` |
| 2 | Orientarsi negli ambienti agentici | Aprire la cartella, fiducia, contatori, Markdown | bozza: `slides/lezione-02.html` |
| 3 | Il primo workflow controllato | Brief in quattro righe · piano · modifica di un file | bozza: `slides/lezione-03.html` |
| 4 | Context engineering e memoria permanente | Scelta silenziosa · invenzione con e senza `AGENTS.md` · profilo disciplinare | bozza: `slides/lezione-04.html` |
| 5 | Knowledge base: file, wiki e RAG | Navigare una LLM wiki · l'agente monta la wiki dal testo di Karpathy | bozza: `slides/lezione-05.html` |
| 6 | Usare e comprendere le skill | Skill `teach` · adattare una skill | bozza: `slides/lezione-06.html` |
| 7 | Creare skill fondate sulla pedagogia | Griglia a 4 indicatori · skill verifica/rubrica | bozza: `slides/lezione-07.html` |
| 8 | Come funziona math-rocks | Demo: lezione e Markdown affiancati · scheda di progetto · prerequisiti a casa | bozza: `slides/lezione-08.html` |
| 9 | Creare la propria istanza di Geode | Messaggio di avvio · onboarding `inizia` · prima lezione in anteprima | da fare |
| 10 | Personalizzare e pubblicare | Checklist · GitHub Pages (facoltativa) | da fare |

---

## Lezione 1 — Dal chatbot all'agente

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
  la risposta dipenderebbe dalla data del giorno (LABORATORIO § Lezione 1);
- strumenti, memoria, autonomia e supervisione: la scala di autonomia come idea, i dettagli
  pratici nelle lezioni 2-3;
- limiti, allucinazioni e responsabilità: prima comparsa dell'**invenzione**, con il giudizio
  chiesto a mani nude (LABORATORIO § Lezione 1);
- chiusura sull'obiettivo dell'ora: una matrice per classificare i casi d'uso raccolti in
  apertura. Assi proposti: *il risultato è verificabile?* · *l'azione è reversibile?* ·
  *ci sono di mezzo dati personali?*

**Laboratorio:** i partecipanti collocano i propri casi d'uso nella matrice (10′). Nessun
account richiesto in quest'ora.

**Materiali da preparare:** modulo per i casi d'uso; matrice stampabile; piano B della demo
(screenshot o registrazione) se la rete non collabora.

**Aperto:** con quale piattaforma fare la demo dal vivo.

## Lezione 2 — Orientarsi negli ambienti agentici

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
da solo, leggere i due contatori (LABORATORIO § Lezione 2).

**Materiali da preparare:** sondaggio; screenshot; checklist dei prerequisiti; archivio zip di
`cartella-di-prova/`.

**Aperto:** installare **Git** già qui, insieme a Python, oppure alla lezione 8? Serve a Geode e,
per chi vuole, a backup e reversibilità nella lezione 3.

## Lezione 3 — Il primo workflow controllato

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
  `demo/lezione-03-conduzione-primo-tentativo.md`.
- **Workflow (17 min):** brief, criterio, reti di sicurezza, piano, modalità, lettura delle
  modifiche, verifica. Ogni pezzo risponde a un guaio appena visto.
- **Secondo tentativo (20 min):** stesso compito dalla copia intatta, con tutti e cinque i
  passi, e confronto fra i due risultati.

Il prima/dopo del formatore sul giudizio quadrimestrale **è uscito dalle slide**: il
confronto lo fanno i corsisti sui propri due tentativi. Il prompt resta in
`LABORATORIO.md § Lezione 3` per chi conduce. La versione precedente del deck è conservata in
`slides/lezione-03-OLD.html`.

**Laboratorio (piccoli gruppi):** in due parti — «sistema questa scheda» → raccolta →
brief scritto → piano → approvazione → esecuzione → verifica e confronto, sulla scheda
`05-materiali/scheda-recupero-equazioni.md` (LABORATORIO § Lezione 3).

**Materiali da preparare:** cartoncino «brief in quattro righe».

**Aperto:** il primo tentativo regge solo se l'agente fa davvero qualche danno. Sui modelli
più recenti può chiedere chiarimenti e restare nei refusi: va provato sui tre prodotti prima
della lezione, e la conduzione prevede il ripiego.

## Lezione 4 — Context engineering e memoria permanente

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
  dal formatore**, circa 15 minuti in tutto (copioni in `demo/lezione-04-demo-*.md`);
- laboratorio sul **profilo disciplinare**, 20 minuti, in una cartella nuova
  (`consegne/lezione-04-lab-profilo.md`);
- «la regola che manca» come esercizio facoltativo da fare a casa, in fondo alla consegna.

**Scheda piattaforma (la terza):** dove ciascuna legge il file-guida, il file-guida per tutte
le cartelle, la memoria automatica. Del vecchio Modulo 4 restano `MEMORY.md`, le lezioni
imparate e `plan.md` come cenno (slide 12).

**Profilo d'esempio:** `materiali/lezione-04-profilo-esempio/`, una docente inventata di Italiano
e Storia in un istituto tecnico — `AGENTS.md` a mappa, rimandi `CLAUDE.md` e `GEMINI.md`, tre
file di dettaglio in `profilo/`. Mostrato nella slide 15; si distribuisce come zip su
Classroom per chi non arriva in fondo al laboratorio. La sua `valutazione.md` fissa la media
del quadrimestre: è la risposta alla scelta silenziosa.

**Materiali da preparare:** lo zip `lezione-04-profilo-esempio.zip` per Classroom.

## Lezione 5 — Knowledge base: file, wiki e RAG

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
- `consegne/lezione-05-lab-knowledge-base.md`, la consegna per Classroom;
- la sezione «Lezione 5» di `LABORATORIO.md`: demo, laboratorio e note di conduzione;
- `slides/img/lezione-05-notebooklm.png`, lo screenshot con tre zone numerate nella slide 11;
- `materiali/lezione-05-fonti-esempio.zip` per chi arriva senza materiale. Tre documenti
  pubblici (Linee guida MIM sull'IA 2025, Raccomandazione UE competenze chiave 2018,
  Raccomandazione UE EQF 2008) in una cartella `fonti/`, più un `LEGGIMI.md`. Soltanto
  documenti istituzionali, per non distribuire materiale di terzi;
- `materiali/lezione-05-llm-wiki/`, il piano B se un prodotto non apre gli URL: copia locale del
  testo di Karpathy e istruzioni per usarlo dalla cartella.

**Aperto:** la licenza del gist di Karpathy. Non ne dichiara una, quindi la copia locale
resta un piano B da passare in aula. Da chiarire prima di caricarla su Classroom.

**Deciso (19/09/2026):** il pacchetto di fonti d'esempio è di **didattica trasversale**
(valutazione, UdA, Linee guida MIM), così serve a qualunque materia. La demo si appoggia a
`wiki-didattica-scuola`: domanda su BICS e CALP, percorso `index.md` → `pagine/bics-e-calp.md`
→ `fonti/2024 CLIL/`.

## Lezione 6 — Usare e comprendere le skill

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
Consegna: `consegne/lezione-06-lab-installare-skill.md`. Nessuna demo.

**Materiali da preparare:** fatto — `materiali/lezione-06-skill-teach/` (copia locale della
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

## Lezione 7 — Creare skill fondate sulla pedagogia

**Fonti wiki:** did:obiettivo-di-apprendimento, did:tassonomia-di-bloom,
did:progettazione-a-ritroso, did:unita-di-apprendimento-uda, did:rubrica-di-valutazione,
did:livelli-di-padronanza, did:competenza, did:sintesi-uda-a-caccia-di-spot;
[[tecniche/workflow-progetto-agentico]], [[tecniche/llm-come-giudice]],
[[concetti/verifica-agenti]].

**Da riusare dal vecchio blocco D:**
- «una struttura è un prompt che scrivete una volta sola»;
- la griglia a quattro indicatori contro il voto unico, e la domanda impossibile senza
  struttura (LABORATORIO § Lezione 7);
- le strutture che i docenti già usano: rubrica (dimensione → criterio → livello →
  descrittore, livelli A/B/C/D della C.M. 3/2015), piano di lavoro UdA a cinque colonne, verbi
  di Bloom come elenco chiuso;
- l'errore vero trovato in un documento didattico reale: livelli «C. Iniziale – D. Base»
  invertiti.

**Da costruire:**
- la procedura fatta fare passo passo all'agente, corretta, e distillata in skill solo dopo
  che ha funzionato (sostituisce l'intervista, 29/09/2026). Il caso vero della slide 7 è
  una conversazione dell'autore nel progetto `Progetti/Scuola` («Progettazione matematica
  primo biennio»): obiettivi di Bloom per bimestre, verifica dalla griglia di dipartimento,
  scaletta delle lezioni. Le correzioni del docente sono le regole della skill.
  Le slide 12-14 (rubrica, descrittori, coerenza) usano la griglia vera di quel caso
  (`Progetti/Scuola/Programmazioni/ProgrammazioneDidDisc_PRIME_Tec_26-27.docx`, allegato:
  quattro indicatori da 2,5, livelli 1-4) e la Parte A di
  `Verifica_PrimoBimestre_Matematica_PRIME.docx`, non la cartella di prova;
- coerenza obiettivi → attività → valutazione; descrittori osservabili;
- revisione umana delle decisioni valutative. Qui entrano le Linee guida MIM del 09/08/2025 e
  l'AI Act, che classifica la valutazione degli apprendimenti come uso ad alto rischio.

**Laboratorio:** dalla programmazione di dipartimento del corsista (portata da casa,
annunciato alla fine della lezione 6) a obiettivi, tabella di specificazione e verifica di
un'unità; poi la skill `verifica-a-ritroso` distillata dalla conversazione e provata in
una sessione nuova su un'altra unità. Consegna: `consegne/lezione-07-lab-skill-verifica.md`.

**Demo:** `demo/lezione-07-demo-btc-task.md` (slide 5) — la skill
[btc-task](https://github.com/mporfido/skills/tree/main/teaching/btc-task) dell'autore del
corso, esempio di skill fondata su un metodo (*Building Thinking Classrooms*);
`demo/lezione-07-demo-dalla-procedura-alla-skill.md` (slide 8) — il ciclo fare, correggere,
distillare, riprovare sulla U2 della 3ª B;
`demo/lezione-07-demo-indicatore-debole.md` (slide 15) — la scelta silenziosa sulla griglia
della verifica 2.

**Deck:** `slides/lezione-07.html`, 19 slide. Le Linee guida MIM sono citate dal testo firmato
(`wiki-didattica-scuola/fonti/`), non ancora ingerite in wiki. Per l'AI Act il deck riporta
solo Allegato III e considerando 56, come li cita il MIM; il calendario degli obblighi per
l'alto rischio è segnato da ricontrollare.

**Materiali da preparare:** ingerire le Linee guida MIM, che stanno in
`wiki-didattica-scuola/fonti/` ma non sono state ingerite; reperire una fonte affidabile
sull'AI Act, oggi assente.

## Lezione 8 — Come funziona math-rocks

**Fonti:** [math-rocks](https://github.com/mporfido/math-rocks) come esempio avanzato; Geode
(`C:\Users\mikil\Documents\Repository\geode`, pubblicato su
<https://github.com/mporfido/geode>) — `README.md`, `docs/README.md` (indice della sintassi),
`docs/struttura.md`, `docs/markdown-base.md`, `docs/blocchi.md`, `docs/COMPONENTI.md`,
`docs/grafici.md`, `docs/p5.md`, i corsi dimostrativi `content/benvenuto/` e `content/esempi/`;
did:scaffolding, did:obiettivo-di-apprendimento.

**Da costruire:**
- che cosa vede lo studente: una lezione di math-rocks aperta nel browser, accanto al suo
  Markdown (stessa cosa, due viste);
- motore, configurazione e contenuti. In Geode: *engine* (`parser/`, `routes/`, `templates/`,
  `static/components/`, `build_courses.py`, `freeze.py`, `tests/`) · configurazione
  (`site.yaml`, `static/theme.css`, temi in `static/themes/`) · contenuti (`content/`, lezioni
  in Markdown, `static/sketches/`). La regola: il motore non si tocca;
- le interazioni disponibili: domande aperte, scelta multipla, menu a tendina, slider,
  contenuti che si rivelano a obiettivi completati, formule, grafici, animazioni p5.js;
- dal testo al sito: anteprima in locale, compilazione in JSON, congelamento in HTML statico,
  pubblicazione su Pages. Privacy: i progressi stanno nel browser dello studente; i servizi
  esterni che vedono l'IP sono GitHub, jsDelivr e cdnjs (elenco nel README di Geode);
- **mini-parte Python, Git, GitHub (15 minuti al massimo)**, solo il necessario:
  - Python: serve a far girare il motore; l'agente crea l'ambiente (`venv`) e installa le
    dipendenze; che cosa guardare se «Python non è stato trovato» (alias del Microsoft Store);
  - Git: repository, salvataggio come fotografia (commit) e ritorno indietro; richiama la
    lezione 3 (backup e reversibilità);
  - GitHub: Git sta sul computer, GitHub è il sito che ospita la copia online; serve solo per
    pubblicare, non per iniziare a lavorare;
- prima l'obiettivo pedagogico, poi la soluzione tecnica; esempi per area disciplinare
  (vedi la scaletta, «Esempi interdisciplinari»).

**Demo:** aprire una lezione di math-rocks e il suo file Markdown; poi il corso `esempi` di
Geode, costrutto per costrutto. Copione in `demo/lezione-08-demo-math-rocks.md`.

**Laboratorio:** scheda di progetto su carta — obiettivo, sequenza di passi, interazione
scelta, criterio di riuscita — prima di aprire l'agente. Consegna:
`consegne/lezione-08-lab-scheda-progetto.md`.

**Prerequisiti, da far installare a casa prima della lezione:** Python 3.12, Git, e
l'assistente scelto (Codex, Antigravity o Claude Desktop). Consegna:
`consegne/lezione-08-prerequisiti.md`, con la guida per Windows e per Mac e due comandi di
verifica (`python --version`, `git --version`). Fonte: `docs/SETUP.md` di Geode.
- Windows: Python da python.org con la spunta **Add python.exe to PATH**; Git for Windows con
  l'opzione «Git from the command line and also from 3rd-party software». In alternativa
  `winget install Python.Python.3.12 Git.Git`.
- Mac: Python da python.org (pacchetto universal2); Git con i Command Line Tools. Da provare:
  la guida di Geode passa dal portale Apple (serve un account), ma di solito basta lanciare
  `git --version` o `xcode-select --install` da Terminale.
- L'account GitHub non serve prima della lezione 10; `gh` si installa lì.
- GitHub Desktop **non** sostituisce Git: lo porta con sé ma non lo mette nel PATH, e non
  include `gh`; l'agente da terminale non lo vedrebbe.

**Deck:** `slides/lezione-08.html`, 17 slide. La scheda di progetto e la consegna dei prerequisiti sono scritte.
**Da preparare:** un esempio di scheda per ciascuna area disciplinare; prova del copione della demo con la copia locale di math-rocks.

## Lezione 9 — Creare la propria istanza di Geode

**Riferimento:** Geode. Le skill sono in `.agents/skills/` (le copie in `.claude/skills/` sono
rimandi): `inizia`, `nuovo-corso`, `bozza-lezione`, `app-interattiva`, `nuovo-componente`,
`salva`, `pubblica`, `aggiorna`.

**Da costruire:**
- partire da una cartella vuota e incollare il messaggio di avvio del README di Geode: l'agente
  prepara una copia indipendente, con storia nuova e senza collegamenti per pubblicare nel
  progetto originale;
- il modo in cui l'agente lavora, letto dal vivo: `README.md`, `AGENTS.md`, `inizia/SKILL.md`;
- l'onboarding della skill `inizia`, in quattro fasi: ambiente (Python, `venv`, dipendenze,
  `git init` e nome/email per firmare i salvataggi), modulo con nome sito, materia e
  destinatari, veste grafica scelta su un'anteprima comparativa (temi `quaderno`, `salvia`,
  `sobrio`), prima anteprima nel browser e corso di benvenuto;
- la prima lezione della propria disciplina a partire dalla scheda di progetto (skill
  `nuovo-corso` e `bozza-lezione`), controllo dell'interattività, correzione dialogando;
- salvataggio del lavoro (skill `salva`);
- confronto tra piattaforme: onboarding con Claude Desktop (Pro o Max), con Codex e con
  Antigravity, questi ultimi con il prompt di adattamento in `docs/SETUP.md`. Scheda
  piattaforma.

**Laboratorio:** `consegne/lezione-09-lab-istanza-geode.md`, da scrivere. Parte dal messaggio
di avvio e arriva a una lezione visibile in anteprima.

**Aperto:**
- l'onboarding è pensato e testato con Claude Code, che non ha piano gratuito. Va provato su
  Codex e Antigravity prima della lezione;
- l'installazione delle dipendenze (`pip`) richiede rete: verificare con la rete della scuola;
- chi resta indietro con Python o Git: tenere un computer di riserva già pronto, o far
  guardare a coppie;
- `storage_prefix` si decide in questa lezione e non si cambia più a sito pubblicato: dirlo.

## Lezione 10 — Personalizzare e pubblicare

**Da costruire:**
- personalizzazione di aspetto, testi e contenuti; prosecuzione libera (nuove lezioni, propri
  documenti come fonte, componenti);
- checklist di revisione: correttezza, pedagogia, privacy, copyright, accessibilità;
- pubblicazione su GitHub Pages con il flusso già pronto in Geode (skill `pubblica`, workflow
  `.github/workflows/pages.yml`): installazione di `gh`, accesso dal browser con
  `gh auth login -s workflow` (senza il permesso `workflow` GitHub rifiuta il push), scelta
  dei corsi dimostrativi da togliere, nome del sito, creazione del repository pubblico e
  push. Il sito è **pubblico**: GitHub Pages gratuito non ha siti privati. Chi non vuole
  pubblicare resta in locale: la pubblicazione è facoltativa;
- aggiornamenti successivi: «aggiorna il sito» e skill `aggiorna` per il motore;
- conservazione del progetto per il lavoro futuro; chiusura del corso.

**Deck:** `slides/lezione-10.html`, 17 slide; la checklist stampabile è la slide 8. Consegna:
`consegne/lezione-10-lab-pubblicazione.md`. Demo: `demo/lezione-10-demo-pubblicazione.md`.
**Da preparare:** un account GitHub di servizio e un sito di prova per la demo; prova del flusso
`pubblica` sulla rete della scuola.

**Aperto:**
- account GitHub: farlo creare a casa prima della lezione, o in aula;
- rete della scuola: Pages e `gh` devono poter uscire;
- la scaletta non cita più Netlify: tenerlo fuori.


---

## Stato delle prove

- ✅ Verificato: sui conti l'agente **non** sbaglia (assenti, virgola decimale, separatori)
- ✅ Verificato: il dataset è coerente ovunque — date, griglie e totali coincidono. Il
  12/09/2026 le date degli orali sono state riallineate al diario: prima cadevano anche di
  sabato, di domenica e durante le vacanze
- ⬜ Da provare: la demo chat/agente sulle insufficienze di gennaio, sulla piattaforma scelta
  per la lezione 1 (numeri giusti: 9 voti, 8 studenti)
- ⬜ **Da provare per forza:** il primo tentativo della lezione 3 («sistema questa scheda»), nei tre
  prodotti. L'intera ora regge su quello che l'agente combina qui. Che cosa fa della regola di
  consegna e di «x2» → «x²»; se riempie la tabella con le soluzioni; se invece chiede
  chiarimenti e non fa danni. I guai che escono davvero vanno riportati nella colonna destra
  della slide 4 e nella tabella di `demo/lezione-03-conduzione-primo-tentativo.md`
- ⬜ Da provare: la divergenza della scelta silenziosa su due sessioni diverse (lezione 4)
- ⬜ Da provare: il grado di invenzione sui 21 giudizi, con e senza `AGENTS.md` (lezione 4). Con
  la memoria automatica spenta: quella di Claude Code è attiva di default e può portarsi
  dietro qualcosa fra le due sessioni
- ⬜ Da provare: se la nota sul PDP finisce nella comunicazione alle famiglie senza
  `AGENTS.md` (lezione 4)
- ⬜ Da ricontrollare la settimana della lezione: la scheda piattaforma della lezione 4. In
  particolare la memoria automatica di Antigravity: le fonti trovate il 14/09/2026 non sono
  concordi
- ⬜ **Da provare per forza:** il prompt del laboratorio della lezione 5 nei tre prodotti. Il
  laboratorio regge sul fatto che l'agente sappia **aprire un URL**: va verificato se Codex,
  Claude Code e Antigravity lo fanno con le impostazioni predefinite dei piani gratuiti, e
  che cosa chiedono all'utente prima di farlo. Se uno dei tre non ci arriva, serve il testo
  di Karpathy anche come file da scaricare da Classroom
- ⬜ Da provare: quanto divergono fra loro le strutture che i tre prodotti generano dallo
  stesso testo (lezione 5). Se divergono molto, è un buon momento per parlarne in aula
- ⬜ Da provare: l'onboarding di Geode su Codex e Antigravity (lezione 9)
- ✅ Fatto: gli screenshot delle tre app (12/09/2026) in `slides/img/`, slide 6-8 della lezione 2.
  Da rifare se cambia l'interfaccia
- ⬜ Da ricontrollare la settimana della lezione: le due schede piattaforma della lezione 2 (fonti di
  luglio–agosto 2026). In particolare, dove si legge il consumo in Claude Code
- ⬜ Da ingerire: skill `teach`, Linee guida MIM, una fonte sull'AI Act (lezioni 6 e 7)

I prompt esatti, i numeri di controllo e le note per chi conduce stanno in `LABORATORIO.md`.
