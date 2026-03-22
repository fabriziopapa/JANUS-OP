# JANUS-OP

**Tesi di Laurea Magistrale LM-56**  
Università Telematica Pegaso

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

## Struttura

```
JANUS-OP/
├── main.tex                  # Documento principale
├── bibliografia.bib          # Riferimenti bibliografici
├── frontmatter/
│   ├── frontespizio.tex      # Frontespizio Pegaso
│   ├── ringraziamenti.tex    # Ringraziamenti
│   ├── introduzione.tex      # Introduzione
│   └── conclusioni.tex       # Conclusioni
├── chapters/
│   ├── capitolo1.tex         # Digital Government, innovazione e cybersecurity
│   ├── capitolo2.tex         # IA nella Pubblica Amministrazione
│   ├── capitolo3.tex         # Data Governance e maturità digitale negli Atenei
│   └── capitolo4.tex         # Casi europei e istituzionali di IA on-premise
├── images/
│   ├── pegaso-logo.png       # Logo Pegaso (storico)
│   └── pegaso-logo-new.png   # Logo Pegaso (2025)
└── .gitignore
```

## Compilazione

### Overleaf
1. Collegare questa repository GitHub a Overleaf
2. Impostare il compilatore su **pdfLaTeX** + **Biber**
3. Attivare **Shell escape** se necessario

### Locale
```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

## Capitoli

1. **Digital Government, innovazione e cybersecurity nella PA**
2. **Intelligenza Artificiale nella Pubblica Amministrazione**
3. **Data Governance e maturità digitale negli Atenei**
4. **Casi europei e istituzionali di IA on-premise nella PA**

## Licenza

Tutti i diritti riservati © 2025 Fabrizio Papa
