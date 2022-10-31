---
title: Sąskaitos struktūros aktyvinimo našumo tobulinimas
description: Šiame straipsnyje paaiškinamas naujas sąskaitos struktūros aktyvinimo proceso našumo patobulinimas.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2022
ms.locfileid: "9714006"
---
# <a name="account-structure-activation-performance-enhancement"></a>Sąskaitos struktūros aktyvinimo našumo tobulinimas

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šis našumo patobulinimas leidžia jums suaktyvinti sąskaitos struktūras greičiau paleidžiant kelis operacijos naujinimus vienu metu. Be to, struktūra yra pažymima kaip aktyvi ją patikrinus ir operacijos apdorojimas gali būti tęsiamas, kol neužregistruotos operacijos yra atnaujinamos į naują struktūrą. Kadangi operacijos atnaujinimai gali šiek tiek užtrukti, galite stebėti aktyvinimo būseną pasirinkdami **Peržiūrėti aktyvinimo būseną** virš tinklelio puslapyje **Sąskaitos struktūros**. Taip pat galite peržiūrėti aktyvinimo būseną pasirinkdami **Peržiūrėti** veiksmų srityje ir tada pasirinkdami **Aktyvinimo būsena** išskleidžiamajame meniu.

[![Sąskaitos struktūrų puslapis.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Pasirinkus **Peržiūrėti aktyvinimo būseną**, rodomas dialogo langas, kuriame pateikiamos atskiros užduotys, vykdomos kaip aktyvinimo proceso dalis. Galite peržiūrėti kiekvienos užduoties būseną ir, pasibaigus užduočiai, pabaigos datą ir laiką.

[![Sąskaitos struktūros aktyvinimo laiko juosta.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Sąskaitos struktūros aktyvinimo patarimai

Sąskaitos struktūros dialogo langas rodomas, kai pasirenkate **Suaktyvinti** juodraštinei sąskaitos struktūrai, kurioje yra skirtuko skyrius pavadinimu **Atnaujinti neužregistruotas operacijas**. Šiame skyriuje yra parinktis pavadinimu **Priverstinis atnaujinimas**. Galite pasirinkti šią parinktį, kad būtų atnaujintos visos neužregistruotos operacijos į esamą struktūrą. Tačiau šią parinktį turėtumėte naudoti tik įvykus klaidai arba „Microsoft“ pagalbos tarnybą nurodė ją naudoti.

Yra veiksnių, kurie gali turėti įtakos aktyvinimo proceso našumui:

- Didelis neužregistruotų žurnalo įrašų skaičius
- Didelis atvirojo šaltinio dokumentų, pvz., laisvos formos sąskaitų faktūrų, tiekėjo sąskaitų faktūrų ir susijusių dokumentų, naudojančių šaltinio dokumentų sistemą ir turinčių atidarytų apskaitos paskirstymų, skaičius
- TaxUncommitted duomenų kiekis
- Atviro biudžeto duomenų kiekis
- Žurnalo duomenų importavimas, kol vis dar vykdomos aktyvinimo užduotys

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
