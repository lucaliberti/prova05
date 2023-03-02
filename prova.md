# mylib.h

## Autore : Luca Liberti 

## Descrizione
Mylib sui pone lo scopo di omogeneizzare le configurazioni/include da specificare sui vari sistemi Windows/Apple/Linux.
Per utilizzarla basta includerla nel seguente modo:

 \#include "mylib.h"

automaticamente vengono effettuate le impostazioni per 
* gestire le stringhe (indipendentemente dal sistema operativo utilizzato)
* è possibile utilizzare il generatore di numeri casuali senza includere nulla di ulteriore
* utilizzare la funzione Sleep() senza includere null'altro
* gestione dell'ora (indipendentemente dal sistema operativo utilizzato)

## Gestione delle stringhe
E' possibile utilizzare "string", indipendentemente dal sistema operativo utilizzato. 
Inoltre sono disponibilile le seguenti funzioni aggiuntive:
- string intToString ( int n );       // Converte da int a stringa
- string floatToString ( float f );   // Converte da float a stringa
- string boolToString ( bool b );     // Converte da float a stringa
    

## Generatore Numeri Casuali
Esempio:
> srand(time(NULL));  // inizializazione del generatore pseudocasuale (basta farlo solo una volta)
> 
> int rnd=rand()%10;  // numero compreso tra [0 ... 9] 

## Utilizzare la funzione Sleep()
E' possibile utilizzare la funzione Sleep() indipendentemente dalla piattaforma utilizzate 
> Sleep(1000); // pausa per 1000 msecs==1 sec


## Gestione dell'orario
gestione dell'ora (indipendentemente dal sistema operativo utilizzato)
- time_t getCuttenTime();             // restituisce data e ora in formato grezzo
- string getCurrentHour(time_t t);    // restituisce la stringa HH:MM:SS (ex. 14:30:45)
- string getCurrentDate(time_t t);    // restituisce la stringa gg-mm-aa (ex. 28-02-2023)

