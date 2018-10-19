--- 
title: "DK sąskaitų operacijų sudengimas"
description: "Ši procedūra nurodo, kaip sudengti operacijas tarp DK sąskaitų ir atšaukti DK sudengimą."
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74522c97716238b62af3d65a1c23ba9e5e60a68b
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="169dc-103">DK sąskaitų operacijų sudengimas</span><span class="sxs-lookup"><span data-stu-id="169dc-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="169dc-104">Ši procedūra nurodo, kaip sudengti operacijas tarp DK sąskaitų ir atšaukti DK sudengimą.</span><span class="sxs-lookup"><span data-stu-id="169dc-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="169dc-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="169dc-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="169dc-106">DK sąskaitų operacijos sudengimas</span><span class="sxs-lookup"><span data-stu-id="169dc-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="169dc-107">Pasirinkite Didžioji knyga > Periodinės užduotys > DK sudengimai.</span><span class="sxs-lookup"><span data-stu-id="169dc-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="169dc-108">Sąraše raskite operaciją, kurią norite sudengti.</span><span class="sxs-lookup"><span data-stu-id="169dc-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="169dc-109">Sumos balansas turi būti nulis.</span><span class="sxs-lookup"><span data-stu-id="169dc-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="169dc-110">Spustelėkite Įtraukti.</span><span class="sxs-lookup"><span data-stu-id="169dc-110">Click Include.</span></span>
4. <span data-ttu-id="169dc-111">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="169dc-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="169dc-112">DK sudengimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="169dc-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="169dc-113">Pasirinkite Didžioji knyga > Užklausos ir ataskaitos > Bandomasis balansas.</span><span class="sxs-lookup"><span data-stu-id="169dc-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="169dc-114">Spustelėdami Parametrai atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="169dc-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="169dc-115">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="169dc-115">Click Update.</span></span>
4. <span data-ttu-id="169dc-116">Sąraše raskite sąskaitą, kurioje yra sudengta operacija.</span><span class="sxs-lookup"><span data-stu-id="169dc-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="169dc-117">Spustelėkite Visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="169dc-117">Click All transactions.</span></span>
6. <span data-ttu-id="169dc-118">Naudokite filtrą, kad galėtumėte sąraše lengvai rasti operaciją.</span><span class="sxs-lookup"><span data-stu-id="169dc-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="169dc-119">Spustelėkite DK sudengimai.</span><span class="sxs-lookup"><span data-stu-id="169dc-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="169dc-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="169dc-120">In the list, mark the selected row.</span></span>


