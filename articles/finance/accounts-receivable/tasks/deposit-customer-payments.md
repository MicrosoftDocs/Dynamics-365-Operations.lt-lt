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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140191"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="09926-103">Mokėti kliento mokėjimus</span><span class="sxs-lookup"><span data-stu-id="09926-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09926-104">Deponuokite kliento mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="09926-104">Deposit customer payments.</span></span> <span data-ttu-id="09926-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="09926-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="09926-106">Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Mokėjimai > Mokėjimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="09926-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="09926-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="09926-107">Select **New**.</span></span>
3. <span data-ttu-id="09926-108">Lauke **Pavadinimas** pasirinkite **CustPay** išplečiamajame meniu.</span><span class="sxs-lookup"><span data-stu-id="09926-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="09926-109">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="09926-109">Select **Lines**.</span></span>
5. <span data-ttu-id="09926-110">Lauke **Klientas** pasirinkite klientą, kuriam išrašote mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="09926-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="09926-111">Lauke **Kreditas** įveskite mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="09926-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="09926-112">Pasirinkdami SF, kurios buvo sumokėtos, galite sumą palikti tuščią, kad ją apskaičiuotų sistema.</span><span class="sxs-lookup"><span data-stu-id="09926-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="09926-113">Lauke **Mokėjimo nuoroda** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09926-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="09926-114">Mokėjimo nuoroda galėtų būti įvedamas mokėjimo čekio numeris.</span><span class="sxs-lookup"><span data-stu-id="09926-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="09926-115">Mokėjimo nuorodos reikia tam, kad mokėjimą būtų galima įtraukti į depozito kvitą,</span><span class="sxs-lookup"><span data-stu-id="09926-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="09926-116">Pažymėkite langelį Naudoti depozito kvitą.</span><span class="sxs-lookup"><span data-stu-id="09926-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="09926-117">Jei mokėjimas turėtų būti įtrauktas į depozitą, šią nuostatą pakeiskite į Taip.</span><span class="sxs-lookup"><span data-stu-id="09926-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="09926-118">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="09926-118">Select **New**.</span></span>
10. <span data-ttu-id="09926-119">Lauke **Klientas** pasirinkite klientą kitam mokėjimui.</span><span class="sxs-lookup"><span data-stu-id="09926-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="09926-120">Lauke **Kreditas** įveskite mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="09926-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="09926-121">Lauke **Mokėjimo nuoroda** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09926-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="09926-122">Pažymėkite langelį **Naudoti depozito kvitą**.</span><span class="sxs-lookup"><span data-stu-id="09926-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="09926-123">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="09926-123">Select **Post**.</span></span> <span data-ttu-id="09926-124">Prieš generuojant depozito kvitą, reikia registruoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="09926-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="09926-125">Tuo siekiama užtikrinti, kad, sugeneravus depozito kvitą, nepasikeistų mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="09926-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="09926-126">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="09926-126">Select **Functions**.</span></span>
16. <span data-ttu-id="09926-127">Pasirinkite **Depozito kvitas**.</span><span class="sxs-lookup"><span data-stu-id="09926-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="09926-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="09926-128">Select **OK**.</span></span> <span data-ttu-id="09926-129">Pirmasis puslapis naudojamas kurti depozito kvitui.</span><span class="sxs-lookup"><span data-stu-id="09926-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="09926-130">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="09926-130">Select **OK**.</span></span> <span data-ttu-id="09926-131">Antrasis veiksmas yra spausdinti depozito kvitą, tačiau šis veiksmas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="09926-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

