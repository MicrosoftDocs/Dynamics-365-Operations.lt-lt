--- 
title: "Nustatyti įsigijimo kategorijų hierarchijų strategijas"
description: "Naudokite šią procedūrą norėdami nustatyti taisykles užsisakyti produktų kategorijoje."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f98f5b578c1d01463d196b6018e9f47a9d924be7
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="92452-103">Nustatyti įsigijimo kategorijų hierarchijų strategijas</span><span class="sxs-lookup"><span data-stu-id="92452-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92452-104">Naudokite šią procedūrą norėdami nustatyti taisykles užsisakyti produktų kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="92452-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="92452-105">Taisyklės nustatomos konkrečiai pirkimo strategijai.</span><span class="sxs-lookup"><span data-stu-id="92452-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="92452-106">Kategorijos prieigos taisyklė nurodo, prie kurių įsigijimo kategorijų darbuotojai turės prieigą kurdami paraišką.</span><span class="sxs-lookup"><span data-stu-id="92452-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="92452-107">Kai kuriama paraiška, taikytinos pirkimo strategijos ir kategorijos prieigos taisyklės nustatomos pagal juridinį subjektą ir veiklos vienetą, kuriam darbuotojas priskirtas.</span><span class="sxs-lookup"><span data-stu-id="92452-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="92452-108">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="92452-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="92452-109">Šią užduotį paprastai atlieka pirkimo vadovas.</span><span class="sxs-lookup"><span data-stu-id="92452-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="92452-110">Rasti įsigijimo strategiją</span><span class="sxs-lookup"><span data-stu-id="92452-110">Find the procurement policy</span></span>
1. <span data-ttu-id="92452-111">Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="92452-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="92452-112">Spustelėkite įsigijimo strategijos USMF strategijos saitą.</span><span class="sxs-lookup"><span data-stu-id="92452-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="92452-113">Tai yra strategija, į kurią įtrauksite į taisyklę.</span><span class="sxs-lookup"><span data-stu-id="92452-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="92452-114">Tai turi būti aktyvi strategija.</span><span class="sxs-lookup"><span data-stu-id="92452-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="92452-115">Sukurti kategorijos prieigos taisyklę</span><span class="sxs-lookup"><span data-stu-id="92452-115">Create a category access rule</span></span>
1. <span data-ttu-id="92452-116">Pasirinkite kategorijos prieigos strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="92452-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="92452-117">Jei mygtukas Kurti strategijos taisyklę patamsintas, taip yra todėl, kad jau yra aktyvi kategorijos prieigos strategijos taisyklė.</span><span class="sxs-lookup"><span data-stu-id="92452-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="92452-118">Patikrinkite laukus Įsigaliojimo data ir Galiojimo data, kad nustatytumėte, kuri tai strategijos taisyklė, tada pasirinkite jį ir spustelėkite Naikinti strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="92452-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="92452-119">Jei mygtuką Kurti strategijos taisyklę galima naudoti, jums nereikia atlikti jokių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="92452-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="92452-120">Spustelėkite Kurti strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="92452-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="92452-121">Lauke Įsigaliojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="92452-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="92452-122">Laikas turi negali sutapti su kita jau suaktyvinta taisykle.</span><span class="sxs-lookup"><span data-stu-id="92452-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="92452-123">Pasirinkite kategoriją, kuriai bus taikoma taisyklė.</span><span class="sxs-lookup"><span data-stu-id="92452-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="92452-124">Pasižymėkite, kuri tai kategorija, nes jos reikės vėliau.</span><span class="sxs-lookup"><span data-stu-id="92452-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="92452-125">Pasirinkus kategoriją, jos pirminė kategorija arba kategorijos taip pat įtraukiamos į sąrašą Pasirinktos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="92452-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="92452-126">Pažymėkite žymės langelį Įtraukti subkategorijas, norėdami taisyklę taikyti visoms pasirinktos kategorijos subkategorijoms.</span><span class="sxs-lookup"><span data-stu-id="92452-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="92452-127">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="92452-127">Click Add.</span></span>
    * <span data-ttu-id="92452-128">Jei parinktį Įtraukti pirminę taisyklę nustatysite į Taip, strategijos taisyklė, kurią nustatote pirminei kategorijai, taip priskiriama jos antrinėms kategorijoms, jei antrinėms kategorijoms nenurodytos strategijos taisyklės.</span><span class="sxs-lookup"><span data-stu-id="92452-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="92452-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="92452-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="92452-130">Sukurti kategorijos strategijos taisyklę</span><span class="sxs-lookup"><span data-stu-id="92452-130">Create a category policy rule</span></span>
1. <span data-ttu-id="92452-131">Pasirinkti kategorijos strategijos taisyklę</span><span class="sxs-lookup"><span data-stu-id="92452-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="92452-132">Jei mygtukas Kurti strategijos taisyklę patamsintas, pasirinkite aktyvią strategijos taisyklę ir tada spustelėkite Panaikinti strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="92452-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="92452-133">Spustelėkite Kurti strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="92452-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="92452-134">Lauke Įsigaliojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="92452-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="92452-135">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="92452-135">Click Add.</span></span>
5. <span data-ttu-id="92452-136">Pasirinkite tą pačią kategoriją, kurią naudojote nustatydami kategorijos prieigos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="92452-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="92452-137">Lauke Tiekėjo pasirinkimas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="92452-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="92452-138">Pasirinkite taisyklę, norėdami valdyti, kokius kategorijos tiekėjus galima pasirinkti kuriant paraiškas.</span><span class="sxs-lookup"><span data-stu-id="92452-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="92452-139">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="92452-139">Click Close.</span></span>
    * <span data-ttu-id="92452-140">Jūsų nustatytos strategijos taisyklės taikomos tipo Suvartojimas paraiškoms.</span><span class="sxs-lookup"><span data-stu-id="92452-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="92452-141">Jei norite nustatyti strategijas tipo Papildymas paraiškoms, kurkite taisyklę, skirtą strategijos taisyklės tipui, kuris vadinamas „Papildymo kategorijos prieigos strategijos taisyklė“.</span><span class="sxs-lookup"><span data-stu-id="92452-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  


