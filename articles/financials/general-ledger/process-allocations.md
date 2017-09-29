---
title: Apdoroti paskirstymus
description: "Šiame straipsnyje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ ir kaip jie gali būti naudojami planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamą apskaitos objektui."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 8859359f70132e9116e6a2d534a0f5f1d0bfeb80
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="process-allocations"></a><span data-ttu-id="4368e-105">Apdoroti paskirstymus</span><span class="sxs-lookup"><span data-stu-id="4368e-105">Process allocations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4368e-106">Šiame straipsnyje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ ir kaip jie gali būti naudojami planuojant biudžetą.</span><span class="sxs-lookup"><span data-stu-id="4368e-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and how they can be used in budget planning.</span></span> <span data-ttu-id="4368e-107">Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių.</span><span class="sxs-lookup"><span data-stu-id="4368e-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="4368e-108">Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamą apskaitos objektui.</span><span class="sxs-lookup"><span data-stu-id="4368e-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="4368e-109">„Microsoft Dynamics 365 for Finance and Operations“ pateikiamos tokios galimybės palaikyti šį procesą:</span><span class="sxs-lookup"><span data-stu-id="4368e-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="4368e-110">Rankiniu būdu paskirstykite operacijų sumas apskaitos paskirstymuose naudodami skaidymo veiksmą arba dokumentui pritaikydami finansinės dimensijos numatytuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="4368e-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="4368e-111">Daugiau informacijos rasite [Apskaitos paskirstymai.](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="4368e-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="4368e-112">Automatiškai paskirstykite operacijų sumas pagal paskirstymo sąlygas, nurodytas atskiroje pagrindinėje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="4368e-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="4368e-113">Paskirstymo sąskaitos įrašai kiekvienam žurnalui bus generuojami pagal procentinę dalį ir paskirties DK sąskaitą, kai apskaitos įrašas atitiks kriterijus, apibrėžtus kaip pirminė DK sąskaita.</span><span class="sxs-lookup"><span data-stu-id="4368e-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="4368e-114">Automatiškai paskirstykite DK balansus arba fiksuotas sumas pagal DK paskirstymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="4368e-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="4368e-115">DK paskirstymo taisyklės apdorojamos periodiškai, naudojant paskirstymo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="4368e-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="4368e-116">Biudžeto planavimo paskirstymai</span><span class="sxs-lookup"><span data-stu-id="4368e-116">Allocations in budget planning</span></span>

<span data-ttu-id="4368e-117">DK paskirstymo taisykles galima naudoti biudžeto planams.</span><span class="sxs-lookup"><span data-stu-id="4368e-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="4368e-118">Kai DK paskirstymo taisykles naudojate planuodami biudžetą, paskirstymo taisyklės veikia taip pat kaip veiktų DK, bet šaltinio duomenys ir paskirties duomenys gaunami iš biudžeto plano.</span><span class="sxs-lookup"><span data-stu-id="4368e-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="4368e-119">Galite neautomatiškai pasirinkti DK paskirstymo taisykles, naudotinas biudžeto planams.</span><span class="sxs-lookup"><span data-stu-id="4368e-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="4368e-120">Be to, galite naudoti paskirstymo grafiką, kuris veikia kaip darbo eigos proceso dalis.</span><span class="sxs-lookup"><span data-stu-id="4368e-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="4368e-121">Biudžetui planuoti negalima naudoti vidinės įmonės DK paskirstymo taisyklių.</span><span class="sxs-lookup"><span data-stu-id="4368e-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>





