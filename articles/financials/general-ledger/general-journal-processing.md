---
title: "Bendrųjų žurnalų apdorojimas"
description: "Šioje temoje aprašytos programos „Microsoft Dynamics 365 for Finance and Operations“ galimybės, galinčios padėti lengviau atlikti bendrąjį žurnalo apdorojimą, taip pat užtikrinti, kad užfiksuoti tinkami duomenys ir nėra pažeidžiama vidinė kontrolė."
author: ShylaThompson
manager: AnnBe
ms.date: 09/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf744bc41ffcca6d029da5dd2031ada607a0109b
ms.openlocfilehash: e77aafafed5c972a6ad8c064107306d3ebde0b79
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---

# <a name="general-journal-processing"></a>Bendrųjų žurnalų apdorojimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašytos programos „Microsoft Dynamics 365 for Finance and Operations“ galimybės, galinčios padėti lengviau atlikti bendrąjį žurnalo apdorojimą, taip pat užtikrinti, kad užfiksuoti tinkami duomenys ir nėra pažeidžiama vidinė kontrolė.  

## <a name="journal-names"></a>Žurnalų pavadinimai

Viena iš svarbiausių sričių, kurias reikia nustatyti, yra žurnalų pavadinimai. Naudinga apibrėžti konkrečius žurnalų pavadinimus kiekvienam tikslui, pavyzdžiui, vidinės įmonės, kaupimo koregavimo ir klaidų taisymo. Galite pritaikyti kiekvieno žurnalo pavadinimą, kad įvesti duomenis kiekvienu tikslu būtų lengva ir saugu. 

Puslapyje **Žurnalų pavadinimai** galite nustatyti šiuos elementus.

-   **Darbo eigos patvirtinimas** – norėdami padidinti vidinę kontrolę, apibrėžkite žurnalo darbo eigas, nustatančias peržiūros ir patvirtinimo veiksmų svarbos ribas pagal tokius kriterijus kaip bendroji debeto suma. Galite nustatyti bendrųjų žurnalų darbo eigas puslapyje **Didžiosios knygos darbo eigos**.
-   **Numatytosios reikšmės** – pasirinkite numatytąsias korespondentinių sąskaitų, valiutos ir finansinių dimensijų reikšmes.
-   **Žurnalo valdymas** – galite nustatyti įmonės ir sąskaitos tipo apribojimus, taip pat segmentų reikšmes. 

**Pavyzdžiai**

Žurnalo pavadinimą galima naudoti tik koreguoti. Tokiu atveju galite nurodyti, kad visoms įmonėms tinkamas tik sąskaitos tipas **Didžioji knyga**. 

[![Žurnalų kontrolės sąskaitos tipai](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Žurnalo pavadinimą galima naudoti tik konkrečiam segmentui arba pagrindinių sąskaitų diapazonui. 

[![Žurnalų kontrolės segmentas](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Parinktis **Automatinis atšaukimas** yra bendruosiuose žurnaluose. Pavyzdžiui, turite kaupimo koregavimą, kurio faktinis dokumentas dar neapdorotas, kaip pavaizduota šioje iliustracijoje.
[![Pagrindinio žurnalo atšaukimas](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

„Microsoft Excel“ papildinys, skirtas žurnalo įrašams, teikia papildomą automatizavimo lygį ir palengvina duomenų įvedimą. Veiksmas **Atidaryti eilutes programoje „Excel“** galimas puslapiuose **Pagrindinis žurnalas** ir **Žurnalo kvitas**. 

Puslapyje **Periodiniai žurnalai** galite nustatyti pasikartojančius žurnalus, kad žurnalų apdorojimas būtų automatizuotas. 

Bet kada galite naudoti kvitų šablonus. Puslapio **Pagrindiniai žurnalai** puslapyje **Žurnalo kvitas**, dalyje **Funkcijos**, rasite veiksmus **Įrašyti** ir **Pasirinkti kvito šabloną**.

## <a name="related-setup"></a>Susijusi sąranka
Ši sąranka nėra susijusi su pagrindiniais žurnalais, bet padės užtikrinti, kad bus įrašomi teisingi duomenys ir įrašyti bus lengva.

### <a name="main-account"></a>Korespondentinė sąskaita, subsąskaita

Pagrindinės sąskaitos sąranka teikia daug pagrindinio žurnalo apdorojimo galimybių.

-   **DC / RC reikalavimas** – naudokite šią parinktį, jei pagrindinė sąskaita naudojama tik debeto arba kredito operacijoms. Sąranka patikrinama, kai žurnalą tikrinamas arba registruojamas.

-   **Numatytoji korespondentinė sąskaita**
-   **Sustabdyta** – sustabdykite visų įmonių arba konkrečios įmonės / juridinio subjekto duomenų įvedimą pagrindinėje sąskaitoje.
-   **Neleisti įvesti rankiniu būdu** – neleidžia vartotojams įvesti sąskaitos reikės žurnaluose rankiniu būdu.
-   **Numatytoji reikšmė / tikrinti valiutą**
-   **Juridinio subjekto nepaisymas** – ši sąranka taikoma apibrėžtai įmonei / juridiniam subjektui.
    -   **Numatytoji reikšmė / tikrinti PVM**
    -   **Numatytoji dimensija** – **Nefiksuota** arba **Fiksuota reikšmė**. **Fiksuota reikšmė** padės užtikrinti, kad visada registruojant iš šios pagrindinės sąskaitos bus naudojama dimensijos reikšmė, nustatyta **Fiksuota**.
-   **Registravimo tikrinimas**
    -   **Vartotojo tikrinimas** – šia parinktimi valdoma, kurie vartotojai gali registruoti pagrindinėje sąskaitoje.
    -   **Registravimo tipo tikrinimas** – šia parinktimi valdoma, kurie registravimo pagrindinėje sąskaitoje tipai yra leidžiami.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Apskaitos struktūros ir išplėstinių taisyklių struktūros

Apskaitos struktūros ir išplėstinių taisyklių struktūros yra labai svarbios siekiant užtikrinti, kad duomenys, būtini finansinėms ataskaitoms ir efektyvumui sekti, būtų įrašomi apdorojant bendrąjį žurnalą ir dokumentuojant. Apskaitos struktūros ir išplėstinių taisyklių struktūros leidžia pritaikyti duomenų įvedimo patirtį. Galite leisti tik kiekvienu atveju svarbių finansinių dimensijų duomenų įrašus, taip pat galite taikyti reikalavimą, kad privalomi ir tikslūs duomenys visada būtį įrašomi.

Daugiau informacijos ieškokite šiose temose:
- [Planavimas: sąskaitų planas](plan-chart-of-accounts.md). 
- [Kurti papildomas žurnalų taisykles](tasks/create-advanced-rules-journals.md)
- [Kurti žurnalo įrašą naudojant šabloną](tasks/create-journal-entry-template.md)
- [Kurti ir patvirtinti žurnalus](tasks/create-validate-journals.md)
- [Periodinių žurnalų registravimas](tasks/post-periodic-journals.md)
- [Didžiosios knygos paskirstymo žurnalo apdorojimas](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Modeliuoti registravimą
Funkciją **Modeliuoti registravimą** dažniausiai galite rasti žurnalų meniu **Tikrinti**. Kai tikrinant žurnalą naudojamasi funkcija  **Tikrinti**, sistema patikrina, ar žurnalas neatitinka konkrečių klaidų sąlygų. Jei naudojate funkciją **Modeliuoti registravimą**, sistema vykdo tuos pačius procesus, kurie vykdomi registruojant, nors iš tiesų žurnalas neregistruojamas. Tada galite peržiūrėti rodomus registravimo pranešimus, ištaisyti rastas klaidas, paskui, spustelėję meniu **Registruoti** užregistruoti žurnalą. 

Atliekant paketinį apdorojimą funkcija **Modeliuoti registravimą** naudotis negalima. Tačiau, norint modeliuoti paketo registravimą, galima naudoti kodą ir kūrėjai, išplėtoję kodą, gali įtraukti šią funkciją.  

