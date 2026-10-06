# Lezione 9 · Laboratorio — La vostra istanza di Geode

> Al computer · da soli · 30 minuti · serve la scheda di progetto della lezione 8

## Cosa facciamo e perché

Oggi nasce il vostro sito. Partite da una **cartella vuota**, incollate un messaggio e fate
preparare il progetto all'agente; poi gli date la scheda di progetto e arrivate a una
prima lezione della vostra materia, visibile in anteprima sul vostro computer.

Non dovete conoscere il motore di Geode né usare il terminale: i comandi li esegue l'agente.
Il vostro lavoro è **leggere che cosa fa, scegliere quando vi viene chiesto e controllare
il risultato**, come nelle lezioni precedenti.

**Nessun dato di studenti**, nemmeno negli esempi.

## Prima di cominciare

- Python 3.12 e Git rispondono in un terminale nuovo (`python --version`, `git --version`).
- L'assistente scelto è aperto e con l'accesso fatto, in una modalità che lavora su una
  **cartella del computer** (per Claude Desktop: scheda **Code**, modalità **Local**).
- Avete davanti la **scheda di progetto** della lezione 8: obiettivo, sequenza,
  interazione, criterio.
- Una **cartella nuova e vuota**, con un nome chiaro (ad esempio `i-miei-corsi`), in un
  posto che ritrovate.

Se Python o Git non rispondono, non andate avanti da soli: chiamate chi conduce, o guardate
a coppie lo schermo di un vicino. Il lavoro si può rifare a casa.

## Passi

### 1 · Cartella e messaggio di avvio · 5 minuti

Aprite la cartella vuota nell'assistente e incollate questo messaggio, così com'è:

```
Sono un docente e voglio creare il sito dei miei corsi con Geode.
Prepara in questa cartella vuota una copia indipendente del progetto
https://github.com/mporfido/geode, con una nuova storia locale e senza
collegamenti per pubblicare nel progetto originale. Se la cartella contiene
già del lavoro, fermati e aiutami a scegliere una cartella vuota.
Leggi README.md, AGENTS.md e CLAUDE.md, poi segui
.agents/skills/inizia/SKILL.md. Verifica tu Python, Git e le dipendenze,
prepara l'ambiente e avvia l'anteprima. Esegui tu i comandi necessari;
guidami con passaggi grafici solo quando serve il mio intervento.
Parlami in italiano, senza gergo tecnico.
```

Se usate **Codex** o **Antigravity**, prima incollate il prompt di adattamento che trovate in
`docs/SETUP.md` di Geode (sezione «Usare Codex o Antigravity»), poi questo messaggio.

Guardate che cosa fa l'agente: scarica il progetto, prepara l'ambiente, installa i
pacchetti. L'installazione richiede la rete e può durare qualche minuto.

### 2 · Modulo e tema · 8 minuti

L'agente vi manda **un solo messaggio** con i dati del sito: nome, sottotitolo, materia,
destinatari, nome per il footer, formule sì/no. Rispondete tutto insieme, anche con un
paragrafo libero.

- Controllate il **riepilogo** prima che scriva i file.
- L'agente ricava dal nome una sigla breve per i progressi degli studenti. **Annotatela:**
  una volta pubblicato il sito non si cambia più.
- Poi vi mostra un'anteprima comparativa dei temi. Scegliete quello che preferite.
- Infine apre il sito nel browser, all'indirizzo `localhost:5000`. Fate un giro nel corso
  **benvenuto**.

### 3 · La prima lezione · 10 minuti

Chiedete all'agente di creare il vostro primo corso e la prima lezione, **incollando la
scheda di progetto per intero**. Ad esempio:

```
Questa è la mia scheda di progetto: [obiettivo, sequenza, interazione, criterio].
Crea il corso e la prima lezione. Prima di scrivere, proponimi la scaletta dei passi
con l'interazione scelta per ciascuno e il motivo.
```

- Rispondete alle poche domande per il corso (titolo, descrizione, ordine delle lezioni).
- Leggete la **scaletta** prima di dare l'ok. Corrisponde alla vostra scheda? Se un passo è
  sbagliato, dite quale e perché.
- Quando la lezione è pronta, aprite l'anteprima.

### 4 · Provare e correggere · 5 minuti

Fate voi lo studente. Rispondete giusto e sbagliato a ogni domanda e guardate che cosa
succede.

- La risposta segnata come giusta lo è davvero?
- Il passo successivo compare quando deve?
- Il testo dice solo cose vere, senza esempi inventati?
- Il tono va bene per la vostra classe?

**Cambiate almeno una cosa.** Una parola o un numero: direttamente nel file. Una
struttura da rifare: chiedetelo all'agente, indicando il passo e il motivo («nel passo 3 le
risposte sbagliate sono troppo ovvie, riscrivile con errori tipici»). Ricaricate la pagina.

### 5 · Il salvataggio · 2 minuti

Scrivete: **«Salva il lavoro».** L'agente riassume che cosa c'è di nuovo e scatta una
fotografia del progetto, con una frase in italiano. Controllate che la frase dica quello
che avete fatto. Il lavoro resta sul vostro computer: **non è online.**

## Da controllare alla fine

- La cartella contiene il progetto e l'anteprima si apre nel browser?
- C'è almeno una lezione della vostra disciplina, nata dalla vostra scheda?
- Avete cambiato qualcosa dopo averla provata?
- Il lavoro è salvato, con una frase che lo descrive?
- Sapete qual è la sigla dei progressi, e che non andrà più cambiata a sito pubblicato?

## Se qualcosa non va

Quasi sempre basta descrivere il problema all'agente, o incollargli il messaggio di errore.

| Che cosa succede | Che cosa fare |
|---|---|
| L'agente si ferma: la cartella non è vuota | È voluto. Create una cartella nuova e riaprite l'assistente lì |
| «Python non è stato trovato» | Su Windows, riaprite l'installatore di Python, scegliete *Modify* e *Add Python to environment variables*; poi chiudete e riaprite l'assistente |
| L'installazione dei pacchetti non finisce | Aspettate; se resta ferma provate un'altra rete e ditelo all'agente |
| L'agente fa molte domande una dopo l'altra | Scrivete: «Segui la skill inizia: manda un solo modulo» |
| Il sito non si apre nel browser | Chiedete: «Avvia l'anteprima e dimmi l'indirizzo» |

## Per chi finisce prima

Aggiungete alla lezione un'**interazione diversa** da quella già scelta (uno slider, un
contenuto che si rivela dopo la risposta) e provate se la lezione ci guadagna. Oppure
scrivete la scheda di una seconda lezione per il prossimo incontro.
