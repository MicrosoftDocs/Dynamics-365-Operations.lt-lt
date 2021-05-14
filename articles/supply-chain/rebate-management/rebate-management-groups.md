---
title: Grąžinimų valdymo grupės
description: Šiame skyriuje paaiškinta, kaip nustatyti grąžinimų valdymų grupes. Grąžinimų valdymo grupės gali būti naudojamos skaičiuojant grąžinimus ir pridėtos prie pagrindinio įrašo.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920066"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="abd91-104">Grąžinimų valdymo grupės</span><span class="sxs-lookup"><span data-stu-id="abd91-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="abd91-105">Grąžinimo ir atskaitymo skaičiavimus galima pagrįsti grupėmis.</span><span class="sxs-lookup"><span data-stu-id="abd91-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="abd91-106">Grąžinimų valdymo grupės gali būti sukurtos klientams, tiekėjams ir prekėms.</span><span class="sxs-lookup"><span data-stu-id="abd91-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="abd91-107">Jas galima pridėti prie pagrindinio įrašo.</span><span class="sxs-lookup"><span data-stu-id="abd91-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="abd91-108">Grąžinimų valdymo kliento grupės</span><span class="sxs-lookup"><span data-stu-id="abd91-108">Rebate management customer groups</span></span>

<span data-ttu-id="abd91-109">Skaičiavimas klientų grupei dažnai sukuriamas įmonių grandinei, pavyzdžiui, prekybos centrų grandinei ar franšizės įmonei.</span><span class="sxs-lookup"><span data-stu-id="abd91-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="abd91-110">Tokio tipo skaičiavimas įprastai susijęs su grąžinimu.</span><span class="sxs-lookup"><span data-stu-id="abd91-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="abd91-111">Atskaitymas dažnai apskaičiuojamas neatsižvelgiant į tai, kam buvo parduotas tinkamumo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="abd91-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="abd91-112">Tačiau yra išimčių.</span><span class="sxs-lookup"><span data-stu-id="abd91-112">However, there are exceptions.</span></span> <span data-ttu-id="abd91-113">Pavyzdžiui, licencijos klientas gali sukurti atskaitymo schemą, pagal kurią klientų grupė A gaus 4 procentus, tačiau klientų grupė B gaus tik 3 procentus.</span><span class="sxs-lookup"><span data-stu-id="abd91-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="abd91-114">Nustatyti klientų grupes</span><span class="sxs-lookup"><span data-stu-id="abd91-114">Set up customer groups</span></span>

<span data-ttu-id="abd91-115">Norėdami dirbti su grąžinimų valdymo kliento grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Kliento grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="abd91-116">Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="abd91-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="abd91-117">Kiekvienai grupei nustatykite toliau pateiktus laukus:</span><span class="sxs-lookup"><span data-stu-id="abd91-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="abd91-118">**Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="abd91-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="abd91-119">**Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="abd91-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="abd91-120">Klientų grupių priskyrimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="abd91-120">Manage customer group assignments</span></span>

<span data-ttu-id="abd91-121">Kiekvienas klientas gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui.</span><span class="sxs-lookup"><span data-stu-id="abd91-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="abd91-122">Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo klientų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="abd91-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="abd91-123">Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės klientus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="abd91-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="abd91-124">Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Klientų grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="abd91-125">Pasirinkite norimą valdyti grupę.</span><span class="sxs-lookup"><span data-stu-id="abd91-125">Select the group to manage.</span></span>
1. <span data-ttu-id="abd91-126">Veiksmų srityje pasirinkite **Klientai**.</span><span class="sxs-lookup"><span data-stu-id="abd91-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="abd91-127">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas klientų, kurie jau yra pasirinktos grupės nariai, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="abd91-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="abd91-128">Norėdami pridėti naują klientą į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="abd91-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="abd91-129">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="abd91-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="abd91-130">**Kliento sąskaita** – pasirinkite kliento sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="abd91-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="abd91-131">**Pavadinimas** – įveskite kliento pavadinimą ir (arba) aprašymą.</span><span class="sxs-lookup"><span data-stu-id="abd91-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="abd91-132">Norėdami pašalinti klientą iš grupės, pasirinkite klientą, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="abd91-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="abd91-133">Norėdami peržiūrėti, pridėti arba pašalinti pasirinkto kliento priskyrimus grupėms, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="abd91-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="abd91-134">Eikite į **Gautinos sumos \> Klientai \> Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="abd91-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="abd91-135">Pasirinkite klientą, su kuriuo norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="abd91-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="abd91-136">Veiksmų srities skirtuke **Klientas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="abd91-137">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinktas klientas jau priklauso, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="abd91-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="abd91-138">Norėdami pridėti klientą į naują grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="abd91-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="abd91-139">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="abd91-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="abd91-140">**Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti klientą.</span><span class="sxs-lookup"><span data-stu-id="abd91-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="abd91-141">**Aprašymas** – įveskite grupės aprašymą (pavyzdžiui, paaiškinkite, kodėl klientas yra jos narys).</span><span class="sxs-lookup"><span data-stu-id="abd91-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="abd91-142">Norėdami pašalinti klientą iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="abd91-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="abd91-143">Grąžinimų valdymo tiekėjo grupės</span><span class="sxs-lookup"><span data-stu-id="abd91-143">Rebate management vendor groups</span></span>

<span data-ttu-id="abd91-144">Skaičiavimas tiekėjų grupei dažnai kuriamas pristatymo taškų grupei.</span><span class="sxs-lookup"><span data-stu-id="abd91-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="abd91-145">Tokio tipo skaičiavimas įprastai susijęs su grąžinimu.</span><span class="sxs-lookup"><span data-stu-id="abd91-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="abd91-146">Tiekėjo grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="abd91-146">Set up vendor groups</span></span>

<span data-ttu-id="abd91-147">Norėdami dirbti su grąžinimų valdymo tiekėjo grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Tiekėjo grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="abd91-148">Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="abd91-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="abd91-149">Kiekvienai grupei nustatykite toliau pateiktus laukus:</span><span class="sxs-lookup"><span data-stu-id="abd91-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="abd91-150">**Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="abd91-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="abd91-151">**Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="abd91-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="abd91-152">Tiekėjo grupių priskyrimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="abd91-152">Manage vendor group assignments</span></span>

<span data-ttu-id="abd91-153">Kiekvienas tiekėjas gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui.</span><span class="sxs-lookup"><span data-stu-id="abd91-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="abd91-154">Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo tiekėjų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="abd91-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="abd91-155">Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės tiekėjus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="abd91-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="abd91-156">Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Tiekėjų grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="abd91-157">Pasirinkite norimą valdyti grupę.</span><span class="sxs-lookup"><span data-stu-id="abd91-157">Select the group to manage.</span></span>
1. <span data-ttu-id="abd91-158">Veiksmų srityje pasirinkite **Tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="abd91-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="abd91-159">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas tiekėjų, kurie jau yra pasirinktos grupės nariai, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="abd91-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="abd91-160">Norėdami pridėti naują tiekėją į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="abd91-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="abd91-161">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="abd91-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="abd91-162">**Tiekėjo sąskaita** – pasirinkite tiekėjo sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="abd91-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="abd91-163">**Pavadinimas** – įveskite tiekėjo pavadinimą ir (arba) aprašymą.</span><span class="sxs-lookup"><span data-stu-id="abd91-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="abd91-164">Norėdami pašalinti tiekėją iš grupės, pasirinkite tiekėją, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="abd91-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="abd91-165">Norėdami peržiūrėti, pridėti arba pašalinti pasirinkto tiekėjo priskyrimus grupėms, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="abd91-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="abd91-166">Eikite į **Mokėtinos sumos \> Tiekėjai \> Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="abd91-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="abd91-167">Pasirinkite tiekėją, su kuriuo norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="abd91-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="abd91-168">Veiksmų srities skirtuke **Tiekėjas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="abd91-169">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinktas tiekėjas jau priklauso, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="abd91-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="abd91-170">Norėdami pridėti tiekėją į naują grupę, iš veiksmų srities pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="abd91-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="abd91-171">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="abd91-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="abd91-172">**Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti tiekėją.</span><span class="sxs-lookup"><span data-stu-id="abd91-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="abd91-173">**Aprašymas** – įveskite grupės aprašymą (pavyzdžiui, paaiškinkite, kodėl tiekėjas yra jos narys).</span><span class="sxs-lookup"><span data-stu-id="abd91-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="abd91-174">Norėdami pašalinti tiekėją iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="abd91-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="abd91-175">Prekių grąžinimo grupės</span><span class="sxs-lookup"><span data-stu-id="abd91-175">Item rebate groups</span></span>

<span data-ttu-id="abd91-176">Grupuodami prekes turite daugiau lankstumo, kai apskaičiuojami grąžinimai ir atskaitymai.</span><span class="sxs-lookup"><span data-stu-id="abd91-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="abd91-177">Šis būdas dažnai yra efektyvesnis nustatant grąžinimus ir atskaitymus klientams ir tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="abd91-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="abd91-178">Nustatyti prekių grupes</span><span class="sxs-lookup"><span data-stu-id="abd91-178">Set up item groups</span></span>

<span data-ttu-id="abd91-179">Norėdami dirbti su grąžinimų valdymo prekių grupėmis, eikite į **Grąžinimo valdymas \> Grąžinimo valdymo grupių nustatymas \> Prekių grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="abd91-180">Galite naudoti veiksmų srities mygtukus grupių pridėjimui ir panaikinimui, kaip reikalinga.</span><span class="sxs-lookup"><span data-stu-id="abd91-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="abd91-181">Kiekvienai grupei nustatykite toliau pateiktus laukus:</span><span class="sxs-lookup"><span data-stu-id="abd91-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="abd91-182">**Grąžinimų valdymo grupė** – įveskite unikalųjį grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="abd91-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="abd91-183">**Aprašymas** – Įveskite grupės aprašymą, jei norite pateikti daugiau informacijos apie jos naudojimą.</span><span class="sxs-lookup"><span data-stu-id="abd91-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="abd91-184">Prekių grupių priskyrimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="abd91-184">Manage item group assignments</span></span>

<span data-ttu-id="abd91-185">Kiekviena prekė gali priklausyti bet kokiam grąžinimo valdymo grupių skaičiui.</span><span class="sxs-lookup"><span data-stu-id="abd91-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="abd91-186">Norėdami peržiūrėti ir priskirti grupės narius, galite pradėti nuo grupių arba nuo prekių sąrašo.</span><span class="sxs-lookup"><span data-stu-id="abd91-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="abd91-187">Taip pat galite įtraukti prekes ir pagal kategorijų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="abd91-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="abd91-188">Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos grupės prekes, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="abd91-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="abd91-189">Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Prekių grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="abd91-190">Pasirinkite norimą valdyti grupę.</span><span class="sxs-lookup"><span data-stu-id="abd91-190">Select the group to manage.</span></span>
1. <span data-ttu-id="abd91-191">Veiksmų srityje pasirinkite **Prekės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="abd91-192">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas prekių, kurios jau yra pasirinktos grupės narės, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="abd91-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="abd91-193">Norėdami pridėti prekę į grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="abd91-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="abd91-194">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="abd91-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="abd91-195">**Prekės sąskaita** – pasirinkite prekės sąskaitos ID.</span><span class="sxs-lookup"><span data-stu-id="abd91-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="abd91-196">**Produkto pavadinimas** – įveskite prekės pavadinimą ir (arba) aprašymą.</span><span class="sxs-lookup"><span data-stu-id="abd91-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="abd91-197">Norėdami pašalinti prekę iš grupės, pasirinkite prekę, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="abd91-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="abd91-198">Norėdami peržiūrėti, pridėti arba pašalinti pasirinktos prekės priskyrimus grupėms, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="abd91-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="abd91-199">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="abd91-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="abd91-200">Pasirinkite prekę, su kuria norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="abd91-200">Select the item to work with.</span></span>
1. <span data-ttu-id="abd91-201">Veiksmų srities skirtuke **Produktas**, grupėje **Grąžinimų valdymas** pasirinkite **Grąžinimų valdymo grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="abd91-202">Atsiranda **Grąžinimo valdymo grupių** puslapis, kuriame pateikiamas grupių, kurioms pasirinkta prekė jau priklauso, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="abd91-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="abd91-203">Norėdami pridėti prekę į naują grupę, veiksmų srityje pasirinkite **Naujas** eilutės įtraukimui į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="abd91-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="abd91-204">Tada nustatykite šiuos laukus naujai eilutei:</span><span class="sxs-lookup"><span data-stu-id="abd91-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="abd91-205">**Grąžinimų valdymo grupė** – pasirinkite grupę, į kurią norite įtraukti prekę.</span><span class="sxs-lookup"><span data-stu-id="abd91-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="abd91-206">**Aprašymas** – įveskite grupės aprašymą (pavyzdžiui, paaiškinkite, kodėl prekė yra jos narė).</span><span class="sxs-lookup"><span data-stu-id="abd91-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="abd91-207">Norėdami pašalinti prekę iš grupės, pasirinkite grupę, o tada veiksmų srityje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="abd91-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="abd91-208">Norėdami įtraukti prekes į grupę pagal jūsų kategorijų hierarchiją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="abd91-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="abd91-209">Eikite **Grąžinimų valdymas \> Grąžinimų valdymo grupių nustatymas \> Prekių grupės**.</span><span class="sxs-lookup"><span data-stu-id="abd91-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="abd91-210">Pasirinkite norimą valdyti grupę.</span><span class="sxs-lookup"><span data-stu-id="abd91-210">Select the group to manage.</span></span>
1. <span data-ttu-id="abd91-211">Veiksmų srityje pasirinkite **Įtraukti prekes**.</span><span class="sxs-lookup"><span data-stu-id="abd91-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="abd91-212">Dialogo lango **Įtraukti elementus** lauke **Kategorijų hierarchija** pasirinkite aukščiausio lygio kategoriją.</span><span class="sxs-lookup"><span data-stu-id="abd91-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="abd91-213">Kairiojoje srityje atidaroma prekių hierarchija.</span><span class="sxs-lookup"><span data-stu-id="abd91-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="abd91-214">Pasirinkite ieškomą hierarchijos lygį.</span><span class="sxs-lookup"><span data-stu-id="abd91-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="abd91-215">Dabar prekės iš pasirinktos hierarchijos ir jos lygio yra išvardintos dešinėje srityje.</span><span class="sxs-lookup"><span data-stu-id="abd91-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="abd91-216">Norėdami dirbti su sritimi, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="abd91-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="abd91-217">Pasirinkite kiekvienos prekės, kurią norite įtraukti, žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="abd91-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="abd91-218">Pasirinkite žymės langelį tinklelio antraštėje, kad pasirinktumėte visas išvardytas prekes.</span><span class="sxs-lookup"><span data-stu-id="abd91-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="abd91-219">Pasirinkite mygtuką **Rodyti pasirinktus**, kad būtų filtruojamas tinklelis taip, jog jame būtų rodomos tik jūsų pasirinktos prekės.</span><span class="sxs-lookup"><span data-stu-id="abd91-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="abd91-220">Vėl pasirinkite mygtuką, jei norite grįžti į pilną sąrašą.</span><span class="sxs-lookup"><span data-stu-id="abd91-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="abd91-221">Pasirinkite **Gerai**, jei norite pritaikyti savo prekių pasirinkimą pasirinktai grupei.</span><span class="sxs-lookup"><span data-stu-id="abd91-221">Select **OK** to apply your item selection to the selected group.</span></span>
