---
title: Grąžinimų valdymo grupės
description: Šiame skyriuje paaiškinta, kaip nustatyti grąžinimų valdymų grupes. Grąžinimų valdymo grupės gali būti naudojamos skaičiuojant grąžinimus ir pridėtos prie pagrindinio įrašo.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271082"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="40f80-104">Grąžinimų valdymo grupės</span><span class="sxs-lookup"><span data-stu-id="40f80-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40f80-105">Grąžinimo valdymo skaičiavimus galima pagrįsti grupėmis.</span><span class="sxs-lookup"><span data-stu-id="40f80-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="40f80-106">Grąžinimų valdymo grupės gali būti sukurtos klientams, tiekėjams ir prekėms.</span><span class="sxs-lookup"><span data-stu-id="40f80-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="40f80-107">Jas galima pridėti prie pagrindinio įrašo.</span><span class="sxs-lookup"><span data-stu-id="40f80-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="40f80-108">Grąžinimų valdymo kliento grupės</span><span class="sxs-lookup"><span data-stu-id="40f80-108">Rebate management customer groups</span></span>

<span data-ttu-id="40f80-109">Skaičiavimas klientų grupei dažnai sukuriamas įmonių grandinei, pavyzdžiui, prekybos centrų grandinei ar franšizės įmonei.</span><span class="sxs-lookup"><span data-stu-id="40f80-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="40f80-110">Tokio tipo skaičiavimas įprastai susijęs su grąžinimu.</span><span class="sxs-lookup"><span data-stu-id="40f80-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="40f80-111">Atskaitymas dažnai apskaičiuojamas neatsižvelgiant į tai, kam buvo parduotas tinkamumo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="40f80-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="40f80-112">Tačiau yra išimčių.</span><span class="sxs-lookup"><span data-stu-id="40f80-112">However, there are exceptions.</span></span> <span data-ttu-id="40f80-113">Pavyzdžiui, licencijos klientas gali sukurti atskaitymo schemą, pagal kurią klientų grupė A gaus 4 procentus, tačiau klientų grupė B gaus tik 3 procentus.</span><span class="sxs-lookup"><span data-stu-id="40f80-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="40f80-114">Nustatyti klientų grupes</span><span class="sxs-lookup"><span data-stu-id="40f80-114">Set up customer groups</span></span>

<span data-ttu-id="40f80-115">Norėdami dirbti su grąžinimų valdymo kliento grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Kliento grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="40f80-116">Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="40f80-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="40f80-117">Kiekvienai grupei nustatykite toliau pateiktus laukus:</span><span class="sxs-lookup"><span data-stu-id="40f80-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="40f80-118">**Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="40f80-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="40f80-119">**Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="40f80-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="40f80-120">Klientų grupių priskyrimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="40f80-120">Manage customer group assignments</span></span>

<span data-ttu-id="40f80-121">Kiekvienas klientas gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui.</span><span class="sxs-lookup"><span data-stu-id="40f80-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="40f80-122">Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo klientų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="40f80-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="40f80-123">Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės klientus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="40f80-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="40f80-124">Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Klientų grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="40f80-125">Pasirinkite norimą valdyti grupę.</span><span class="sxs-lookup"><span data-stu-id="40f80-125">Select the group to manage.</span></span>
1. <span data-ttu-id="40f80-126">Veiksmų srityje pasirinkite **Klientai**.</span><span class="sxs-lookup"><span data-stu-id="40f80-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="40f80-127">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas klientų, kurie jau yra pasirinktos grupės nariai, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="40f80-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="40f80-128">Norėdami pridėti naują klientą į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="40f80-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="40f80-129">Tada nustatykite šį lauką naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="40f80-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="40f80-130">**Kliento sąskaita** – pasirinkite kliento sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="40f80-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="40f80-131">Norėdami pašalinti klientą iš grupės, pasirinkite klientą, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="40f80-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="40f80-132">Norėdami peržiūrėti, pridėti arba pašalinti pasirinkto kliento priskyrimus grupėms, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="40f80-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="40f80-133">Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="40f80-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="40f80-134">Pasirinkite klientą, su kuriuo norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="40f80-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="40f80-135">Veiksmų srities skirtuke **Klientas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="40f80-136">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinktas klientas jau priklauso, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="40f80-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="40f80-137">Norėdami pridėti klientą į naują grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="40f80-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="40f80-138">Tada nustatykite šį lauką naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="40f80-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="40f80-139">**Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti klientą.</span><span class="sxs-lookup"><span data-stu-id="40f80-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="40f80-140">Norėdami pašalinti klientą iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="40f80-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="40f80-141">Grąžinimų valdymo tiekėjo grupės</span><span class="sxs-lookup"><span data-stu-id="40f80-141">Rebate management vendor groups</span></span>

<span data-ttu-id="40f80-142">Skaičiavimas tiekėjų grupei dažnai kuriamas pristatymo taškų grupei.</span><span class="sxs-lookup"><span data-stu-id="40f80-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="40f80-143">Tokio tipo skaičiavimas įprastai susijęs su grąžinimu.</span><span class="sxs-lookup"><span data-stu-id="40f80-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="40f80-144">Tiekėjo grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="40f80-144">Set up vendor groups</span></span>

<span data-ttu-id="40f80-145">Norėdami dirbti su grąžinimų valdymo tiekėjo grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Tiekėjo grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="40f80-146">Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="40f80-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="40f80-147">Kiekvienai grupei nustatykite toliau pateiktus laukus:</span><span class="sxs-lookup"><span data-stu-id="40f80-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="40f80-148">**Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="40f80-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="40f80-149">**Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="40f80-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="40f80-150">Tiekėjo grupių priskyrimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="40f80-150">Manage vendor group assignments</span></span>

<span data-ttu-id="40f80-151">Kiekvienas tiekėjas gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui.</span><span class="sxs-lookup"><span data-stu-id="40f80-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="40f80-152">Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo tiekėjų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="40f80-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="40f80-153">Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės tiekėjus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="40f80-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="40f80-154">Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Tiekėjų grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="40f80-155">Pasirinkite norimą valdyti grupę.</span><span class="sxs-lookup"><span data-stu-id="40f80-155">Select the group to manage.</span></span>
1. <span data-ttu-id="40f80-156">Veiksmų srityje pasirinkite **Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="40f80-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="40f80-157">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas tiekėjų, kurie jau yra pasirinktos grupės nariai, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="40f80-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="40f80-158">Norėdami pridėti naują tiekėją į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="40f80-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="40f80-159">Tada nustatykite šį lauką naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="40f80-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="40f80-160">**Tiekėjo sąskaita** – pasirinkite tiekėjo sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="40f80-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="40f80-161">Norėdami pašalinti tiekėją iš grupės, pasirinkite tiekėją, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="40f80-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="40f80-162">Norėdami peržiūrėti, pridėti arba pašalinti pasirinkto tiekėjo priskyrimus grupėms, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="40f80-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="40f80-163">Eikite į **Mokėtinos sumos \> Tiekėjai \> Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="40f80-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="40f80-164">Pasirinkite tiekėją, su kuriuo norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="40f80-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="40f80-165">Veiksmų srities skirtuke **Tiekėjas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="40f80-166">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinktas tiekėjas jau priklauso, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="40f80-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="40f80-167">Norėdami pridėti tiekėją į naują grupę, iš veiksmų srities pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="40f80-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="40f80-168">Tada nustatykite šį lauką naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="40f80-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="40f80-169">**Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti tiekėją.</span><span class="sxs-lookup"><span data-stu-id="40f80-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="40f80-170">Norėdami pašalinti tiekėją iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="40f80-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="40f80-171">Prekių grąžinimo grupės</span><span class="sxs-lookup"><span data-stu-id="40f80-171">Item rebate groups</span></span>

<span data-ttu-id="40f80-172">Grupuodami prekes turite daugiau lankstumo, kai apskaičiuojami grąžinimai ir atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="40f80-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="40f80-173">Šis būdas dažnai yra efektyvesnis nustatant grąžinimus ir atskaitymus klientams ir tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="40f80-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="40f80-174">Nustatyti prekių grupes</span><span class="sxs-lookup"><span data-stu-id="40f80-174">Set up item groups</span></span>

<span data-ttu-id="40f80-175">Norėdami dirbti su grąžinimų valdymo prekių grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Prekių grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="40f80-176">Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="40f80-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="40f80-177">Kiekvienai grupei nustatykite toliau pateiktus laukus:</span><span class="sxs-lookup"><span data-stu-id="40f80-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="40f80-178">**Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="40f80-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="40f80-179">**Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="40f80-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="40f80-180">Prekių grupių priskyrimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="40f80-180">Manage item group assignments</span></span>

<span data-ttu-id="40f80-181">Kiekviena prekė gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui.</span><span class="sxs-lookup"><span data-stu-id="40f80-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="40f80-182">Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo prekių sąrašo.</span><span class="sxs-lookup"><span data-stu-id="40f80-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="40f80-183">Taip pat galite įtraukti prekes ir pagal kategorijų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="40f80-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="40f80-184">Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės prekes, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="40f80-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="40f80-185">Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Prekių grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="40f80-186">Pasirinkite norimą valdyti grupę.</span><span class="sxs-lookup"><span data-stu-id="40f80-186">Select the group to manage.</span></span>
1. <span data-ttu-id="40f80-187">Veiksmų srityje pasirinkite **Prekės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="40f80-188">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas prekių, kurios jau yra pasirinktos grupės narės, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="40f80-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="40f80-189">Norėdami pridėti prekę į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="40f80-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="40f80-190">Tada nustatykite šį lauką naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="40f80-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="40f80-191">**Prekės sąskaita** – pasirinkite prekės sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="40f80-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="40f80-192">Norėdami pašalinti prekę iš grupės, pasirinkite prekę, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="40f80-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="40f80-193">Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos prekės priskyrimus grupėms, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="40f80-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="40f80-194">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="40f80-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="40f80-195">Pasirinkite prekę, su kuria norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="40f80-195">Select the item to work with.</span></span>
1. <span data-ttu-id="40f80-196">Veiksmų srities skirtuke **Produktas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="40f80-197">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinkta prekė jau priklauso, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="40f80-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="40f80-198">Norėdami pridėti prekę į naują grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="40f80-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="40f80-199">Tada nustatykite šį lauką naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="40f80-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="40f80-200">**Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti prekę.</span><span class="sxs-lookup"><span data-stu-id="40f80-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="40f80-201">Norėdami pašalinti prekę iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="40f80-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="40f80-202">Norėdami įtraukti prekes į grupę pagal jūsų kategorijų hierarchiją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="40f80-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="40f80-203">Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Prekių grupės**.</span><span class="sxs-lookup"><span data-stu-id="40f80-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="40f80-204">Pasirinkite norimą valdyti grupę.</span><span class="sxs-lookup"><span data-stu-id="40f80-204">Select the group to manage.</span></span>
1. <span data-ttu-id="40f80-205">Veiksmų srityje pasirinkite **Įtraukti prekes**.</span><span class="sxs-lookup"><span data-stu-id="40f80-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="40f80-206">Dialogo lango **Įtraukti elementus** lauke **Kategorijų hierarchija** pasirinkite aukščiausio lygio kategoriją.</span><span class="sxs-lookup"><span data-stu-id="40f80-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="40f80-207">Kairiojoje srityje atidaroma prekių hierarchija.</span><span class="sxs-lookup"><span data-stu-id="40f80-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="40f80-208">Pasirinkite ieškomą hierarchijos lygį.</span><span class="sxs-lookup"><span data-stu-id="40f80-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="40f80-209">Dabar prekės iš pasirinktos hierarchijos ir jos lygio yra išvardintos dešinėje srityje.</span><span class="sxs-lookup"><span data-stu-id="40f80-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="40f80-210">Norėdami dirbti su sritimi, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="40f80-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="40f80-211">Pasirinkite kiekvienos prekės, kurią norite įtraukti, žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="40f80-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="40f80-212">Pasirinkite žymės langelį tinklelio antraštėje, kad pasirinktumėte visas išvardytas prekes.</span><span class="sxs-lookup"><span data-stu-id="40f80-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="40f80-213">Pasirinkite mygtuką **Rodyti pasirinktus**, kad būtų filtruojamas tinklelis taip, jog jame būtų rodomos tik jūsų pasirinktos prekės.</span><span class="sxs-lookup"><span data-stu-id="40f80-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="40f80-214">Vėl pasirinkite mygtuką, jei norite grįžti į pilną sąrašą.</span><span class="sxs-lookup"><span data-stu-id="40f80-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="40f80-215">Pasirinkite **Gerai**, jei norite pritaikyti savo prekių pasirinkimą pasirinktai grupei.</span><span class="sxs-lookup"><span data-stu-id="40f80-215">Select **OK** to apply your item selection to the selected group.</span></span>
