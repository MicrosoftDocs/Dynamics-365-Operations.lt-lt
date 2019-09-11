---
title: Didžiosios knygos paskirstymo žurnalo apdorojimas
description: Šioje temoje aiškinama, kaip apdoroti paskirstymo užsakymą programoje „Dynamics 365 for Finance and Operations“.
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0798d9f1c09e827bf64635cf67102f77244948c5
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867444"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="4bfd1-103">Didžiosios knygos paskirstymo žurnalo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="4bfd1-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bfd1-104">Šioje temoje aiškinama, kaip apdoroti paskirstymo užsakymą programoje „Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-104">This topic explains how to process an allocation request in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="4bfd1-105">Norėdami kurti paskirstymo žurnalą, kurį būtų galima peržiūrėti ir patvirtinti prieš registruojant į DK arba registruoti tiesiogiai į DK, naudokite puslapį Paskirstymo užklausos apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="4bfd1-106">Norint sukurti paskirstymo žurnalą, privalo būti bent viena aktyvi Didžiosios knygos paskirstymo taisyklė.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="4bfd1-107">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="4bfd1-108">Naršymo srityje eikite į **Moduliai > Didžioji knyga > Paskirstymai > Paskirstymo užklausos procesas**.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="4bfd1-109">Lauke **Taisyklė** pasirinkite norimą įrašą išplečiamajame meniu.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="4bfd1-110">Lauke **Nuo datos** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="4bfd1-111">Laukas **Nuo datos** yra ypač svarbus, kai DK yra taisyklės duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="4bfd1-112">Šia data reguliuojama, kuriuos didžiosios knygos balansus įtraukti į paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="4bfd1-113">Lauke **Nulinis šaltinis** pasirinkite **Stabdyti**.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="4bfd1-114">Šiuo veiksmu sustabdysite paskirstymo procesą ir pasirodys pranešimas, kuriama bus nurodoma, jog buvo pasirinktas nulinis šaltinių skaičius.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="4bfd1-115">Lauke **Pasiūlymo parinktys** pasirinkite **Tik pasiūlymas**.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="4bfd1-116">Pasirinkite **Tik pasiūlymas** peržiūrėti ir papildomai patvirtinti rezultatus paskirstymo žurnale prieš registruodami paskirstymą DK.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="4bfd1-117">Lauke DK registravimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="4bfd1-118">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-118">Select **OK**.</span></span>
7. <span data-ttu-id="4bfd1-119">Naršymo srityje eikite į **Moduliai > Didžioji knyga > Paskirstymai > Paskirstymų žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="4bfd1-120">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-120">Select **Lines**.</span></span>
9. <span data-ttu-id="4bfd1-121">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-121">Select **Post**.</span></span>
10. <span data-ttu-id="4bfd1-122">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="4bfd1-122">Select **Post**.</span></span>

