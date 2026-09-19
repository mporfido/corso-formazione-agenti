# Laboratorio — prompt e note per chi conduce

Prompt esatti, numeri di controllo e note di conduzione, divisi per ora secondo la
[scaletta](scaletta-corso-13-ore.md). Quasi tutto lavora sulla `cartella-di-prova/`: una 3ª B
di matematica a fine gennaio 2026, 21 studenti, tutto inventato.

Una premessa che vale per tutto il laboratorio: **non stiamo cercando errori di
calcolo.** I modelli recenti i conti li fanno bene. Quello che continuano a fare
è **decidere al posto vostro senza dirvelo**, e **riempire i vuoti** quando
un'informazione non c'è. È lì che guardiamo.

> Questo foglio sta **fuori** dalla cartella di prova, apposta: se stesse dentro,
> l'agente ci leggerebbe le risposte invece di ricavarle.

> I dati della cartella sono inventati. Non inserite lì dati veri della vostra
> classe.

Due cartelle affiancano questo foglio, e le slide di demo e laboratorio ci
rimandano dal piè di pagina:

- `consegne/`: una consegna per laboratorio, **per i corsisti**, da caricare su
  Classroom. Niente numeri di controllo e niente trappole svelate: quelli
  restano qui.
- `demo/`: il copione di ogni dimostrazione, **per chi conduce**. Contiene
  prompt, passi, cosa deve succedere e il piano B.

| Ora | Prove |
|---|---|
| 1 | La stessa domanda a chat e agente · A mani nude: l'invenzione |
| 2 | Fatti guardare intorno · Cambia motore |
| 3 | Il brief in quattro righe · Il primo workflow completo |
| 4 | La scelta silenziosa · Il vuoto riempito · Trenta secondi · Il profilo disciplinare · La regola che manca (facoltativa) |
| 5 | Navigare una wiki vera · La wiki costruita da una descrizione |
| 7 | Con i dati strutturati |
| 6, 8-13 | da scrivere |

---

## Ora 1 — Dal chatbot all'agente

### La stessa domanda a chat e agente

Demo condotta dal formatore. La stessa domanda, prima in una chat senza file,
poi all'agente aperto sulla `cartella-di-prova/`:

```
Quante insufficienze ci sono state in 3ªB a gennaio?
```

**Cosa guardare.** La chat non ha i dati e rimanda il lavoro a voi. L'agente
cerca da solo dove stanno i voti, apre scritti e orali, filtra gennaio e conta.
Fate contare ai presenti i passi che compie prima di rispondere.

**I numeri giusti.** A gennaio ci sono la verifica 3 (22/01) e le
interrogazioni del secondo giro.

- Verifica 3: **7 insufficienze** — Bianchi 5,5 · Caruso 5,0 · Esposito 4,5 ·
  Fontana 5,5 · Greco 4,5 · Parisi 5,0 · Villa 5,0. Marchetti era assente
  (`ASS`): non è un'insufficienza.
- Orali di gennaio: **2 insufficienze** — Conti 5,5 · Esposito 4,5.
- In tutto **9 voti insufficienti**, ma **8 studenti**: Esposito compare due volte.

Se l'agente risponde «8» o «9» senza dire quale dei due ha contato, avete
un'anteprima gratuita della scelta silenziosa dell'ora 4: basta chiedergli
«voti o studenti?».

### A mani nude: l'invenzione

Da fare **in chat** (ChatGPT, Claude, Gemini), non nella cartella. Se lo fate
nell'agente, aggiungete «non guardare i file». Nell'ora 1 la conduce il
formatore: ai partecipanti non serve ancora un account.

```
Devo scrivere il giudizio del primo quadrimestre di matematica per uno
studente di terza liceo che ha una media del 6 e mezzo. Scrivimelo.
```

**Cosa guardare.** Esce un giudizio che va bene per chiunque, e contiene cose
che non avete mai detto: «ha mostrato crescente interesse», «partecipa
attivamente». Nessuno gliele ha dette — le ha inventate. Quando non sa, riempie.
Tenetelo a mente: torna nell'ora 4, con la cartella davanti.

La versione costruita bene della stessa richiesta si fa nell'ora 3.

---

## Ora 2 — Orientarsi negli ambienti agentici

### Fatti guardare intorno

Aprite la `cartella-di-prova/` con l'agente. Prima di rispondere alla domanda
di fiducia, aprite voi `AGENTS.md` e leggetelo: è il gesto da ripetere con ogni
cartella che non avete scritto voi. Poi:

```
Dimmi cosa c'è in questa cartella e a cosa serve. Non modificare niente.
```

**Cosa guardare.** Quali passi compie, e in che ordine: di solito apre prima il
file-guida e il `README.md`, poi scende nelle sottocartelle. Poi aprite voi
`AGENTS.md`: l'ha letto da solo, senza che nessuno glielo indicasse.

Aprite anche il `README.md` in due modi — in anteprima e come testo semplice —
per vedere che cosa sono davvero `#`, `**` e le tabelle in Markdown.

A fine prova guardate i due contatori: quanto contesto ha già occupato una
domanda così semplice, e quanto vi resta del piano.

### Cambia motore

La stessa domanda prima con il modello leggero, poi con l'intermedio, in due
sessioni nuove:

```
Chi non ha ancora un voto orale nel secondo giro? Fammi una lista da
recuperare a febbraio.
```

**Cosa guardare.** Su un compito così semplice, di solito la differenza nel
risultato non c'è; quella nel consumo sì. È la ragione pratica per non usare
sempre il modello di punta.

---

## Ora 3 — Il primo workflow controllato

L'ora si apre al computer: i corsisti fanno il compito **due volte**, prima chiedendolo
male e poi con il workflow completo. Non c'è demo del formatore; la conduzione del primo
tentativo e della raccolta sta in `demo/ora-03-conduzione-primo-tentativo.md`.

### Primo tentativo — a mani nude

Prima di tutto la **copia** di `05-materiali/scheda-recupero-equazioni.md`: è il punto di
ritorno, e serve davvero, perché il secondo tentativo riparte da lì.

Poi, in modalità manuale, una riga sola, identica per tutti i gruppi:

```
Sistema questa scheda.
```

**Cosa guardare.** Che cosa cambia oltre ai refusi; se tocca esercizi e risultati; che
fine fa la regola di consegna; se riempie la tabella con le soluzioni; come chiude.

### La raccolta

Parlano prima i gruppi, poi si scopre l'elenco. La frase che chiude: nessuno di questi è
un errore dell'agente, sono decisioni che gli sono state lasciate prendere. Da qui in poi
ogni pezzo del workflow risponde a un guaio già visto, e conviene nominarlo.

### Secondo tentativo — il workflow completo

Si rimette la scheda com'era dalla copia. Il brief si scrive *prima* di parlare con
l'agente:

```
Obiettivo: sistemare 05-materiali/scheda-recupero-equazioni.md.
Contesto: è una scheda per la 3ª B; è piena di refusi e c'è una tabella rotta.
Vincoli: non cambiare esercizi, risultati e regole di consegna; solo forma e refusi.
Completamento: nessun refuso, la tabella si vede bene in anteprima, e mi
elenchi ogni modifica fatta.
```

Poi, in **modalità piano**: farsi proporre il piano, leggerlo, correggerlo se serve, e
solo allora approvare. Durante l'esecuzione si guarda la richiesta di conferma prima
della scrittura: è il freno di cui si parla nelle slide.

**La verifica è loro.** Confrontare con la copia: le modifiche elencate sono davvero
tutte quelle fatte? Il criterio di completamento è rispettato punto per punto? E infine
il confronto fra i due tentativi: quale riga del brief ha evitato quale guaio.

**Ruoli nel gruppo:** chi guida l'agente, chi legge le modifiche ad alta voce, chi
annota (senza toccare la tastiera), chi verifica.

**Le trappole della scheda** — da guardare nella verifica finale:

- la regola «chi non la consegna non viene ammesso alla prova di recupero» non
  è un refuso: se l'agente la ammorbidisce o la toglie, ha violato il vincolo;
- «x2» che diventa «x²», «delta» che diventa «Δ»: forma o contenuto? Nel primo tentativo
  lo decide l'agente. È una scelta silenziosa in piccolo, e anticipa l'ora 4;
- la tabella dell'esercizio 2 ha l'intestazione a tre colonne e la riga di
  separazione a due: dopo la correzione deve vedersi in anteprima con tre
  colonne vuote da riempire, non con le soluzioni già scritte.

### Il giudizio dell'ora 1, chiesto bene

Non sta più nelle slide, ma resta un buon esempio da tenere in tasca se serve una seconda
illustrazione del brief:

```
Sei un docente di matematica di liceo. Scrivi il giudizio quadrimestrale
di uno studente in 3 frasi, per il consiglio di classe.
Vincoli: parla solo di risultati nelle prove, non di atteggiamento o
partecipazione; niente aggettivi entusiastici; se un dato non te l'ho
dato, non inventarlo — scrivi [dato mancante].
Dati: tre scritti 6,0 - 5,5 - 5,5; due orali 7,0 e 6,0.
```

Ricondotto alle quattro voci: **obiettivo** (il giudizio, per il consiglio di classe) ·
**contesto** (i dati) · **vincoli** (solo risultati, niente invenzioni) · **criterio di
completamento** (tre frasi, `[dato mancante]` dove serve).

### Facoltativo: fatti intervistare

Sempre in modalità piano:

```
Devo scrivere i giudizi del quadrimestre. Prima di partire, intervistami
per capire cosa mi serve.
```

Confrontate le domande che vi fa con quelle che vi sareste fatti voi.

---

## Ora 4 — Context engineering e memoria permanente

Le prime tre prove sono **demo condotte dal formatore** (copioni:
`demo/ora-04-demo-scelta-silenziosa.md`, `demo/ora-04-demo-vuoto-riempito.md`,
`demo/ora-04-demo-comunicazione-famiglie.md`): il laboratorio dei partecipanti è
il profilo disciplinare (`consegne/ora-04-lab-profilo.md`). Se il gruppo è
piccolo e il tempo c'è, le prove si possono far rifare a coppie.

Se il prodotto ha una **memoria automatica** (Claude Code ce l'ha attiva di
default), spegnetela o svuotatela prima delle demo: fra una sessione e l'altra
non deve portarsi dietro niente.

### Prima di cominciare

Rinominate il file-guida: le prossime due prove devono girare senza.

```
cd cartella-di-prova
ren AGENTS.md AGENTS.md.off
```

(su Mac o Linux: `mv AGENTS.md AGENTS.md.off`)

### La scelta silenziosa

```
Guarda la cartella. Fammi una tabella con la media del primo quadrimestre
di ogni studente.
```

Prima di tutto verificate che sui conti sia affidabile: gli assenti sono
segnati `ASS` e non vanno contati come zero. Le risposte giuste sono
**Marchetti 4,5**, **Esposito 4,5**, **Sanna 6,25** di media negli scritti. Quasi
sempre le azzecca.

**Il punto della prova è un altro.** Nessuno ha mai detto all'agente:

- se gli orali pesano quanto gli scritti, o meno;
- se si fa la media di tutti i voti messi insieme, o la media degli scritti e
  quella degli orali poi mediate fra loro;
- che cosa fare di chi ha tre scritti e una sola interrogazione;
- se Sanna, arrivato a novembre da un'altra scuola senza aver mai fatto le
  equazioni, vada valutato sulle tre prove o sulle due che ha potuto svolgere.

Ha deciso lui. E non ve l'ha detto.

**Guardate Caruso Matteo** (tre scritti: 4,5 – 4,0 – 5,0; una sola
interrogazione: 6,0). A seconda della scelta esce:

| Come si calcola | Media |
|---|---|
| Media di tutti e quattro i voti | **4,9** |
| Scritti e orali pesati uguale | **5,25** |
| Scritti due terzi, orali un terzo | **5,0** |

Tre numeri diversi, tre letture tutte difendibili. Ma la prima è
un'insufficienza netta e la seconda è un caso da discutere in consiglio.

Due cose da fare adesso:

```
Come hai deciso di calcolare la media? Quali alternative avevi?
```

Di solito a questo punto le elenca tutte — sapeva benissimo che erano possibili,
semplicemente ne ha scelta una e ha tirato dritto.

Poi, **la prova che conta**: fate rifare la stessa identica domanda a un collega
accanto a voi, in una sessione nuova. Confrontate le due tabelle. Se sono
diverse, avete appena visto il vero problema — e nessuna delle due è sbagliata.

### Il vuoto riempito

Restiamo senza `AGENTS.md` ancora per un momento.

```
Scrivimi il giudizio del primo quadrimestre per tutti e 21 gli studenti,
tre righe ciascuno.
```

**Cosa guardare.** Ventuno giudizi da rendere diversi l'uno dall'altro: per
riuscirci il modello attinge a quello che non ha. Cercate frasi come «si impegna
con costanza», «partecipa attivamente», «ha mostrato progressi nell'ultimo
periodo», «atteggiamento collaborativo». Poi scegliete uno studente qualsiasi —
Villa Jacopo va benissimo — e chiedete:

```
«Si impegna con costanza» su Villa: da quale file l'hai preso?
```

Non c'è. Di Villa la cartella contiene tre voti scritti, i punteggi delle tre
griglie e un'interrogazione con una riga di commento sulle conoscenze, niente
altro. Sull'impegno e sulla partecipazione dei singoli studenti la cartella non
dice **una parola**: le sole annotazioni individuali riguardano Fontana,
Marchetti e Sanna, in `01-classe/note-classe.md`, e nessuna parla di impegno.

Ora rimettete il file al suo posto e **aprite una sessione nuova**. È
importante: quella di prima ha già in memoria le frasi inventate.

```
ren AGENTS.md.off AGENTS.md
```

E ridate **lo stesso identico prompt**, senza aggiungere niente.

**Cosa cambia.** I giudizi restano attaccati ai dati, vi dicono da quale prova
viene ogni numero, e dove manca un'informazione ve lo segnalano invece di
coprirla. Non gliel'avete detto voi: l'ha letto da solo aprendo la cartella.

Aprite `cartella-di-prova/AGENTS.md` e cercate le righe che hanno fatto la
differenza — sono tre, sotto «Come scrivere». Tre righe scritte una volta sola,
che valgono per tutte le sessioni future.

```
Cosa hai letto in questa cartella prima di rispondermi?
```

### Trenta secondi, e apre una discussione

```
Prepara una comunicazione per le famiglie della classe sugli esiti del
primo quadrimestre.
```

Nell'elenco studenti c'è una nota su un piano didattico personalizzato.
Guardate se finisce nel testo. Con `AGENTS.md` attivo non dovrebbe — c'è una
regola apposta. Senza, può succedere.

Qui il dato è finto. Nella vostra cartella vera no. È anche il ponte verso il
profilo disciplinare: nel contesto permanente **non** entrano dati personali
degli studenti.

### Il profilo disciplinare

Il laboratorio dell'ora. In una cartella nuova e vuota — non nella cartella di
prova — fatevi intervistare:

```
Voglio creare il mio profilo di docente: un AGENTS.md che rileggerai ogni
volta che lavoriamo in questa cartella. Intervistami una domanda alla
volta su materia, classi, stile dei materiali e convenzioni di
valutazione. Poi proponimi il file: breve, a mappa, con i dettagli lunghi
in file separati che richiami solo quando servono. Non inserire nomi o
dati di studenti.
```

**Cosa controllare nel risultato.** Sta sotto le ~250 righe? Rimanda a file
separati invece di contenere tutto? C'è qualche riga che, cancellata, non
cambierebbe niente? Allora era un *no-op*: via.

### Facoltativo: la regola che manca

Il `AGENTS.md` della cartella di prova dice come trattare gli assenti e come
scrivere, ma **non dice niente su come si calcola la media del quadrimestre**. È
esattamente il buco trovato nella scelta silenziosa.

Scrivetela voi. Aggiungete ad `AGENTS.md`, sotto «Come muoverti qui dentro», due
o tre righe che fissino la vostra scelta — per esempio:

```markdown
- La media del quadrimestre si calcola come media fra la media degli scritti
  e la media degli orali, con peso uguale. Chi ha una sola interrogazione
  fa media con quella. Riporta sempre le due medie separate accanto a quella
  complessiva.
```

Poi sessione nuova, e di nuovo la domanda della scelta silenziosa. Confrontate
con il collega: adesso le due tabelle devono coincidere.

È questo il mestiere. Il file-guida non serve a rendere l'agente più
intelligente: serve a far sì che la decisione la prendiate voi, una volta, e che
resti presa.

---

## Ora 5 — Knowledge base: file, wiki e RAG

L'ora ha **una demo condotta dal formatore** (navigare una wiki vera) e **un
laboratorio dei partecipanti** (`consegne/ora-05-lab-knowledge-base.md`). È
l'unica ora che non lavora sulla cartella di prova: la demo gira su
`wiki-didattica-scuola`, il laboratorio su una cartella nuova di ciascuno.

Il perno dell'ora non è più l'invenzione: è **la potenza di una descrizione**.
Nel laboratorio nessuno decide come si fa una knowledge base. Si consegna
all'agente il testo di Karpathy che la descrive, e l'agente monta l'impianto.
L'invenzione torna solo alla fine, nella domanda di controllo.

### Navigare una wiki vera

Serve una copia di `C:\Users\mikil\Progetti\wiki-didattica-scuola` sulla
macchina che proietta: 40 pagine in `pagine/`, 4 fonti in `fonti/`, un
`index.md` e un `CLAUDE.md` che fa da schema. Apritela con l'agente **prima**
della lezione: il primo avvio è lento e non deve vedersi.

```
Devo spiegare a un collega la differenza fra BICS e CALP e perché conta
quando si valuta in CLIL. Rispondimi in dieci righe e dimmi da quali pagine
e da quali fonti hai preso ogni cosa.
```

**Cosa deve succedere.** L'agente apre `index.md` per primo, e da lì sceglie.
Le pagine che toccano l'argomento sono sette, ma quelle che serve aprire sono
due o tre: quasi sempre `pagine/bics-e-calp.md`, spesso anche
`pagine/jim-cummins.md` e `pagine/valutazione-in-clil.md`. Le altre trentotto
non le guarda.

Fermatevi su questo numero: **tre pagine aperte su quaranta**. Il lavoro di
selezione lo ha fatto l'indice, e l'indice lo ha scritto l'agente quando sono
state aggiunte le fonti.

Poi aprite davvero uno dei file citati e controllate con la classe che ci sia
scritto quello che l'agente riporta. `pagine/bics-e-calp.md` dichiara le sue
fonti in testa: sono due PDF dentro `fonti/2024 CLIL/`. Il percorso completo
indice → pagina → fonte si vede tutto lì.

Chiudete chiedendo di archiviare la risposta:

```
Questa risposta mi servirà ancora. Archiviala come pagina nuova della wiki,
con le convenzioni che usi di solito, e aggiorna l'indice.
```

**Il punto.** La wiki cresce anche con le domande, non soltanto con le fonti.

Se avanza tempo, la domanda di controllo funziona anche qui: **la valutazione
formativa e il debate non sono in questa wiki** (verificato il 19/09/2026).
Chiedete «che cosa dicono le mie fonti sulla valutazione formativa?» e guardate
se ammette il buco o se risponde a braccio.

### Il laboratorio — la wiki costruita da una descrizione

Cartella nuova e vuota, con dentro tre-cinque fonti proprie. Il prompt è questo:

```
Leggi questo testo:
https://gist.githubusercontent.com/karpathy/442a6bf555914893e9891c11519de94f/raw/ac46de1ad27f92b28ac95459c782c07f6b8c964a/llm-wiki.md

Descrive un modo di costruire una knowledge base mantenuta da un agente.
Seguendo quelle linee guida, prepara in questa cartella la mia wiki su
[argomento]. Crea le cartelle, scrivi il file-guida con le convenzioni e le
operazioni, e crea l'indice e il registro. Poi spiegami in poche righe le
scelte che hai fatto.
```

Poi l'ingest delle proprie fonti, una alla volta:

```
Ingerisci le fonti che ho messo nella cartella, una alla volta. Per ognuna
fermati e dimmi che cosa hai scritto, prima di passare alla successiva.
```

E la chiusura, con una domanda vera e poi la domanda di controllo su un
argomento che il corsista sa non essere nelle sue fonti.

**Cosa controllare nel risultato.** Il file-guida deve descrivere le tre
operazioni (ingest, query, lint) e la regola che vieta di toccare le fonti. Ogni
pagina deve citare la fonte da cui viene. L'indice deve elencarle tutte. Alla
domanda di controllo l'agente deve ammettere il buco.

**Le strutture generate saranno diverse fra loro**, e va bene così: cartelle con
nomi diversi, campi diversi in testa alle pagine, file-guida più o meno lunghi.
Se in aula qualcuno se ne accorge, è il momento buono per dirlo: il testo di
Karpathy descrive un modello, non detta un formato.

### Note di conduzione dell'ora 5

- **La cosa che può far saltare il laboratorio è l'accesso a internet.** Il
  prompt funziona solo se l'agente sa aprire un URL. Da verificare nei tre
  prodotti prima della lezione, con le impostazioni predefinite dei piani
  gratuiti, e da sapere che cosa chiedono all'utente prima di farlo. Il piano B
  è pronto in `materiali/ora-05-llm-wiki/`: si passa il file al corsista, lui lo
  mette nella cartella e cambia la prima riga del prompt in «leggi il file
  `llm-wiki.md` che trovi in questa cartella». Il `LEGGIMI.md` lì dentro segnala
  anche la questione della licenza, da chiarire prima di caricarlo su Classroom.
- **Chi arriva senza fonti proprie** usa `materiali/ora-05-fonti-esempio.zip`.
  Dentro c'è una cartella `fonti/` con tre documenti pubblici — Linee guida MIM
  sull'IA (2025), Raccomandazione UE sulle competenze chiave (2018),
  Raccomandazione UE sull'EQF (2008) — più un `LEGGIMI.md` con l'argomento
  suggerito per la wiki e una domanda di controllo pronta. Il pacchetto contiene
  soltanto documenti istituzionali, per non distribuire materiale di terzi.
  Averlo già su Classroom evita di perdere cinque minuti all'inizio.
- **La domanda di controllo per chi usa il pacchetto** è il *debate*: in quei
  tre documenti non compare. Se qualcuno usa fonti proprie, aiutatelo a
  scegliere un argomento davvero assente, perché la prova regge su quello.
- Nel passo 2 molti vorranno andare avanti senza leggere il file-guida che
  l'agente ha scritto. Fermateli: leggerlo e correggerlo è il laboratorio, il
  resto è esecuzione.
- **Attenzione ai PDF fatti di scansioni.** Qualcuno arriverà con materiale
  scansionato, che l'agente non legge come testo. Se succede, fate mettere da
  parte quel file e andate avanti con gli altri: è un buon esempio da nominare,
  senza fermarsi a risolverlo.
- Le fonti dei corsisti sono materiale loro e possono essere coperte da
  copyright. Restano sui loro computer e non si caricano da nessuna parte.
- Nella wiki della demo non ci sono dati di studenti, ed è bene dirlo: la
  knowledge base raccoglie fonti e metodo, il registro sta altrove.

---

## Ora 6 — Usare e comprendere le skill

L'ora **non ha demo**: è teoria e un unico laboratorio dei partecipanti
(`consegne/ora-06-lab-installare-skill.md`). Non si lavora sulla cartella di
prova: ognuno apre una cartella nuova, perché la skill costruisce lì dentro il
proprio spazio di lavoro.

Il perno dell'ora è che **una skill è un file di testo che si può aprire e
leggere**. Tre momenti, in quest'ordine: la installo senza sapere com'è fatta,
scopro dove è finita, la leggo e capisco perché si comporta come si comporta.
L'adattamento alla propria materia non si fa in aula: è il compito facoltativo
di chiusura, e diventa lavoro vero nell'ora 7.

### Il laboratorio — installare, trovare, leggere, usare

Cartella nuova e vuota, aperta con l'agente. Tre passi.

**Passo 1 — l'installazione (4 minuti).**

```
Installa come skill di questo progetto quella che trovi qui:
https://github.com/mattpocock/skills/tree/main/skills/productivity/teach
Scarica SKILL.md e tutti i file che stanno nella stessa cartella. Poi
dimmi in quale cartella li hai messi e perché proprio lì.
```

**Numeri di controllo.** I file da scaricare sono **sei**: `SKILL.md` (1.488
parole) e quattro file di formato — `MISSION-FORMAT.md`,
`LEARNING-RECORD-FORMAT.md`, `RESOURCES-FORMAT.md`, `GLOSSARY-FORMAT.md` — più
`agents/openai.yaml`, che legge solo Codex e che contiene
`allow_implicit_invocation: false` (torna utile al passo 2). Se l'agente ne
scarica uno solo, fateglieli chiedere di nuovo: i quattro file di formato sono
proprio il «materiale di riferimento» della slide 5, e senza quelli la lezione
dopo non si vede.

**Destinazioni attese** (documentazione ufficiale, verificata il 19/09/2026):

| | skill del progetto | skill globali |
|---|---|---|
| Claude Code | `.claude/skills/teach/` | `~/.claude/skills/` |
| Codex | `.agents/skills/teach/` | `~/.agents/skills/` |
| Antigravity | `.agents/skills/teach/` | `~/.gemini/config/skills/` |

Codex e Antigravity leggono **la stessa cartella** `.agents/skills/`: è il punto
della slide 10 e lo stesso schema di `AGENTS.md`. Per le globali di Antigravity
i percorsi ufficiali cambiano fra IDE (`~/.gemini/antigravity/skills/`) e CLI
(`~/.gemini/antigravity-cli/skills/`); `~/.gemini/config/skills/` è l'unico che
funziona con tutte le versioni, ed è quello che vale la pena dire in aula.

Se qualcuno si ritrova un percorso diverso da questi, non correggetelo: fate
confrontare. La domanda «dove l'ha messa e perché» vale più della risposta.

**Passo 2 — leggere il sorgente e la prova del trabocchetto (6 minuti).**

Si apre `SKILL.md` con un editor di testo (o si chiede all'agente di mostrarne
le prime venti righe) e si guarda il frontmatter. La riga che conta è
`disable-model-invocation: true`.

Poi la prova, da scrivere **senza nominare la skill**:

```
Vorrei imparare a usare bene i fogli di calcolo.
```

**Cosa deve succedere: non deve succedere niente.** L'agente risponde come
risponderebbe sempre, senza aprire `MISSION.md` e senza creare cartelle. È la
dimostrazione, sul loro schermo, della differenza fra le due filosofie di
attivazione della slide 7.

> **Attenzione: in Antigravity la prova va al contrario.** Il frontmatter di
> Antigravity accetta soltanto `name` e `description`, e non esiste alcun campo
> per impedire l'attivazione automatica: decide sempre l'agente. `teach` lì
> dentro **può partire da sola**. Chi lavora in Claude Code trova la chiave
> `disable-model-invocation`, chi lavora in Codex trova
> `allow_implicit_invocation: false` dentro `agents/openai.yaml`, e la skill sta
> ferma.
>
> Non è un incidente, è il regalo migliore dell'ora: la stessa identica cartella
> si comporta in due modi diversi, e la differenza sta in una riga di un file di
> testo. Se in aula succede, chiedete ai due gruppi di confrontare gli schermi.
> La slide 7 lo dice già in fondo, così non vi coglie di sorpresa.

Poi si invoca per davvero. In Claude Code basta `/teach`; negli altri, «usa la
skill teach».

**Passo 3 — usarla sul proprio argomento (10 minuti).**

```
Usa la skill teach. Voglio imparare [argomento].
Scrivi in italiano: MISSION.md, le lezioni e le schede di riferimento
devono essere tutte in italiano.
Prima di scrivere la prima lezione fammi le domande che ti servono per
capire perché mi serve.
```

**Cosa deve succedere.** L'agente fa domande prima di insegnare — è
`MISSION.md` che glielo impone. Poi cerca fonti, scrive `MISSION.md`, e produce
una prima lezione in `lessons/0001-*.html` che prova ad aprire nel browser.

Insistete sul fatto che **l'argomento deve essere personale**, non didattico.
Chi sceglie «come si insegna la matematica» ottiene una lezione tiepida; chi
sceglie «come si legge un bilancio», «l'uncinetto», «la fotografia in manuale»
vede la skill lavorare sul serio, perché la missione è vera.

**Cosa controllare nel risultato.** Nella cartella devono esserci `MISSION.md`
e almeno un file dentro `lessons/`. La lezione deve essere corta, con un
esercizio o una domanda, e con almeno un link a una fonte esterna. Se è un
muro di testo senza esercizio e senza citazioni, l'agente sta ignorando la
skill: fatelo notare, è informazione utile quanto il successo.

### Note di conduzione dell'ora 6

- **L'accesso a internet è il punto fragile, come nell'ora 5.** Qui serve due
  volte: per scaricare la skill e perché la skill stessa cerca fonti. Il piano B
  è pronto in `materiali/ora-06-skill-teach/`: si distribuisce la cartella
  `teach/` e il prompt del passo 1 diventa «installa come skill di questo
  progetto la cartella `teach` che trovi qui». Va verificato nei tre prodotti
  prima della lezione, con le impostazioni predefinite dei piani gratuiti.
- **La licenza è a posto.** `mattpocock/skills` è pubblicato con licenza MIT
  (Matt Pocock, 2026): si può copiare, modificare e ridistribuire portandosi
  dietro la nota di copyright. Nel pacchetto su Classroom il file `LICENSE` c'è
  già, e la slide 13 dice perché ci si guarda. La questione lasciata aperta in
  `Struttura.md` si può chiudere.
- **La skill è in inglese e i corsisti scrivono in italiano.** Funziona, e la
  risposta arriva in italiano. Quello che resta inglese sono i *nomi dei file*
  che la skill impone (`MISSION.md`, `learning-records/`, `lessons/`) e, ogni
  tanto, un titolo dentro la lezione HTML. La riga sulla lingua nel prompt del
  passo 3 serve a questo. Se qualcuno se ne lamenta, è l'aggancio perfetto per
  il compito a casa: aprire il file e tradurlo è già potatura.
- **Qualcuno chiederà di installarla per tutti i progetti invece che per uno.**
  Va benissimo ed è anzi il caso d'uso vero di `teach`, ma in aula fate fare
  l'installazione locale: si trova più facilmente e non lascia strascichi sulle
  loro macchine.
- **Il numero 1.488 parole di `SKILL.md` stona con «le skill vanno tenute
  piccole».** È voluto e va detto: `teach` è un metodo di insegnamento intero,
  non una singola operazione, e infatti i suoi quattro file di formato stanno
  fuori dal corpo. Il termine di paragone sono le skill del progetto delle ore
  11-13, fra 270 e 850 parole (`salva` è la più corta).
- **Il collegamento con la didattica va nominato esplicitamente** (slide 12):
  zona di sviluppo prossimale e scaffolding sono in
  `wiki-didattica-scuola/pagine/`, e in aula ci sarà chi li ha studiati. È il
  ponte verso l'ora 7: una skill è didattica messa per iscritto.
- **Sugli studenti (slide 15) non si apre la discussione**, o si mangia il
  laboratorio. Si nominano le quattro questioni aperte e si rimanda alle ore 7 e
  9. Se qualcuno insiste, la risposta è: provatelo su voi stessi per un mese,
  poi ne riparliamo.
- L'argomento che ciascuno sceglie è roba sua e resta sul suo computer. Non c'è
  niente da caricare da nessuna parte, e nessun dato di studenti entra in gioco
  in quest'ora.

---

## Ora 7 — Creare skill fondate sulla pedagogia

### Con i dati strutturati

Una domanda impossibile se aveste solo il voto finale:

```
Nella verifica 2, su quale dei quattro indicatori la classe ha perso più
punti? Dimmi anche come hai fatto il conto.
```

I numeri veri, da `03-verifiche/griglia-verifica-02.csv`:

| Indicatore | Punti presi / massimo | % |
|---|---|---|
| Linguaggio e ordine | 23,5 / 40 | **58,8 %** |
| Calcolo | 36,5 / 60 | 60,8 % |
| Procedura | 37 / 60 | 61,7 % |
| Comprensione | 25 / 40 | 62,5 % |

**Di nuovo la scelta silenziosa**, e qui la vedete a occhio nudo. In percentuale
il più debole è *linguaggio*. In punti persi in assoluto è *calcolo* (23,5 punti
buttati contro 16,5). Due risposte diverse, tutte e due difendibili — come nella
media di Caruso, ma stavolta potete controllare, perché la griglia c'è.

È il motivo per cui conviene conservare i quattro indicatori e non solo il voto
finale: non rende l'agente più bravo, rende **voi** in grado di verificarlo.

Poi l'uso vero, quello per cui siete qui:

```
Prepara una scheda di recupero di 6 esercizi mirata sull'indicatore più
debole della verifica 2. Scrivila seguendo lo stile e la struttura di
05-materiali/scheda-ripasso-retta.md
```

L'ultima riga è un esempio dato con un file invece che incollato nel prompt.

*Da scrivere:* l'intervista che porta dalla procedura del docente a una skill
per verifiche e rubriche.

---

## Ore 8-13

*Da scrivere.*

- **Ora 8** — dalla programmazione annuale e dal calendario scolastico alla
  prima versione della skill `calendario-lezioni`.
- **Ora 9** — dal PDF fittizio del registro al piano aggiornato. Il diario
  `02-programmazione/argomenti-svolti.md` contiene già verifiche spostate, fasci
  di rette fatti «per cenni» e interrogazioni da completare.
- **Ora 10** — la scheda di recupero dell'ora 7 prodotta da quattro ruoli, con
  un revisore che deve trovare un'incoerenza.
- **Ore 11-13** — su Geode.

---

## Altre richieste che funzionano bene su questi dati

- «Chi ha valutazioni insufficienti in entrambe le prove scritte più recenti?»
- «Chi non ha ancora un voto orale nel secondo giro? Fammi una lista da
  recuperare a febbraio.» (usata nell'ora 2)
- «Quali argomenti sono stati svolti prima della seconda verifica?»
- «Sistema `05-materiali/scheda-recupero-equazioni.md`: è pieno di refusi e
  c'è una tabella rotta.» (usata nell'ora 3)

---

## Per chi conduce il laboratorio

- **Il vecchio perno non funziona più.** I modelli attuali gestiscono
  correttamente `ASS`, la virgola decimale e il punto e virgola: provato con
  Sonnet. Per questo il laboratorio è costruito sull'ambiguità e
  sull'invenzione, non sull'errore di calcolo — sono fallimenti che non
  dipendono da quanto è bravo il modello.
- La scelta silenziosa (ora 4) rende al massimo con **due postazioni
  affiancate**. Se il gruppo è piccolo, fate girare la stessa domanda due volte
  di seguito in sessioni nuove: la divergenza si vede lo stesso, ma è meno
  teatrale.
- Nel vuoto riempito (ora 4) il grado di invenzione **varia**: chiedete tutti e
  21 i giudizi, non uno solo. È la richiesta di variare a spingere il modello a
  inventare. Se proprio resta prudente, aggiungete «scrivili in modo che si
  distinguano bene l'uno dall'altro».
- Fra una prova e l'altra la sessione va chiusa davvero, non solo svuotata: è
  anche l'occasione per far vedere il contatore del contesto.
- Dopo l'ora 4 controllate che `AGENTS.md` sia tornato al suo nome: le ore
  successive lo danno per presente.
- Il dataset **è coerente ovunque**: date, griglie e totali coincidono, e le
  medie tornano. Se volete mostrare anche l'agente-revisore (ora 10), cambiate a
  mano un voto in `04-valutazioni/voti-scritti.csv` prima della lezione: senza
  file-guida lo riporta con sicurezza, con il file-guida lo segnala (c'è la
  regola che indica le griglie come fonte vera).
- Il `README.md` dentro la cartella è stato alleggerito apposta: non contiene
  più gli esercizi né anticipazioni sul PDP.
