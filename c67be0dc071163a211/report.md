# Prediktivní kvalifikace ochranných povlaků — AI zkracuje 7–15leté zkoušky stárnutí, degradace a ekologického dopadu u povlaků pro letectví a lodní dopravu

**Founder:** @charbjak  ·  **Project:** startup — https://gitlab.fit.cvut.cz/charbjak/startup

> Lze z krátkých zrychlených zkoušek a historických dat předpovědět výsledek několikaletého kvalifikačního programu podle konkrétní normy tak, aby predikce byla akceptovatelná jako podklad rozhodnutí?

**Tags:** `deeptech`, `materials`, `coatings`, `aerospace`, `ai`

## 📊 Market intelligence

Trh, na který tato myšlenka míří, není 'AI navrhuje materiály', ale **kvalifikace** materiálu: než se nový povlak dostane na letadlo nebo trup lodi, musí projít několikaletým programem zkoušek stárnutí, degradace a korozní odolnosti. Ochranné a marine povlaky jsou samy o sobě trh ~22,4 mld. USD (2026) a letecké povlaky další ~1,2–3,9 mld. USD (odhady se mezi analytiky výrazně liší); zkoušení materiálů jako služba je ~3,9–6,6 mld. USD. Prodejné je zkrácení a zlevnění jednoho konkrétního kvalifikačního rozhodnutí, ne obecné hledání materiálů.

**Why now:** Evropská regulace právě vynucuje přeformulování prakticky celého portfolia ochranných povlaků — a každé přeformulování znamená novou, několikaletou kvalifikaci. (1) PFAS: ECHA uzavřela finální konzultaci 25. 5. 2026, RAC vydal finální a SEAC návrh stanoviska podporující celoevropské omezení, žádost průmyslu vyjmout fluoropolymery SEAC nepřijal, vědecké hodnocení se má dokončit do konce 2026; návrh pokrývá >10 000 látek. (2) Cr(VI): chromáty pro aerospace/defence dostaly 12letou autorizaci, ale ECHA chystá široké omezení Cr(VI) s přijetím cca září 2026 / začátek 2027 — tedy tlak na chrome-free primery, u nichž dosud nikdo spolehlivě neprokázal stejnou korozní ochranu. Reformulační vlna + neměnně dlouhé zkoušky = poptávka po prediktivní kvalifikaci právě teď.
**Positioning:** Ne 'materials discovery platforma' (tam už je Citrine, MaterialsZone, Polymerize, Osium AI, Radical AI), ale **prediktivní kvalifikace povlaků**: z krátkých zrychlených zkoušek a historických dat předpovědět výsledek dlouhého kvalifikačního programu pro konkrétní normu (ISO 9227, ISO 11997-1 cycle B, VDA 621-415, SAE J2334, MIL-PRF-85285). Hodnota není v přesnosti modelu, ale v tom, že predikce je **akceptovatelná jako podklad rozhodnutí** — tedy napojená na normy a na akreditovanou laboratoř (ISO/IEC 17025).
**Whitespace / wedge:** Publikované ML modely predikce životnosti povlaků existují (dvoustupňový model 'prostředí → fyzikální vlastnost → korozní porucha' v npj Materials Degradation 2025, CNN pro epoxidy v hlubokomořském prostředí s chybou 2,6 %, semi-supervised model atmosférického stárnutí akrylátů) — metoda tedy sama o sobě není obhajitelná výhoda. Nikdo z financovaných hráčů ale nevlastní **kvalifikační workflow pro letecké a marine povlaky**: materials-informatics platformy řeší formulaci, self-driving laby (Radical AI, Argonne Polybot) řeší syntézu a screening, zkušebny (Q-Lab, Element, SVÚOM) prodávají hodiny v komoře, ne rozhodnutí. Mezera je mezi nimi: data z komor + terénu → predikce → akceptovaná evidence.

### ✅ Strategic recommendations
- Zvol JEDNO kvalifikační rozhodnutí, které chceš vytlačit — např. 'projde tento chrome-free primer 2000h ISO 9227 a cyklickou zkoušku?' — a měř se proti němu. 'Zrychlujeme vývoj materiálů' není prodejné tvrzení.
- Data před cofounderem: bez označkovaných dat (zrychlené zkoušky spárované s terénní expozicí) není co trénovat. V ČR ta data fyzicky existují — Technopark Kralupy VŠCHT (~100 průmyslových kontraktů ročně) a akreditovaná zkušebna SVÚOM (zkušebna č. 1096, ISO/IEC 17025). Dohoda o datech je reálný moat, ne model.
- Dva termíny v příštích šesti týdnech, kde je celá česká komunita povlaků pohromadě: konference Pigmenty a pojiva 4.–6. 11. 2026 (hotel Jezerka u Sečské přehrady) a 29. konference AKI 11.–13. 11. 2026 (Clarion, Ústí nad Labem) — letošní téma AKI je přímo 'silnostěnné organické povlaky'. Cíl: cofounder + 10 zákaznických rozhovorů do konce listopadu.
- Why-now vyprávěj přes regulaci (PFAS + Cr(VI) reformulační vlna), ne přes 'AI umí navrhnout materiál za den'. Regulace je to, co rozpočet uvolňuje.
- Coatings před bateriemi je správné rozhodnutí — u povlaků existuje opakovaná re-kvalifikace (u MIL-PRF-85285 probíhá periodické ověření ve dvouletých intervalech od původní kvalifikace), což je opakovaný příjem; u baterií je cyklus delší, kapitálově těžší a uzavřený na OEM.
- Ověř ochotu platit číslem, ne názorem: zjisti u 5 formulátorů, kolik je dnes stojí jeden kvalifikační program (fakturace zkušebny + zdržení uvedení na trh v měsících).
- Počítej s tím, že zákazník nemůže tvou predikci rychle ověřit (proto ten problém existuje) — potřebuješ retrospektivní validaci na historických datech, kde už je znám výsledek po 7–15 letech.

### ⚠️ Key risks
- Akceptace, ne přesnost: predikce, která se nedá napojit na normu a akreditovanou zkušebnu, nemá v kvalifikaci hodnotu. Toto je hlavní riziko celého podnikání.
- Přístup k datům: označkovaná data o stárnutí drží zkušebny a formulátoři a jsou důvěrná. Bez smluvního přístupu není produkt.
- Metoda je publikovaná (npj Materials Degradation, Nature Sci. Rep., MDPI Polymers) → z modelu nevznikne IP výhoda; obhajitelné je jen data + workflow + certifikační vztahy.
- Kapitálově silná konkurence s leteckým akcionářem: Radical AI má 55 mil. USD seed vedený RTX Ventures (RTX = letecký koncern) a NVentures.
- Dlouhý prodejní cyklus v aerospace/defence a malý počet rozhodovatelů — trh je úzký a konzervativní; to je dobré pro moat a špatné pro rychlost učení.
- Závislost na cofounderovi: bez materiálového chemika nebude tvrzení o degradaci důvěryhodné ani pro zákazníka, ani pro investora.

### Kolik je na trhu peněz — a kde z nich je adresovatelná část
Povlaky samotné jsou velký a pomalu rostoucí trh; adresovatelná je ale jen ta část rozpočtu, která dnes odtéká do kvalifikačních zkoušek a do zdržení uvedení na trh. Analytické odhady se mezi sebou liší až trojnásobně, takže shora-dolů čísla používej jen jako kontext a rozhodnutí opři o bottom-up.
- Protective & marine coatings: 22,44 mld. USD v roce 2026 s výhledem 30,92 mld. USD v roce 2035 (CAGR 3,4 %) podle Business Research Insights.
- Letecké povlaky: odhady pro 2026 se rozcházejí — 1,19 mld. USD (Mordor Intelligence, CAGR 4,03 %), 2,73 mld. USD s výhledem 5,10 mld. USD v 2034 (Fortune Business Insights), 3,90 mld. USD s výhledem 6,60 mld. USD v 2033 při CAGR 7,8 % (Coherent Market Insights). Rozptyl je dán různým vymezením trhu — necituj jen to nejvyšší číslo.
- Zkoušení materiálů jako trh: 3,93 mld. USD v 2026 → 6,05 mld. USD v 2035 (Roots Analysis, CAGR 4,91 %), resp. 6,56 mld. USD v 2026 → 9,47 mld. USD v 2033 (Coherent Market Insights); Mordor uvádí 63,99 mld. USD v 2026 při jiném, mnohem širším vymezení.
- Bottom-up pro první tři roky (předpoklady k ověření, ne fakta): vážných globálních formulátorů leteckých a marine povlaků je řádově 20–40 (AkzoNobel, PPG, Sherwin-Williams, Axalta, Hempel, Jotun, Mankiewicz, Chugoku a další), plus řádově 100–300 průmyslových formulátorů v EU; při ACV 50–250 tis. USD za prediktivní kvalifikaci vychází SAM v nízkých stovkách mil. USD a realistický SOM roku 1–3 na 3–10 design partnerů × 30–80 tis. EUR pilotu, tj. 0,1–0,8 mil. EUR. Ověř: počet kvalifikačních programů ročně u jednoho formulátora a cena jednoho programu.

_Sources:_ [[1]](https://www.businessresearchinsights.com/market-reports/protective-marine-coatings-market-101594) [[2]](https://www.fortunebusinessinsights.com/aerospace-coatings-market-105309) [[3]](https://www.mordorintelligence.com/industry-reports/aerospace-coatings-market) [[4]](https://www.coherentmarketinsights.com/industry-reports/aerospace-coating-market) [[5]](https://www.rootsanalysis.com/material-testing-market) [[6]](https://www.coherentmarketinsights.com/industry-reports/material-testing-market)

### Kdo už v tom je — a proč to není totéž
Tři oddělené skupiny: materials-informatics platformy (formulace), self-driving laby (syntéza a screening) a zkušebny (hodiny v komoře). Predikci výsledku kvalifikačního programu neprodává ani jedna — ale akademická literatura ji už umí, takže konkurenční výhoda nemůže ležet v modelu.
- Materials informatics je malý, slabě financovaný segment: podle Tracxn 33 firem, z toho 17 financovaných, celkem 133 mil. USD. Citrine Informatics (2013, Redwood City) má 81,3 mil. USD a je v Series C; MaterialsZone 7 mil. USD (Tel Aviv); Polymerize 4,4 mil. USD (Singapur); Uncountable a Aionics rovněž aktivní.
- Nejbližší evropský analog je Osium AI (Paříž, 2023): 3,1 mil. USD celkem, podle Latka ~990 tis. USD příjmů s devítičlenným týmem v roce 2025 — realistický benchmark pro služebně vedený start, ne pro platformový hype.
- Self-driving laby jsou kapitálově v jiné lize: Radical AI (2024) zvedla 55 mil. USD seed v červenci 2025 vedený RTX Ventures s účastí NVentures a staví autonomní laboratoře v Brooklyn Navy Yard; Periodic Labs má po 200 mil. USD seed a 350 mil. USD Series A (říjen 2025) celkem 550,7 mil. USD při valuaci >1,3 mld. USD.
- Pro povlaky konkrétně už existuje autonomní platforma v národní laboratoři: Argonne Polybot automatizuje formulaci, nanášení a post-processing polymerních filmů s optimalizací vodivosti a nízkou defektností; univerzitní tým AUTODIAL (Toronto) dělá totéž pro keramické povlaky a slitiny.
- Inkumbenti na straně zkoušek prodávají kapacitu, ne predikci: Q-Lab (od 1956, QUV je nejrozšířenější přístroj pro zrychlené zvětrávání, plus akreditované kontraktní zkoušky v A2LA), Element Materials Technology (globální síť laboratoří, zrychlené zvětrávání pro nátěry a plasty) a v ČR akreditovaná zkušebna SVÚOM.
- Metoda je publikovaná: dvoustupňový ML model 'environmental factors → physical property → corrosion failure' (npj Materials Degradation, 2025), CNN predikce životnosti epoxidových povlaků v hlubokomořském prostředí s průměrnou chybou 2,60 %, semi-supervised model atmosférického stárnutí akrylátových povlaků a ML-asistovaný návrh self-healing epoxidu. Kdokoli s daty to umí zreplikovat.

_Sources:_ [[7]](https://tracxn.com/d/trending-business-models/startups-in-material-informatics/__zCPscUCJyfvFdUzoLsSLt9w9uvOSQFw1pGrAY3Rw2NI/companies) [[8]](https://tracxn.com/d/companies/citrine-informatics/__OVyUkPfdQiRY9SN1pP739S6CyJuGZZOKcSBuZbZuKgA) [[9]](https://getlatka.com/companies/osium.ai) [[10]](https://pitchbook.com/profiles/company/229130-47) [[11]](https://research.contrary.com/company/periodic-labs) [[12]](https://www.anl.gov/article/selfdriving-lab-transforms-materials-discovery) [[13]](https://www.nature.com/articles/s41529-025-00614-6) [[14]](https://www.nature.com/articles/srep40827) [[15]](https://www.q-lab.com/weathering) [[16]](https://www.element.com/materials-testing-services/accelerated-weathering-test-methods)

### Proč právě teď: reformulační vlna vynucená regulací
Dvě evropská regulační řízení nutí průmysl přeformulovat povlaky, u nichž je kvalifikace nejdražší a nejdelší. To je jediný důvod, proč by dnes někdo platil za zkrácení zkoušek.
- PFAS: ECHA spustila 26. 3. 2026 finální konzultaci k návrhu omezení PFAS, zveřejnila finální stanovisko RAC a návrh stanoviska SEAC — oba podporují celoevropské omezení výroby, uvedení na trh a použití s konkrétními derogacemi; konzultace se uzavřela 25. 5. 2026 a ECHA chce vědecké hodnocení dokončit do konce roku 2026.
- Návrh pokrývá více než 10 000 látek; počet navržených derogací se zvýšil z 26 na 74, ale žádost průmyslu vyjmout fluoropolymery ze scope SEAC nepřijal — dotčena jsou i fluoropolymerní procesní aditiva používaná při výrobě povlaků a membrán.
- Cr(VI): Evropská komise po přezkumu udělila 12letou autorizaci pro použití chromátů v aerospace a defence (v REACH komitétu s výrazně pozitivním hlasováním) — přitom stále platí, že u žádné alternativy nebyla spolehlivě prokázána stejná úroveň korozní ochrany jako u chromátových pigmentů.
- Zároveň ECHA 29. 4. 2025 oznámila záměr navrhnout široké omezení látek s Cr(VI) podle REACH; přijetí omezení se očekává kolem září 2026, případně začátkem 2027. Kombinace 'autorizace na 12 let + chystané omezení' znamená, že kvalifikace chrome-free náhrad musí začít nyní.
- Self-driving laby se posouvají z výzkumu do praxe (C&EN, červen 2026: 'self-driving labs are changing how chemists work') a zrychlené hodnocení koroze s vysokopropustnou charakterizací + AI predikcí je už samostatné téma v marine engineering (npj Materials Degradation, 2025).

_Sources:_ [[17]](https://www.whitecase.com/insight-alert/europes-pfas-restriction-proposal-moving-forward) [[18]](https://echa.europa.eu/-/echa-announces-timeline-for-pfas-restriction-evaluation) [[19]](https://www.european-coatings.com/news/markets-companies/what-the-eus-pfas-restriction-means-for-coatings-and-paints/) [[20]](https://www.asd-europe.org/news-media/news-events/news/eu-grants-12-year-authorisation-for-chromates/) [[21]](https://www.sustainable-markets.com/echa-chromium-vi-restriction-proposal-what-manufacturers-should-know/) [[22]](https://www.iaeg.com/binaries/content/assets/iaeg/news/wg5-chromate-authorization-communication.pdf) [[23]](https://www.nature.com/articles/s41529-025-00663-x) [[24]](https://cen.acs.org/physical-chemistry/computational-chemistry/Self-driving-labs-changing-chemists/104/web/2026/06)

### Normy, do kterých musí predikce zapadnout
Kvalifikace je definovaná normami a akreditací. Predikce má hodnotu jen tehdy, když mluví jazykem konkrétní zkoušky a vychází z akreditovaného prostředí — to je zároveň nejtvrdší vstupní bariéra i budoucí moat.
- Zrychlené a cyklické korozní zkoušky, které jsou v ČR akreditovaně dostupné (zkušebna SVÚOM č. 1096, akreditace ČIA podle ČSN EN ISO/IEC 17025:2018): ČSN EN ISO 9227, PV 1210, VDA 621-415, SAE J 2334, ČSN EN ISO 11997-1 cyklus B a cyklické zkoušky pod UV lampami. Toto je konkrétní seznam cílových veličin pro predikci.
- Letecký příklad kvalifikace: MIL-PRF-85285 je výkonová specifikace DoD pro polyuretanové vrchní nátěry letadel; certifikaci administruje U.S. Naval Air Warfare Center Patuxent River a je to standardní topcoat na všech letadlech U.S. Navy a USMC.
- Kvalifikace není jednorázová: periodické ověřování certifikací probíhá ve dvouletých intervalech od data původní kvalifikace a iniciuje ho kvalifikující orgán — tj. existuje opakující se rozpočet, nikoli jen jednorázový projekt.
- Zkoušky v MIL-PRF-85285 zahrnují adhezi (mřížkový řez + odtrh lepicí páskou), adhezi po expozici kapalinám a prostředí a odolnost proti nárazu — predikce musí mířit na tyto konkrétní přejímací veličiny, ne na abstraktní 'degradaci'.

_Sources:_ [[25]](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) [[26]](https://svuom.cz/index.php?lang=cz&zobraz=tnkorzk) [[27]](https://www.valencesurfacetech.com/the-news/mil-prf-85285-type-1/) [[28]](https://chemsol.com/wp-content/uploads/2013/09/MIL-PRF-85285E.pdf)

### Kam tekly peníze a kdo je logický investor
Čistá materials-informatics kategorie je financovaná skromně, zatímco 'AI + vlastní laboratoř' přitáhlo stovky milionů. Pro pre-seed z Prahy to znamená: buď služebně vedený, kapitálově štíhlý start (cesta Osium AI), nebo strategický partner s laboratoří a daty.
- Celý segment material informatics podle Tracxn: 33 firem, 17 financovaných, dohromady 133 mil. USD rizikového a private-equity kapitálu — tedy méně než jedno kolo Radical AI.
- Citrine Informatics je nejdále (81,3 mil. USD celkem, Series C; poslední kolo 2,6 mil. USD v lednu 2025 — tedy zpomalení, ne akcelerace).
- Naopak 'AI + robotická laboratoř' táhne: Radical AI 55 mil. USD seed (červenec 2025, RTX Ventures + NVentures), Periodic Labs 550,7 mil. USD celkem při valuaci >1,3 mld. USD (Series A, říjen 2025, s účastí Nvidia).
- Investor s tezí přímo na povlaky v Evropě existuje — zurišský fond s více než 1 mld. EUR spravovaných aktiv, jehož zaměření Materials & Packaging explicitně zahrnuje ochranné povlaky a nanostrukturované materiály, portfolio 90+ firem z 25 000+ posouzených dealů. Konkrétní jméno a kontakt jsou v sekci kontaktů (odemyká se s trakcí).
- Lokální pre-seed je dostupný, ale nespecializovaný: dva české fondy dělají pre-seed a seed v rozmezí 100 tis.–1,5 mil. EUR včetně deeptech/hardware — relevantní teprve ve chvíli, kdy budeš mít data a design partnera. Také v sekci kontaktů.

_Sources:_ [[29]](https://tracxn.com/d/trending-business-models/startups-in-material-informatics/__zCPscUCJyfvFdUzoLsSLt9w9uvOSQFw1pGrAY3Rw2NI)

## 🔗 Sources  ·  all links
1. [businessresearchinsights.com](https://www.businessresearchinsights.com/market-reports/protective-marine-coatings-market-101594)
2. [fortunebusinessinsights.com](https://www.fortunebusinessinsights.com/aerospace-coatings-market-105309)
3. [mordorintelligence.com](https://www.mordorintelligence.com/industry-reports/aerospace-coatings-market)
4. [coherentmarketinsights.com](https://www.coherentmarketinsights.com/industry-reports/aerospace-coating-market)
5. [rootsanalysis.com](https://www.rootsanalysis.com/material-testing-market)
6. [coherentmarketinsights.com](https://www.coherentmarketinsights.com/industry-reports/material-testing-market)
7. [tracxn.com](https://tracxn.com/d/trending-business-models/startups-in-material-informatics/__zCPscUCJyfvFdUzoLsSLt9w9uvOSQFw1pGrAY3Rw2NI/companies)
8. [tracxn.com](https://tracxn.com/d/companies/citrine-informatics/__OVyUkPfdQiRY9SN1pP739S6CyJuGZZOKcSBuZbZuKgA)
9. [getlatka.com](https://getlatka.com/companies/osium.ai)
10. [pitchbook.com](https://pitchbook.com/profiles/company/229130-47)
11. [research.contrary.com](https://research.contrary.com/company/periodic-labs)
12. [anl.gov](https://www.anl.gov/article/selfdriving-lab-transforms-materials-discovery)
13. [nature.com](https://www.nature.com/articles/s41529-025-00614-6)
14. [nature.com](https://www.nature.com/articles/srep40827)
15. [q-lab.com](https://www.q-lab.com/weathering)
16. [element.com](https://www.element.com/materials-testing-services/accelerated-weathering-test-methods)
17. [whitecase.com](https://www.whitecase.com/insight-alert/europes-pfas-restriction-proposal-moving-forward)
18. [echa.europa.eu](https://echa.europa.eu/-/echa-announces-timeline-for-pfas-restriction-evaluation)
19. [european-coatings.com](https://www.european-coatings.com/news/markets-companies/what-the-eus-pfas-restriction-means-for-coatings-and-paints/)
20. [asd-europe.org](https://www.asd-europe.org/news-media/news-events/news/eu-grants-12-year-authorisation-for-chromates/)
21. [sustainable-markets.com](https://www.sustainable-markets.com/echa-chromium-vi-restriction-proposal-what-manufacturers-should-know/)
22. [iaeg.com](https://www.iaeg.com/binaries/content/assets/iaeg/news/wg5-chromate-authorization-communication.pdf)
23. [nature.com](https://www.nature.com/articles/s41529-025-00663-x)
24. [cen.acs.org](https://cen.acs.org/physical-chemistry/computational-chemistry/Self-driving-labs-changing-chemists/104/web/2026/06)
25. [svuom.cz](https://svuom.cz/index.php?lang=cz&zobraz=akrzk)
26. [svuom.cz](https://svuom.cz/index.php?lang=cz&zobraz=tnkorzk)
27. [valencesurfacetech.com](https://www.valencesurfacetech.com/the-news/mil-prf-85285-type-1/)
28. [chemsol.com](https://chemsol.com/wp-content/uploads/2013/09/MIL-PRF-85285E.pdf)
29. [tracxn.com](https://tracxn.com/d/trending-business-models/startups-in-material-informatics/__zCPscUCJyfvFdUzoLsSLt9w9uvOSQFw1pGrAY3Rw2NI)

## 🤝 Recommended contacts

_Intros are **earned** — you unlock contacts as your venture clears each stage, so we only connect you when you're ready. Feedback above is always free._

### ✅ Available now
- **Tomáš Prošek** (academia, ✓ verified) — Vede skupinu Kovové konstrukční materiály v Technoparku Kralupy VŠCHT: atmosférická koroze, korozní zkoušky a monitoring, ochranné kovové i organické povlaky. Skupina má 13 lidí a dělá ~100 průmyslových kontraktů ročně — první telefonát, protože drží data i zákazníky.
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
- **SVÚOM s.r.o.** (network, ✓ verified) — Akreditovaná zkušebna č. 1096 (ČIA, ČSN EN ISO/IEC 17025:2018) pro protikorozní ochranu: urychlené a cyklické zkoušky podle ISO 9227, PV 1210, VDA 621-415, SAE J 2334, ISO 11997-1 cyklus B i cyklické zkoušky pod UV. Tady leží data i akreditace, bez kterých predikce není použiteln
  - [svuom.cz](https://www.svuom.cz/) · [svuom.cz](https://svuom.cz/index.php?lang=cz&zobraz=akrzk) · [svuom.cz](https://svuom.cz/index.php?lang=cz&zobraz=tnkorzk)

### 🔓 Earn introductions — unlock by progressing your venture
- 🔒 **Investor / high-profile** (venture) — Still analysing your repo — push an update to generate readiness.
- 🔒 **Investor / high-profile** (venture) — Still analysing your repo — push an update to generate readiness.
- 🔒 **Investor / high-profile** (venture) — Still analysing your repo — push an update to generate readiness.

---
_StartupCoach — an AI mentor for founders, built at **FIT CTU** (Czech Technical University), operated by **Pavel Kordík**._