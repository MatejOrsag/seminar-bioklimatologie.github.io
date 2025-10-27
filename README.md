# Základní informace
- Můj kontaktní email je matej.orsag@mendelu.cz, najdete mě v kanceláři N5060 (snažme se ale maximum vyřešit osobně, ve cvičení)
- Na každé cvičení potřebuju notebook, MS Excel s __dokončenou prací z minulého cvičení__

## Jak dostanu zápočet
- Splním 2 úkoly:
  - Seminární práce z klimatologie
  - Docházka (můžu mít max. 2 absence, přičemž moje nulová aktivita ve cvičení může být považována za absenci, přestože nacvičení fyzicky jsem)   

## Co potřebuji pro práci ve cvičení
- Wi-Fi - ideálně EDUROAM ([ZDE najdu jak se připojit](https://eduroam.mendelu.cz/25350-navody-k-instalaci))
- MS Excel ([ZDE najdu jak ho získám](https://tech.mendelu.cz/25346-instalace-baliku-microsoft))

## Co mám dělat když něco nevím nebo nestíhám?
  - Ptám se na cvičení
  - Ptám se spolužáků
  - Ptám se Googlu nebo AI

# Zadání seminární práce
Cílem seminární práce je osvojit si základy práce s klimatologickými časovými řadami. V rámci práce budou využita volně dostupná pozorovaná data Českého hydrometeorologického ústavu (ČHMÚ). Data jsou k dispozici v denním či měsíčním časovém kroku.

Kromě práce s pozorovanými daty se rovněž seznámíme s klimatickými scénáři připravenými Ústavem výzkumu globální změny AV ČR, v. v. i. (CzechGlobe). Data budoucích klimatických podmínek jsou k dispozici [zde](https://www.climrisk.cz/mapa-cr/).

<details markdown="1">
<summary> Cvičení 01 </summary>

# Cvičení 01 (týden od 06.10.2025) - Zadání seminární práce z klimatologie, získání dat

- Cílem cvičení je vybrat si stanici se kterou budu v rámci semestru pracovat a získat výchozí data pro další práci
- __Na konci cvičení mám MS Excel soubor s měsíčními daty pro průměrné teploty vzduchu a sumy srážek pro mojí vybranou stanici__

## DŮLEŽITÉ ODKAZY ##
- Mapa stanic Českého hydrometeorologického ústavu: [Mapa stanic ZDE](https://www.chmi.cz/files/portal/docs/poboc/OS/stanice/ShowStations_CZ.html)
- Metadatový soubor pro vyhledání identifikátoru stanic: [Metadata ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/metadata/meta1.csv)
- Datový repozitář ČHMÚ: [Datový repozitář ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/)

## Postup získání dat ##

1. Pro práci ve cvičení a na seminární práci vytvořím nový MS Excel soubor, který pojmenuju jako __PrijmeniJmeno_Bioklimatologie.xlsx__ (uložím si ho, vím kde je, budu ho potřebovat každé cvičení)

2. Na mapě stanic vyberu stanici [Mapa stanic ZDE](https://www.chmi.cz/files/portal/docs/poboc/OS/stanice/ShowStations_CZ.html)
     - 2.1 V legendě vyberu stanice podle legendy (zkontroluju, jestli je zakliknuté "T" a "SRA", jako teplota a hledám stanici kde se obě veličiny měří = překrývá se v jejich ikonce čtvereček (teplota) a puntík (srážky)).
     - 2.2 Každý student ve skupině si vybere jinou stanici
     - 2.3 Zapamatuji (opíšu si) z mapy ID stanice (např. B2KUCH01) a jméno
     - 2.4 nevybírám si následující stanice (nedostatečná data - krátké časové řady)
          - _Žamberk_, _Třebařov_, _Ústí nad Orlicí_, _Jičín_, _Libice nad Doubravou_, _Šumperk_, _Kobylí_, _Hubenov_, _Praděd_, _Jeseník_, _Třeboň_, _Lednice_, _Protivanov_, _Třinec_, _Strážnice_

3. Stáhnu si z odkazu soubor s metadaty o stanicích [Metadata ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/metadata/meta1.csv)
     - 3.1 Otevřu metadatový soubor v MS Excel
     - 3.2 Vyhledám svoji vybranou stanici pomocí jména či ID stanice (__CTRL+F__)
     - 3.3 Ověřím že stanice měří kontinuálně od roku 1961, pokud ne, raději zvolím jinou
     - 3.4 Poznačím si interní kód stanice (sloupec A "WSI")
     - 3.5 Poznačím si souřadnice stanice (sloupce F "GEOGR1" a G "GEOGR2") a nadmořskou výšku (sloupec H "ELEVATION")

4. Vrátím se na stránky datového repozitáře [Datový repozitář ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/)
     - 4.1 Volím složku __monthly__
     - 4.2 Budeme pracovat se dvěma složkami - __temperature__ a __precipitation__ (postup bude stejný, začneme teplotou)
     - 4.3 Nyní využiji svůj interní kód stanice (_viz. bod 3.4_) a pomocí něj vyhledám příslušné soubory (__CTRL+F__)
     - 4.4 Zajímá nás pouze soubor označený "T" (Nezajímá nás: TMA, TMI, TMInoc, TPM) a ten stáhneme
     - 4.5 Zopakuji postup získání dat pro srážky
   
5. Příprava vstupních dat
     - 5.1 Otevřu stažený CSV soubor v MS Excel 
     - 5.2 Rozdělíme data do sloupců (POZOR NA HODNOTY! - Podívám se do sloupce "VALUE" jestli tam nevidím žádné římské číslice - Excel možná bude převádět vaše čísla na datumy, pokud jo, zavřu soubor a nejdříve upravím data dle bodu "Úprava dat" na konci zadání)
     - 5.3 U teploty nezapomenu vyfiltrovat pouze průměrné hodnoty ("AVG" - sloupce E a F): výsledkem jsou měsíční hodnoty průměrné teploty vzduchu ve všech letech dostupných pro moji stanici
     - 5.4 Data ze sloupců C ("YEAR"), D ("MONTH") a G ("VALUE") zkopíruji do připraveného Excelu (viz __Krok 1__) na první list
     - 5.5 Sloupec "VALUE" přejmenuji na TAVG
     - 5.6 Zopakuji postup pro srážky (hodnota "SUM" ze sloupce F "MDFUNCTION")

6. Bonus
     - 6.1 Z dat srážek a průměrných denních teplot si vytvořím jednoduchý spojnicový graf a podívám se na průběh hodnot v čase

Úprava dat (návod pro Windows):
- 1: najdu si pomocí průzkumníku souborů stažená data ve formátu csv
- 2: Pravým tlačítkem myši otevřu na souboru kontextovou nabídku a zvolím "Otevřít v aplikaci poznámkový blok"
- 3: Data se otevřou v poznámkovém bloku
- 4: Zmáčknu současně klávesy __CTRL__ a __H__ a otevře si mi nabídka "Najít a nahradit"
- 5: Nejdříve nahradím všechny symboly čárky (,) za symboly středník (;) a dám "Nahradit vše" (Všechny čárky v souboru by měly nyní být změněny na středníky
- 6: Pak opakuji postup a nahradím všechny symboly tečky (.) za symboly čárky (,)
- 7: Uložím soubor (klávesová zkratka __CTRL__ a __S__) a otevřu ho  aplikaci MS Excel - nyní by už mělo být vše v pořádku a pokračuju filtrováním dat (bod 5.3)

## Další zdroje:
  - (OS Windows) Klávesové zkratky a mapa znaků pro českou klávesnici: [ZDE](http://www.ceskaklavesnice.cz/zkratky) 
</details>

<details markdown="1">
<summary> Cvičení 02 </summary>
  
# Cvičení 02 (týden od 13.10.2025) - Radiace a teplota
- Cílem cvičení je vysvětlit si základní terminologii k tématu [slunečního záření (=solární radiace)](https://is.muni.cz/do/rect/el/estud/pedf/ps14/fyz_geogr/web/pages/03-prvky.html), pochopení vztahu radiace a teploty vzduchu a otestovat si možnosti získání dat z jiných zdrojů, než je ČHMÚ.
- __Na konci cvičení mám MS Excel soubor s novým listem kde srovnáme měsíční hodnoty solární radiace a teplot pro naši vybranou stanici__
  
## DŮLEŽITÉ ODKAZY ##
- [Copernicus](https://www.copernicus.eu/cs) je program Evropské unie pro pozorování Země, který poskytuje bezplatná a systematická data o naší planetě a jejím prostředí prostřednictvím šesti tematických služeb pro širokou škálu uživatelů. Tyto služby monitorují atmosféru, mořské prostředí, pevninu, klima, bezpečnost a krizové situace a poskytují informace pro rozhodování v oblasti politiky, vědy a pro širokou veřejnost, tedy i pro nás. My si odtud stáhneme data pro globální radiaci pro naši stanici.
- [Data k získání ZDE](https://ads.atmosphere.copernicus.eu/datasets/cams-solar-radiation-timeseries?tab=overview)

## Postup práce ve cvičení ##

1. Ve svém MS Excel souboru __PrijmeniJmeno_Bioklimatologie.xlsx__ vytvořím nový list a pojmenuji ho TeplotaRadiace.
 - 1.1 Do prvních 3 sloupců na novém listu nakopíruji data (CTRL+C, CTRL+V) ze sloupců obsahujících __rok, měsíc a hodnoty teploty vzduchu__ z listu s daty pro teplotu.
 - 1.2 Nechám si v listu pouze časovou řadu únor 2004 až prosinec 2024 (ve službě Copernicus jsou data až od února r. 2004) a zbytek mohu z tohoto listu smazat (__pozor, nesmažte si hodnoty z originálních dat teploty, které máte na listu _Teplota___).

2. Stahuji data pro solární radiaci ze služby Copernicus
 - 2.1 Na stránkách Copernicus [Data k získání ZDE](https://ads.atmosphere.copernicus.eu/datasets/cams-solar-radiation-timeseries?tab=overview) vyberu záložku __Download__ (MUSÍM SE REGISTROVAT MAILEM, díky čemuž budu moci službu využívat kdykoli v budoucnu)
 - 2.2 Vyplním formulář pro získání dat s pomocí následující nápovědy
 - 2.3 U výběru __Sky type__ volím __Both cloud-free and actual weather conditions__
 - 2.4 Zadám souřadnice mojí stanice (pokud jsem si minule neopsal souřadnice ze souboru meta1.csv, můžu tak učinit znovu, anebo si je najdu pomocí mapy.com). Na mapě mohu zkontrolovat že jsem souřadnice zadal správně a poloha puntíku cca odpovídá poloze mojí stanice. Pozn. pokud mě to zaujalo, mohu si analogicky stáhnout data radiace pro libovolný bod v rámci Evropy).
 - 2.5 Zadám nadmořskou výšku mojí stanice
 - 2.6 Jako rozpětí datumů zvolím __2004-02-01 až 2024-12-31__ (k dispozici jsou data od února r. 2004 do předvčerejška)
 - 2.7 U výběru __Time step__ volím __1 month__
 - 2.8 U výběru __Time reference__ volím __True solar time__
 - 2.9 U výběru __Data format__ volím __CSV__
 - 2.10 Potvrdím potřebné souhlasy a požádám o data klikem na __Submit form__- budeme pár minut čekat, než se pro nás data vygenerují a pak si je stáhneme

3. Práce se staženými daty solární radiace
 - 3.1 Stažený soubor otevřeme v programu MS EXCEL, pomocí kombinace kláves __CTRL__ a __H__ (nebo nástroje __Najít a nahradit__) najdeme čárky a nahradíme je středníky (;), dále nahradíme tečky za čárky, jako na prvním cvičení s daty z ČHMÚ.
 - 3.2 Použijeme trik s rozdělením dat do sloupců (Vyberu sloupec _A_ a na kartě _Data_ zvolím _Text do sloupců_), kde máme středník (__;__) jako oddělovač
 - 3.3 Prozkoumáme hlavičky souboru a co v nich vše můžeme vidět za informace
 - 3.4 Pro další postup budeme pracovat s hodnotami __Globální radiace__ označená jako __GHI__
 - 3.5 Vybereme hodnoty ze sloupce __GHI__ a __Observation period__ a nakopírujeme je na náš připravený list TeplotaRadiace v MS Excel (Zkontroluji, zda data mají stejný začátek a konec v čase a případně si to upravím tak, aby měla)

4. Porovnání dat měsíčních teplot a sum globální radiace
 - 4.1 Pro snadné vizuální porovnání hodnot vytvoříme spojnicový graf průběhu obou veličin v čase, na kterém si zároveň vyzkoušíme tvorbu kompletního grafu se všemi náležitostmi  
 - 4.2 Na listu TeplotaRadiace vybereme data pro měsíční teploty a globální radiaci
 - 4.3 Vložíme spojnicový graf (v Excelu záložka __Vložit__)
 - 4.4 Rozdělíme naše dvě veličiny na dvě osy - pomocí kontextové nabídky grafu (pravý klik myší) vyberu __Změnit typ grafu__ a vyberu z nabídky __Kombinovaný__
 - 4.5 Obě veličiny chceme zobrazit jako spojnicový graf, na sekundární osu přesuneme globální radiaci
 - 4.6 Kompletní graf je čitelný a obsahuje minimálně: Název, Legendu, Popisky os včetně jednotek, Uvedený zdroj/zdroje dat
</details>
  
<details markdown="1">
<summary> Cvičení 03 </summary>

# Cvičení 03 (týden od 20.10.2025) - Srovnání průměrných měsíčních teplot za dvě normálová období
  - Cílem cvičení je vytvořit grafy průměrných měsíčních teplot pro dva třicetileté klimatické normály a porovnat hodnoty v těchto obdobích.
- __Na konci cvičení mám MS Excel soubor s novým listem NormalyTeploty, kde srovnáme data průměrných teplot vzduchu v jednotlivých měsících v rámci dvou klimatických normálů 1961-1990 and 1991-2020, včetně grafického zobrazení__

## Postup práce ve cvičení ##
1. Ve svém MS Excel souboru __PrijmeniJmeno_AgroMeteo.xlsx__ vytvořím nový list a pojmenuji ho __NormalyTeploty__
   
2. Příprava dat a vytvoření kontingenční tabulky - teplota vzduchu
 - 2.1 Na nový list __NormalyTeploty__ nakopíruji data z listu __Teplota__, vyberu pouze časové úseky 1961-1990 a 1991 až 2020. Hodnoty pro první normál (rok, měsíc, teploty) nakopíruju od sloupce __A__, hodnoty pro druhý normál (rok, měsíc, teploty) od sloupce __E__
 - 2.2 Pokud mi chybí záhlaví (pojmenování sloupců) tak ho u obou normálů doplním
 - 2.3 Nyní vložíme tzv. kontingenční graf a kontingenční tabulku. Na záložce __Vložit__ vybereme __Kontingenční graf__ a následně možnost __Kontingenční graf a kontingenční tabulka__ (Na MacOS stačí jen __Kontingenční graf__ a pak už rovnou zadávám oblast dat)
 - 2.3 V nabídce __Vybrat tabulku nebo oblast__ vybereme sloupce __A, B, C (data normálu 1961-1990)__ a potvrdíme výběr
 - 2.4 Měla by se objevit plátna pro kontingenční tabulku a kontingenční graf (zatím prázdná)
 - 2.5 V nabídce __Pole kontingenčního grafu__ přeneseme (drag and drop) položku __Měsíc__ (nebo odpovídající název vašeho sloupce s označením měsíce) do boxu __Osa kategorie__
 - 2.6 Stejným způsobem přeneseme položku __Teplota__ do boxu __Hodnoty__
 - 2.7 U boxu __Hodnoty__ změníme v nabídce __Nastavení polí hodnot...__ funkci na __Průměr__ a potvrdíme
 - 2.8 Prohlédnu si vygenerovaný graf a vizuálně zhodnotím jestli dává smysl (např. jaké hodnoty jsou na osách X, Y, jestli vidím předpokládaný roční průběh teploty v jednotlivých měsících atd.). Pokud je vše OK, samotný graf můžu smazat.
 - 2.9 hodnoty z vygenerované kontingenční tabulky vyberu a pomocí __Vložit hodnoty__ je nakopíruju na volné místo na listu (doporučuju sloupec __I__). Původní kontingenční tabulku smažu
 - 2.10 Postup tvorby kontingenční tabulky zopakujeme pro druhé normálové období

3. Vytvoření jednoho spojnicového grafu pro porovnání obou normálových období
 - 3.1 Po vytvoření obou kontingenčních tabulek pro období 1961-1990 a 1991-2020 budeme zobrazovat obě řady měsíčních průměrných teplot v jednom spojnicovém grafu
 - 3.2 Vybereme vstupní data a pomocí __Vložit__, __Spojnicový graf__ vložíme graf který dále upravíme do podoby kompletního grafu
 - Přidáme název, popisy os, zdroj vstupních dat, jednotky, upravíme legendu tak aby byla čitelná

## Otázky k interpretaci dat a zamyšlení ##
1. Jaké pozorujete rozdíly a změny mezi dvěma srovnávanými obdobími?
2. Ve kterých měsících nového normálového období 1991-2020 se teplota oproti původnímu normálovému období 1961-2020 zvýšila nejvíce a ve kterých nejméně, nebo dokonce snížila?
3. Dochází k rovnoměrnému oteplení během roku, nebo je zřetelnější v určitých ročních obdobích?
4. Jsou některé měsíce, kde došlo dokonce k ochlazení?
5. Jaké dopady v krajině mohou tyto změny mít v jednotlivých ročních obdobích? (např. může mít nárůst teplot v zimě dopad na vegetační období, přezimování hmyzu či fenologii rostlin? Může oteplení jarních měsíců ovlivnit načasování rašení, kvetení či pěstování plodin? Co může znamenat vyšší letní teplota pro vodní bilanci, evapotranspiraci a sucho? Jak by tyto teplotní změny mohly ovlivnit bioklimatické indexy (např. sumy efektivních teplot)?

</details>
  
<details markdown="1"> 
<summary> Cvičení 04 </summary>

# Cvičení 04 (týden od 27.10.2025, úterý 28.10. státní svátek) - Změna klimatu - získání dat budoucího vývoje klimatu z portálu www.climRisk.cz
- Cílem cvičení je (pomocí dat z climrisk.cz) analyzovat předpokládaný budoucí vývoj klimatu pro naši stanici a porovnat jej s daty, získanými z historických (1961-2020) měření z ČHMÚ (stáhli jsme si v prvním cvičení).
- __Na konci cvičení mám MS Excel soubor s novým listem BudouciKlima kde srovnáme průměrné měsíční hodnoty normálových období 1961-1990 a 1991-2020 se získanými daty budoucího vývoje klimatu__
  
## DŮLEŽITÉ ODKAZY ##
- Tabulky podnebí: [ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf)
- Data budoucího vývoje klimatu: [Dostupná na portálu ClimRisk](https://www.climrisk.cz/)

## Postup práce ve cvičení ##
1. Příprava pracovního Excelu
     - 1.0 Vytvořím si dva nové listy a pojmenuji je __KlimatickyGradient__ a __BudouciKlima__

2. Popsání klimatického teplotního gradientu s pomocí Tabulek podnebí
     - 2.0 Otevřu si Tabulky podnebí buď [stáhnu pdf (50MB) ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf),  anebo si vezmu papírovou kopii.
     - 2.1 Pomocí mapy vyberu 10 stanic s rozdílnými nadmořskými výškami
     - 2.2 Opíšu si jména stanic a nadmořské výšky z __Abecedního seznamu klimatických stanic__
     - 2.3 Opíšu průměrné roční teploty (__Tabulka 1: Průměrná teplota vzduchu (°C) za období 1901-1950__)
     - 2.4 V MS Excel vytvořím bodový graf z dat teploty (svislá osa) a nadmořské výšky (vodorovná osa).
     - 2.5 Zobrazím spojnici trendu včetně funkce (klik pravým na bod v grafu a z nabídky vybrat "Přidat spojnici trendu", v pravo v nabídce zaškrtnu "Lineární" a dole "Zobrazit rovnici v grafu") a s pomocí zobrazené funkce ověřím míru teplotního gradientu v okolí mojí stanice.
     - 2.6 U grafu doplním veškeré náležitosti (Název, popisky os včetně jednotek, úplnou legendu, zdroj dat)
  
3. Získání ročních dat pro všechny časové agregace z portálu ClimRisk
     - 3.1 Otevřu portál [ClimRisk](https://www.climrisk.cz/)
     - 3.2 Vyberu __Česká Republika__
     - 3.3 V pravém menu vybereme jako parametr možnost __Průměrná teplota vzduchu__
     - 3.4 V horním menu stránky vyberu položku __Stahování dat__ a vyplníme formulář pro stažení hodnot
     - 3.5 Oblast: Česká republika, Podoblast: Okres ve kterém se nachází moje stanice, Region: Katastrální území mojí stanice (většinou stejné jako název obce)
     - 3.6 V nabídce Agregace vyberte pouze rok
     - 3.7 V nabídce Klimatická projekce vyberte __všechny dostupná období__
     - 3.8 V nabídce Scénář vyberte některou z možností __SSP126, SSP245, SSP370 nebo SSP585__
     - 3.9 V nabídce Klimatická charakteristika vyberte __Průměrná teplota vzduchu__ a  __Srážkový úhrn__
     - 3.10 V nabídce email zadejte vaši mailovou adresu a nechte si zaslat data
  
4. Práce se staženými daty a tvorba grafů
     - 4.1 Pro roční hodnoty časových agregací scénářů budoucího vývoje klimatu vytvořím spojnicový graf průběhu včetně mediánu a všech percentilů
  
5. Bonus: Získání měsíčních dat z portálu ClimRisk
     - 5.1 Otevřu portál [ClimRisk](https://www.climrisk.cz/)
     - 5.2 Vyberu __Česká Republika__
     - 5.3 V pravém menu vybereme jako parametr možnost __Průměrná teplota vzduchu__
     - 5.4 V horním menu stránky vyberu položku __Stahování dat__ a vyplníme formulář pro stažení hodnot
     - 5.5 Oblast: Česká republika, Podoblast: Okres ve kterém se nachází moje stanice, Region: Katastrální území mojí stanice (většinou stejné jako název obce)
     - 5.6 V nabídce Agregace vyberte všechny měsíce (leden-prosinec) a také rok
     - 5.7 V nabídce Klimatická projekce vyberte období __2035 (2021-2050)__ a __2065 (2051-2080)__
     - 5.8 V nabídce Scénář vyberte některou z možností __SSP126, SSP245, SSP370 nebo SSP585__
     - 5.9 V nabídce Klimatická charakteristika vyberte __Průměrná teplota vzduchu__ a  __Srážkový úhrn__
     - 5.10 V nabídce email zadejte vaši mailovou adresu a nechte si zaslat data
     - 5.11 Do grafu průměrných měsíčních teplot ve dvou normálových obdobích z minulého cvičení přidám data z budoucích normálových období 2035 (2021-2050)__ a __2065 (2051-2080)

</details>
  
<details markdown="1">
<summary> Cvičení 05 </summary>
# Cvičení 05 (týden od 03.11.2025) - Teplota vzduchu
</details>
  
<details markdown="1">
<summary> Cvičení 06 </summary>
# Cvičení 06 (týden od 10.11.2025) - Charakteristické dny
</details>
  
<details markdown="1">
<summary> Cvičení 07 </summary>
# Cvičení 07 (týden od 18.11.2025, pondělí 17.11. státní svátek) - Vlhkost vzduchu a výpar
</details>
  
<details markdown="1">
<summary> Cvičení 08 </summary>
# Cvičení 08 (24.11.2025) - Srážky
</details>
  
<details markdown="1">
<summary> Cvičení 09 </summary>
# Cvičení 09 (01.12.2025) - Sucho
</details>
  
<details markdown="1">
<summary> Cvičení 10 </summary>
# Cvičení 10 (08.12.2025) - Tlak a vítr
</details>
  
<details markdown="1">
<summary> Cvičení 11 </summary>
# Cvičení 11 (15.12.2025) - Kontrola seminárních prací a zápočty
</details>


