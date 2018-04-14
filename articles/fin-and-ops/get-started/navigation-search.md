---
title: "Naršymo ieška"
description: "Šioje temoje paaiškinama, kaip naudoti ieškos funkciją, norint pasiekti puslapius „Microsoft Dynamics 365 for Finance and Operations“."
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: be4ed89982e27d9b46a83bc945d7cd99ef892fbe
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="navigation-search"></a>Naršymo ieška

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip naudoti ieškos funkciją, norint pasiekti puslapius „Microsoft Dynamics 365 for Finance and Operations“.

„Finance and Operations‟ suteikia funkcijų įvairioms pramonės šakoms ir segmentams. Programa apima ne vieną sritį ir puslapį, kurie padeda atlikti įvairias užduotis. Norėdami greitai rasti puslapius, kurie reikalingi norint užbaigti užduotis, naudokite naršymo ieškos funkciją. 

Norėdami naudoti šią funkciją, spustelėkite **Ieškos** piktogramą, kad būtų rodomas **Ieškos** langelis. Tada langelyje galite surinkti vieną ar kelis žodžius. Sistema iš karto ieško susijusių programos puslapių, kurie atitinka jūsų įvestus žodžius. Pavyzdžiui, kaip įvestį galėtumėte įvesti „tiekėjo SF‟, tada sistema rodytų rezultatus, kurie atitinka tą įvestį. 

**Pastaba.** **Ieškos** langelis padeda rasti ir pereiti į puslapius. Jis nepadės rasti konkrečių duomenų ar veiksmų. 

[![search-box](media/navigation-search.png "Ieškos laukas") 

## <a name="quickly-navigate-to-a-particular-page"></a>Greitas perėjimas į konkretų puslapį
Naršymo ieškos funkcija taip pat naudojama kaip puikus būdas greitai pereiti į konkretų puslapį. Pavyzdžiui, jeigu esate mokėtinų sumų klerkas, kuris dažnai naudoja puslapį **Mokėjimų žurnalas**, lauke **Ieška** galėtumėte įvesti „mokėjimų žurnalas“. Kadangi įvestis visiškai atitinka puslapio pavadinimą, puslapis pateikiamas paieškos rezultatų viršuje ir galite greitai į jį patekti. 

Ieškos rezultatų sąraše rodomas puslapio pavadinimas bei naršymo kelias. Tai nurodo puslapio vietą programoje. Taip pat rezultatuose lengviau atskirti du ar kelis panašius puslapius. 

Kai ieškote puslapio, jūsų įvestis gretinama su puslapio pavadinimu bei jo naršymo keliu. Pavyzdžiui, jei lauke **Ieška** įvesite „gautinos‟, matysite puslapių rezultatus, pateikiamus srityje Gautinos sumos, nors puslapių pavadinimuose ir nėra žodžio „gautinos‟. 

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Greitas perėjimas į puslapį naudojant techninį formos pavadinimą
Naršymo ieškos funkcija taip pat suteikia patyrusių naudotojų labai pageidautą funkciją: galimybę greitai pereiti į puslapį pagal techninį formos pavadinimą. Daug naudotojų yra tiek susipažinę su sistema, jog žino tikslius formų, su kuriomis dirba, pavadinimus. Jei esate vienas iš šių naudotojų, galite įvesti **form:**, o po to – ieškomos formos pavadinimą. Pavyzdžiui, jei įvesite **form: vendinvoice**, ieškos rezultatuose bus rodomi visi puslapiai, kur formos pavadinimas prasideda **vendinvoice**. 

## <a name="administration-and-security"></a>Administravimas ir sauga
Administravimo ir saugos požiūriu, naudojant naršymo ieškos funkciją, rodomi tik dviejų tolesnių tipų rezultatai.

-   Puslapiai, įgalinti dabartinėje konfigūracijoje (naudojant konfigūracijos raktus).
-   Puslapiai, prie kurių vartotojas turi prieigą pagal vartotojo vaidmenį.

Ieškos rezultatų sąrašas apribotas iki 10 elementų. Jei rezultatuose nerandate to, ko ieškote, reikėtų pabandyti patikslinti ar atnaujinti įvestį. 

## <a name="development"></a>Plėtra 
Programavimo požiūriu naršymo ieškos funkciją labai lengva įdiegti, nes tarp meniu elementų diegimo ir jų rodymo ieškos rezultatuose praktiškai nėra vėlavimo. Kol į meniu elementus nurodoma iš naršymo srities ar ataskaitų srities, jie automatiškai tampa ieškotinais. 

