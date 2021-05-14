---
title: Mažiau nei sunkvežimio (LTL) krovinių klasės
description: Šioje temoje paaiškinama, kas yra mažiau nei sunkvežimio krovinio (LTL) klasės ir aprašoma, kaip jas nustatyti programoje „Microsoft Dynamics 365 Supply Chain Management“.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941815"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="475a1-103">Mažiau nei sunkvežimio (LTL) krovinių klasės</span><span class="sxs-lookup"><span data-stu-id="475a1-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="475a1-104">Mažiau nei sunkvežimio krovinio (LTL) klasė yra krovinio siuntimo klasė, naudojama prekėms, kurios gali būti siunčiamos, klasifikuoti.</span><span class="sxs-lookup"><span data-stu-id="475a1-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="475a1-105">Paprastai kiekvienas produkto ar prekės tipas turi „National Motor Freight Classification“ (NMFC) kodą, kuris atitinka specialų LTL siuntų transportavimo klasės numerį.</span><span class="sxs-lookup"><span data-stu-id="475a1-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="475a1-106">LTL transportavimo klasės nurodo prekių kategorijas, o NMFC kodai yra susiję su konkrečiomis prekėmis kiekvienoje iš 18 transportavimo klasių.</span><span class="sxs-lookup"><span data-stu-id="475a1-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="475a1-107">Ši funkcija jums leidžia jums naudoti jūsų sistemą siekiant atlikti tolesnes užduotis:</span><span class="sxs-lookup"><span data-stu-id="475a1-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="475a1-108">Nustatykite jūsų įmonėje naudojamas LTL transportavimo klases.</span><span class="sxs-lookup"><span data-stu-id="475a1-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="475a1-109">Kiekvienai LTL klasei priskirkite NMFC kodą **NMFC kodų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="475a1-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="475a1-110">Daugiau informacijos ieškokite [„National Motor Freight Classificatio“ (NMFC) ](nmfc-codes.md) kodais.</span><span class="sxs-lookup"><span data-stu-id="475a1-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="475a1-111">Kiekvienam produktui produktų puslapyje priskirkite NMFC kodą (ir su juo susijęs LTL) **kodas**.</span><span class="sxs-lookup"><span data-stu-id="475a1-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="475a1-112">Tiksliai įvertinti kiekvieno produkto, prie kurių priskirtas NMFC kodas, LTL klasę.</span><span class="sxs-lookup"><span data-stu-id="475a1-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="475a1-113">Nustatyti pakavimo reikalavimus kiekvienai LTL klasei, tikrinant tarptautinius LTL standartus.</span><span class="sxs-lookup"><span data-stu-id="475a1-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="475a1-114">Taip užtikrinate, kad jūsų produktai bus gerai apsaugoti ir saugiai išsiųsti.</span><span class="sxs-lookup"><span data-stu-id="475a1-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="475a1-115">Gauti tikslius siuntimo įvertinimus, remiantis kiekvieno produkto LTL transportavimo klase.</span><span class="sxs-lookup"><span data-stu-id="475a1-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="475a1-116">Šioje temoje aprašoma, kaip sukurti LTL klases, naudojant „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="475a1-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="475a1-117">LTL klasės kūrimas</span><span class="sxs-lookup"><span data-stu-id="475a1-117">Create an LTL class</span></span>

<span data-ttu-id="475a1-118">Norėdami sukurti LTL klasę, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="475a1-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="475a1-119">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="475a1-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="475a1-120">Eikite į **Sandėlio valdymas \> Nustatymas \> Atsargos \> LTL klasės**.</span><span class="sxs-lookup"><span data-stu-id="475a1-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="475a1-121">Eikite į **Gabenimo valdymas \> Nustatymai \> Gabenimo standartai \> LTL klasės**.</span><span class="sxs-lookup"><span data-stu-id="475a1-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="475a1-122">Veiksmų srityje pasirinkite **Nauja** tam, kad sukurtumėte LTL klasę.</span><span class="sxs-lookup"><span data-stu-id="475a1-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="475a1-123">Tada nustatykite toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="475a1-123">Then set the following fields:</span></span>

    - <span data-ttu-id="475a1-124">**LTL klasė – įveskite prekės tipo vidinį įmonės LTL klasės** identifikatorių (ID).</span><span class="sxs-lookup"><span data-stu-id="475a1-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="475a1-125">Daugelis įmonių naudoja tarptautinius standartą.</span><span class="sxs-lookup"><span data-stu-id="475a1-125">Most companies use the international standard.</span></span> <span data-ttu-id="475a1-126">Tokiu atveju šio lauko vertė atitiks lauko Klasė **vertę**.</span><span class="sxs-lookup"><span data-stu-id="475a1-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="475a1-127">Tačiau, jei jūsų įmonė naudoja savo standartą, įveskite kodą, kuris atitinka tą standartą.</span><span class="sxs-lookup"><span data-stu-id="475a1-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="475a1-128">**Pavadinimas** – įveskite aprašomąjį pavadinimą, kuris padės jums ir kitiems vartotojams pasirinkti teisingą kiekvieno NMFC kodo LTL klasę.</span><span class="sxs-lookup"><span data-stu-id="475a1-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="475a1-129">**Klasė** – įveskite prekės tipo tarptautinės standartinės LTL klasės ID.</span><span class="sxs-lookup"><span data-stu-id="475a1-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="475a1-130">Čia įvedamas kodas turi atitikti oficialų standartą.</span><span class="sxs-lookup"><span data-stu-id="475a1-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="475a1-131">Pavyzdys: LTL klasių rinkinys</span><span class="sxs-lookup"><span data-stu-id="475a1-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="475a1-132">Toliau pateikiamas pavyzdys rodo, kaip nustatyti dvi skirtingas LTL klases, kurias galima naudoti su skirtingais produktų tipais.</span><span class="sxs-lookup"><span data-stu-id="475a1-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="475a1-133">Eikite į **Sandėlio valdymas \> Nustatymas \> Atsargos \> LTL klasės**.</span><span class="sxs-lookup"><span data-stu-id="475a1-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="475a1-134">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="475a1-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="475a1-135">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="475a1-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="475a1-136">**LTL klasė:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="475a1-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="475a1-137">**Pavadinimas:** *kompiuteriai, stebėjimas, programos*</span><span class="sxs-lookup"><span data-stu-id="475a1-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="475a1-138">**Klasė:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="475a1-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="475a1-139">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="475a1-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="475a1-140">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="475a1-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="475a1-141">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="475a1-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="475a1-142">**LTL klasė:** *125*</span><span class="sxs-lookup"><span data-stu-id="475a1-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="475a1-143">**Pavadinimas:** *mažas plėtinys*</span><span class="sxs-lookup"><span data-stu-id="475a1-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="475a1-144">**Klasė:** *125*</span><span class="sxs-lookup"><span data-stu-id="475a1-144">**Class:** *125*</span></span>

1. <span data-ttu-id="475a1-145">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="475a1-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="475a1-146">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="475a1-146">Additional resources</span></span>

- [<span data-ttu-id="475a1-147">„National Motor Freight Classification“ (NMFC) kodai</span><span class="sxs-lookup"><span data-stu-id="475a1-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="475a1-148">Važtaraščio kūrimas</span><span class="sxs-lookup"><span data-stu-id="475a1-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
