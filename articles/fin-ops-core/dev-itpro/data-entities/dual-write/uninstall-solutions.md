---
title: Šalinti dvigubo rašymo programos instrumentavimo sprendimus
description: Šioje temoje aprašoma, kaip pašalinti dvigubo rašymo programos instrumentavimo sprendimus.
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 781b2cb19a563d5712fa65718c93bfdc242f0c4a
ms.sourcegitcommit: abfaef124c8747827d6f297821f01f1f6fbca6b7
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/17/2022
ms.locfileid: "8455311"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>Šalinti dvigubo rašymo programos instrumentavimo sprendimus

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip pašalinti dvigubo rašymo programos instrumentavimo sprendimus.

Kai kurie klientai netyčia įdiegia dvigubo rašymo programos instrumentavimo paketą, kuris savo aplinkoje įdiegia kelis Microsoft Dataverse sprendimus. Diegiant papildomus paketo sprendimus gali kilti netikėtų ir pereičių problemų.

Norėdami išspręsti problemas, susijusias su dvigubo rašymo programos instrumentavimo paketo diegimu, pašalinkite nenorimus dvigubo rašymo sprendimus tokia tvarka:

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed (jei yra)
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed (Norėdami pašalinti šį sprendimą, turite atidaryti palaikymo bilietą su Microsoft.)
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

Jei buvo įdiegti šalies ir visuotinės adresų knygelės sprendimai, pašalinkite sprendimus tokia tvarka:

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. "Dynamics365FinanceExtended"
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. Šalis
1. Dynamics365Company_managed
1. Valiutų kursai
1. msdyn_AssetCommon
1. FieldServiceCommon
