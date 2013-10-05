Parallel Web Spell Checker
==========================

'Parallel Web Spell Checker' este un crawler web care verifică ortografia paginilor vizitate.
Reprezintă un script shell și este bazat pe un exemplu de crawler web din manualul programului GNU parallel (https://www.gnu.org/software/parallel/man.html#example__breadth_first_parallel_web_crawler_mirrorer).

Configurare și rulare
---------------------

Pentru a rula script-ul este necesar ca următoarele programe să fie instalate în sistemul dumnevostră GNU/Linux:

* 'GNU parallel'; se instalează în Ubuntu folosind comenzile

```
    sudo apt-get install parallel
    sudo rm /etc/parallel/config
```
* 'Lynx'; se instalează în Ubuntu folosind comanda

```
sudo apt-get install lynx
```
* 'Aspell'; se instalează în Ubuntu folosind comanda

```
    sudo apt-get install aspell   
```
Nu uitați să instalți dicționarele corespunzătoare pentru aspell, de exemplu dicționarele românești (în Ubuntu) se instalează folosind comanda
``` 
    sudo apt-get install aspell-ro
```

### Configurare Aspell

Implicit aspell utilizează doar ortografia cu 'â/sunt', pentru a activea și cealaltă ortogarfie, cu '(î/sînt)', utilizată pe larg în Republica Moldova, este nevoie de a executa următoarea comandă (http://rospell.sourceforge.net/dictionary_ro.html#c4): 

```
    echo "master ro-classic" > ~/.aspell.conf
```


### Rularea script-ului
```
    ./pwspell http://gatt.org.yeslab.org/
```

Note
-----

Acest script primește 3 parametri:

1. `URL` - URL-ul de la care crawler-ul va începe pargurgerea;
2. `DEPTH` (opțional) - adîncimea maximală de parcurgere;
3. `SLANG` (opțional) - limba folosita la verificarea ortografiei.

