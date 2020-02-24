---
title: Produktų duomenų objektai
description: Šioje temoje pateikiama informacijos apie skirtingus objektus, kuriuos naudojant galima importuoti ir eksportuoti produktų duomenis.
author: cvocph
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 83191ea3d07ec9e2ed6261ee997e06b802ee7645
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935944"
---
# <a name="product-data-entities"></a>Produktų duomenų objektai

[!include [banner](../includes/banner.md)]

Norėdami importuoti ir eksportuoti produktų duomenis, turite naudoti duomenų objektus. Tolesnėje lentelėje pateikiama išsami informacija apie su produktais susijusių duomenų objektus ir aprašoma kiekvieno iš jų paskirtis.

| Objektas | Programos objektų medžio (AOT) pavadinimas (tipas) | Pastabos |
|--------|-------------------------------------------|-------|
| Produktai V2 | EcoResProductV2Entity | Šis objektas naudojamas bendrai naudojamiems produktams – išskirtiesiems produktams bei bendriesiems produktams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Jis nepalaiko rinkiniu pagrįstų SQL operacijų. Jį galima naudoti su „Open Data Protocol“ („OData“). |
| Išleisti produktai V2 | EcoResReleasedProductV2Entity | Šis objektas naudojamas išleistiems produktams – išskirtiesiems produktams bei bendriesiems produktams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Norint jį naudoti, jau turi būti sukurtas bendrai naudojamas produktas. Importavus naują išleistą produktą, išleidžiamas bendrai naudojamas produktas. Taip pat yra atskirų objektų, kuriuos naudojant galima importuoti ir eksportuoti išleistus bendruosius produktus bei išleistus išskirtuosius variantus. Šis objektas nepalaiko rinkiniu pagrįstų SQL operacijų ar naikinimo operacijų. Jį galima naudoti su „OData“. |
| Išleisto produkto kūrimas V2 | EcoResReleasedProductCreationV2Entity | Naudojant šį objektą, vienu veiksmu importuojami bendrai naudojami produktai ir išleisti produktai. Nors objektas palaiko eksportavimo galimybę, taip jo naudoti nerekomenduojama, nes objektas skirtas produktams kurti. Jis nepalaiko naujinimų. Jis palaiko ribotą laukų rinkinį (laukų, esančių produktų kūrimo dialogo lange). Jis nepalaiko rinkiniu pagrįstų SQL operacijų. Jis nėra pasiekiamas naudojant „OData“. |
| Produkto variantai | EcoResProductVariantEntity | Šis objektas naudojamas bendrai naudojamiems produktų variantams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Norint jį naudoti, jau turi būti sukurtos dimensijų reikšmės. Integravimo raktas yra bendrasis produktas su produkto dimensijomis. Šis objektas nepalaiko rinkiniu pagrįstų SQL operacijų. Jį galima naudoti su „OData“. Jis palaiko naikinimo operacijas. Jo negalima išplėsti įtraukiant naujų produkto dimensijų. |
| Produktų variantai pagal produktų numerių identifikavimą | EcoResProductNumberIdentifiedProductVariantEntity | Šis objektas naudojamas bendrai naudojamiems produktų variantams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Norint jį naudoti, jau turi būti sukurtos dimensijų reikšmės. Integravimo raktas yra produkto numeris (o objekto **Produkto variantai** integravimo raktas yra bendrasis produktas su produkto dimensijomis). |
| Patvirtinto produkto variantai | EcoResReleasedProductVariantEntity | Šis objektas naudojamas išleistiems produktų variantams importuoti ir eksportuoti. Jį naudojant galima naujinimo funkcija. Norint jį naudoti, jau turi būti sukurti bendrai naudojami produkto variantai. Importavus naują išleistą produkto variantą, išleidžiamas bendrai naudojamas produkto variantas. Šis objektas nepalaiko rinkiniu pagrįstų SQL operacijų. Jį galima naudoti su „OData“. Nors objektas palaiko naikinimo operacijas, taip jį naudojant sugadinami duomenys, nes dabartinėje platformoje yra klaida. Šio objekto negalima išplėsti įtraukiant naujų produkto dimensijų. |
| Išleisti produktų variantai pagal produktų numerių identifikavimą | EcoResProductNumberIdentifiedReleasedProductVariantEntity | Šis objektas yra panašus į objektą **Išleisti produkto variantai**, tačiau integravimo raktas yra produkto numeris, o ne bendrasis produktas su produkto dimensijomis. Jį galima išplėsti įtraukiant naujų produkto dimensijų. |
| Parduodami išleisti produktai | EcoResSellableReleasedProductEntity | Šis objektas naudojamas tik parduodamiesiems produktams eksportuoti. Parduodamieji produktai – tai produktai, apie kuriuos pateikta informacija, reikalinga norint produktus naudoti pardavimo užsakyme. Tos pačios taisyklės taikomos, kai produktas patikrinamas naudojant puslapio **Išleisti produktai** funkciją **Tikrinti**. |
| Išleisti išskirtieji produktai V2 | EcoResDistinctProductV2Entity | Šis objektas naudojamas išskirtiesiems produktams eksportuoti. Išskirtieji produktai gali būti produktai, potipio produktai ir produkto variantai. |
| Išleisti bendrieji produktai V2 | EcoResProductMasterV2Entity | Šis objektas naudojamas bendriesiems produktams importuoti ir eksportuoti. Jis neturi duomenų tvarkymo galimybės. |
| Prekė - brūkšninis kodas | EcoResProductBarcodeEntity | Šis objektas naudojamas produktams ir brūkšniniams kodams eksportuoti. |
| Produktų ciklo būsenos | EcoResProductLifecycleSateEntity | Naudojant šį objektą, galima importuoti ir eksportuoti skirtingas produktų ciklo būsenas, kurios gali būti priskiriamos produktui. |

> [!NOTE]
> Naudodami duomenų objektą **Išleisti produktai V2**, produktų į sistemą galite importuoti, tik jei jau sukurtas bendrai naudojamas produktas. Kitu atveju, norėdami į sistemą importuoti produktų, turite naudoti duomenų objektą **Produktų kūrimas**.