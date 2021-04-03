---
title: Pirkimo sutarties kūrimas
description: Šioje temoje aprašoma, kaip kurti pirkimo sutartį.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fb3d397b277429954ef91e13445189fe21560b6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237208"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="bd9e5-103">Pirkimo sutarties kūrimas</span><span class="sxs-lookup"><span data-stu-id="bd9e5-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd9e5-104">Šioje temoje aprašoma, kaip kurti pirkimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="bd9e5-105">Paprastai tai atlieka pirkimo vadybininkas.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="bd9e5-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="bd9e5-107">Prieš pradėdami turite nustatyti pirkimo sutarčių klasifikacijas.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="bd9e5-108">Sukūrę sutartį, galėsite ją naudoti, kai sukursite PU – pirkimo sutarties sąlygos bus nukopijuotos į antraštę ir į visas užsakymo eilutes, susijusias su šia sutartimi.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="bd9e5-109">Kurti naują pirkimo sutartį</span><span class="sxs-lookup"><span data-stu-id="bd9e5-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="bd9e5-110">Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir išteklių paskirstymas > Pirkimo sutartys > Pirkimo sutartys**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="bd9e5-111">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-111">Click **New**.</span></span>
3. <span data-ttu-id="bd9e5-112">Lauke **Tiekėjo klientas** pažymėkite išskleidžiamąjį meniu, tada pažymėkite pageidaujamo įrašo eilutę.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="bd9e5-113">Lauke **Pirkimo sutarčių klasifikacija** pažymėkite išskleidžiamąjį meniu, tada pažymėkite pageidaujamo įrašo eilutę.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="bd9e5-114">Išplėskite **Bendra** FastTab.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="bd9e5-115">Lauke **Galiojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="bd9e5-116">Ši galiojimo data bus numatytoji visose įsipareigojimų eilutėse ir nulems, kiek laiko galios kiekvienas konkretus įsipareigojimas.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="bd9e5-117">Lauke **Dokumento pavadinimas** įveskite savo pirkimo sutarties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="bd9e5-118">Palikite lauką **Numatytasis įsipareigojimas** nustatytą kaip **Produkto kiekio įsipareigojimas** (arba pakeiskite, jei nustatyta kitaip).</span><span class="sxs-lookup"><span data-stu-id="bd9e5-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="bd9e5-119">Numatytoji įsipareigojimo reikšmė nurodo jūsų parinktis sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="bd9e5-120">Jei jums reikia naujo įsipareigojimo tipo kuriant sutarties eilutes, turite pakeisti numatytąjį įsipareigojimą antraštėje.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="bd9e5-121">Yra 4 tipų įsipareigojimai: **Produkto kiekio įsipareigojimas** – skirta konkrečiam produkto kiekiui, **Produkto vertės įsipareigojimas** – skirta konkrečiai produkto sumos valiutai, **Produkto kategorijos įsipareigojimas** – skirta konkrečios valiutos sumai įsigijimo kategorijoje, kurioje suma gali būti skirta katalogo elementui arba ne katalogo elementui, **Vertės įsipareigojimas** – skirta konkrečios valiutos sumai, kurią galima užpildyti naudojant produktą arba įsigijimo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="bd9e5-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="bd9e5-123">Įtraukti įsipareigojimą</span><span class="sxs-lookup"><span data-stu-id="bd9e5-123">Add a commitment</span></span>
1. <span data-ttu-id="bd9e5-124">Pasirinkite **Pridėti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-124">Select **Add line**.</span></span>
2. <span data-ttu-id="bd9e5-125">Lauke **Elemento numeris** išplečiamajame meniu pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="bd9e5-126">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="bd9e5-127">Tai yra bendras kiekis, kurį susitarėte pirkti iš tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="bd9e5-128">Lauke **Vieneto kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="bd9e5-129">Išplėskite skyrių **Eilutės informacija** section.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="bd9e5-130">Parinktį **Maksimaliai vykdoma** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="bd9e5-131">Parinktis **Maksimaliai vykdoma** apriboja įsipareigojimų naudojimą.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="bd9e5-132">Galite pirkti iki kiekio, kuris nurodytas eilutės lauke **Kiekis**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="bd9e5-133">Įtraukti antraštės sąlygas</span><span class="sxs-lookup"><span data-stu-id="bd9e5-133">Add header conditions</span></span>
1. <span data-ttu-id="bd9e5-134">Veiksmų srityje pasirinkite **Parinktys**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="bd9e5-135">Pasirinkite **Keisti rodinį**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-135">Select **Change view**.</span></span>
3. <span data-ttu-id="bd9e5-136">Pasirinkite **Antraštės rodinys**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-136">Select **Header view**.</span></span>
4. <span data-ttu-id="bd9e5-137">Išplėskite skyrių **Sąlygos**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="bd9e5-138">Lauke **Mokėjimo metodas** išplečiamajame meniu pažymėkite pageidaujamą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="bd9e5-139">Čia pagal numatytuosius nustatymus rodomos mokėjimo sąlygos iš tiekėjo sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="bd9e5-140">Lauke **Pristatymo režimas** išplečiamajame meniu pažymėkite pageidaujamą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="bd9e5-141">Lauke **Pristatymo sąlygos** pažymėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="bd9e5-142">Patvirtinti ir aktyvinti sutartį</span><span class="sxs-lookup"><span data-stu-id="bd9e5-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="bd9e5-143">Veiksmų srityje pasirinkite **Pirkimo sutartis**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="bd9e5-144">Pasirinkite **Patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-144">Select **Confirmation**.</span></span> <span data-ttu-id="bd9e5-145">Nustatykite parinktį **Pažymėti sutartį kaip galiojančią** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="bd9e5-146">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-146">Select **OK**.</span></span>
4. <span data-ttu-id="bd9e5-147">Veiksmų srityje pasirinkite **Pirkimo sutartis**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="bd9e5-148">Pasirinkite **Pirkimo sutarties patvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="bd9e5-149">Parinktis **Peržiūrėti / spausdinti** leidžia generuoti pirkimo sutarties dokumentą, kurį galite spausdinti arba siųsti tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="bd9e5-150">Jei vėliau sutartį atnaujinsite ir iš naujo patvirtinsite, abi jos versijos bus rodomas čia.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="bd9e5-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bd9e5-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]