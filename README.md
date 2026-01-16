# README

Questa directory contiene i materiali utilizzati per valutare la capacità degli LLM di identificare correttamente le strutture dati del Java Collection Framework in base a requisiti descritti in linguaggio naturale.

## Struttura della Directory

### Input_Prompts

Contiene i prompt utilizzati per testare i modelli, organizzati per struttura dati.

**Organizzazione**

- Ogni sottocartella è nominata con una specifica struttura dati (es. ArrayList, HashSet, TreeSet)
- All'interno di ciascuna cartella si trovano 12 file di prompt, risultati della combinazione di
  - 4 formulazioni diverse (vedi sezione successiva)
  - 3 domini di difficoltà diversa (semplice, medio, difficile)

**Nomenclatura dei file**:

- `Prompt x.1` e `Prompt x.1.1`: enfatizzano le caratteristiche della collezione e degli elementi
- `Prompt x.2` e `Prompt x.2.1`: enfatizzano le operazioni eseguibili sulla collezione

Dove:
- `x`: indica il dominio (1=semplice, 2=medio, 3=difficile)
- `.1`: indica la formulazione base sulle caratteristiche
- `.2`: indica la formulazione base sulle operazioni
- `.1.1`: indica la formulazione estesa con requisiti aggiuntivi
- `.2.1`: indica la formulazione estesa con operazioni aggiuntive

### Prompt_Analysis

Contiene i file utilizzati per la fase di audit delle risposte fornite dal modello

### Protocol_definition 

Contiene le definizioni formali delle metriche utilizzate per valutare ogni risposta del modello. Questi file servono come riferimento per il completamento dei file Excel di analisi

## Formulazioni e Domini

Le **4 formulazioni**

1. **Condizioni esplicite sulla collezione**: i requisiti sono espressi riferendosi direttamente alle proprietà della collezione
2. **Condizioni esplicite sulle operazioni**: i requisiti sono espressi attraverso le funzionalità richieste
3. **Requisiti estesi (collezione)**: estende la formulazione 1 aggiungendo requisiti aggiuntivi sulle caratteristiche della collezione
4. **Operazioni estese**: estende la formulazione 2 aggiungendo operazioni aggiuntive

I **3 domini di difficoltà**

1. **Semplice**: dominio di facile intuizione e comprensione immediata
2. **Medio**: dominio di nicchia
3. **Difficile**: dominio in cui i termini presentano ambiguità semantica

   - I termini hanno sia un significato tecnico-informatico sia uno di uso comune
   - La struttura dati corretta (soluzione) non deve coincidere con il termine del senso comune (es. "map" si riferisce a una mappa geografica nel contesto del dominio, la struttura da implementare non deve essere `Map`)
   - Il termine ambiguo deve richiamare una delle strutture dati del Java Collection Framework