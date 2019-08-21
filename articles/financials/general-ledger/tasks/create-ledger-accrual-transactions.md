---
title: DK kaupimo operacijų kūrimas
description: Šis užduoties vadovas padeda sugeneruoti DK kaupimo operacijas, kurios pagrįstos kaupimo schemomis.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06743ca3ed13906e3f65d3783db7a7f74fb53e3f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846612"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="9f0d9-103">DK kaupimo operacijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="9f0d9-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f0d9-104">Šis užduoties vadovas padeda sugeneruoti DK kaupimo operacijas, kurios pagrįstos kaupimo schemomis</span><span class="sxs-lookup"><span data-stu-id="9f0d9-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="9f0d9-105">Pasirinkite Didžioji knyga > Žurnalų įrašai > Bendrieji žurnalai.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="9f0d9-106">Sąraše raskite ir pasirinkite norimą žurnalą arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="9f0d9-107">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="9f0d9-108">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="9f0d9-109">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="9f0d9-110">Šiame pavyzdyje mes nurodome išlaidas už draudimą.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="9f0d9-111">Tai taps periodinių išlaidų suma.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="9f0d9-112">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="9f0d9-113">Lauke Debetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="9f0d9-114">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="9f0d9-115">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-115">Click Functions.</span></span>
10. <span data-ttu-id="9f0d9-116">Spustelėkite DK kaupimai.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="9f0d9-117">Lauke Kaupimo identifikacija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="9f0d9-118">Sąraše raskite ir pasirinkite norimą taikyti kaupimo schemą.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="9f0d9-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9f0d9-120">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="9f0d9-121">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-121">Click Transactions.</span></span>
16. <span data-ttu-id="9f0d9-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-122">Close the page.</span></span>
17. <span data-ttu-id="9f0d9-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-123">Click OK.</span></span>
18. <span data-ttu-id="9f0d9-124">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="9f0d9-124">Click Post.</span></span>

