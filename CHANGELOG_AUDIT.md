# Changelog correzioni audit — JANUS-OP

Base: versione "buona" del repo GitHub `fabriziopapa/JANUS-OP` (commit `9ae42fa`).
Tutte le modifiche sono state validate: nessuna chiave `\gls`/`\ref` rotta, parentesi bilanciate, tutte le citazioni risolvibili nel `.bib`.

## A — Coerenza fattuale
- **Caso Parthenope (A1):** *non* rimosso dal cap. 2 perché il tuo cap. 2 attuale già rinvia al cap. 3 sui benchmark; **la promessa nominativa "Università Parthenope" resta nel cap. 2 (riga ~191) ma il cap. 3 non la tratta.** → da decidere tu: o reintroduci un cenno alla Parthenope nel cap. 3, o togli il nome nel cap. 2. *(Lasciato a te perché è una scelta di contenuto.)*
- **Conteggio casi (A2):** introduzione → da «sette casi … Estonia, Francia, Germania, Paesi Bassi, Finlandia, Svezia/Scozia e Italia» a «**otto casi**: cinque nazionali (Estonia, Francia, Germania, Paesi Bassi, Finlandia) e tre istituzionali (Aristote, Helmholtz-CINECA, Svezia/DIGG-Scozia)», allineato al cap. 4.
- **Conteggio modelli (A2):** introduzione → «la tassonomia dei **sette** modelli» → «**otto** modelli».
- **Nomi dei 4 pattern (A2):** conclusioni → da «sovranità-prima, consortile, governance-first e proattivo» a «**normativa come driver architetturale, consorzialità, separazione tra dato e output, gradualità dell'adozione**» (i 4 pattern reali del cap. 4).
- **Acronimo OP / man-in-the-loop (A3):** aggiunta in introduzione una frase che anticipa il concetto «man-in-the-loop» come secondo pilastro valoriale accanto all'on-premise.
- **Leonardo (A4):** cap. 3 → da «tra i **dieci** sistemi HPC più potenti» a «tra i **primi cinque** … al momento dell'entrata in esercizio», coerente con il cap. 4.
- **Data AI Act (A4):** cap. 2 → obblighi deployer alto rischio da «2 **febbraio** 2026» a «2 **agosto** 2026», coerente con cap. 4 e conclusioni.
- **Riferimento SAM (A5):** cap. 4 → rimosso «SAM» dall'elenco dei framework attribuiti al cap. 2 (il SAM è introdotto solo nel cap. 4).

## B — Grammatica
- «una asimmetria» → «**un'asimmetria**» (cap. 2 e cap. 3).
- «architett**uale**» → «architett**urale**» (cap. 4, ×5).
- «gouvernement-as-a-platform» → «**government as a platform**» (cap. 4), allineato al cap. 1.

## C — Stile (interventi mirati)
- Rimosso l'aforisma di chiusura «Come Giano insegna da due millenni e mezzo.» (conclusioni).
- Frase argomentativa duplicata verbatim intro/cap. 2: nel cap. 2 ora è marcata come richiamo («— già anticipata nell'Introduzione —»).

## D — Formattazione, citazioni, bibliografia
- **Citazione rotta (D1):** `\parencite{Nograšek2014}` → `\parencite{Nograsek2014}` (cap. 2), allineata alla chiave del `.bib`.
- **Elenco figure vuoto (D3):** rimosso `\listoffigures` da `main.tex` (non c'erano figure).
- **Acronimi (D2):** aggiunte 8 definizioni mancanti (ACN, CAPEX, DIGG, DINUM, EuroHPC, MLOps, OPEX, SAM) e inserito `\glsaddall` prima di `\printglossary` → **l'Elenco degli Acronimi ora è completo**.
  - ⚠️ *Non* è stata fatta la conversione in-testo a `\gls{}` nei cap. 1/3/4: in questo ambiente non posso compilare (mancano babel-italiano e biber), e una conversione di massa non verificabile a ridosso del push è rischiosa. `\glsaddall` ottiene comunque l'elenco completo. Se vuoi la conversione in-testo completa, la faccio con un compile in loop.
- **Bibliografia dedup (D4):** rimosse **14 voci duplicate**. 12 erano duplicati non citati; 2 coppie erano la stessa fonte citata con due chiavi:
  - `Hohmann2025AIActGDPR` → unificato su `HohmannKollar2025` (citazioni cap. 3 rimappate).
  - `MadanAshok2022` → unificato su `Madan2023` (citazione cap. 4 rimappata; aggiunto DOI).
  - Altre rimosse: McNicol2024, Dabbous2026, Torichnyi2025, Pham2025, Madhavan2025, Abdallah2026, PatonRomero2018, Wichmann2020, Enqvist2024, Lore2023, Ribeiro2025, Criado2019. Voci: 179 → **165**.
- **Campi bib (D5):** *non* ho aggiunto in massa `urldate`/`langid`/DOI mancanti nel blocco recente: richiederebbero dati per-fonte che non posso inventare senza falsare la bibliografia. Da completare a mano.
- **Riferimento tabella (D6):** cap. 3 → «La tabella seguente sintetizza…» → «La Tabella~\ref{tab:framework-governance} sintetizza…» (le altre tabelle restano introdotte discorsivamente: cosmetico).

## Non applicato / da decidere
- A1 caso Parthenope (scelta di contenuto, vedi sopra).
- D2 conversione in-testo `\gls{}` completa (serve compile locale).
- D5 uniformazione campi bib oltre il dedup.
- C editing stilistico esteso (hai scelto "solo interventi mirati").

## Come pushare
Il repo locale risultava in uno **stato di rebase git interrotto**. Se git protesta:
```
git rebase --abort        # se segnala un rebase in corso
git add -A
git commit -m "Audit fix: coerenza, grammatica, citazioni, acronimi, bib dedup"
git push
```
In alternativa è incluso `audit-fix.patch` (applicabile a un clone pulito con `git am audit-fix.patch`).
**Verifica consigliata:** compila la tesi in locale (con biber) prima del push, per controllare l'Elenco Acronimi e la bibliografia.
