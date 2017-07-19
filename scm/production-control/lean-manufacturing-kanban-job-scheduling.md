---
title: "„Kanban“ užduoties, skirtos „lean manufacturing“, planavimas"
description: "Šiame straipsnyje pateikiama informacija apie „kanban“ užduočių planavimo vizualinę kontrolę ir įvairius būdus planuoti „kanban“ užduotis."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 27db57170ccc23c2ea18a49c1a3e5950c870fa13
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>„Kanban“ užduoties, skirtos „lean manufacturing“, planavimas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama informacija apie „kanban“ užduočių planavimo vizualinę kontrolę ir įvairius būdus planuoti „kanban“ užduotis.  

Puslapyje **„kanban“ užduočių planavimas** galima valdyti „lean manufacturing“ darbo elementų grafikus. Jame apžvelgiamos visos „kanban“ užduotys bei pateikiamos kelios filtravimo parinktys. Šiame puslapyje galite pereiti į visu kitus su „kanban“ konfigūracija ir vykdymu susijusius puslapius.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Automatinis „kanban“ užduočių planavimas
Planavimo procesas gali būti automatiškai paleidžiamas, jei nustatysite „kanban“ taisyklės parametrą **Automatinio planavimo kiekis**. Jei nustatysite parametro **Automatinio planavimo kiekis** vertę **1**, vos tik sukūrus bet kurią „kanban“ užduotį, ji bus suplanuojama. Bus gaunamas pirmiausia apdorojamo operacijų kiekio rezultatas. Jei nustatysite didesnę už 1 parametro **Automatinio planavimo kiekis** vertę, „kanban“ užduotys prieš suplanuojant bus sugrupuojamos. 

Dėl šios koncepcijos „kanban“ dydžiai gali būti mažesni už faktinius ekonominio paketo dydžius. Pavyzdžiui, konkrečios prekės (ar prekių grupės) ekonominio paketo dydis yra 30. Galite nekurti „kanban“, kuriuose naudojamas produktų kiekis yra 30, o konfigūruoti „kanban" taisyklę, kurioje apibrėžtas produktų kiekis būtų 10, o parametro **Automatinio planavimo kiekis** reikšmė – **3**. Nors taikant automatinio planavimo funkciją darbo elemento „kanban“ užduotys suplanuojamos tik tada, kai yra trys nesuplanuotos užduotys, tačiau planuotojui ir darbo laiko prižiūrėtojui bus visiškai aišku, kad reikia atlikti dvi nesuplanuotas užduotis. Tuomet planuotojas arba darbo laiko vadybininkas, rankiniu būdu suplanavęs šias dvi užduotis arba sukūręs papildomus „kanban“, gali įtraukti jas į gamybos procesą.

## <a name="manual-scheduling"></a>Rankinis planavimas
Programoje „Microsoft Dynamics AX 2012“ pradėta naudoti rankiniam planavimui skirta „kanban“ planavimo lenta. Rankinio planavimo funkciją galima kartu naudoti su automatiniu planavimu. Naudodami „kanban“ planavimo lentą galite suplanuoti užduotis ir panaikinti jų planavimą, jas perkelti sekoje arba iš vieno laikotarpio į kitą. Galima rankiniu būdu panaikinti pagal „kanban“ taisyklę, kurioje nustatyta parametro **Automatinis planavimas** vertė didesnė už **0**, sukurtų užduočių planavimą. Tačiau šios užduotys bus perplanuotos įvykus kitam automatinio planavimo įvykiui (t. y. sukūrus naują „kanban“). Galima naudoti toliau nurodytas rankinio planavimo parinktis.

-   Naudojant parinktį **Grafikas** pagal terminus suplanuojamos pasirinktos užduotys (ši parinktis panaši į automatinio planavimo parinktį).
-   Naudojant parinktį **Grafikas pirmyn nuo datos** bandoma pagal terminus suplanuoti pasirinktas užduotis, tačiau rezultatas apribojamas naudojant nurodytą anksčiausią pradžios datą.
-   Naudojant parinktį **Atgal** pasirinktos suplanuotos užduotys sekoje perkeliamos atgal, o jų data išlieka laikotarpio diapazone.
-   Naudojant parinktį **Pirmyn** pasirinktos suplanuotos užduotys sekoje perkeliamos pirmyn, o jų data išlieka laikotarpio diapazone.
-   Naudojant parinktį **Ankstesnis laikotarpis** pasirinktos suplanuotos užduotys perkeliamos į ankstesnio laikotarpio pradžią arba pabaigą.
-   Naudojant parinktį **Kitas laikotarpis** pasirinktos suplanuotos užduotys perkeliamos į kito laikotarpio pradžią arba pabaigą.
-   Naudojant parinktį **Planas** &gt; **Grąžinti užduoties būseną** galite panaikinti suplanuotos užduoties planavimą.

## <a name="lean-scheduling-groups"></a>„lean“ planavimo grupės
Kiekviena spalva nurodo „lean“ planavimo grupę. „lean“ planavimo grupes galima savo nuožiūra nustatyti bendrosiomis grupėmis arba vienam darbo elementui priklausančiomis grupėmis. Prekes ir dimensijas galima savo nuožiūra priskirti planavimo grupėms. Pavyzdžiui, su elementu Dažymas susieta planavimo grupė gali nurodyti produkto spalvą. Darbo, kurį atliekant taikomi reikalavimai konkretiems įrankiams, elemente prekės gali būti sugrupuojamos pagal įrankio reikalavimą, o pakavimo darbo elemente prekės gali būti sugrupuojamos pagal pakuotės šabloną. „lean“ planavimo grupėse nebūtina naudoti spalvų, tačiau rekomenduojama jas naudoti. Tuomet pagerėja plano būsenos matomumas. Pavyzdžiui, labai lengva pamatyti, kada pagaminti konkrečių spalvų produktai, bei galima greitai nustatyti šio darbo optimizavimo veiksmus.

## <a name="work-cell-capacity-and-period-capacity"></a>Darbo elemento pajėgumas ir laikotarpio pajėgumas
„lean“ darbo elemento pajėgumas – tai visada vienu metu vykstančių užduočių pajėgumas. Kitaip tariant, tuo pačiu metu gali būti aktyvios kelios darbo elemento užduotys. Pajėgumą galima sekti naudojant du režimus: našumo ir valandų.

### <a name="throughput"></a>Našumas

Darbo elemento pajėgumas nustatomas pagal vidutinį ataskaitinio laikotarpio (standartinės darbo dienos, savaitės ar mėnesio) našumą. Tada faktinis pajėgumas per dieną arba savaitę apskaičiuojamas pagal darbo elementui priskirto kalendoriaus darbo laikus. Užduoties pajėgumas – tai užduoties kiekis, kuris pakoreguojamas pagal darbo elemento našumo koeficientą.

### <a name="hours"></a>Valandos

Galimas pajėgumas per dieną arba savaitę nustatomas pagal darbo elementui priskirtą kalendorių. Užduoties pajėgumas – tai veiklos ciklo laikas, kuris pakoreguojamas pagal darbo elemento kiekį (numatytąjį veiklos kiekį lyginant su faktiniu užduoties kiekiu) ir našumo koeficientą.

#### <a name="period-capacity-factbox"></a>Laikotarpio pajėgumo „FactBox“

Sąrašo puslapyje **„kanban“ užduočių planavimas** yra „FactBox“, kurioje nurodytas galimas ir suplanuotas pasirinkto darbo elemento laikotarpio pajėgumas. Laikotarpiai vaizduojami dienomis arba savaitėmis – tai priklauso nuo pasirinktų gamybos eigos modelio grafiko laikotarpių.

<a name="see-also"></a>Taip pat žiūrėkite
--------




