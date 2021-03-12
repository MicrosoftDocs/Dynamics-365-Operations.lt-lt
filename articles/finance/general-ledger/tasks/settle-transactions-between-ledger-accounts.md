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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8220bacc8d683163e97956ec59a5af929b04319c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994420"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="0cb49-103">DK sąskaitų operacijų sudengimas</span><span class="sxs-lookup"><span data-stu-id="0cb49-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0cb49-104">Ši procedūra nurodo, kaip sudengti operacijas tarp DK sąskaitų ir atšaukti DK sudengimą.</span><span class="sxs-lookup"><span data-stu-id="0cb49-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="0cb49-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="0cb49-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="0cb49-106">DK sąskaitų operacijos sudengimas</span><span class="sxs-lookup"><span data-stu-id="0cb49-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="0cb49-107">Pasirinkite Didžioji knyga > Periodinės užduotys > DK sudengimai.</span><span class="sxs-lookup"><span data-stu-id="0cb49-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="0cb49-108">Sąraše raskite operaciją, kurią norite sudengti.</span><span class="sxs-lookup"><span data-stu-id="0cb49-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="0cb49-109">Sumos balansas turi būti nulis.</span><span class="sxs-lookup"><span data-stu-id="0cb49-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="0cb49-110">Spustelėkite Įtraukti.</span><span class="sxs-lookup"><span data-stu-id="0cb49-110">Click Include.</span></span>
4. <span data-ttu-id="0cb49-111">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="0cb49-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="0cb49-112">DK sudengimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="0cb49-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="0cb49-113">Pasirinkite Didžioji knyga > Užklausos ir ataskaitos > Bandomasis balansas.</span><span class="sxs-lookup"><span data-stu-id="0cb49-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="0cb49-114">Spustelėdami Parametrai atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="0cb49-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="0cb49-115">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="0cb49-115">Click Update.</span></span>
4. <span data-ttu-id="0cb49-116">Sąraše raskite sąskaitą, kurioje yra sudengta operacija.</span><span class="sxs-lookup"><span data-stu-id="0cb49-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="0cb49-117">Spustelėkite Visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="0cb49-117">Click All transactions.</span></span>
6. <span data-ttu-id="0cb49-118">Naudokite filtrą, kad galėtumėte sąraše lengvai rasti operaciją.</span><span class="sxs-lookup"><span data-stu-id="0cb49-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="0cb49-119">Spustelėkite DK sudengimai.</span><span class="sxs-lookup"><span data-stu-id="0cb49-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="0cb49-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0cb49-120">In the list, mark the selected row.</span></span>

