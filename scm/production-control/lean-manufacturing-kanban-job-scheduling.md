---
title: "Kanban užduočių planavimą tausojančios gamybos"
description: "Šiame straipsnyje pateikiama informacija apie „kanban“ užduočių planavimo vizualinę kontrolę ir įvairius būdus planuoti „kanban“ užduotis."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 02 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 062cbbc8a4fd3b4dc738f24ee0606a3741736377
ms.lasthandoff: 03/29/2017


---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kanban užduočių planavimą tausojančios gamybos

Šiame straipsnyje pateikiama informacija apie „kanban“ užduočių planavimo vizualinę kontrolę ir įvairius būdus planuoti „kanban“ užduotis.  

Puslapyje **„kanban“ užduočių planavimas** galima valdyti „lean manufacturing“ darbo elementų grafikus. Jame apžvelgiamos visos „kanban“ užduotys bei pateikiamos kelios filtravimo parinktys. Šiame puslapyje galite pereiti į visu kitus su „kanban“ konfigūracija ir vykdymu susijusius puslapius.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Automatinis „kanban“ užduočių planavimas
Planavimas gali būti paleista automatiškai jei nustatysite į **Automatinis planavimas kiekis** parametras kanban teisinės valstybės principu. Jei nustatysite **Automatinis planavimas kiekis** į **1**, kiekviena kanban darbas planuojamas nedelsiant, kai jis yra sukurtas. Bus gaunamas pirmiausia apdorojamo operacijų kiekio rezultatas. Jei nustatysite didesnę už 1 parametro **Automatinio planavimo kiekis** vertę, „kanban“ užduotys prieš suplanuojant bus sugrupuojamos. Dėl šios koncepcijos „kanban“ dydžiai gali būti mažesni už faktinius ekonominio paketo dydžius. Pvz., konkrečios prekės (ar prekių grupei) ekonominės siuntos dydis yra 30. Užuot kūrę kanbans, naudojamo produkto kiekį, 30, galite konfigūruoti kanban taisyklė, kad jo 10 produkto kiekis ir ** automatinis planavimas kiekis ** vertė **3**. Nors taikant automatinio planavimo funkciją darbo elemento „kanban“ užduotys suplanuojamos tik tada, kai yra trys nesuplanuotos užduotys, tačiau planuotojui ir darbo laiko prižiūrėtojui bus visiškai aišku, kad reikia atlikti dvi nesuplanuotas užduotis. Tuomet planuotojas arba darbo laiko vadybininkas, rankiniu būdu suplanavęs šias dvi užduotis arba sukūręs papildomus „kanban“, gali įtraukti jas į gamybos procesą.

## <a name="manual-scheduling"></a>Rankinis planavimas
Programoje „Microsoft Dynamics AX 2012“ pradėta naudoti rankiniam planavimui skirta „kanban“ planavimo lenta. Rankinio planavimo funkciją galima kartu naudoti su automatiniu planavimu. Naudodami „kanban“ planavimo lentą galite suplanuoti užduotis ir panaikinti jų planavimą, jas perkelti sekoje arba iš vieno laikotarpio į kitą. Galima rankiniu būdu panaikinti pagal „kanban“ taisyklę, kurioje nustatyta parametro **Automatinis planavimas** vertė didesnė už **0**, sukurtų užduočių planavimą. Tačiau šios užduotys bus perplanuotos įvykus kitam automatinio planavimo įvykiui (t. y. sukūrus naują „kanban“). Galima naudoti toliau nurodytas rankinio planavimo parinktis.

-   Naudojant parinktį **Grafikas** pagal terminus suplanuojamos pasirinktos užduotys (ši parinktis panaši į automatinio planavimo parinktį).
-   Naudojant parinktį **Grafikas pirmyn nuo datos** bandoma pagal terminus suplanuoti pasirinktas užduotis, tačiau rezultatas apribojamas naudojant nurodytą anksčiausią pradžios datą.
-   Naudojant parinktį **Atgal** pasirinktos suplanuotos užduotys sekoje perkeliamos atgal, o jų data išlieka laikotarpio diapazone.
-   Naudojant parinktį **Pirmyn** pasirinktos suplanuotos užduotys sekoje perkeliamos pirmyn, o jų data išlieka laikotarpio diapazone.
-   Naudojant parinktį **Ankstesnis laikotarpis** pasirinktos suplanuotos užduotys perkeliamos į ankstesnio laikotarpio pradžią arba pabaigą.
-   Naudojant parinktį **Kitas laikotarpis** pasirinktos suplanuotos užduotys perkeliamos į kito laikotarpio pradžią arba pabaigą.
-   **Planą,**&gt;**grąžinti užduoties būsena** leidžia unschedule planinė užduotis.

## <a name="lean-scheduling-groups"></a>„lean“ planavimo grupės
Kiekviena spalva nurodo „lean“ planavimo grupę. „lean“ planavimo grupes galima savo nuožiūra nustatyti bendrosiomis grupėmis arba vienam darbo elementui priklausančiomis grupėmis. Prekes ir dimensijas galima savo nuožiūra priskirti planavimo grupėms. Pavyzdžiui, su elementu Dažymas susieta planavimo grupė gali nurodyti produkto spalvą. Darbo, kurį atliekant taikomi reikalavimai konkretiems įrankiams, elemente prekės gali būti sugrupuojamos pagal įrankio reikalavimą, o pakavimo darbo elemente prekės gali būti sugrupuojamos pagal pakuotės šabloną. „lean“ planavimo grupėse nebūtina naudoti spalvų, tačiau rekomenduojama jas naudoti. Tai pagerina matomumą į plano būsena. Pvz., labai lengva pamatyti, kokios spalvos yra gaminami kurią dieną, ir jūs galite pasakyti iš pirmo žvilgsnio, kaip šis darbas gali būti optimizuotas.

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


