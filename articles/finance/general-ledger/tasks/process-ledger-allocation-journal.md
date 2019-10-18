---
title: Didžiosios knygos paskirstymo žurnalo apdorojimas
description: Šioje temoje aiškinama, kaip apdoroti paskirstymo užsakymą programoje „Dynamics 365 Finance“.
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
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186077"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="1792d-103">Didžiosios knygos paskirstymo žurnalo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="1792d-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1792d-104">Šioje temoje aiškinama, kaip apdoroti paskirstymo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1792d-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="1792d-105">Norėdami kurti paskirstymo žurnalą, kurį būtų galima peržiūrėti ir patvirtinti prieš registruojant į DK arba registruoti tiesiogiai į DK, naudokite puslapį Paskirstymo užklausos apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="1792d-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="1792d-106">Norint sukurti paskirstymo žurnalą, privalo būti bent viena aktyvi Didžiosios knygos paskirstymo taisyklė.</span><span class="sxs-lookup"><span data-stu-id="1792d-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="1792d-107">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="1792d-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1792d-108">Naršymo srityje eikite į **Moduliai > Didžioji knyga > Paskirstymai > Paskirstymo užklausos procesas**.</span><span class="sxs-lookup"><span data-stu-id="1792d-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="1792d-109">Lauke **Taisyklė** pasirinkite norimą įrašą išplečiamajame meniu.</span><span class="sxs-lookup"><span data-stu-id="1792d-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="1792d-110">Lauke **Nuo datos** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="1792d-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="1792d-111">Laukas **Nuo datos** yra ypač svarbus, kai DK yra taisyklės duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="1792d-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="1792d-112">Šia data reguliuojama, kuriuos didžiosios knygos balansus įtraukti į paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="1792d-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="1792d-113">Lauke **Nulinis šaltinis** pasirinkite **Stabdyti**.</span><span class="sxs-lookup"><span data-stu-id="1792d-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="1792d-114">Šiuo veiksmu sustabdysite paskirstymo procesą ir pasirodys pranešimas, kuriama bus nurodoma, jog buvo pasirinktas nulinis šaltinių skaičius.</span><span class="sxs-lookup"><span data-stu-id="1792d-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="1792d-115">Lauke **Pasiūlymo parinktys** pasirinkite **Tik pasiūlymas**.</span><span class="sxs-lookup"><span data-stu-id="1792d-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="1792d-116">Pasirinkite **Tik pasiūlymas** peržiūrėti ir papildomai patvirtinti rezultatus paskirstymo žurnale prieš registruodami paskirstymą DK.</span><span class="sxs-lookup"><span data-stu-id="1792d-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="1792d-117">Lauke DK registravimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="1792d-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="1792d-118">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1792d-118">Select **OK**.</span></span>
7. <span data-ttu-id="1792d-119">Naršymo srityje eikite į **Moduliai > Didžioji knyga > Paskirstymai > Paskirstymų žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="1792d-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="1792d-120">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="1792d-120">Select **Lines**.</span></span>
9. <span data-ttu-id="1792d-121">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="1792d-121">Select **Post**.</span></span>
10. <span data-ttu-id="1792d-122">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="1792d-122">Select **Post**.</span></span>

