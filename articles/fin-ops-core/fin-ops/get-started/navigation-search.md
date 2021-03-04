---
title: Naršymo ieška
description: Šioje temoje aiškinama, kaip naudoti ieškos funkciją, norint pasiekti puslapius.
author: aneesmsft
manager: AnnBe
ms.date: 04/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 25991
ms.assetid: eef0676f-c4b1-490e-a032-e9c8580f3fea
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b68182ff7da07f350e2eacaf569089e0fdf44a8d
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4695066"
---
# <a name="navigation-search"></a>Naršymo ieška

[!include [banner](../includes/banner.md)]

Šioje temoje aiškinama, kaip naudoti ieškos funkciją, norint pasiekti puslapius.

Programa apima ne vieną sritį ir puslapį, kurie padeda atlikti įvairias užduotis. Norėdami greitai rasti puslapius, kurie reikalingi norint užbaigti užduotis, naudokite naršymo ieškos funkciją.

Norėdami naudoti šią funkciją, spustelėkite **Ieškos** piktogramą, kad būtų rodomas **Ieškos** langelis. Tada langelyje galite surinkti vieną ar kelis žodžius. Sistema iš karto ieško susijusių programos puslapių, kurie atitinka jūsų įvestus žodžius. Pavyzdžiui, kaip įvestį galėtumėte įvesti „tiekėjo SF‟, tada sistema rodytų rezultatus, kurie atitinka tą įvestį.

> [!NOTE]
> **Ieškos** langelis padeda rasti ir pereiti į puslapius. Jis nepadės rasti konkrečių duomenų ar veiksmų.

[![ieškos laukas](media/navigation-search.png "Ieškos laukas")

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