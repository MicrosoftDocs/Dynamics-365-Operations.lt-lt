---
title: Naršymo ieška
description: Šiame straipsnyje paaiškinama, kaip naudoti ieškos funkciją, norint naršyti į puslapius.
author: jasongre
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.openlocfilehash: 4c362e4cd83f926e7e21d775abd24ae6ddfcbbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292344"
---
# <a name="navigation-search"></a>Naršymo ieška

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šiame straipsnyje paaiškinama, kaip naudoti ieškos funkciją, norint naršyti į puslapius.

Programa apima ne vieną sritį ir puslapį, kurie padeda atlikti įvairias užduotis. Norėdami greitai rasti puslapius, kurie reikalingi norint užbaigti užduotis, naudokite naršymo ieškos funkciją.

Norėdami naudoti šią funkciją, spustelėkite **Ieškos** piktogramą, kad būtų rodomas **Ieškos** langelis. Tada langelyje galite surinkti vieną ar kelis žodžius. Sistema iš karto ieško susijusių programos puslapių, kurie atitinka jūsų įvestus žodžius. Pavyzdžiui, kaip įvestį galėtumėte įvesti „tiekėjo SF‟, tada sistema rodytų rezultatus, kurie atitinka tą įvestį.

> [!NOTE]
> **Ieškos** langelis padeda rasti ir pereiti į puslapius. Jis nepadės rasti konkrečių duomenų ar veiksmų.

![ieškos laukas.](media/navigation-search.png "Ieškos laukas")

## <a name="quickly-navigate-to-a-particular-page"></a>Greitas perėjimas į konkretų puslapį

Naršymo ieškos funkcija taip pat naudojama kaip puikus būdas greitai pereiti į konkretų puslapį. Pavyzdžiui, jeigu esate mokėtinų sumų klerkas, kuris dažnai naudoja puslapį **Mokėjimų žurnalas**, lauke **Ieška** galėtumėte įvesti „mokėjimų žurnalas“. Kadangi įvestis visiškai atitinka puslapio pavadinimą, puslapis pateikiamas paieškos rezultatų viršuje ir galite greitai į jį patekti.

Ieškos rezultatų sąraše rodomas puslapio pavadinimas bei naršymo kelias. Tai nurodo puslapio vietą programoje. Taip pat rezultatuose lengviau atskirti du ar kelis panašius puslapius.

Kai ieškote puslapio, jūsų įvestis gretinama su puslapio pavadinimu bei jo naršymo keliu. Pavyzdžiui, jei **ieškos** lauke įvesite „gautinos‟, matysite rezultatus, galimus Gautinų sumų srityje – nors puslapių pavadinimuose ir nėra žodžio „gautinos‟.

## <a name="quickly-navigate-to-a-page-based-on-the-technical-form-name"></a>Greitas perėjimas į puslapį naudojant techninį formos pavadinimą

Naršymo ieškos funkcija taip pat suteikia patyrusių naudotojų labai pageidautą funkciją: galimybę greitai pereiti į puslapį pagal techninį formos pavadinimą. Daug naudotojų yra tiek susipažinę su sistema, jog žino tikslius formų, su kuriomis dirba, pavadinimus. Jei esate vienas iš šių naudotojų, galite įvesti **form:**, o po to – ieškomos formos pavadinimą. Pavyzdžiui, jei įvesite **form: vendinvoice**, ieškos rezultatuose bus rodomi visi puslapiai, kur formos pavadinimas prasideda **vendinvoice**.

## <a name="administration-and-security"></a>Administravimas ir sauga

Administravimo ir saugos požiūriu, naudojant naršymo ieškos funkciją, rodomi tik dviejų tolesnių tipų rezultatai.

- Puslapiai, įgalinti dabartinėje konfigūracijoje (naudojant konfigūracijos raktus).
- Puslapiai, prie kurių vartotojas turi prieigą pagal vartotojo vaidmenį.

Ieškos rezultatų sąrašas apribotas iki 10 elementų. Jei rezultatuose nerandate to, ko ieškote, reikėtų pabandyti patikslinti ar atnaujinti įvestį.

## <a name="development"></a>Plėtra

Programavimo požiūriu naršymo ieškos funkciją labai lengva įdiegti, nes tarp meniu elementų diegimo ir jų rodymo ieškos rezultatuose praktiškai nėra vėlavimo. Kol į meniu elementus nurodoma iš naršymo srities ar ataskaitų srities, jie automatiškai tampa ieškotinais.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
