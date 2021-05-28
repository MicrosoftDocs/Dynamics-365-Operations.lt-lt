---
title: Nustatykite TDS įstaigos mokėjimų mokėjimo mokesčius
description: Šioje temoje paaiškinama, kaip nustatyti mokėjimo mokesčius, kurie taikomi šaltinio (TDS) valdžios institucijos mokėjimams.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023463"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="80608-103">Nustatykite TDS įstaigos mokėjimų mokėjimo mokesčius</span><span class="sxs-lookup"><span data-stu-id="80608-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80608-104">Šioje temoje paaiškinama, kaip nustatyti mokėjimo mokesčius, kurie taikomi šaltinio (TDS) valdžios institucijos mokėjimams.</span><span class="sxs-lookup"><span data-stu-id="80608-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="80608-105">Pasirinkite **Mokėtinos sumos \> Mokėjimų sąranka \> Mokėjimo mokestis**.</span><span class="sxs-lookup"><span data-stu-id="80608-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="80608-106">[![Mokėjimo mokesčio puslapis](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="80608-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="80608-107">Rinkitės **Nauja** norėdami sukurti mokėjimo mokestį ir įveskite reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="80608-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="80608-108">Lauke **Mokesčio tipas** pasirinkite mokesčio atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="80608-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="80608-109">**None**</span><span class="sxs-lookup"><span data-stu-id="80608-109">**None**</span></span>
    - <span data-ttu-id="80608-110">**Palūkanos** – skaičiuojamos pavėluotų mokėjimų, kurie atliekami TDS institucijos tiekėjui, palūkanos.</span><span class="sxs-lookup"><span data-stu-id="80608-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="80608-111">**Kiti** – skaičiuojamos kiti mokesčiai, kurie atliekami TDS institucijos tiekėjui, palūkanos.</span><span class="sxs-lookup"><span data-stu-id="80608-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="80608-112">Jei pasirenkate **Palūkanos** arba **Kita**, laukas mokestis automatiškai **nustatomas** į **DK**.</span><span class="sxs-lookup"><span data-stu-id="80608-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="80608-113">Jei pasirinkote **Palūkanos** arba **Kita** lauke **Lauko tipas** laukelyje **Pagrindinė sąskaita** rinkitės DK, į kurią registruosite palūkanas ir kitas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="80608-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="80608-114">Įveskite kitą reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="80608-114">Enter the other required details.</span></span>
6. <span data-ttu-id="80608-115">Veiksmų juostoje rinkitės **Mokesčio mokėjimo nustatymas** norėdami atverti **Mokesčio nustatymą** puslapį, kuriame galite nustatyti įvairių bankų, mokėjimo būdų, mokėjimo specifikacijų, valiutų ir datos intervalų mokėjimo mokesčius.</span><span class="sxs-lookup"><span data-stu-id="80608-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="80608-116">[![Mokėjimo mokesčių puslapis](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="80608-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="80608-117">Lauko **Grupavimai** skirtuke **Peržiūra** nurodykite, kuriems bankams nustatote mokėjimo mokestį:</span><span class="sxs-lookup"><span data-stu-id="80608-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="80608-118">**Lentelė** – mokestis taikomas konkrečiai banko sąskaitai.</span><span class="sxs-lookup"><span data-stu-id="80608-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="80608-119">**Grupė** – mokestis taikomas konkrečiai banko grupei.</span><span class="sxs-lookup"><span data-stu-id="80608-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="80608-120">**Visi** – Mokestis galioja visoms banko sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="80608-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="80608-121">Jei pasirinkote **Lentelė** ar **Grupė** lauke **Grupavimas** laukelyje **Banko ataskaita** pasirinkite konkrečią banko sąskaitą ar grupę, kurios mokėjimo mokestį nustatote.</span><span class="sxs-lookup"><span data-stu-id="80608-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="80608-122">Lauke **Mokėjimo būdas** pasirinkite dabartinio mokesčio mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="80608-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="80608-123">Mokėjimo specifikacijos **lauke pasirinkite** arba įveskite mokėjimo specifikacijos kodą, kuris buvo sugeneruotas **mokėjimo specifikacijos** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="80608-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="80608-124">Mokėjimo specifikacija naudojama su elektroniniais mokėjimo lėšų pervedimo būdais.</span><span class="sxs-lookup"><span data-stu-id="80608-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="80608-125">Lauke **Mokėjimo valiuta** pasirinkite mokesčio valiutą, kuri įjungia mokestį.</span><span class="sxs-lookup"><span data-stu-id="80608-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="80608-126">Tik operacijos, kurios naudoja pasirinktą valiutą, gali suaktyvinti mokestį.</span><span class="sxs-lookup"><span data-stu-id="80608-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="80608-127">Jei paliksite šį lauką tuščią, mokestį suaktyvins visos valiutos.</span><span class="sxs-lookup"><span data-stu-id="80608-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="80608-128">Lauke **Procentai/suma** pasirinkite skaičiavimo metodą.</span><span class="sxs-lookup"><span data-stu-id="80608-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="80608-129">Galimos pasirinktys: **Suma**, **Procentas** ir **Intervalas**.</span><span class="sxs-lookup"><span data-stu-id="80608-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="80608-130">Mokesčio **sumos lauke** nurodykite mokesčio sumą kaip mokėjimo procentą arba kaip vieno mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="80608-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="80608-131">Lauke **Mokesčio valiuta** nurodykite mokesčio valiutos kodą.</span><span class="sxs-lookup"><span data-stu-id="80608-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="80608-132">Pasirinkite skirtuką **Bendra**, norėdami peržiūrėti arba modifikuoti pasirinktos banko sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="80608-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="80608-133">[![Skirtukas Bendra](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="80608-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="80608-134">Lauke **Minimali** įveskite minimalią mokestį suaktyvinaą operacijos sumą.</span><span class="sxs-lookup"><span data-stu-id="80608-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="80608-135">Lauke **Maksimali** įveskite maksimalų mokestį suaktyvinaą operacijos sumą.</span><span class="sxs-lookup"><span data-stu-id="80608-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="80608-136">Laukuose **Nuo datos** ir **Iki datos** nurodykite mokesčių skaičiavimo datų diapazoną.</span><span class="sxs-lookup"><span data-stu-id="80608-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="80608-137">Mokesčio **Minimalus mokestis** nurodykite mokesčio sumą kaip mokėjimo procentą arba kaip vieno mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="80608-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="80608-138">Lauke **PVM grupė** pasirinkite PVM grupę, kurią naudosite skaičiuodami mokesčio sumos PVM.</span><span class="sxs-lookup"><span data-stu-id="80608-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="80608-139">Lauke **Prekės PVM grupė** pasirinkite prekės PVM grupę, kurią naudosite skaičiuodami prekės mokesčio sumos PVM.</span><span class="sxs-lookup"><span data-stu-id="80608-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="80608-140">Pasirinkite skirtuką **Intervalas**.</span><span class="sxs-lookup"><span data-stu-id="80608-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="80608-141">[![Skirtukas Intervalas](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="80608-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="80608-142">Laukelyje **Dienos** įveskite dienų tarp mokesčio registravimo datos (nuolaidos datos) ir paprastojo vekselio termino skaičių.</span><span class="sxs-lookup"><span data-stu-id="80608-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="80608-143">Lauke **Procentai/suma** pasirinkite ar specifikacija yra procentas, ar nustatyta suma.</span><span class="sxs-lookup"><span data-stu-id="80608-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="80608-144">Mokesčio **Mokesčio suma** įveskite mokesčio sumą kaip mokėjimo procentą arba kaip vieno mokėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="80608-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="80608-145">Uždarykite mokėjimo **mokesčio nustatymo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="80608-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="80608-146">Uždarykite **mokėjimo mokesčio** puslapį.</span><span class="sxs-lookup"><span data-stu-id="80608-146">Close the **Payment fee** page.</span></span>
