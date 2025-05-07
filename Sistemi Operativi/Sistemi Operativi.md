## Introduzione
Un **sistema operativo** è un insieme di programmi che operano sull'hardware di un **sistema di calcolo**.
**Sistema di calcolo**:
- dispositivi fisici (hardware)
- sistema operativo
- programmi di sistema (fornisce un'interfaccia verso l'hardware)
- programmi applicativi (applicazioni che risolvono problemi specifici)
- utenti (qualsiasi agente che usa il sistema di calcolo per risolvere un problema)

##### Sistema Operativo
- Programma che permette di eseguire i programmi utente
- Gestisce le risorse agli utilizzatori
- sempre in esecuzione nel sistema di calcolo
- viene chiamato Kernel

#### Hardware
La CPU e i device controller possono concorrere per l'utilizzo del bus e per l'accesso alla memoria tramite il bus.
Un device controller gestisce uno specifico device e usa un buffer locale per leggere e scrivere i dati che poi serviranno alla CPU. La sincronizzazione per l'utilizzo del buffer avviene tramite gli **interrupts**.
##### Interrupts
il segnale di interrupt viene inviato dal controller -> la CPU intercetta il segnale e determina il tipo di interrupt ->la CPU invoca la procedura di servizio associata all'interrupt -> lo stato della CPU viene salvato e ripreistinato al termine della procedura
normalmente si utilizza un vettore delle interruzioni

##### Memoria
Divisa in due parti:
- **Memoria Principale** (Random Access Memory), unica memoria di grandi dimensioni accessibile dalla CPU, **Volatile**
- **Memoria Secondaria** (Nastri, dischi, flash), compensa le limitazioni della memoria principale
###### Gerarchia della memoria
```
  (Faster)
  Registers
	  |
    Cache
	  |
 Main Memory
	  |
Electronic Disks
	  |
 Magnetic Disks
	  |
 Optical Disks
	  |
 Magnetic Tapes
   (Slower)
```

##### DMA (Direct Memory Access)
Le operazioni di accesso alla memoria da parte dei dispositivi di I/O vengono eseguite senza la CPU, ovvero il DMA controller ha il compito di trasferire i dati dal buffer del dispositivo I/O alla memoria centrale e viceversa. Al termine del trasferimento la CPU viene notificata dal DMA controller. Questa tecnica aumenta le prestazioni perché la CPU continua a lavorare durante il trasferimento dei dati.

#### Sistema Operativo
###### Sistemo operativio Monogrammato
Oltre al Sistema Operativo in memoria risiede al più un programma, quindi il sitema esegue un lavoro alla volta ed il sistema operativo deve solamente gestire il trasferimento da un job al sucessivo.

###### Sistemo operativio Multiprogrammato
In memoria riesiedono **contemporaneamente** più programmi da eseguire, il sistema operativo può eseguire un altro job mentre quello che era in esecuzione termina oppure si mette in attesa di un evento "esterno" ad esempio I/O.

##### Time Sharing
Tecnica utilizzata dai sistemi operativi multiprogrammati:
- i context switch tra job avvengono ad intervalli prestabiliti, non necessariamente in corrispondenza di operazioni di I/O
- il tempo della CPU è suddivisa tra più job
- i context switch fanno credere all'utente di utilizzare un sistema di calcolo dedicato solamente a lui
Consideriamo tre job P1, P2 e P3 che utilizzano sia la CPU ma eseguono anche operazioni di I/O.

![](Images/ExecutionTypes.png)
#### Processo
Un **processo** è un'attività unitaria di elaborazione, caratterizzata da un singolo **flusso sequenziale di esecuzione**, uno **stato corrente** ed una collezione di **risorse** assegnate dal sistema.

- ogni utente può avere anche più di un job contemporaneamente in memoria centrale
- quando la memoria centrale non è sufficiente, alcuni processi vengono spostati sulla memoria di massa:
	- job pool, contenente processi che stanno eseguendo e i processi pronti all'esecuzione, ogni processo è visto come un blocco unico (non più utilizzata)
	- swap, contentente parti di processi non più utilizzate chiamate pagine, ogni processo è suddiviso in pagine e alcune possono stare in memoria centrale e alcune in memoria di massa
- Il sistema operativo sceglie quali processi caricare in memoria centrale (**job scheduling**)
- il sistema operativo sceglie quale processo eseguire in memoria centrale (**CPU scheduling**)

**processo** è un'entità del Sistema Operativo, un processo è l'istanza di un programma in esecuzione ed è l'unità minima di misura per le risorse,
ogni processo consiste della sua imamgine, contesto di esecuzione, memoria, files...; etimológicamente un processo è l'insieme degli step che il processore deve eseguire. Il processo consiste in uno o più threads che è l'unità di misura dello scheduler.

**job** è un'entità ad alto livello composta da più tasks, al giorno d'oggi job è un insieme di processi, mentre task indica un processo, un thread oppure un unità di lavoro eseguito dal processo o da un thread.

**Virtual Memory (Paging)** è un layer di astrazione fornito ad ogni processo, ad esempio se il sistema ha 2GB di RAM fisica con indirizzi da 0 a 2GB, un processo potrebbe vedere uno spazio di indirizzamento di 4GB tutto per lui. La gestione degli indirizzi da virtuali a fisici è gestita dal MMU(Memory Management Unit) che è gestita dal sistema operativo, suddivisa in pagine di una dimensione prefissata.

**Swapping** è il processo di spostare le pagine, dalla memoria centrale alla memoria di massa in un'area chiamata area di swap


##### Modalità di funzionamento
In presenza di più processi che condividono risorse è necessario che ogni processo non danneggi gli altri.
Con questo proposito vengono introdotte due modalità di funzionamento, **user mode** e **kernel mode**
