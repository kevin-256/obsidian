Grafo struttura formata da:
- nodi(Nodes) overtici(Vertex)
- linee o archi (Edges)
### Vertici (Nodes)
V = {v<sub>1</sub>,v<sub>2</sub>,v<sub>3</sub>,...v<sub>n</sub>,}
- Grafo del web:
	- nodi = pagine web
	- archi = link ipertestuali tra pagine
- grafo sociale di amicizie:
	- nodi = persone
	- archi = amicizie, conoscenze
Grandezza dell'insieme di vertici = |V|

### Archi (Edges)
E = {e<sub>1</sub>,e<sub>2</sub>,e<sub>3</sub>,...e<sub>n</sub>,}

### Grafo
G(V, E)

### Archi e grafi: diretti (directed) e indiretti (undirected)
grafi diretti: e(v<sub>2,</.sub>v<sub>1</sub>) e e(v<sub>1,</.sub>v<sub>2</sub>) indicano due archi diversi
grafi indiretti: e(v<sub>2,</.sub>v<sub>1</sub>) e e(v<sub>1,</.sub>v<sub>2</sub>) indicano lo stesso arco

### Grafi pesati
Gli archi hanno un peso
G(V, E, W)

### Sottografo (subgraph)
un grafo G'(V',E') è  un sottografo di G(V,E) se 
V'⊆ di V
E' ⊆ (V'xV') ∩ E

### Vicinato
il vicinato di un noto v
- in un grafo indiretto è l'insieme dei nodi collegati ad un nodo v tramite un arco
- dei grafi diretti:
	- vicini in ingresso
	- vicini in uscita
	- vicinato generico -> considero sia i nodi che entrano in v che quelli che escono da v

### Cammino
cammino: sequenza di archi tale che ogni arco è incidente allo stesso nodo del successivo
- diretto: solo seguendo la direzione degli archi
- indiretto: trascurando la direzione degli archi
Un cammino può avere una lunghezza data dal numero di archi o dal numero di nodi

### Connettività 
Due nodi sono connessi se c’è un cammino da uno all'altro
Un grafo è connesso se esiste un cammino fra ogni coppia di nodi 
 - indiretto: se esiste un cammino fra ogni coppia di nodi
 - diretto:
	 - fortemente connesso-> c’è un cammino diretto fra ogni copia di nodi
	 - debolmente connesso -> esiste un cammino indiretto fra ogni coppia di nodi (posso percorrere gli archi anche nel verso inverso)
Grafo disconnesso

### Componenti
Una componente di un grafo è un sottografo connesso e massimale(se aggiungo altri nodi, questi altri nodi rendono la componente non connessa)
- fortemente connessa: per ogni coppia di nodi u, v c’è un cammino diretto da u a v
- debolmente connessa: per ogni coppia di nodi u, v c’è un cammino **in**diretto da u a v
una componente fortemente connessa è allo stesso tempo debolmente connessa

### Grado
il grado di un nodo è  il numero di archi collegati a quel nodo
Nei grafi diretti
- in-degree -> archi che entrano nel nodo
- out-degree -> archi che escono nel nodo

### Sequenza dei Gradi
**Sequenza di gradi**, per ogni nodo, che grado ha
### Distribuzione dei Gradi (Degree Distribution)
**Degree distribution**, per ogni grado ci dice quanti nodi hanno quel grado
- "Distribuzione di frequenza dei gradi"
	- frequenza assoluta
	- frequenza relativa (nodi con quella frequenza diviso nodi totali,  la somma delle frequenze relative deve dare 1)


**Theorema**: La sommatoria dei gradi in un grado indiretto è due volte il numero degli archi
**Corollari**
- il numero di nodi con grado dispari è pari
- in ogni grafo diretto la somma degli in-degree è  uguale alla somma degli out-degree


### Grafico della degree distribution
- asse delle x rappresenta il grado
- asse delle y rappresenta la frazione(relativa) o il numero(assoluta) dei nodi che hanno quel grado
- spesso su scala log-log
- sui social media, di solito decrescente
	- tanti profili utente conn poche connessioni 
	- alcuni utenti con tante connessioni
