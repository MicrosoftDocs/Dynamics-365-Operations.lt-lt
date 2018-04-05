---
title: "Biudžeto planavimo duomenų paskirstymas"
description: "Šiame straipsnyje aprašyti įvairūs paskirstymo metodai, kuriuos galima naudoti „Microsoft Dynamics 365 for Finance and Operations“, ir kaip juos naudoti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b5f262318b4defb941f1216d0bfe06961f62bad4
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning-data-allocation"></a>Biudžeto planavimo duomenų paskirstymas

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašyti įvairūs paskirstymo metodai, kuriuos galima naudoti „Microsoft Dynamics 365 for Finance and Operations“, ir kaip juos naudoti.  

Biudžeto plano duomenis galima paskirstyti keliais būdais, kad būtų tiksliai atvaizduojamos numatomos sumos.

## <a name="allocation-methods"></a>Paskirstymo būdai
Naudojantis trimis paskirstymo būdais (Paskirstyti laikotarpiams, Paskirstyti dimensijoms ir Naudoti DK paskirstymo taisykles) galima sukurti biudžeto plano eilutes, kurios pagrįstos to paties biudžeto plano eilutėmis. Naudojantis trimis kitais būdais (Sujungti, Paskirstyti ir Kopijuoti iš biudžeto plano) galima sukurti biudžeto plano eilutes kituose biudžeto planuose. Naudodami visus šešis paskirstymo būdus nurodote paskirties scenarijų. Paskirties scenarijus gali būti toks pat kaip šaltinio scenarijus arba kitoks negu šaltinio scenarijus. Be to, galite nurodyti, ar prie biudžeto plano prijungti naujas eilutes, ar pakeisti dabartines biudžeto plano eilutes.

[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Paskirstyti laikotarpiams** – norint paskirstyti šaltinio biudžeto plano scenarijaus biudžeto plano eilutes paskirties scenarijaus laikotarpiams naudojama laikotarpio paskirstymo kategorija. Šaltinio suma priskiriama kelioms paskirties scenarijaus eilutėms, priklausomai nuo laikotarpio paskirstymo kategorijoje nurodyto procento ir datos.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Paskirstyti dimensijoms** – biudžeto plano eilutės iš šaltinio biudžeto planavimo scenarijaus paskirstomos į vieną ar kelias paskirties scenarijaus eilutes, priklausomai nuo pasirinktose biudžeto paskirstymo sąlygose nurodytų procentų ir finansinių dimensijų.           

![AggregateChart](./media/aggregatechart-300x230.png)
**Sujungti** – biudžeto plano eilutės sujungiamos iš šaltinio biudžeto plano scenarijaus susijusiuose (antriniuose) biudžeto planuose į paskirties scenarijų pirminiame biudžeto plane. Naudojantis šiuo būdu galima naudoti tas biudžeto sumas, kurios žemesniame organizacijos lygyje yra paruoštos konsolidavimui aukštesniame lygyje.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Paskirstyti** – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto planavimo scenarijaus pirminiame biudžeto plane į paskirties scenarijų susijusiuose (antriniuose) biudžeto planuose, priklausomai nuo susijusių planų organizacijos vienetų finansinių dimensijų. Naudojantis šiuo būdu galima naudoti tas biudžeto sumas, kurios aukštesniame organizacijos lygyje yra paruoštos labiau lokalizuotai peržiūrai.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Naudoti DK paskirstymo taisykles** – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto plano scenarijaus į paskirties biudžeto plano scenarijų pagal pasirinktą DK paskirstymo taisyklę. 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopijuoti iš biudžeto plano** – naudojant paskirstymo platinimo būdą biudžeto plano eilutės sukuriamos paskirtyje, priklausomai nuo susijusio biudžeto plano eilučių. Tačiau naudojant šį būdą šaltinio biudžeto planas neturi būti pirminis, bet gali būti aukštesniame biudžeto plano hierarchijos lygmenyje. Šis paskirstymo būdas naudingas, jei į biudžetą iš pradžių buvo įtrauktos daug aukštesnio lygio konsoliduotos sumos, kurios turi būti perkeltos į žemesnį organizacijos lygį, kad prieš joms gaunant aukštesnio lygio patvirtinimą būtų galima atlikti išsamią peržiūrą ir koreguoti.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Paskirstymo būdų naudojimas biudžeto plane
Norėdami atlikti paskirstymus biudžeto plano puslapyje, pasirinkite eilutes, kurias reikia paskirstyti, tada spustelėkite **Paskirstyti biudžetą**.

[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Po to pasirinkite paskirstymo būdą. Tada pagal jūsų pasirinktą metodą nustatomi likusieji laukai. Šiuose laukuose nurodomas biudžeto plano duomenų šaltinis, paskirtis ir pasirinktis, kuri kuriant paskirties sumas leidžia padauginti šaltinį iš nurodyto koeficiento, kad būtų paprasčiau koreguoti kiekį. Taip pat galite nustatyti pasirinktį **Pridėti prie plano** . Jeigu norite pakeisti esamas biudžeto plano eilutes, pasirinkite **Ne** arba, jeigu norite išsaugoti esamas biudžeto plano eilutes ir įtraukti naujų eilučių, skirtų paskirstytoms sumoms, pasirinkite  **Taip**.

## <a name="automating-allocations-during-a-workflow"></a>Paskirstymų automatizavimas darbo eigos metu
Viena galinga funkcija leidžia paskirstymus atlikti automatiškai, kaip biudžeto planavimo darbo eigos dalį. Vykstant biudžeto plano darbo eigai automatizuotos užduotys gali iškviesti nurodyto biudžeto planavimo etapo paskirstymą. 

Norėdami nustatyti automatinį paskirstymą, pirmiausia puslapyje **Biudžeto planavimo konfigūracija** turite sukurti paskirstymo grafiką. Paskirstymo grafike nurodomas paskirstymo būdas, kuris bus naudojamas vykdant automatinį paskirstymą, ir įvairių paskirstymo pasirinkčių (žr. jų aprašymus ankstesniame skyriuje) reikšmės. 

Po to puslapyje **Biudžeto planavimo konfigūracija** sukurkite etapo paskirstymą. Etapo paskirstymas priskiria paskirstymo grafiką biudžeto planavimo darbo eigai ir etapui. 

Galiausiai pridėkite norimo darbo eigos etapo biudžeto planavimo etapo paskirstymo automatizuotą užduotį. Šiame pavyzdyje į darbo eigą įtraukti du biudžeto planavimo etapo paskirstymai (pažymėti raudonai).

[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)




