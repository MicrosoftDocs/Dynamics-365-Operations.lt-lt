---
title: Bendrųjų žurnalų apdorojimas
description: Šioje temoje aprašytos programos „Microsoft Dynamics 365 Finance“ galimybės, galinčios padėti lengviau atlikti bendrąjį žurnalo apdorojimą, taip pat gali padėti užtikrinti, kad užfiksuoti tinkami duomenys ir nėra pažeidžiama vidinė kontrolė.
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd854b2188b07830e5641ccdd4bb02804a07b55c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975638"
---
# <a name="general-journal-processing"></a>Bendrųjų žurnalų apdorojimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašytos programos galimybės, galinčios padėti lengviau atlikti bendrąjį žurnalo apdorojimą, taip pat gali padėti užtikrinti, kad užfiksuoti tinkami duomenys ir nėra pažeidžiama vidinė kontrolė.  

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
- [Sąskaitų plano rengimas](plan-chart-of-accounts.md) 
- [Žurnalų išplėstinių taisyklių kūrimas](tasks/create-advanced-rules-journals.md)
- [Kurti žurnalo įrašą naudojant šabloną](tasks/create-journal-entry-template.md)
- [Žurnalų kūrimas ir tvirtinimas](tasks/create-validate-journals.md)
- [Periodinių žurnalų registravimas](tasks/post-periodic-journals.md)
- [Didžiosios knygos paskirstymo žurnalo apdorojimas](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Modeliuoti registravimą
Funkciją **Modeliuoti registravimą** dažniausiai galite rasti žurnalų meniu **Tikrinti**. Kai tikrinant žurnalą naudojamasi funkcija  **Tikrinti**, sistema patikrina, ar žurnalas neatitinka konkrečių klaidų sąlygų. Jei naudojate funkciją **Modeliuoti registravimą**, sistema vykdo tuos pačius procesus, kurie vykdomi registruojant, nors iš tiesų žurnalas neregistruojamas. Tada galite peržiūrėti rodomus registravimo pranešimus, ištaisyti rastas klaidas, tada atidaryti meniu **Registruoti** ir užregistruoti žurnalą. 

Atliekant paketinį apdorojimą funkcija **Modeliuoti registravimą** naudotis negalima. Tačiau, norint modeliuoti paketo registravimą, galima naudoti kodą ir kūrėjai, išplėtoję kodą, gali įtraukti šią funkciją.  

## <a name="journal-unlock"></a>Žurnalo atrakinimas
Žurnalo puslapyje yra mygtukas, skirtas atrakinti žurnalą, kurio parametro „užrakino sistema“ nustatyta reikšmė yra „Taip“. Šį atrakinimą gali vykdyti sistemos administratorius, kuris išanalizavo visas vykdymo paketines užduotis ir įsitikino, kad šis žurnalas nėra aktyviai apdorojamas paketinės užduoties. Šį mygtuką galima suaktyvinti naudojant funkciją **Žurnalo atrakinimo mygtukas** puslapyje **Funkcijų valdymas**. 

## <a name="workflow-recall"></a>Darbo eigos atšaukimas 
Galimybė atšaukti žurnalą darbo eigoje, kurio būsena yra „neištaisoma“, yra įjungta naudojant **darbo eigos** mygtuką, esantį žurnale ir puslapyje **Darbo eigos retrospektyva**. Ją suaktyvina funkcija **Žurnalų darbo eigos būsenos atkūrimas** puslapyje **Funkcijų valdymas**.

## <a name="delete-journal-lines"></a>Naikinti žurnalo eilutes
Galimybė greitai panaikinti visas žurnalo eilutes yra įjungta žurnale **Funkcijos** > **Naikinti žurnalo eilutes**. Norėdami suaktyvinti šią funkciją, **Funkcijų valdymas** pasirinkite **Naikinti žurnalo našumo optimizavimus**.
