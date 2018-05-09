--- 
title: PVM ID nustatymas
description: "Šioje procedūroje aprašomos būtinosios PVM ID registracijos sąlygos, pvz., registracijos tipo nustatymas ir jo priskyrimas registracijos kategorijai."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 139c37e3c0f2963a5199bb470a619a255bacb243
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-vat-id"></a><span data-ttu-id="133fe-103">PVM ID nustatymas</span><span class="sxs-lookup"><span data-stu-id="133fe-103">Set up VAT ID</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="133fe-104">Šioje procedūroje aprašomos būtinosios PVM ID registracijos sąlygos, pvz., registracijos tipo nustatymas ir jo priskyrimas registracijos kategorijai.</span><span class="sxs-lookup"><span data-stu-id="133fe-104">This procedure walks you through VAT ID registration prerequisites, such as setting up a registration type and assigning it to a registration category.</span></span> <span data-ttu-id="133fe-105">Žinyno temoje Registracijos ID galite rasti papildomos informacijos apie registracijos ID ir registracijos ID apdorojimą, įskaitant būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="133fe-105">You can find additional information about registration IDs and registration ID processing, including required prerequisites, in the Registration IDs help topic.</span></span> 

<span data-ttu-id="133fe-106">Čia pateikta informacija taikoma visoms Europos šalims / regionams.</span><span class="sxs-lookup"><span data-stu-id="133fe-106">The information here applies to all European countries/regions.</span></span> <span data-ttu-id="133fe-107">Užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Vokietijoje.</span><span class="sxs-lookup"><span data-stu-id="133fe-107">The task was created using the demo data company DEMF with Germany as the legal entity primary address.</span></span> <span data-ttu-id="133fe-108">Ši užduotis yra skirta sistemos administratoriams.</span><span class="sxs-lookup"><span data-stu-id="133fe-108">This task is intended for system administrators.</span></span> <span data-ttu-id="133fe-109">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="133fe-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="133fe-110">Pasirinkite Organizacijos administravimas > Visuotinė adresų knygelė > Registracijos tipai > Registracijos tipai.</span><span class="sxs-lookup"><span data-stu-id="133fe-110">Go to Organization administration > Global address book > Registration types > Registration types.</span></span>
2. <span data-ttu-id="133fe-111">Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="133fe-111">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="133fe-112">Lauke Pavadinimas įveskite VAT ID.</span><span class="sxs-lookup"><span data-stu-id="133fe-112">In the Name field, type 'VAT ID'.</span></span>
4. <span data-ttu-id="133fe-113">Lauke Aprašas įveskite PVM numeris.</span><span class="sxs-lookup"><span data-stu-id="133fe-113">In the Description field, VAT number.</span></span>
5. <span data-ttu-id="133fe-114">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę DEU</span><span class="sxs-lookup"><span data-stu-id="133fe-114">In the Country/region field, enter or select a value DEU</span></span>
6. <span data-ttu-id="133fe-115">Lauke Unikalus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="133fe-115">Select Yes in the Unique field.</span></span>
    * <span data-ttu-id="133fe-116">Pažymėkite šį žymės langelį, jei norite patikrinti, ar PVM ID yra unikalus.</span><span class="sxs-lookup"><span data-stu-id="133fe-116">Select this check box to verify if the VAT ID is unique.</span></span>  
7. <span data-ttu-id="133fe-117">Lauke Pagrindinis šalies pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="133fe-117">Select Yes in the Primary for country field.</span></span>
    * <span data-ttu-id="133fe-118">Pažymėkite šį žymės langelį, jei PVM ID turi būti taikomas visiems nurodytos šalies / regiono adresams.</span><span class="sxs-lookup"><span data-stu-id="133fe-118">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
8. <span data-ttu-id="133fe-119">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="133fe-119">Click Create.</span></span>
9. <span data-ttu-id="133fe-120">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="133fe-120">Click Add.</span></span>
10. <span data-ttu-id="133fe-121">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę ITA</span><span class="sxs-lookup"><span data-stu-id="133fe-121">In the Country/region field, enter or select a value ITA</span></span>
11. <span data-ttu-id="133fe-122">Lauke Formatas įveskite ###########.</span><span class="sxs-lookup"><span data-stu-id="133fe-122">In the Format field, type '###########'.</span></span>
    * <span data-ttu-id="133fe-123">Kai įvedate šio tipo pasirinktos šalies / regiono registracijos ID, registracijos ID bus patikrintas pagal šį formatą.</span><span class="sxs-lookup"><span data-stu-id="133fe-123">When you enter a registration ID of this type for the selected country/region, the registration ID will be verified against this format.</span></span>  
12. <span data-ttu-id="133fe-124">Pažymėkite žymės langelį Unikalus.</span><span class="sxs-lookup"><span data-stu-id="133fe-124">Select the Unique check box.</span></span>
    * <span data-ttu-id="133fe-125">Pažymėkite šį žymės langelį, jei norite patikrinti, ar PVM ID yra unikalus.</span><span class="sxs-lookup"><span data-stu-id="133fe-125">Select this check box to verify if the VAT ID is unique.</span></span>  
13. <span data-ttu-id="133fe-126">Pasirinkite žymės langelį Pirminės šalies.</span><span class="sxs-lookup"><span data-stu-id="133fe-126">Select the Primary for country check box.</span></span>
    * <span data-ttu-id="133fe-127">Pažymėkite šį žymės langelį, jei PVM ID turi būti taikomas visiems nurodytos šalies / regiono adresams.</span><span class="sxs-lookup"><span data-stu-id="133fe-127">Select this check box if the VAT ID should be effective for all addresses belonging to the specified country/region.</span></span>  
14. <span data-ttu-id="133fe-128">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="133fe-128">Click Save.</span></span>
15. <span data-ttu-id="133fe-129">Pasirinkite Organizacijos administravimas > Visuotinė adresų knygelė > Registracijos tipai > Registracijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="133fe-129">Go to Organization administration > Global address book > Registration types > Registration categories.</span></span>
16. <span data-ttu-id="133fe-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="133fe-130">Click New.</span></span>
17. <span data-ttu-id="133fe-131">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę VAT ID, DEU</span><span class="sxs-lookup"><span data-stu-id="133fe-131">In the Country/region field, enter or select a value VAT ID, DEU</span></span>
18. <span data-ttu-id="133fe-132">Lauke Registracijos kategorija pasirinkite VAT ID.</span><span class="sxs-lookup"><span data-stu-id="133fe-132">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="133fe-133">Priskirkite registracijos tipą, kurį sukūrėte anksčiau, iš anksto nustatytai registracijos kategorijai.</span><span class="sxs-lookup"><span data-stu-id="133fe-133">Assign the registration type that you created earlier to a predefined Registration category.</span></span>  
19. <span data-ttu-id="133fe-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="133fe-134">Click New.</span></span>
20. <span data-ttu-id="133fe-135">Lauke Šalis / regionas įveskite arba pasirinkite reikšmę VAT ID, ITA</span><span class="sxs-lookup"><span data-stu-id="133fe-135">In the Country/region field, enter or select a value VAT ID, ITA</span></span>
21. <span data-ttu-id="133fe-136">Lauke Registracijos kategorija pasirinkite VAT ID.</span><span class="sxs-lookup"><span data-stu-id="133fe-136">In the Registration category field, select 'VAT ID'.</span></span>
    * <span data-ttu-id="133fe-137">Priskirkite registracijos tipą, kurį sukūrėte, iš anksto nustatytai registracijos kategorijai.</span><span class="sxs-lookup"><span data-stu-id="133fe-137">Assign the registration type that you created to a predefined registration category.</span></span>  
22. <span data-ttu-id="133fe-138">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="133fe-138">Click Save.</span></span>


