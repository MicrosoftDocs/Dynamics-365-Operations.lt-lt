---
title: Prognozės modelio tobulinimas (peržiūros versija)
description: Šioje temoje aprašomos funkcijos, kurias galite naudoti norėdami pagerinti prognozavimo modelių efektyvumą.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2bcdea4a2a8f4386b274077cd1e95398fb6fac37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009374"
---
# <a name="improve-the-prediction-model-preview"></a>Prognozės modelio tobulinimas (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje aprašomos funkcijos, kurias galite naudoti norėdami pagerinti prognozavimo modelių efektyvumą. Paleidžiate savo modelį programos „Microsoft Dynamics 365 Finance“ darbo srityje **Klientų mokėjimo prognozės**. Tada tobulinimo veiksmai atliekami naudojant „AI Builder“.

## <a name="select-historical-outcomes"></a>Pasirinkite retrospektyvinius rezultatus

Pirmiausia turite pasirinkti vieną ar daugiau iš trijų galimų SF rezultatų: **Laiku**, **Vėlavimas** ir **Žymus vėlavimas**. Turi būti parenkami visi trys rezultatai. Jei išvalysite bet kurio iš rezultatų žymėjimą, SF bus išfiltruota iš mokymo proceso ir bus sumažintas prognozavimas.

[![Rezultatų patvirtinimas](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Jei jūsų organizacijai reikalingi tik du rezultatai, pakeiskite **Vėlavimas** ir **Žymus vėlavimas** ribines vertes į 0 (nulį) dienų. Tokiu būdu galite efektyviai sutraukti prognozavimą į dvejetainę būseną **Laiku** arba **Vėlavimas**.

## <a name="select-fields"></a>Pasirinkti laukus

Jums renkantis laukelius, kuriuo reikia įtraukti į modelį, įsitikinkite, kad sąraše yra visi prieinami laukeliai „Microsoft Dataverse“ lentelėje, kuri yra žemėlapyje duomenyse „Azure“ duomenų ežere. Kai kurie šių laukų **neturėtų** būti pasirenkami. Laukai, kurie neturėtų būti parenkami, patenka į vieną iš trijų kategorijų.

- Laukelis turi būti „Dataverse“ lentelei, tačiau nėra jokių atsarginės kopijos duomenų jam duomenų ežere.
- Šis laukas yra ID, todėl jo mašininio mokymo funkcija nesupranta.
- Lauke yra informacijos, kuri bus nepasiekiama prognozuojant.

Toliau esančiuose skyriuose pateikiami laukai, kurie galimi SF ir kliento objektams, ir nurodomi laukai, kurie **neturėtų** būti parenkami mokymui. Kiekvienam iš šių laukų nurodyta kategorija nurodo ankstesnio sąrašo kategorijas.
 
### <a name="invoice-dataverse-table"></a>Sąskaitos „Dataverse“ lentelė

Šiame paveiksle parodyti laukeliai, kurie yra prieinami sąskaitos lentelei.

[![Prieinami laukeliai sąskaitos lentelei](./media/available-fields.png)](./media/available-fields.png)

Šie laukai neturėtų būti parenkami mokymui.

- **SF sąskaita** (2 kategorija)
- **Uždaryta** (3 kategorija) – šis laukas naudojamas, norint filtruoti (uždarytas) ir prognozuoti (neuždarytas) SF.
- **Pavadinimas** (1 kategorija)
- **Šaltinio ID** (2 kategorija)
- **Šaltinio įrašas** (2 kategorija)
- **Šaltinio lentelė** (2 kategorija)

### <a name="customer-dataverse-table"></a>Kliento „Dataverse“ lentelė

Šiame paveiksle parodyti laukeliai, kurie yra prieinami kliento lentelei.

[![Prieinami laukeliai kliento lentelei](./media/related-entities.png)](./media/related-entities.png)

Šis laukas neturėtų būti parenkamas mokymui.

- **Eilučių unikalusis raktas** (2 kategorija)

## <a name="filters"></a>Filtrai

Šiuo metu filtrai nepalaiko kliento mokėjimo prognozavimo scenarijaus. Todėl pasirinkite **Praleisti šį veiksmą** ir pereikite prie suvestinės puslapio.

[![Fokusavimo režimas su filtrais](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

#### <a name="privacy-notice"></a>Privatumo pranešimas
Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.
