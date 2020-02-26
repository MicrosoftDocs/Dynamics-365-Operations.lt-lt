---
title: Produktų rekomendacijų apžvalga
description: Šioje temoje pateikta bendra informacija apie produkto rekomendacijas. Produktų rekomendacijos leidžia vartotojams lengvai ir greitai rasti norimus produktus ir netgi produktų, kurių jie neketina pirkti.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024984"
---
# <a name="product-recommendations-overview"></a>Produktų rekomendacijų apžvalga

[!include [banner](includes/banner.md)]

„Microsoft Dynamics 365 Commerce“ gali būti naudojama rodyti produkto rekomendacijas „e-Commerce“ svetainėje ir elektroninio kasos aparato (EKA) įrenginyje. Produkto rekomendacijos – tai prekės, kurios gali sudominti klientą. Rekomendacijos yra paremtos kitų klientų pirkimo tendencijomis internetinėse ir fizinėse parduotuvėse.

Pasitelkdami produktų rekomendacijas vartotojai gali lengvai ir greitai rasti norimų produktų, tad ši funkcija jiems labai naudinga. Kryžminis pardavimas ir papildomas pardavimas netgi gali būti naudojami siekiant padėti klientams surasti papildomų produktų, kurių iš pradžių jie net neketino pirkti. Naudojant rekomendacijas padėti aptikti produktų, jomis galima sukurti daugiau konvertavimo galimybių, padėti padidinti įplaukas ir netgi padėti padidinti klientų pasitenkinimą bei išsaugojimą.

„Commerce“ produktų rekomendacijoms plačiai naudojama „Microsoft“ rekomendacijų mašininio mokymo technologijų platforma.


## <a name="scenarios"></a>Scenarijai

Produktų rekomendacijos pasiekiamos toliau nurodytais scenarijais:

- **Bet kuriame parduotuvės naršymo puslapyje ar nukreipimo puslapyje el. prekyboje:** Jei klientai arba parduotuvės partneriai lankosi parduotuvės puslapyje, rekomendacijų mechanizmas gali siūlyti produktus iš sąrašų **Nauja**, **Perkamiausi** ir **Populiaru**.
- **Produkto išsamios informacijos puslapyje:** Jei klientai ar parduotuvės partneriai apsilanko puslapyje **Produkto išsami informacija**, rekomendacijos mechanizmas pasiūlys papildomas prekes, kurios taip pat gali būti perkamos. Šie elementai rodomi sąraše **Žmonėms taip pat patiko**.
- **Operacijų puslapyje arba pirkimo užbaigimo puslapyje:** rekomendacijų mechanizmas siūlo prekių pagal visų prekių krepšelyje sąrašą. Šios prekės rodomos sąraše **Dažnai kartu perkama**.
- **Pagal asmeninius poreikius pritaikytos rekomendacijos:** prekybininkai gali pateikti prisijungusiems klientams asmeninius sąrašus **Parinkta jums**, be naujų funkcijų, leidžiančių esamus sąrašo scenarijus pritaikyti pagal asmeninius poreikius ir atsižvelgiant į konkretų klientą. Norėdami sužinoti daugiau, žr. funkcijos dokumentaciją:\[įgalinti pagal asmeninius poreikius pritaikytas rekomendacijas.](personalized-recommendations.md)

## <a name="recommendation-service"></a>Rekomendacijų paslauga

Produktų rekomendacijoms naudojamos rekomendacijų mašininio mokymo technologijos šiais būdais:

- Rekomendavimo paslaugai reikiamu formatu pateikti duomenys ištraukiami iš „Commerce“ operacinės duomenų bazės ir siunčiami į objekto parduotuvę.
- Rekomendavimo paslaugai naudojami duomenys, skirti mokyti rekomendavimo modelius sąrašams **Žmonėms taip pat patiko**, **Dažnai kartu perkama**, **Nauja**, **Perkamiausi** ir **Populiaru**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Įgalinti asmeniniams poreikiams pritaikytas rekomendacijas](personalized-recommendations.md)

[Produktų rinkinio modulio peržiūra](product-collection-module-overview.md)

[Kurti kuruojamus produktų rekomendacijų sąrašus](create-editorial-recommendation-lists.md)

[Tvarkyti AI-ML pagrįstų produktų rekomendacijų rezultatus](modify-product-recommendation-results.md)

[ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius](add-reco-list-to-page.md)
