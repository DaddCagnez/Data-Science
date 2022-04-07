Laboratorio di Data Science for Business, svolto da:

734486 Marco Imperiale
732521 Davide Cagnetta
733433 Alessandro Ciapponi

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Per una migliore lettura del file README.md consigliamo di non limitarsi a visualizzare l'anteprima ma di aprirlo.

LABORATORIO 1: ANALYSIS AND PREPROCESSING

Scaricare la cartella denominata Analysis.zip
Assicurarsi di aggiungere i vari dataset in formato csv nella cartella Analysis, contenente il file Analysis.ipynb, il file PreAnalysis.ipynb e il file Labor_Market_Data_Cleaning.csv

Abbiamo utilizzato i seguenti Dataset:
1- https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-attivati/qbau-cyuc che contiene informazioni riguardanti rapporti di lavoro attivati
2- https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-cessati/nwz3-p6vm che contiene informazioni riguardanti rapporti di lavoro cessati
3- https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-prorogati/chng-cman che contiene informazioni riguardanti rapporti di lavoro prorogati
4- https://www.dati.lombardia.it/Attivit-Produttive/Rapporti-di-lavoro-trasformati/8dwx-jjag che contiene informazioni riguardanti rapporti di lavoro trasformati

Abbiamo preferito non inserire i dataset all'interno della cartella Analysis in quanto troppo pesanti.
Abbiamo inserito però il nostro dataset generato nalla fase di preprocessing, relativo all'unione e alla pulizia dei 4 dataset sopracitati. Tale file ci permette di far funzionare Analysis.ipynb senza dover runnare PreAnalysis.ipynb. Per il funzionamento di quest'ultimo file invece è necessario aggiungere i vari dataset.

LABORATORIO 2: DATA TRASFORMATION

Il file inerente a questa parte è Trasformation.ipynb, tale fail genererà il file Labor_Market_Data_Trasformation.csv.

Partendo dal dataset ottenuto in precedenza, abbiamo eliminando la colonna YEAR e abbiamo trasformato tutti i valori in dati numerici. Infine abbiamo inserito all'interno di un nuovo dataframe la matrice contenente i valori numerici pronti per la fase di ML.



