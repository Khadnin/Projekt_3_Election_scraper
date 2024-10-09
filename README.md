
# Projekt_3_Election_scraper
Tento projekt slouží k extrahování výsledků z parlamentních voleb v roce 2006, 2013, 2017 a 2021 (ne 2010, nebo starších než 2006).

Odkaz k prohlédnutí najedete [zde](https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=14&xnumnuts=8104)

# Instalace knihoven

Knihovny potřebné pro chod kódu jsou uloženy v souboru requirements.txt. Pro instalaci je doporučeno použít nové virtuální prostředí a nainstalovat do něj 

```
pip3 --version                      # Oveření verze manažeru/instaleru
pip3 install -r requirements.txt    # Nainstaluje všechny potřebné knihovny
```

# Spuštění projektu

Spuštění souboru Projekt_3_Election_scraper v rámci příkazového řádku vyžaduje dva povinné argumenty.

```
Python Projekt_3_Election_scraper <odkaz-uzemniho-celku> <vysledny-soubor.csv>
```

Jestliže *<odkaz-uzemniho-celku>* obsahuje znak `&`, může se stát, že příkazový řádek nespustí skript správně. V takovémto případě jen zadejte odkaz-uzemniho-celku do uvozovek `"..."` případně do `'...'` - například `"odkaz-uzemniho-celku"`

Zároveň *<vysledny-soubor.csv>* je třeba zadat i s příponou `.csv`

V případě správného zadání se stáhnou výsledky do souboru s příponou `.csv`.

# Ukázka projektu

Výsledky hlasování pro okres Nový Jičín:

 - Argument 1: `https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=14&xnumnuts=8104`
 - Argument 2: `Vysledky_Novy_Jicin.csv`

Spuštění programu:

`python Projekt_3_Election_scraper "https://www.volby.cz/pls/ps2017nss/ps32?xjazyk=CZ&xkraj=14&xnumnuts=8104" Vysledky_Novy_Jicin.csv`

Průběh stahování:

```
Argumenty jsou správně zadané a mají správný formát.                                                                    
Zahajuji stahování a vytváření souboru

1 z 54 obcí scrapováno.                                                                                                 
2 z 54 obcí scrapováno.                                                                                                 
3 z 54 obcí scrapováno.
.
.
.
52 z 54 obcí scrapováno.                                                                                                
53 z 54 obcí scrapováno.                                                                                                
54 z 54 obcí scrapováno.                                                                                                                                                                                                                        

Soubor úspěšně vytvořen.                                                                                                                                                      

Hotovo. Script běžel: 10.39  s 
```

Částečný výstup:

```
code,location,registered,envelopes,valid,...
568741,Albrechtičky,559,357,355,36,0,1,23,1,12,23,3,2,1,2,1,39,0,1,22,106,0,1,47,0,1,0,0,33,0
599212,Bartošovice,1341,735,734,39,3,0,56,2,6,104,13,2,9,0,0,38,0,0,7,281,1,2,23,0,1,3,2,140,2
568481,Bernartice nad Odrou,779,547,542,70,1,0,25,1,18,21,12,2,4,1,6,47,0,1,11,163,0,0,110,0,6,0,0,43,0
...
```
