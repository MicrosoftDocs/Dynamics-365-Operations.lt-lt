---
title: 'ER: mokėjimų elektroninių dokumentų generavimas naudojant formato konfigūraciją'
description: Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali naudodamas naują elektroninių ataskaitų (ER) formato konfigūraciją generuoti elektroninius mokėjimų apdorojimo dokumentus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e88df5c2f92ee2b9b448ba100c8bc4105eddae4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681738"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="63acd-103">ER: mokėjimų elektroninių dokumentų generavimas naudojant formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="63acd-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63acd-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali naudodamas naują elektroninių ataskaitų (ER) formato konfigūraciją generuoti elektroninius mokėjimų apdorojimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="63acd-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="63acd-105">Šiuos veiksmus galima atlikti pavyzdinėje įmonėje GBSI.</span><span class="sxs-lookup"><span data-stu-id="63acd-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="63acd-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „Mokėjimo dokumento formato konfigūracijos kūrimas“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="63acd-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="63acd-107">Elektroninio mokėjimo būdo konfigūracijos keitimas</span><span class="sxs-lookup"><span data-stu-id="63acd-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="63acd-108">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="63acd-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="63acd-109">Jei reikia, dalį Failo formatas išskleisite ją perjungdami.</span><span class="sxs-lookup"><span data-stu-id="63acd-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="63acd-110">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="63acd-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="63acd-111">Pvz., filtruokite lauką Mokėjimo būdas reikšme „Elektroninis“.</span><span class="sxs-lookup"><span data-stu-id="63acd-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="63acd-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="63acd-112">Click Edit.</span></span>
5. <span data-ttu-id="63acd-113">Lauką Bendrosios elektroninės ataskaitos nustatykite į Taip.</span><span class="sxs-lookup"><span data-stu-id="63acd-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="63acd-114">Pasirinkite Taip, kad generuoti mokėjimo failams naudotumėte šabloną Bendrosios elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="63acd-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="63acd-115">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="63acd-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="63acd-116">Pasirinkite BACS (JK fiktyvus) formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="63acd-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="63acd-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63acd-117">Click Save.</span></span>
9. <span data-ttu-id="63acd-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="63acd-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="63acd-119">Sugeneruotų mokėjimo failų formato tikrinimas</span><span class="sxs-lookup"><span data-stu-id="63acd-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="63acd-120">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="63acd-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="63acd-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63acd-121">Click New.</span></span>
3. <span data-ttu-id="63acd-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="63acd-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="63acd-123">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="63acd-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="63acd-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="63acd-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="63acd-125">Pasirinkite „VendPay‟.</span><span class="sxs-lookup"><span data-stu-id="63acd-125">Select VendPay.</span></span>  
6. <span data-ttu-id="63acd-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63acd-126">Click Save.</span></span>
7. <span data-ttu-id="63acd-127">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="63acd-127">Click Lines.</span></span>
8. <span data-ttu-id="63acd-128">Lauke Įmonė įveskite„DEMF‟.</span><span class="sxs-lookup"><span data-stu-id="63acd-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="63acd-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="63acd-129">DEMF</span></span>  
9. <span data-ttu-id="63acd-130">Lauke „Sąskaita“ nustatykite reikšmes „DE-01001“.</span><span class="sxs-lookup"><span data-stu-id="63acd-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="63acd-131">DE – 01001</span><span class="sxs-lookup"><span data-stu-id="63acd-131">DE-01001</span></span>  
10. <span data-ttu-id="63acd-132">Lauke Aprašas įveskite „Mokėjimas‟.</span><span class="sxs-lookup"><span data-stu-id="63acd-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="63acd-133">Mokėjimas</span><span class="sxs-lookup"><span data-stu-id="63acd-133">Payment</span></span>  
11. <span data-ttu-id="63acd-134">Lauke Debetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="63acd-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="63acd-135">1000</span><span class="sxs-lookup"><span data-stu-id="63acd-135">1000</span></span>  
12. <span data-ttu-id="63acd-136">Spustelėkite skirtuką Mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="63acd-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="63acd-137">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="63acd-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="63acd-138">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="63acd-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="63acd-139">Pasirinkite reikšmę Elektroninis.</span><span class="sxs-lookup"><span data-stu-id="63acd-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="63acd-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="63acd-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="63acd-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63acd-141">Click Save.</span></span>
17. <span data-ttu-id="63acd-142">Spustelėkite Generuoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="63acd-142">Click Generate payments.</span></span>
18. <span data-ttu-id="63acd-143">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="63acd-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="63acd-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="63acd-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="63acd-145">Pasirinkite reikšmę Elektroninis.</span><span class="sxs-lookup"><span data-stu-id="63acd-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="63acd-146">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="63acd-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="63acd-147">Pasirinkite reikšmę Elektroninis.</span><span class="sxs-lookup"><span data-stu-id="63acd-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="63acd-148">Lauke „Failo pavadinimas“ suveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="63acd-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="63acd-149">Pavyzdžiui, įveskite „mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="63acd-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="63acd-150">Lauke Banko sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="63acd-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="63acd-151">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="63acd-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="63acd-152">Pasirinkite reikšmę GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="63acd-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="63acd-153">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="63acd-153">Click OK.</span></span>
25. <span data-ttu-id="63acd-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="63acd-154">Click OK.</span></span>
    * <span data-ttu-id="63acd-155">Sukurtą mokėjimo failą analizuokite XML formatu.</span><span class="sxs-lookup"><span data-stu-id="63acd-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="63acd-156">Jį palyginkite su sukurtu dokumento maketu ir apibrėžtais mokėjimo operacijų atributais.</span><span class="sxs-lookup"><span data-stu-id="63acd-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

