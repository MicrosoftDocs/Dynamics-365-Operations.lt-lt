---
title: "Integravimas su „Microsoft Dynamics 365 for Field Service“"
description: "Šioje temoje pateikiama integravimo su „Microsoft Dynamics 365 for Field Service“ apžvalga."
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: cb21667021a32381fd8038e1c9f0182b05622e3d
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integravimas su „Microsoft Dynamics 365 for Field Service“

[!include[banner](../includes/banner.md)]

„Microsoft Dynamics 365 for Finance and Operations“ leidžia sinchronizuoti verslo procesus tarp „Finance and Operations“ ir „Microsoft Dynamics 365 for Field Service“. Integravimo scenarijai sukonfigūruojami naudojant išplečiamuosius duomenų integratoriaus šablonus ir „Common Data Service“ (CDS), kad būtų galima sinchronizuoti verslo procesus.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/field-service-integration.png)](./media/field-service-integration.png)

Pirmasis integravimo tarp „Field Service“ ir „Finance and Operations“ etapas orientuotas į darbo užsakymų ir sutarčių įgalinimą „Field Service“, kad „Finance and Operations“ būtų galima išrašyti SF. Palaikomas srautas pradedamas „Field Service“, kai darbo užsakymų informacija su „Finance and Operations“ sinchronizuojama kaip pardavimo užsakymai. Programoje „Finance and Operations“ pardavimo užsakymams išrašomos SF, kad būtų sugeneruoti SF dokumentai. Be to, „Field Service“ pateikiama sutarčių SF informacija sinchronizuojama su „Finance and Operations“. „Microsoft Dynamics 365“ duomenų integratorius sinchronizuoja duomenis panaudodamas pritaikomus projektus. Standartiniai šablonai gali būti naudojami, siekiant sukurti pasirinktinius integravimo projektus, kuriuose papildomus standartinius ir pasirinktinius laukus bei objektus būtų galima susieti norint pakoreguoti integravimą ir atitikti specifinius reikalavimus.

Pirmame integravimo tarp „Field Service“ ir „Finance and Operations“ etape galima sinchronizuoti toliau nurodytus elementus elementus.

- [„Finance and Operations“ produktus su „Field Service“ produktais, kuriuose pateikiama produkto tipo informacija](field-service-product.md)
- [„Field Service“ darbo užsakymus su „Finance and Operations“ pardavimo užsakymais](field-service-work-order.md)
- [„Field Service“ SF su „Finance and Operations“ laisvos formos SF.](field-service-invoice.md)

Norėdami pamatyti pavyzdį, kaip galima sinchronizuoti darbo užsakymą tarp „Field Service“ ir „Finance and Operations“, peržiūrėkite trumpą „YouTube“ vaizdo įrašą [Kaip sinchronizuoti darbo užsakymą su „Microsoft Dynamics 365“ integravimu](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>„Finance and Operations“ sistemos reikalavimai
„Field Service“ integravimas palaikomas toliau nurodytose versijose.

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>„Dynamics 365 for Finance and Operations‟ 8.0 (2018 m. balandžio mėn.) ar naujesnėje versijoje

- „Dynamics 365 for Finance and Operations“ 8.0 (2018 m. balandžio mėn.) versija buvo išleista 2018 m. balandį. Programos versijos numeris – 8.0.30.8020 su 15 platformos naujinimu (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>„Field Service“ sistemos reikalavimai
Norėdami naudoti sprendimą „Field Service“, turite įdiegti toliau nurodytus komponentus.

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>„Microsoft Dynamics 365 for Field Service“ 9.0 arba naujesnę versiją

- „Dynamics 365 for Field Service“ 1612 versiją (9.0.1.733) (DB 9.0.1.733) internete arba naujesnę versiją.
- „Dynamics 365“ skirtą sprendimą „Potencialūs klientai ir grynieji pinigai“ (P2C), 1.15.0.1 arba naujesnė versija. Sprendimą galima atsisiųsti iš [„AppSource“](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- „Dynamics 365“ skirtas „Field Service“ integravimo sprendimas, 1.0.0.0 arba naujesnė versija. Sprendimą galima atsisiųsti iš [„AppSource“](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).

