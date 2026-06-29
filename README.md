# JANUS-OP

**Tesi di Laurea Magistrale LM-56**  
Università Telematica Pegaso

> *JANUS-OP prende ispirazione dalla divinità romana Giano, simbolo della capacità di osservare simultaneamente passato e futuro per supportare decisioni strategiche consapevoli. OP = On-Premise + man-in-the-loop.*

## Titolo

*L'utilizzo di sistemi di Intelligenza Artificiale in ambiente on-premise a supporto dei processi decisionali strategici nella Pubblica Amministrazione*

## Informazioni

| Campo | Dettaglio |
|-------|-----------|
| **Candidato** | Fabrizio Papa |
| **Matricola** | 0612400849 |
| **Corso** | Economia, Digital Data Analysis e Amministrazioni Pubbliche (LM-56) |
| **Relatore** | Prof. Pasquale Sasso |
| **ORCID Relatore** | [0000-0002-7996-2602](https://orcid.org/0000-0002-7996-2602) |
| **Insegnamento** | Innovation & Cybersecurity Management per la PA |
| **Anno Accademico** | 2025/2026 |

## Stato di avanzamento

| Capitolo | Titolo | Stato |
|----------|--------|-------|
| Introduzione | JANUS-OP: motivazioni e struttura della tesi | ✅ Revisionata |
| Capitolo 1 | Digital Government, innovazione e cybersecurity nella PA | ✅ Completato |
| Capitolo 2 | L'IA nella PA: framework teorici, dimensione strategica e governance | ✅ Completato |
| Capitolo 3 | Data Governance e maturità digitale negli Atenei | ✅ Completato |
| Capitolo 4 | Casi europei e istituzionali di adozione di IA on-premise nella PA | ✅ Completato |
| Conclusioni | Sintesi, implicazioni, limiti e prospettive | ✅ Completate |

La tesi compila integralmente (116 pagine: front matter, 4 capitoli, conclusioni, bibliografia, elenco tabelle, elenco acronimi).

## Struttura repository

```
JANUS-OP/
├── main.tex                      # Documento principale
├── bibliografia.bib              # 165 voci (deduplicata: rimossi 14 doppioni)
├── frontmatter/
│   ├── acronimi.tex              # ~49 acronimi (aggiungere qui i nuovi)
│   ├── frontespizio.tex          # Frontespizio conforme Pegaso
│   ├── ringraziamenti.tex        # Ringraziamenti
│   ├── introduzione.tex          # ✅ Revisionata (allineata a tutti e 4 i capitoli)
│   └── conclusioni.tex           # ✅ Completate
├── chapters/
│   ├── capitolo1.tex             # ✅ Digital Government, cybersecurity, DESI
│   ├── capitolo2.tex             # ✅ IA nella PA: UTAUT, RBV, TOE, DEG, TCE
│   ├── capitolo3.tex             # ✅ Data Governance, benchmark europei, gap analysis
│   └── capitolo4.tex             # ✅ Analisi comparativa casi europei (8 casi, tassonomia 8 modelli)
├── images/
│   ├── pegaso-logo.svg           # Logo ufficiale Pegaso (SVG originale)
│   └── pegaso-logo.png           # Logo Pegaso 300dpi (generato da SVG)
├── .gitignore
└── README.md
```

## Struttura del documento

```
Frontespizio → Ringraziamenti → Indice → Introduzione
→ Cap. 1 → Cap. 2 → Cap. 3 → Cap. 4 → Conclusioni
→ Bibliografia → Elenco Tabelle → Elenco Acronimi
```

## Indice dettagliato

<details>
<summary><strong>Capitolo 1</strong> — Digital Government, innovazione e cybersecurity nella PA</summary>

- §1.1 Evoluzione del paradigma: da e-Government a Digital Government
- §1.2 Piano Triennale ICT 2024–2026
- §1.3 Infrastrutture digitali e cloud strategy nella PA (Strategia Cloud Italia, PSN, classificazione tripartita dati)
- §1.4 Cybersecurity e sovranità digitale (ACN, NIS 2, Perimetro Cibernetico, CLOUD Act)
- §1.5 Indicatori europei di maturità digitale (DESI, Digital Government Index)

</details>

<details>
<summary><strong>Capitolo 2</strong> — L'IA nella PA: framework teorici, dimensione strategica e governance</summary>

- §2.1 Framework teorici di information systems (UTAUT, RBV, TOE, DeLone & McLean)
- §2.2 L'IA come leva di cambiamento strategico (DEG, technology enactment, Leavitt)
- §2.3 Governance dell'IA: modelli di maturità, AI capability, NIST AI RMF, ISO/IEC 42001, AI Act Allegato III
- §2.4 Sovranità digitale e autonomia strategica (Floridi, Roberts, Couture; PSN)
- §2.5 Scelta make-or-buy: TCE, vendor lock-in, TCO, architetture ibride, modello decisionale a 4 dimensioni

</details>

<details>
<summary><strong>Capitolo 3</strong> — Data Governance e maturità digitale negli Atenei</summary>

- §3.1 Il ruolo delle università nella transizione digitale
- §3.2 Framework di Data Governance (DAMA-DMBOK, ISO/IEC 38505, ISO/IEC 27001, NIST AI RMF)
- §3.3 Maturity model per la PA (CMMI-DMM, modello AI-readiness a 4 livelli)
- §3.4 Benchmark europei (TU Delft, KU Leuven, CINECA)
- §3.5 Gap analysis e criticità (4 gap critici: governance dato, certificazione sicurezza, governance rischio algoritmico, competenze MLOps)

</details>

<details>
<summary><strong>Capitolo 4</strong> — Casi europei e istituzionali di adozione di IA on-premise nella PA</summary>

- §4.1 Framework metodologico (comparative case study, macro-meso-micro, TOE, SAM, Dynamic Capabilities)
- §4.2 Casi nazionali europei (Estonia, Francia/DINUM, Germania/Gaia-X, Paesi Bassi, Finlandia/AuroraAI)
- §4.3 Casi istituzionali (consorzio Aristote, rete Helmholtz-CINECA, Svezia/DIGG-Scozia)
- §4.4 Analisi comparativa trasversale (4 pattern ricorrenti, driver TOE, barriere strutturali, tassonomia 8 modelli di adozione)
- §4.5 Implicazioni per la PA italiana e per gli atenei (modello consortile, 4 raccomandazioni manageriali, paradigma JANUS-OP)

</details>

## Formattazione (linee guida Pegaso)

| Parametro | Valore |
|-----------|--------|
| Font | Times New Roman 12pt |
| Margini | sup. 2.5cm, inf. 2cm, sx 3cm (2+1 rilegatura), dx 2cm |
| Interlinea | Doppia |
| Rientro | 0.5cm |
| Titoli capitolo | 16pt grassetto |
| Titoli sezione | 12pt grassetto |
| Titoli sottosezione | 12pt grassetto corsivo |
| Intestazioni / piè di pagina | 9pt |
| Numerazione | Front matter in romano (i, ii, …), corpo in arabo (1, 2, …) |
| Tabelle | Font ridotto, testo a bandiera, interlinea singola |
| Bibliografia | BibLaTeX + Biber, stile authoryear |
| Citazione in testo | `\textcite{}` se autore in frase, `\parencite{}` parentetica |

## Compilazione

### Overleaf
1. Caricare il progetto (Upload Project con lo ZIP) oppure collegare questa repository GitHub
2. Compilatore **pdfLaTeX** (Overleaf esegue automaticamente **Biber** e **makeglossaries**)
3. Premere **Recompile**

### Locale
```bash
pdflatex main.tex
biber main
makeglossaries main
pdflatex main.tex
pdflatex main.tex
```

### Aggiungere un nuovo acronimo
Editare `frontmatter/acronimi.tex` e aggiungere:
```latex
\newacronym{chiave}{SIGLA}{Definizione estesa}
```
Poi usare `\gls{chiave}` nel testo. Tutti i capitoli usano `\gls{}`; `\glsaddall` (in `main.tex`) garantisce che l'Elenco degli Acronimi sia completo anche per le sigle non richiamate via `\gls`.

### Convenzione chiavi BibTeX
Usare suffisso disambiguante: `Cognome2025KeywordBreve` (es. `Hohmann2025AIActGDPR`).  
Non aggiungere duplicati: verificare sempre in `bibliografia.bib` prima di inserire nuove voci. Le chiavi non devono contenere caratteri non-ASCII.

## Revisione editoriale

Il progetto ha subito un audit completo (grammatica, stile, coerenza discorsiva, formattazione e bibliografia). In sintesi:

- coerenza fattuale: uniformati i conteggi (8 casi, 8 modelli), allineati i nomi dei pattern, riconciliate cifre e date, rimosso il riferimento non sviluppato al caso Parthenope;
- grammatica e refusi corretti; citazione `Nograsek2014` riparata;
- acronimi convertiti a `\gls{}` nei capitoli, Elenco Acronimi completato;
- bibliografia deduplicata (179 → 165 voci); il file `BIB_CAMPI_MANCANTI.md` elenca i campi (`urldate`, `langid`, `doi`) ancora da completare a mano;
- formattazione: rimosso l'elenco figure vuoto, intestazioni a 9pt con titoli brevi per i capitoli lunghi, tabelle rese leggibili, URL spezzabili (`xurl`), front matter in numeri romani.

## Paradigma di lavoro

Questo progetto segue il paradigma **man-in-the-loop**: ogni modifica viene analizzata e proposta prima del push, che avviene solo dopo approvazione esplicita dell'autore.

## Licenza

Tutti i diritti riservati © 2026 Fabrizio Papa
