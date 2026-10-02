# Lezione 8 · Prerequisiti — Preparare il computer per la lezione 9

> A casa · una volta sola · circa 20 minuti · per Windows e per Mac

## Che cosa serve e perché

Nella lezione 9 create la vostra copia di Geode. Per farla funzionare sul vostro computer
servono due programmi, che si installano come tutti gli altri:

- **Python**, il linguaggio in cui è scritto il motore. Lo usa l'agente, non voi.
- **Git**, che conserva le «fotografie» del vostro lavoro, così si può sempre tornare
  indietro.

Servono anche l'**applicazione dell'agente** che avete scelto nella lezione 2, già
installata, e **la scheda di progetto** compilata nel laboratorio di oggi.

**Non serve ancora un account GitHub.** Servirà solo nell'ultima lezione, se deciderete di
pubblicare il sito.

Se qualcosa non funziona, **non preoccupatevi**: venite lo stesso. All'inizio della
lezione 9 c'è tempo per sistemare le installazioni.

## Windows

### 1 · Python 3.12

1. Scaricate l'installatore da
   <https://www.python.org/downloads/release/python-31210/>: nella sezione *Files* scegliete
   **Windows installer (64-bit)**.
2. Aprite il file. Nella **prima schermata** spuntate **Add python.exe to PATH**, e poi
   premete **Install Now**.

La spunta è il passaggio che permette all'agente di trovare Python. Se l'avete saltata,
riaprite l'installatore, scegliete *Modify*, poi *Next* e **Add Python to environment
variables**.

### 2 · Git

1. Scaricate **Git for Windows** da <https://git-scm.com/downloads/win> e aprite il file.
2. Mantenete le opzioni proposte. Quando chiede come usare Git dalla riga di comando,
   lasciate **Git from the command line and also from 3rd-party software**.

*(Alternativa per chi è pratico: da PowerShell,
`winget install Python.Python.3.12 Git.Git`.)*

## Mac

### 1 · Python 3.12

Scaricate da <https://www.python.org/downloads/release/python-31210/> il
**macOS 64-bit universal2 installer**, aprite il file `.pkg` e seguite la procedura.

### 2 · Git

Aprite il **Terminale** (cercatelo con Spotlight) e scrivete:

```
git --version
```

Se Git non c'è, il Mac propone di installare gli **strumenti da riga di comando**: accettate
e attendete la fine. Non occorre installare Xcode.

## Il controllo

**Chiudete e riaprite** il Terminale (su Windows, PowerShell). Poi scrivete, una riga alla
volta:

```
python --version
git --version
```

Devono rispondere con un numero di versione, per esempio `Python 3.12.10` e
`git version 2.x`.

### Se qualcosa non va

- **Su Windows `python` apre il Microsoft Store, oppure dice che non viene trovato.**
  Quasi sempre è la spunta *Add python.exe to PATH* saltata. Riaprite l'installatore di
  Python come descritto sopra, poi chiudete e riaprite PowerShell.
- **`git` non risponde subito dopo l'installazione.** Chiudete e riaprite la finestra da
  cui lanciate il comando.
- **Il computer è della scuola e non lascia installare.** Venite lo stesso, e ditelo
  all'inizio della lezione 9.

## Da portare alla lezione 9

- [ ] Python e Git rispondono al controllo
- [ ] L'applicazione dell'agente è installata e aperta almeno una volta
- [ ] La scheda di progetto, fotografata o in un file di testo
