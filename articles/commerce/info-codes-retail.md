---
title: Informacijos kodai ir informacijos kodų grupės
description: Šiame straipsnyje apžvelgiami informacijos kodai, informacijos kodų grupės ir tai, kaip juos naudoti.
author: mugunthanm
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d4ab9b8546ee5b13edcb86b3e09004130eaeec07
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797025"
---
# <a name="info-codes-and-info-code-groups"></a>Informacijos kodai ir informacijos kodų grupės

[!include [banner](includes/banner.md)]

Šiame straipsnyje apžvelgiami informacijos kodai, informacijos kodų grupės ir tai, kaip juos naudoti.

Informacijos kodai suteikia būdą fiksuoti duomenis elektroninio kasos aparato (EKA) registre. Naudodami informacijos kodus galite paraginti kasininką įvesti informaciją atliekant įvairius veiksmus EKA, pvz., parduodant prekes, grąžinant prekes arba renkantis klientus. Kasininkai gali pasirinkti įvestį sąraše arba įvesti ją kaip kodą, numerį, datą arba tekstą. Galite priskirti informacijos kodus iš anksto nustatytiems parduotuvėms veiksmams, mažmeninėms prekėms, mokėjimo būdams, klientams ar tam tikrai elektroninio kasos aparato veiklai. Informacijos kodus galite naudoti norėdami atlikti šiuos veiksmus:

- Fiksuokite papildomą informaciją operacijos metu, pvz., skrydžio numerį arba grąžinimo priežastį.
- Paraginkite kasininką rinktis iš konkrečių produktų kainų sąrašo.
- Susiekite antrinį kodą su informacijos kodu, kuris paragina kasininką įvesti, kai atliekama tam tikra veikla. Pavyzdžiui, kai klientas grąžina produktą, galite paraginti kasininką paklausti, kodėl produktas grąžinamas. Tada naudodami antrinius kodus galite atidaryti priežasčių sąrašą, kuriame kasininkas galės pasirinkti.
- Parduokite produktą įprastai, su nuolaida arba kaip nemokamą produktą.
- Paraginkite kasininką įvesti reikšmę arba rinktis iš antrinių kodų sąrašo, jei kasos aparato stalčius atidaromas neatliekant pardavimo operacijos.

## <a name="info-codes-group"></a>Informacijos kodų grupė

„Commerce“ galite kurti informacijos kodų grupes. Informacijos kodų grupės suteikia lankstumo, nes galite nustatyti mažiau informacijos kodų, bet naudoti juos lanksčiau. Informacijos kodų grupes galite naudoti šiais būdais:

- Apibrėžkite mažiau informacijos kodų ir lengvai naudokite juos pakartotinai. Informacijos kodai, įtraukti į informacijos kodų grupes, neturi nustatytos priklausomybės nuo kitų informacijos kodų. Galite įtraukti tą patį informacijos kodą į kelias informacijos kodų grupes ir tada naudodami prioritetų nustatymo funkciją išdėstyti informacijos kodus tvarka, tinkama konkrečiai situacijai.
- Susiekite informacijos kodus su kitais informacijos kodais arba jų grupėmis, kad surinktumėte informaciją apie produktą arba operaciją, neapibrėždami atskiro informacijos kodo arba nesusiedami informacijos kodo kiekvienam scenarijui.

## <a name="info-code-examples"></a>Informacijos kodų pavyzdžiai

**1 pavyzdys. Pakartotinis informacijos kodų naudojimas**

Galima susieti informacijos kodus, kad paleidus vieną informacijos kodą, kitas kodas būtų paleistas iš karto po jo. Pavyzdžiui, parduodant tam tikrus produktus norite paraginti kasininką paklausti kliento, ar šis nenori įsigyti maitinimo elementų ir produkto garantijos. Parduodant kitus produktus, galite kasininką paraginti paklausti kliento, ar jis nenori įsigyti maitinimo elementų, ir paprašyti jo pašto kodo. Jei tokiems scenarijams sukūrėte susietus informacijos kodus, turite nustatyti kiekvieną informacijos kodo variantą, kad kasininkas būtų raginamas teirautis reikiamos informacijos. Jei naudojate informacijos kodų grupes, galite vieną kartą nustatyti bendrus informacijos kodus, pvz., klausimo apie maitinimo elementus, o tada naudoti juos keliose informacijos kodų grupėse. Taip pat galite nustatyti prioritetus informacijos kodų grupėse ir taip nurodyti tvarką, kuria rodomi paraginimai.

**2 pavyzdys. Informacijos kodų susiejimas su informacijos kodų grupėmis**

Parduodami tam tikrus produktus, pvz., mobiliuosius įrenginius, visada norite surinkti tam tikrą konkrečios informacijos rinkinį, pvz., telefono numerį, mobiliosios įrangos identifikatorių (MEID) ir serijos numerį. Bet norite surinkti kitokią informaciją apie planšetę nei apie mobilųjį telefoną. Galite nustatyti informacijos kodų grupę, kuri apima raginimus, skirtus telefono numeriui, MEID ir serijos numeriui, o tada susieti šią informacijos kodų grupę su konkrečiu informacijos kodu. Kai paleidžiamas produktui skirtas informacijos kodas, galima paleisti informacijos kodų grupę, kad galėtumėte surinkti bendruosius duomenis nenustatydami kelių susietų informacijos kodų rinkinių kiekvienam įrenginiui.


[!INCLUDE[footer-include](../includes/footer-banner.md)]