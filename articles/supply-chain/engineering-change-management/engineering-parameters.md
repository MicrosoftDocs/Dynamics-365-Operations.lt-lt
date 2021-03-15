---
title: Inžinierinių pakeitimų valdymo parametrai
description: Šioje temoje paaiškina, kaip konfigūruoti inžinerijos keitimus valdymo funkcijose „Microsoft Dynamics 365 Supply Chain Management“.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: dee5429c31bfc872afedfa76ced89633b4b72c96
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005382"
---
# <a name="engineering-change-management-parameters"></a>Inžinierinių pakeitimų valdymo parametrai

[!include [banner](../includes/banner.md)]

**Inžinerijos keitimo valdymo parametrų** puslapyje pateikti nustatymo parametrai, kurie keičia nustatytąją elgseną susietą su leidimo produkto struktūra ir inžinerijos keitimo valdymo procesuose.

## <a name="open-the-engineering-change-management-parameters-page"></a>Atverkite inžinerijos keitimo valdymo parametrų puslapį

Siekiant atverti **Inžinerijos keitimo valdymo parametrų** puslapį, eikite į **Inžinerijos keitimo valdymas \> Nustatymai \> Inžinerijos keitimo valdymo parametrai**. Tuomet galite nustatyti laukelius kaip aprašyta likusiose šios temos skyriuose.

## <a name="release-control-tab"></a>Paleiskite valdiklio skirtuką

Tolesnė lentelė aprašo laukelius, kurie yra prienami **Leidimo valdiklio** skirtuke puslapyje **Inžinerijos keitimo valdymo parametrai**. Šie laukeliai keičia leidimo produkto struktūros procesą.

| Laukas | aprašymas |
|---|---|
| Prekės numerio taisyklė | Pasirinkite, kaip prekės skaičius turi būti nustatytas, kai produktas yra išleistas juridiniam asmeniui. Pasirinkite *Inžinerijos produkto skaičius* jei produkto skaičius gaunančiame juridiniame asmenyje turi atitikti produkto skaičių inžinerijos įmonėje. Pasirinkite *Vietinė prekės skaičiaus seka* jei produktas turi paimti koitą skaičių skaičių sekoje produktų skaičiams gaunančiame juridiniame asmenyje. |
| KS pavadinimo taisyklė | Pasirinkite, kaip medžagų važtaraščio pavadinimas (BOM) yra nustatytas, kai produktas gaunamas (išleidžiamas) juridiniame asmenyje. Pasirinkite ar *Inžinerijos pavadinimą* ar *Gavimo prekės skaičius*. |
| Maršruto pavadinimo taisyklė | Pasirinkite, kaip maršruto pavadinimas turi būti nustatytas, kai produkto maršrutas yra gaunamas (išleidžiamas) juridiniame asmenyje. Pasirinkite ar *Inžinerijos pavadinimą* ar *Gavimo prekės skaičius*. |
| Vykdyti KS patikrą | Pasirinkite, ar BOM patikra bus vykdoma, kai produktas gaunamas (išleidžiamas) juridiniame asmenyje. |
| Neaktyvios KS išleidimo būdas | Pasirinkite, ar produktas gali būti išleistas, jei yra neįjungtas BOM. Pasirinkite *Priimti*, *Tik įspėti* ar *Neleidžiama*. |
| Neaktyvaus maršruto išleidimo būdas | Pasirinkite, ar produktas gali būti išleistas, jei yra neįjungtas maršrutas. Pasirinkite *Priimti*, *Tik įspėti* ar *Neleidžiama*.|
| Produkto priėmimas | Pasirinkite, ar papildomas priėmimo žingsnis yra būtinas prieš tai, kai produktas gali būti išleistas jurdiniam asmeniui. Pasirinkite *Rankinis* tam, kad įtrauktumėte priėmimo žingsnį. Tokiu atveju, **Atverkite produkto išleidimų** puslapį, kuris rodys produktus. Pasirinkite *Automatinis* tam, kad jis rodytų produktą tiesiogiai **Išleisti produktai** puslapyje tiksliniame juridiniame asmenyje iš karto po to, kai produktas išleistas kartu su išleisto produkto struktūra. |

## <a name="engineering-change-management-tab"></a>Inžinerijos keitimo valdymo skirtukas

Tolesnė lentelė aprašo laukelius, kurie yra prienami **Inžinerijos keitimo valdymas** skirtuke puslapyje **Inžinerijos keitimo valdymo parametrai**. Šie nustatymai paveikia inžinerijos keitimo valdymo procesą.

| Laukas | aprašymas |
|---|---|
| Kategorija | Nustatytoji kategorija bus naudojama, kai inžinerijos keitimo užklausa sukuriama. |
| Pirmenybė | Nustatytoji pirmenybė bus naudojama, kai inžinerijos keitimo užklausa sukuriama. |
| Svarbos taisyklė | Pasirinkite, kaip inžinerijos keitimo užsakymo sunkumas turi būti įsteigtas. Pasirinkite *Rankinis*, jei vartotojas turi įvesti vertę **Sunkumo** laukelyje. Rinkitės *Apskaičiuoti* tam, kad sistema apskaičiuotų **Sunkumo** laukelio vertę jums pasirinkus **Skaičiuoti sunkumą** inžinerijos keitimo užsakymo veiksmų juostoje. šiuo atveju sistema naudos sunkumo taisykles, kurios nustatytos **Sunkumo taisyklių rinkinio** puslapyje. Rinkitės *Skaičiuoti automatiškai* tam, kad vertė **Sunkumo** laukelyje būtų skaičiuojama automatiniu būdu ir užpildoma pagal sunkumo taisyklių rinkinius. |
| Pakartotinai išleisti paveiktus produktus | Šis laukelis taikomas jums išleidžiant produktus per inžinerijos keitimo užsakymą. Jums pasirinkus, ar visi produktai ar tik paveikti produktai turi būti siūlomi **Leidimų** teksto laukelyje. |
| KS lygiai, kuriuos reikia išleisti | BOM lygio gylis leidimo metu. Jei BOM turi daugiau lygių (tai yra, jei jis gilesnis), tuomet vertė yra nurodyta čia, bus išleisti tik nurodytos vertės didesni lygiai. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]