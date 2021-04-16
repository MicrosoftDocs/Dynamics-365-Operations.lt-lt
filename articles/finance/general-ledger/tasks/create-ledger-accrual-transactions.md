---
title: DK kaupimo operacijų kūrimas
description: Šis užduoties vadovas padeda sugeneruoti DK kaupimo operacijas, kurios pagrįstos kaupimo schemomis.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6eb0d20c530e25c3ec5c1e013859b9d7e776b30f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832831"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="5283b-103">DK kaupimo operacijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="5283b-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5283b-104">Šis užduoties vadovas padeda sugeneruoti DK kaupimo operacijas, kurios pagrįstos kaupimo schemomis</span><span class="sxs-lookup"><span data-stu-id="5283b-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="5283b-105">Pasirinkite Didžioji knyga > Žurnalų įrašai > Bendrieji žurnalai.</span><span class="sxs-lookup"><span data-stu-id="5283b-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="5283b-106">Sąraše raskite ir pasirinkite norimą žurnalą arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="5283b-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="5283b-107">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="5283b-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="5283b-108">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="5283b-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="5283b-109">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="5283b-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="5283b-110">Šiame pavyzdyje mes nurodome išlaidas už draudimą.</span><span class="sxs-lookup"><span data-stu-id="5283b-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="5283b-111">Tai taps periodinių išlaidų suma.</span><span class="sxs-lookup"><span data-stu-id="5283b-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="5283b-112">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5283b-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="5283b-113">Lauke Debetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="5283b-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="5283b-114">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="5283b-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="5283b-115">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="5283b-115">Click Functions.</span></span>
10. <span data-ttu-id="5283b-116">Spustelėkite DK kaupimai.</span><span class="sxs-lookup"><span data-stu-id="5283b-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="5283b-117">Lauke Kaupimo identifikacija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="5283b-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="5283b-118">Sąraše raskite ir pasirinkite norimą taikyti kaupimo schemą.</span><span class="sxs-lookup"><span data-stu-id="5283b-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="5283b-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5283b-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="5283b-120">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="5283b-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="5283b-121">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="5283b-121">Click Transactions.</span></span>
16. <span data-ttu-id="5283b-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5283b-122">Close the page.</span></span>
17. <span data-ttu-id="5283b-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5283b-123">Click OK.</span></span>
18. <span data-ttu-id="5283b-124">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="5283b-124">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]