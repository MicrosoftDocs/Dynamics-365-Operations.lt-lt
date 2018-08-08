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
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4c36d938000fdb70fd4fbedb1e05b0c8a5350fac
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="febbb-103">Nustatyti garantinio rašto banko priemones ir registravimo šablonus</span><span class="sxs-lookup"><span data-stu-id="febbb-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="febbb-104">Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.</span><span class="sxs-lookup"><span data-stu-id="febbb-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="febbb-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="febbb-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="febbb-106">Didžiosios knygos parametras</span><span class="sxs-lookup"><span data-stu-id="febbb-106">General ledger parameter</span></span>
1. <span data-ttu-id="febbb-107">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="febbb-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="febbb-108">Išplėskite skyrių Banko dokumentas.</span><span class="sxs-lookup"><span data-stu-id="febbb-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="febbb-109">Pasirinkite parinktį Įjungti garantinį raštą.</span><span class="sxs-lookup"><span data-stu-id="febbb-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="febbb-110">Lauke Operacijų žurnalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="febbb-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="febbb-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="febbb-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="febbb-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="febbb-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="febbb-113">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="febbb-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="febbb-114">Garantinio rašto numerio ir garantinio rašto operacijos nuorodų numeracijos kodo nustatymas</span><span class="sxs-lookup"><span data-stu-id="febbb-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="febbb-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="febbb-115">Click Save.</span></span>
9. <span data-ttu-id="febbb-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="febbb-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="febbb-117">Banko priemonės kūrimas</span><span class="sxs-lookup"><span data-stu-id="febbb-117">Create Bank facility</span></span>
1. <span data-ttu-id="febbb-118">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko priemonės.</span><span class="sxs-lookup"><span data-stu-id="febbb-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="febbb-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="febbb-119">Click New.</span></span>
3. <span data-ttu-id="febbb-120">Lauke Priemonių grupė įveskite garantinio rašto operacijos banko priemonių grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="febbb-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="febbb-121">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="febbb-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="febbb-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="febbb-122">Click Save.</span></span>
6. <span data-ttu-id="febbb-123">Spustelėkite skirtuką Paslaugų tipai.</span><span class="sxs-lookup"><span data-stu-id="febbb-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="febbb-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="febbb-124">Click New.</span></span>
8. <span data-ttu-id="febbb-125">Lauke Priemonės tipas įveskite banko priemonės tipo, kuris yra susijęs su banko priemonės sutartimi, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="febbb-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="febbb-126">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="febbb-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="febbb-127">Lauke Priemonių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="febbb-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="febbb-128">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="febbb-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="febbb-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="febbb-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="febbb-130">Lauke Priemonės pobūdis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="febbb-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="febbb-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="febbb-131">Click Save.</span></span>
15. <span data-ttu-id="febbb-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="febbb-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="febbb-133">Banko registravimo šablonas</span><span class="sxs-lookup"><span data-stu-id="febbb-133">Bank posting profile</span></span>
1. <span data-ttu-id="febbb-134">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko dokumentų registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="febbb-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="febbb-135">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="febbb-135">Click New.</span></span>
3. <span data-ttu-id="febbb-136">Lauke Sąskaitos / grupės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="febbb-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="febbb-137">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="febbb-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="febbb-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="febbb-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="febbb-139">Lauke Sudengimo sąskaita pasirinkite pagrindinę sudengimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="febbb-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="febbb-140">Lauke Išlaidų sąskaita pasirinkite išlaidų operacijų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="febbb-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="febbb-141">Lauke Maržos sąskaita pasirinkite maržos operacijos sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="febbb-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="febbb-142">Lauke Likvidavimo sąskaita pasirinkite garantinio rašto operacijos likvidavimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="febbb-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="febbb-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="febbb-143">Click Save.</span></span>
11. <span data-ttu-id="febbb-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="febbb-144">Close the page.</span></span>


