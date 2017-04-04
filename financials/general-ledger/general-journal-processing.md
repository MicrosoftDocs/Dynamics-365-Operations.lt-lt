---
title: "Bendrųjų žurnalų apdorojimas"
description: "Šiame straipsnyje aprašoma Microsoft Dynamics 365 veiklą, tai gali padėti padaryti bendrojo žurnalo pavojams, ir kad taip pat gali padėti užtikrinti, kad teisingus duomenis yra užfiksuotas ir nebus pažeisti vidaus kontrolės pajėgumus."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Bendrųjų žurnalų apdorojimas

Šiame straipsnyje aprašytos programos „Microsoft Dynamics AX“ galimybės, galinčios padėti lengviau atlikti bendrąjį žurnalo apdorojimą, taip pat gali padėti užtikrinti, kad užfiksuoti tinkami duomenys ir nėra pažeidžiama vidinė kontrolė.  

Žurnalų pavadinimai

Viena iš svarbiausių sričių, nustatyti yra žurnalų pavadinimus. Tai gera idėja, kad nustatyti konkrečius pavadinimus kiekvienam tikslui, tokios kaip vidinės įmonės, kaupimo reguliavimo ir taisyti jos klaidas. Jūs galite pritaikyti kiekvieno žurnalo pavadinime, kad duomenų įvedimo šiems tikslams, lengva ir saugu. 

Puslapyje **Žurnalų pavadinimai** galite nustatyti šiuos elementus.

-   **Darbo eigos patvirtinimas** – norėdami padidinti vidinę kontrolę, apibrėžkite žurnalo darbo eigas, nustatančias peržiūros ir patvirtinimo veiksmų svarbos ribas pagal tokius kriterijus kaip bendroji debeto suma. Galite nustatyti iki darbo eigas bendrųjų žurnalų, ** DK darbo eigos ** puslapis.
-   **Numatytosios reikšmės** – pasirinkite numatytąsias korespondentinių sąskaitų, valiutos ir finansinių dimensijų reikšmes.
-   **Žurnalo valdymas** – galite nustatyti įmonės ir sąskaitos tipo apribojimus, taip pat segmentų reikšmes. 

**Pavyzdžiai**

Žurnalo pavadinimą galima naudoti tik koreguoti. Tokiu atveju galite nurodyti, kad visoms įmonėms tinkamas tik sąskaitos tipas **Didžioji knyga**. [![Leidinyje kontrolės sąskaitų tipai](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Žurnalo pavadinimą galima naudoti tik konkrečiam segmentui arba pagrindinių sąskaitų diapazonui. [![Leidinyje valdymo segmentas](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

Parinktis **Automatinis atšaukimas** yra bendruosiuose žurnaluose. Pavyzdžiui, turite kaupimo koregavimą, kurio faktinis dokumentas dar neapdorotas, kaip pavaizduota šioje iliustracijoje.
[![Bendrasis žurnalas, atbulinės eigos](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

Microsoft Excel papildinys, skirtas žurnalo įrašas suteikia papildomą automatizavimo lygį ir palengvina duomenų įvedimo. Veiksmas **Atidaryti eilutes programoje „Excel“ **galimas puslapiuose **Pagrindinis žurnalas** ir **Žurnalo kvitas**. 

Puslapyje **Periodiniai žurnalai** galite nustatyti pasikartojančius žurnalus, kad žurnalų apdorojimas būtų automatizuotas. 

Kvitų šablonai galite bet kuriuo metu. Dėl į **bendrųjų žurnalų** puslapyje, į **įrašyti** ir **pasirinkite kvitų šabloną** veiksmai yra rasti į **žurnalo kvitas** puslapis, kaip **funkcijos** kvito eilutėms.

## <a name="related-setup"></a>Susijusi sąranka
Ši sąranka nėra susijusi su pagrindiniais žurnalais, bet padės užtikrinti, kad bus įrašomi teisingi duomenys ir įrašyti bus lengva.

### <a name="main-account"></a>Korespondentinė sąskaita, subsąskaita

Pagrindinės sąskaitos sąranka teikia daug pagrindinio žurnalo apdorojimo galimybių.

-   **DC / RC reikalavimas** – naudokite šią parinktį, jei pagrindinė sąskaita naudojama tik debeto arba kredito operacijoms. Sąranka patikrinama, kai žurnalą tikrinamas arba registruojamas.
-   **Numatytoji korespondentinė sąskaita**
-   **Sustabdyta** – sustabdykite visų įmonių arba konkrečios įmonės / juridinių subjektų duomenų įvedimą pagrindinėje sąskaitoje.
-   **Neleisti įvesti rankiniu būdu** – neleidžia vartotojams įvesti sąskaitos reikės žurnaluose rankiniu būdu.
-   **Numatytoji reikšmė / tikrinti valiutą**
-   **Juridinio subjekto nepaisymas** – ši sąranka taikoma apibrėžtai įmonei / juridiniam subjektui.
    -   **Numatytoji reikšmė / tikrinti PVM**
    -   **Numatytoji dimensija** – **Nefiksuota** arba **Fiksuota reikšmė**. **Fiksuota reikšmė** padės užtikrinti, kad visada registruojant iš šios pagrindinės sąskaitos bus naudojama dimensijos reikšmė, nustatyta **Fiksuota**.
-   **Registravimo tikrinimas**
    -   **Vartotojo tikrinimas** – šia parinktimi valdoma, kurie vartotojai gali registruoti pagrindinėje sąskaitoje.
    -   **Registravimo tipo tikrinimas** – šia parinktimi valdoma, kurie registravimo pagrindinėje sąskaitoje tipai yra leidžiami.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Apskaitos struktūros ir išplėstinių taisyklių struktūros

Apskaitos struktūros ir išplėstinių taisyklių struktūros yra labai svarbios siekiant užtikrinti, kad duomenys, būtini finansinėms ataskaitoms ir efektyvumui sekti, būtų įrašomi apdorojant bendrąjį žurnalą ir dokumentuojant. Apskaitos struktūros ir išplėstinių taisyklių struktūros leidžia pritaikyti duomenų įvedimo patirtį. Galite leisti tik kiekvienu atveju svarbių finansinių dimensijų duomenų įrašus, taip pat galite taikyti reikalavimą, kad privalomi ir teisingi duomenys visada būtį įrašomi.

Daugiau informacijos rasite [planavimas: sąskaitų](plan-chart-of-accounts.md). 


