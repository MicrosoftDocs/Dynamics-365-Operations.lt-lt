---
title: Loginės kategorijos ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie logines funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916642"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Loginės kategorijos ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant logines modulio Elektroninės ataskaitos (ER) funkcijas, galima dirbti su loginėmis reikšmėmis, norint viename reiškinyje atlikti daugiau nei vieną palyginimą arba patikrinti kelias sąlygas. Šioje temoje pateikiama šių funkcijų suvestinė.

## <a name="list-of-supported-functions"></a>Palaikomų funkcijų sąrašas

| Funkcija | Aprašymas |
|----------|-------------|
| [Ir](er-functions-logical-and.md)                       | Jei visos nurodytos sąlygos yra teisingos, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**. |
| [Saugykla](er-functions-logical-case.md)                     | Ši funkcija nurodyto reiškinio reikšmę įvertina pagal nurodytas alternatyvias parinktis ir pateikia pirmosios parinkties, kuri yra lygi nurodyto reiškinio reikšmei, rezultatą. Kitu atveju ji pateikia pasirenkamą numatytąjį rezultatą, jei numatytasis rezultatas yra nurodytas kaip paskutinis iškviestos funkcijos argumentas, prieš kurį nėra parinkties. Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė. |
| [Jei](er-functions-logical-if.md)                         | Jei nurodyta sąlyga yra tenkinama, ši funkcija pateikia pirmą nurodytą reikšmę. Kitu atveju ji pateikia antrą nurodytą reikšmę. Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė. |
| [Ne](er-functions-logical-not.md)                       | Ši funkcija pateikia nurodytos sąlygos atvirkštinę loginę reikšmę kaip *Bulio logikos* reikšmę. |
| [Or](er-functions-logical-or.md)                         | Jei visos nurodytos sąlygos yra klaidingos, ši funkcija pateikia *Bulio logikos* reikšmę **FALSE**. Jei bet kuri nurodyta sąlyga yra teisinga, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**. |
| [ValueIn](er-functions-logical-valuein.md)               | Ši funkcija nustato, ar nurodyta įvestis atitinka bet kurią pateiktame sąraše nurodyto elemento reikšmę. Grąžinama *Bulio logikos* reikšmė **TEISINGA**, jei nurodyta įvestis sutampa su nurodytos išraiškos vykdymo rezultatu bent vienam nurodyto sąrašo įrašui. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)
