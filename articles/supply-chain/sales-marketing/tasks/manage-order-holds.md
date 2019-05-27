---
title: Valdyti užsakymų sulaikymą
description: Šioje procedūroje parodoma, kaip sulaikyti kliento pardavimo užsakymus, kaip dirbti su užsakymo sulaikymo išregistravimu ir kaip pašalinti užsakymų sulaikymą.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad19ff166c15748b7bbb4b82ef71dbf3e1e8ebd2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563879"
---
# <a name="manage-order-holds"></a><span data-ttu-id="587d8-103">Valdyti užsakymų sulaikymą</span><span class="sxs-lookup"><span data-stu-id="587d8-103">Manage order holds</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="587d8-104">Šioje procedūroje parodoma, kaip sulaikyti kliento pardavimo užsakymus, kaip dirbti su užsakymo sulaikymo išregistravimu ir kaip pašalinti užsakymų sulaikymą.</span><span class="sxs-lookup"><span data-stu-id="587d8-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="587d8-105">Užsakymas gali būti sulaikytas dėl įvairių priežasčių.</span><span class="sxs-lookup"><span data-stu-id="587d8-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="587d8-106">Pavyzdžiui, galima sulaikyti užsakymą, kol bus patikrintas kliento adresas ar mokėjimo būdas arba kol vadybininkas peržiūrės kliento kredito limitą.</span><span class="sxs-lookup"><span data-stu-id="587d8-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="587d8-107">Kai užsakymas sulaikytas, negalima apdoroti siųstinų prekių.</span><span class="sxs-lookup"><span data-stu-id="587d8-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="587d8-108">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="587d8-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="587d8-109">Nustatyti užsakymų sulaikymą</span><span class="sxs-lookup"><span data-stu-id="587d8-109">Set up order holds</span></span>
1. <span data-ttu-id="587d8-110">Pasirinkite Pardavimas ir rinkodara > Sąranka > Pardavimo užsakymai > Užsakymo sulaikymo kodai.</span><span class="sxs-lookup"><span data-stu-id="587d8-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="587d8-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="587d8-111">Click New.</span></span>
3. <span data-ttu-id="587d8-112">Lauke Sulaikymo kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="587d8-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="587d8-113">Pavyzdžiui, surinkite Perskambinti.</span><span class="sxs-lookup"><span data-stu-id="587d8-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="587d8-114">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="587d8-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="587d8-115">Pavyzdžiui, užsakymas sulaikomas, nes laukiama kliento perskambinimo.</span><span class="sxs-lookup"><span data-stu-id="587d8-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="587d8-116">Norėdami iš užsakymo pašalinti visus faktinius rezervavimus, kai pridėtas šis sulaikymo kodas, pasirinktinai pažymėkite žymės langelį Pašalinti rezervavimus.</span><span class="sxs-lookup"><span data-stu-id="587d8-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="587d8-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="587d8-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="587d8-118">Sulaikyti užsakymą</span><span class="sxs-lookup"><span data-stu-id="587d8-118">Place order on hold</span></span>
1. <span data-ttu-id="587d8-119">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="587d8-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="587d8-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="587d8-120">Click New.</span></span>
3. <span data-ttu-id="587d8-121">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="587d8-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="587d8-122">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="587d8-122">Click OK.</span></span>
5. <span data-ttu-id="587d8-123">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="587d8-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="587d8-124">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="587d8-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="587d8-125">Veiksmų srityje spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="587d8-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="587d8-126">Spustelėkite Užsakymų sulaikymas.</span><span class="sxs-lookup"><span data-stu-id="587d8-126">Click Order holds.</span></span>
9. <span data-ttu-id="587d8-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="587d8-127">Click New.</span></span>
10. <span data-ttu-id="587d8-128">Lauke Sulaikymo kodas pasirinkite kodą, kurį sukūrėte ankstesnėje papildomoje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="587d8-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="587d8-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="587d8-129">Click Save.</span></span>
12. <span data-ttu-id="587d8-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="587d8-130">Close the page.</span></span>
13. <span data-ttu-id="587d8-131">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="587d8-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="587d8-132">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="587d8-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="587d8-133">Šiuo metu sulaikytų užsakymų laukai „Neapdoroti” ir „Sulaikyta” yra pažymėti.</span><span class="sxs-lookup"><span data-stu-id="587d8-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="587d8-134">Veiksmų srityje spustelėkite Paimti ir pakuoti.</span><span class="sxs-lookup"><span data-stu-id="587d8-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="587d8-135">Valdyti užsakymų sulaikymą</span><span class="sxs-lookup"><span data-stu-id="587d8-135">Manage order holds</span></span>
1. <span data-ttu-id="587d8-136">Pasirinkite Pardavimas ir rinkodara > Pardavimo užsakymai > Atviri užsakymai > Užsakymų sulaikymas.</span><span class="sxs-lookup"><span data-stu-id="587d8-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="587d8-137">Užsakymų sulaikymo puslapis veikia kaip darbastalis, kuriame galima peržiūrėti ir tvarkyti visus dabartinius ir apdorotus sulaikymus bei susijusius pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="587d8-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="587d8-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="587d8-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="587d8-139">Veiksmų srityje spustelėkite Sulaikyti pirkimo užbaigimą.</span><span class="sxs-lookup"><span data-stu-id="587d8-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="587d8-140">Spustelėkite Išregistruoti.</span><span class="sxs-lookup"><span data-stu-id="587d8-140">Click Check out.</span></span>
5. <span data-ttu-id="587d8-141">Sąraše atžymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="587d8-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="587d8-142">Išregistravimo lauke dabar rodomas jūsų vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="587d8-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="587d8-143">Spustelėkite Valyti išregistravimą.</span><span class="sxs-lookup"><span data-stu-id="587d8-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="587d8-144">Veiksmų srityje spustelėkite Išvalyti sulaikymą.</span><span class="sxs-lookup"><span data-stu-id="587d8-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="587d8-145">Turite išvalyti sulaikymą, kai būsite pasirengę jį pašalinti ir leisite tęsti kitą užsakymo vykdymo veiksmą.</span><span class="sxs-lookup"><span data-stu-id="587d8-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="587d8-146">Jei užsakymui nereikia jokių pakeitimų, galite vykdyti veiksmą Išvalyti sulaikymą.</span><span class="sxs-lookup"><span data-stu-id="587d8-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="587d8-147">Tačiau galite naudoti veiksmą Valyti ir modifikuoti, jei išvalius sulaikymą reikia atnaujinti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="587d8-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="587d8-148">Veiksmas Valyti ir pateikti taikomas tik naudojant skambučių centro funkcijas.</span><span class="sxs-lookup"><span data-stu-id="587d8-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="587d8-149">Spustelėkite Išvalyti sulaikymą.</span><span class="sxs-lookup"><span data-stu-id="587d8-149">Click Clear holds.</span></span>
    * <span data-ttu-id="587d8-150">Sulaikymas dabar išvalytas iš užsakymo ir pašalintas iš aktyvių sulaikymų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="587d8-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="587d8-151">Norėdami peržiūrėti visus sulaikymus arba jų subrinkinį pagal konkrečią būseną, pakeiskite lauko Rodyti reikšmę.</span><span class="sxs-lookup"><span data-stu-id="587d8-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

