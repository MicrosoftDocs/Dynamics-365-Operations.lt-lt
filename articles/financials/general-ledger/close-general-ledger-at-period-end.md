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
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 16acadf0b814ff5863873280cd8d6e6ddbdcffc8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="55184-103">DK uždarymas laikotarpio pabaigoje</span><span class="sxs-lookup"><span data-stu-id="55184-103">Close the general ledger at period end</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="55184-104">Šioje temoje aprašomos užduotis, kurios paprastai atliekamos uždarant DK laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="55184-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="55184-105">Didžiojoje knygoje galite atlikti laikotarpio ar metų uždarymo procedūras.</span><span class="sxs-lookup"><span data-stu-id="55184-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="55184-106">Uždarymo procesai parengia sistemą naujam laikotarpui.</span><span class="sxs-lookup"><span data-stu-id="55184-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="55184-107">Norėdami parengti sistemą naujiems metams, turite paleisti uždarymo metų pabaigoje procesą.</span><span class="sxs-lookup"><span data-stu-id="55184-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="55184-108">Kiekviena organizacija turi skirtingus procesus ir veiksmus, kuriuos atlieka laikotarpio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="55184-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="55184-109">Štai keletas pasirinktinų veiksmų laikotarpio pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="55184-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="55184-110">Užbaikite visas užduotis visuose kituose moduliuose, pvz., Gautinos sumos, Mokėtinos sumos ir Atsargos.</span><span class="sxs-lookup"><span data-stu-id="55184-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="55184-111">Patikrinkite, ar visi žurnalai užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="55184-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="55184-112">Vykdykite užsienio valiutos kurso pasikeitimą, kad sugeneruotumėte negauto pelno ar nuostolio sumas.</span><span class="sxs-lookup"><span data-stu-id="55184-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="55184-113">Sudenkite kiekvienos DK sąskaitos operacijas.</span><span class="sxs-lookup"><span data-stu-id="55184-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="55184-114">Vykdykite bet kokius reikiamus paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="55184-114">Process any required allocations.</span></span>
-   <span data-ttu-id="55184-115">Neautomatiniu būdu registruokite laikotarpio pabaigos koregavimus.</span><span class="sxs-lookup"><span data-stu-id="55184-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="55184-116">Įtraukite operacijas į žurnalą ir peržiūrėkite ataskaitą **DK žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="55184-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="55184-117">Atlikite konsolidavimą naudodami konsoliduojančią įmonę arba finansines ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="55184-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="55184-118">Sugeneruokite laikotarpio pabaigos finansines ataskaitas srityje „Finansinės ataskaitos“.</span><span class="sxs-lookup"><span data-stu-id="55184-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="55184-119">Nustatykite DK laikotarpių reikšmę **Sulaikyta**, kad nebūtų atliekamas joks kitas registravimas.</span><span class="sxs-lookup"><span data-stu-id="55184-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="55184-120">Taip pat galite riboti laikotarpį konkrečiai vartotojų grupei, kol vykdomi laikotarpio pabaigos veiksmai, siekiant geresnės kontrolės.</span><span class="sxs-lookup"><span data-stu-id="55184-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="55184-121">Nėra tikslinga nustatyti laikotarpių reikšmę **Uždaryta visam laikui**, nes uždaryto laikotarpio vėl atidaryti nebegalėsite.</span><span class="sxs-lookup"><span data-stu-id="55184-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="55184-122">Darbo sritį Finansinio laikotarpio uždarymas galima naudoti norint organizuoti ir sekti užduotis, reikalingas įvairiems periodams ir procesams.</span><span class="sxs-lookup"><span data-stu-id="55184-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="55184-123">Daugiau informacijos žr. tolesnėse temose:</span><span class="sxs-lookup"><span data-stu-id="55184-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="55184-124">Finansinio laikotarpio uždarymo darbo sritis</span><span class="sxs-lookup"><span data-stu-id="55184-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="55184-125">Uždarymas metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="55184-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="55184-126">Masinis finansinio laikotarpio uždarymas</span><span class="sxs-lookup"><span data-stu-id="55184-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)




