# Cartella di prova — Classe 3ª B

Materiale **completamente inventato**, creato per il corso *Dalla IA generativa
alla IA agentica*. Serve per far lavorare l'agente su dati realistici senza
toccare dati veri di studenti.

> ⚠️ Nomi, voti, date e annotazioni sono di fantasia. Qualunque somiglianza con
> persone reali è casuale. Non inserite qui dati veri della vostra classe.

## Lo scenario

Siete il docente di **Matematica** della **3ª B** (Liceo delle Scienze Umane),
**3 ore settimanali** — lunedì, mercoledì, venerdì.
Siamo a fine gennaio 2026: il primo quadrimestre si è appena chiuso e dovete
tirare le somme. In classe ci sono **21 studenti**.

Nel quadrimestre avete svolto **3 verifiche scritte** e **2 giri di
interrogazioni**. Non tutti hanno tutte le valutazioni: qualcuno era assente,
qualcuno è arrivato a novembre, qualcuno non è ancora stato interrogato nel
secondo giro. È voluto — è la situazione in cui vi trovate davvero.

## Cosa c'è dentro

| Cartella | Contenuto |
|---|---|
| `01-classe/` | Elenco degli studenti e annotazioni sulla classe |
| `02-programmazione/` | Programmazione annuale e diario delle lezioni svolte |
| `03-verifiche/` | Testi delle tre verifiche + griglie di valutazione compilate |
| `04-valutazioni/` | Riepilogo dei voti: scritti e orali |
| `05-materiali/` | Materiale didattico prodotto durante l'anno |

`AGENTS.md` è il file-guida: l'agente lo legge da solo quando apre la cartella.
`CLAUDE.md` e `GEMINI.md` sono lì solo per rimandare ad `AGENTS.md`, così la
cartella funziona con qualunque strumento usiate.

## Come sono fatti i voti

I voti degli scritti derivano dalle griglie in `03-verifiche/`. Ogni verifica è
valutata su quattro indicatori — comprensione 0-2, procedura 0-3, calcolo 0-3,
linguaggio e ordine 0-2 — e il totale fa 10.

---

Gli esercizi del laboratorio sono nel file `LABORATORIO.md`, nella cartella
principale del corso: sta **fuori** di qui apposta.
