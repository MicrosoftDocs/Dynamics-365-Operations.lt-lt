---
title: Vėlesnio tiekėjo čekio sudengimas
description: Sudenkite vėlesnį čekį, išduotą tiekėjui, kai bankas apdorojo čekio operaciją, po to, kai čekis tapo vėlesniu ir bankas jį apdorojo.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46b419ab613425ae2d758f80105ac94f1ec5cc2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "324335"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="9d88b-103">Vėlesnio tiekėjo čekio sudengimas</span><span class="sxs-lookup"><span data-stu-id="9d88b-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d88b-104">Sudenkite vėlesnį čekį, išduotą tiekėjui, kai bankas apdorojo čekio operaciją, po to, kai čekis tapo vėlesniu ir bankas jį apdorojo.</span><span class="sxs-lookup"><span data-stu-id="9d88b-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="9d88b-105">Prieš pradėdami šią atlikite toliau nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="9d88b-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="9d88b-106">Vėlesnių čekių nustatymas</span><span class="sxs-lookup"><span data-stu-id="9d88b-106">Set up postdated checks</span></span>

2) <span data-ttu-id="9d88b-107">Registruoti tiekėjo vėlesnį čekį</span><span class="sxs-lookup"><span data-stu-id="9d88b-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="9d88b-108">Šios procedūros vaidmuo yra Iždininkas.</span><span class="sxs-lookup"><span data-stu-id="9d88b-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="9d88b-109">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="9d88b-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="9d88b-110">Pasirinkite Mokėtinos sumos > Mokėjimai > Vėlesni tiekėjo čekiai.</span><span class="sxs-lookup"><span data-stu-id="9d88b-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="9d88b-111">Spustelėkite Sudengimas.</span><span class="sxs-lookup"><span data-stu-id="9d88b-111">Click Settle.</span></span>
3. <span data-ttu-id="9d88b-112">Spustelėkite Sudengti atsiskaitymo įrašus.</span><span class="sxs-lookup"><span data-stu-id="9d88b-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="9d88b-113">Apmokėkite tiekėjo čekio operacijos sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="9d88b-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="9d88b-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9d88b-114">Close the page.</span></span>
5. <span data-ttu-id="9d88b-115">Pasirinkite Didžioji knyga > Žurnalų įrašai > Bendrieji žurnalai.</span><span class="sxs-lookup"><span data-stu-id="9d88b-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="9d88b-116">Lauke Rodyti pasirinkite „Visi‟.</span><span class="sxs-lookup"><span data-stu-id="9d88b-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="9d88b-117">Pažymėkite arba išvalykite žymės langelį Rodyti tik vartotojo sukurtus.</span><span class="sxs-lookup"><span data-stu-id="9d88b-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="9d88b-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="9d88b-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9d88b-119">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="9d88b-119">Click Lines.</span></span>
10. <span data-ttu-id="9d88b-120">Spustelėkite Kvitas.</span><span class="sxs-lookup"><span data-stu-id="9d88b-120">Click Voucher.</span></span>
11. <span data-ttu-id="9d88b-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9d88b-121">Close the page.</span></span>

