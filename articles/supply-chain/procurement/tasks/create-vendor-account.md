--- 
title: "Tiekėjo sąskaitos kūrimas"
description: "Ši procedūra nurodo, kaip sukurti tiekėjo sąskaitą ir įtraukti adresą bei kontaktinę informaciją."
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e978b7c0add7b262ee7d3dbcf1da8648350ea8f5
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-vendor-account"></a><span data-ttu-id="591ad-103">Tiekėjo sąskaitos kūrimas</span><span class="sxs-lookup"><span data-stu-id="591ad-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="591ad-104">Ši procedūra nurodo, kaip sukurti tiekėjo sąskaitą ir įtraukti adresą bei kontaktinę informaciją.</span><span class="sxs-lookup"><span data-stu-id="591ad-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="591ad-105">Procedūra nenurodo, kaip užpildyti visus laukus, pirkimo ir finansiniais sumetimais.</span><span class="sxs-lookup"><span data-stu-id="591ad-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="591ad-106">Jei norite apie šiuos laukus sužinoti daugiau, prašome perskaityti laukų aprašus.</span><span class="sxs-lookup"><span data-stu-id="591ad-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="591ad-107">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="591ad-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="591ad-108">Tiekėjų sąskaitas paprastai kuria profesionalūs už pirkimus ar gautinas sumas atsakingi darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="591ad-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="591ad-109">Tiekėjo sąskaitos kūrimas</span><span class="sxs-lookup"><span data-stu-id="591ad-109">Create a vendor account</span></span>
1. <span data-ttu-id="591ad-110">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Tiekėjai > Visi tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="591ad-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="591ad-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="591ad-111">Click New.</span></span>
3. <span data-ttu-id="591ad-112">Lauke Tiekėjo sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="591ad-113">Reikšmė gali būti įvesta automatiškai.</span><span class="sxs-lookup"><span data-stu-id="591ad-113">The value may be populated automatically.</span></span> <span data-ttu-id="591ad-114">Tokiu atveju šį veiksmą galite praleisti.</span><span class="sxs-lookup"><span data-stu-id="591ad-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="591ad-115">Galite kurti tiekėjo sąskaitas asmeniui arba organizacijai.</span><span class="sxs-lookup"><span data-stu-id="591ad-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="591ad-116">Nuo to priklausys, kuriuos laukus bus galima naudoti.</span><span class="sxs-lookup"><span data-stu-id="591ad-116">This will affect which fields are available.</span></span> <span data-ttu-id="591ad-117">Šiame pavyzdyje sukursime organizacijos tiekėjo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="591ad-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="591ad-118">Lauke Pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="591ad-119">Jei jūsų tiekėjas jau yra jūsų sistemoje registruota šalis, galite jį pasirinkti išplečiamojo sąrašo lauke, o nauja tiekėjo sąskaita perims jau registruotą adresą ir kontaktinę informaciją.</span><span class="sxs-lookup"><span data-stu-id="591ad-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="591ad-120">Lauke Grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="591ad-121">Tiekėjų grupė skirta sugrupuoti tiekėjams, kuriems bendri bet kurie iš šių parametrų: mokėjimo sąlygos, sudengimo laikotarpis, atsargų registravimo DK sąskaitos – įskaitant PVM grupę, numatytosios DK sąskaitos, produktų filtravimo kodai arba tiekimo prognozės konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="591ad-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="591ad-122">Lauke „Darbuotojų skaičius“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="591ad-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="591ad-123">Lauke „Organizacijos numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="591ad-124">Įtraukti adresą</span><span class="sxs-lookup"><span data-stu-id="591ad-124">Add an address</span></span>
1. <span data-ttu-id="591ad-125">Išplėskite skyrių Adresai.</span><span class="sxs-lookup"><span data-stu-id="591ad-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="591ad-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="591ad-126">Click Add.</span></span>
3. <span data-ttu-id="591ad-127">Lauke Tikslas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="591ad-128">Galite pasirinkti vieną arba kelis tikslus.</span><span class="sxs-lookup"><span data-stu-id="591ad-128">You can select one or more purposes.</span></span> <span data-ttu-id="591ad-129">Jie naudojami norint pasirinkti tinkamą konkretaus tikslo adresą.</span><span class="sxs-lookup"><span data-stu-id="591ad-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="591ad-130">Pavyzdžiui, jei tikslas yra „Sąskaita faktūra“, tas adresas bus naudojamas siunčiant sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="591ad-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="591ad-131">Lauke Pavadinimas arba aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="591ad-132">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="591ad-133">Įveskite adreso informaciją.</span><span class="sxs-lookup"><span data-stu-id="591ad-133">Enter the address details.</span></span> <span data-ttu-id="591ad-134">Nuo jūsų pasirinktos šalies / regiono priklausys jums rodomi laukai, atitinkantys šalies / regiono adreso formatą.</span><span class="sxs-lookup"><span data-stu-id="591ad-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="591ad-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="591ad-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="591ad-136">Įtraukti kontaktinę informaciją</span><span class="sxs-lookup"><span data-stu-id="591ad-136">Add contact information</span></span>
1. <span data-ttu-id="591ad-137">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="591ad-137">Click Add.</span></span>
2. <span data-ttu-id="591ad-138">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="591ad-139">Lauke „Tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="591ad-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="591ad-140">Lauke „Kontaktinis numeris / adresas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="591ad-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="591ad-141">Jei tai yra pirminis kontaktas, galite pažymėkite žymės langelį Pirminis.</span><span class="sxs-lookup"><span data-stu-id="591ad-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="591ad-142">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="591ad-142">Click Save.</span></span>
6. <span data-ttu-id="591ad-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="591ad-143">Close the page.</span></span>
7. <span data-ttu-id="591ad-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="591ad-144">Close the page.</span></span>


