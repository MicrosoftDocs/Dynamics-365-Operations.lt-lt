---
title: Apdoroti paskirstymus
description: Šiame straipsnyje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis „Microsoft“ „Dynamics 365 Finance“ ir kaip jie gali būti naudojami planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamam apskaitos objektui.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8216ebdd1f26601743e6b35849be0813d06b4a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446000"
---
# <a name="process-allocations"></a><span data-ttu-id="718db-105">Paskirstymų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="718db-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="718db-106">Šiame straipsnyje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis ir kaip jie gali būti naudojami planuojant biudžetą.</span><span class="sxs-lookup"><span data-stu-id="718db-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="718db-107">Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių.</span><span class="sxs-lookup"><span data-stu-id="718db-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="718db-108">Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamam apskaitos objektui.</span><span class="sxs-lookup"><span data-stu-id="718db-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="718db-109">Šis procesas palaiko toliau pateikiamas galimybes.</span><span class="sxs-lookup"><span data-stu-id="718db-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="718db-110">Rankiniu būdu paskirstykite operacijų sumas apskaitos paskirstymuose naudodami skaidymo veiksmą arba dokumentui pritaikydami finansinės dimensijos numatytuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="718db-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="718db-111">Daugiau informacijos žr. [Apskaitos paskirstymai](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="718db-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="718db-112">Automatiškai paskirstykite operacijų sumas pagal paskirstymo sąlygas, nurodytas atskiroje pagrindinėje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="718db-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="718db-113">Paskirstymo sąskaitos įrašai kiekvienam žurnalui bus generuojami pagal procentinę dalį ir paskirties DK sąskaitą, kai apskaitos įrašas atitiks kriterijus, apibrėžtus kaip pirminė DK sąskaita.</span><span class="sxs-lookup"><span data-stu-id="718db-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="718db-114">Dėl platesnės informacijos, žr. [Pagrindinės paskyros paskirstymo sąlygas](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="718db-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="718db-115">Automatiškai paskirstykite DK balansus arba fiksuotas sumas pagal DK paskirstymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="718db-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="718db-116">DK paskirstymo taisyklės apdorojamos periodiškai, naudojant paskirstymo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="718db-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="718db-117">Norėdami gauti daugiau informacijos, žr. [Paskirstymo taisykles](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="718db-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="718db-118">Biudžeto planavimo paskirstymai</span><span class="sxs-lookup"><span data-stu-id="718db-118">Allocations in budget planning</span></span>

<span data-ttu-id="718db-119">DK paskirstymo taisykles galima naudoti biudžeto planams.</span><span class="sxs-lookup"><span data-stu-id="718db-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="718db-120">Kai DK paskirstymo taisykles naudojate planuodami biudžetą, paskirstymo taisyklės veikia taip pat kaip veiktų DK, bet šaltinio duomenys ir paskirties duomenys gaunami iš biudžeto plano.</span><span class="sxs-lookup"><span data-stu-id="718db-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="718db-121">Galite neautomatiškai pasirinkti DK paskirstymo taisykles, naudotinas biudžeto planams.</span><span class="sxs-lookup"><span data-stu-id="718db-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="718db-122">Be to, galite naudoti paskirstymo grafiką, kuris veikia kaip darbo eigos proceso dalis.</span><span class="sxs-lookup"><span data-stu-id="718db-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="718db-123">Biudžetui planuoti negalima naudoti vidinės įmonės DK paskirstymo taisyklių.</span><span class="sxs-lookup"><span data-stu-id="718db-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>

