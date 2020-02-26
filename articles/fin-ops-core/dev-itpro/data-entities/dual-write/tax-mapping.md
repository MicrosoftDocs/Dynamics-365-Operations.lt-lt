---
title: Integruoti mokesčiai
description: Šioje temoje aprašomas mokesčių duomenų integravimas tarp „Finance and Operations“ ir „Common Data Service“.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
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
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019916"
---
# <a name="integrated-tax"></a>Integruoti mokesčiai

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka. Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.

## <a name="templates"></a>Šablonai

Mokesčių duomenis sudaro objektų schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.

„Finance and Operations“   | Kitos „Dynamics 365” programos
-------------------------|---------------------------------
Mokesčių kodai                  | msdyn\_taxcodes.md
Mokesčių grupės               | msdyn\_taxgroups.md
Mokesčių prekių grupės          | msdyn\_taxitemgroups.md
Mokesčių lengvatos           | msdyn\_taxexemptcodes.md
Mokesčių institucijos          | msdyn\_taxauthorities.md
Išskaitomų mokesčių kodai      | msdyn\_withholdingtaxcodes.md
Išskaitomo mokesčio grupės   | msdyn\_withholdingtaxgroups.md
Mokesčių DK sąskaitų grupė | msdyn\_taxpostinggroups  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

