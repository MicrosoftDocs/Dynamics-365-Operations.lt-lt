---
title: Biudžeto planavimo duomenų paskirstymas
description: Šiame straipsnyje aprašomi 365 finansuose Microsoft Dynamics galimi paskirstymo metodai ir jų naudojimas.
author: panolte
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5788f6dc8aa6cddad5c8eaba748827307a4d38a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901466"
---
# <a name="budget-planning-data-allocation"></a>Biudžeto planavimo duomenų paskirstymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi 365 finansuose Microsoft Dynamics galimi paskirstymo metodai ir jų naudojimas.  

Biudžeto plano duomenis galima paskirstyti keliais būdais, kad būtų tiksliai atvaizduojamos numatomos sumos.

## <a name="allocation-methods"></a>Paskirstymo būdai
Naudojantis trimis paskirstymo būdais (Paskirstyti laikotarpiams, Paskirstyti dimensijoms ir Naudoti DK paskirstymo taisykles) galima sukurti biudžeto plano eilutes, kurios pagrįstos to paties biudžeto plano eilutėmis. Naudojantis trimis kitais būdais (Sujungti, Paskirstyti ir Kopijuoti iš biudžeto plano) galima sukurti biudžeto plano eilutes kituose biudžeto planuose. Naudodami visus šešis paskirstymo būdus nurodote paskirties scenarijų. Paskirties scenarijus gali būti toks pat kaip šaltinio scenarijus arba kitoks negu šaltinio scenarijus. Be to, galite nurodyti, ar prie biudžeto plano prijungti naujas eilutes, ar pakeisti dabartines biudžeto plano eilutes.

> [!NOTE] 
> Telkimui reikia naudoti unikalų scenarijų, kuris skiriasi nuo scenarijaus, naudojamo paskirstymui ar kitoms modifikacijoms, anksčiau atliktoms pirminiame plane.  

[![Paskirstymo metodas „Paskirstyti laikotarpiams“.](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Paskirstyti laikotarpiams** – norint paskirstyti šaltinio biudžeto plano scenarijaus biudžeto plano eilutes paskirties scenarijaus laikotarpiams naudojama laikotarpio paskirstymo kategorija. Šaltinio suma priskiriama kelioms paskirties scenarijaus eilutėms, priklausomai nuo laikotarpio paskirstymo kategorijoje nurodyto procento ir datos.         

[![Paskirstymo metodas „Paskirstyti dimensijoms“.](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Paskirstyti dimensijoms** – biudžeto plano eilutės iš šaltinio biudžeto planavimo scenarijaus paskirstomos į vieną ar kelias paskirties scenarijaus eilutes, priklausomai nuo pasirinktose biudžeto paskirstymo sąlygose nurodytų procentų ir finansinių dimensijų.           

![Sujungimo diagrama.](./media/aggregatechart-300x230.png)
**Sujungti** – biudžeto plano eilutės sujungiamos iš šaltinio biudžeto plano scenarijaus susijusiuose (antriniuose) biudžeto planuose į paskirties scenarijų pirminiame biudžeto plane. Naudojantis šiuo būdu galima naudoti tas biudžeto sumas, kurios žemesniame organizacijos lygyje yra paruoštos konsolidavimui aukštesniame lygyje.          

[![Paskirstymo diagrama.](./media/distributechart-300x230.png)](./media/distributechart.png)
**Paskirstyti** – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto planavimo scenarijaus pirminiame biudžeto plane į paskirties scenarijų susijusiuose (antriniuose) biudžeto planuose, priklausomai nuo susijusių planų organizacijos vienetų finansinių dimensijų. Naudojantis šiuo būdu galima naudoti tas biudžeto sumas, kurios aukštesniame organizacijos lygyje yra paruoštos labiau lokalizuotai peržiūrai.           

[![DK paskirstymo taisyklės.](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Naudoti DK paskirstymo taisykles** – biudžeto plano eilutės paskirstomos iš šaltinio biudžeto plano scenarijaus į paskirties biudžeto plano scenarijų pagal pasirinktą DK paskirstymo taisyklę. 

[![Kopijuoti iš biudžeto plano.](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopijuoti iš biudžeto plano** – naudojant paskirstymo platinimo būdą biudžeto plano eilutės sukuriamos paskirtyje, priklausomai nuo susijusio biudžeto plano eilučių. Tačiau naudojant šį būdą šaltinio biudžeto planas neturi būti pirminis, bet gali būti aukštesniame biudžeto plano hierarchijos lygmenyje. Šis paskirstymo būdas naudingas, jei į biudžetą iš pradžių buvo įtrauktos daug aukštesnio lygio konsoliduotos sumos, kurios turi būti perkeltos į žemesnį organizacijos lygį, kad prieš joms gaunant aukštesnio lygio patvirtinimą būtų galima atlikti išsamią peržiūrą ir koreguoti.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Paskirstymo būdų naudojimas biudžeto plane
Norėdami atlikti paskirstymus biudžeto plano puslapyje, pasirinkite eilutes, kurias reikia paskirstyti, tada spustelėkite **Paskirstyti biudžetą**.

[![Biudžeto paskirstymo mygtukas.](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Po to pasirinkite paskirstymo būdą. Tada pagal jūsų pasirinktą metodą nustatomi likusieji laukai. Šiuose laukuose nurodomas biudžeto plano duomenų šaltinis, paskirtis ir pasirinktis, kuri kuriant paskirties sumas leidžia padauginti šaltinį iš nurodyto koeficiento, kad būtų paprasčiau koreguoti kiekį. Taip pat galite nustatyti pasirinktį **Pridėti prie plano** . Jeigu norite pakeisti esamas biudžeto plano eilutes, pasirinkite **Ne** arba, jeigu norite išsaugoti esamas biudžeto plano eilutes ir įtraukti naujų eilučių, skirtų paskirstytoms sumoms, pasirinkite  **Taip**.

## <a name="automating-allocations-during-a-workflow"></a>Paskirstymų automatizavimas darbo eigos metu
Viena galinga funkcija leidžia paskirstymus atlikti automatiškai, kaip biudžeto planavimo darbo eigos dalį. Vykstant biudžeto plano darbo eigai automatizuotos užduotys gali iškviesti nurodyto biudžeto planavimo etapo paskirstymą. 

Norėdami nustatyti automatinį paskirstymą, pirmiausia puslapyje **Biudžeto planavimo konfigūracija** turite sukurti paskirstymo grafiką. Paskirstymo grafike nurodomas paskirstymo būdas, kuris bus naudojamas vykdant automatinį paskirstymą, ir įvairių paskirstymo pasirinkčių (žr. jų aprašymus ankstesniame skyriuje) reikšmės. 

Po to puslapyje **Biudžeto planavimo konfigūracija** sukurkite etapo paskirstymą. Etapo paskirstymas priskiria paskirstymo grafiką biudžeto planavimo darbo eigai ir etapui. 

Galiausiai pridėkite norimo darbo eigos etapo biudžeto planavimo etapo paskirstymo automatizuotą užduotį. Šiame pavyzdyje į darbo eigą įtraukti du biudžeto planavimo etapo paskirstymai (pažymėti raudonai).

[![Biudžeto planavimo etapo paskirstymai.](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
