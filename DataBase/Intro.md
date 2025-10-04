Tratti che contraddistinguono una base di dati da altro software:
- persistenza -> i dati esistono prima dell'interazione e dopo l'interazione da parte dell'utente
	- i dati non risiedono in memoria principale ma risiedono in memoria persistente nella memoria secondaria
- mole -> hanno senso quando si ha a che fare con grandi quantità di dati che non possono stare completamente in memoria principale, quindi il problema si sposta dal tempo di calcolo per ordinare i dati al fatto che devono essere spostati dalla memoria secondaria alla memoria centrale
- globalità -> problematiche che derivano da diversi utenti che ci accedono, permessi, accesso concorrente ai dati in modo da non introdurre inconsistenze e confliti

- l'interazione alla base di dati viene fatta tramite il modello logico, usando le tabelle e senza sapere come funziona sotto, del tipo non sappiamo che usa un algoritmo di ordinamento per ordinare i dati
- le operazioni devono essere fatte in tempi ragionevoli, i database usano delle strutture di indicizzazione e ottimizzazione delle interrogazioni
- efficacia(convenienza)

### Perché introdurre un Database e non usare il file system?
