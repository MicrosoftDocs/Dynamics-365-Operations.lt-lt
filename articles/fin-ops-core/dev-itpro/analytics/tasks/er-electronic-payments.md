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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179e8a20dd65847f90872ae0e56b3e4991a6b00e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184996"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="0767d-103">ER: mokėjimų elektroninių dokumentų generavimas naudojant formato konfigūraciją</span><span class="sxs-lookup"><span data-stu-id="0767d-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0767d-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali naudodamas naują elektroninių ataskaitų (ER) formato konfigūraciją generuoti elektroninius mokėjimų apdorojimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="0767d-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="0767d-105">Šiuos veiksmus galima atlikti pavyzdinėje įmonėje GBSI.</span><span class="sxs-lookup"><span data-stu-id="0767d-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="0767d-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „Mokėjimo dokumento formato konfigūracijos kūrimas“ veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0767d-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="0767d-107">Elektroninio mokėjimo būdo konfigūracijos keitimas</span><span class="sxs-lookup"><span data-stu-id="0767d-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="0767d-108">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="0767d-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="0767d-109">Jei reikia, dalį Failo formatas išskleisite ją perjungdami.</span><span class="sxs-lookup"><span data-stu-id="0767d-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="0767d-110">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="0767d-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0767d-111">Pvz., filtruokite lauką Mokėjimo būdas reikšme „Elektroninis“.</span><span class="sxs-lookup"><span data-stu-id="0767d-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="0767d-112">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="0767d-112">Click Edit.</span></span>
5. <span data-ttu-id="0767d-113">Lauką Bendrosios elektroninės ataskaitos nustatykite į Taip.</span><span class="sxs-lookup"><span data-stu-id="0767d-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="0767d-114">Pasirinkite Taip, kad generuoti mokėjimo failams naudotumėte šabloną Bendrosios elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="0767d-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="0767d-115">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0767d-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0767d-116">Pasirinkite BACS (JK fiktyvus) formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="0767d-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="0767d-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0767d-117">Click Save.</span></span>
9. <span data-ttu-id="0767d-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0767d-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="0767d-119">Sugeneruotų mokėjimo failų formato tikrinimas</span><span class="sxs-lookup"><span data-stu-id="0767d-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="0767d-120">Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="0767d-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="0767d-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0767d-121">Click New.</span></span>
3. <span data-ttu-id="0767d-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0767d-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0767d-123">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0767d-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0767d-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0767d-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0767d-125">Pasirinkite „VendPay‟.</span><span class="sxs-lookup"><span data-stu-id="0767d-125">Select VendPay.</span></span>  
6. <span data-ttu-id="0767d-126">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0767d-126">Click Save.</span></span>
7. <span data-ttu-id="0767d-127">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="0767d-127">Click Lines.</span></span>
8. <span data-ttu-id="0767d-128">Lauke Įmonė įveskite„DEMF‟.</span><span class="sxs-lookup"><span data-stu-id="0767d-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="0767d-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="0767d-129">DEMF</span></span>  
9. <span data-ttu-id="0767d-130">Lauke „Sąskaita“ nustatykite reikšmes „DE-01001“.</span><span class="sxs-lookup"><span data-stu-id="0767d-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="0767d-131">DE – 01001</span><span class="sxs-lookup"><span data-stu-id="0767d-131">DE-01001</span></span>  
10. <span data-ttu-id="0767d-132">Lauke Aprašas įveskite „Mokėjimas‟.</span><span class="sxs-lookup"><span data-stu-id="0767d-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="0767d-133">Mokėjimas</span><span class="sxs-lookup"><span data-stu-id="0767d-133">Payment</span></span>  
11. <span data-ttu-id="0767d-134">Lauke Debetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0767d-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="0767d-135">1000</span><span class="sxs-lookup"><span data-stu-id="0767d-135">1000</span></span>  
12. <span data-ttu-id="0767d-136">Spustelėkite skirtuką Mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="0767d-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="0767d-137">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0767d-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="0767d-138">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0767d-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0767d-139">Pasirinkite reikšmę Elektroninis.</span><span class="sxs-lookup"><span data-stu-id="0767d-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="0767d-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0767d-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="0767d-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0767d-141">Click Save.</span></span>
17. <span data-ttu-id="0767d-142">Spustelėkite Generuoti mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="0767d-142">Click Generate payments.</span></span>
18. <span data-ttu-id="0767d-143">Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0767d-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="0767d-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0767d-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0767d-145">Pasirinkite reikšmę Elektroninis.</span><span class="sxs-lookup"><span data-stu-id="0767d-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="0767d-146">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0767d-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0767d-147">Pasirinkite reikšmę Elektroninis.</span><span class="sxs-lookup"><span data-stu-id="0767d-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="0767d-148">Lauke „Failo pavadinimas“ suveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0767d-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="0767d-149">Pavyzdžiui, įveskite „mokėjimai‟.</span><span class="sxs-lookup"><span data-stu-id="0767d-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="0767d-150">Lauke Banko sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0767d-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="0767d-151">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0767d-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0767d-152">Pasirinkite reikšmę GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="0767d-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="0767d-153">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0767d-153">Click OK.</span></span>
25. <span data-ttu-id="0767d-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0767d-154">Click OK.</span></span>
    * <span data-ttu-id="0767d-155">Sukurtą mokėjimo failą analizuokite XML formatu.</span><span class="sxs-lookup"><span data-stu-id="0767d-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="0767d-156">Jį palyginkite su sukurtu dokumento maketu ir apibrėžtais mokėjimo operacijų atributais.</span><span class="sxs-lookup"><span data-stu-id="0767d-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  

