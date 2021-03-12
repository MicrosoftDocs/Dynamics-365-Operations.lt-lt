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
ms.openlocfilehash: 9221101581a6a130889b7c941ca228070a000c56
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003161"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="ad880-103">Mokėti kliento mokėjimus</span><span class="sxs-lookup"><span data-stu-id="ad880-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad880-104">Deponuokite kliento mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="ad880-104">Deposit customer payments.</span></span> <span data-ttu-id="ad880-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="ad880-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ad880-106">Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Mokėjimai > Mokėjimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="ad880-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="ad880-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ad880-107">Select **New**.</span></span>
3. <span data-ttu-id="ad880-108">Lauke **Pavadinimas** pasirinkite **CustPay** išplečiamajame meniu.</span><span class="sxs-lookup"><span data-stu-id="ad880-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="ad880-109">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="ad880-109">Select **Lines**.</span></span>
5. <span data-ttu-id="ad880-110">Lauke **Klientas** pasirinkite klientą, kuriam išrašote mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="ad880-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="ad880-111">Lauke **Kreditas** įveskite mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="ad880-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="ad880-112">Pasirinkdami SF, kurios buvo sumokėtos, galite sumą palikti tuščią, kad ją apskaičiuotų sistema.</span><span class="sxs-lookup"><span data-stu-id="ad880-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="ad880-113">Lauke **Mokėjimo nuoroda** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ad880-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="ad880-114">Mokėjimo nuoroda galėtų būti įvedamas mokėjimo čekio numeris.</span><span class="sxs-lookup"><span data-stu-id="ad880-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="ad880-115">Mokėjimo nuorodos reikia tam, kad mokėjimą būtų galima įtraukti į depozito kvitą,</span><span class="sxs-lookup"><span data-stu-id="ad880-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="ad880-116">Pažymėkite langelį Naudoti depozito kvitą.</span><span class="sxs-lookup"><span data-stu-id="ad880-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="ad880-117">Jei mokėjimas turėtų būti įtrauktas į depozitą, šią nuostatą pakeiskite į Taip.</span><span class="sxs-lookup"><span data-stu-id="ad880-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="ad880-118">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ad880-118">Select **New**.</span></span>
10. <span data-ttu-id="ad880-119">Lauke **Klientas** pasirinkite klientą kitam mokėjimui.</span><span class="sxs-lookup"><span data-stu-id="ad880-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="ad880-120">Lauke **Kreditas** įveskite mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="ad880-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="ad880-121">Lauke **Mokėjimo nuoroda** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ad880-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="ad880-122">Pažymėkite langelį **Naudoti depozito kvitą**.</span><span class="sxs-lookup"><span data-stu-id="ad880-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="ad880-123">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="ad880-123">Select **Post**.</span></span> <span data-ttu-id="ad880-124">Prieš generuojant depozito kvitą, reikia registruoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="ad880-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="ad880-125">Tuo siekiama užtikrinti, kad, sugeneravus depozito kvitą, nepasikeistų mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="ad880-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="ad880-126">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="ad880-126">Select **Functions**.</span></span>
16. <span data-ttu-id="ad880-127">Pasirinkite **Depozito kvitas**.</span><span class="sxs-lookup"><span data-stu-id="ad880-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="ad880-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ad880-128">Select **OK**.</span></span> <span data-ttu-id="ad880-129">Pirmasis puslapis naudojamas kurti depozito kvitui.</span><span class="sxs-lookup"><span data-stu-id="ad880-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="ad880-130">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ad880-130">Select **OK**.</span></span> <span data-ttu-id="ad880-131">Antrasis veiksmas yra spausdinti depozito kvitą, tačiau šis veiksmas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="ad880-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

