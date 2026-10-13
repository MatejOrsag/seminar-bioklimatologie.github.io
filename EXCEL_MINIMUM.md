# Excel minimum

[← zpět na zadání cvičení](README.md)

Tohle je všechno, co z Excelu během semestru potřebuju. Když se zaseknu, nejdřív se podívám sem.

### 1. Kde je můj soubor
- Soubor ukládám přes __Soubor → Uložit jako → Procházet__ a vyberu složku, kterou znám (např. Dokumenty/Bioklimatologie).
- Pozor na OneDrive: pokud Excel ukládá „do cloudu“, ověřím si, že soubor najdu i příště.
- Název souboru bez mezer a bez diakritiky: __PrijmeniJmeno_Bioklimatologie.xlsx__
- Ukládám průběžně: __CTRL + S__

### 2. Čárka, tečka, středník (nejčastější problém!)
- Český Excel používá __desetinnou čárku__ (12,5) a ve vzorcích __středník__ jako oddělovač: `=KDYŽ(A2>0;"ano";"ne")`
- Anglický Excel používá __desetinnou tečku__ (12.5) a ve vzorcích __čárku__: `=IF(A2>0,"yes","no")`
- Data z ČHMÚ a Copernicus jsou v „anglickém“ formátu (čárky mezi sloupci, tečky v číslech).
- Když po otevření vidím místo čísel __datumy__ (např. 12.IV nebo 5.led), Excel si číslo špatně vyložil. Soubor zavřu bez uložení a použiju převodník nebo postup s Poznámkovým blokem (viz Cvičení 01 v [README](README.md)).
- Když vzorec nefunguje, první co zkusím: vyměnit `;` za `,` nebo naopak.

### 3. Vzorce
- Vzorec vždy začíná znakem __=__
- __Zkopírování vzorce dolů:__ kliknu na buňku se vzorcem, najedu myší na malý čtvereček v pravém dolním rohu buňky (kurzor se změní na tenký křížek) a táhnu dolů. Nebo na čtvereček __dvakrát kliknu__ a Excel vzorec zkopíruje sám až na konec dat.
- __Zafixování buňky ($):__ když chci, aby se při kopírování odkaz neposouval, napíšu `$G$11` místo `G11`. Rychle: kliknu do odkazu ve vzorci a zmáčknu __F4__.
- Názvy funkcí v české a anglické verzi:

| Česky | Anglicky | K čemu |
|---|---|---|
| SUMA | SUM | součet |
| PRŮMĚR | AVERAGE | průměr |
| KDYŽ | IF | podmínka |
| COUNTIF | COUNTIF | kolikrát se hodnota vyskytuje |
| ZAOKROUHLIT | ROUND | zaokrouhlení |
| CELÁ.ČÁST | INT | celá část čísla (useknutí desetin) |
| MOD | MOD | zbytek po dělení |

<!-- SCREENSHOT: img/excel_uchyt_vzorce.png | malý čtvereček v pravém dolním rohu vybrané buňky -->

### 4. Kopírování a vkládání
- __CTRL + C__ kopírovat, __CTRL + V__ vložit, __CTRL + Z__ krok zpět (zachrání mě skoro vždy)
- __Vložit jen hodnoty:__ pravý klik → __Možnosti vložení__ → ikona se schránkou a „123“ (Hodnoty). Použiju, když kopíruju výsledky vzorců nebo kontingenční tabulky a chci jen čísla.
- __Výběr celého sloupce dat až na konec:__ kliknu na první buňku a zmáčknu __CTRL + SHIFT + šipka dolů__
- __Skok na konec dat:__ __CTRL + šipka dolů__

<!-- SCREENSHOT: img/excel_vlozit_hodnoty.png | pravý klik, možnosti vložení, ikona Hodnoty (123) -->

### 5. Filtr
- Kliknu do tabulky, karta __Data → Filtr__ (nebo __CTRL + SHIFT + L__). V záhlaví sloupců se objeví šipky.
- Šipka → odškrtnu/zaškrtnu hodnoty, nebo __Filtry čísel → Mezi__.
- Pozor: filtr data jen __skrývá__, nemaže. Když chci filtr zrušit, dám znovu __Data → Filtr__.

### 6. Kontingenční tabulka (pivot)
- Slouží k rychlému výpočtu průměru/součtu podle skupin (např. průměrná teplota pro každý měsíc).
- __Vložení → Kontingenční tabulka__ (nebo Kontingenční graf), vyberu data.
- Vpravo v podokně přetáhnu: skupinu (Měsíc, Dekáda) do __Řádky / Osa__, hodnotu (Teplota, Srážky) do __Hodnoty__.
- ⚠️ Excel automaticky dává __Součet__. Pro teploty i měsíční srážky v normálu chci __Průměr__: klik na pole v Hodnotách → __Nastavení polí hodnot → Průměr__.
- Když vidím teplotu v červenci 500 °C, mám Součet místo Průměru.

<!-- SCREENSHOT: img/excel_kontingencni_pole.png | podokno polí kontingenční tabulky, Měsíc v Řádky, Teplota v Hodnoty -->
<!-- SCREENSHOT: img/excel_nastaveni_poli_prumer.png | okno Nastavení polí hodnot s vybraným Průměr -->

### 7. Grafy
- Vyberu data → karta __Vložení__ → typ grafu.
- __Spojnicový graf__: hodnoty v čase (teplota po měsících, roky).
- __Bodový (XY) graf__: vztah dvou čísel (teplota vs. nadmořská výška). Pro gradienty vždy bodový, ne spojnicový!
- __Sloupcový graf__: porovnání skupin (srážky po měsících ve dvou obdobích).
- Úpravy grafu: kliknu na graf, vpravo nahoře se objeví __+__ (prvky grafu: názvy os, legenda, spojnice trendu).
- __Spojnice trendu s rovnicí:__ pravý klik na body/čáru v grafu → __Přidat spojnici trendu__ → Lineární → dole zaškrtnu __Zobrazit rovnici v grafu__.

## Kompletní graf
Platí pro všechny grafy v semestru.
- [ ] Název grafu (co, kde, kdy), např. „Průměrná měsíční teplota vzduchu, Brno-Tuřany, 1961–1990 a 1991–2020“
- [ ] Popisek osy X i Y __včetně jednotek__ (°C, mm, m n. m., Wh/m²)
- [ ] Legenda, pokud je v grafu víc řad, a v legendě srozumitelné názvy (ne „Řada1“)
- [ ] Zdroj dat (vložím textové pole pod graf, např. „Zdroj: ČHMÚ“)
- [ ] Čitelné písmo a barvy, které se dají rozlišit

<!-- SCREENSHOT: img/vzorovy_kompletni_graf.png | vzorový hotový graf s popsanými náležitostmi (šipky na název, osy, jednotky, legendu, zdroj) -->

### 8. Mac
- Místo __CTRL__ používám __CMD (⌘)__.
- Některé nabídky se jmenují jinak nebo jsou jinde. Když něco nenajdu, ptám se.
