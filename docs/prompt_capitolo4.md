# PROMPT — Stesura Capitolo 4: JANUS-OP
**File di riferimento operativo per la generazione automatica del Capitolo 4**
*Salvato su repo: `docs/prompt_capitolo4.md`*

---

## 1. IDENTITÀ DEL DOCUMENTO

Stai scrivendo il **Capitolo 4** della tesi magistrale:

> **Titolo tesi**: *L'utilizzo di sistemi di Intelligenza Artificiale in ambiente on-premise a supporto dei processi decisionali strategici nella Pubblica Amministrazione*
> **Acronimo**: JANUS-OP
> **Candidato**: Fabrizio Papa, Matricola 0612400849
> **Relatore**: Prof. Pasquale Sasso
> **Corso**: LM-56 — Economia, Digital Data Analysis e Amministrazioni Pubbliche, Università Telematica Pegaso
> **Stile citazioni**: BibLaTeX + Biber, authoryear — `\textcite{}` quando l'autore è parte della frase, `\parencite{}` per citazione parentetica
> **Formattazione**: Times New Roman 12pt, margini sup 2.5cm / inf 2cm / sx 3cm / dx 2cm, interlinea doppia

---

## 2. TITOLO E INDICE AUTORIZZATO DAL PROFESSORE

```
Capitolo 4 — Proposta di architettura IA on-premise per l'Università Parthenope

§4.1  Requisiti funzionali e normativi
§4.2  Architettura tecnica proposta
§4.3  Modello di governance e ruoli
§4.4  Analisi economico-finanziaria (NPV, ROI, TCO)
§4.5  Analisi dei rischi (cyber, legali, organizzativi)
§4.6  Valutazione comparativa on-premise vs cloud
```

---

## 3. CASO DI RIFERIMENTO — UNIVERSITÀ PARTHENOPE (dati reali)

| Dato | Valore |
|---|---|
| Studenti a.a. 2024/25 | 13.505 |
| Studenti a.a. 2022/23 | 12.756 (+9,3%) |
| Docenti (31/12/2022) | 379 |
| RTD (31/12/2024) | 127 |
| Dipartimenti | 8 |
| Scuole | 2 |
| Corsi di studio | 37 |
| Ratio PTA/Docenti | 0,73 |
| RTD referente | Giuseppe Aiello |
| Prorettore IT | Luigi Romano |
| Sistemi gestionali | ESSE3, U-GOV, CSA, IRIS, Titulus 5 |
| Cloud attivo | Azure + Oracle + CINECA |
| Criticità ANVUR 2024 | Wi-Fi instabile, laboratori insufficienti, dati in silos, dematerializzazione incompleta |

**Fonti istituzionali da citare**:
- `Parthenope_ANVUR2024` — https://www.anvur.it/sites/default/files/relazioni-nuclei/2024/Napoli_Parthenope-Relazione_Nuclei_2024-43.pdf
- `Parthenope_PTI2022`
- `Parthenope_Brochure2025`

**Profilo AI-readiness**: livello 2–3 del modello proposto in §3.3.3. Ateneo paradigmatico italiano medio per dimensione e struttura.

---

## 4. REGOLA FONDAMENTALE: COSA NON RIPETERE

I Capitoli 1–3 hanno già trattato in modo approfondito i seguenti argomenti. Nel Cap. 4 **non ridescriverli**: usa esclusivamente `\ref{}` con rimando esplicito alla sezione.

| Argomento già trattato | Dove | Come richiamare nel Cap. 4 |
|---|---|---|
| Sovranità digitale (Floridi, Roberts, Couture) | Cap. 2 §2.4 `\label{sec:cap2-sovranita}` | `come analizzato in §\ref{sec:cap2-sovranita}` |
| CLOUD Act e rischio giuridico | Cap. 1 §1.4.3 + Cap. 2 §2.4.2 | Semplice `\ref{}` in §4.5 |
| Architetture ibride come soluzione ottimale | Cap. 2 §2.5.3 `\label{sec:cap2-tce}` | `la soluzione ibrida già identificata in §\ref{sec:cap2-tce}` |
| Modello decisionale 4 dimensioni | Cap. 2 §2.5.4 | Applicarlo con dati Parthenope in §4.6, non ridescriverlo |
| NIST AI RMF (Govern-Map-Measure-Manage) | Cap. 2 §2.3.3 + Cap. 3 §3.2.4 | Applicarlo a JANUS-OP in §4.3/§4.5, non ridescriverlo |
| DAMA-DMBOK struttura tripartita | Cap. 3 §3.2.1 `\label{sec:framework-governance}` | `come descritto in §\ref{sec:framework-governance}` |
| Pattern architetturali benchmark (TU Delft, KU Leuven, CINECA) | Cap. 3 §3.4 `\label{sec:benchmark-europei}` | Richiamarli come punto di partenza in §4.2 |
| 4 gap critici degli atenei italiani | Cap. 3 §3.5 `\label{sec:gap-analysis}` | Mostrare come JANUS-OP li chiude in §4.2/§4.3 |
| TCO come concetto multi-componente | Cap. 2 §2.5.3 | `\ref{sec:cap2-tce}` + fornire i numeri per Parthenope |
| Vendor lock-in (3 tipologie, Opara 2016) | Cap. 2 §2.5.2 | Semplice `\ref{}` in §4.5/§4.6 |
| NIS 2 e Perimetro Cibernetico | Cap. 1 §1.4 `\label{sec:cybersecurity}` | Semplice `\ref{}` in §4.1/§4.5 |
| AI Act Allegato III (8 categorie alto rischio) | Cap. 2 §2.3.3 + Cap. 3 §3.1.2 | Tabella tracciabilità in §4.1 con `\ref{}` |
| PSN come infrastruttura sovrana | Cap. 2 §2.4.3 | Includerlo come terza opzione in §4.6 |
| ISO/IEC 42001 (38 controlli) | Cap. 2 §2.3.3 | Semplice `\ref{}` in §4.1/§4.3 |
| UTAUT e resistenza culturale | Cap. 2 §2.1 `\label{sec:cap2-framework-is}` | Richiamare in §4.5 (rischi organizzativi) |
| federated learning (concetto) | Cap. 3 §3.4.2 | Non reintrodurre; usare come opzione architetturale in §4.2 |

---

## 5. CONTENUTO DA COSTRUIRE EX NOVO — SEZIONE PER SEZIONE

### §4.1 — Requisiti funzionali e normativi

**Aprire con**: «Il quadro normativo entro cui JANUS-OP si inscrive è stato ricostruito nei Capitoli 1 e 2; la presente sezione ne deriva i requisiti operativi specifici per il caso Parthenope.»

**Da costruire**:
1. **Tabella requisiti normativi** (norma → requisito verificabile → come JANUS-OP lo soddisfa):
   - AI Act Allegato III: supervisione umana qualificata, conservazione log 10 anni, FRIA
   - GDPR art. 25: privacy by design, minimizzazione
   - NIS 2 D.Lgs. 138/2024: cifratura at-rest e in-transit, notifica incidenti 24h
   - Strategia Cloud Italia: dati strategici → hosting sovrano
   - ISO/IEC 27001: prerequisito infrastrutturale
   - ISO/IEC 42001: sistema di gestione IA certificabile
2. **Tabella requisiti funzionali** (novità assoluta — non trattata nei Cap. precedenti):
   - Latenza di inferenza (ms target)
   - Throughput documentale (documenti/ora)
   - Interfacce verso ESSE3, U-GOV, CSA, IRIS, Titulus 5
   - Modalità di supervisione umana (*man-in-the-loop*)
   - Formato di esportazione log per audit
   - Requisiti di accessibilità (D.Lgs. 82/2005 CAD, WCAG 2.1)
3. **Tabella di tracciabilità requisiti → norma** (ingegneria dei requisiti)

---

### §4.2 — Architettura tecnica proposta

**Aprire con**: «I pattern federato, ibrido e consortile identificati nel Cap. 3 (§\ref{sec:benchmark-europei}) convergono nell'architettura JANUS-OP come segue…»

**Da costruire**:
1. **Diagramma a blocchi** dell'architettura JANUS-OP (primo elemento visivo dell'intera tesi):
   - Strato: ingestione dati → preprocessing → fine-tuning → inferenza → supervisione umana → output documentale → audit log
   - Connettori verso ESSE3 / U-GOV / IRIS / Titulus 5
   - Integrazione CINECA per risorse HPC consortili
2. **Stack tecnologico** (tutto ex novo):
   - Modello LLM open-source: Mistral / LLaMA / Gemma o distillato (cit. Hong 2025)
   - Framework di inferenza: Ollama / vLLM / LiteLLM
   - Pipeline RAG (cit. Mala 2025)
   - Hardware GPU: NVIDIA A100/H100 vs soluzioni edge
3. **Collocazione nel modello AI-readiness**: «L'architettura proposta è compatibile con il livello 3 (*Defined*) del modello in §\ref{sec:maturity-model} e progettata per abilitare il passaggio al livello 4 nell'arco di 24 mesi»
4. **Pipeline MLOps**: ciclo di vita del modello (addestramento / fine-tuning / deployment / monitoraggio / retraining / ritiro)
5. **Dimensionamento hardware**: capacità computazionale, consumo energetico stimato, piano di scalabilità

**Non ripetere**: motivazione normativa dell'on-premise (già §1.4 + §2.4), descrizione del federated learning (già §3.4.2)

---

### §4.3 — Modello di governance e ruoli

**Aprire con**: «Il modello di governance proposto declina operativamente la struttura DAMA-DMBOK (§\ref{sec:framework-governance}) e le funzioni NIST AI RMF (§\ref{subsec:nist-airmf}) nel contesto specifico di Parthenope.»

**Da costruire** (tutto ex novo — i framework sono già nei Cap. 2–3):
1. **Organigramma specifico JANUS-OP**: nomi dei ruoli, linee di riporto, ownership decisionale
   - CDO (Chief Data Officer) — da istituire ex novo (gap n. 1)
   - AI Ethics Officer
   - Data Steward di Area (per ciascun dipartimento)
   - MLOps Engineer (interno o convenzionato) — gap n. 4
   - Delegato alla Transizione Digitale come pivot operativo
   - DPO in raccordo con AI Ethics Officer
2. **RACI matrix** per le decisioni chiave:
   - Delibera di adozione di un nuovo modello
   - Gestione incidente algoritmico
   - Aggiornamento dataset di fine-tuning
   - Comunicazione verso studenti sui meccanismi algoritmici
   - Audit periodico del sistema
3. **Comitato di Supervisione Algoritmica**: composizione (dirigente, DPO, responsabile tecnico, rappresentante studenti), frequenza, poteri deliberativi
4. **Procedure di escalation**: anomalie algoritmiche (bias rilevato, drift, incidente privacy)
5. **Raccordo esplicito con i 4 gap di §\ref{sec:gap-analysis}**: mostrare come JANUS-OP chiude gap 1 (governance dato), gap 3 (governance rischio algoritmico) e gap 4 (competenze MLOps)

---

### §4.4 — Analisi economico-finanziaria (NPV, ROI, TCO)

**Aprire con**: «Il TCO, come definito in §\ref{sec:cap2-tce}, include le seguenti voci per il caso JANUS-OP…»

**Questa è la sezione più originale dell'intero capitolo. Costruire con dati numerici:**

1. **Assunzioni dichiarate** (tutte esplicite e documentate):
   - Dimensione: 13.505 studenti, 379 docenti, 8 dipartimenti
   - Volume documentale stimato (atti amministrativi/anno)
   - Costo medio personale PA (€/ora)
   - Costo kWh (tariffa PA)
   - Orizzonte temporale: 5 anni
   - Tasso di sconto: 4–5% (costo capitale PA italiana)

2. **TCO on-premise JANUS-OP**:
   - CAPEX: hardware GPU, integrazione sistemi legacy, certificazione ISO 27001
   - OPEX annuo: personale MLOps, energia (PUE stimato), manutenzione, aggiornamento modello

3. **TCO alternativo** (benchmark):
   - Cloud SaaS: costo per inferenza × volume atteso
   - Status quo: costo del non-fare (inefficienze stimate)

4. **NPV differenziale**: proiezione flussi di cassa on-premise vs cloud/status quo, con tasso di sconto

5. **ROI**: benefici quantificati (ore-funzionario risparmiate × costo orario, riduzione errori) vs investimento netto

6. **Analisi di sensitività** su almeno 3 variabili:
   - Volume di utilizzo del sistema
   - Costo dell'energia
   - Tasso di adozione del personale (variabile UTAUT)

7. **Scenario CINECA vs hardware proprietario**: comparazione costi HPC consortile vs GPU dedicate Parthenope

---

### §4.5 — Analisi dei rischi (cyber, legali, organizzativi)

**Aprire con**: «Il quadro dei rischi cyber e legali del deployment IA nella PA è stato analizzato in §\ref{sec:cybersecurity} (Cap. 1) e §\ref{sec:cap2-sovranita} (Cap. 2). La presente sezione si concentra sui rischi specifici del sistema JANUS-OP, con particolare riguardo alle dimensioni algoritmiche, etiche e organizzative non trattate in precedenza.»

**Richiamare senza ripetere** (solo `\ref{}`): NIS 2, CLOUD Act, Perimetro Cibernetico, vendor lock-in

**Da costruire** (tutto ex novo):
1. **Risk register strutturato** (tabella): rischio | probabilità | impatto | score | owner | misura di mitigazione | KRI di monitoraggio
   - Voci minime: 10–12 rischi tra le categorie seguenti

2. **Rischi algoritmici specifici JANUS-OP**:
   - Bias nei dati degli studenti di Parthenope (distribuzione demografica, studenti con disabilità, studenti internazionali, distribuzione per corso di laurea)
   - Drift del modello in caso di modifica al regolamento didattico
   - Allucinazioni in documenti amministrativi ufficiali
   - Opacità decisionale (collegare a obbligo trasparenza Allegato III AI Act con `\ref{}`)

3. **Rischi cyber specifici dell'on-premise** (paradossalmente assenti nei Cap. 1–2 che trattano rischi cloud):
   - Vulnerabilità hardware fisiche e accesso non autorizzato locale
   - Aggiornamenti software ritardati (patch management)
   - Insider threat su infrastruttura GPU

4. **Rischi organizzativi interni al progetto** (ex novo):
   - Turnover del profilo MLOps (key person risk)
   - Resistenza culturale del personale (richiamare UTAUT §\ref{sec:cap2-framework-is})
   - Rischio di sotto-utilizzo del sistema
   - Mancata compliance AI Act: sanzioni ex Art. 99 (fino a 3% fatturato mondiale)

5. **Rischi etici e reputazionali**:
   - Impatto di predizioni errate sugli studenti (es. predizione di dropout → stigma)
   - Comunicazione ai meccanismi algoritmici (obbligo trasparenza AI Act)

6. **Piano di Business Continuity**:
   - RTO (Recovery Time Objective) e RPO (Recovery Point Objective) per il sistema IA
   - Ridondanza dei nodi di inferenza
   - Procedure di failover

---

### §4.6 — Valutazione comparativa on-premise vs cloud

**⚠ SEZIONE A RISCHIO RIDONDANZA ALTA**: il Cap. 2 §2.5 è già una valutazione comparativa teorica completa. Questa sezione deve operare **esclusivamente sul piano applicativo-quantitativo** con i dati reali di Parthenope.

**Aprire con**: «Il framework teorico per la valutazione comparativa è stato sviluppato in §\ref{sec:cap2-tce} (TCE) e §\ref{sec:cap2-sovranita} (sovranità digitale). Il presente paragrafo lo applica al caso Parthenope attraverso una matrice multi-criterio e i dati economici elaborati in §4.4.»

**Da costruire**:
1. **Matrice multi-criterio** — 3 opzioni × ≥6 criteri:

   | Criterio | On-premise JANUS-OP | PSN | Cloud SaaS qualificato |
   |---|---|---|---|
   | Conformità normativa (AI Act, NIS 2) | … | … | … |
   | Sovranità del dato | … | … | … |
   | TCO a 5 anni (da §4.4) | … | … | … |
   | Maturità organizzativa richiesta | … | … | … |
   | Flessibilità e scalabilità | … | … | … |
   | Rischio lock-in | … | … | … |

2. **Applicazione del modello decisionale §2.5.4** con valori specifici di Parthenope:
   - Sensibilità dati: [classificazione per ESSE3/U-GOV/IRIS]
   - Specificità processi: [valutazione specifica]
   - Maturità organizzativa: livello 2–3 AI-readiness
   - Orizzonte temporale: [piano pluriennale]

3. **Collocazione di Parthenope nel modello AI-readiness** (§\ref{sec:maturity-model}): livello 2–3 attuale → livello 3–4 obiettivo in 24 mesi

4. **Exit strategy** (ex novo):
   - Scenario di desmobilizzazione o migrazione verso PSN
   - Portabilità dei modelli fine-tunati
   - Costi di switching stimati

5. **Raccomandazione finale motivata**: perché l'architettura ibrida CINECA on-premise + componente locale è preferibile alle alternative per Parthenope

**Non ripetere**: §1.3.4 (nodo irrisolto), §2.5.3 (architetture ibride in astratto), §3.4.5 (sintesi benchmark). Solo `\ref{}`.

---

## 6. CONCETTI PONTE — OBBLIGATORI DA RACCOGLIERE

I seguenti costrutti sono stati «annunciati» nei Cap. 1–3 e creano un'attesa narrativa che il Cap. 4 deve obbligatoriamente soddisfare, pena la rottura del filo logico della tesi.

| Concetto | Dove annunciato | Come raccoglierlo nel Cap. 4 |
|---|---|---|
| JANUS-OP come architettura operativa | Introduzione + §3.5.3 "ponte al Cap. 4" | §4.2 risponde alla promessa di §3.5.3; richiamare gap → assi di intervento |
| Man-in-the-loop come risposta ai gap | §3.1.2 + §3.5.3 | §4.2 (architettura) + §4.3 (governance) declinano i 4 assi |
| Modello AI-readiness applicato a Parthenope | §3.3.3 con indicazione esplicita livello 2–3 | §4.2 o §4.6: collocare Parthenope sul modello, motivare scelta architetturale |
| 4 gap critici come problema da risolvere | §3.5 gap analysis | §4.3 chiude gap 1+3; §4.2 chiude gap 2; §4.3 chiude gap 4 |
| PSN come complemento all'on-premise | §2.4.3 + §1.3.3 | §4.6: terza opzione nella matrice comparativa |
| Modello decisionale §2.5.4 applicato | §2.5.4: «guida l'analisi dei casi empirici» | §4.6: prima applicazione esplicita con dati reali |
| TCO/NPV come strumenti promessi | §2.5.3: annuncio senza numeri | §4.4: i numeri che il Cap. 2 ha promesso senza dare |
| CLOUD Act come vincolo operativo | §1.4.3 → §2.4.2 → §3.4.4 | §4.5: chiudere il percorso con implicazioni operative specifiche per JANUS-OP |

---

## 7. CHIAVI BIBLIOGRAFICHE DISPONIBILI IN BIBLIOGRAFIA.BIB

Le seguenti chiavi sono già presenti in `bibliografia.bib` (171 entries) e sono rilevanti per il Cap. 4. Usarle direttamente senza aggiungere duplicati.

**Normativa e framework**:
- `AIAct2024` — Regolamento UE AI Act
- `NIST_AI_RMF` — NIST Artificial Intelligence Risk Management Framework 2023
- `ISO42001` — ISO/IEC 42001:2023
- `GDPR` — Regolamento UE 2016/679
- `NIS2Directive` — Direttiva (UE) 2022/2555
- `DLgs138_2024` — D.Lgs. 138/2024 (recepimento NIS 2)
- `StrategiaCloudItalia` — Strategia Cloud Italia
- `AgIDPianoTriennale2024` — Piano Triennale ICT 2024–2026
- `PerimetroCibernetico` — D.L. 105/2019
- `DataAct2023` — Data Act europeo
- `CLOUDAct_Wire2025` — CLOUD Act
- `ACNQualificazioneCloud` — Qualificazione ACN

**Framework teorici (già citati nei Cap. 1–3, richiamare con \ref)**:
- `Venkatesh2003` — UTAUT
- `Barney1991` — RBV
- `TornatzkyFleischer1990` — TOE
- `DeLone1992` — DeLone & McLean
- `Wirtz2020` — Framework governance IA
- `Williamson1985` — TCE
- `Opara2016` — Vendor lock-in 71%
- `Floridi2020` — Sovranità digitale
- `Couture2019` — 3 dimensioni sovranità
- `Teece2007` — Dynamic Capabilities

**Benchmarks (già citati in Cap. 3, richiamare con \ref)**:
- `Specht2023DataLearning` — TU Delft whitepaper
- `NIST_SP800_145` — NIST cloud computing

**Fonti Parthenope (per Cap. 4)**:
- `Parthenope_ANVUR2024` — Relazione Nuclei 2024
- `Parthenope_PTI2022` — Piano Triennale Informatico
- `Parthenope_Brochure2025` — Brochure istituzionale

**Fonti tecniche IA (per §4.2)**:
- `Hong2025` — Knowledge distillation per LLM on-premise
- `Mala2025` — Pipeline RAG

---

## 8. ISTRUZIONI OPERATIVE PER LA GENERAZIONE

1. **Scrivi direttamente in LaTeX** seguendo le convenzioni degli altri capitoli già sul repo (stessi package, stesso stile, stessi `\label{}`)
2. **Ogni sezione deve aprire con la frase di raccordo** indicata sopra, che aggancia il Cap. 4 al capitolo precedente pertinente
3. **Non aggiungere nuove chiavi bib** senza verificare che non esistano già in `bibliografia.bib`; se necessario aggiungere nuove entry, segnalarle esplicitamente prima di procedere
4. **Le tabelle** vanno in ambiente `table[H]` con `\caption{}` e `\label{}`, usando `tabularx` con `\textwidth` come negli altri capitoli
5. **Il diagramma architetturale** (§4.2) può essere costruito in TikZ o descritto come figura con `\includegraphics{}` se fornita esternamente
6. **I valori numerici** di TCO/NPV/ROI devono essere accompagnati da una sottosezione «Assunzioni e limitazioni» che ne documenti la base di calcolo
7. **Il tono** è analitico-critico e manageriale, non descrittivo: ogni affermazione deve essere argomentata, ogni scelta tecnica motivata, ogni tabella commentata
8. **Lunghezza stimata**: 35–45 pagine (coerente con i Cap. 1–3)

---

## 9. PRIORITÀ DI COSTRUZIONE

| Priorità | Tipo | Sezione | Motivo |
|:---:|---|---|---|
| 1 | **COSTRUIRE** | §4.2 — Diagramma architetturale | Prima rappresentazione visiva dell'intera tesi |
| 2 | **COSTRUIRE** | §4.4 — NPV/ROI/TCO numerici | Unica sezione quantitativa originale, promessa dal Cap. 2 |
| 3 | **COSTRUIRE** | §4.5 — Risk register JANUS-OP | Specifica per il sistema, assente nei Cap. precedenti |
| 4 | **COSTRUIRE** | §4.3 — Organigramma + RACI matrix | Operativizzazione dei framework già teorizzati |
| 5 | **COSTRUIRE** | §4.6 — Matrice comparativa + dati Parthenope | Alta ridondanza teorica: deve essere esclusivamente applicativo |
| 6 | **APPLICARE** | §4.2/§4.6 — Modello AI-readiness su Parthenope | Collocazione esplicita livello 2–3 → 3–4 |
| 7 | **APPLICARE** | §4.6 — Modello decisionale §2.5.4 con valori reali | Prima applicazione con dati, non riformulazione teorica |
| 8 | **APPLICARE** | §4.3 — Gap analysis → assi di intervento | Chiudere la promessa di §3.5.3 |
| 9 | **RICHIAMARE** | §4.1 — Requisiti normativi con tabella tracciabilità | Sintesi operativa, non ridescrittura delle norme |
| 10 | **RICHIAMARE** | §4.2 — Pattern benchmark Cap. 3 come fondamento | Solo `\ref{}`, non ridescrivere |
| 11 | **EVITARE** | — | Ridescrivere sovranità digitale, CLOUD Act, architetture ibride in astratto |

---

*Fine del prompt operativo — `docs/prompt_capitolo4.md`*
*Generato il: 2026-05-17 | Commit cap. 3: `4cdea41` | Commit introduzione: `06748af`*
