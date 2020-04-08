---
title: Nustatyti garantinio rašto banko priemones ir registravimo šablonus
description: Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff5402b11cd2ccdfde2881268d9cd936947cd77e
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144257"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="be874-103">Nustatyti garantinio rašto banko priemones ir registravimo šablonus</span><span class="sxs-lookup"><span data-stu-id="be874-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be874-104">Ši užduotis sukuria banko priemonės ir registravimo šabloną, reikalingą norint apdoroti garantinį raštą.</span><span class="sxs-lookup"><span data-stu-id="be874-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="be874-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="be874-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="be874-106">Didžiosios knygos parametras</span><span class="sxs-lookup"><span data-stu-id="be874-106">General ledger parameter</span></span>
1. <span data-ttu-id="be874-107">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="be874-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="be874-108">Išplėskite skyrių Banko dokumentas.</span><span class="sxs-lookup"><span data-stu-id="be874-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="be874-109">Pasirinkite parinktį Įjungti garantinį raštą.</span><span class="sxs-lookup"><span data-stu-id="be874-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="be874-110">Lauke Operacijų žurnalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="be874-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="be874-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="be874-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="be874-112">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="be874-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="be874-113">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="be874-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="be874-114">Garantinio rašto numerio ir garantinio rašto operacijos nuorodų numeracijos kodo nustatymas</span><span class="sxs-lookup"><span data-stu-id="be874-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="be874-115">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="be874-115">Click Save.</span></span>
9. <span data-ttu-id="be874-116">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="be874-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="be874-117">Banko priemonės kūrimas</span><span class="sxs-lookup"><span data-stu-id="be874-117">Create Bank facility</span></span>
1. <span data-ttu-id="be874-118">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko priemonės.</span><span class="sxs-lookup"><span data-stu-id="be874-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="be874-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="be874-119">Click New.</span></span>
3. <span data-ttu-id="be874-120">Lauke Priemonių grupė įveskite garantinio rašto operacijos banko priemonių grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="be874-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="be874-121">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="be874-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="be874-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="be874-122">Click Save.</span></span>
6. <span data-ttu-id="be874-123">Spustelėkite skirtuką Paslaugų tipai.</span><span class="sxs-lookup"><span data-stu-id="be874-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="be874-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="be874-124">Click New.</span></span>
8. <span data-ttu-id="be874-125">Lauke Priemonės tipas įveskite banko priemonės tipo, kuris yra susijęs su banko priemonės sutartimi, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="be874-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="be874-126">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="be874-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="be874-127">Lauke Priemonių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="be874-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="be874-128">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="be874-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="be874-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="be874-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="be874-130">Lauke Priemonės pobūdis pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="be874-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="be874-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="be874-131">Click Save.</span></span>
15. <span data-ttu-id="be874-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="be874-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="be874-133">Banko registravimo šablonas</span><span class="sxs-lookup"><span data-stu-id="be874-133">Bank posting profile</span></span>
1. <span data-ttu-id="be874-134">Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymai > Banko dokumentų registravimo šablonas.</span><span class="sxs-lookup"><span data-stu-id="be874-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="be874-135">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="be874-135">Click New.</span></span>
3. <span data-ttu-id="be874-136">Lauke Sąskaitos / grupės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="be874-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="be874-137">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="be874-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="be874-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="be874-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="be874-139">Lauke Sudengimo sąskaita pasirinkite pagrindinę sudengimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="be874-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="be874-140">Lauke Išlaidų sąskaita pasirinkite išlaidų operacijų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="be874-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="be874-141">Lauke Maržos sąskaita pasirinkite maržos operacijos sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="be874-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="be874-142">Lauke Likvidavimo sąskaita pasirinkite garantinio rašto operacijos likvidavimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="be874-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="be874-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="be874-143">Click Save.</span></span>
11. <span data-ttu-id="be874-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="be874-144">Close the page.</span></span>

