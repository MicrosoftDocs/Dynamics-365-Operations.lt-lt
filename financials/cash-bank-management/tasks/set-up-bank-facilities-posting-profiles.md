--- 
title: "Nustatyti garantinio rašto banko priemones ir registravimo šablonus"
description: "Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą."
author: kweekley
manager: AnnBe
ms.date: 02/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c23fe66c58e9ceff74469cc8eab61eb606c57ee1
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="67e9b-103">Nustatyti garantinio rašto banko priemones ir registravimo šablonus</span><span class="sxs-lookup"><span data-stu-id="67e9b-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67e9b-104">Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="67e9b-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="67e9b-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="67e9b-106">Didžiosios knygos parametras</span><span class="sxs-lookup"><span data-stu-id="67e9b-106">General ledger parameter</span></span>
1. <span data-ttu-id="67e9b-107">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="67e9b-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="67e9b-108">Išplėskite skyrių Banko dokumentas.</span><span class="sxs-lookup"><span data-stu-id="67e9b-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="67e9b-109">Pasirinkite parinktį Įjungti garantinį raštą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="67e9b-110">Lauke Operacijų žurnalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="67e9b-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="67e9b-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="67e9b-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="67e9b-113">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="67e9b-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="67e9b-114">Garantinio rašto numerio ir garantinio rašto operacijos nuorodų numeracijos kodo nustatymas</span><span class="sxs-lookup"><span data-stu-id="67e9b-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="67e9b-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="67e9b-115">Click Save.</span></span>
9. <span data-ttu-id="67e9b-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="67e9b-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="67e9b-117">Banko priemonės kūrimas</span><span class="sxs-lookup"><span data-stu-id="67e9b-117">Create Bank facility</span></span>
1. <span data-ttu-id="67e9b-118">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko priemonės.</span><span class="sxs-lookup"><span data-stu-id="67e9b-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="67e9b-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="67e9b-119">Click New.</span></span>
3. <span data-ttu-id="67e9b-120">Lauke Priemonių grupė įveskite garantinio rašto operacijos banko priemonių grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="67e9b-121">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="67e9b-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="67e9b-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="67e9b-122">Click Save.</span></span>
6. <span data-ttu-id="67e9b-123">Spustelėkite skirtuką Paslaugų tipai.</span><span class="sxs-lookup"><span data-stu-id="67e9b-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="67e9b-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="67e9b-124">Click New.</span></span>
8. <span data-ttu-id="67e9b-125">Lauke Priemonės tipas įveskite banko priemonės tipo, kuris yra susijęs su banko priemonės sutartimi, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="67e9b-126">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="67e9b-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="67e9b-127">Lauke Priemonių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="67e9b-128">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="67e9b-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="67e9b-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="67e9b-130">Lauke Priemonės pobūdis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="67e9b-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="67e9b-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="67e9b-131">Click Save.</span></span>
15. <span data-ttu-id="67e9b-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="67e9b-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="67e9b-133">Banko registravimo šablonas</span><span class="sxs-lookup"><span data-stu-id="67e9b-133">Bank posting profile</span></span>
1. <span data-ttu-id="67e9b-134">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko dokumentų registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="67e9b-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="67e9b-135">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="67e9b-135">Click New.</span></span>
3. <span data-ttu-id="67e9b-136">Lauke Sąskaitos / grupės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="67e9b-137">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="67e9b-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="67e9b-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="67e9b-139">Lauke Sudengimo sąskaita pasirinkite pagrindinę sudengimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="67e9b-140">Lauke Išlaidų sąskaita pasirinkite išlaidų operacijų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="67e9b-141">Lauke Maržos sąskaita pasirinkite maržos operacijos sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="67e9b-142">Lauke Likvidavimo sąskaita pasirinkite garantinio rašto operacijos likvidavimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="67e9b-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="67e9b-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="67e9b-143">Click Save.</span></span>
11. <span data-ttu-id="67e9b-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="67e9b-144">Close the page.</span></span>


