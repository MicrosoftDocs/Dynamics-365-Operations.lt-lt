---
title: Produktų kategorijų ir produktų valdymas
description: Šiame straipsnyje aprašoma, kaip prekybos vadovai gali naudoti produktų kategorijas, kad galėtų valdyti ryšius tarp "Commerce" produktų hierarchijos ir išleisto produkto informacijos.
author: ashishmsft
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0871475e0910e0a46544c56083b505ff647fd6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878588"
---
# <a name="manage-product-categories-and-products"></a>Produktų kategorijų ir produktų valdymas

[!include [banner](./includes/banner.md)]

Šiame straipsnyje aprašomas patobulintas produktų kategorijų ir produktų valdymo būdas Dynamics 365 Commerce. Dėl šių patobulinimų reklamavimo parduotuvėje vadovams leidžiama peržiūrėti produktų ypatybių struktūrą, bendrinamą tarp produktų hierarchijos ir išsamios informacijos apie išleistus produktus.

Norėdami sužinoti daugiau apie tai, kaip valdyti produktų kategorijas, darbo srityje **Kategorijų ir produktų valdymas** pasirinkite plytelę **Prekybos produktų hierarchija**.

Atkreipkite dėmesį į patobulintą rodomo puslapio **Prekybos produktų hierarchija** struktūrą. Ankstesnėse programos versijose produktų ypatybės pagal jų taikomumą buvo suskirstytos į *pagrindines produktų ypatybes* ir *Mažmeninės prekybos produktų ypatybes*. Mažmeninės prekybos produkto ypatybės pagal taikomumą yra *visuotinos*. Kitaip tariant, ta pati konkrečios produkto ypatybės reikšmė taikoma visiems juridiniams subjektams. Priešingu atveju, pagrindinės produktų ypatybės yra taikomos *konkrečiam juridiniam subjektui*. Kitaip tariant, juridinių subjektų naudojama konkrečios pagrindinės produktų ypatybės reikšmė gali skirtis priklausomai nuo atskirų kiekvieno juridinio subjekto verslo poreikių.

Patobulintoje produktų kategorijų struktūroje produktų ypatybės logiškai atskiriamos pagal jų taikomumą grupėje, kad būtų atspindėta išsamios išleisto produkto informacijos formos struktūra.

![Laukai, sugrupuoti pagal taikomumo ypatybes.](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

Galite valdyti visų juridinių subjektų arba konkretaus juridinio subjekto ypatybes, taikomas konkrečiam juridiniam subjektui.

Norėdami valdyti ypatybes visuose juridiniuose subjektuose, pasirinkite **Peržiūrėti visus juridinius subjektus** (arba **Redaguoti visus juridinius subjektus**).

![Peržiūrėti / redaguoti visus juridinius subjektus.](media/ToggleBackToEditForSpecificLegalEntity.PNG)

Norėdami valdyti konkretaus juridinio subjekto ypatybes, pasirinkite **Peržiūrėti konkretų juridinį subjektą** (arba **Redaguoti konkretų juridinį subjektą**).

![Peržiūrėti / redaguoti konkretų juridinį subjektą.](media/ToggleToEditForAllLegalEntities.PNG)

Be to, patobulintoje produktų kategorijų struktūroje reklamavimo parduotuvėje vadovas dabar taip pat gali apibrėžti numatytąsias papildomo produktų ypatybių rinkinio reikšmes atskiros kategorijos lygiu. Tada, sukūrus produktų, šias numatytąsias produkto ypatybių reikšmes produktai paveldi pagal savo susiejimą su atskiros produktų hierarchijos kategorijos savybėmis. Šias paveldėtas kiekvieno produkto ypatybes taip pat galima modifikuoti, kad būtų įvykdyti atskiri verslo reikalavimai.

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>Produktų naujinimo ypatybių prekybos produktų hierarchijos puslapyje pasirinkimas

Šią naują patobulintą produktų ypatybių struktūrą galite naudoti pasirinkdami atnaujintų produktų ypatybes, kurias reikia perkelti į susietus produktus. Puslapio **Prekybos produktų hierarchija** veiksmų srityje pasirinkite **Kategorija**, tada pasirinkite **Naujinti produktus**, kad atidarytumėte dialogo langą **Produktų naujinimas**.

![Produktų naujinimo dialogo langas.](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]