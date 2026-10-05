# ChemistryAI — AI, která rozhoduje, jaký experiment spustit jako další tam, kde jsou experimenty pomalé, drahé, destruktivní nebo dlouhodobé; cílem je zkrátit cestu od požadavku na materiál k validovanému materiálu s dostatkem důkazů, aby ho šlo nasadit

**Founder:** @charbjak  ·  **Project:** startup — https://gitlab.fit.cvut.cz/charbjak/startup

> Který vertikál × workflow × problém je ten správný první wedge — tedy kde lepší rozhodování o experimentech nezlepší R&D o 10–20 %, ale rozhodne o tom, jestli je program vůbec proveditelný?

**Tags:** `deeptech`, `materials`, `active-learning`, `qualification`, `ai`

## 📊 Market intelligence

Tvoje otázka zní „kde přesně začít", takže tahle rešerše netvrdí, jak velký je trh s AI pro materiály — tvrdí, kde v něm je rozhodnutí, za které někdo platí. Kategorie sama o sobě je malá a neusazená: AI v objevování materiálů je 0,97 mld. USD v roce 2026 s výhledem 2,77 mld. v 2030, a odhady „materials informatics" se mezi analytiky liší třikrát (0,21 / 0,25 / 0,37 mld. USD pro 2026), což samo o sobě říká, že nikdo neví, co do ní patří. Peníze nejsou v kategorii, jsou v rozhodnutích pod ní: kvalifikace materiálu běžně trvá 5 až 15 let, znamená tisíce zkoušek za miliony dolarů, a každá změna parametru může vynutit re-kvalifikaci.

**Why now:** Tři věci se potkaly. (1) Regulace nutí přeformulovat: ECHA uzavřela finální konzultaci k PFAS 25. 5. 2026 a hodnocení dokončuje do konce roku, SEAC nepřijal vyjmutí fluoropolymerů, návrh pokrývá přes 10 000 látek; k tomu se chystá široké omezení Cr(VI) s přijetím kolem září 2026 až začátku 2027. (2) Evropa to podepřela penězi a politikou: sdělení „Advanced Materials for Industrial Leadership" (COM(2024) 98, únor 2024), Safe and Sustainable by Design jako kritérium, a v Horizon Europe výzva HORIZON-CL4-2026-01-MAT-PROD-23 na urychlení vývoje materiálů digitalizací a AI s rozpočtem 37 mil. EUR a 5 až 6,5 mil. EUR na projekt. (3) Metoda je prokázaná: predikce drahého dlouhého testu z levného krátkého měření funguje tam, kde někdo data vyrobil záměrně.
**Positioning:** Ne „AI for materials" platforma — tam už sedí Citrine, MaterialsZone, Polymerize, Osium AI, Albert Invent, Entalpic a hlavně Intellegens, jejichž Alchemite je přímo prodávaný jako nástroj pro návrh experimentů nad řídkými a zašuměnými daty. Volné místo je úzké a konkrétní: **predikce výsledku kvalifikačního programu z krátkých zkoušek, napojená na normu a akreditovanou zkušebnu**. Hodnota není v přesnosti modelu, ale v tom, že je predikce přijatelná jako podklad rozhodnutí o nasazení materiálu.
**Whitespace / wedge:** Nejsilnější existující důkaz tvé teze je z baterií: Severson, Attia a spol. předpověděli životnost článku s chybou 9,1 % z prvních 100 cyklů a zařadili články do dvou skupin s chybou 4,9 % z prvních pěti cyklů, na datasetu 169 LFP/grafitových článků — a navazující práce z toho udělala uzavřenou smyčku optimalizující protokol rychlého nabíjení. Autoři to sami shrnují jako spojení **záměrné výroby dat** s datovým modelem. To je zároveň důkaz i hranice: nikdo totéž neudělal pro degradaci povlaků, korozi ani kvalifikaci, protože tam chybí ten dataset, ne ta metoda.

### ✅ Strategic recommendations
- Třídicí test pro každou příležitost: stojí špatná volba experimentu jeden kvalifikační cyklus, nebo pár týdnů laboratoře? Jen to první je kategorie „program by jinak nebyl proveditelný".
- Dostupnost dat povyš z šestého kritéria na první filtr. V literatuře o kvalifikaci se uvádí extrapolace v čase zhruba 20× a víc — 30 let provozu z jednoho až dvou let dat — ale výslovně jen při velkých krátkodobých datových sadách. Vázaným zdrojem jsou data, ne model.
- Než vybereš vertikál, zjisti, kde v něm leží časově spárovaná fyzikální data. NIMS provozuje veřejné datové listy pro creep (cds.nims.go.jp) i korozi (cods.nims.go.jp); v ČR drží páry zrychlená zkouška ↔ terénní expozice Technopark Kralupy VŠCHT a akreditovaná zkušebna SVÚOM. Většina otevřených materiálových dat je ale výpočetních, ne degradačních — to je ta vzácná věc.
- Tři kandidáti, kteří testem procházejí: kvalifikace chrome-free primerů, přeformulování kvůli PFAS, a substituce kritických surovin. První dva mají regulatorní termín, tedy rozpočet a datum; třetí má politickou prioritu (z 47 strategických projektů CRMA jsou jen dva substituční) a evropské peníze, ale ne termín.
- V rozhovorech se ptej na poslední re-kvalifikaci: co ji spustila, jak dlouho trvala, co stála, co se kvůli ní nestihlo. Vrací datum, číslo a jméno rozhodovatele; „bylo by fajn to zrychlit" nevrací nic.
- Postav si jednu věc, kterou nikdo jiný nemá, a to je retrospektivní validace: vezmi archivní sadu, kde je výsledek po letech známý, zakryj si ho a ukaž, že z krátkých dat předpovíš, co se stalo. To je jediný způsob, jak si zákazník může tvoje tvrzení ověřit rychleji, než trvá ten test.
- Vyber jeden vertikál na 30 dní a aktivně se ho snaž zabít. Tři paralelně držené hypotézy jsou v téhle fázi horší než jedna vyvrácená.

### ⚠️ Key risks
- Obecná platforma už existuje a prodává se. Intellegens Alchemite je komerční nástroj pro návrh experimentů nad řídkými daty s tvrzením až o 80 % kratší experimentální práci; Albert Invent má 22,5 mil. USD od Coatue na chemii v enterprise R&D. Jestli tvůj první produkt bude znít jako oni, soutěžíš s jejich obchodním týmem, ne s jejich technologií.
- Vázaným zdrojem jsou časově spárovaná data. Bez archivu, kde je krátkodobé měření spojené se známým dlouhodobým výsledkem, není co trénovat ani čím se validovat.
- Akceptace, ne přesnost. Predikce, která se nedá napojit na normu (ISO 9227, ISO 11997-1, VDA 621-415, SAE J 2334, MIL-PRF-85285) a na akreditovanou zkušebnu podle ISO/IEC 17025, nemá v kvalifikaci hodnotu, i kdyby byla správná.
- Zákazník nemůže tvou predikci rychle ověřit — to je přesně ten důvod, proč problém existuje. Bez retrospektivní validace zůstáváš u tvrzení, kterému nikdo nemá jak uvěřit.
- Kapitál proti tobě je nesouměřitelný a míří na obecnou vrstvu: Lila Sciences 350 mil. USD v Series A (550 mil. celkem), Periodic Labs 550,7 mil., Radical AI 55 mil. seed vedený RTX Ventures. Úzký, regulací ohraničený wedge je jediný tvar, kde tohle nehraje roli.
- Šest kritérií bez termínu se snadno stane způsobem, jak nevybrat. Hlavní riziko téhle fáze je rozhodovací, ne technické.

### Kategorie je malá a neusazená; rozhodnutí pod ní jsou velká
Shora-dolů čísla pro „AI v materiálech" používej jen jako kontext — rozcházejí se natolik, že samy o sobě nic nerozhodnou. Rozhodnutí opři o to, co stojí jeden kvalifikační program u jednoho zákazníka.
- AI v objevování materiálů: 0,74 mld. USD v 2025 → 0,97 mld. USD v 2026 (CAGR 30,3 %) s výhledem 2,77 mld. USD do roku 2030.
- „Materials informatics" jako kategorie je mnohem menší a odhady se rozcházejí třikrát: 0,25 mld. USD (Meticulous, 2026), 0,21 mld. USD (360iResearch, 2026) a 0,37 mld. USD (Towards Chem&Materials, 2026). Takový rozptyl znamená, že se analytici neshodnou ani na tom, co do kategorie patří.
- Generativní AI v materiálové vědě se vykazuje zvlášť a je větší: 2,24 mld. USD v 2026 → 7,01 mld. USD v 2030 (CAGR 33 %). Pozor, do téhle škatulky spadají i věci, které s tvým problémem nemají nic společného.
- Trhy, kterých se tvůj wedge dotýká, jsou o řád větší než ta kategorie: ochranné a marine povlaky 22,44 mld. USD (2026), zkoušení materiálů 3,9 až 6,6 mld. USD podle vymezení.
- Bottom-up, které si můžeš ověřit v rozhovorech: kolik kvalifikačních programů ročně spustí jeden formulátor nebo výrobce, kolik stojí jeden program (faktura zkušebny plus zdržení v měsících), a kolik z nich bylo vynucených změnou normy nebo suroviny. Tři taková čísla nahradí všechny odhady výše.

_Sources:_ [[1]](https://www.researchandmarkets.com/reports/6227043/ai-in-materials-discovery-global-market-report) [[2]](https://finance.yahoo.com/technology/ai/articles/ai-materials-discovery-market-reach-081000013.html) [[3]](https://www.meticulousresearch.com/product/materials-informatics-market-6787) [[4]](https://www.360iresearch.com/library/intelligence/material-informatics) [[5]](https://www.thebusinessresearchcompany.com/report/generative-artificial-intelligence-ai-in-material-science-global-market-report) [[6]](https://www.businessresearchinsights.com/market-reports/protective-marine-coatings-market-101594)

### Kdo už prodává „rozhodni, co změřit dál"
Obecnou vrstvu někdo prodává a dělá to dobře. Konkrétní vrstvu — predikci výsledku kvalifikace z krátkých zkoušek, přijatelnou jako důkaz — neprodává nikdo. Nejsilnější existující důkaz, že to jde, je akademický a je z baterií.
- Intellegens (Cambridge, 2017) prodává Alchemite jako nástroj pro strojové učení nad řídkými a neúplnými daty a výslovně jako „data-driven experimental design tool" s tvrzením o zkrácení experimentální práce až o 80 %; novější verze přidávají LLM vedení. Tohle je tvůj nejbližší komerční soused.
- Zbytek obecné vrstvy: Citrine Informatics (81,3 mil. USD, Series C), MaterialsZone (7 mil.), Polymerize (4,4 mil.), Osium AI (3,1 mil., ~990 tis. USD tržeb s devíti lidmi v 2025), Albert Invent (22,5 mil. USD Series A vedená Coatue, chemistry-native AI pro enterprise R&D), Entalpic (8,5 mil. EUR seed, experimentální laboratoř v Grenoblu na konci 2026), Uncountable.
- Autonomní laboratoře hrají jinou, kapitálově těžší hru: Lila Sciences 350 mil. USD Series A při 550 mil. celkem na „AI Science Factories", Periodic Labs 550,7 mil. USD, Radical AI 55 mil. USD seed vedený RTX Ventures, Argonne Polybot pro polymerní filmy a povlaky.
- Důkaz tvé konkrétní teze existuje a je citovaný: Severson, Attia a spol. předpověděli životnost lithiových článků s chybou 9,1 % z prvních 100 cyklů a klasifikovali je do dvou skupin s chybou 4,9 % z prvních pěti cyklů, na 169 LFP/grafitových článcích; navazující práce z toho udělala uzavřenou smyčku optimalizující nabíjecí protokol. Autoři zdůrazňují spojení záměrné výroby dat s datovým modelem.
- Pro povlaky a korozi existují publikované ML modely životnosti (dvoustupňový model v npj Materials Degradation 2025, CNN na epoxidy s chybou 2,60 %, semi-supervised model atmosférického stárnutí akrylátů), ale žádný produkt. Metoda tedy není obhajitelná výhoda; data a napojení na normu ano.
- Zkušebny prodávají kapacitu, ne rozhodnutí: Q-Lab (QUV, akreditované kontraktní zkoušky), Element (globální síť laboratoří), v ČR SVÚOM (akreditovaná zkušebna č. 1096).

_Sources:_ [[7]](https://intellegens.com/solutions/) [[8]](https://techcrunch.com/2024/12/11/albert-invent-hopes-to-revolutionize-the-chemicals-sector-with-its-ai-platform) [[9]](https://entalpic.ai/) [[10]](https://www.lila.ai/news/announcing-the-close-of-our-series-a) [[11]](https://www.semanticscholar.org/paper/Data-driven-prediction-of-battery-cycle-life-before-Severson-Attia/242a5c2ecb74cbbc2f9d9bdb6e76bb1ca36cdcb9) [[12]](https://www.nature.com/articles/s41529-025-00614-6) [[13]](https://getlatka.com/companies/osium.ai) [[14]](https://tracxn.com/d/trending-business-models/startups-in-material-informatics/__zCPscUCJyfvFdUzoLsSLt9w9uvOSQFw1pGrAY3Rw2NI)

### Kde ta data vlastně jsou — tvůj první filtr
Otevřených materiálových dat je hodně, ale skoro všechna jsou výpočetní. Vzácné je to, co potřebuješ ty: krátkodobé fyzikální měření spárované se známým dlouhodobým výsledkem. Vyber vertikál podle toho, kde takové páry existují.
- NIMS (Japonsko) provozuje v rámci MatNavi strukturální datové listy, které jsou přesně tenhle typ dat: Creep Data Sheet (cds.nims.go.jp) a Corrosion Data Sheet (cods.nims.go.jp), plus databáze únavy a mikrostruktury creepovaných materiálů. Jde o desítky let systematického měření, veřejně dostupného.
- NOMAD drží přes 50 milionů výpočtů celkové energie a je open-source; NIST Materials Data Facility publikuje sdílená data výzkumníků. Obojí je ale převážně výpočetní nebo charakterizační, ne degradační — na predikci stárnutí se to samo o sobě nehodí.
- V Česku leží páry zrychlená zkouška ↔ terénní expozice tam, kde se obojí dělá: Technopark Kralupy VŠCHT (urychlené korozní a klimatické zkoušky, ~100 průmyslových kontraktů ročně) a akreditovaná zkušebna SVÚOM, která provádí zkoušky podle ISO 9227, PV 1210, VDA 621-415, SAE J 2334 a ISO 11997-1 cyklus B.
- V bateriích je referenční veřejný dataset 169 LFP/grafitových článků cyklovaných podle různých protokolů rychlého nabíjení — a je jediný důvod, proč tam ta predikce funguje. Analogický dataset pro povlaky zatím veřejně neexistuje; kdo ho sestaví, drží v ruce aktivum.
- Praktický důsledek: první obchodní rozhovor nemusí být o produktu. Může být o přístupu k archivu výměnou za jeho zpracování — to je levnější vstup než licence a rovnou vytváří tvoje aktivum.

_Sources:_ [[15]](https://www.osti.gov/etdeweb/biblio/20949172) [[16]](https://doi.org/10.1080/27660400.2025.2518745) [[17]](https://github.com/blaiszik/Materials-Databases) [[18]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) [[19]](https://www.technopark-kralupy.cz/sluzby)

### Proč teď: regulace vyrábí kvalifikační práci
Nejsilnější poptávka po rychlejším rozhodování o experimentech nevzniká z chuti inovovat, ale z toho, že se mění pravidla a celé portfolio se musí znovu doložit.
- PFAS: ECHA spustila 26. 3. 2026 finální konzultaci, RAC vydal finální a SEAC návrh stanoviska podporující celoevropské omezení, konzultace se uzavřela 25. 5. 2026 a vědecké hodnocení se má dokončit do konce roku 2026. Návrh pokrývá přes 10 000 látek a žádost průmyslu vyjmout fluoropolymery SEAC nepřijal.
- Cr(VI): chromáty pro aerospace a defence dostaly 12letou autorizaci, ale ECHA chystá široké omezení Cr(VI) s přijetím kolem září 2026 až začátku 2027 — a stále platí, že u žádné alternativy nebyla prokázána stejná úroveň korozní ochrany.
- Kvalifikace je sama o sobě úzké hrdlo: úplná empirická kvalifikace materiálu obvykle zabere 5 až 15 let, tisíce jednotlivých zkoušek a miliony dolarů; zpoždění mezi objevem materiálu a jeho kvalifikací se odhaduje asi na 30 let, a jakákoli změna parametru nebo procesu může vynutit re-kvalifikaci.
- Tentýž zdroj uvádí, že modely dokážou extrapolovat v čase zhruba 20× a víc — materiál na 30 let provozu by šlo kvalifikovat z jednoho až dvou let dat — ale výslovně jen při dostupnosti velkých krátkodobých datových sad.
- Substituce je nejhůře obsazená noha Critical Raw Materials Act: z 47 strategických projektů vybraných Komisí jsou jen dva substituční.
- Evropa to podepřela strategií: sdělení „Advanced Materials for Industrial Leadership" (COM(2024) 98, 27. 2. 2024) a kritéria Safe and Sustainable by Design jako součást Chemicals Strategy for Sustainability.

_Sources:_ [[20]](https://www.whitecase.com/insight-alert/europes-pfas-restriction-proposal-moving-forward) [[21]](https://www.asd-europe.org/news-media/news-events/news/eu-grants-12-year-authorisation-for-chromates/) [[22]](https://www.cargroup.org/wp-content/uploads/2017/02/Material-Qualification.pdf) [[23]](https://insidemetaladditivemanufacturing.com/2024/05/20/qualification-and-certification-costs-contributing-factors-for-am-metal-aerospace-parts/) [[24]](https://ieu-monitoring.com/editorial/raw-materials-in-europe-eu-commission-selects-47-strategic-projects-to-diversify-access/551430) [[25]](https://research-and-innovation.ec.europa.eu/research-area/industrial-research-and-innovation/chemicals-and-advanced-materials/advanced-materials-industrial-leadership_en)

### Normy, do kterých musí predikce zapadnout
Kvalifikace je definovaná normami a akreditací. Predikce má hodnotu jen tehdy, když mluví jazykem konkrétní zkoušky a vychází z akreditovaného prostředí — to je zároveň vstupní bariéra i budoucí moat.
- Zrychlené a cyklické korozní zkoušky dostupné akreditovaně v ČR (zkušebna SVÚOM č. 1096, ČIA podle ČSN EN ISO/IEC 17025:2018): ČSN EN ISO 9227, PV 1210, VDA 621-415, SAE J 2334, ČSN EN ISO 11997-1 cyklus B a cyklické zkoušky pod UV lampami. Tohle je konkrétní seznam cílových veličin pro predikci.
- Letecký příklad: MIL-PRF-85285 je výkonová specifikace DoD pro polyuretanové vrchní nátěry; certifikaci administruje U.S. Naval Air Warfare Center Patuxent River a periodické ověřování probíhá ve dvouletých intervalech od původní kvalifikace. Opakovaná re-kvalifikace je tedy opakovaný rozpočet.
- Zkoušky v té specifikaci míří na konkrétní přejímací veličiny — adhezi mřížkovým řezem a odtrhem, adhezi po expozici kapalinám a prostředí, odolnost proti nárazu. Predikce musí cílit na ně, ne na abstraktní „degradaci".
- Safe and Sustainable by Design přidává druhou osu: nová pokročilá materiálová řešení mají být bezpečná a udržitelná už návrhem, což z hodnocení dopadu dělá součást vývoje, ne jeho dodatek.

_Sources:_ [[18]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) [[26]](https://www.valencesurfacetech.com/the-news/mil-prf-85285-type-1/) [[27]](https://www.asme.org/codes-standards/find-codes-standards/standard-for-verification-and-validation-in-computational-fluid-dynamics-and-heat-transfer) [[28]](https://research-and-innovation.ec.europa.eu/research-area/industrial-research-and-innovation/chemicals-and-advanced-materials_en)

### Kdo dostal peníze a odkud je můžeš vzít ty
Rizikový kapitál teče do obecné vrstvy a do autonomních laboratoří, tedy tam, kde se soutěží objemem. Pro tebe je relevantnější evropské projektové financování, protože je navázané přesně na ten regulatorní tlak, který tvůj problém vytváří.
- Obecná vrstva: Citrine 81,3 mil. USD (Series C), Albert Invent 22,5 mil. USD (Series A, Coatue), Entalpic 8,5 mil. EUR (seed), Osium AI 3,1 mil. USD, MaterialsZone 7 mil., Polymerize 4,4 mil.
- Autonomní laboratoře: Lila Sciences 350 mil. USD Series A a 550 mil. celkem, Periodic Labs 550,7 mil. USD, Radical AI 55 mil. USD seed vedený RTX Ventures s účastí NVentures.
- Horizon Europe, Cluster 4: výzva HORIZON-CL4-2026-01-MAT-PROD-23 na urychlení objevu a vývoje chemikálií a pokročilých materiálů digitalizací a AI, rozpočet 37 mil. EUR, 5 až 6,5 mil. EUR na projekt, otevření 6. 1. 2026 a uzávěrka 21. 4. 2026 — tedy pro tebe až další kolo, ale je to přesně tvoje téma a stojí za to vědět, kdo ho letos vyhrál.
- Souběžně běží výzvy na bezpečné a udržitelné materiály a procesy snižující závislost na kritických a strategických surovinách, dohromady 36 mil. EUR, 6 až 7,5 mil. EUR na projekt.
- K tomu Komise avizovala v rámci cirkulární ekonomiky další výzvy Horizon Europe za 593 mil. EUR v pracovním programu 2026–2027.

_Sources:_ [[8]](https://techcrunch.com/2024/12/11/albert-invent-hopes-to-revolutionize-the-chemicals-sector-with-its-ai-platform) [[10]](https://www.lila.ai/news/announcing-the-close-of-our-series-a) [[29]](https://pitchbook.com/profiles/company/229130-47) [[30]](https://errin.eu/calls/accelerating-discovery-and-development-chemicals-and-innovative-advanced-materials-through) [[31]](https://ec.europa.eu/info/funding-tenders/opportunities/docs/2021-2027/horizon/wp-call/2026-2027/wp-7-digital-industry-and-space_horizon-2026-2027_en.pdf)

## 🔗 Sources  ·  all links
1. [researchandmarkets.com](https://www.researchandmarkets.com/reports/6227043/ai-in-materials-discovery-global-market-report)
2. [finance.yahoo.com](https://finance.yahoo.com/technology/ai/articles/ai-materials-discovery-market-reach-081000013.html)
3. [meticulousresearch.com](https://www.meticulousresearch.com/product/materials-informatics-market-6787)
4. [360iresearch.com](https://www.360iresearch.com/library/intelligence/material-informatics)
5. [thebusinessresearchcompany.com](https://www.thebusinessresearchcompany.com/report/generative-artificial-intelligence-ai-in-material-science-global-market-report)
6. [businessresearchinsights.com](https://www.businessresearchinsights.com/market-reports/protective-marine-coatings-market-101594)
7. [intellegens.com](https://intellegens.com/solutions/)
8. [techcrunch.com](https://techcrunch.com/2024/12/11/albert-invent-hopes-to-revolutionize-the-chemicals-sector-with-its-ai-platform)
9. [entalpic.ai](https://entalpic.ai/)
10. [lila.ai](https://www.lila.ai/news/announcing-the-close-of-our-series-a)
11. [semanticscholar.org](https://www.semanticscholar.org/paper/Data-driven-prediction-of-battery-cycle-life-before-Severson-Attia/242a5c2ecb74cbbc2f9d9bdb6e76bb1ca36cdcb9)
12. [nature.com](https://www.nature.com/articles/s41529-025-00614-6)
13. [getlatka.com](https://getlatka.com/companies/osium.ai)
14. [tracxn.com](https://tracxn.com/d/trending-business-models/startups-in-material-informatics/__zCPscUCJyfvFdUzoLsSLt9w9uvOSQFw1pGrAY3Rw2NI)
15. [osti.gov](https://www.osti.gov/etdeweb/biblio/20949172)
16. [doi.org](https://doi.org/10.1080/27660400.2025.2518745)
17. [github.com](https://github.com/blaiszik/Materials-Databases)
18. [svuom.cz](https://svuom.cz/index.php?lang=cz&zobraz=akrzk)
19. [technopark-kralupy.cz](https://www.technopark-kralupy.cz/sluzby)
20. [whitecase.com](https://www.whitecase.com/insight-alert/europes-pfas-restriction-proposal-moving-forward)
21. [asd-europe.org](https://www.asd-europe.org/news-media/news-events/news/eu-grants-12-year-authorisation-for-chromates/)
22. [cargroup.org](https://www.cargroup.org/wp-content/uploads/2017/02/Material-Qualification.pdf)
23. [insidemetaladditivemanufacturing.com](https://insidemetaladditivemanufacturing.com/2024/05/20/qualification-and-certification-costs-contributing-factors-for-am-metal-aerospace-parts/)
24. [ieu-monitoring.com](https://ieu-monitoring.com/editorial/raw-materials-in-europe-eu-commission-selects-47-strategic-projects-to-diversify-access/551430)
25. [research-and-innovation.ec.europa.eu](https://research-and-innovation.ec.europa.eu/research-area/industrial-research-and-innovation/chemicals-and-advanced-materials/advanced-materials-industrial-leadership_en)
26. [valencesurfacetech.com](https://www.valencesurfacetech.com/the-news/mil-prf-85285-type-1/)
27. [asme.org](https://www.asme.org/codes-standards/find-codes-standards/standard-for-verification-and-validation-in-computational-fluid-dynamics-and-heat-transfer)
28. [research-and-innovation.ec.europa.eu](https://research-and-innovation.ec.europa.eu/research-area/industrial-research-and-innovation/chemicals-and-advanced-materials_en)
29. [pitchbook.com](https://pitchbook.com/profiles/company/229130-47)
30. [errin.eu](https://errin.eu/calls/accelerating-discovery-and-development-chemicals-and-innovative-advanced-materials-through)
31. [ec.europa.eu](https://ec.europa.eu/info/funding-tenders/opportunities/docs/2021-2027/horizon/wp-call/2026-2027/wp-7-digital-industry-and-space_horizon-2026-2027_en.pdf)

## 🤝 Recommended contacts

_Intros are **earned** — you unlock contacts as your venture clears each stage, so we only connect you when you're ready. Feedback above is always free._

### ✅ Available now
- **Tomáš Prošek** (academia, ✓ verified) — Vede skupinu Kovové konstrukční materiály v Technoparku Kralupy VŠCHT: atmosférická koroze, urychlené korozní a klimatické zkoušky, ochranné povlaky. 13 lidí a ~100 průmyslových kontraktů ročně — drží data i zákazníky. První telefonát, a to kvůli archivu, ne kvůli prodeji.
  - [technopark-kralupy.cz](https://www.technopark-kralupy.cz/lide/pracovnici/prosek-cz) · [vedavyzkum.cz](https://vedavyzkum.cz/rozhovory-a-osobnosti/rozhovory-a-profily/tomas-prosek-nasimi-koroznimi-testy-prochazi-horolezecke-skoby-z-celeho-sveta) · [sciprofiles.com](https://sciprofiles.com/profile/754796)
- **Milan Kouřil** (academia, ✓ verified) — Docent na Ústavu kovových materiálů a korozního inženýrství VŠCHT, vede skupinu Korozní inženýrství a je viceprezidentem Asociace korozních inženýrů. Věnuje se koroznímu monitoringu a protikorozní ochraně — vstup do celé české korozní komunity.
  - [ukmki.vscht.cz](https://ukmki.vscht.cz/lide/kouril) · [ukmki.vscht.cz](https://ukmki.vscht.cz/veda-a-vyzkum/koroze)
- **Andréa Kalendová** (academia, ✓ verified) — Profesorka na Fakultě chemicko-technologické Univerzity Pardubice, 25+ let výzkumu antikorozních pigmentů a organických povlaků, 100+ článků; spolupracuje s ÚACH AV ČR v Řeži a ÚMCH AV ČR. Nejsilnější česká adresa na formulaci povlaků — a přímo v profilu potenciálního cofoundera.
  - [upce.cz](https://www.upce.cz/prof-ing-andrea-kalendova-dr) · [fcht.upce.cz](https://fcht.upce.cz/sites/default/files/public/luva3059/metody-test-kor-vl.pdf)
- **Pavel Praks** (academia, ✓ verified) — IT4Innovations / VŠB-TUO: dělá přesně to, co ty — AI predikci provozního stárnutí a životnosti vysokoteplotních aluminidových difuzních povlaků, včetně symbolické regrese, společně s Fraunhofer ICT. Nejbližší český předchůdce tvé metody.
  - [vsb.cz](https://www.vsb.cz/fip-ai/en/news-detail/?reportId=51901) · [papers.ssrn.com](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7228546)
- **Vladislav Kolarik** (academia, ✓ verified) — Fraunhofer ICT — průmyslová strana téhož ML výzkumu stárnutí aluminidových povlaků (spoluautor s Praksem, prezentace na ICMCTF). Užitečný pro mezinárodní validaci a pro pochopení, jak takový výsledek kupuje průmysl.
  - [papers.ssrn.com](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7228546) · [avsconferences.org](https://avsconferences.org/ICMCTF2026/Topics/ProgramBookDownload?topicCode=MA)
- **Technopark Kralupy VŠCHT** (network, ✓ verified) — Výzkumné a inovační centrum VŠCHT, které přímo nabízí „urychlené korozní a klimatické zkoušky“ a skupinu Kovové konstrukční materiály. Nejrealističtější první partner pro data i pro společný projekt.
  - [technopark-kralupy.cz](https://www.technopark-kralupy.cz/) · [technopark-kralupy.cz](https://www.technopark-kralupy.cz/sluzby)
- **NIMS Structural Materials Data Sheets** (network, ✓ verified) — Japonský NIMS provozuje veřejné datové listy pro creep (cds.nims.go.jp) i korozi (cods.nims.go.jp) — desítky let systematického dlouhodobého měření. Přesně ten typ časově spárovaných dat, který je u tebe prvním filtrem, a je volně dostupný.
  - [cods.nims.go.jp](https://cods.nims.go.jp/) · [cds.nims.go.jp](https://cds.nims.go.jp/) · [osti.gov](https://www.osti.gov/etdeweb/biblio/20949172)
- **Konference Pigmenty a pojiva 2026** (network, ✓ verified) — 4.–6. 11. 2026, hotel Jezerka u Sečské přehrady. Organizuje CHEMAGAZÍN s Ústavem chemie a technologie makromolekulárních materiálů FCHT Univerzity Pardubice — celá česká formulátorská komunita na jednom místě. Nejlevnější způsob, jak za tři dny udělat deset zákaznických rozhovorů
  - [pigmentyapojiva.cz](https://pigmentyapojiva.cz/cs) · [pigmentyapojiva.cz](https://pigmentyapojiva.cz/cs/vlozne-a-registrace)
- **29. konference AKI — Koroze a protikorozní ochrana materiálů** (network, ✓ verified) — 11.–13. 11. 2026, hotel Clarion, Ústí nad Labem. Letošní téma je přímo „silnostěnné organické povlaky“ — tedy tvoje doména, s lidmi, kteří zkoušky reálně provádějí a platí.
  - [aki-koroze.cz](https://www.aki-koroze.cz/konference.php) · [mck.technicalmuseum.cz](https://mck.technicalmuseum.cz/akce/domaci-akce/29-konference-aki-koroze-a-protikorozni-ochrana-materialu/)
- **Asociace korozních inženýrů (AKI)** (network, ✓ verified) — Profesní asociace českých a slovenských korozních inženýrů — kurzy, časopis Koroze a ochrana materiálu, členská síť. Členství je nejjednodušší legitimní vstupenka do oboru pro člověka zvenčí.
  - [aki-koroze.cz](https://aki-koroze.cz/info.php?sel_casopis=0&submenu=o-cas) · [aki-koroze.cz](https://aki-koroze.cz/kurzy.php)
- **Konference Projektování a provoz povrchových úprav** (network, ✓ verified) — 52. ročník konference o povrchových úpravách — publikum z provozů a lakoven, tedy ti, kdo nesou důsledky špatné kvalifikace povlaku. Doplněk k akademičtějším AKI a Pigmentům.
  - [konferencepppu.cz](http://konferencepppu.cz/)
- **ESA BIC Czech Republic** (network, ✓ verified) — Inkubátor ESA provozovaný CzechInvestem: 50 000 EUR nekapitálové podpory plus technický a business mentoring pro startupy přenášející vesmírné technologie. Povlaky pro letecký a vesmírný segment do scope zapadají.
  - [czechinvest.gov.cz](https://czechinvest.gov.cz/cz/Sluzby-pro-startupy/ESA-BIC-Czech-Republic) · [podporapodniku.gov.cz](https://podporapodniku.gov.cz/vesmir/16/esa-bic-czech-republic/)
- **SVÚOM s.r.o.** (network, ✓ verified) — Akreditovaná zkušebna č. 1096 (ČIA, ČSN EN ISO/IEC 17025:2018): zkoušky podle ISO 9227, PV 1210, VDA 621-415, SAE J 2334 i ISO 11997-1 cyklus B. Drží páry zrychlená zkouška ↔ výsledek, tedy data, na kterých se dá postavit retrospektivní validace.
  - [svuom.cz](https://www.svuom.cz/) · [svuom.cz](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) · [svuom.cz](https://svuom.cz/index.php?lang=cz&zobraz=tnkorzk)

### 🔓 Earn introductions — unlock by progressing your venture
- 🔒 **Investor / high-profile** (venture) — Reach Value Prop & Business Model (currently unknown).
- 🔒 **Investor / high-profile** (venture) — Reach Value Prop & Business Model (currently unknown).

---
_StartupCoach — an AI mentor for founders, built at **FIT CTU** (Czech Technical University), operated by **Pavel Kordík**._