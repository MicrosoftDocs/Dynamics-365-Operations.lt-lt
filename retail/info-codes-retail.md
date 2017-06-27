---
title: Informacijos kodai
description: "Šiame straipsnyje apžvelgiami informacijos kodai, informacijos kodų grupės ir tai, kaip juos naudoti."
author: mugunthanm
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5790f54a531336b30ee140ebf8b9c782d8b347f7
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="info-codes"></a>Informacijos kodai

[!include[banner](includes/banner.md)]


Šiame straipsnyje apžvelgiami informacijos kodai, informacijos kodų grupės ir tai, kaip juos naudoti.

Informacijos kodai suteikia būdą fiksuoti duomenis elektroninio kasos aparato (EKA) registre. Naudodami informacijos kodus galite paraginti kasininką įvesti informaciją atliekant įvairius veiksmus EKA, pvz., parduodant prekes, grąžinant prekes arba renkantis klientus. Kasininkai gali pasirinkti įvestį sąraše arba įvesti ją kaip kodą, numerį, datą arba tekstą. Galite priskirti informacijos kodus iš anksto nustatytiems parduotuvėms veiksmams, mažmeninėms prekėms, mokėjimo būdams, klientams ar tam tikrai elektroninio kasos aparato veiklai. Informacijos kodus galite naudoti norėdami atlikti šiuos veiksmus:
-   Fiksuokite papildomą informaciją operacijos metu, pvz., skrydžio numerį arba grąžinimo priežastį.
-   Paraginkite kasininką rinktis iš konkrečių produktų kainų sąrašo.
-   Susiekite antrinį kodą su informacijos kodu, kuris paragina kasininką įvesti, kai atliekama tam tikra veikla. Pavyzdžiui, kai klientas grąžina produktą, galite paraginti kasininką paklausti, kodėl produktas grąžinamas. Tada naudodami antrinius kodus galite atidaryti priežasčių sąrašą, kuriame kasininkas galės pasirinkti.
-   Parduokite produktą įprastai, su nuolaida arba kaip nemokamą produktą.
-   Paraginkite kasininką įvesti reikšmę arba rinktis iš antrinių kodų sąrašo, jei kasos aparato stalčius atidaromas neatliekant pardavimo operacijos.

## <a name="info-codes-group-in-retail-and-commerce"></a>Mažmeninės prekybos ir prekybos informacijos kodų grupės
„Dynamics 365 for Operations“ – versija „Retail“, galite kurti informacijos kodų grupes. Informacijos kodų grupės suteikia lankstumo, nes galite nustatyti mažiau informacijos kodų, bet naudoti juos lanksčiau. Informacijos kodų grupes galite naudoti šiais būdais:
-   Apibrėžkite mažiau informacijos kodų ir lengvai naudokite juos pakartotinai. Informacijos kodai, įtraukti į informacijos kodų grupes, neturi nustatytos priklausomybės nuo kitų informacijos kodų. Galite įtraukti tą patį informacijos kodą į kelias informacijos kodų grupes ir tada naudodami prioritetų nustatymo funkciją išdėstyti informacijos kodus tvarka, tinkama konkrečiai situacijai.
-   Susiekite informacijos kodus su kitais informacijos kodais arba jų grupėmis, kad surinktumėte informaciją apie produktą arba operaciją, neapibrėždami atskiro informacijos kodo arba nesusiedami informacijos kodo kiekvienam scenarijui.

## <a name="info-code-examples"></a>Informacijos kodų pavyzdžiai
**1 pavyzdys. Pakartotinis informacijos kodų naudojimas** Informacijos kodus galima susieti, kad paleidus vieną informacijos kodą, kitas kodas būtų paleistas iš karto po jo. Pavyzdžiui, parduodant tam tikrus produktus norite paraginti kasininką paklausti kliento, ar šis nenori įsigyti maitinimo elementų ir produkto garantijos. Parduodant kitus produktus, galite kasininką paraginti paklausti kliento, ar jis nenori įsigyti maitinimo elementų, ir paprašyti jo pašto kodo. Jei tokiems scenarijams sukūrėte susietus informacijos kodus, turite nustatyti kiekvieną informacijos kodo variantą, kad kasininkas būtų raginamas teirautis reikiamos informacijos. Jei naudojate informacijos kodų grupes, galite vieną kartą nustatyti bendrus informacijos kodus, pvz., klausimo apie maitinimo elementus, o tada naudoti juos keliose informacijos kodų grupėse. Taip pat galite nustatyti prioritetus informacijos kodų grupėse ir taip nurodyti tvarką, kuria rodomi paraginimai.


**2 pavyzdys. Informacijos kodų susiejimas su informacijos kodų grupėmis** Parduodami tam tikrus produktus, pvz., mobiliuosius įrenginius, visada norite surinkti tam tikrą informacijos rinkinį, pvz., telefono numerį, mobiliosios įrangos identifikatorių (MEID) ir serijos numerį. Bet norite surinkti kitokią informaciją apie planšetę nei apie mobilųjį telefoną. Galite nustatyti informacijos kodų grupę, kuri apima raginimus, skirtus telefono numeriui, MEID ir serijos numeriui, o tada susieti šią informacijos kodų grupę su konkrečiu informacijos kodu. Kai paleidžiamas produktui skirtas informacijos kodas, galima paleisti informacijos kodų grupę, kad galėtumėte surinkti bendruosius duomenis nenustatydami kelių susietų informacijos kodų rinkinių kiekvienam įrenginiui.

 



