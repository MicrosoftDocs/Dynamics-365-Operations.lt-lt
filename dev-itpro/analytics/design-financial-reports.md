---
title: "Finansinių ataskaitų peržiūra ir kūrimas"
description: "Šiame straipsnyje pateikiami pratimai, kurie padeda peržiūrėti ir kurti finansines ataskaitas, skirtas „Microsoft Dynamics 365 for Operations“."
author: jcart1106
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1c0787327830d2cdff9e8a48798165dc83493393
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="view-and-design-financial-reports"></a>Finansinių ataskaitų peržiūra ir kūrimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiami pratimai, kurie padeda peržiūrėti ir kurti finansines ataskaitas, skirtas „Microsoft Dynamics 365 for Operations“. Finansines ataskaitas sudaro peržiūros patirtis programoje „Dynamics 365 for Operations“ ir vieno paspaudimo ataskaitų dizaino įrankis, kuris suteikia galimybę kurti ir redaguoti finansines ataskaitas.  

<a name="exercise-1-generate-and-explore-a-default-financial-report"></a>1 užduotis: sugeneruokite ir išnagrinėkite numatytąją finansinę ataskaitą
-----------------------------------------------------------

Atlikdami šią užduotį, jūs generuosite ir nagrinėsite esamą numatytąją ataskaitą. Ši ataskaita apima visas sąskaitas bei sąskaitų ypatybes (atributus). Gilinsitės į operacijų informaciją, taikysite dimensijų filtrus, keisite ataskaitos valiutą. Pirma atnaujinsime finansinių ataskaitų dimensijų rodymo tvarką. Tai leidžia pasirinkti, kaip bus rodomos dimensijos ne tik kuriant ir peržiūrint finansines ataskaitas.

1.  Eikite į **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas** didžiosios knygos srityje **Sąskaitų plano dimensijos**.
2.  Perkelkite dimensijas, kad rodomos tokia tvarka:
    1.  Pagrindinė sąskaita
    2.  Verslo struktūros vienetas
    3.  Išlaidų centras
    4.  Padalinys

    Pastaba: kitos dimensijos gali likti rodomos dabartine tvarka.
3.  Įrašykite dimensijos konfigūraciją. Paskui generuosime ataskaitą ir nagrinėsime ataskaitos duomenis.
4.  Eikite į **Finansinės ataskaitos** didžiosios knygos srityje **Užklausos ir ataskaitos**.
5.  Pasirinkite eilutę ataskaitoje, kuri vadinasi **DK informacija – numatytoji.**
6.  Pasirinkite **Redaguoti**. Pastaba: būsite paraginti atsisiųsti vieno paspaudimo ataskaitų dizaino įrankį ir prisijungti. Prisijunkite naudodami kredencialus.
7.  Pakeiskite pagrindinius metus į 2012 ir pasirinkite **Generuoti**. Kai ataskaitų dizaino įrankis sugeneruos ataskaitą, ji bus atidaryta naujame naršyklės skirtuke. Galite panagrinėti ataskaitą naujame naršyklės skirtuke arba eiti į savo pradinį naršyklės skirtuką ir atidaryti ataskaitą iš ten, ją pasirinkdami iš sąrašo **Finansinės ataskaitos**.
8.  Atidarytoje ataskaitoje pasirinkite vieną iš sumų, kad detalizuotumėte tos ataskaitos sąskaitų informaciją.
9.  Atidarę sąskaitos informaciją, pasirinkite sąskaitą su duomenimis ir **detalizuokite iki ataskaitos operacijų lygio**. Ataskaitos operacijų lygyje galite peržiūrėti ypatybes (atributus), kurie įtraukti į šios ataskaitos dizainą. Priklausomai nuo operacijos ir sąskaitos, gali būti rodomi kai kurie arba visi atributai.
10. Uždarykite ataskaitos operacijų lygį.
11. Pasirinkite tą pačią arba kitą sąskaitą ir **atidarykite kvitų operacijas.** Kvitų operacijos filtruojamos pagal laikotarpį, metus ir sąskaitą + pasirinktos sąskaitos dimensijos kombanaciją. Kvito operacijose galite pasirinkti nagrinėti kitą informaciją apie operaciją.
12. Uždarykite kvitų operacijas. Finansinėje ataskaitoje galite peržiūrėti duomenis už kitą laikotarpį ir metus arba taikant kitus atributus ir dimensijas. Tai atliekama naudojant **Ataskaitos parinktys**.
13. Pasirinkite **Ataskaitos parinktys**.
14. Pasirinkite **Įtraukti dimensijos filtrą** ir pasirinkite **Verslo struktūros vienetas**.
15. Įveskite 001 į lauką ir pasirinkite **Gerai**. Dabar ataskaitoje pateikiami tik 001 verslo struktūros vieneto duomenys. Tai suasmenintas ataskaitos rodinys, kurio negali matyti kiti.
16. Uždarykite filtruot! ataskaitą. Finansines ataskaitas galima rodyti bet kuria valiuta, kuri įtraukta į „Dynamics 365 for Operations“.
17. Pasirinkite **Valiutos**, tada pasirinkite **EUR.** Dabar ataskaitoje pateikiamos sumos eurais. Bet kokie valiutos kodai ar simboliai, įtraukti į ataskaitos dizainą, dabar rodo taikomą valiutą. Jei valiutai nėra priskirtas simbolis, valiutos simbolis nerodomas.
18. Uždarykite ataskaitą **DK informacija**.
19. Uždarykite **Ataskaitų dizaino įrankis**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>2 užduotis: įtraukite papildomas sąskaitos ypatybes į ataskaitos dizainą
Atlikdami šią užduotį, jūs modifikuosite esamą numatytąją ataskaitą. Atnaujinsite eilutės apibrėžimą, kad apimtų visas sąskaitas, ir atnaujinsite stulpelio apibrėžimą, kad apimtų sąskaitos atributus. Kai atnaujinimai baigti, galite generuoti naujai sukurtą ataskaitą ir ją panagrinėti. Pradėsime nuo finansinių ataskaitų sąrašo.

1.  Eikite į **Finansinės ataskaitos** didžiosios knygos srityje „Užklausos ir ataskaitos“.
2.  Pasirinkite ataskaitos eilutę, kuri vadinasi **Bandomojo balanso suvestinė – numatytoji.**
3.  Pasirinkite **Redaguoti**. **Bandomojo balanso suvestinė – numatytasis** bus atidaryta ataskaitų dizaino įrankyje.
4.  Pasirinkite **Failas**, tada **Įrašyti kaip** ir pavadinkite ataskaitą Išsamus bandomasis balansas su atributais. Pastaba: kiekvieną kartą, kai ataskaitų dizaino įrankyje sukuriama nauja ataskaita, atnaujinamas finansinių ataskaitų sąrašas „Dynamics 365 for Operations“.
5.  Iš ataskaitos aprašo pasirinkite eilutės apibrėžimo piktogramą, kad atidarytumėte **Bandomasis balansas – numatytasis eilutės apibrėžimas**.
6.  Įrašykite eilutės apibrėžimą kaip **Išsamus bandomasis balansas su atributais**
7.  Nuvilkę žymeklį ant 50 eilutės, pasirinkite **Redaguoti**, tada **Įterpti eilutes iš dimensijų**. „Įterpti eilutes iš dimensijų“ leidžia pasirinkti, kokias dimensijas norite turėti savo eilutės apibrėžime. Atlikdami šią užduotį, kursime eilutės apibrėžimą naudodami pagrindinę sąskaitą.
8.  Įsitikinkite, kad **Pagrindinė sąskaita** apima visus konjunkcijos ženklus (&) ir pasirinkite **Gerai**. Dabar eilutės apibrėžime yra visos jūsų numatytojo juridinio subjekto USMF pagrindinės sąskaitos.
9.  Slinkite žemyn į 11110 eilutę ir ją panaikinkite.
10. 11080 eilutėje pasirinkite **---(Pabrauktos sumos)**.
11. 11140 eilutėje įveskite **Bendroji visų sąskaitų suma** stulpelyje B.
12. C stulpelyje pasirinkite **TOT** iš išplečiamojo sąrašo.
13. Įveskite **50:11080** stulpelyje D.
14. **Įrašyti** eilutės apibrėžimą. Eilutės apibrėžimas dabar apima visas sąskaitas ir bendros sumos eilutę, į kurią įtrauktos visos sąskaitos. Dabar atnaujinsime stulpelio apibrėžimą, kad įtrauktų papildomus sąskaitos atributus.
15. Iš ataskaitos aprašo **Išsamus bandomasis balansas su atributais** pasirinkite stulpelio apibrėžimo piktogramą, kad atidarytumėte stulpelio apibrėžimą **Bandomojo balanso suvestinė – numatytoji**.
16. Įrašykite stulpelio apibrėžimą kaip **Išsamus bandomasis balansas su atributais**. Stulpelio apibrėžimas apima finansinių duomenų stulpelius, aprašymo stulpelį ir skaičiavimo stulpelius. Pridėsime atributų stulpelius prie stulpelio apibrėžimo, pateikdami papildomos informacijos apie sąskaitas.
17. Šie atributai bus pridedami prie stulpelio apibrėžimo:
    -   Žurnalo numeris
    -   Žurnalo aprašymas
    -   Operacijos data
    -   Sukūrė
    -   Paskutinį kartą modifikavo

18. I stulpelyje pasirinkite stulpelio tipą **ATTR**. Tada pasirinkite **Žurnalo numeris** kaip atributų kategoriją.
19. Toliau pridėkite likusių atributų stulpelius.
20. Eilutėje **2 antraštė** pridėkite kiekvieno naujai pridėto stulpelio aprašymus.
21. Įrašykite stulpelio apibrėžimą. Atnaujinę eilutės apibrėžimą ir stulpelio apibrėžimą, turėsime juos įtraukti į ataskaitos aprašą.
22. Iš ataskaitos aprašo **Išsamus bandomasis balansas su atributais** pasirinkite „Išsamus bandomasis balansas su atributais“ ir eilutės apibrėžimui, ir stulpelio apibrėžimui.
23. Pakeiskite pagrindinius metus į **2012.**
24. **Įrašykite** ataskaitos aprašą ir **generuokite**. Kai ataskaita baigs generuoti ir atsidarys, galėsite ją panagrinėti kaip ir pirmoje užduotyje. Detalizuokite skirtingas sąskaitas, kad pamatytumėte, kaip rodomi papildomi atributai.
25. Uždarykite ataskaitą **Išsamus bandomasis balansas su atributais**.
26. Uždarykite **Ataskaitų dizaino įrankis**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>3 užduotis: sukurkite kelių dimensijų ataskaitą naudodami ataskaitų medį
Atlikdami šią užduotį, jūs modifikuosite esamą numatytąją ataskaitą. Kursite ataskaitų medį ir įtrauksite į ataskaitos aprašą, sukurdami išlaidų centrą / padalinių įplaukų ataskaitą. Kai atnaujinimai bus baigti, galėsite generuoti išlaidų centrą / padalinių pajamų ataskaitą ir panagrinėti ataskaitą naudodami ataskaitų medį. Pradėsime nuo finansinių ataskaitų sąrašo.

1.  Eikite į **Finansinės ataskaitos** didžiosios knygos srityje „Užklausos ir ataskaitos“.
2.  Pasirinkite eilutę ataskaitoje, kuri vadinasi **įplaukų ataskaita – numatytoji.**
3.  Pasirinkite **Redaguoti**. **Įplaukų ataskaita – numatytoji** bus atidaryta ataskaitų dizaino įrankyje.
4.  Meniu **Failas** paspauskite **Naujas**, tada spustelėkite **Ataskaitų medžio apibrėžimas**.
5.  Meniu **Redaguoti** spustelėkite **Įterpti ataskaitinius vienetus iš dimensijų**...
6.  Išvalykite visų dimensijų, išskyrus **Išlaidų centrą**, žymės langelius.
7.  Spustelėkite išlaidų centro **007** tipo dimensijos lauką **Iš dimensijos** ir spustelėkite klavišą Tab. Lauke **Į dimensiją** įveskite **018**.
8.  **Įrašykite** gautą medį su pavadinimu **Išlaidų centrai pagal padalinius.** Dabar, kai ataskaitų medis sukurtas, jį modifikuosite, kad apimtų tris naujus sumavimo vienetus: rinkodarą, operacijas ir mažmeninę prekybą.
9.  Meniu **Langas** spustelėkite **išlaidų centrai pagal padalinius**. (Jei ataskaitų medis buvo uždarytas, pasirinkite jį iš ataskaitų medžio apibrėžimų naršymo srityje.)
10. Spustelėkite vienetą numeris du, **Parodos**, ir spustelėkite piktogramą **įĮerpti ataskaitų vienetą**.
11. Dukart spustelėkite objekto stulpelio tuščią eilutę ir pasirinkite **USMF**.
12. Įveskite **Rinkodara** stulpeliuose, B ir C.
13. Spustelėkite vienetą numeris penki, **Aptarnavimo operacijos**, ir spustelėkite dešiniuoju pelės mygtuku. **Įterpti ataskaitinius vienetus**.
14. Pakartokite 11 veiksmą.
15. Įveskite **Operacijos** stulpeliuose B ir C.
16. Spustelėkite vienetą numeris dvylika, **Parduotuvė**, ir spustelėkite dešiniuoju pelės mygtuku. Pasirinkite **Įterpti ataskaitinius vienetus**.
17. Pakartokite 11 veiksmą.
18. Įveskite **Mažmeninė prekyba** stulpeliuose B ir C. Atkreipkite dėmesį, kad rinkodaros, operacijų ir mažmeninės prekybos vienetai rodomi tame pačiame lygyje kaip dabartiniai sumavimo vienetai. Toliau organizuojami nauji vienetai. Ataskaitų vienetai organizuojami per dešiniojo pelės mygtuko parinktis; teikite arba mažinkite pirmenybę, arba vilkite ir numeskite.
19. Patikrinkite, kad trečias vienetas, **Parodos**, yra aktyvus ir dešiniuoju pelės mygtuku spustelėkite.
20. Pasirinkite **Perkelti ataskaitinį vienetą į žemesnį lygį**. Atkreipkite dėmesį, kad dabar vienetas rodomas kaip antrinis **Rinkodara** vienetas.
21. Spustelėkite ketvirtą vienetą, **Rinkodaros** **kampanija**, ir spustelėkite dešiniuoju pelės mygtuku.
22. Pasirinkite **Perkelti ataskaitinį vienetą į žemesnį lygį**.
23. Spustelėkite **Aptarnavimo operacijos** grafiniame formate. Paspauskite ir laikykite nuspaudę kairįjį pelės mygtuką, vilkdami vienetą iki **Operacijos**. Atleiskite kairįjį pelės mygtuką, kad numestumėte vienetą į operacijos sumavimą. Kartokite **Gamybai, kokybės kontrolei, logistikai, įsigijimams ir administravimui**.
24. Valdykite **Parduotuvė**, **Super**, **Prekybos centras** ir **Internetinė** antriniai **Mažmeninė prekyba** perkeldami į žemesnį lygį arba vilkdami ir numesdami.
25. Įrašykite gautą reorganizaciją. Dabar, kai sukūrėme ir suorganizavome ataskaitų medį, jį galima įtraukti į ataskaitos aprašą.
26. Meniu **Langas** pasirinkite **Įplaukų ataskaita – numatytoji**, kad atidarytumėte ataskaitos aprašą.
27. Spustelėkite išplečiamąją rodyklę **Medžio tipas** ir pasirinkite **Ataskaitų medis**.
28. Spustelėkite medžio išplečiamąją rodyklę ir pasirinkite **Išlaidų centrai pagal padalinį**.
29. Pakeiskite pagrindinius metus į **2012**, **įrašykite** pakeitimus ir **sygeneruokite** ataskaitą. Kai ataskaita baigs generuotis ir atsidarys, galėsite ją panagrinėti.
30. Pasirinkite išplečiamąjį sąrašą **Ataskaitų medis**, kad peržiūrėtumėte ataskaitų vienetus. Taip pat galite gali detalizuoti ataskaitos eilutę, kad matytumėte visų ataskaitos medžio vienetų visus balansus.
31. Uždarykite **Įplaukų ataskaita – numatytoji**.
32. Uždarykite **Ataskaitų dizaino įrankis**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>4 užduotis: sukurkite konsoliduotą ataskaitą naudodami organizacijos hierarchiją
Atlikdami šią užduotį, jūs modifikuosite esamą numatytąją ataskaitą. Įtrauksite organizacijos hierarchiją į ataskaitos aprašą, kad parengtumėte konsoliduotą įplaukų ataskaitą ir balansą. Kai atnaujinimai bus baigti, galėsite generuoti konsoliduotą ataskaitą ir panagrinėti ataskaitą naudodami ataskaitų medį. Pradėsime nuo finansinių ataskaitų sąrašo.

1.  Eikite į **Finansinės ataskaitos** didžiosios knygos srityje „Užklausos ir ataskaitos“.
2.  Pasirinkite eilutę ataskaitos, kuri vadinasi **Balanso ir sugretinamų įplaukų ataskaita – numatytoji**
3.  Pasirinkite **Redaguoti**. **Balanso ir sugretinamų įplaukų ataskaita – numatytoji** atsidarys ataskaitos dizaino įrankyje.
4.  Pasirinkite **Failas** &gt; **Įrašyti kaip** ir pavadinkite ataskaitą **Konsoliduota balanso ir sugretinamų įplaukų ataskaita**.
5.  Pakeiskite pagrindinius metus į 2012.
6.  Spustelėkite medžio tipo išplečiamąją rodyklę ir pasirinkite **Organizacijos hierarchijos**.
7.  Spustelėkite medžio išplečiamąją rodyklę ir pasirinkite **Contoso Holdings.**
8.  Įrašykite pakeitimus ir sugeneruokite ataskaitą. Jei būsite paraginti, pasirinkite visus ataskaitų vienetus. Kai ataskaita baigs generuotis ir atsidarys, galėsite ją panagrinėti.
9.  Pasirinkite **Ataskaitos parinktys**.
10. Pasirinkite **Įtraukti dimensijos filtrą** ir pasirinkite **Padalinys**.
11. Įveskite **022** į lauką ir pasirinkite **Gerai**.
12. Uždarykite filtruot! ataskaitą.
13. Pasirinkite išplečiamąjį sąrašą **Ataskaitų medis**, kad peržiūrėtumėte ataskaitų vienetus. Taip pat galite gali detalizuoti ataskaitos eilutę, kad matytumėte visų ataskaitos medžio vienetų visus balansus.
14. Uždarykite **Konsoliduotą balanso ir įplaukų ataskaitą vieną šalia kitos – numatytoji**.
15. Uždarykite **Ataskaitų dizaino įrankis**.

## <a name="exercise-5-create-a-sidebyside-departmental-report"></a>5 užduotis: sukurkite sugretinamą padalinių ataskaitą
Šioje užduotyje kursite naują ataskaitą. Ataskaita yra sugretinamų padalinių įplaukų ataskaita. Naudosite esamą eilutės apibrėžimą, tačiau sukursite naują ataskaitos aprašą ir naują stulpelio apibrėžimą, kuris naudoja dimensijų filtrus. Pradėsime nuo finansinių ataskaitų sąrašo.

1.  Eikite į **Finansinės ataskaitos** didžiosios knygos srityje „Užklausos ir ataskaitos“.
2.  Pasirinkite **Naujas**. Ataskaitų dizaino įrankis atsidarys su atviru tuščiu ataskaitos aprašu. Jūsų pirmoji užduotis bus sukurti stulpelio apibrėžimą.
3.  Sukurkite naują stulpelio apibrėžimą spustelėkję **Failas**, tada **Naujas**, o tada **Stulpelio apibrėžimas**.
4.  **Stulpelyje A** pasirinkite stulpelio tipą **DESC**.
5.  **Stulpelyje B** pasirinkite stulpelio tipą **FD**.
6.  Dukart spustelėkite lauke **Dimensijos filtras**.
7.  Lange **Dimensija** dukart spustelėkite **padalinio** stulpelį.
8.  Dialogo atskirame arba diapazono skyriuje spustelėkite **daugtaškį** lauke **Iš**, kad būtų rodomas padalinių sąrašas.
9.  Pasirinkite padalinį **022**, **Pardavimai ir rinkodara**, ir tada spustelėkite**Gerai**.
10. Pakartokite 5 – 8 veiksmus, taikydami 23-25 padaliniams.
11. Kiekvieno FD stulpelio eilutėje **2 antraštė** įveskite tokius padalinių aprašymus:
    -   B stulpelis – Pardavimai ir rinkodara
    -   C stulpelis – Operacijos
    -   D stulpelis – Finansai
    -   E stulpelis – IT

12. Stulpelio apibrėžimą įrašykite kaip „Sugretinami padaliniai“. Naudojame esamą eilutės apibrėžimą, todėl dabar ataskaitos aprašą galima modifikuoti, panaudojant naujai sukurtą stulpelio apibrėžimą ir esamos eilutės apibrėžimą.
13. Meniu **Langas** pasirinkite **Naujas ataskaitos aprašas**, kad atidarytumėte ataskaitos aprašą.
14. Pasirinkite **Įplaukų ataskaita – numatytoji** kaip eilutės apibrėžimą ir **Sugretinami padaliniai** – kaip stulpelio apibrėžimą.
15. Įrašykite ataskaitos aprašą kaip **Sugretinamų padalinių įplaukų ataskaita**.
16. Pakeiskite pagrindinius metus į **2012**.
17. Pakeiskite išsamumo lygį į **finansų, sąskaitos ir operacijų**.
18. **Įrašykite** savo atliktus pakeitimus ir **generuokite**. Kai ataskaita baigs generuotis ir atsidarys, galėsite ją panagrinėti.

## <a name="additional-resources"></a>Papildomi ištekliai
[Finansinės ataskaitos](/dynamics365/operations/financials/general-ledger/financial-reporting-getting-started) 
[Peržiūrėti finansines ataskaitas](/dynamics365/operations/financials/general-ledger/view-financial-reports) 
[„Dynamics‟ finansinių ataskaitų tinklaraštis](http://blogs.msdn.com/b/dynamics_financial_reporting/)




