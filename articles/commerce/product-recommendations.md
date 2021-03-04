---
title: Produktų rekomendacijų apžvalga
description: Šioje temoje pateikta bendra informacija apie produkto rekomendacijas. Produktų rekomendacijos leidžia vartotojams lengvai ir greitai rasti norimus produktus ir netgi produktų, kurių jie neketina pirkti.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 5aa7db8e53906f9e1416b912fe2c3b70d5430258
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414220"
---
# <a name="product-recommendations-overview"></a>Produktų rekomendacijų apžvalga

[!include [banner](includes/banner.md)]

„Microsoft Dynamics 365 Commerce“ gali būti naudojama rodyti produkto rekomendacijas „e-Commerce“ svetainėje ir elektroninio kasos aparato (EKA) įrenginyje. Produkto rekomendacijos – tai prekės, kurios gali sudominti klientą. Rekomendacijos yra paremtos kitų klientų pirkimo tendencijomis internetinėse ir fizinėse parduotuvėse.

Pasitelkdami produktų rekomendacijomis vartotojai gali lengvai ir greitai rasti norimų produktų, tad ši funkcija jiems labai naudinga. Kryžminis pardavimas ir papildomas pardavimas gali būti naudojami netgi siekiant padėti klientams surasti papildomų produktų, kurių iš pradžių jie net neketino pirkti. Kai rekomendacijos yra naudojamos siekiant pagerinti produkto atradimą, atsiranda daugiau konversijos padidinimo galimybių, išauga pardavimo įplaukos, netgi pagerėja klientų pasitenkinimas ir tokiu būdu jie išsaugomi.

„e-Commerce“ produktų rekomendacijoms plačiai naudojama „Microsoft“ rekomendacijų mašininio mokymo technologijų platforma.

## <a name="recommendation-service"></a>Rekomendacijų paslauga

Produkto rekomendacijų paslauga naudoja dirbtinio intelekto ir mašininio mokymosi (AI-ML) technologijas toliau nurodytais būdais.

- Rekomendavimo paslaugai reikiamu formatu pateikti duomenys ištraukiami iš „Commerce“ operacinės duomenų bazės ir siunčiami į Azure Data Lake Storage arba objekto parduotuvę.
- Rekomendacijų paslaugai naudojami išsaugoti duomenys, skirti mokyti rekomendavimo modelius sąrašams **Žmonėms taip pat patiko**, **Dažnai kartu perkama**, **Nauja**, **Perkamiausi** ir **Populiaru**.

## <a name="scenarios"></a>Scenarijai

Produktų rekomendacijos pasiekiamos toliau nurodytais scenarijais:

- **Bet kuriame parduotuvės naršymo puslapyje ar nukreipimo puslapyje el. prekyboje:** Jei klientai arba parduotuvės partneriai lankosi parduotuvės puslapyje, rekomendacijų mechanizmas gali siūlyti produktus iš sąrašų **Nauja**, **Perkamiausi** ir **Populiaru**.
- **Produkto išsamios informacijos puslapyje:** Jei klientai ar parduotuvės partneriai apsilanko puslapyje **Produkto išsami informacija**, rekomendacijos mechanizmas pasiūlys papildomas prekes, kurios taip pat gali būti perkamos. Šie elementai rodomi sąraše **Žmonėms taip pat patiko**.
- **Operacijų puslapyje arba pirkimo užbaigimo puslapyje:** rekomendacijų mechanizmas siūlo prekių pagal visų prekių krepšelyje sąrašą. Šios prekės rodomos sąraše **Dažnai kartu perkama**.
- **Pagal asmeninius poreikius pritaikytos rekomendacijos:** prekybininkai gali pateikti prisijungusiems klientams asmeninius sąrašus **Parinkta jums**, be naujų funkcijų, leidžiančių esamus sąrašo scenarijus pritaikyti pagal asmeninius poreikius ir atsižvelgiant į konkretų klientą. Norėdami sužinoti daugiau, žr. [Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md).

### <a name="types-of-product-recommendations"></a>Produktų rekomendacijų tipai

Šioje lentelėje aprašytos įvairių tipų automatizuotos produktų rekomendacijos, kurias mažmenininkai gali naudoti „Dynamics 365 Commerce“ per [produktų rinkinio modulį](product-collection-module-overview.md). Mažmenininkai taip pat gali šiame sąraše prisiregistravusiam vartotojui pateikti personalizuotus rezultatus, jei svetainės autorius nustato atitinkamą parinktį.

| Produktų atsiėmimo modulis  | Tipas | aprašymas |
|----------------------------|------|-------------|
| Naujos                        | Algoritminis | Šiame modulyje rodomas naujausių produktų, kurie buvo neseniai atrinkti į kanalus ir katalogus, sąrašas. |
| Perkamiausia               | Algoritminis | Šiame modulyje rodomas produktų, kurie išdėstyti pagal didžiausią pardavimo skaičių, sąrašas. |
| Populiaru                   | Algoritminis | Šis modulis pateikia tam tikro laikotarpio labiausiai parduodamų produktų sąrašą pagal didžiausią pardavimų skaičių.  |
| Dažnai perkama kartu | AI-ML | Šiame modulyje rekomenduojami produktai, kurie dažniausiai perkami kartu su dabartinio vartotojo krepšelio turiniu. |
| Žmonėms taip pat patinka           | AI-ML | Šiame modulyje rekomenduojami tam tikro pradinio gaminio produktai, atsižvelgiant į vartotojų pirkimo tendencijas. |
| Parinkta jums              | AI-ML | Šiame modulyje rekomenduojamas asmeniniams poreikiams pritaikytų produktų sąrašas, atsižvelgiant į prisiregistravusio vartotojo pirkimo tendencijas. Vartotojui svečiui bus rodomas sutrauktas sąrašas. |

## <a name="additional-resources"></a>Papildomi ištekliai

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]