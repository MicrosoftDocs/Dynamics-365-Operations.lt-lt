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
ms.openlocfilehash: 6813871a4773d39d4abfdecc896a2aa8b320cbe0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222100"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="29be2-103">DK sąskaitų operacijų sudengimas</span><span class="sxs-lookup"><span data-stu-id="29be2-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29be2-104">Ši procedūra nurodo, kaip sudengti operacijas tarp DK sąskaitų ir atšaukti DK sudengimą.</span><span class="sxs-lookup"><span data-stu-id="29be2-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="29be2-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="29be2-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="29be2-106">DK sąskaitų operacijos sudengimas</span><span class="sxs-lookup"><span data-stu-id="29be2-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="29be2-107">Pasirinkite Didžioji knyga > Periodinės užduotys > DK sudengimai.</span><span class="sxs-lookup"><span data-stu-id="29be2-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="29be2-108">Sąraše raskite operaciją, kurią norite sudengti.</span><span class="sxs-lookup"><span data-stu-id="29be2-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="29be2-109">Sumos balansas turi būti nulis.</span><span class="sxs-lookup"><span data-stu-id="29be2-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="29be2-110">Spustelėkite Įtraukti.</span><span class="sxs-lookup"><span data-stu-id="29be2-110">Click Include.</span></span>
4. <span data-ttu-id="29be2-111">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="29be2-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="29be2-112">DK sudengimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="29be2-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="29be2-113">Pasirinkite Didžioji knyga > Užklausos ir ataskaitos > Bandomasis balansas.</span><span class="sxs-lookup"><span data-stu-id="29be2-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="29be2-114">Spustelėdami Parametrai atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="29be2-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="29be2-115">Spustelėkite Naujinti.</span><span class="sxs-lookup"><span data-stu-id="29be2-115">Click Update.</span></span>
4. <span data-ttu-id="29be2-116">Sąraše raskite sąskaitą, kurioje yra sudengta operacija.</span><span class="sxs-lookup"><span data-stu-id="29be2-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="29be2-117">Spustelėkite Visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="29be2-117">Click All transactions.</span></span>
6. <span data-ttu-id="29be2-118">Naudokite filtrą, kad galėtumėte sąraše lengvai rasti operaciją.</span><span class="sxs-lookup"><span data-stu-id="29be2-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="29be2-119">Spustelėkite DK sudengimai.</span><span class="sxs-lookup"><span data-stu-id="29be2-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="29be2-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="29be2-120">In the list, mark the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]