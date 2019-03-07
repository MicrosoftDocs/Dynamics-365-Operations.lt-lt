---
title: Mokėti kliento mokėjimus
description: Deponuokite kliento mokėjimus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "313387"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="97e97-103">Mokėti kliento mokėjimus</span><span class="sxs-lookup"><span data-stu-id="97e97-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97e97-104">Deponuokite kliento mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="97e97-104">Deposit customer payments.</span></span> <span data-ttu-id="97e97-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="97e97-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="97e97-106">Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="97e97-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="97e97-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="97e97-107">Click New.</span></span>
3. <span data-ttu-id="97e97-108">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="97e97-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="97e97-109">Pasirinkite mokėjimų žurnalą.</span><span class="sxs-lookup"><span data-stu-id="97e97-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="97e97-110">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="97e97-110">Click Lines.</span></span>
6. <span data-ttu-id="97e97-111">Lauke Sąskaita pasirinkite klientą, kuriam įrašote mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="97e97-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="97e97-112">Lauke Kreditas įveskite mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="97e97-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="97e97-113">Pasirinkdami SF, kurios buvo sumokėtos, galite sumą palikti tuščią, kad ją apskaičiuotų sistema.</span><span class="sxs-lookup"><span data-stu-id="97e97-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="97e97-114">Lauke Mokėjimo nuoroda surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97e97-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="97e97-115">Mokėjimo nuoroda galėtų būti įvedamas mokėjimo čekio numeris.</span><span class="sxs-lookup"><span data-stu-id="97e97-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="97e97-116">Mokėjimo nuorodos reikia tam, kad mokėjimą būtų galima įtraukti į depozito kvitą,</span><span class="sxs-lookup"><span data-stu-id="97e97-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="97e97-117">Pažymėkite langelį Naudoti depozito kvitą.</span><span class="sxs-lookup"><span data-stu-id="97e97-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="97e97-118">Jei mokėjimas turėtų būti įtrauktas į depozitą, šią nuostatą pakeiskite į Taip.</span><span class="sxs-lookup"><span data-stu-id="97e97-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="97e97-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="97e97-119">Click New.</span></span>
11. <span data-ttu-id="97e97-120">Lauke Sąskaita pasirinkite kito mokėjimo klientą.</span><span class="sxs-lookup"><span data-stu-id="97e97-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="97e97-121">Lauke Kreditas įveskite mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="97e97-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="97e97-122">Lauke Mokėjimo nuoroda surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97e97-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="97e97-123">Pažymėkite langelį Naudoti depozito kvitą.</span><span class="sxs-lookup"><span data-stu-id="97e97-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="97e97-124">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="97e97-124">Click Post.</span></span>
    * <span data-ttu-id="97e97-125">Prieš generuojant depozito kvitą, reikia registruoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="97e97-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="97e97-126">Tuo siekiama užtikrinti, kad, sugeneravus depozito kvitą, nepasikeistų mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="97e97-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="97e97-127">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="97e97-127">Click Functions.</span></span>
17. <span data-ttu-id="97e97-128">Spustelėkite Depozito kvitas.</span><span class="sxs-lookup"><span data-stu-id="97e97-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="97e97-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="97e97-129">Click OK.</span></span>
    * <span data-ttu-id="97e97-130">Pirmasis puslapis naudojamas kurti depozito kvitui.</span><span class="sxs-lookup"><span data-stu-id="97e97-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="97e97-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="97e97-131">Click OK.</span></span>
    * <span data-ttu-id="97e97-132">Antrasis veiksmas yra spausdinti depozito kvitą, tačiau šis veiksmas nebūtinas.</span><span class="sxs-lookup"><span data-stu-id="97e97-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

