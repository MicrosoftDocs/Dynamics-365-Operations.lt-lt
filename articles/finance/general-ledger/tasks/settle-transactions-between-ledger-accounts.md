---
title: DK sąskaitų operacijų sudengimas
description: Ši procedūra nurodo, kaip sudengti operacijas tarp DK sąskaitų ir atšaukti DK sudengimą.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6ed76f82532d43a3c05b60b12176fe851e327956
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175541"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="8caa3-103">DK sąskaitų operacijų sudengimas</span><span class="sxs-lookup"><span data-stu-id="8caa3-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8caa3-104">Ši procedūra nurodo, kaip sudengti operacijas tarp DK sąskaitų ir atšaukti DK sudengimą.</span><span class="sxs-lookup"><span data-stu-id="8caa3-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="8caa3-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="8caa3-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="8caa3-106">DK sąskaitų operacijos sudengimas</span><span class="sxs-lookup"><span data-stu-id="8caa3-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="8caa3-107">Pasirinkite Didžioji knyga > Periodinės užduotys > DK sudengimai.</span><span class="sxs-lookup"><span data-stu-id="8caa3-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="8caa3-108">Sąraše raskite operaciją, kurią norite sudengti.</span><span class="sxs-lookup"><span data-stu-id="8caa3-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="8caa3-109">Sumos balansas turi būti nulis.</span><span class="sxs-lookup"><span data-stu-id="8caa3-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="8caa3-110">Spustelėkite Įtraukti.</span><span class="sxs-lookup"><span data-stu-id="8caa3-110">Click Include.</span></span>
4. <span data-ttu-id="8caa3-111">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="8caa3-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="8caa3-112">DK sudengimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="8caa3-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="8caa3-113">Pasirinkite Didžioji knyga > Užklausos ir ataskaitos > Bandomasis balansas.</span><span class="sxs-lookup"><span data-stu-id="8caa3-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="8caa3-114">Spustelėdami Parametrai atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="8caa3-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="8caa3-115">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="8caa3-115">Click Update.</span></span>
4. <span data-ttu-id="8caa3-116">Sąraše raskite sąskaitą, kurioje yra sudengta operacija.</span><span class="sxs-lookup"><span data-stu-id="8caa3-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="8caa3-117">Spustelėkite Visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="8caa3-117">Click All transactions.</span></span>
6. <span data-ttu-id="8caa3-118">Naudokite filtrą, kad galėtumėte sąraše lengvai rasti operaciją.</span><span class="sxs-lookup"><span data-stu-id="8caa3-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="8caa3-119">Spustelėkite DK sudengimai.</span><span class="sxs-lookup"><span data-stu-id="8caa3-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="8caa3-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8caa3-120">In the list, mark the selected row.</span></span>

