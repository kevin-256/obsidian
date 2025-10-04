Tratti che contraddistinguono una base di dati da altro software:
- persistenza -> i dati esistono prima dell'interazione e dopo l'interazione da parte dell'utente
	- i dati non risiedono in memoria principale ma risiedono in memoria persistente nella memoria secondaria
- mole -> hanno senso quando si ha a che fare con grandi quantità di dati che non possono stare completamente in memoria principale, quindi il problema si sposta dal tempo di calcolo per ordinare i dati al fatto che devono essere spostati dalla memoria secondaria alla memoria centrale
- globalità -> problematiche che derivano da diversi utenti che ci accedono, permessi, accesso concorrente ai dati in modo da non introdurre inconsistenze e confliti

- l'interazione alla base di dati viene fatta tramite il modello logico, usando le tabelle e senza sapere come funziona sotto, del tipo non sappiamo che usa un algoritmo di ordinamento per ordinare i dati
- le operazioni devono essere fatte in tempi ragionevoli, i database usano delle strutture di indicizzazione e ottimizzazione delle interrogazioni
- efficacia(convenienza)

### Perché introdurre un Database e non usare il file system?
- usando il filesystem introdurremo sicuramente della ridondanza che può portare ad un'inconsistenza dei dati, a volte la ridondanza viene utilizzata nelle basi di dati nelle viste tipo e usando trigger per tenerle aggiornate
- difficoltà di accesso ai dati
- disomogeneità dei dati
- problemi di integritò dei dati
- non atomicità delle operazioni di accesso ai dati
- un accesso concorrente ai dati
- problemi di sicurezza/protezioni dei dati(non tutti possono vedere tutti e non tutti possono modificare tutto)

### Cos'è una base di dati?
I **dati** sono quelli nudi e crudi registrati nel sistema
Le **informazioni** sono le cose che vengono codificate tramite i dati e sono quelle che uno cerca quando interroga una base di dati

Un **DBMS** è una collezione di file interconnessi e insieme di programmi che consentono di accedere e modificare tali file. In pratica è un layer di astrazione che nasconde come vengono salvate le informazioni nei file e ci fornisce dei metodi per accedervi e modificarli.

Le basi di dati supportano astrazioni sui dati. I livelli di astrazione sono:
- livello fisico -> vede file e programmi che operano sui file
- livello logico/concettuale -> modello relazionale e modello entità-relazione
- livello delle viste -> (non è un livello di astrazione) sono dei ritagli della base di dati che possono essere dovuti a permessi

### Modello dei dati

Un **modello dei dati** è una collezione di strumenti per descrivere i dati, le loro relazioni e i vincoli di consistenza sui dati.