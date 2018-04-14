--- 
title: "Nustatyti kliento mokėjimo mokesčius"
description: "Sukurkite mokėjimų klientams mokesčius."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d740ea3f9aeef9ae302fbf3f03e9ecebff24aa5d
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="d79af-103">Nustatyti kliento mokėjimo mokesčius</span><span class="sxs-lookup"><span data-stu-id="d79af-103">Establish customer payment fees</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d79af-104">Sukurkite mokėjimų klientams mokesčius.</span><span class="sxs-lookup"><span data-stu-id="d79af-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="d79af-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="d79af-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d79af-106">Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="d79af-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="d79af-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d79af-107">Click New.</span></span>
3. <span data-ttu-id="d79af-108">Lauke Mokesčio ID įveskite mokesčio ID.</span><span class="sxs-lookup"><span data-stu-id="d79af-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="d79af-109">Mokesčio ID rodomas mokėjimų žurnaluose, todėl nurodykite jį aprašomąjį, kad suprastumėte, koks mokestis nustatomas.</span><span class="sxs-lookup"><span data-stu-id="d79af-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="d79af-110">Lauke Pavadinimas įveskite mokesčio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="d79af-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="d79af-111">Lauke Mokesčio aprašas įveskite mokesčio aprašą.</span><span class="sxs-lookup"><span data-stu-id="d79af-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="d79af-112">Pasirinkite, ar mokestis bus taikomas klientui, ar DK sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="d79af-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="d79af-113">Jei mokesčiu apmokestinamas klientas, pasirinkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="d79af-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="d79af-114">Jei mokesčiu, kaip išlaidomis, bus apmokestinta jūsų organizacija, pasirinkite Didžioji knyga.</span><span class="sxs-lookup"><span data-stu-id="d79af-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="d79af-115">Šiai užduočiai atlikti pasirinkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="d79af-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="d79af-116">Pasirinkite žurnalo, kuris gali naudoti šį mokėjimo mokestį, tipą.</span><span class="sxs-lookup"><span data-stu-id="d79af-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="d79af-117">Jei šie mokesčiai naudojami klientų mokėjimams, žurnalo tipas greičiausiai bus Kliento mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="d79af-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="d79af-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d79af-118">Click Save.</span></span>
9. <span data-ttu-id="d79af-119">Spustelėkite Mokėjimo mokesčio sąranka.</span><span class="sxs-lookup"><span data-stu-id="d79af-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="d79af-120">Mokėjimo mokesčio sąranka naudojama apibrėžti kriterijams, kada mokėjimo mokesčiu bus apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="d79af-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="d79af-121">Pavyzdžiui, galite apibrėžti, kad mokestis bus skaičiuojamas, jei banko sąskaita bus USMF OPER, o mokėjimo būdas bus čekis.</span><span class="sxs-lookup"><span data-stu-id="d79af-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="d79af-122">Pasirinkite Lentelė, Grupė arba Visos, kad apibrėžtumėte, kurioms banko sąskaitoms bus taikomas šis mokestis.</span><span class="sxs-lookup"><span data-stu-id="d79af-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="d79af-123">Jei pasirenkate Visos, šiuo mokesčiu galėtų būti apmokestintos visos banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="d79af-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="d79af-124">Jei pasirenkate Lentelė, šiuo mokesčiu gali būti apmokestinta tik jūsų pasirinkta banko sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d79af-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="d79af-125">Jei pasirenkate Grupė, šiuo mokesčiu gali būti apmokestintos tik pasirinktos bankų grupės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="d79af-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="d79af-126">Pasirinkite banko grupę arba banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="d79af-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="d79af-127">Jei pasirinkote Lentelė, peržvalgoje bus rodomos banko sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="d79af-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="d79af-128">Jei pasirinkote Grupė, peržvalgoje bus rodomos bankų grupės.</span><span class="sxs-lookup"><span data-stu-id="d79af-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="d79af-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d79af-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d79af-130">Pasirinkite mokėjimo būdą, kuriam šis mokestis bus taikomas.</span><span class="sxs-lookup"><span data-stu-id="d79af-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="d79af-131">Pavyzdžiui., mokesčiu galite apmokestinti savo klientus, jei jie mokėjimus siunčia kaip čekį, o ne kaip elektroninį mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="d79af-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="d79af-132">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d79af-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="d79af-133">Jei tai aktualu, įveskite mokėjimo valiutą.</span><span class="sxs-lookup"><span data-stu-id="d79af-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="d79af-134">Mokėjimo valiuta naudojama kaip papildomas kriterijus nustatyti, ar bus taikomas mokestis.</span><span class="sxs-lookup"><span data-stu-id="d79af-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="d79af-135">Pavyzdžiui, jūsų bankas gali taikyti papildomą mokestį už mokėjimus, gautus JAV doleriais, nes jie paprastai operuoja tik eurais.</span><span class="sxs-lookup"><span data-stu-id="d79af-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="d79af-136">Pasirinkite, ar mokestis bus procentas, suma, ar intervalas.</span><span class="sxs-lookup"><span data-stu-id="d79af-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="d79af-137">Įveskite mokesčio procentą arba sumą.</span><span class="sxs-lookup"><span data-stu-id="d79af-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="d79af-138">Jei laukas Procentas / suma yra Procentas, tada čia įvesta reikšmė bus procentas.</span><span class="sxs-lookup"><span data-stu-id="d79af-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="d79af-139">Jei laukas Procentas / suma yra Suma, tada čia jūsų įvesta reikšmė bus suma.</span><span class="sxs-lookup"><span data-stu-id="d79af-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="d79af-140">Jei laukas Procentas / suma yra intervalas, naudokite skirtuką Intervalas, kad apibrėžtumėte pakopas.</span><span class="sxs-lookup"><span data-stu-id="d79af-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="d79af-141">Lauke Mokesčio valiuta pasirinkite mokesčio valiutą.</span><span class="sxs-lookup"><span data-stu-id="d79af-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="d79af-142">Tai valiuta, kuria bus sukurta mokestis.</span><span class="sxs-lookup"><span data-stu-id="d79af-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="d79af-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d79af-143">Click Save.</span></span>


