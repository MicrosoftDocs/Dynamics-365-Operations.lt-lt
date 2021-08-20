---
title: Produktų duomenų objektai
description: Šioje temoje pateikiama informacijos apie skirtingus objektus, kuriuos naudojant galima importuoti ir eksportuoti produktų duomenis.
author: cvocph
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: f40b4157520a399f1c2971a425e47b904b3b2f5eb30b87e54f8b810647bcdaeb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747918"
---
# <a name="product-data-entities"></a>Produktų duomenų objektai

[!include [banner](../includes/banner.md)]

Norėdami importuoti ir eksportuoti produktų duomenis, turite naudoti duomenų objektus. Tolesnėje lentelėje pateikiama išsami informacija apie su produktais susijusių duomenų objektus ir aprašoma kiekvieno iš jų paskirtis.

| Objektas | Programos objektų medžio (AOT) pavadinimas (tipas) | Pastabos |
|--------|-------------------------------------------|-------|
| Produktai V2 | `EcoResProductV2Entity` | Šis objektas naudojamas bendrai naudojamiems produktams – išskirtiesiems produktams bei bendriesiems produktams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Jis nepalaiko rinkiniu pagrįstų SQL operacijų. Jį galima naudoti su „Open Data Protocol“ („OData“). |
| Išleisti produktai V2 | `EcoResReleasedProductV2Entity` | Šis objektas naudojamas išleistiems produktams – išskirtiesiems produktams bei bendriesiems produktams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Norint jį naudoti, jau turi būti sukurtas bendrai naudojamas produktas. Importavus naują išleistą produktą, išleidžiamas bendrai naudojamas produktas. Taip pat yra atskirų objektų, kuriuos naudojant galima importuoti ir eksportuoti išleistus bendruosius produktus bei išleistus išskirtuosius variantus. Šis objektas nepalaiko rinkiniu pagrįstų SQL operacijų ar naikinimo operacijų. Jį galima naudoti su „OData“. |
| Išleisto produkto kūrimas V2 | `EcoResReleasedProductCreationV2Entity` | Naudojant šį objektą, vienu veiksmu importuojami bendrai naudojami produktai ir išleisti produktai. Nors objektas palaiko eksportavimo galimybę, taip jo naudoti nerekomenduojama, nes objektas skirtas produktams kurti. Jis nepalaiko naujinimų. Jis palaiko ribotą laukų rinkinį (laukų, esančių produktų kūrimo dialogo lange). Jis nepalaiko rinkiniu pagrįstų SQL operacijų. Jis nėra pasiekiamas naudojant „OData“. |
| Produkto variantai | `EcoResProductVariantEntity` | Šis objektas naudojamas bendrai naudojamiems produktų variantams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Norint jį naudoti, jau turi būti sukurtos dimensijų reikšmės. Integravimo raktas yra bendrasis produktas su produkto dimensijomis. Šis objektas nepalaiko rinkiniu pagrįstų SQL operacijų. Jį galima naudoti su „OData“. Jis palaiko naikinimo operacijas. Jo negalima išplėsti įtraukiant naujų produkto dimensijų. |
| Produktų variantai pagal produktų numerių identifikavimą | `EcoResProductNumberIdentifiedProductVariantEntity` | Šis objektas naudojamas bendrai naudojamiems produktų variantams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Norint jį naudoti, jau turi būti sukurtos dimensijų reikšmės. Integravimo raktas yra produkto numeris (o objekto **Produkto variantai** integravimo raktas yra bendrasis produktas su produkto dimensijomis). |
| Patvirtinto produkto variantai | `EcoResReleasedProductVariantEntity` | Šis objektas naudojamas išleistiems produktų variantams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Norint jį naudoti, jau turi būti sukurti bendrai naudojami produkto variantai. Importavus naują išleistą produkto variantą, išleidžiamas bendrai naudojamas produkto variantas. Šis objektas nepalaiko rinkiniu pagrįstų SQL operacijų. Jį galima naudoti su „OData“. Nors objektas palaiko naikinimo operacijas, taip jį naudojant sugadinami duomenys, nes dabartinėje platformoje yra klaida. Šio objekto negalima išplėsti įtraukiant naujų produkto dimensijų. |
| Išleisti produktų variantai pagal produktų numerių identifikavimą | `EcoResProductNumberIdentifiedReleasedProductVariantEntity` | Šis objektas yra panašus į objektą **Išleisti produkto variantai**, tačiau integravimo raktas yra produkto numeris, o ne bendrasis produktas su produkto dimensijomis. Jį galima išplėsti įtraukiant naujų produkto dimensijų. |
| Parduodami išleisti produktai | `EcoResSellableReleasedProductEntity` | Šis objektas naudojamas tik parduodamiesiems produktams eksportuoti. Parduodamieji produktai – tai produktai, apie kuriuos pateikta informacija, reikalinga norint produktus naudoti pardavimo užsakyme. Tos pačios taisyklės taikomos, kai produktas patikrinamas naudojant puslapio **Išleisti produktai** funkciją **Tikrinti**. |
| Išleisti išskirtieji produktai V2 | `EcoResDistinctProductV2Entity` | Šis objektas naudojamas išskirtiesiems produktams eksportuoti. Išskirtieji produktai gali būti produktai, potipio produktai ir produkto variantai. |
| Išleisti bendrieji produktai V2 | `EcoResProductMasterV2Entity` | Šis objektas naudojamas bendriesiems produktams importuoti ir eksportuoti. Jis neturi duomenų tvarkymo galimybės. |
| Elementas - brūkšninis kodas | `EcoResProductBarcodeEntityV3` | Šis objektas naudojamas produktams ir brūkšniniams kodams eksportuoti. Šis objektas neleidžia keisti sekimo, naujinimų ar panaikinimų, Norėdami naudoti brūkšninių kodų keičiamą sekimą, naujinimus ar naikinimus, naudokite **Elementas - brūkšninio kodo susiejimo** objektą. |
| Prekė – brūkšninių kodų susiejimas | `EcoResProductBarcodeAssociationEntity` | Šis objektas naudojamas produktams ir brūkšniniams kodams eksportuoti. Jis leidžia keisti sekimą, naujinimus ir panaikinimus. Norėdami naudoti objektą, funkcija  *Elementas - brūkšninio kodo pagerinimai* turi būti įjungta  [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Tai objekto raktas `AssociationID`, kuris sukuria sąsają tarp brūkšninio kodo ir gaminio. Norėdami įtraukti pagalbą šiam raktui, lentelė `InventitemBarcodeAssociation` bus užpildoma esančiais elemento brūkšninio kodo duomenimis jums įjungus funkciją. Lentelė yra užpildoma naudojant krūvos darbą ir jei jūsų brūkšninio kodo lentelė turi didelį skaičių įrašų, gali užtrukti nemažai laiko krūvos darbo vykdymui. Dėl to, rekomenduojame jums planuoti įjungti funkciją (dėl to, vykdyti krūvos darbą), kai tai suderinta su jūsų verslo grafiku. |
| Produktų ciklo būsenos | `EcoResProductLifecycleSateEntity` | Naudojant šį objektą, galima importuoti ir eksportuoti skirtingas produktų ciklo būsenas, kurios gali būti priskiriamos produktui. |

> [!NOTE]
> Naudodami duomenų objektą **Išleisti produktai V2**, produktų į sistemą galite importuoti, tik jei jau sukurtas bendrai naudojamas produktas. Kitu atveju, norėdami į sistemą importuoti produktų, turite naudoti duomenų objektą **Produktų kūrimas**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]