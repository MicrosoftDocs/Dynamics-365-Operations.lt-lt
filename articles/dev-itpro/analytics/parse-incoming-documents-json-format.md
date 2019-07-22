---
title: Gaunamų dokumentų analizė JSON formatu
description: Šioje temoje paaiškinama, kaip nustatyti elektroninių ataskaitų (ERŲ) formatus, kad būtų išanalizuoti gaunami dokumentai „JavaScript Object Notation“ (JSON) formatu.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703926"
---
# <a name="parse-incoming-documents-in-json-format"></a>Gaunamų dokumentų analizė JSON formatu

[!include[banner](../includes/banner.md)]

Galite sukurti elektroninių ataskaitų (ER) formatus ir išanalizuoti gaunamus elektroninius dokumentus, kuriuose yra duomenų teksto formatu „JavaScript“ pagrindu (kitaip tariant, failų „JavaScript Object Notation“ \[JSON\] formatu).

Norėdami apie šią funkciją sužinoti daugiau, atsisiųskite toliau pateiktoje lentelėje nurodytus failus ir paleiskite ER užduočių vedlį Formato konfigūracijos kūrimas importuojant duomenis iš išorinio JSON failo. Šiame užduočių vedlyje nurodoma, kaip naudojantis ER formatu išanalizuoti gaunamą JSON failą, kad būtų galima atnaujinti programos duomenis.

| Pareigos                                  | Failo vardas |
|----------------------------------------|-----------|
| ER formato konfigūracija                | [Tiekėjų failo trans_JSON.xml importavimo formatas](https://go.microsoft.com/fwlink/?linkid=874111) |
| Gaunamo failo .csv formatu pavyzdys | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Reikalavimai

Norint atlikti ER užduočių vedlio Formato konfigūracijos kūrimas importuojant duomenis iš išorinio JSON failo veiksmus, turi būti laikomasi toliau nurodyto reikalavimo.

- Pirminiai JSON failo elementai gali būti tik objekto elementai.
- Įdėtieji objekto elementai turėtų būti ypatybių elementai, kad būtų sukuriama tinkama JSON struktūra.
- JSON masyvai gali būti tik įdėtieji objekto ypatybių elementų elementai.
- JSON masyvus gali sudaryti tik JSON objektai. Juose negali būti tiesioginių eilučių / skaitinių verčių ir įdėtųjų masyvų. Šių masyvų elementai išanalizuojami formate nurodyta tvarka. Atsižvelgiama į kiekvieno JSON objekto daugialypumo nuostatas.

Be to, turite užbaigti užduočių vedlį [ER Reikiamų konfigūracijų kūrimas elektroninėse ataskaitose, norint importuoti duomenis iš išorinio failo](tasks/er-required-configurations-import-data.md), jei jo dar neužbaigėte. Atsisiųskite toliau nurodytą failą norėdami užbaigti užduočių vedlį.

| Pareigos                  | Failo vardas |
|------------------------|-----------|
| ER modelio konfigūracija | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |
