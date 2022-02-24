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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646084"
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

Pasirinkus laukus, kuriuos reikia įtraukti į modelį, reikia žinoti, kad sąraše yra visi galimi „Common Data Service“ objekto laukai, kurie susieti su duomenimis, kurie yra „Azure“ duomenų telkinyje. Kai kurie šių laukų **neturėtų** būti pasirenkami. Laukai, kurie neturėtų būti parenkami, patenka į vieną iš trijų kategorijų.

- Laukas reikalingas „Common Data Service“ objektui, tačiau duomenų telkinyje nėra atsarginių duomenų.
- Šis laukas yra ID, todėl jo mašininio mokymo funkcija nesupranta.
- Lauke yra informacijos, kuri bus nepasiekiama prognozuojant.

Toliau esančiuose skyriuose pateikiami laukai, kurie galimi SF ir kliento objektams, ir nurodomi laukai, kurie **neturėtų** būti parenkami mokymui. Kiekvienam iš šių laukų nurodyta kategorija nurodo ankstesnio sąrašo kategorijas.
 
### <a name="invoice-common-data-model-entity"></a>SF „Common Data Model“ objektas

Tolesnėje iliustracijoje parodyti SF objekto laukai.

[![Galimi SF objekto laukai](./media/available-fields.png)](./media/available-fields.png)

Šie laukai neturėtų būti parenkami mokymui.

- **SF sąskaita** (2 kategorija)
- **Uždaryta** (3 kategorija) – šis laukas naudojamas, norint filtruoti (uždarytas) ir prognozuoti (neuždarytas) SF.
- **Pavadinimas** (1 kategorija)
- **Šaltinio ID** (2 kategorija)
- **Šaltinio įrašas** (2 kategorija)
- **Šaltinio lentelė** (2 kategorija)

### <a name="customer-common-data-model-entity"></a>Kliento „Common Data Model“ objektas

Tolesnėje iliustracijoje parodyti kliento objekto laukai.

[![Galimi kliento objekto laukai](./media/related-entities.png)](./media/related-entities.png)

Šis laukas neturėtų būti parenkamas mokymui.

- **Eilučių unikalusis raktas** (2 kategorija)

## <a name="filters"></a>Filtrai

Šiuo metu filtrai nepalaiko kliento mokėjimo prognozavimo scenarijaus. Todėl pasirinkite **Praleisti šį veiksmą** ir pereikite prie suvestinės puslapio.

[![Fokusavimo režimas su filtrais](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

#### <a name="privacy-notice"></a>Privatumo pranešimas
Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.
