---
title: Vėlesnio čekio iš kliento sudengimas
description: Galite sudengti vėlesnį čekį, kai čekis apdorojamas banko.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 635a1c50390bca59cd1c9ba0cf0421c510b2998c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179041"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="69005-103">Vėlesnio čekio iš kliento sudengimas</span><span class="sxs-lookup"><span data-stu-id="69005-103">Settle a postdated check from a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="69005-104">Galite sudengti vėlesnį čekį, kai čekis apdorojamas banko.</span><span class="sxs-lookup"><span data-stu-id="69005-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="69005-105">Ši finansinė operacija taip pat apdoroja vėlesnio čekio tarpinės sąskaitos operaciją.</span><span class="sxs-lookup"><span data-stu-id="69005-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="69005-106">Prieš pradėdami šitą, turite įvykdyti toliau nurodytas užduotis.</span><span class="sxs-lookup"><span data-stu-id="69005-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="69005-107">Vėlesnių čekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="69005-107">Set up postdated checks</span></span>

2) <span data-ttu-id="69005-108">Registruoti kliento vėlesnį čekį</span><span class="sxs-lookup"><span data-stu-id="69005-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="69005-109">Šio užduočių vadovo vaidmuo yra Iždininkas.</span><span class="sxs-lookup"><span data-stu-id="69005-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="69005-110">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="69005-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="69005-111">Pasirinkite Kreditas ir mokėjimai > Užklausos ir ataskaitos > Mokėjimai > Kliento vėlesni čekiai.</span><span class="sxs-lookup"><span data-stu-id="69005-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="69005-112">Spustelėkite Sudengimas.</span><span class="sxs-lookup"><span data-stu-id="69005-112">Click Settle.</span></span>
3. <span data-ttu-id="69005-113">Spustelėkite Sudengti atsiskaitymo įrašus.</span><span class="sxs-lookup"><span data-stu-id="69005-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="69005-114">Apmokėkite kliento čekio operacijos sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="69005-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="69005-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="69005-115">Close the page.</span></span>
5. <span data-ttu-id="69005-116">Pasirinkite Didžioji knyga > Žurnalų įrašai > Bendrieji žurnalai.</span><span class="sxs-lookup"><span data-stu-id="69005-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="69005-117">Lauke Rodyti pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="69005-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="69005-118">Pažymėkite arba išvalykite žymės langelį Rodyti tik vartotojo sukurtus.</span><span class="sxs-lookup"><span data-stu-id="69005-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="69005-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="69005-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="69005-120">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="69005-120">Click Lines.</span></span>
10. <span data-ttu-id="69005-121">Spustelėkite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="69005-121">Click Voucher.</span></span>
11. <span data-ttu-id="69005-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="69005-122">Close the page.</span></span>

