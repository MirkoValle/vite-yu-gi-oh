Descrizione:
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Al caricamento della pagina, effettuate una chiama ajax all'API di Yu Gi Oh: https://db.ygoprodeck.com/api/v7/cardinfo.php e con i dati restituiti, stampate una card per ogni carta.
ATTENZIONE:
l’api restituisce tutti i risultati in un colpo solo.
Per evitare attese e/o rallentamenti nelle richieste, potete diminuire il numero di risultati sfruttando i parametri num e offset
https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0
Bonus:
Creare un componente loader da visualizzare fintantoché i risultati non sono pronti.


Creo i componenti necessari per il layout.
Faccio una chiamata API che mi restituisce tutte le carte e le salvo in un array nello store.
Mostro le carte ricevute in pagina con le relative informazioni.
Creo un loader da visualizzare all'inizio come esempio di caricamento.

Creo un dropdown contenente tutti gli archetype disponibili
Aggiungo una chiamata API che mi restituisce l'archetype selezionato e lo mostro in pagina
