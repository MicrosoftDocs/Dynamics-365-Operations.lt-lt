---
title: Prekių, kurioms įjungta patobulinto sandėliavimo funkcija, registravimas naudojant prekių gavimo žurnalą
description: Šioje temoje pateikiamas scenarijus, kaip registruoti prekes naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830839"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="fb1f1-103">Prekių, kurioms įjungta patobulinto sandėliavimo funkcija, registravimas naudojant prekių gavimo žurnalą</span><span class="sxs-lookup"><span data-stu-id="fb1f1-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fb1f1-104">Šioje temoje pateikiamas scenarijus, kaip registruoti prekes naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="fb1f1-105">Paprastai tai atlieka gavimo klerkas.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="fb1f1-106">Duomenų pavyzdžių įgalinimas</span><span class="sxs-lookup"><span data-stu-id="fb1f1-106">Enable sample data</span></span>

<span data-ttu-id="fb1f1-107">Norėdami dirbti pagal šį scenarijų naudojant šioje temoje nurodytus pavyzdinius įrašus ir reikšmes, turite naudoti sistemą, kurioje įdiegti standartiniai demonstraciniai duomenys, ir pasirinkti *„USMF”* juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="fb1f1-108">Vietoj to, galite dirbti pagal šį scenarijų pakeisdami reikšmes iš jūsų duomenų, jeigu turite šiuos duomenis:</span><span class="sxs-lookup"><span data-stu-id="fb1f1-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="fb1f1-109">Turite patvirtintą pirkimo užsakymą su atvira pirkimo užsakymo eilute.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="fb1f1-110">Prekė eilutėje turi būti laikoma atsargose.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-110">The item on the line must be stocked.</span></span> <span data-ttu-id="fb1f1-111">Ji neturi naudoti produkto variantų ir turėti sekimo dimensijų.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="fb1f1-112">Prekė turi būti susieta su saugojimo dimensijų grupe, kurioje įgalintas sandėlio valdymo procesas.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="fb1f1-113">Naudojamame sandėlyje turi būti įgalinti sandėlio valdymo procesai, o vieta, kurią naudojate prekių gavimui, turi būti kontroliuojama numerio lentelės.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="fb1f1-114">Prekių gavimo žurnalo antraštės, naudojančios sandėlio valdymą, kūrimas</span><span class="sxs-lookup"><span data-stu-id="fb1f1-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="fb1f1-115">Toliau pateikiamas scenarijus rodo, kaip sukurti prekių gavimo žurnalo antraštę, naudojančią sandėlio valdymą:</span><span class="sxs-lookup"><span data-stu-id="fb1f1-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="fb1f1-116">Įsitikinkite, kad jūsų sistemoje yra patvirtintas pirkimo užsakymas, atitinkantis ankstesniame skyriuje nustatytus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="fb1f1-117">Šis scenarijus naudoja įmonės pirkimo užsakymą, skirtą *„USMF”* įmonei, tiekėjo sąskaitai *1001,* sandėliui *51 su* užsakymo eilute, skirta prekės *„M9200”* numerio *10 PL* (10 padėklų).</span><span class="sxs-lookup"><span data-stu-id="fb1f1-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="fb1f1-118">Pasižymėkite pirkimo užsakymo numerį, kurį naudosite.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="fb1f1-119">Eikite į **Atsargų valdymas \> Žurnalo įrašai \> Prekių gavimas \> Prekių gavimas**.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="fb1f1-120">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="fb1f1-121">Atsidaro **Sandėlio valdymo žurnalo kūrimo** dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="fb1f1-122">Pasirinkite žurnalo pavadinimą lauke **Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="fb1f1-123">Jei naudojate *„USMF”* demonstracinius duomenis, pasirinkite *„WHS”*.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="fb1f1-124">Jei naudojate savo duomenis, jūsų pasirinktame žurnale **Tikrinti paėmimo vietą** turi būti nustatyta į *Ne* ir **Sulaikymo valdymas** taip pat nustatytas į *Ne*.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="fb1f1-125">Nustatykite **Nuoroda** į *Pirkimo užsakymas*.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="fb1f1-126">Nustatykite **Paskyros numeris** į *„1001”*.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="fb1f1-127">Nustatykite **Numeris** į pirkimo užsakymo, kurį nurodėte šiam pratimui, numerį.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="fb1f1-128">![Prekių pristatymo žurnalas](../media/item-arrival-journal-header.png "Prekių gavimo žurnalas")</span><span class="sxs-lookup"><span data-stu-id="fb1f1-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="fb1f1-129">Pasirinkite **Gerai** žurnalo antraštės sukūrimui.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="fb1f1-130">Skyriuje **Žurnalo eilutės** pasirinkite **Įtraukti eilutę** ir įveskite šiuos duomenis:</span><span class="sxs-lookup"><span data-stu-id="fb1f1-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="fb1f1-131">**Prekės numeris** – Nustatykite į *„M9200”*.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="fb1f1-132">**Saitas**, **Sandėlis** ir **Kiekis** bus nustatyti pagal atsargų operacijos duomenis 10 padėklų (1000 vnt.).</span><span class="sxs-lookup"><span data-stu-id="fb1f1-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="fb1f1-133">**Vieta** – Nustatykite į *„001”*.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="fb1f1-134">Ši konkreti vieta neseka numerio lentelių.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="fb1f1-135">![Prekių gavimo žurnalo eilutė](../media/item-arrival-journal-line.png "Prekių gavimo žurnalo eilutė")</span><span class="sxs-lookup"><span data-stu-id="fb1f1-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="fb1f1-136">Lauke **Data** nurodoma data, kada atsargose bus užregistruotas turimas šios prekės kiekis.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="fb1f1-137">Lauką **Partijos ID** užpildys sistema, jei jį galima identifikuoti pagal pateiktą informaciją.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="fb1f1-138">Kitu atveju turėsite įvesti jį patys.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="fb1f1-139">Tai yra būtinasis laukas, kuris susieja šią registraciją su konkrečia šaltinio dokumento eilute.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="fb1f1-140">Pasirinkite **Patvirtinti** veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="fb1f1-141">Patikrinama, ar žurnalas parengtas registruoti.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="fb1f1-142">Jei patikrinti nepavyksta, norint registruoti žurnalą reikia ištaisyti klaidas.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="fb1f1-143">Atsidaro **Tikrinti žurnalą** dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="fb1f1-144">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-144">Select **OK**.</span></span>
1. <span data-ttu-id="fb1f1-145">Peržiūrėkite pranešimų juostą.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-145">Review the message bar.</span></span> <span data-ttu-id="fb1f1-146">Ten turėtų būti pranešimas apie tai, kad operacija baigta.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="fb1f1-147">Veiksmų srityje pasirinkite **Skelbti**.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="fb1f1-148">Atsidaro **Skelbti žurnalą** dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="fb1f1-149">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-149">Select **OK**.</span></span>
1. <span data-ttu-id="fb1f1-150">Peržiūrėkite pranešimų juostą.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-150">Review the message bar.</span></span> <span data-ttu-id="fb1f1-151">Ten turėtų būti pranešimai apie tai, kad operacija baigta.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="fb1f1-152">Veiksmų srityje pasirinkite **Funkcijos > Produkto gavimo kvitas** tam, kad atnaujintumėte pirkimo užsakymo eilutę ir užregistruotumėte produkto gavimo kvitą.</span><span class="sxs-lookup"><span data-stu-id="fb1f1-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
