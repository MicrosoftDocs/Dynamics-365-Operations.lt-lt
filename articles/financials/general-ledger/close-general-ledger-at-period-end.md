---
title: "DK uždarymas laikotarpio pabaigoje"
description: "Šioje temoje aprašomos užduotis, kurios paprastai atliekamos uždarant DK laikotarpį."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c08d039863253b33438c92243d5c164408ef85f3
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="189d5-103">DK uždarymas laikotarpio pabaigoje</span><span class="sxs-lookup"><span data-stu-id="189d5-103">Close the general ledger at period end</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="189d5-104">Šioje temoje aprašomos užduotis, kurios paprastai atliekamos uždarant DK laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="189d5-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="189d5-105">Didžiojoje knygoje galite atlikti laikotarpio ar metų uždarymo procedūras.</span><span class="sxs-lookup"><span data-stu-id="189d5-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="189d5-106">Uždarymo procesai parengia sistemą naujam laikotarpui.</span><span class="sxs-lookup"><span data-stu-id="189d5-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="189d5-107">Norėdami parengti sistemą naujiems metams, turite paleisti uždarymo metų pabaigoje procesą.</span><span class="sxs-lookup"><span data-stu-id="189d5-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="189d5-108">Kiekviena organizacija turi skirtingus procesus ir veiksmus, kuriuos atlieka laikotarpio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="189d5-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="189d5-109">Štai keletas pasirinktinų veiksmų laikotarpio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="189d5-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="189d5-110">Užbaikite visas užduotis visuose kituose moduliuose, pvz., Gautinos sumos, Mokėtinos sumos ir Atsargos.</span><span class="sxs-lookup"><span data-stu-id="189d5-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="189d5-111">Patikrinkite, ar visi žurnalai užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="189d5-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="189d5-112">Vykdykite užsienio valiutos kurso pasikeitimą, kad sugeneruotumėte negauto pelno ar nuostolio sumas.</span><span class="sxs-lookup"><span data-stu-id="189d5-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="189d5-113">Sudenkite kiekvienos DK sąskaitos operacijas.</span><span class="sxs-lookup"><span data-stu-id="189d5-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="189d5-114">Vykdykite bet kokius reikiamus paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="189d5-114">Process any required allocations.</span></span>
-   <span data-ttu-id="189d5-115">Neautomatiniu būdu registruokite laikotarpio pabaigos koregavimus.</span><span class="sxs-lookup"><span data-stu-id="189d5-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="189d5-116">Įtraukite operacijas į žurnalą ir peržiūrėkite ataskaitą **DK žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="189d5-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="189d5-117">Atlikite konsolidavimą naudodami konsoliduojančią įmonę arba finansines ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="189d5-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="189d5-118">Sugeneruokite laikotarpio pabaigos finansines ataskaitas srityje „Finansinės ataskaitos“.</span><span class="sxs-lookup"><span data-stu-id="189d5-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="189d5-119">Nustatykite DK laikotarpių reikšmę **Sulaikyta**, kad nebūtų atliekamas joks kitas registravimas.</span><span class="sxs-lookup"><span data-stu-id="189d5-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="189d5-120">Taip pat galite riboti laikotarpį konkrečiai vartotojų grupei, kol vykdomi laikotarpio pabaigos veiksmai, siekiant geresnės kontrolės.</span><span class="sxs-lookup"><span data-stu-id="189d5-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="189d5-121">Nėra tikslinga nustatyti laikotarpių reikšmę **Uždaryta visam laikui**, nes uždaryto laikotarpio vėl atidaryti nebegalėsite.</span><span class="sxs-lookup"><span data-stu-id="189d5-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="189d5-122">Darbo sritį Finansinio laikotarpio uždarymas galima naudoti norint organizuoti ir sekti užduotis, reikalingas įvairiems periodams ir procesams.</span><span class="sxs-lookup"><span data-stu-id="189d5-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="189d5-123">Daugiau informacijos žr. tolesnėse temose:</span><span class="sxs-lookup"><span data-stu-id="189d5-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="189d5-124">Finansinio laikotarpio uždarymo darbo sritis</span><span class="sxs-lookup"><span data-stu-id="189d5-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="189d5-125">Uždarymas metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="189d5-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="189d5-126">Masinis finansinio laikotarpio uždarymas</span><span class="sxs-lookup"><span data-stu-id="189d5-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)





