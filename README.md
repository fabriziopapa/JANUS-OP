# JANUS-OP

**Tesi di Laurea Magistrale LM-56**  
Università Telematica Pegaso

> *JANUS-OP prende ispirazione dalla divinità romana Giano, simbolo della capacità di osservare simultaneamente passato e futuro per supportare decisioni strategiche consapevoli. OP = On-Premise.*

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
| Introduzione | JANUS-OP: motivazioni e struttura | ✅ Completata |
| Capitolo 1 | Digital Government, innovazione e cybersecurity nella PA | ✅ Completato |
| Capitolo 2 | L'IA nella PA: framework teorici, dimensione strategica e governance | ✅ Completato |
| Capitolo 3 | Data Governance e maturità digitale negli Atenei | 🔄 In corso |
| Capitolo 4 | Casi europei e istituzionali di IA on-premise nella PA | 🔄 In corso |
| Conclusioni | — | ⏳ Da scrivere |

## Struttura repository

```
JANUS-OP/
├── main.tex                      # Documento principale
├── bibliografia.bib              # 132 voci verificate (zero duplicati)
├── frontmatter/
│   ├── acronimi.tex              # 28 acronimi (aggiungere qui i nuovi)
│   ├── frontespizio.tex          # Frontespizio conforme Pegaso
│   ├── ringraziamenti.tex        # Ringraziamenti
│   ├── introduzione.tex          # Introduzione con spiegazione JANUS-OP
│   └── conclusioni.tex           # Conclusioni (placeholder)
├── chapters/
│   ├── capitolo1.tex             # ✅ Digital Government, cybersecurity, DESI
│   ├── capitolo2.tex             # ✅ IA nella PA: UTAUT, RBV, TOE, DEG, TCE
│   ├── capitolo3.tex             # 🔄 Data Governance e caso Parthenope
│   └── capitolo4.tex             # 🔄 Casi europei IA on-premise
├── images/
│   ├── pegaso-logo.svg           # Logo ufficiale Pegaso (SVG originale)
│   └── pegaso-logo.png           # Logo Pegaso 300dpi (generato da SVG)
├── .gitignore
└── README.md
```

## Struttura del documento (Scuola B)

```
Frontespizio → Ringraziamenti → Indice → Introduzione
→ Cap. 1 → Cap. 2 → Cap. 3 → Cap. 4 → Conclusioni
→ Bibliografia → Elenco Figure → Elenco Tabelle → Elenco Acronimi
```

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

## Paradigma di lavoro

Questo progetto segue il paradigma **man-in-the-loop**: ogni modifica viene analizzata e proposta prima del push, che avviene solo dopo approvazione esplicita.

## Licenza

Tutti i diritti riservati © 2026 Fabrizio Papa
