---
title: Beveik realiuoju laiku vykstantis duomenų integravimas su „Common Data Service”
description: Šioje temoje pateikiama integravimo tarp „Finance and Operations“ ir „Common Data Service“ apžvalga.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019922"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Beveik realiuoju laiku vykstantis duomenų integravimas su „Common Data Service”

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Šiame skaitmeniniame pasaulyje verslo ekosistemos naudoja „Microsoft Dynamics 365“ programas kaip visumą. Kadangi žmonių, klientų, operacijų ir daiktų interneto („IoT“) įrenginiai patenka į vieną šaltinį, galimos skaitmeninės grįžtamojo ryšio spragos. Norint pasiekti šią patirtį, būtinas integravimas tarp „Finance and Operations“ programų ir kitų „Dynamics 365“ programų. Kai kurios programos sukurtos remiantis „Common Data Service“. Integravus „Finance and Operations“ programų duomenis į „Common Data Service“, kitos programos nuosekliai ir sklandžiai palaiko ryšį su „Finance and Operations“.

„Finance and Operations“ programos ir „Common Data Service“ užtikrina duomenų sinchronizavimą tarp „Finance and Operations“ programų ir kitų „Dynamics 365” programų beveik realiuoju laiku per dvigubo rašymo sistemą. Padengimas yra platus ir apima 28 programos paviršiaus sritis. Tikslas yra suteikti „One Dynamics 365“ vartotojo patirtį per sklandžius duomenų srautus, kurie jungia verslo procesus visose programose.

![Struktūros apžvalgos diagrama](media/dual-write-overview.jpg)

Galimi tolesni vertės pasiūlymai.

+ [Organizacijos hierarchija Common Data Service](organization-mapping.md)
+ [Įmonės sąvoka programoje „Common Data Service“](company-data.md)
+ [Integruotas kliento šablonas](customer-mapping.md)
+ [Integruota didžioji knyga](ledger-mapping.md)
+ [Bendrosios produkto funkcijos](product-mapping.md)
+ [Integruotas tiekėjo šablonas](vendor-mapping.md)
+ [Integruotos svetainės ir sandėliai](sites-warehouses-mapping.md)
+ [Bendrieji integruotų mokesčių duomenys](tax-mapping.md)

## <a name="system-requirements"></a>Sistemos reikalavimai

Sinchroninis, dvikryptis, beveik realiojo laiko duomenų srautams reikia šių versijų:

+ Microsoft Dynamics 365 for Finance and Operations 10.0.4 versija (2019 m. liepos mėn.) su 28 arba naujesniu platformos versija
+ Microsoft Dynamics 365 for Customer Engagement, 9.1 (4.2) arba naujesnė versija

## <a name="setup-instructions"></a>Sąrankos instrukcijos

Norėdami nustatyti „Finance and Operations“ programų ir „Common Data Service“ integravimą, atlikite tolesnius veiksmus.
    
1. Informacijos apie dvigubo rašymo sistemos diegimą ieškokite [išsamiame vadove](https://aka.ms/dualwrite-docs) temoje „Dbigubo rašymo peržiūros paskelbimas“.
2. Sprendimą atsisiųskite ir įdiekite iš „Yammer“ grupės [„Fin Ops and CDS/CE Integration via Dual-Write“](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096). Pakete yra penki sprendimai:

    + Dynamics365Company
    + Valiutų kursai
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Sekite vykdymo tvarką, skirtą [pradinių nuorodos duomenų sinchronizavimui](initial-sync.md).
4. Jei susiduriate su dvigubo rašymo sinchronizavimo problemomis, žr. [„Duomenų integravimo tirikčių šalinimo vadovas](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Jūs negalite vienu metu paleisti funkcijos [Potencialus klientas į grynuosius pinigus](../../../../supply-chain/sales-marketing/prospect-to-cash.md) ir dvigubo rašymo. Jei naudojate potencialaus kliento į grynuosius pinigus sprendimą, turite jį pašalinti. Taip pat turite išjungti kliento ir tiekėjo dvigubo rašymo šablonus, kurie yra potencialaus kliento į grynuosius pinigus sprendimo dalis.
