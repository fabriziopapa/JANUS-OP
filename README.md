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

| Capitolo | Titolo | Stato | Commit |
|----------|--------|-------|--------|
| Introduzione | JANUS-OP: motivazioni e struttura della tesi | ✅ Revisionata | `06748af` |
| Capitolo 1 | Digital Government, innovazione e cybersecurity nella PA | ✅ Completato | — |
| Capitolo 2 | L'IA nella PA: framework teorici, dimensione strategica e governance | ✅ Completato | — |
| Capitolo 3 | Data Governance e maturità digitale negli Atenei | ✅ Completato | `4cdea41` |
| Capitolo 4 | Proposta di architettura IA on-premise per l'Università Parthenope | 🏗️ Struttura pronta | `4d7f568` |
| Conclusioni | — | ⏳ Da scrivere | — |

## Struttura repository

```
JANUS-OP/
├── main.tex                      # Documento principale
├── bibliografia.bib              # 171 voci verificate (zero duplicati)
├── frontmatter/
│   ├── acronimi.tex              # Acronimi (aggiungere qui i nuovi)
│   ├── frontespizio.tex          # Frontespizio conforme Pegaso
│   ├── ringraziamenti.tex        # Ringraziamenti
│   ├── introduzione.tex          # ✅ Revisionata (allineata ai 3 cap. definitivi)
│   └── conclusioni.tex           # Conclusioni (placeholder)
├── chapters/
│   ├── capitolo1.tex             # ✅ Digital Government, cybersecurity, DESI
│   ├── capitolo2.tex             # ✅ IA nella PA: UTAUT, RBV, TOE, DEG, TCE
│   ├── capitolo3.tex             # ✅ Data Governance, benchmark europei, gap analysis
│   └── capitolo4.tex             # 🏗️ Struttura con indice definitivo del prof.
├── images/
│   ├── pegaso-logo.svg           # Logo ufficiale Pegaso (SVG originale)
│   └── pegaso-logo.png           # Logo Pegaso 300dpi (generato da SVG)
├── docs/
│   └── prompt_capitolo4.md       # Prompt operativo per la stesura del Cap. 4
├── .gitignore
└── README.md
```

## Struttura del documento (Scuola B)

```
Frontespizio → Ringraziamenti → Indice → Introduzione
→ Cap. 1 → Cap. 2 → Cap. 3 → Cap. 4 → Conclusioni
→ Bibliografia → Elenco Figure → Elenco Tabelle → Elenco Acronimi
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
<summary><strong>Capitolo 3</strong> — Data Governance e maturità digitale negli Atenei ✅</summary>

- §3.1 Il ruolo delle università nella transizione digitale (DESI 2024, Italia 18°, Fast Tracker)
- §3.2 Framework di Data Governance (DAMA-DMBOK, ISO/IEC 38505, ISO/IEC 27001, NIST AI RMF)
- §3.3 Maturity model per la PA (CMMI-DMM, modello AI-readiness a 4 livelli)
- §3.4 Benchmark europei (TU Delft, KU Leuven, CINECA)
- §3.5 Gap analysis e criticità (4 gap critici: governance dato, certificazione sicurezza, governance rischio algoritmico, competenze MLOps)

</details>

<details>
<summary><strong>Capitolo 4</strong> — Proposta di architettura IA on-premise per l'Università Parthenope 🏗️</summary>

- §4.1 Requisiti funzionali e normativi
- §4.2 Architettura tecnica proposta
- §4.3 Modello di governance e ruoli
- §4.4 Analisi economico-finanziaria (NPV, ROI, TCO)
- §4.5 Analisi dei rischi (cyber, legali, organizzativi)
- §4.6 Valutazione comparativa on-premise vs cloud

> 📄 Vedi `docs/prompt_capitolo4.md` per le istruzioni operative complete di stesura.

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
| Bibliografia | BibLaTeX + Biber, stile authoryear |
| Citazione in testo | `\textcite{}` se autore in frase, `\parencite{}` parentetica |

## Compilazione

### Overleaf
1. Collegare questa repository GitHub a Overleaf
2. Impostare il compilatore su **pdfLaTeX** + **Biber**
3. Attivare **makeglossaries** per l'elenco acronimi

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
Poi usare `\gls{chiave}` nel testo.

### Convenzione chiavi BibTeX
Usare suffisso disambiguante: `Cognome2025KeywordBreve` (es. `Hohmann2025AIActGDPR`).  
Non aggiungere duplicati: verificare sempre in `bibliografia.bib` prima di inserire nuove voci.

## Paradigma di lavoro

Questo progetto segue il paradigma **man-in-the-loop**: ogni modifica viene analizzata e proposta prima del push, che avviene solo dopo approvazione esplicita dell'autore.

## Licenza

Tutti i diritti riservati © 2026 Fabrizio Papa
