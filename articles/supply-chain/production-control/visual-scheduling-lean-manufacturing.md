---
title: "„Lean manufacturing“ vaizdinis planavimas"
description: "Šioje temoje pateikiama informacijos apie „Kanban“ grafiko sritį, kurią gamybos planuotojas gali naudoti norėdamas valdyti ir optimizuoti „kanban“ užduočių gamybos planą."
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d2ead061fe39c3dcb54d697f246c2c826339b699
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="visual-scheduling-for-lean-manufacturing"></a>„Lean manufacturing“ vaizdinis planavimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacijos apie „Kanban“ grafiko sritį, kurią gamybos planuotojas gali naudoti norėdamas valdyti ir optimizuoti „kanban“ užduočių gamybos planą.

Šioje temoje pateikiama informacijos apie „Kanban“ grafiko sritį, kurią gamybos planuotojas gali naudoti norėdamas valdyti ir optimizuoti „kanban“ užduočių gamybos planą.

„Kanban“ grafiko sritis leidžia gamybos planuotojui valdyti ir optimizuoti „kanban“ užduočių gamybos planą. „Kanban“ užduočių srautas tampa skaidrus, o gamybos planuotojas gauna įrankį, kuris optimizuoja ir pakoreguoja „lean manufacturing“ darbo elemento gamybos planą.

## <a name="visual-scheduling-of-kanban-jobs"></a>Vaizdinis „kanban“ užduočių planavimas
„Kanban“ užduotį gali sudaryti viena arba daugiau „kanban“ užduočių. „Kanban“ užduotys gali būti dviejų tipų:

-   Procesas
-   Perkėlimas

Galite planuoti tik užduotis, kurių tipas **Procesas**. „Kanban“ užduotis ir jos ypatybės, pvz., veiklos laikas, apibrėžiamos gamybos „kanban“ sraute. Gamybos „kanban“ sraute „kanban“ užduotis taip pat priskiriama darbo elementui. Darbo elemento dienos pajėgumas apskaičiuojamas pagal darbo elemento pajėgumą, nustatytą išteklių grupėje. Jis pakoreguojamas pagal dienos darbo laiką susijusiame kalendoriuje. Kai planuojama „kanban“ užduotis, užduotis įkelia darbo elemento pajėgumą. „Kanban“ grafiko srityje yra šios pagrindinės funkcijos:

-   Grafinė gamybos plano apžvalga „lean“ darbo elemente. Ši apžvalga parodo suplanuotas „kanban“ proceso užduotis apibrėžtais laikotarpiais.
-   Įrankis, kuris leidžia planuoti nesuplanuotas „kanban“ užduotis ir perplanuoti anksčiau suplanuotas užduotis.

## <a name="kanban-schedule-board"></a>„Kanban“ grafiko sritis
Puslapyje **„Kanban“ grafiko sritis** yra septyni pagrindiniai elementai, kaip parodyta paveikslėlyje. 

![„Kanban“ grafiko sritis](./media/kanban-schedule-board-1024x554.png)
1.  Veiksmų sritis
2.  Filtruoti laukus
3.  Nesuplanuotų užduočių mygtukas
4.  Laikotarpio mazgas
5.  „Kanban“ užduotis
6.  Pajėgumo juosta
7.  Laiko skalė

### <a name="view-the-time-scale"></a>Peržiūrėti laiko skalę

Sritis yra padalyta į laikotarpius, iš kurių kiekvienas pateikiamas kaip mazgas (4). Laikotarpio mazgai yra išvardyti vertikalioje ašyje, o horizontali prieiga reiškia laiko skalę (7), kurioje pateikta laikotarpio trukmė. Laikotarpio ilgis yra viena diena arba savaitė. Laikotarpio ilgis priklauso nuo darbo elemento, kuris pasirinktas „Kanban“ grafiko srityje (2), konfigūracijos. Dėl kiekvieno laikotarpio mazgo „Kanban“ grafiko sritis nurodo, kiek laikotarpyje yra suplanuotų „kanban“ užduočių. Be to, nurodomas didžiausias laikotarpio našumas. Jei suplanuotas našumas viršija didžiausią našumą, laikotarpis laikomas perkrautu ir atsiranda raudonas įspėjimo simbolis. Suplanuota „kanban“ užduotis atsiranda laikotarpyje, kuris turi suplanuotą pradžios ir pabaigos laiką (5). Užduoties trukmė yra lygi veiklos laikui. „Kanban“ užduotys laikotarpyje rodomos kaip persidengiančios, jeigu jų veiklos laikas viršija darbo elemento vieneto gamybos laiką.

### <a name="view-job-status"></a>Peržiūrėti užduoties būseną

Daugiau informacijos apie „kanban“ užduotį yra patarime, kuris pasirodo, kai laikote žymeklį virš užduoties. Simbolis pateikia informaciją apie užduoties būseną. Pvz., laikrodžio simbolis nurodo, kad „kanban“ užduotis vėluoja.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Naudoti spalvas, norint peržiūrėti „Kanban“ grafiko sritį

Norėdami patobulinti „Kanban“ grafiko srities pateikiamą apžvalgą, galite naudoti spalvas, kad atskirtumėte „kanban“ užduotis. „Kanban“ užduoties spalva sukonfigūruojama pažangiosios gamybos planavimo grupėje, kurioje galite sudėti produktus, kurie turėtų būti gaminama ta pačia tvarka. Veiksmų srities skirtuko **Sritis** mygtukas **Naudoti temos spalvas** leidžia perjungti programos temų spalvas ir spalvas, sukonfigūruotas pažangiosios gamybos planavimo grupėje. Kiekvieno laikotarpio pajėgumo juosta (6) rodo, kiek esamų laikotarpio valandų užimta „kanban“ užduotimis. Jei laikotarpis perkrautas, pajėgumo juosta yra storesnė ir raudonos spalvos. Visos šios funkcijos pasiekiamos veiksmų srities (1) skirtuke **Sritis**, puslapio **„Kanban“ grafiko sritis** viršuje.

## <a name="plan-unplanned-jobs"></a>Planuoti nesuplanuotas užduotis
Galite suplanuoti nesuplanuotas „kanban“ užduotis dialogo lange **Planuoti nesuplanuotas užduotis**. Norėdami atidaryti šį dialogo langą spustelėkite mygtuką **Nesuplanuotos užduotys**, kuris rodo dabartinį nesuplanuotų užduočių skaičių. Arba spustelėkite **Planuoti nesuplanuotas užduotis** veiksmų srities skirtuke **Sritis**. Dialogo lange rodomas nesuplanuotų darbo elemento „kanban“ užduočių sąrašas. Galite naudoti lauką **Filtras** norėdami filtruoti visus tinklelio laukus. Pavyzdžiui, galite filtruoti konkretaus produkto „kanban“ užduotis. Po to, kai gaunate užduočių, kurias norite planuoti, filtruotą sąrašą, pasirinkite jas sąraše ir spustelėkite **Gerai**. Norėdami užduotis planuoti automatiškai, nustatykite parinktį **Automatinis planavimas** į **Taip**. Šiuo atveju laikotarpio užduotys planuojamos pagal jų terminą. Be to, galite planuoti užduotis pagal laikotarpį. Tiesiog pasirinkite laikotarpį lauke **Laikotarpis**. Šiame paveikslėlyje rodomas dialogo lango **Planuoti neplanuotas užduotis** pavyzdys. 

![Dialogo langas Planuoti nesuplanuotas užduotis](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Išdėstyti „kanban“ užduotis tame pačiame laikotarpyje
Galite pakeisti vienos ar daugiau pasirinktų laikotarpio užduočių seką. Ši galimybė gali būti naudinga, jei norite nustatyti kai kurių laikotarpio užduočių pirmumą. Be to, galite norėti išdėstyti užduotis, kurių produktų atributai yra vienodi, kad optimizuotumėte užduočių vykdymą. Galite pakeisti seką naudodami nuvilkimo operaciją arba meniu elementus **Atgal** ir **Pirmyn**, esančius veiksmų srities skirtuke **Sritis**.

## <a name="reassign-kanban-jobs-across-periods"></a>Iš naujo priskirti „kanban“ užduotis laikotarpiams
Užduotis galima iš naujo priskirti iš vieno laikotarpio kitam. Ši galimybė gali būti naudinga, jei laikotarpis yra perkrautas ir norite paskirstyti apkrovą laikotarpiams, kuriuose yra atsarginių pajėgumų. Galite iš naujo priskirti užduotis naudodami nuvilkimo operaciją arba meniu elementus **Tolesnis laikotarpis** ir **Ankstesnis laikotarpis**, esančius veiksmų srities skirtuke **Sritis**.

## <a name="open-the-kanban-schedule-board"></a>Atidaryti „Kanban“ grafiko sritį
„Kanban“ grafiko sritį galite atidaryti naudodami meniu elementą šiuose puslapiuose:

-   Puslapis **Gamybos sritis**
-   Puslapis **„Kanban“ užduočių planavimas**
-   Puslapis **Gamybos eigos vizualizavimas**


<a name="additional-resources"></a>Papildomi ištekliai
--------

[„Lean manufacturing“ – „kanban“ užduočių planavimas](lean-manufacturing-kanban-job-scheduling.md)


