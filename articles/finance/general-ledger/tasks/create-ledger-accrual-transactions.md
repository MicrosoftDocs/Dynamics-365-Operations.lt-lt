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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cbda1c535aad63df55d40bcbadccffc3f35b455
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994645"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="7af9c-103">DK kaupimo operacijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="7af9c-103">Create ledger accrual transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7af9c-104">Šis užduoties vadovas padeda sugeneruoti DK kaupimo operacijas, kurios pagrįstos kaupimo schemomis</span><span class="sxs-lookup"><span data-stu-id="7af9c-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="7af9c-105">Pasirinkite Didžioji knyga > Žurnalų įrašai > Bendrieji žurnalai.</span><span class="sxs-lookup"><span data-stu-id="7af9c-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="7af9c-106">Sąraše raskite ir pasirinkite norimą žurnalą arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="7af9c-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="7af9c-107">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="7af9c-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="7af9c-108">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="7af9c-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="7af9c-109">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="7af9c-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="7af9c-110">Šiame pavyzdyje mes nurodome išlaidas už draudimą.</span><span class="sxs-lookup"><span data-stu-id="7af9c-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="7af9c-111">Tai taps periodinių išlaidų suma.</span><span class="sxs-lookup"><span data-stu-id="7af9c-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="7af9c-112">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7af9c-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="7af9c-113">Lauke Debetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7af9c-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="7af9c-114">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="7af9c-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="7af9c-115">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="7af9c-115">Click Functions.</span></span>
10. <span data-ttu-id="7af9c-116">Spustelėkite DK kaupimai.</span><span class="sxs-lookup"><span data-stu-id="7af9c-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="7af9c-117">Lauke Kaupimo identifikacija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="7af9c-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="7af9c-118">Sąraše raskite ir pasirinkite norimą taikyti kaupimo schemą.</span><span class="sxs-lookup"><span data-stu-id="7af9c-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="7af9c-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7af9c-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7af9c-120">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="7af9c-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="7af9c-121">Spustelėkite Operacijos.</span><span class="sxs-lookup"><span data-stu-id="7af9c-121">Click Transactions.</span></span>
16. <span data-ttu-id="7af9c-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7af9c-122">Close the page.</span></span>
17. <span data-ttu-id="7af9c-123">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7af9c-123">Click OK.</span></span>
18. <span data-ttu-id="7af9c-124">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="7af9c-124">Click Post.</span></span>

