---
title: "Gaunamų dokumentų analizė „Microsoft Excel“"
description: "Šioje temoje pateikiama informacija apie elektroninių ataskaitų (ER) formatų kūrimą, norint analizuoti gaunamų „Microsoft Excel“ failų turinį."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 001e287590b9f43ed38de803bcace3a25a6f6637
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2018

---

# <a name="parse-incoming-microsoft-excel-files"></a>Gaunamų „Microsoft Excel“ failų analizė

[!include[banner](../includes/banner.md)]

Galite sukurti elektroninių ataskaitų (ER) formatus, skirtus analizuoti gaunamus „Microsoft Excel“ failus, kurie atitinka „Microsoft Excel“ darbaknygių duomenis (XLSX formato failus). Tada galite naudoti šių failų turinį programos duomenims atnaujinti. Tai naudinga, jei:

-   Sukurkite naują modelį ir formatą ir patikrinkite juos vykdymo metu. Tokiu atveju, „Excel“ imituoja faktinius programos duomenis.
-   Tvarkykite duomenis už savo programos ribų programoje „Excel“ ir importavę šiuos duomenis pateikite konkrečią ataskaitą.

Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlius **ER importavimo duomenys iš „Microsoft Excel“ failo (1 dalis: formato kūrimas)** ir **ER importavimo duomenys iš „Microsoft Excel“ failo (2 dalis: duomenų importavimas)** (verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) dalys). Šie užduočių vedliai parodys jums, kaip galima analizuoti gaunamą „Excel“ failą naudojant ER formatą, skirtą importuoti informaciją iš gaunamų dokumentų ir atnaujinti programos duomenis. Užduočių vedlių failus galite atsisiųsti iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684).

Atsisiųskite šiuos failus norėdami užbaigti aukščiau minėtus užduočių vedlius:

| Turinio aprašas                        | Failas                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| Gaunamas failas XLSX formatu – šablonas   | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)  |
| Gaunamas failas XLSX formatu – duomenų pavyzdys| [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Jei dar neleidote šio užduoties vedlio, [ER reikiamų konfigūracijų kūrimas norint importuoti duomenis iš išorinio failo](./tasks/er-required-configurations-import-data.md) dabartinėje programoje „Dynamics 365 for Finance and Operation“, atsisiųskite šį failą.

| Turinio aprašas                        | Failas                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| ER modelio konfigūracija                     | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266)            |


