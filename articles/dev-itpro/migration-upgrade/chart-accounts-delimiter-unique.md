---
title: "Unikalios sąskaitų plano skyriklio vertės nustatymas"
description: "Programoje „Dynamics 365 for Finance and Operations“ sąskaitų plano ir dimensijų reikšmių skyrikliai negali būti tokie patys. Atnaujinę turite pakeisti skyriklio reikšmes."
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="3dc02-104">Unikalios sąskaitų plano skyriklio vertės nustatymas</span><span class="sxs-lookup"><span data-stu-id="3dc02-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3dc02-105">Programoje „Microsoft Dynamics AX 2012“ sąskaitų planui ir dimensijų vertėms galite naudoti tą patį skyriklį.</span><span class="sxs-lookup"><span data-stu-id="3dc02-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="3dc02-106">Programoje „Dynamics 365 for Finance and Operations“ sąskaitų plano ir dimensijų reikšmių skyrikliai negali būti tokie patys.</span><span class="sxs-lookup"><span data-stu-id="3dc02-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="3dc02-107">Jei yra pasikartojantis skyriklis, atnaujinę galite jį pakeisti.</span><span class="sxs-lookup"><span data-stu-id="3dc02-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="3dc02-108">Ši funkcija yra pasiekiama:</span><span class="sxs-lookup"><span data-stu-id="3dc02-108">This feature is available in:</span></span>
- <span data-ttu-id="3dc02-109">„Dynamics 365 for Finance and Operations‟ 8.0 versijoje</span><span class="sxs-lookup"><span data-stu-id="3dc02-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="3dc02-110">„Dynamics 365 for Finance and Operations“ 7.1 versijoje, KB 4094701, įvesti finansinių dimensijų negalite tada, kai dimensijų vertėse yra sąskaitų plano skyriklis</span><span class="sxs-lookup"><span data-stu-id="3dc02-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="3dc02-111">„Dynamics 365 for Finance and Operations“ 7.2 versijoje, KB 4092967, subprojekto kaip dimensijos negalite pasirinkti tada, kai subprojekto formate yra dimensijos skyriklis</span><span class="sxs-lookup"><span data-stu-id="3dc02-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="3dc02-112">Atnaujinkite skyriklį</span><span class="sxs-lookup"><span data-stu-id="3dc02-112">Update delimiter</span></span>
<span data-ttu-id="3dc02-113">Jei tarp sąskaitų plano, sąskaitų plano skyriklio ir projekto / subprojekto ID yra neatitikimas, formatą galima keisti.</span><span class="sxs-lookup"><span data-stu-id="3dc02-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="3dc02-114">Kitų dimensijos skyriklių keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="3dc02-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="3dc02-115">Sąskaitų plano skyriklį galite keisti atnaujinę „Finance and Operations“ versiją ir apsilankę parinktyje **DK parametrai** > **Sąskaitų planas ir dimensijos** > **Skyriklio keitimas**.</span><span class="sxs-lookup"><span data-stu-id="3dc02-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="3dc02-116">Jei vienintelis neatitikimas yra tarp projekto / subprojekto ID formato, tą reikšmę galite pakeisti parinktyje **Projektų valdymo ir apskaitos parametrai** > **Bendra** > **Subprojekto formato keitimas**.</span><span class="sxs-lookup"><span data-stu-id="3dc02-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="3dc02-117">Kaip nustatyti, ar jūsų aplinkoje reikia atnaujinti skyriklius</span><span class="sxs-lookup"><span data-stu-id="3dc02-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="3dc02-118">Jei skyrikliai atnaujintoje aplinkoje neatitinka, segmentuoto įrašo valdiklyje arba dimensijų įrašo valdiklyje įvedant reikšmes gali kilti nestabilumų.</span><span class="sxs-lookup"><span data-stu-id="3dc02-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="3dc02-119">Tai reiškia, kad įvesdami sąskaitos ir dimensijos kombinacijas visada turėsite naudoti peržvalgas arba iškeliamąjį meniu.</span><span class="sxs-lookup"><span data-stu-id="3dc02-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
