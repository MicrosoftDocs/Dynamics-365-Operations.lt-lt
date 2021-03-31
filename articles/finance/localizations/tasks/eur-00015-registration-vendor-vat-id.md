---
title: 'EUR-00015: tiekėjo PVM ID registravimas'
description: Šioje procedūroje parodoma, kaip įtraukti PVM registracijos ID ir neapmokestinimo kodą į tiekėjo kodą.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb72a5f187afe9ebe1081acd6fe0b039c370718e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227909"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="d37b3-103">EUR-00015: tiekėjo PVM ID registravimas</span><span class="sxs-lookup"><span data-stu-id="d37b3-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d37b3-104">Šioje procedūroje parodoma, kaip įtraukti PVM registracijos ID ir neapmokestinimo kodą į tiekėjo kodą.</span><span class="sxs-lookup"><span data-stu-id="d37b3-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="d37b3-105">Šis procesas yra panašus ir kai naudojami juridiniai subjektai bei klientai.</span><span class="sxs-lookup"><span data-stu-id="d37b3-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="d37b3-106">Prieš atlikdami šią procedūrą, turite nustatyti PVM ID.</span><span class="sxs-lookup"><span data-stu-id="d37b3-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="d37b3-107">Ši procedūra taikoma visoms Europos šalims / regionams.</span><span class="sxs-lookup"><span data-stu-id="d37b3-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="d37b3-108">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="d37b3-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="d37b3-109">Ši procedūra yra skirta duomenų valdymo administratoriui, mokėtinų sumų vadovui arba gautinų sumų vadovui.</span><span class="sxs-lookup"><span data-stu-id="d37b3-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="d37b3-110">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="d37b3-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="d37b3-111">Pasirinkite Mokėtinos sumos > Tiekėjai > Visi tiekėjai.</span><span class="sxs-lookup"><span data-stu-id="d37b3-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="d37b3-112">Sąraše raskite ir pasirinkite tiekėją DE-01001</span><span class="sxs-lookup"><span data-stu-id="d37b3-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="d37b3-113">Spustelėkite Registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="d37b3-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="d37b3-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d37b3-114">Click Add.</span></span>
5. <span data-ttu-id="d37b3-115">Pasirinkite PVM ID.</span><span class="sxs-lookup"><span data-stu-id="d37b3-115">Select VAT ID.</span></span>
6. <span data-ttu-id="d37b3-116">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d37b3-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="d37b3-117">Nurodykite pasirinkto tiekėjo PVM ID Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="d37b3-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="d37b3-118">ID turi atitikti nurodytą registracijos tipo formatą.</span><span class="sxs-lookup"><span data-stu-id="d37b3-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="d37b3-119">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="d37b3-119">Click the General tab.</span></span>
8. <span data-ttu-id="d37b3-120">Lauke Įsigalioja įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d37b3-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="d37b3-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d37b3-121">Click Save.</span></span>
10. <span data-ttu-id="d37b3-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d37b3-122">Click New.</span></span>
11. <span data-ttu-id="d37b3-123">Lauke Pavadinimas arba aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d37b3-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="d37b3-124">Pavyzdžiui, įveskite ITA.</span><span class="sxs-lookup"><span data-stu-id="d37b3-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="d37b3-125">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d37b3-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="d37b3-126">Pavyzdžiui, pasirinkite ITA.</span><span class="sxs-lookup"><span data-stu-id="d37b3-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="d37b3-127">Lauke Pagrindinis šalies pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="d37b3-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="d37b3-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d37b3-128">Click Save.</span></span>
15. <span data-ttu-id="d37b3-129">Spustelėkite skirtuką Peržiūra.</span><span class="sxs-lookup"><span data-stu-id="d37b3-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="d37b3-130">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d37b3-130">Click Add.</span></span>
17. <span data-ttu-id="d37b3-131">Lauke Registracijos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d37b3-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="d37b3-132">Pavyzdžiui, pasirinkite PVM ID.</span><span class="sxs-lookup"><span data-stu-id="d37b3-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="d37b3-133">Lauke Registracijos numeris įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d37b3-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="d37b3-134">Pavyzdžiui, nurodykite PVM ID Italijoje.</span><span class="sxs-lookup"><span data-stu-id="d37b3-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="d37b3-135">ID turi atitikti nurodytą registracijos tipo formatą.</span><span class="sxs-lookup"><span data-stu-id="d37b3-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="d37b3-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d37b3-136">Click Save.</span></span>
20. <span data-ttu-id="d37b3-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d37b3-137">Close the page.</span></span>
21. <span data-ttu-id="d37b3-138">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d37b3-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d37b3-139">Pavyzdžiui, pasirinkite DE-01001.</span><span class="sxs-lookup"><span data-stu-id="d37b3-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="d37b3-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d37b3-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="d37b3-141">Išplėskite skyrių SF ir pristatymas.</span><span class="sxs-lookup"><span data-stu-id="d37b3-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="d37b3-142">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="d37b3-142">Click Edit.</span></span>
25. <span data-ttu-id="d37b3-143">Lauke Neapmokestinimo kodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="d37b3-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="d37b3-144">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d37b3-144">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]