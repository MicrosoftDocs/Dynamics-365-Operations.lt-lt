---
title: Apdoroti didžiosios knygos paskirstymo žurnalą
description: Norėdami kurti paskirstymo žurnalą, kurį būtų galima peržiūrėti ir patvirtinti prieš registruojant į DK arba registruoti tiesiogiai į DK, naudokite puslapį Paskirstymo užklausos apdorojimas.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2046e25719c9023bee99736488a4ee6f22723fe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550826"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="6754f-103">Apdoroti didžiosios knygos paskirstymo žurnalą</span><span class="sxs-lookup"><span data-stu-id="6754f-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6754f-104">Norėdami kurti paskirstymo žurnalą, kurį būtų galima peržiūrėti ir patvirtinti prieš registruojant į DK arba registruoti tiesiogiai į DK, naudokite puslapį Paskirstymo užklausos apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="6754f-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="6754f-105">Norint sukurti paskirstymo žurnalą, privalo būti bent viena aktyvi Didžiosios knygos paskirstymo taisyklė.</span><span class="sxs-lookup"><span data-stu-id="6754f-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="6754f-106">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="6754f-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6754f-107">Eikite į Didžioji knyga > Paskirstymai > Apdoroti paskirstymo užklausą.</span><span class="sxs-lookup"><span data-stu-id="6754f-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="6754f-108">Lauke Taisyklė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="6754f-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6754f-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="6754f-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6754f-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="6754f-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6754f-111">Lauke Taikymo pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="6754f-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="6754f-112">Taikymo pradžios data yra labai svarbi, kai Didžioji knyga yra taisyklės Duomenų šaltinis.</span><span class="sxs-lookup"><span data-stu-id="6754f-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="6754f-113">Šia data reguliuojama, kuriuos didžiosios knygos balansus įtraukti į paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="6754f-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="6754f-114">Lauke Nulinis šaltinis pasirinkite Stabdyti.</span><span class="sxs-lookup"><span data-stu-id="6754f-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="6754f-115">Taip bus sustabdytas paskirstymo procesas ir bus rodomas pranešimas, kuriame teigiama, kad pasirinkta nulinė šaltinio suma.</span><span class="sxs-lookup"><span data-stu-id="6754f-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="6754f-116">Lauke Pasiūlymo pasirinktys pasirinkite „Tik pasiūlymas“.</span><span class="sxs-lookup"><span data-stu-id="6754f-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="6754f-117">Pasirinkite Pasiūlymas tik tam, kad prieš registruodami paskirstymą Didžiojoje knygoje galėtumėte peržiūrėti ir pasirinktinai patvirtinti paskirstymo žurnalų rezultatą.</span><span class="sxs-lookup"><span data-stu-id="6754f-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="6754f-118">Lauke DK registravimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="6754f-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="6754f-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="6754f-119">Click OK.</span></span>
9. <span data-ttu-id="6754f-120">Eikite į Didžioji knyga > Paskirstymas > Paskirstymo žurnalai.</span><span class="sxs-lookup"><span data-stu-id="6754f-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="6754f-121">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="6754f-121">Click Lines.</span></span>
11. <span data-ttu-id="6754f-122">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="6754f-122">Click Post.</span></span>
12. <span data-ttu-id="6754f-123">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="6754f-123">Click Post.</span></span>

