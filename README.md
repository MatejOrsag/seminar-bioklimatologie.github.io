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
     - 5.11 Do grafu průměrných měsíčních teplot ve dvou normálových obdobích z minulého cvičení přidám data z budoucích normálových období __2035 (2021-2050)__ a __2065 (2051-2080)__

</details>
  
<details markdown="1">
<summary> Cvičení 05 </summary>
# Cvičení 05 (týden od 03.11.2025) - Analýza měsíčních teplot vzduchu jejich trendů po dekádách (1961–2020)
  
Cílem cvičení je zjistit, o kolik stupňů se změnila průměrná měsíční teplota za jednotlivé dekády mezi lety 1961–2020 a vytvořit graf, který ukáže trendy (změnu) mezi jednotlivými dekádami.

## Postup práce ve cvičení ##
1. Příprava pracovního Excelu
     - 1.0 Vytvořím si nový list a pojmenuji ho __TeplotyDekadyTrendy__
     - 1.1 Z prvního listu svého pracovního excelu nakopíruju do nového listu TeplotyDekadyTrendy vedle sebe do sloupce A Rok a do sloupce B Měsíční teploty vzduchu 1961-2020.
2. Vytvoř pomocný sloupec „Dekáda“
     - 2.1 Do sloupce C napíšu do buňky C2 vzorec: =ROUNDDOWN(A2/10,0)*10  Tento vzorec zaokrouhlí rok na začátek dekády (např. 1961–1969 → 1960, 1970–1979 → 1970). Pokud mám jako desetinný oddělovač čárku, tak do vzorce místo čárky dám středník, jinak nebude fungovat.
     - 2.2 Zkopíruju vzorec až dolů tak, že buňku se vzorcem chytnu levým dlouhým klikem za pravý dolní roh buňky a stáhnu=zkopíruju vzorec dolů až na konec dat.
3. Spočítám průměrnou teplotu za dekádu
   - 3.1 Označím data (sloupce „Dekáda“ a „Teplota“) a na kartě Vložení → Kontingenční graf a kontingenční tabulka. Umístím ji na nový list.
   - 3.2 V nabídce Pole kontingenčního grafu přeneseme (drag and drop) položku Dekáda do boxu Osa kategorie a stejným způsobem přeneseme položku Teplota do boxu Hodnoty.
   - 3.3 U boxu Hodnoty změníme v nabídce Nastavení polí hodnot… funkci ze Sumy na Průměr a potvrdíme.
   - 3.4 Prohlédnu si vygenerovaný graf a vizuálně zhodnotím jestli dává smysl (např. jaké hodnoty jsou na osách X, Y, jestli vidím předpokládaný roční průměrné teploty v jednotlivých dekádách atd.).
   - 3.5 Hodnoty z vygenerované kontingenční tabulky (jen údaje pro dekády 1960-2010, tzn. šest řádků a čísly) označím, pomocí CTRL+C zkopíruju a pomocí pravý klik a "Vložit jen hodnoty" je nakopíruju na volné místo v listu __TeplotyDekadyTrendy__. 
4. Vypočítej změnu teploty mezi dekádami
   - 4.1 Vedle zkopírované tabulky se sloupcem Dekády a průměrnou teplotou vzduchu za dekádu si vytvořím další sloupec s nadpisem rozdíl (°C), kde odečtu teploty jedné dekády od té předcházející. Tzn. Napíšu vzorec např.: =B3-B2 (kde B2 a B3 jsou průměrné teploty dvou po sobě jdoucích dekád). Tím zjistím, o desetin kolik °C se průměrná teplota zvýšila nebo snížila mezi dvěma dekádama.
   - 4.2 Zkopíruj vzorec dolů (viz bod 2.2)
   - 4.3 Do nového sloupce přidej název „Změna (°C / dekáda)“
5. Vytvoř spojnicový graf s daty měsíčních teplot pro celé období 1961-2020, ze kterého následně pomocí budeš s pomocí filtru zobrazovat každou dekádu zvlášť.
   - 5.1 Nejdříve si udělej prostor na graf, vlož nad první řádek cca 15 nových prázdných (pravý klik na jedničku v prvním řádku, klik na "vložit buňky" a zmáčknutím "F4" na klávesnici akci zopakujete 15x = vložíte 15 řádků). Graf má být úplně nahoře, data (Rok, Teplota, atd.) až pod tím, protože se nám obsah pod filtrem bude při filtrování měnit a graf by nám mizel. Doplň do grafu popisky os s jednotkami a legendu, ať je ten graf kompletní a finální.
   - 5.2 Přidej ještě do grafu spojnici trendu: Pravý klik na data v grafu → „Přidat spojnici trendu“. V nabídce vpravo vyberu „lineární“ a dole zaškrtni zobrazit rovnici spojnice trendu.
   - 5.3 V grafu se mi objeví rovnice trendu ve tvaru:
     y=ax+b , kde číslo "a" mi udává sklon (slope), což je v našem případě průměrná změna teploty za jeden časový interval. Ze sklonu křivky dalším kroku spočítám trend změny teploty za vybrané období.
   - 5.4 Ale nejdřív si postupně vyfiltruju (zobrazím) každou dekádu zvlášť. Označ celý sloupec "Rok" a v záložce Data zapni pro tento sloupec funkci Filtr, který ti umožní zobrazit jen vybraný časový rozsah (např. dekáda 1961-1970) → kliknu na ikonku Filtru ve sloupci s rokem, zvolím "Filtry čisel" a z nabídky vpravo vyberu "Mezi". Filtruj mezi hodnotami „>=1961“ a „<=1970“ (aby bylo jasné, že jde o obě hranice včetně).
   - 5.5 Tím se časový rozsah grafu upraví na požadovanou dekádu a stejně tak se změní rovnice se sklonem.
   - 5.6 Přepočítám změnu (trend) teploty za dekádu. Naše osa x v měsících, takže číslo sklonu "a" je změna teploty vzduchu ve °C za rok. Změna za dekádu je pak 120×a, protože 12 měsíců × 10 let = 120.
   - 5.7 Zkontroluji ještě jednou, jestli tam mám popisky os, přepíšu název grafu jej podle dekády, kterou zobrazuje, označím jej a zkopíruji jako obrázek (karta Domů, vlevo nahoře kopírovat jako obrázek) a vložím pomocí CTRL+V do listu TeplotyDekadyTrendy.
   - 5.8 Postup zopakuji pro každou dekádu zvlášť (1961-1970, 1971-1980, ...) až po poslední dekádu 2010-2020. Takže budu mít na konci 6 grafů pro 6 dekád.
7. Zamyšlení
   „Jak se průměrná teplota měnila po dekádách?“
   „Ve které dekádě byl nejrychlejší nárůst?“
   „Jaká je průměrná změna za dekádu?“
</details>
  
<details markdown="1">
<summary> Cvičení 06 </summary>
# Cvičení 06 (týden od 10.11.2025) - Srážky
  
- Cílem cvičení je prověřit předpokládaný budoucí vývoj klimatu pro naši stanici a jejich srovnání s daty získanými z historických měření ČHMÚ
- __Na konci cvičení mám MS Excel soubor s novými listy NormalySrazky a DnySnih3cm, kde srovnáme data srážkových úhrnů v jednotlivých měsících v rámci dvou klimatických normálů 1961-1990 and 1991-2020, včetně grafického zobrazení a počet dní se sněhovou pokrývkou nad 3 cm v současném a budoucím klimatu__

## DŮLEŽITÉ ODKAZY ##
- Data budoucího vývoje klimatu: [Dostupná na portálu ClimRisk](https://www.climrisk.cz/)

## Postup práce ve cvičení ##
1. Ve svém MS Excel souboru __PrijmeniJmeno_AgroMeteo.xlsx__ vytvořím dva nové listy a pojmenuji je __NormalySrazky__ a __DnySnih3cm__

2. Příprava dat a vytvoření kontingenční tabulky - srážky
     - 2.1 Na nový list __NormalySrazky__ nakopíruji data z listu __Srazky__, vyberu pouze časové úseky 1961-1990 a 1991 až 2020. Hodnoty pro první normál (rok, měsíc, srážky) nakopíruju od sloupce __A__, hodnoty pro druhý normál (rok, měsíc, srážky) od sloupce __E__
     - 2.2 Pokud mi chybí záhlaví (pojmenování sloupců) tak ho u obou normálů doplním (__ROK, MĚSÍC, SUMA SRÁŽEK__)
     - 2.3 Nyní vložíme tzv. kontingenční graf a kontingenční tabulku. Na záložce __Vložit__ vybereme __Kontingenční graf__ a následně možnost __Kontingenční graf a kontingenční tabulka__ (Na MacOS stačí jen __Kontingenční graf__ a pak už rovnou zadávám oblast dat)
     - 2.3 V nabídce __Vybrat tabulku nebo oblast__ vybereme sloupce __A, B, C (data normálu 1961-1990)__ a potvrdíme výběr
     - 2.4 Měla by se objevit plátna pro kontingenční tabulku a kontingenční graf (zatím prázdná)
     - 2.5 V nabídce __Pole kontingenčního grafu__ přeneseme (drag and drop) položku __Měsíc__ (nebo odpovídající název vašeho sloupce s označením měsíce) do boxu __Osa kategorie__
     - 2.6 Stejným způsobem přeneseme položku __Srážky__ do boxu __Hodnoty__
     - 2.7 U boxu __Hodnoty__ změníme v nabídce __Nastavení polí hodnot...__ funkci na __Průměr__ a potvrdíme
     - 2.8 Prohlédnu si vygenerovaný graf a vizuálně zhodnotím jestli dává smysl (např. jaké hodnoty jsou na osách X, Y, jestli vidím předpokládaný roční průběh teploty v jednotlivých měsících atd.). Pokud je vše OK, samotný graf můžu smazat.
     - 2.9 hodnoty z vygenerované kontingenční tabulky vyberu a pomocí __Vložit hodnoty__ je nakopíruju na volné místo na listu (doporučuju sloupec __I__). Původní kontingenční tabulku smažu
     - 2.10 Postup tvorby kontingenční tabulky zopakujeme pro druhé normálové období

3. Vytvoření jednoho kombinovaného sloupcového grafu pro porovnání obou normálových období
     - 3.1 Po vytvoření obou kontingenčních tabulek pro období 1961-1990 a 1991-2020 budeme zobrazovat obě řady měsíčních sum srážek v jednom společném sloupcovém grafu
     - 3.2 Vybereme vstupní data a pomocí __Vložit__, __Sloupcový graf__ vložíme graf který dále upravíme do podoby kompletního grafu
     - Přidáme název, popisy os, zdroj vstupních dat, jednotky, upravíme legendu tak aby byla čitelná
  
4. Stažení dat pro sněhovou pokrývku nad 3 cm z portálu ClimRisk
     - 4.1 Otevřu portál [ClimRisk](https://www.climrisk.cz/)
     - 4.2 Vyberu __Česká Republika__
     - 4.3 V horním menu stránky vyberu položku __Stahování dat__ a vyplníme formulář pro stažení hodnot
     - 4.4 Oblast: Česká republika, Podoblast: Okres ve kterém se nachází moje stanice, Region: Katastrální území mojí stanice (většinou stejné jako název obce)
     - 4.5 V nabídce Agregace zatrhněte všechny měsíce leden-prosinec a rok
     - 4.6 V nabídce Klimatická projekce vyberte __1995 (1981-2010), 2005 (1991-2020), 2035 (2021-2050), 2065 (2051-2080)__
     - 4.7 V nabídce Scénář vyberte některou z možností __SSP126, SSP245, SSP370 nebo SSP585__
     - 4.8 V nabídce Klimatická charakteristika vyberte __Počet dní se sněhovou pokrývkou nad 3 cm__
     - 4.9 V nabídce email zadejte vaši mailovou adresu a nechte si zaslat data
       
5. Zpracování dat sněhové pokrývky
     - 5.1 Na nový list __DnySnih3cm__ nakopíruji data stažená z portálu ClimRisk
     - 5.2 Data nakopíruju do sloupců vedle sebe, pojmenovaných podle jednotlivých normálů, použiji pouze číslo měsíce a počet dní se sněhovou pokrývkou v daném měsíci a za celý rok, zbývající data z listu ClimRisk smažu
     - 5.3 Všechny stažené datové sady pro normálový období porovnám pomocí sloupcového grafu, kde pro každý měsíc mám čtyři sloupce (pro každé normálové období jeden).
       
## Otázky k interpretaci dat ##
1. Jaké pozorujeme rozdíly ve srážkových úhrnech mezi dvěma historickými normály?
2. Jak souvisí tyto změny s již posouzenými změnami teplot a změnami v zaznamenané a očekávané sněhové pokrývce?
3. Jaké mohou tyto změny mít dopady v krajině v jednotlivých ročních obdobích?
4. Pokud srovnáte výsledky na vaši stanici a výsledky některého z kolegů, jaké pozorujete rozdíly?

</details>
  
<details markdown="1">
<summary> Cvičení 07 </summary>
# Cvičení 07 (týden od 18.11.2025, pondělí 17.11. státní svátek) - Vlhkost vzduchu a výpar
  - Cílem cvičení je probrat vlkostní charakteristiky a ověřit srážkový gradient na vybraných stanicích
- __Na konci cvičení mám MS Excel soubor s novým listem SrazkovyGradient s opsanými daty pro vybrané stanice a vykresleným grafem gradientu__

## DŮLEŽITÉ ODKAZY ##
- Tabulky podnebí: [ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf)

1. Popsání srážkového gradientu s pomocí Tabulek podnebí
     - 1.0 Otevřu si Tabulky podnebí buď [ZDE](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf) nebo si vezmu papírovou kopii
     - 1.1 Opíšu si jména stanic a nadmořské výšky 10 stanic z __Abecedního seznamu srážkoměrných stanic__ (téměř na konci tabulek, před tabulkou č. 52) na list __SrazkovyGradient__ ve svém pracovním excelu
     - 1.2 Nalistuji téměř na konci __Tabulku č. 52: Průměrný úhrn srážek (mm) za období 1901-1950__
     - 1.3 Opíšu průměrné roční srážkové úhrny
     - 1.4 V MS Excel vytvořím bodový graf z dat srážek a nadmořské výšky
     - 1.5 Zobrazím spojnici trendu včetně funkce a s pomocí zobrazené funkce ověřím míru teplotního gradientu u mojí stanice
     - 1.6 U grafu doplním veškeré náležitosti (Název, popisky os včetně jednotek, úplnou legendu, zdroj dat)

</details>
  
<details markdown="1">
<summary> Cvičení 08 </summary>
# Cvičení 08 (týden od 24.11.2025) - Tlak a vítr
- Cílem cvičení je získat a zpracovat data směru větru pro námi vybranou stanici a vytvořit větrnou růžici
- __Na konci cvičení mám MS Excel soubor s novým listem SmerVetru s denními daty směru větru pro moji stanici a hotový graf větrné růžice__

## DŮLEŽITÉ ODKAZY ##
- Denní data směru větru pro naši stanici z repozitáře ČHMÚ [ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/daily/wind/)

1. Stažení denních dat směru větru pro moji stanici
     - 1.0 [ZDE](https://opendata.chmi.cz/meteorology/climate/historical_csv/data/daily/wind/) vyhledejte pomocí ID stanice soubor který v názvu obsahuje parametr _Dmax_ (ne D10, ani Fmax).
     - 1.1 Pokud se sem dostáváte z úvodní stránky repozitáře tak zvolte __daily__ a následně __wind__
  
2. Zpracování stažených dat
     - 2.0 Stažená data obsahují denní hodnoty směru větru (pro maximální rychlost) ve stupních, pro výšku 10 m nad zemí
     - 2.1 Data jsou oddělena čárkami a oddělovačem desetinných míst je tečka - musím data dostat do formátu čitelného mojí verzí MS Excel
          - Možnost 1: Můj Excel je přenastaven nebo od začátku operuje s čárkami a tečkami - nic neměním a jen otevřu data a zkontroluji že vypadají v pořádku
          - Možnost 2: Přenastavím Excel aby takto fungoval (potenciálně si rozbiju veškerá starší data, která zde již mám)
          - Možnost 3: Použiju fígl s poznámkovým blokem - nahradím čárky za středníky (;) a následně tečky za čárky, data uložím jako csv a načtu do MS Excel
     - 2.2 Pro další práci budeme potřebovat sloupce _DT_ a __VALUE__, zbývající můžeme smazat
     - 2.3 Smažeme veškerá data před rokem 1961
     - 2.4 Vytvoříme si pomocný sloupec __SmerZaokrouhleni__, pomocí kterého zjednodušíme data pouze na základní směry větru
     - 2.5 Potřebujeme směry pro 45, 90, 135, 180, 225, 270, 315, 360 stupňů a také zachovat hodnoty 0, kterými se označuje bezvětří
          - Vzorec pro českou verzi MS Excel: =KDYŽ(B2=0;"Calm";ZAOKR.DOLŮ(B2;45)). Pokud to excel nechápe, zkuste vyměnit středníky za čárky.
          - Vzorec pro anglickou verzi MS Excel: =IF(B2=0,"Calm",ROUNDDOWN(B2,45))
     - 2.6 Funkční vzorec použijeme pro celá data
     - 2.7 Bokem na stejném listu připravíme pomocnou tabulku pro vykreslení větrné růžice
          - Nadepíšeme si sloupce __Směr, SměrText, Četnost, Podíl__
          - Do sloupce __Směr__ opíšeme hodnoty 0, 360, 45, 90, 135, 180, 225, 270, 315 a Calm. Tady se trochu komplikuje, protože severní směr větru odpovídá jak azimutu 0, tak 360, takže v dalším kroku do sloupce SměrText napíšeme nejdříve 0, pod to 360 a pokračujeme 45, 90, ...
          - Do sloupce __SměrText__ S, S, SV, V, JV, J, JZ, Z, SZ a Bezvětří
          - Do sloupce __Četnost__ spočítáme kolikrát se daná zaokrouhlená hodnota vyskytuje v našem denním záznamu a použijeme výpočet pro všechny hodnoty směru
               - Vzorec využije funkci countif: __=COUNTIF(C:C;D2)__ (sečti všechny výskyty ve sloupci C, kdy se hodnota rovná vybrané buňce - v mém případě D2)
          - Do sloupce __Podíl__ dopočítáme procentuální vyjádření četnosti
               - Nejdříve si pro všechny vypočítané četnosti uděláme sumu hodnot (např. __=suma(H3:H11)__)
               - Následně do sloupce __Podíl__ pro jednotlivé směry vypočítáme trojčlenkou procentuální zastoupení - abychom mohli vzorec roztáhnout pro všechny hodnoty musíme si zafixovat hodnotu sumy pomocí symbolů dolaru - např. __$H$12__
          - Výsledkem je hotová tabulka pro tvorbu grafu větrné růžice pro naši stanici
          - Pokud jste dočetli až sem a jste v pasti a nic z toho nechápete, data četností směru větru lze alternativně stáhnout z [Tabulek podnebí](https://www.intersucho.cz/runtime/cache/files/original/t/tabulky-podnebi-final-verze-na-tisk-20251022101851.pdf), kde jsou hodnoty uvedeny v Tab. 34 a udělat graf z nich.
      
3. Tvorba grafu větrné růžice
     - 3.0 Pro tvorbu grafu vybereme naše procentuální hodnoty směru větru (mimo bezvětří)
     - 3.1 Na kartě __Vložení__ zvolíme možnost __Vložit vodopádový, trychtýřový, burzovní, povrchový nebo paprskový graf__ a v další nabídce vybereme __Paprskový s výplní__
     - 3.2 Doplníme všechny náležitosti grafu
     - 3.3 Jako popisky os zvolíme námi připravené texty ze sloupce __SměrText__
     - 3.4 Do grafu jako text přidáme také procentuální hodnotu pro bezvětří

</details>
  
<details markdown="1">
<summary> Cvičení 09 </summary>
# Cvičení 09 (týden 01.12.2025) - Test nanečisto a opakování a doplnění znalostí z předcházejících cvičení

# Odkazy pro zvídavé #
- Infografiky k dopadů klimatické změny v ČR: [www.klimatickazmena.cz](https://www.klimatickazmena.cz/infografiky/)
- Portál světové meteorologické organizace: [Atlas témat ZDE](https://wmo.int/topics)
- Podklady portálu Fakta o klimatu: [Grafiky ZDE](https://faktaoklimatu.cz/temata/klimaticka-zmena)
- Data budoucího vývoje klimatu: [Dostupná na portálu ClimRisk](https://www.climrisk.cz/)
</details>
  
<details markdown="1">
<summary> Cvičení 10 </summary>
# Cvičení 10 (týden od 08.12.2025) - Oblaka (ne mraky)
- Cílem cvičení je získat přehled o klasifikaci a druzích oblaků. 

# Odkazy pro zvídavé #
- Můžete navštívit stránky světové meteorologické asociace (WMO), kde najdete [online atlas oblaků](https://cloudatlas.wmo.int/en/home.html) (eng).
- Najdete tam také [klasifikaci jednotlivých mraků](https://cloudatlas.wmo.int/en/clouds-definitions.html), na základě výšky, v jaké se tvoří, nebo jejich vertikálního vývoje .
- Najdete tam i [definice jednotlivých typů oblaků](https://cloudatlas.wmo.int/en/descriptions-of-clouds.html), včetně mnoha fotografií.
- Komu to nestačilo, můžete si zopakovat i cvičení o meteorech a podívat se na [definice a popis jednotlivých typů meteorů](https://cloudatlas.wmo.int/en/definitions-and-descriptions-of-meteors.html).
</details>
  
<details markdown="1">
<summary> Cvičení 11 </summary>
# Cvičení 11 (týden 15.12.2025) - Kontrola seminárních prací a zápočty
- Kdo má všechno hotové a nemá víc jak dvě neomluvené absence, ten nechť dostane zápočet a může jít ke zkoušce.

  
 ![The End](/end of semester.png)
</details>


