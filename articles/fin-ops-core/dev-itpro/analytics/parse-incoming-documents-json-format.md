---
title: Gaunamų dokumentų analizė JSON formatu
description: Šioje temoje paaiškinama, kaip nustatyti elektroninių ataskaitų (ERŲ) formatus, kad būtų išanalizuoti gaunami dokumentai „JavaScript Object Notation“ (JSON) formatu.
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ba30b06cc0c4af230113d532a932594278e13b29a87e6252849483c9dfcbc198
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713923"
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

Be to, turite užbaigti užduočių vedlį [ER reikiamų konfigūracijų kūrimas, norint importuoti duomenis iš išorinio failo](tasks/er-required-configurations-import-data.md), jei jo dar neužbaigėte. Atsisiųskite toliau nurodytą failą norėdami užbaigti užduočių vedlį.

| Pareigos                  | Failo vardas |
|------------------------|-----------|
| ER modelio konfigūracija | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]