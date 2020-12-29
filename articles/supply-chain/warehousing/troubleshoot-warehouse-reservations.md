---
title: Sandėlio valdymo rezervacijų trikčių šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio rezervacijoms „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645125"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="fe8d1-103">Sandėlio valdymo rezervacijų trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe8d1-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio rezervacijoms „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="fe8d1-105">Gaunu tolesnį klaidos pranešimą: „Rezervacijų negalima panaikinti dėl to, kad sukurtas darbas remiasi rezervacijomis.“</span><span class="sxs-lookup"><span data-stu-id="fe8d1-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe8d1-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-106">Issue description</span></span>

<span data-ttu-id="fe8d1-107">Negalite atrezrervuoti inventoriaus pardavimo eilutėje, nes eilutei yra atvertas darbas.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe8d1-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-108">Issue resolution</span></span>

<span data-ttu-id="fe8d1-109">Nustatykite, ar atviro pakavimo grupės darbas yra skirtas siekiant perkelti prekę iš pakavimo stoties į kitą stotį (tokią kaip *Baydoor*).</span><span class="sxs-lookup"><span data-stu-id="fe8d1-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="fe8d1-110">Peržiūrėkite įrašus **Darbo sukūrimo istorijos žurnale** ir **Išsamios darbo informacijos** puslapiuose siekiant nustatyti, kas fiziškai rezervuoja inventorių ir tada užbaikite bei panaikinkite darbą siekiant atlaisvinti rezervaciją.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="fe8d1-111">Gaunu tolesnį klaidos pranešimą: „Inventoriaus kiekis -%1 negali būti atnaujintas dėl nepakankamų inventoriaus perlaidų prekei %2...."</span><span class="sxs-lookup"><span data-stu-id="fe8d1-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe8d1-112">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-112">Issue description</span></span>

<span data-ttu-id="fe8d1-113">Ši klaida gali įvykti, jei sistema negali atnaujinti inventoriaus kiekio dėl to, kad nesama pakankamai inventoriaus perlaidų, turinčių nurodytus matmenis.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="fe8d1-114">Štai visas klaidos pranešimo tekstas:</span><span class="sxs-lookup"><span data-stu-id="fe8d1-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="fe8d1-115">Inventoriaus kiekis -%1 negali būti naujinamas dėl nepakankamų inventoriaus perlaidų prekei %2 su matmenimis Dydis=%3, Spalva=%4, Prieda=%5, Saitas=%6, Sandėlis=%7, Vieta=%8, Inventoriaus būsena=Prieinamas, Licensijos plokštelė=%9, Palaido kiekio numeris=%10 ataskaitos ID %11 partijos ID %12.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe8d1-116">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-116">Issue resolution</span></span>

<span data-ttu-id="fe8d1-117">Įsitikinkite, kad nėra jokių inventoriaus perlaidų, kurios fiziškai rezervuoja kiekį.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="fe8d1-118">Pavyzdžiui, šios perlaidos gali atverti kiekio užsakymus, inventoriaus blokavimo įrašus ar išvesties užsakymus.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="fe8d1-119">Gaunu tolesnį klaidos pranešimą: „Fiziškai turima...negalima rezervuoti dėl to, kad tik 0,00 yra prieinama inventoriuje."</span><span class="sxs-lookup"><span data-stu-id="fe8d1-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe8d1-120">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-120">Issue description</span></span>

<span data-ttu-id="fe8d1-121">Ši klaida gali įvykti, jei sistema negali atnaujinti inventoriaus kiekio dėl to, kad nesama pakankamai inventoriaus perlaidų, turinčių nurodytus matmenis.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="fe8d1-122">Štai visas klaidos pranešimo tekstas:</span><span class="sxs-lookup"><span data-stu-id="fe8d1-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="fe8d1-123">Fiziškai turima Saitas=%1, Sandėlis=%2, Inventoriaus būsena=Prieinama, Palaido kiekio numeris=%3, Savininkas=%4: %5 negalima rezervuoti, nes tik 0.00 yra prieinama inventoriuje.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe8d1-124">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-124">Issue resolution</span></span>

<span data-ttu-id="fe8d1-125">Šią klaidą greičiausiai sukelia atviras darbas.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="fe8d1-126">Pabaikite darbą arba gaukite nesukūrę darbo.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="fe8d1-127">Įsitikinkite, kad nėra jokių inventoriaus perlaidų, kurios fiziškai rezervuoja kiekį.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="fe8d1-128">Pavyzdžiui, šios perlaidos gali būti atviri kiekio užsakymai, inventoriaus blokavimo įrašai ar išvesties užsakymai.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="fe8d1-129">Gaunu tolesnį klaidos pranešimą: „Tam kad būtų priskirtos prie bangos, krovinio eilutės turi nurodyti matmenis virš vietos.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="fe8d1-130">Norėdami priskirti šiuos matmenis, rezervuokite ir iš naujo sukurkite krovinio eilutę."</span><span class="sxs-lookup"><span data-stu-id="fe8d1-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="fe8d1-131">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-131">Issue description</span></span>

<span data-ttu-id="fe8d1-132">Jums naudojant prekę, kuri turi „palaidas kiekis aukščiau“ rezervacijos hierarchiją (su **Palaido kiekio** matmenimis esančiais *virš* tos **Vietos** matmenų), **Paleista į sandėlį** komanda **Įkelti suplanuotą darbo slenkstį** puslapyje daliniam kiekiui neveikia.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="fe8d1-133">Gaunate šį klaidos pranešimą ir joks darbas nesukuriamas daliniam kiekiui.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="fe8d1-134">Nepaisant to, jei naudojant prekę, kuri turi „palaidas kiekis žemiau“ rezervacijos hierarchiją (su **Palaido kiekio** matmenimis esančiais *žemiau* tos **Vietos** matmenų), ygalite atlaisvinti krovinį nuo **Įkelti suplanuotą darbo slenkstį** puslapyje daliniam kiekiui neveikia.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="fe8d1-135">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="fe8d1-135">Issue resolution</span></span>

<span data-ttu-id="fe8d1-136">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-136">This behavior is by design.</span></span> <span data-ttu-id="fe8d1-137">Jei padedate matmenis virš **Vietos** matmens rezervacijos hierarchijoje, jis turi būti nurodytas prieš paleidžiant į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="fe8d1-138">„Microsoft“ įvertino šią klaidą ir nustatė, kad jos funkcijos apribojimai išleidžiami į sandėlį iš krovinio planavimo darbo slenksčio.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="fe8d1-139">Daliniai kiekiai negali būti išleisti, jei vieneri ar keli matmenys virš **Vietos** nenurodyti.</span><span class="sxs-lookup"><span data-stu-id="fe8d1-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="fe8d1-140">Dėl išsamesnės informacijos, žr. [Lanksti sandėlio lygmens matmenų rezervacijos politika](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="fe8d1-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
