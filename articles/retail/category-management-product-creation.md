---
title: Mažmeninės prekybos produktų kategorijų ir produktų valdymas
description: Šioje temoje aprašoma, kaip reklamavimo vadovai gali naudoti mažmeninės prekybos produktų kategorijas ryšiams tarp mažmeninės prekybos produktų hierarchijos ir išsamios informacijos apie išleistus produktus valdyti.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0bcc5989edd9913fce414c0c24068f111d8c1aeb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "344690"
---
# <a name="manage-retail-product-categories-and-products"></a>Mažmeninės prekybos produktų kategorijų ir produktų valdymas

[!include [banner](./includes/banner.md)]

Šioje temoje aprašomas patobulintas būdas valdyti mažmeninės prekybos produktų kategorijas ir produktus sprendime „Microsoft Dynamics 365 for Retail“. Dėl šių patobulinimų reklamavimo parduotuvėje vadovams leidžiama peržiūrėti produktų ypatybių struktūrą, bendrinamą tarp mažmeninės prekybos produktų hierarchijos ir išsamios informacijos apie išleistus produktus.

Norėdami sužinoti daugiau apie tai, kaip valdyti mažmeninės prekybos produktų kategorijas, darbo srityje **Kategorijų ir produktų valdymas** pasirinkite plytelę **Mažmeninės prekybos produktų hierarchija**.

Atkreipkite dėmesį, į patobulintą rodomo puslapio **Mažmeninės prekybos produktų hierarchija** struktūrą. Ankstesnėse „Retail“ versijose produktų ypatybės pagal jų taikomumą buvo suskirstytos į *pagrindines produktų ypatybes* ir *mažmeninės prekybos produktų ypatybes*. Mažmeninės prekybos produkto ypatybės pagal taikomumą yra *visuotinos*. Kitaip tariant, ta pati konkrečios „Retail“ produkto ypatybės reikšmė taikoma visiems juridiniams subjektams. Priešingu atveju, pagrindinės produktų ypatybės yra taikomos *konkrečiam juridiniam subjektui*. Kitaip tariant, juridinių subjektų naudojama konkrečios pagrindinės produktų ypatybės reikšmė gali skirtis priklausomai nuo atskirų kiekvieno juridinio subjekto verslo poreikių.

Patobulintoje mažmeninės prekybos produktų kategorijų struktūroje produktų ypatybės logiškai atskiriamos pagal jų taikomumą grupėje, kad būtų atspindėta išsamios išleisto produkto informacijos formos struktūra.

![Laukai, sugrupuoti pagal taikomumo ypatybes](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Galite valdyti visų juridinių subjektų arba konkretaus juridinio subjekto ypatybes, taikomas konkrečiam juridiniam subjektui.

Norėdami valdyti ypatybes visuose juridiniuose subjektuose, pasirinkite **Peržiūrėti visus juridinius subjektus** (arba **Redaguoti visus juridinius subjektus**).

![Peržiūrėti / redaguoti visus juridinius subjektus](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Norėdami valdyti konkretaus juridinio subjekto ypatybes, pasirinkite **Peržiūrėti konkretų juridinį subjektą** (arba **Redaguoti konkretų juridinį subjektą**).

![Peržiūrėti / redaguoti konkretų juridinį subjektą](media/ToggleToEditForAllLegalEntities.PNG)

Be to, patobulintoje mažmeninės prekybos produktų kategorijų struktūroje reklamavimo parduotuvėje vadovas dabar taip pat gali apibrėžti numatytąsias papildomo produktų ypatybių rinkinio reikšmes atskiros kategorijos lygiu. Tada, sukūrus produktų, šias numatytąsias produkto ypatybių reikšmes produktai paveldi pagal savo susiejimą su atskiros mažmeninės prekybos produktų hierarchijos kategorijos savybėmis. Šias paveldėtas kiekvieno produkto ypatybes taip pat galima modifikuoti, kad būtų įvykdyti atskiri verslo reikalavimai.

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a>Produktų naujinimo ypatybių mažmeninės prekybos produktų hierarchijos puslapyje pasirinkimas

Šią naują patobulintą produktų ypatybių struktūrą galite naudoti pasirinkdami atnaujintų produktų ypatybes, kurias reikia perkelti į susietus produktus. Puslapio **Mažmeninės prekybos produktų hierarchija** veiksmų srityje pasirinkite **Kategorija**, tada pasirinkite **Naujinti produktus**, kad atidarytumėte dialogo langą **Produktų naujinimas**.

![Produktų naujinimo dialogo langas](media/NewUpdateProductsEnhancedView.PNG)
