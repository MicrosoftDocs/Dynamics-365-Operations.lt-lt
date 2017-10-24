--- 
title: "Kurti kaupimo schemą"
description: "Šis užduoties vadovas padeda sukurti kaupimo schemą."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 324be23a1e26de0d05c7cf6a61567f7260d0c390
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="ecf74-103">Kurti kaupimo schemą</span><span class="sxs-lookup"><span data-stu-id="ecf74-103">Create accrual schemes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ecf74-104">Šis užduoties vadovas padeda sukurti kaupimo schemą.</span><span class="sxs-lookup"><span data-stu-id="ecf74-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="ecf74-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="ecf74-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ecf74-106">Pasirinkite Didžioji knyga > Žurnalo nustatymas > Kaupimo schemos.</span><span class="sxs-lookup"><span data-stu-id="ecf74-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="ecf74-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ecf74-107">Click New.</span></span>
3. <span data-ttu-id="ecf74-108">Lauke Kaupimo identifikacija įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ecf74-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="ecf74-109">Lauke Kaupimo schemos aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ecf74-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="ecf74-110">Lauke Debetas nurodykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ecf74-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="ecf74-111">Nurodyta pagrindinė sąskaita žurnalo kvito eilutėje pakeis debeto pagrindinę sąskaitą, be to ji bus naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="ecf74-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="ecf74-112">Lauke Kreditas nurodykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ecf74-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="ecf74-113">Nurodyta pagrindinė sąskaita žurnalo kvito eilutėje pakeis kredito pagrindinę sąskaitą, be to ji bus naudojama atšaukiant atidėjimą pagal DK kaupimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="ecf74-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="ecf74-114">Lauke Kvitas pasirinkite, kaip norite nustatyti kvitą registruojant operacijas.</span><span class="sxs-lookup"><span data-stu-id="ecf74-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="ecf74-115">Lauke Aprašas įveskite reikšmę, kuria būtų aprašomos registruojamos operacijos.</span><span class="sxs-lookup"><span data-stu-id="ecf74-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="ecf74-116">Lauke Laikotarpio dažnis pasirinkite, kaip dažnai operacijos turėtų būti vykdomos.</span><span class="sxs-lookup"><span data-stu-id="ecf74-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="ecf74-117">Lauke Pasikartojimų skaičius pagal laikotarpį įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ecf74-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="ecf74-118">Lauke Registruoti operacijas pasirinkite, kada turi būti registruojamos operacijos, pvz., kas mėnesį.</span><span class="sxs-lookup"><span data-stu-id="ecf74-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


