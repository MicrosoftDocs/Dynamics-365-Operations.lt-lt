---
title: Prognozės modelio tobulinimas
description: Šioje temoje aprašomos funkcijos, kurias galite naudoti norėdami pagerinti prognozavimo modelių efektyvumą.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 804c18c1b165fff99390db1fda22da0137249373
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595042"
---
# <a name="improve-the-prediction-model"></a>Prognozės modelio tobulinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos funkcijos, kurias galite naudoti norėdami pagerinti prognozavimo modelių efektyvumą. Paleidžiate savo modelį programos „Microsoft Dynamics 365 Finance“ darbo srityje **Klientų mokėjimo prognozės**. Tada tobulinimo veiksmai atliekami naudojant „AI Builder“.

## <a name="select-historical-outcomes"></a>Pasirinkite retrospektyvinius rezultatus

Pirmiausia turite pasirinkti vieną ar daugiau iš trijų galimų SF rezultatų: **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**. Turi būti parenkami visi trys rezultatai. Jei išvalysite bet kurio iš rezultatų žymėjimą, SF bus išfiltruota iš mokymo proceso ir bus sumažintas prognozavimas.

[![Rezultatų patvirtinimas.](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Jei jūsų organizacijai reikalingi tik du rezultatai, pakeiskite **Vėlavimas** ir **Žymus vėlavimas** ribines vertes į 0 (nulį) dienų. Tokiu būdu galite efektyviai sutraukti prognozavimą į dvejetainę būseną **Laiku** arba **Vėlavimas**.

## <a name="select-fields"></a>Pasirinkti laukus

Jums renkantis laukelius, kuriuo reikia įtraukti į modelį, įsitikinkite, kad sąraše yra visi prieinami laukeliai „Microsoft Dataverse“ lentelėje, kuri yra žemėlapyje duomenyse „Azure“ duomenų ežere. Kai kurie šių laukų **neturėtų** būti pasirenkami. Laukai, kurie neturėtų būti parenkami, patenka į vieną iš trijų kategorijų.

- Laukelis turi būti „Dataverse“ lentelei, tačiau nėra jokių atsarginės kopijos duomenų jam duomenų ežere.
- Šis laukas yra ID, todėl jo mašininio mokymo funkcija nesupranta.
- Lauke yra informacijos, kuri bus nepasiekiama prognozuojant.

Toliau esančiuose skyriuose pateikiami laukai, kurie galimi SF ir kliento objektams, ir nurodomi laukai, kurie **neturėtų** būti parenkami mokymui. Kiekvienam iš šių laukų nurodyta kategorija nurodo ankstesnio sąrašo kategorijas.
 
### <a name="invoice-dataverse-table"></a>Sąskaitos „Dataverse“ lentelė

Šiame paveiksle parodyti laukeliai, kurie yra prieinami sąskaitos lentelei.

[![Prieinami laukeliai sąskaitos lentelei.](./media/available-fields.png)](./media/available-fields.png)

Šie laukai neturėtų būti parenkami mokymui.

- **SF sąskaita** (2 kategorija)
- **Uždaryta** (3 kategorija) – šis laukas naudojamas, norint filtruoti (uždarytas) ir prognozuoti (neuždarytas) SF.
- **Pavadinimas** (1 kategorija)
- **Šaltinio ID** (2 kategorija)
- **Šaltinio įrašas** (2 kategorija)
- **Šaltinio lentelė** (2 kategorija)

### <a name="customer-dataverse-table"></a>Kliento „Dataverse“ lentelė

Šiame paveiksle parodyti laukeliai, kurie yra prieinami kliento lentelei.

[![Prieinami laukeliai kliento lentelei.](./media/related-entities.png)](./media/related-entities.png)

Šis laukas neturėtų būti parenkamas mokymui.

- **Eilučių unikalusis raktas** (2 kategorija)

## <a name="filters"></a>Filtrai

Galite filtruoti sąskaitas faktūras, naudojamas mokymo metu, nustatydami SF arba klientų lentelių laukų filtro kriterijus. Pavyzdžiui, galite nustatyti ribinę vertę, kad būtų įtrauktos tik tos sąskaitos faktūros, kurių suma atitinka arba viršija konkrečią sumą. Taip pat galite neįtraukti sąskaitų faktūrų, kurios susietos su konkrečios klientų grupės klientais.

Daugiau informacijos apie duomenų filtravimą ieškokite [Prognozės modelio kūrimas](/ai-builder/prediction-create-model#filter-your-data).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
