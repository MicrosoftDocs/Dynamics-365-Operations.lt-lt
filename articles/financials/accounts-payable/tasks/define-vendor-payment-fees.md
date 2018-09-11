--- 
title: "Nustatyti tiekėjo mokėjimo mokesčius"
description: "Nustatykite tiekėjų mokėjimų mokesčius."
author: abruer
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 7760bc7f33500afd374fff8e29464313854b000d
ms.contentlocale: lt-lt
ms.lasthandoff: 09/11/2018

---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="bae40-103">Nustatyti tiekėjo mokėjimo mokesčius</span><span class="sxs-lookup"><span data-stu-id="bae40-103">Define vendor payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bae40-104">Nustatykite tiekėjų mokėjimų mokesčius.</span><span class="sxs-lookup"><span data-stu-id="bae40-104">Set up vendor payment fees.</span></span> <span data-ttu-id="bae40-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="bae40-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="bae40-106">Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="bae40-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="bae40-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bae40-107">Click New.</span></span>
3. <span data-ttu-id="bae40-108">Lauke Mokesčio ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bae40-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="bae40-109">Mokesčio ID turėtų apibūdinti, kada šis mokestis bus naudojamas, pvz., „EFT_mokestis‟.</span><span class="sxs-lookup"><span data-stu-id="bae40-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="bae40-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bae40-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bae40-111">Lauke Mokesčio aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bae40-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="bae40-112">Pridėkite aprašą, kad suteiktumėte daugiau informacijos apie tai, kada mokestis taikomas.</span><span class="sxs-lookup"><span data-stu-id="bae40-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="bae40-113">Lauke Mokestis pasirinkite Tiekėjas arba Didžioji knyga.</span><span class="sxs-lookup"><span data-stu-id="bae40-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="bae40-114">DK yra naudojama, kai mokestis priskiriamas organizacijai.</span><span class="sxs-lookup"><span data-stu-id="bae40-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="bae40-115">Tiekėjas naudojamas, kai mokestis taikomas tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="bae40-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="bae40-116">Įveskite pagrindinę sąskaitą, kuriai mokestis bus priskiriamas.</span><span class="sxs-lookup"><span data-stu-id="bae40-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="bae40-117">Ši parinktis galima tik tada, kai kaip parinktis Mokestis pasirenkama Didžioji knyga.</span><span class="sxs-lookup"><span data-stu-id="bae40-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="bae40-118">Pasirinkite žurnalą, kuriame šis mokestis gali būti naudojamas.</span><span class="sxs-lookup"><span data-stu-id="bae40-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="bae40-119">Tiekėjo mokėjimo mokesčiui reikėtų pasirinkti žurnalą „Išmoka tiekėjui‟.</span><span class="sxs-lookup"><span data-stu-id="bae40-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="bae40-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bae40-120">Click Save.</span></span>
10. <span data-ttu-id="bae40-121">Spustelėkite Mokėjimo mokesčio sąranka.</span><span class="sxs-lookup"><span data-stu-id="bae40-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="bae40-122">Pereikite prie mokėjimo mokesčio sąrankos, kad apibrėžtumėte, kada mokestis turėtų pagal numatytąsias nuostatas būti taikomas jūsų pasirinktam žurnalui.</span><span class="sxs-lookup"><span data-stu-id="bae40-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="bae40-123">Pasirinkite Lentelė, Grupė arba Visi.</span><span class="sxs-lookup"><span data-stu-id="bae40-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="bae40-124">Lentelė naudojama norint pasirinkti vieną banko sąskaitą, Grupė naudojama norint pasirinkti bankų grupę, o Visi – šią mokesčio sąranką naudoti visoms banko sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="bae40-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="bae40-125">Pasirinkite banko grupę arba banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="bae40-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="bae40-126">Peržvalga rodys bankų grupę, jei pasirinkote Grupė, ir – banko sąskaitas, jei pasirinkote Lentelė.</span><span class="sxs-lookup"><span data-stu-id="bae40-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="bae40-127">Pasirinkite mokėjimo būdą, kada šis mokestis bus taikomas.</span><span class="sxs-lookup"><span data-stu-id="bae40-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="bae40-128">Pasirinkite pasirinkto mokėjimo būdo mokėjimo specifikaciją.</span><span class="sxs-lookup"><span data-stu-id="bae40-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="bae40-129">Mokėjimo specifikacija naudojama su elektroniniais mokėjimo lėšų pervedimo būdais.</span><span class="sxs-lookup"><span data-stu-id="bae40-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="bae40-130">Pasirinkite, ar mokestis yra procentas, suma, ar intervalas.</span><span class="sxs-lookup"><span data-stu-id="bae40-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="bae40-131">Įveskite mokesčio procentą arba sumą.</span><span class="sxs-lookup"><span data-stu-id="bae40-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="bae40-132">Jei mokestis yra procentas, įveskite tą procentą.</span><span class="sxs-lookup"><span data-stu-id="bae40-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="bae40-133">Jei mokestis yra suma, įveskite mokesčio sumą.</span><span class="sxs-lookup"><span data-stu-id="bae40-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="bae40-134">Jei mokestis yra intervalas, naudokite skirtuką Intervalas, kad apibrėžtumėte pakopinius mokesčius.</span><span class="sxs-lookup"><span data-stu-id="bae40-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="bae40-135">Lauke Mokesčio valiuta pasirinkite valiutą, kuria mokestis bus taikomas.</span><span class="sxs-lookup"><span data-stu-id="bae40-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="bae40-136">Tai – mokesčio valiuta.</span><span class="sxs-lookup"><span data-stu-id="bae40-136">This currency is for the fee.</span></span> <span data-ttu-id="bae40-137">Mokėjimo valiuta naudojama apibrėžti, kada mokesčių taisyklė turėtų būti taikoma pagal mokėjimo valiutą.</span><span class="sxs-lookup"><span data-stu-id="bae40-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="bae40-138">Pvz., bankas gali taikyti mokestį, kai mokėjimas atliekamas eurais, tačiau visiems kitiems mokėjimams mokestis netaikomas.</span><span class="sxs-lookup"><span data-stu-id="bae40-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="bae40-139">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bae40-139">Click Save.</span></span>


