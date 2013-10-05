Parallel Web Spell Checker
==========================

This script is a breadth first crawler that checks the spelling of a website. 
It is based on the example of 'Breadth first parallel web crawler/mirrorer' from GNU parallel's man page (https://www.gnu.org/software/parallel/man.html#example__breadth_first_parallel_web_crawler_mirrorer).

Although 'pwspell' can do what is written above it must be seen not as a functional web crawler, but as a 'proof of concept' and an shell script exercise.

Quick start
-----------

You need the following programs to be installed on your GNU/Linux system in order to be possible to run the script:

1. 'GNU parallel', install it on Ubuntu using

```
    sudo apt-get install parallel
    sudo rm /etc/parallel/config
```
2. 'Lynx', install it on Ubuntu using

```
    sudo apt-get install lynx
```
3. 'Aspell', install it on Ubuntu using

```
    sudo apt-get install aspell   
```
Do not forget to install the language files for aspell, e.g. romanian language files are installed (in Ubuntu) using

``` 
    sudo apt-get install aspell-ro
```

### Run the script

```
    ./pwspell http://gatt.org.yeslab.org/
```

Notes
-----

The script may take 3 arguments:

1. `URL` - the start (seed) URL for the crawler;

2. `DEPTH` - the maximum depth of crawling;

3. `SLANG` - the language to use for spelling checking.
