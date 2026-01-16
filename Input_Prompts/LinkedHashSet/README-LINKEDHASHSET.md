*Questions about the graph:*

- key-value pairs? → **no**
- allow duplicate values? → **no**
- order is important? → **yes**
- sorted? → **by Insertion order**

*Domain*

- *simple:* gestione di un Cluster Job Scheduling. Il sistema deve gestire una coda di processi (job), ciascuno dotato di un ID univoco. E’ richiesto che i job vengano mantenuti in ordine di inserimento.
- *meddle:* swatch (campionario tessile). Costruire una palette che contenga ogni swatch al massimo una volta e preservi l’ordine di inserimento
- *difficult:* gestione di una waitlist. Implementare un sistema che memorizzi gli utenti in lista d’attesa, garantendo l’unicità di ogni utente e rispettando l’ordine di arrivo