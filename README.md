
# Progetto-ICON

# 1 Snake
Questo progetto si basa sul classico gioco degli anni settanta. 
Realizzato in linguaggio Python e utilizzando l'interfaccia grafica della libreria tkinter, il gioco viene realizzato implementando una tecnologia di intelligenza artificiale nota come Deep Neural Network.

# 2 Deep Neural Network (DNN)
Una **rete neurale** (in inglese **Neural Network**) è un modello computazionale composto di "neuroni" artificiali. I suddetti neuroni ricevono in input dei dati, li elaborano e comunicano il dato elaborato al nodo successivo. Si può pensare che se due neuroni comunicano fra loro utilizzando maggiormente alcune connessioni allora tali connessioni avranno un **peso** maggiore, fino a che non si creeranno delle connessioni tra l'ingresso e l'uscita della rete che sfruttano "percorsi preferenziali" creando delle reti. La rete non produce tuttavia un unico percorso ma ne produce svariati con pesi differenti.
Una Neural Network è composta da diversi strati, detti **layer**:

 - layer di ingresso (**input layer**)
 - layer intermedio (**hidden layer**)
 - layer di output (**output layer**)

Il passaggio da un layer al successivo avviene attraverso l'esecuzione di una funzione lineare che moltiplica il valore in input con il **peso** della connessione tra il layer di partenza e il laser di arrivo.
Una Neural Network che presenta più hidden layer è detta **Deep Neural Network**.
In particolare, l'algoritmo implementato per questo progetto presenta due hidden layer.

# 3 Algoritmo
Data una popolazione di brains (neuroni), ognuno di essi giocherà una partita (num_trails = 1 ) e totalizzerà un punteggio in base a quanto bene giocherà. Di questa popolazione (pop_size = 100), il 25% col punteggio più alto verrà replicato nella generazione successiva e di questi ne verrà fatta una copia mutata seguendo la funzione **mutate (self, brain)**. Il resto dei brain verrà prodotto randomicamente fino a riempire il vettore della popolazione. Questa procedura verrà iterata per un numero di volte prestabilite (num_generation) e l'output sarà dato dal 25% migliore dell'ultima generazione che verrà mostrato a schermo.

![Algoritmo](https://github.com/aleSant10/Progetto-ICON/blob/main/Algoritmo.png)

# 4. Considerazioni al variare dei dati di input

## Fattori rilevanti nella generazione della popolazione

 - **mutation_chance** : la probabilità che una mutazione venga introdotta nella creazione della nuova generazione 
 - **mutation_size** : il 'peso' della mutazione

![Tabella](https://github.com/aleSant10/Progetto-ICON/blob/main/Tabella.png)

In caso di avvenuta mutazione, i risultati possono variare: quindi non si possono considerare stabili questi valori e trarne una valutazione universale. 
Questi valori sono stati ottenuti con i seguenti valori fissi:

 - **pop_size** = 100
 - **num_generations** = 100 
 - **num_trails** = 1 
 - **window_size** = 7
 - **hidden_size** = 15
 - **board_size** = 10

