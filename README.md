Laboratorio di Data Science for Business, svolto da:

734486 Marco Imperiale
732521 Davide Cagnetta
733433 Alessandro Ciapponi

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Per una migliore lettura del file README.md consigliamo di non limitarsi a visualizzare l'anteprima ma di aprirlo.

LABORATORIO 1: ANALYSIS AND PREPROCESSING

Scaricare la cartella denominata Analysis.zip
Assicurarsi di aggiungere i vari dataset in formato csv nella cartella Analysis, contenente il file Analysis.ipynb, il file PreAnalysis.ipynb e il file Labor_Market_Data_Cleaning.csv.

Abbiamo utilizzato i seguenti Dataset:
1- https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-attivati/qbau-cyuc che contiene informazioni riguardanti rapporti di lavoro attivati
2- https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-cessati/nwz3-p6vm che contiene informazioni riguardanti rapporti di lavoro cessati
3- https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-prorogati/chng-cman che contiene informazioni riguardanti rapporti di lavoro prorogati
4- https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-trasformati/8dwx-jjag che contiene informazioni riguardanti rapporti di lavoro trasformati

Abbiamo preferito non inserire i dataset all'interno della cartella Analysis in quanto troppo pesanti.
Abbiamo inserito però il nostro dataset generato nalla fase di preprocessing, relativo all'unione e alla pulizia dei 4 dataset sopracitati. Tale file ci permette di far funzionare Analysis.ipynb senza dover runnare PreAnalysis.ipynb. Per il funzionamento di quest'ultimo file invece è necessario aggiungere i vari dataset.

LABORATORIO 2: DATA TRASFORMATION

Il file inerente a questa parte è Transformations.ipynb.
Partendo dal dataset ottenuto in precedenza (Labor_Market_Data_Cleaning.csv), abbiamo eliminando la colonna YEAR e abbiamo trasformato tutti i valori in dati numerici.
Abbiamo prima di tutto ridotto ulteriormente il nostro dataframe prendedno in considerazione solo i valori per cui la feature PROVINCIAIMPRESA fosse uguale a MILANO o SONDRIO o VARESE, ovvero le sedi delle nostre abitazioni e del nostro ateneo. Per ridurre ulteriormente il numero di record abbiamo selezionato solamente quelli che avevano una nazione tra le prime cinque per numero di occorrenze e lo stesso ragionamento è stato fatto per la feature SETTOREECONOMICODETTAGLIO. Successivamente, al fine di implementare la matrice di previsione, abbiamo raggruppato diverse features, procedendo poi a classifcarle in base al valore contenuto.
Infine abbiamo inserito all'interno di un nuovo dataframe la matrice contenente i valori numerici pronti per la fase di ML e abbiamo trasformato il dataframe nel dataset Labor_Market_Data_Transforming.csv, disponibile nella nostra repository github.

LABORATORIO 3: MACHINE LEARNING

Il file inerente a questa parte è Machine_Learning.ipynb.
Partendo dal dataset ottenuto in precedenza (Labor_Market_Data_Transforming.csv), abbiamo proceduto con la linear regression tra "SCALETA" e "SCALETITOLO" e fra "SCALETA" e "SCALECONTRATTO".
Per entrambe le regressioni abbiamo anche calcolato i coefficienti di Pearson, Spearman e Kendall tau per calcolare la correlazione tra le due variabili e abbiamo calcolato anche il coefficiente di determinazione.
Abbiamo poi ridotto le dimensioni del nostro dataset oltre ad aver usato la PCA per poter eseguire al meglio la classificazione KNN.
Per quanto riguarda il K-means ci siamo concentrati su "SCALETITOLO", "SCALECONTRATTO", "SCALESETTORE" in relazione alle tre provincie considerate.
Al fine di verificare la correttezza dei modelli sono stati implementati dei grafici per illustrarne il funzionamento.


