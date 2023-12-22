# Human Activity Recognition per l’identificazione del bullismo e cyberbullismo da smartphone

## Indice

1. [Introduzione](#1-introduzione)
2. [Struttura Progetto](#2-struttura-progetto)
3. [Eseguire il progetto su Google Colab](#3-eseguire-il-progetto-su-google-colab)
4. [Sviluppi Futuri](#4-sviluppi-futuri)

## 1. Introduzione
Il seguente progetto è un'implementazione di un esperimento di Human Activity Recognition condotto su studenti di primo anno di università e su studenti liceali di secondo anno in modo da identificare e riconoscere eventuali attività di bullismo svolte durante la compilazione di un questionario.

## 2. Struttura Progetto

Il progetto è strutturato nel seguente modo:

```
|––mmsa
|    |––Test1
|    |    |––1A
|    |    |    |––1A_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––1B
|    |    |    |––1B_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––1C
|    |    |    |––1C_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––1D
|    |    |    |––1D_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––csv_estratti
|    |    |––sensors
|    |––Test2
|    |    |––2A
|    |    |    |––2A_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––2B
|    |    |    |––2B_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––2C
|    |    |    |––2C_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––2D
|    |    |    |––2D_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––csv_estratti
|    |    |––sensors
|    |––Test3
|    |    |––3A
|    |    |    |––3A_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––3B
|    |    |    |––3B_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––3C
|    |    |    |––3C_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––3D
|    |    |    |––3D_tabella
|    |    |    |––completi
|    |    |    |––reso
|    |    |––csv_estratti
|    |    |––sensors
|    |––CNN_Bi_LSTM.ipynb
|    |––csv_finale.ipynb
|    |––LSTM.ipynb
|    |––media_tot.ipynb
|    |––T2_CNN.ipynb
|    |––T5_CNN.ipynb
|    |––README.md
|––dataset
|    |––DatasetUniba.csv
|    |––unimibshar.csv
```

Nel seguito si dettagliano i ruoli dei diversi componenti:

- **mmsa**: la cartella principale del progetto, in cui sono presenti tutti i classificatori testati e i dati relativi ad ogni test:
  - **Test1/2/3**: contiene dati grezzi estratti e dati elaborati per ogni test
    - **(1/2/3)(A/B/C/D)**: contiene i dati relativi al singolo test. I numeri 1, 2 e 3 identificano il test, le lettere A, B, C, D identificano il classificatore utilizzato per la predizione.
    - **csv_estratti**: contiene i csv estratti in seguito all'elaborazione dei dati grezzi
    - **sensors**: contiene i dati grezzi generati dai sensori dello smartphone durante la compilazione del questionario.
  - **media_tot.ipynb**: calcola le medie di attività svolte per ogni categoria (bullo, cyberbullo, ecc)
  - **extraction.ipynb** permette l'estrazione dei soli valori relativi all'accelerometro dai dati grezzi e salva il risultato in un CSV.
  - **classificatori**: i vari classificatori implementati (LSTM, Bi-LSTM, CNN);

## 3. Eseguire il progetto su Google Colab
Questo progetto è stato sviluppato e testato su Google Colab. Per eseguire il progetto, segui i seguenti passaggi:

1. Apri un file Jupyter Notebook (.ipynb) .
2. Assicurati di avere un account Google e accedi con le tue credenziali.
3. Nel notebook, esegui i vari blocchi di codice uno alla volta poichè dipendenti.
4. Alcuni blocchi potrebbero richiedere l'esecuzione di operazioni intensive o il caricamento di grandi quantità di dati.


## 4. Sviluppi Futuri

L'esperimento è stato effuato su un gruppo sperimentali di studenti di primo anno di università (circa 19 anni d'età) e su un secondo gruppo sperimentale di studenti liceali di secondo anno (circa 16 anni d'età).
In futuro si potrebbe provare a replicare l’esperimento su un altro gruppo sperimentale di utenti di un'età ben diversa per provare ad ottenere nuove informazioni, e capire altre correlazioni tra le categorie e le schermate del questionario.