---
title: Mokėti kliento mokėjimus
description: Deponuokite kliento mokėjimus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7357683e46df04c3dedd7e22607748512c9de94a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220256"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="fffbe-103">Mokėti kliento mokėjimus</span><span class="sxs-lookup"><span data-stu-id="fffbe-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fffbe-104">Deponuokite kliento mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="fffbe-104">Deposit customer payments.</span></span> <span data-ttu-id="fffbe-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="fffbe-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="fffbe-106">Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Mokėjimai > Mokėjimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="fffbe-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-107">Select **New**.</span></span>
3. <span data-ttu-id="fffbe-108">Lauke **Pavadinimas** pasirinkite **CustPay** išplečiamajame meniu.</span><span class="sxs-lookup"><span data-stu-id="fffbe-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="fffbe-109">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-109">Select **Lines**.</span></span>
5. <span data-ttu-id="fffbe-110">Lauke **Klientas** pasirinkite klientą, kuriam išrašote mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="fffbe-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="fffbe-111">Lauke **Kreditas** įveskite mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="fffbe-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="fffbe-112">Pasirinkdami SF, kurios buvo sumokėtos, galite sumą palikti tuščią, kad ją apskaičiuotų sistema.</span><span class="sxs-lookup"><span data-stu-id="fffbe-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="fffbe-113">Lauke **Mokėjimo nuoroda** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fffbe-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="fffbe-114">Mokėjimo nuoroda galėtų būti įvedamas mokėjimo čekio numeris.</span><span class="sxs-lookup"><span data-stu-id="fffbe-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="fffbe-115">Mokėjimo nuorodos reikia tam, kad mokėjimą būtų galima įtraukti į depozito kvitą,</span><span class="sxs-lookup"><span data-stu-id="fffbe-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="fffbe-116">Pažymėkite langelį Naudoti depozito kvitą.</span><span class="sxs-lookup"><span data-stu-id="fffbe-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="fffbe-117">Jei mokėjimas turėtų būti įtrauktas į depozitą, šią nuostatą pakeiskite į Taip.</span><span class="sxs-lookup"><span data-stu-id="fffbe-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="fffbe-118">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-118">Select **New**.</span></span>
10. <span data-ttu-id="fffbe-119">Lauke **Klientas** pasirinkite klientą kitam mokėjimui.</span><span class="sxs-lookup"><span data-stu-id="fffbe-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="fffbe-120">Lauke **Kreditas** įveskite mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="fffbe-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="fffbe-121">Lauke **Mokėjimo nuoroda** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fffbe-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="fffbe-122">Pažymėkite langelį **Naudoti depozito kvitą**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="fffbe-123">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-123">Select **Post**.</span></span> <span data-ttu-id="fffbe-124">Prieš generuojant depozito kvitą, reikia registruoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="fffbe-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="fffbe-125">Tuo siekiama užtikrinti, kad, sugeneravus depozito kvitą, nepasikeistų mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="fffbe-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="fffbe-126">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-126">Select **Functions**.</span></span>
16. <span data-ttu-id="fffbe-127">Pasirinkite **Depozito kvitas**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="fffbe-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-128">Select **OK**.</span></span> <span data-ttu-id="fffbe-129">Pirmasis puslapis naudojamas kurti depozito kvitui.</span><span class="sxs-lookup"><span data-stu-id="fffbe-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="fffbe-130">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fffbe-130">Select **OK**.</span></span> <span data-ttu-id="fffbe-131">Antrasis veiksmas yra spausdinti depozito kvitą, tačiau šis veiksmas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="fffbe-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]