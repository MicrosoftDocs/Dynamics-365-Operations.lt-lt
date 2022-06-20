---
title: Gaunamų dokumentų analizė „Excel“ formatu
description: Šiame straipsnyje pateikiama informacija apie elektroninių ataskaitų (ER) formatų dizainą norint išanalizuoti gaunamų failų Microsoft Excel turinį.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 64371ffb09836d6d60ba2073c706628d2009116e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858686"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Gaunamų dokumentų analizė „Excel“ formatu

[!include[banner](../includes/banner.md)]

Galite sukurti elektroninių ataskaitų (ER) formatus, skirtus analizuoti gaunamus „Microsoft Excel“ failus, kurie atitinka „Microsoft Excel“ darbaknygių duomenis (XLSX formato failus). Tada galite naudoti šių failų turinį programos duomenims atnaujinti. Tai naudinga, jei:

- Sukurkite naują modelį ir formatą ir patikrinkite juos vykdymo metu. Tokiu atveju, „Excel“ imituoja faktinius programos duomenis.
- Tvarkykite duomenis už savo programos ribų programoje „Excel“ ir importavę šiuos duomenis pateikite konkrečią ataskaitą.

Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlius **ER importavimo duomenys iš „Microsoft Excel“ failo (1 dalis: formato kūrimas)** ir **ER importavimo duomenys iš „Microsoft Excel“ failo (2 dalis: duomenų importavimas)** (verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) dalys). Šie užduočių vedliai parodys jums, kaip galima analizuoti gaunamą „Excel“ failą naudojant ER formatą, skirtą importuoti informaciją iš gaunamų dokumentų ir atnaujinti programos duomenis. Užduočių vedlių failus galite atsisiųsti iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684).

Atsisiųskite šiuos failus norėdami užbaigti aukščiau minėtus užduočių vedlius:

| Turinio aprašas                         | Failas                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Gaunamas failas XLSX formatu – šablonas    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Gaunamas failas XLSX formatu – duomenų pavyzdys | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Jei dar neleidote šio užduoties vedlio, [ER reikiamų konfigūracijų kūrimas norint importuoti duomenis iš išorinio failo](./tasks/er-required-configurations-import-data.md) dabartinėje „Finance and Operations“ programoje, atsisiųskite šį failą.

| Turinio aprašas    | Failas                                                            |
|------------------------|-----------------------------------------------------------------|
| ER modelio konfigūracija | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]