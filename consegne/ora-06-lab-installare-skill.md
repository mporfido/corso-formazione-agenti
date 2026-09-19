# Ora 6 · Laboratorio — Installare una skill e capire come è fatta

> Al computer · da soli · 20 minuti · si crea una cartella nuova · serve un argomento che
> volete imparare voi

## Cosa facciamo e perché

Installate una skill scritta da qualcun altro, senza sapere in anticipo com'è fatta. Poi
andate a cercare dove è finita, la aprite e la leggete.

Sembra poco, ed è invece il passaggio che cambia il rapporto con questi strumenti. Una skill
non è un componente misterioso che si scarica e funziona: è un file di testo con dentro
delle istruzioni scritte in italiano — in questo caso in inglese — che potete leggere,
giudicare e correggere. Chi lo ha fatto una volta smette di avere soggezione.

La skill si chiama `teach` e serve a farsi insegnare qualcosa. Nell'ultima parte la mettete
al lavoro su di voi.

## Prima di cominciare

Pensate a **una cosa che vorreste imparare voi**. Non per la classe: per voi.

Uno strumento che non padroneggiate, un argomento di una materia che non insegnate, un
mestiere che vi incuriosisce. «Come si legge il bilancio di una società», «la fotografia in
manuale», «l'uncinetto», «le basi del diritto del lavoro». Funziona meglio se è vera:
questa skill, prima di insegnare, vi chiede perché vi interessa, e a una ragione inventata
si vede che risponde male.

## Passi

### 1 · L'installazione · 4 minuti

Create una cartella nuova e vuota, per esempio `imparare`, in un posto che ritroverete.
Apritela con l'agente.

Incollate questa richiesta così com'è:

```
Installa come skill di questo progetto quella che trovi qui:
https://github.com/mattpocock/skills/tree/main/skills/productivity/teach
Scarica SKILL.md e tutti i file che stanno nella stessa cartella. Poi
dimmi in quale cartella li hai messi e perché proprio lì.
```

Se l'agente vi chiede il permesso di aprire un indirizzo internet, dateglielo.

**Annotatevi la risposta alla seconda domanda: in quale cartella li ha messi.** Vi serve fra
un minuto, e vi servirà fra un mese quando vorrete ritrovare la skill.

I file scaricati devono essere **sei**: `SKILL.md`, quattro file il cui nome finisce per
`-FORMAT.md` e un `openai.yaml` dentro una sottocartella. Se ne ha scaricato uno solo,
ditegli di prendere anche gli altri.

### 2 · Leggere il sorgente · 6 minuti

Andate nella cartella che vi ha detto e **aprite `SKILL.md` con un editor di testo**. Se non
sapete come fare, chiedete all'agente: «mostrami le prime venti righe di SKILL.md».

In cima, fra due righe di trattini, c'è la scheda che l'agente legge per sapere se questa
skill lo riguarda. Cercate questa riga:

```
disable-model-invocation: true
```

Vuol dire: *questa skill non si attiva mai da sola*. Adesso verificatelo. Scrivete
all'agente una richiesta che somiglia molto a quello che la skill fa, **senza nominarla**:

```
Vorrei imparare a usare bene i fogli di calcolo.
```

Non deve succedere niente di speciale. L'agente vi risponde come vi risponderebbe sempre:
non crea nessuna cartella, non vi fa domande sul perché. Questa è la prova, sul vostro
schermo, che l'attivazione di una skill non è magia: è una riga di configurazione, e sta
scritta in un file che avete appena aperto.

**Se invece la skill parte lo stesso, non avete sbagliato niente.** Vuol dire che il vostro
strumento quella riga non la legge. In Antigravity, per esempio, non esiste proprio: le
skill lì si attivano sempre e solo in base alla descrizione, e non c'è modo di impedirlo.
Chi lavora in Codex trova la stessa istruzione scritta altrove, dentro
`agents/openai.yaml`, con il nome `allow_implicit_invocation: false`. Confrontatevi con chi
vi sta vicino: se usate strumenti diversi vedrete la stessa cartella comportarsi in due
modi, e la differenza sta tutta in una riga di testo.

### 3 · Usarla davvero · 10 minuti

Adesso chiamatela per nome. Incollate questo, con il vostro argomento al posto della
parentesi quadra:

```
Usa la skill teach. Voglio imparare [argomento].
Scrivi in italiano: MISSION.md, le lezioni e le schede di riferimento
devono essere tutte in italiano.
Prima di scrivere la prima lezione fammi le domande che ti servono per
capire perché mi serve.
```

**La skill è scritta in inglese, ma voi le scrivete in italiano e lei vi risponde in
italiano.** La riga in mezzo serve perché anche i documenti che produce siano in italiano:
senza, qualche titolo resta inglese.

Rispondete alle domande che vi fa. Sono domande sullo scopo, non sull'argomento: perché vi
serve, che cosa volete riuscire a fare. Può sembrare una perdita di tempo, ma è scritto
dentro la skill che deve farle prima di insegnare qualunque cosa, e la ragione è buona:
senza uno scopo vero le lezioni vengono astratte.

Quando ha finito, guardate che cosa è comparso nella cartella: `MISSION.md` con il vostro
scopo, e una lezione dentro `lessons/`. La lezione è una pagina web: apritela.

## Da controllare alla fine

- **Sapete dire in che cartella è finita la skill?** Se non ve lo ricordate, richiedeteglielo
  adesso.
- **Avete trovato la riga che le impedisce di partire da sola?** E avete visto che
  effettivamente non parte?
- **La cartella contiene `MISSION.md`?** Leggetelo: è il vostro scopo, scritto dall'agente
  a partire da quello che gli avete detto.
- **La lezione si apre ed è corta?** Deve starci in pochi minuti, avere un esercizio o una
  domanda, e almeno un link a una fonte esterna. Se è un muro di testo senza esercizio,
  l'agente sta ignorando la skill: è un risultato interessante anche questo, segnatevelo.

## Se non arrivate in fondo

Fermatevi al passo 2. Aver installato una skill e averne letto il sorgente è la parte che
conta di quest'ora; usarla potete farlo con calma a casa, quando avete mezz'ora vera.

## A casa, facoltativo · Adattarla

Aprite `SKILL.md` e chiedete all'agente:

```
Riscrivi questa skill in italiano e adattala alla mia materia, che è
[materia]. Togli tutto quello che non mi riguarda. Prima di riscriverla
dimmi che cosa hai intenzione di togliere e perché.
```

La parte interessante è la risposta alla seconda domanda. Quello che decide di togliere è la
*potatura* di cui si è parlato a lezione: vedere quali paragrafi considera inutili per voi
dice molto su che cosa quei paragrafi stessero facendo.

Tenete da parte l'originale prima di modificarlo. È pubblicato con licenza MIT, quindi
copiarlo e riscriverlo è pienamente consentito: basta lasciare dentro la nota di copyright
dell'autore.

## Quando avete finito

- Avete una skill installata e sapete dove sta.
- Avete letto il file che la definisce e capito da che cosa dipende la sua attivazione.
- Avete una cartella con il vostro scopo scritto dentro e una prima lezione su un argomento
  che volevate imparare.
