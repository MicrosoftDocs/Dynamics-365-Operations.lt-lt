---
title: Beveik realiojo laiko integravimas tarp „Finance and Operations“ ir „Common Data Service“
description: Šioje temoje apžvelgiamas integravimas tarp „Finance and Operations“ programų ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b7d9e6be6fb2fef85bcf1182f89b8e370abea3d6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184490"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Beveik realiuoju laiku vykstantis duomenų integravimas su „Common Data Service”

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Šiame skaitmeniniame pasaulyje verslo ekosistemos naudoja „Microsoft Dynamics 365“ programas kaip visumą. Kadangi žmonių, klientų, operacijų ir daiktų interneto („IoT“) įrenginiai patenka į vieną šaltinį, galimos skaitmeninės grįžtamojo ryšio spragos. Norint pasiekti šią patirtį, būtinas integravimas tarp „Finance and Operations“ ir „Dynamics 365“ programų. Kai kurios programos sukurtos remiantis „Common Data Service“. „Finance and Operations“ programų duomenų integravimas su „Common Data Service“ leidžia kitoms programoms nuosekliai ir sklandžiai sąveikauti su „Finance and Operations“.

„Finance and Operations“ programos ir „Common Data Service“ pateikia beveik realaus laiko duomenų sinchronizavimą tarp „Finance and Operations“ programų ir kitų „Dynamics 365” programų per dvigubo rašymo sistemą. Padengimas yra platus ir apima 28 programos paviršiaus sritis. Tikslas yra suteikti „One Dynamics 365“ vartotojo patirtį per sklandžius duomenų srautus, kurie jungia verslo procesus visose programose.

![Struktūros apžvalgos diagrama](media/dual-write-overview.jpg)

Klientams prieinami šie vertės pasiūlymas:

+ [Organizacijos hierarchija Common Data Service](dual-write-organization.md)
+ [Įmonės sąvoka programoje „Common Data Service“](dual-write-company.md)
+ [Integruotas kliento šablonas](dual-write-customer.md)
+ [Integruotas tiekėjo šablonas](dual-write-vendor.md)
+ Vieningo produkto šablonas

## <a name="system-requirements"></a>Sistemos reikalavimai

Sinchroninis, dvikryptis, beveik realiojo laiko duomenų srautams reikia šių versijų:

+ Microsoft Dynamics 365 for Finance and Operations 10.0.4 versija (2019 m. liepos mėn.) su 28 arba naujesniu platformos versija
+ Microsoft Dynamics 365 for Customer Engagement, 9.1 (4.2) arba naujesnė versija

## <a name="setup-instructions"></a>Sąrankos instrukcijos

Atlikite šiuos veiksmus, kad nustatytumėte „Finance and Operations“ programų ir „Common Data Service“ integravimą.
    
1. Informacijos apie dvigubo rašymo sistemos diegimą ieškokite [išsamiame vadove](https://aka.ms/dualwrite-docs) temoje „Dbigubo rašymo peržiūros paskelbimas“.
2. Atsisiųsti ir įdiegti sprendimą iš [Finance and Operations, Common Data Service ir „Customer Engagement“ integravimo](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer grupės. Pakete yra penki sprendimai:

    + Dynamics365Company
    + Valiutų kursai
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Sekite vykdymo tvarką, skirtą [pradinių nuorodos duomenų sinchronizavimui](dual-write-initial.md).
4. Jei susiduriate su dvigubo rašymo sinchronizavimo problemomis, žr. [„Duomenų integravimo tirikčių šalinimo vadovas](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Jūs negalite vienu metu paleisti funkcijos [Potencialus klientas į grynuosius pinigus](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) ir dvigubo rašymo. Jei naudojate potencialaus kliento į grynuosius pinigus sprendimą, turite jį pašalinti. Taip pat turite išjungti kliento ir tiekėjo dvigubo rašymo šablonus, kurie yra potencialaus kliento į grynuosius pinigus sprendimo dalis.
