# ChemistryAI — AI, která rozhoduje, jaký experiment spustit jako další tam, kde jsou experimenty pomalé, drahé, destruktivní nebo dlouhodobé; cílem je zkrátit cestu od požadavku na materiál k validovanému materiálu s dostatkem důkazů, aby ho šlo nasadit

**Founder:** @charbjak  ·  **Project:** startup — https://gitlab.fit.cvut.cz/charbjak/startup

> Který vertikál × workflow × problém je ten správný první wedge — tedy kde lepší rozhodování o experimentech nezlepší R&D o 10–20 %, ale rozhodne o tom, jestli je program vůbec proveditelný?

**Tags:** `deeptech`, `materials`, `active-learning`, `qualification`, `ai`

## 📊 Market intelligence

Od říjnové rešerše se změnily tři věci a dvě z nich mění, co máš stavět. A jedno číslo jsem ti napsal špatně. První: „predikce kvalifikace" jsou dva různé produkty a říjnová rešerše je slévala. (A) Predikce výsledku laboratorní zkoušky. U ochranných nátěrů trvá cyklická kvalifikační zkouška podle ISO 12944 čtyři až šest měsíců — 2 688 hodin pro třídu C5 very high [[1]](https://socotec.co.uk/media/blog/understanding-iso-12944), 4 200 hodin pro offshore [[2]](https://www.icorr.org/iso-12944-9-defining-laboratory-test-methods-for-offshore-and-related-structures/) — ne roky. (B) Predikce chování v provozu. Tam roky jsou, jenže tam je sporná už sama laboratorní zkouška: v pětileté terénní studii 19 nátěrů na čtyřech lokalitách souhlasila solná mlha s terénem v 6 případech z 12 a systémy bez zinkového základu v laboratoři prošly a venku selhaly [[3]](https://doi.org/10.3390/cmd5040023). Kdo předpoví výsledek zkoušky, ještě nepředpověděl životnost. Druhá: nejsi první, kdo to zkouší. Projekt VIPCOAT (Horizon 2020, 5,5 mil. EUR, 2021–2025) stavěl platformu, která spojuje strojové učení s fyzikálními modely pro ochranné povlaky bez chromanů v letectví, s Airbusem a AkzoNobelem v konsorciu [[4]](https://materialsperformance.com/news/2021/05/eu-funds-55-million-corrosion-protection-platform). Ti lidé vědí, co nefungovalo. Třetí: obecná vrstva „rozhodni, co změřit dál" je dnes buď zdarma, nebo má za sebou stovky milionů. Merck dal svůj plánovač experimentů BayBE na GitHub pod licencí Apache 2.0 [[5]](https://www.emdgroup.com/en/news/opensource-ai-experimentation-planner-06-12-2023.html); CuspAI v červenci 2026 získala 450 mil. USD při ocenění 2,6 mld. [[6]](https://sifted.eu/articles/cuspai-lands-450m-round-to-accelerate-ai-materials-discovery). Mezi tím není místo pro další platformu. Oprava: bateriový dataset Seversona a Attiy má 124 článků, ne 169, jak stálo v říjnové rešerši i v issue [[7]](https://ui.adsabs.harvard.edu/abs/2019NatEn...4..383S/abstract). Chyby 9,1 % a 4,9 % platí.

**Why now:** Regulatorní kalendář se od října posunul o krok a je konkrétnější. U šestimocného chromu má výbor SEAC přijmout finální stanovisko v listopadu 2026; konzultace k jeho návrhu běžela od 17. 6. do 17. 8. [[8]](https://www.adcr-consortium.eu/echa-launches-crvi-consultation-on-draft-seac-opinion). Omezení má chromany přesunout z autorizace (příloha XIV REACH) do omezení (příloha XVII), protože počet žádostí o autorizaci přerostl kapacitu výborů. U PFAS přijal výbor RAC finální stanovisko 2. 3. 2026 [[9]](https://www.echa.europa.eu/-/echa-s-risk-assessment-committee-adopts-its-opinion-on-pfas-restriction-proposal) a SEAC má své dokončit do konce roku [[10]](https://www.echa.europa.eu/-/echa-s-socio-economic-analysis-committee-agrees-its-draft-opinion-on-pfas-restriction-proposal). Pak je na řadě Komise: návrhy tedy čekej v roce 2027 a přechodná období až po nich. Poptávka po přeformulování a nové kvalifikaci proto nevrcholí letos, ale v letech 2027 až 2029. Znamená to dvě věci. Máš čas udělat retrospektivní validaci dřív, než ji někdo bude chtít koupit. A nemáš čas vybírat vertikál další rok. K tomu politika a peníze: Advanced Materials Act má Komise v pracovním programu na čtvrté čtvrtletí 2026 a zatím ho nepředložila [[11]](https://www.europarl.europa.eu/legislative-train/theme-a-new-plan-for-europe-s-sustainable-prosperity-and-competitiveness/file-advanced-materials-act); výzvy HORIZON-CL4-2027-01 na pokročilé materiály mají uzávěrku 2. 2. 2027 [[12]](https://www.horizon-europe.gouv.fr/circular-innovative-advanced-materials-facilitating-transition-design-markets-ria-innovative-42693).
**Positioning:** Vyber si jeden ze dvou produktů a řekni to nahlas. (A) „Po šesti týdnech ti řeknu, jak dopadne tvoje pětiměsíční cyklická zkouška." Kupuje vedoucí vývoje u výrobce nátěrů. Data leží v archivech formulátorů a zkušeben, výsledek se dá ověřit za měsíce, a je to přesně tvar důkazu z baterií — prvních sto cyklů místo celé životnosti [[7]](https://ui.adsabs.harvard.edu/abs/2019NatEn...4..383S/abstract). Konkurencí jsou obecné platformy a zdarma BayBE [[5]](https://www.emdgroup.com/en/news/opensource-ai-experimentation-planner-06-12-2023.html); žádná z nich ale nemá časové řady z korozních komor. (B) „Řeknu ti, jak dlouho ten systém vydrží v provozu." Kupuje vlastník konstrukce nebo letecký výrobce. Správná odpověď vzniká roky a z laboratorní zkoušky ji podle terénních studií vzít nejde [[3]](https://doi.org/10.3390/cmd5040023) [[13]](https://onlinelibrary.wiley.com/doi/10.1002/maco.202313858). Na tomhle poli už stojí fyzikální simulace (Elsyca CorrosionMaster [[14]](https://www.digitalengineering247.com/article/corrosion-simulation-rust-never-sleeps)) a konsorcia jako VIPCOAT [[15]](https://ms.hereon.de/vipcoat). Doporučuju začít u A a B si nechat jako směr. A má rychlou zpětnou vazbu, data, která existují, a kupujícího s rozpočtem. A u nátěrů neříkej „7 až 15 let": to číslo patří leteckým materiálům a slitinám [[16]](https://www.cargroup.org/wp-content/uploads/2017/02/Material-Qualification.pdf). U nátěrů je bolest jinde — každá iterace receptury stojí čtyři až šest měsíců v komoře, takže přeformulování kvůli PFAS nebo chromanům znamená roky pokusů jdoucích za sebou.
**Whitespace / wedge:** Chybí dvě věci a obě se dají vlastnit. První je dataset: časové řady z cyklických zkoušek — průběžná hodnocení po jednotlivých cyklech, ne jen konečný verdikt — spárované s recepturou. Veřejně žádný takový není. Nejbližší popsaná práce trénovala na historických datech ze solné mlhy se 148 surovinami; navržené receptury obstály v cyklické zkoušce stejně nebo lépe než reference, ale autoři sami mluví o proof of principle a říkají, že receptury nebyly komerčně použitelné a že model neumí vysvětlit, proč fungují [[17]](https://www.european-coatings.com/news/people-careers/why-ai-makes-human-judgement-more-valuable-in-coatings/). Druhá je forma, ve které je predikce přijatelná. Tu nemusíš vymýšlet. REACH dovoluje nahradit zkoušku predikcí, když je model vědecky platný, látka leží v jeho aplikační doméně, výsledek stačí pro daný účel a všechno je zdokumentováno; OECD k tomu v roce 2023 vydala hodnoticí rámec, který posuzuje každou jednotlivou predikci, ne jen model [[18]](https://one.oecd.org/document/ENV/CBC/MONO%282023%2932/en/pdf). „Protokol predikce pro nátěrovou zkoušku" podle téhle šablony je konkrétní výstup, který dnes nikdo nedodává, a je to věc, o které se dá mluvit s akreditovanou zkušebnou [[19]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk).

### ✅ Strategic recommendations
- Rozhodni se mezi A a B do konce listopadu a napiš to jednou větou do README. „Predikce výsledku cyklické zkoušky z prvních týdnů" a „predikce životnosti v provozu" mají jiného kupujícího, jiná data a jinou konkurenci.
- Do každého rozhovoru přidej jednu otázku: „Zaznamenáváte u cyklické zkoušky průběžná hodnocení po jednotlivých cyklech, nebo jen výsledek na konci? A jak dlouho ty záznamy držíte?" Na odpovědi závisí, jestli se produkt A dá postavit z existujících dat.
- Retrospektivní validace zůstává první stavbou, teď s konkrétním zadáním: 30 až 50 dokončených cyklických zkoušek s průběžnými daty, konec si zakryj a ukaž, co předpovíš po šesti týdnech. Kde hledat: Technopark Kralupy [[20]](https://www.technopark-kralupy.cz/sluzby), SVÚOM [[19]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk), jeden výrobce nátěrů.
- Ozvi se lidem z VIPCOAT — Hereon, TU Delft, Fraunhofer ITWM [[15]](https://ms.hereon.de/vipcoat). Jedna otázka: co se stalo s platformou po dubnu 2025 a která část se v praxi ukázala jako nepoužitelná. Je to nejlevnější způsob, jak neopakovat čtyři roky cizí práce.
- Napiš predikční protokol pro jednu zkoušku podle rámce OECD [[18]](https://one.oecd.org/document/ENV/CBC/MONO%282023%2932/en/pdf): co přesně předpovídáš, pro jaké systémy model platí (pojiva, tloušťky, podklady), jak velká je nejistota a kdy model řekne „nevím". Dvě strany stačí a je to dokument, který si zákazník i zkušebna umí přečíst.
- Nech si udělat cenovou nabídku na jednu cyklickou zkoušku o 2 688 hodinách. Zkušebny ceny nezveřejňují [[21]](https://www.ri.se/en/materials-and-durability/corrosion/service/corrosion-testing-of-materials-coatings-and-products), a cena jedné iterace je přitom jediná cenová kotva, kterou máš.
- Konference AKI běží od dneška do pátku v Ústí nad Labem [[22]](https://www.aki-koroze.cz/konference.php). Jestli tam jsi, použij otázku z druhého bodu. Jestli ne, program a seznam přednášejících jsou hotový seznam lidí, kterým napsat.
- Do Horizon Europe nechoď jako koordinátor; uzávěrka 2. 2. 2027 je za dvanáct týdnů [[12]](https://www.horizon-europe.gouv.fr/circular-innovative-advanced-materials-facilitating-transition-design-markets-ria-innovative-42693). Reálné je být partnerem v konsorciu, které už někdo skládá. Zeptej se na to přímo na VŠCHT a v Technoparku.

### ⚠️ Key risks
- Záměna dvou produktů. Slíbíš životnost a postavíš predikci zkoušky; zákazník ten rozdíl pozná na první schůzce. Solná mlha je zkouška pro kontrolu kvality a i výrobce komor píše, že materiál může zkouškou projít a v provozu selhat [[23]](https://www.q-lab.com/Corrosion-test-standards/iso-9227).
- Data nemusí existovat v podobě, kterou potřebuješ. Jestli zkušebny archivují jen konečný protokol, časová řada není a produkt A se bez nových zkoušek natrénovat nedá. To je první věc, kterou je třeba zjistit.
- Obecná vrstva je zdarma nebo nedostižně financovaná: BayBE pod Apache 2.0 [[5]](https://www.emdgroup.com/en/news/opensource-ai-experimentation-planner-06-12-2023.html), CuspAI 450 mil. USD [[6]](https://sifted.eu/articles/cuspai-lands-450m-round-to-accelerate-ai-materials-discovery), Lila Sciences 550 mil. USD celkem [[24]](https://www.lila.ai/news/announcing-the-close-of-our-series-a), Periodic Labs 300 mil. USD už v seed kole [[25]](https://a16z.com/announcement/investing-in-periodic-labs/). Jestli tvůj první produkt zní jako oni, nesoutěžíš technologií, ale rozpočtem.
- Předchůdce s 5,5 mil. EUR, Airbusem a AkzoNobelem po sobě nenechal veřejně viditelný produkt [[26]](https://ms.hereon.de/vipcoat/109044/index.php.en). Buď je to těžší, než to vypadá, nebo zůstal výsledek uvnitř konsorcia. Než začneš stavět, zjisti, co z toho platí.
- Akceptace. Bez formy, kterou je někdo ochoten podepsat, je i správná predikce jen názor.
- Chybí chemik. Hledání spoluzakladatele z materiálové chemie zůstává podmínkou, ne doplňkem; konference tento týden je nejlevnější místo, kde ho potkat.
- Rozhodovací riziko trvá. Od říjnového issue uběhlo pět týdnů a vertikál vybraný není. Regulace ti dává čas do roku 2027, ale ne na výběr.

### Kdo to už zkusil a kdo co prodává
Říjnová rešerše popsala obecné platformy a autonomní laboratoře. Chyběli v ní ti nejbližší: evropský projekt, který stavěl skoro totéž pro letecké povlaky, firma, která korozi simuluje fyzikálně, a nástroj, který obecnou vrstvu rozdává zdarma.
- VIPCOAT — „Virtual Open Innovation Platform for active protective coatings guided by modelling and optimization“. Horizon 2020, grant 952903, 5 519 625 EUR, 1. 5. 2021 až duben 2025. Koordinátor Helmholtz-Zentrum Hereon; v konsorciu Airbus, AkzoNobel, Fraunhofer ITWM, SINTEF Ocean, Smallmatek, TU Delft, Elsyca, LIST, NTNU a VUB.
- Cíl VIPCOAT: platforma kombinující strojové učení a fyzikální modely, která pomáhá vyvíjet povlaky a zrychlené zkoušky životnosti, nejdřív pro letectví a náhradu chromanů. Prototyp byl online na podzim 2022; aplikace zahrnovaly hledání inhibitorů koroze strojovým učením, uvolňování inhibitoru z povlaku a korozi v defektu.
- Co po projektu zůstalo veřejně k použití, se z webu zjistit nedá. To je otázka na lidi z konsorcia, ne na vyhledávač.
- Elsyca (Belgie), člen téhož konsorcia, prodává CorrosionMaster: fyzikální simulaci, která hledá korozní ohniska a počítá rychlost koroze, modeluje degradaci nátěru a sčítá poškození po dobu životnosti. Referenční případ je galvanická koroze dveří Audi A6. To je produkt B řešený fyzikou, ne daty.
- BayBE: plánovač experimentů od Merck KGaA a Acceleration Consortium z Toronta, od prosince 2023 na GitHubu pod Apache 2.0. Umí víc cílů najednou, transfer learning a aktivní učení a u Mercku pohání desítky použití včetně samoobslužného plánovače pro laboranty. Obecné „co změřit dál“ je tedy zadarmo.
- Intellegens (Cambridge) prodává Alchemite jako nástroj pro návrh experimentů nad řídkými a zašuměnými daty; zůstává nejbližším komerčním sousedem obecné verze tvé myšlenky.
- MaterialsZone uvádí u evropského dodavatele surovin o 56 % méně fyzických zkoušek při přeformulování dekorativních barev při zachování kryvosti, lesku a odolnosti proti oděru. Je to tvrzení dodavatele a jde o dekorativní barvy, ne o protikorozní ochranu.
- Albert Invent (chemie v podnikovém vývoji) a Entalpic (Grenoble, vlastní laboratoř) míří na chemický průmysl obecně; korozní kvalifikaci jako produkt nenabízí nikdo z nich.
- Zkušebny dál prodávají kapacitu komor, ne rozhodnutí: v Česku SVÚOM (akreditovaná zkušebna č. 1096) a Technopark Kralupy VŠCHT. Právě ony ale drží data a zákazníky, takže jsou spíš tvůj kanál než konkurence.

_Sources:_ [[15]](https://ms.hereon.de/vipcoat) [[4]](https://materialsperformance.com/news/2021/05/eu-funds-55-million-corrosion-protection-platform) [[26]](https://ms.hereon.de/vipcoat/109044/index.php.en) [[14]](https://www.digitalengineering247.com/article/corrosion-simulation-rust-never-sleeps) [[5]](https://www.emdgroup.com/en/news/opensource-ai-experimentation-planner-06-12-2023.html) [[27]](https://pubs.rsc.org/en/content/articlehtml/2025/dd/d5dd00050e) [[28]](https://intellegens.com/solutions/) [[29]](https://www.pcimag.com/articles/115507-half-the-lab-work-same-paint-performance) [[30]](https://techcrunch.com/2024/12/11/albert-invent-hopes-to-revolutionize-the-chemicals-sector-with-its-ai-platform) [[31]](https://entalpic.ai/) [[19]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) [[20]](https://www.technopark-kralupy.cz/sluzby)

### Co se v nátěrech opravdu změřilo: důkazy pro i proti
Metoda funguje tam, kde někdo vyrobil data. V nátěrech existuje pár malých důkazů, že to jde, a dvě terénní studie, které říkají, že laboratorní zkouška sama o provozu vypovídá málo.
- Baterie, opraveno: Severson, Attia a spol. (Nature Energy 2019) měli 124 komerčních LFP/grafitových článků s životností 150 až 2 300 cyklů. Životnost předpověděli s chybou 9,1 % z prvních 100 cyklů a zařazení do dvou skupin s chybou 4,9 % z prvních 5 cyklů. V říjnu jsem uváděl 169 článků; to bylo špatně.
- Nátěry, historická data: v práci popsané v European Coatings (srpen 2026) trénovali výzkumníci na historických výsledcích solné mlhy se 148 surovinami. Model navrhl dvě receptury s neintuitivní kombinací složek; v cyklické zkoušce chránily stejně nebo lépe než reference. Autoři to označují za proof of principle, receptury nebyly komerčně použitelné a model neumí říct, proč fungují.
- Nátěry, malá data: tým s TU Delft optimalizoval samohojivý epoxid z 32 výchozích receptur (ortogonální návrh) pomocí bayesovské optimalizace a ověřil ho 60 dny v neutrální solné mlze (npj Materials Degradation, 2024).
- Nátěry, terén: dvoustupňový model v npj Materials Degradation (2025) spojuje roční venkovní expozici polyuretanu na devíti lokalitách s cyklováním UV a solné mlhy v laboratoři. Je to jedna z mála prací, která výslovně páruje terén a komoru.
- Proti: 19 organických nátěrů pro ocelové vodní konstrukce, 5 let v terénu na 4 lokalitách (2024). Neutrální solná mlha korelovala s terénem v 6 případech z 12; největší rozdíl byl u systémů bez zinkového základu, které v laboratoři prošly a venku selhaly.
- Proti: roční venkovní expozice akrylátem natřené oceli, hliníku a pozinku proti několika komorovým zkouškám (Materials and Corrosion, 2023). Závěr autorů: žádná z komorových zkoušek přirozenou expozici správně nesimulovala.
- Přehled strojového učení pro povlaky v ACS Applied Materials & Interfaces (2025) jmenuje tři překážky: dostupnost, kvalitu a standardizaci dat; interpretovatelnost modelů; a začlenění do zavedeného postupu formulace. Na prvním místě jsou data, stejně jako v tvém seznamu kritérií.
- Co chybí úplně: práce, která by z prvních týdnů cyklické zkoušky předpověděla její konec. To je přesný protějšek bateriového důkazu a zároveň tvoje retrospektivní validace.

_Sources:_ [[7]](https://ui.adsabs.harvard.edu/abs/2019NatEn...4..383S/abstract) [[17]](https://www.european-coatings.com/news/people-careers/why-ai-makes-human-judgement-more-valuable-in-coatings/) [[32]](https://research.tudelft.nl/en/publications/machine-learning-assisted-discovery-of-high-efficiency-self-heali) [[33]](https://www.nature.com/articles/s41529-025-00614-6) [[3]](https://doi.org/10.3390/cmd5040023) [[13]](https://onlinelibrary.wiley.com/doi/10.1002/maco.202313858) [[34]](https://www.european-coatings.com/news/coatings-technologies/machine-learning-transforms-design-of-surface-coatings/)

### V jaké podobě je predikce přijatelná jako důkaz
Akceptaci jsi měl mezi riziky. Existuje pro ni hotová šablona ve stejné regulatorní rodině, která tvůj problém vyrábí: chemická legislativa už predikci místo zkoušky přijímá a ví přesně, co k tomu chce vidět.
- REACH, příloha XI, bod 1.3: výsledek (Q)SAR modelu smí nahradit zkoušku, když jsou splněny čtyři podmínky — model je vědecky platný, látka spadá do jeho aplikační domény, výsledek je dostatečný pro daný regulatorní účel a metoda je přiměřeně zdokumentována.
- OECD (Q)SAR Assessment Framework (2023) posuzuje každou jednotlivou predikci, ne jen model: platný model nezaručuje platnost každého svého výsledku. K tomu patří kontrolní seznamy a dva formuláře — jeden popisuje model, druhý konkrétní predikci.
- ECHA rámec používá při hodnocení dokumentací; v březnu 2024 k němu pořádala webinář a uvádí, že shrnuje zhruba deset let její praxe s hodnocením predikcí.
- Přeloženo do tvého světa: cílová veličina je výsledek normované zkoušky (stupeň puchýřkování, koroze od řezu, přilnavost po expozici), aplikační doména je vymezení pojiv, pigmentů, tlouštěk a podkladů, pro které má model data, a ke každé predikci patří nejistota a věta, kdy model odpovědět neumí.
- Akceptace není automatická ani u chemikálií — závisí na účelu a na konkrétní veličině. Šablona ti nedá razítko, dá ti jazyk, kterému regulatorní a kvalitářská oddělení už rozumějí.
- V letectví se kvalifikace opakuje: MIL-PRF-85285 pro polyuretanové vrchní nátěry se ověřuje ve dvouletých intervalech. Kde se zkouška opakuje, vzniká i opakovaná potřeba doložit, že se nic nezměnilo.
- Akreditovaná zkušebna (ČSN EN ISO/IEC 17025) je přirozený spolupodpis: predikce vydaná spolu se zkušebnou, která pak výsledek skutečně změří, je nabídka, ve které se zákazník nemusí rozhodovat mezi modelem a zkouškou.

_Sources:_ [[18]](https://one.oecd.org/document/ENV/CBC/MONO%282023%2932/en/pdf) [[35]](https://echa.europa.eu/documents/10162/74278515/210324_qsar_webinar_qa_en.pdf/f19f111f-0896-709c-77f2-a45aa501e39f) [[36]](https://www.valencesurfacetech.com/the-news/mil-prf-85285-type-1/) [[19]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk)

### Kde ta data jsou — a v jaké podobě
Dostupnost dat zůstává prvním filtrem. Nově je jasnější, jaká data přesně potřebuješ: ne konečné protokoly, ale průběh zkoušky v čase.
- Pro produkt A potřebuješ průběžná hodnocení z cyklických zkoušek — fotografie nebo stupně hodnocení po jednotlivých týdenních cyklech — spojená s recepturou a výsledkem na konci. Jestli je zkušebny a výrobci zaznamenávají a archivují, veřejné zdroje neříkají.
- V Česku se takové zkoušky dělají v Technoparku Kralupy VŠCHT (urychlené korozní a klimatické zkoušky pro průmysl) a v SVÚOM, který má akreditované zkoušky podle ISO 9227, VDA 621-415, SAE J 2334 a ISO 11997-1 cyklus B.
- Veřejná terénní data pro organické povlaky jsou vzácná. Jedna dohledatelná sada je venkovní studie NIST z Gaithersburgu z let 2002–2006 se 36 vzorky sledovanými infračervenou spektroskopií; v roce 2025 ji znovu použila práce o modelování degradace.
- NIMS (Japonsko) zveřejňuje dlouhodobé korozní datové listy, jde ale o kovy, ne o nátěrové systémy. Pro vertikál nátěrů je to inspirace, jak má taková sada vypadat, ne trénovací data.
- Devět lokalit a roční expozice v práci z npj Materials Degradation (2025) ukazuje, jak velký terénní dataset dnes stačí na publikaci. Na produkt je to málo, na společný projekt se zkušebnou dost.
- Z toho plyne nabídka pro první rozhovor o datech: zpracuju vám archiv cyklických zkoušek a vrátím vám, které zkoušky šlo ukončit dřív. Zkušebna tím získá argument pro zákazníka, ty dataset.

_Sources:_ [[20]](https://www.technopark-kralupy.cz/sluzby) [[19]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) [[37]](https://arxiv.org/abs/2504.05484) [[38]](https://cods.nims.go.jp/) [[33]](https://www.nature.com/articles/s41529-025-00614-6)

### Normy a hodiny: co přesně by predikce zkracovala
Kvalifikace nátěrového systému je definovaná počtem hodin v komoře. To číslo je menší, než naznačuje tvůj pitch, a o to snáz se s ním počítá.
- ISO 12944-9 (offshore, kategorie CX): cyklické stárnutí v týdenních cyklech — 72 hodin UV a kondenzace, 72 hodin solné mlhy, 24 hodin při −20 °C — opakované 25krát, tedy 4 200 hodin, zhruba půl roku.
- ISO 12944-6: pro kategorii C5 a životnost very high se uvádí 16 cyklů, tedy 2 688 hodin (112 dní). Životnost very high znamená víc než 25 let; zkouška za čtyři měsíce tedy zastupuje čtvrt století provozu.
- U kterých nižších kategorií je cyklická zkouška povinná a kde volitelná, se sekundární zdroje neshodnou. Než to někomu řekneš, ověř si to v normě samotné.
- ISO 9227 (neutrální solná mlha) je zkouška pro kontrolu kvality a porovnání. I výrobce zkušebních komor uvádí, že některé materiály nebo nátěry zkouškou projdou a v reálném prostředí selžou, protože zkouška nenapodobuje střídání vlhkosti a teploty.
- Cyklické zkoušky se považují za bližší provozu než trvalá solná mlha; ISO 12944-9 kombinuje UV, solnou mlhu a mráz. Ani u nich ale není shoda s terénem zaručená.
- Víceleté lhůty z tvého pitche platí pro letecké a automobilové materiály obecně: kvalifikace nového materiálu se tam počítá na roky a každá změna procesu může vynutit další. U nátěrů na ocelové konstrukce je jednotkou času iterace o čtyřech až šesti měsících.

_Sources:_ [[2]](https://www.icorr.org/iso-12944-9-defining-laboratory-test-methods-for-offshore-and-related-structures/) [[1]](https://socotec.co.uk/media/blog/understanding-iso-12944) [[23]](https://www.q-lab.com/Corrosion-test-standards/iso-9227) [[19]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) [[16]](https://www.cargroup.org/wp-content/uploads/2017/02/Material-Qualification.pdf)

### Proč teď: kalendář omezení a co z něj plyne
Obě velká omezení jsou o krok dál než v říjnu a žádné ještě není přijaté. Tlak je skutečný, ale jeho vrchol leží v letech 2027 až 2029.
- Šestimocný chrom: návrh omezení má vybrané sloučeniny Cr(VI) přesunout z přílohy XIV (autorizace) do přílohy XVII (omezení), protože počet žádostí o autorizaci přesáhl kapacitu výborů ECHA.
- Stav: RAC své stanovisko přijal; konzultace k návrhu stanoviska SEAC běžela od 17. 6. do 17. 8. 2026; finální stanovisko SEAC se čeká v listopadu 2026. Potom rozhoduje Komise.
- Kosmický průmysl (Eurospace, srpen 2026) varuje před navrženými limity a dopadem na dodavatelský řetězec. Letectví a obrana mají do té doby dvanáctiletou autorizaci chromanů.
- PFAS: RAC přijal finální stanovisko 2. 3. 2026, SEAC se shodl na návrhu svého 10. 3., konzultace skončila 25. 5. a finální stanovisko SEAC se čeká do konce roku 2026. Návrh aktu Komise zatím neexistuje.
- Důsledek pro tebe: přeformulování s pevným datem přijde, až bude známé přechodné období, tedy nejdřív v roce 2027. Kdo bude mít do té doby ověřenou metodu, bude ji mít komu nabídnout.
- Advanced Materials Act: v pracovním programu Komise na 4. čtvrtletí 2026, veřejná konzultace skončila 13. 1. 2026, návrh zatím předložen nebyl.
- Substituce kritických surovin zůstává nejslaběji obsazenou částí Critical Raw Materials Act: ze 47 strategických projektů jsou jen dva substituční. Má politickou prioritu a peníze, ale ne termín.

_Sources:_ [[8]](https://www.adcr-consortium.eu/echa-launches-crvi-consultation-on-draft-seac-opinion) [[39]](https://echa.europa.eu/registry-of-restriction-intentions/-/dislist/details/0b0236e18971243a) [[40]](https://eurospace.org/eurospace-warns-against-prohibitive-limit-values-and-space-supply-chain-risks-in-proposed-eu-chromiumvi-restriction-under-eu-reach/) [[41]](https://www.asd-europe.org/news-media/news-events/news/eu-grants-12-year-authorisation-for-chromates/) [[9]](https://www.echa.europa.eu/-/echa-s-risk-assessment-committee-adopts-its-opinion-on-pfas-restriction-proposal) [[10]](https://www.echa.europa.eu/-/echa-s-socio-economic-analysis-committee-agrees-its-draft-opinion-on-pfas-restriction-proposal) [[11]](https://www.europarl.europa.eu/legislative-train/theme-a-new-plan-for-europe-s-sustainable-prosperity-and-competitiveness/file-advanced-materials-act) [[42]](https://ieu-monitoring.com/editorial/raw-materials-in-europe-eu-commission-selects-47-strategic-projects-to-diversify-access/551430)

### Kdo kupuje: tři role a jedna cesta k nim
V říjnu jsem po tobě chtěl roli kupujícího. Tady je, jak to vypadá z veřejných zdrojů; počty chybějí a doplnit je můžeš jen ty z rozhovorů.
- Výrobce nátěrů, vedoucí vývoje — kupující produktu A. Platí za každou iteraci receptury měsíci v komoře a kvůli PFAS a chromanům ho čeká přeformulování celých řad. Otázka pro něj: kolik iterací ročně a kolik z nich skončilo až na konci zkoušky neúspěchem.
- Vlastník konstrukce nebo letecký výrobce — kupující produktu B. Rozhoduje o nasazení systému a nese následky. Chce důkaz o provozu, ne o zkoušce, a predikci přijme jen ve formě, kterou podepíše jeho oddělení kvality.
- Zkušebna — kanál, ne zákazník. Má komory, data i zákazníky obou typů. Predikce jako doplněk ke zkoušce („po šesti týdnech vám řekneme, kam to míří“) je služba, kterou může prodávat pod svou akreditací.
- V Česku jsou dvě místa, kde se potkává všechno najednou: Technopark Kralupy VŠCHT a SVÚOM. Obě máš mezi otevřenými kontakty.
- Konference AKI (11.–13. 11. 2026, Ústí nad Labem) má letos téma silnostěnné organické povlaky — tedy přesně systémy, které se kvalifikují podle ISO 12944.
- Co veřejné zdroje neřeknou: kolik výrobců v Česku a v EU cyklické zkoušky vůbec zadává, jak často, a kdo je platí. Tři rozhovory to změní z odhadu na číslo.

_Sources:_ [[20]](https://www.technopark-kralupy.cz/sluzby) [[19]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) [[22]](https://www.aki-koroze.cz/konference.php) [[2]](https://www.icorr.org/iso-12944-9-defining-laboratory-test-methods-for-offshore-and-related-structures/)

### Velikost trhu: kategorie je malá, jednotkou je cena jedné iterace
Čísla shora dolů zůstávají jen kontextem. Užitečné číslo je jedno a zatím ho nemáš: co stojí jedna cyklická zkouška a kolik jich zákazník za rok udělá.
- Kategorie „AI v objevování materiálů“ se odhaduje na necelou miliardu dolarů v roce 2026; „materials informatics“ na 0,2 až 0,4 mld. USD podle toho, kdo počítá. Rozptyl říká, že se analytici neshodnou, co do kategorie patří. (Údaje z října, znovu neověřováno.)
- Trh, kterého se dotýkáš, je o řád větší: ochranné a lodní nátěry přes 22 mld. USD ročně. Tvůj podíl na něm ale není procento z tržeb, je to cena ušetřeného času ve vývoji.
- Cenu zkoušky žádná laboratoř nezveřejňuje; švédský institut RISE i další uvádějí jen „cena na vyžádání“. Cenová nabídka od české zkušebny je proto první tvrdé číslo, které můžeš mít do týdne.
- Výpočet zdola, který si doplníš: počet iterací za rok × (cena zkoušky + měsíce zdržení × cena měsíce vývojového týmu) × podíl iterací, které šlo ukončit dřív. Bez prvních dvou čísel je každý odhad trhu jen tvar.
- Pro srovnání hodnoty: dodavatel obecné platformy uvádí u dekorativních barev o 56 % méně fyzických zkoušek. U protikorozních systémů, kde jedna zkouška trvá měsíce, má stejné procento násobně větší cenu.

_Sources:_ [[43]](https://www.researchandmarkets.com/reports/6227043/ai-in-materials-discovery-global-market-report) [[44]](https://www.meticulousresearch.com/product/materials-informatics-market-6787) [[45]](https://www.businessresearchinsights.com/market-reports/protective-marine-coatings-market-101594) [[21]](https://www.ri.se/en/materials-and-durability/corrosion/service/corrosion-testing-of-materials-coatings-and-products) [[29]](https://www.pcimag.com/articles/115507-half-the-lab-work-same-paint-performance)

### Peníze: kdo je dostal a odkud je můžeš vzít ty
Rizikový kapitál se za poslední rok přesunul k obecné vrstvě v řádu stovek milionů. Pro úzký, regulací ohraničený problém jsou reálnější evropské projektové peníze a první platící zkušebna.
- CuspAI: 450 mil. USD v sérii B při ocenění 2,6 mld. USD (červenec 2026), kolo vedly Kleiner Perkins a NEA; současně ohlásila „AI Materials Foundry“ s více než 45 partnery. Ocenění při sérii A v září 2025 bylo 520 mil. USD.
- Periodic Labs: 300 mil. USD v seed kole vedeném Andreessen Horowitz (podzim 2025). Říjnová rešerše uváděla 550,7 mil. USD; to číslo zdroje nepotvrzují.
- Lila Sciences: 350 mil. USD v sérii A, 550 mil. USD celkem, na autonomní „AI Science Factories“.
- Albert Invent (22,5 mil. USD, série A) a Entalpic (8,5 mil. EUR, seed) zůstávají příkladem toho, kolik stojí obecná platforma pro chemii. (Údaje z října.)
- Horizon Europe, výzva HORIZON-CL4-2027-01, uzávěrka 2. 2. 2027: téma MAT-PROD-06 o cirkulárních pokročilých materiálech (36 mil. EUR, výslovně zmiňuje digitální nástroje, FAIR data a postupy založené na AI) a MAT-PROD-22 o materiálech a procesech snižujících závislost na kritických surovinách.
- Výzva na urychlení vývoje materiálů pomocí AI z roku 2026 je uzavřená; kdo ji vyhrál, je seznam konsorcií, která tvoje téma právě řeší — a tedy možných partnerů.
- Nejkratší cesta k prvním penězům nevede přes investora ani grant, ale přes zkušebnu nebo výrobce, který zaplatí za zpracování svého archivu.

_Sources:_ [[6]](https://sifted.eu/articles/cuspai-lands-450m-round-to-accelerate-ai-materials-discovery) [[25]](https://a16z.com/announcement/investing-in-periodic-labs/) [[46]](https://siliconangle.com/2025/10/01/periodic-labs-raises-300m-accelerate-scientific-research-ai/) [[24]](https://www.lila.ai/news/announcing-the-close-of-our-series-a) [[30]](https://techcrunch.com/2024/12/11/albert-invent-hopes-to-revolutionize-the-chemicals-sector-with-its-ai-platform) [[31]](https://entalpic.ai/) [[12]](https://www.horizon-europe.gouv.fr/circular-innovative-advanced-materials-facilitating-transition-design-markets-ria-innovative-42693) [[47]](https://www.euacc.ai/calls/HORIZON-CL4-2027-01-MAT-PROD-22)

## 🔗 Sources  ·  all links
1. [socotec.co.uk](https://socotec.co.uk/media/blog/understanding-iso-12944)
2. [icorr.org](https://www.icorr.org/iso-12944-9-defining-laboratory-test-methods-for-offshore-and-related-structures/)
3. [doi.org](https://doi.org/10.3390/cmd5040023)
4. [materialsperformance.com](https://materialsperformance.com/news/2021/05/eu-funds-55-million-corrosion-protection-platform)
5. [emdgroup.com](https://www.emdgroup.com/en/news/opensource-ai-experimentation-planner-06-12-2023.html)
6. [sifted.eu](https://sifted.eu/articles/cuspai-lands-450m-round-to-accelerate-ai-materials-discovery)
7. [ui.adsabs.harvard.edu](https://ui.adsabs.harvard.edu/abs/2019NatEn...4..383S/abstract)
8. [adcr-consortium.eu](https://www.adcr-consortium.eu/echa-launches-crvi-consultation-on-draft-seac-opinion)
9. [echa.europa.eu](https://www.echa.europa.eu/-/echa-s-risk-assessment-committee-adopts-its-opinion-on-pfas-restriction-proposal)
10. [echa.europa.eu](https://www.echa.europa.eu/-/echa-s-socio-economic-analysis-committee-agrees-its-draft-opinion-on-pfas-restriction-proposal)
11. [europarl.europa.eu](https://www.europarl.europa.eu/legislative-train/theme-a-new-plan-for-europe-s-sustainable-prosperity-and-competitiveness/file-advanced-materials-act)
12. [horizon-europe.gouv.fr](https://www.horizon-europe.gouv.fr/circular-innovative-advanced-materials-facilitating-transition-design-markets-ria-innovative-42693)
13. [onlinelibrary.wiley.com](https://onlinelibrary.wiley.com/doi/10.1002/maco.202313858)
14. [digitalengineering247.com](https://www.digitalengineering247.com/article/corrosion-simulation-rust-never-sleeps)
15. [ms.hereon.de](https://ms.hereon.de/vipcoat)
16. [cargroup.org](https://www.cargroup.org/wp-content/uploads/2017/02/Material-Qualification.pdf)
17. [european-coatings.com](https://www.european-coatings.com/news/people-careers/why-ai-makes-human-judgement-more-valuable-in-coatings/)
18. [one.oecd.org](https://one.oecd.org/document/ENV/CBC/MONO%282023%2932/en/pdf)
19. [svuom.cz](https://svuom.cz/index.php?lang=cz&zobraz=akrzk)
20. [technopark-kralupy.cz](https://www.technopark-kralupy.cz/sluzby)
21. [ri.se](https://www.ri.se/en/materials-and-durability/corrosion/service/corrosion-testing-of-materials-coatings-and-products)
22. [aki-koroze.cz](https://www.aki-koroze.cz/konference.php)
23. [q-lab.com](https://www.q-lab.com/Corrosion-test-standards/iso-9227)
24. [lila.ai](https://www.lila.ai/news/announcing-the-close-of-our-series-a)
25. [a16z.com](https://a16z.com/announcement/investing-in-periodic-labs/)
26. [ms.hereon.de](https://ms.hereon.de/vipcoat/109044/index.php.en)
27. [pubs.rsc.org](https://pubs.rsc.org/en/content/articlehtml/2025/dd/d5dd00050e)
28. [intellegens.com](https://intellegens.com/solutions/)
29. [pcimag.com](https://www.pcimag.com/articles/115507-half-the-lab-work-same-paint-performance)
30. [techcrunch.com](https://techcrunch.com/2024/12/11/albert-invent-hopes-to-revolutionize-the-chemicals-sector-with-its-ai-platform)
31. [entalpic.ai](https://entalpic.ai/)
32. [research.tudelft.nl](https://research.tudelft.nl/en/publications/machine-learning-assisted-discovery-of-high-efficiency-self-heali)
33. [nature.com](https://www.nature.com/articles/s41529-025-00614-6)
34. [european-coatings.com](https://www.european-coatings.com/news/coatings-technologies/machine-learning-transforms-design-of-surface-coatings/)
35. [echa.europa.eu](https://echa.europa.eu/documents/10162/74278515/210324_qsar_webinar_qa_en.pdf/f19f111f-0896-709c-77f2-a45aa501e39f)
36. [valencesurfacetech.com](https://www.valencesurfacetech.com/the-news/mil-prf-85285-type-1/)
37. [arxiv.org](https://arxiv.org/abs/2504.05484)
38. [cods.nims.go.jp](https://cods.nims.go.jp/)
39. [echa.europa.eu](https://echa.europa.eu/registry-of-restriction-intentions/-/dislist/details/0b0236e18971243a)
40. [eurospace.org](https://eurospace.org/eurospace-warns-against-prohibitive-limit-values-and-space-supply-chain-risks-in-proposed-eu-chromiumvi-restriction-under-eu-reach/)
41. [asd-europe.org](https://www.asd-europe.org/news-media/news-events/news/eu-grants-12-year-authorisation-for-chromates/)
42. [ieu-monitoring.com](https://ieu-monitoring.com/editorial/raw-materials-in-europe-eu-commission-selects-47-strategic-projects-to-diversify-access/551430)
43. [researchandmarkets.com](https://www.researchandmarkets.com/reports/6227043/ai-in-materials-discovery-global-market-report)
44. [meticulousresearch.com](https://www.meticulousresearch.com/product/materials-informatics-market-6787)
45. [businessresearchinsights.com](https://www.businessresearchinsights.com/market-reports/protective-marine-coatings-market-101594)
46. [siliconangle.com](https://siliconangle.com/2025/10/01/periodic-labs-raises-300m-accelerate-scientific-research-ai/)
47. [euacc.ai](https://www.euacc.ai/calls/HORIZON-CL4-2027-01-MAT-PROD-22)

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