---
title: Inžinierinių pakeitimų valdymo parametrai
description: Šioje temoje paaiškina, kaip konfigūruoti inžinerijos keitimus valdymo funkcijose „Microsoft Dynamics 365 Supply Chain Management“.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 0cf0e56a8aece98379aa0f181d7b7ff665767544
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434046"
---
# <a name="engineering-change-management-parameters"></a><span data-ttu-id="8f04c-103">Inžinierinių pakeitimų valdymo parametrai</span><span class="sxs-lookup"><span data-stu-id="8f04c-103">Engineering change management parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f04c-104">**Inžinerijos keitimo valdymo parametrų** puslapyje pateikti nustatymo parametrai, kurie keičia nustatytąją elgseną susietą su leidimo produkto struktūra ir inžinerijos keitimo valdymo procesuose.</span><span class="sxs-lookup"><span data-stu-id="8f04c-104">The **Engineering change management parameters** page contains setup parameters that change the default behavior that is related to the release product structure and engineering change management processes.</span></span>

## <a name="open-the-engineering-change-management-parameters-page"></a><span data-ttu-id="8f04c-105">Atverkite inžinerijos keitimo valdymo parametrų puslapį</span><span class="sxs-lookup"><span data-stu-id="8f04c-105">Open the Engineering change management parameters page</span></span>

<span data-ttu-id="8f04c-106">Siekiant atverti **Inžinerijos keitimo valdymo parametrų** puslapį, eikite į **Inžinerijos keitimo valdymas \> Nustatymai \> Inžinerijos keitimo valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="8f04c-106">To open the **Engineering change management parameters** page, go to **Engineering change management \> Setup \> Engineering change management parameters**.</span></span> <span data-ttu-id="8f04c-107">Tuomet galite nustatyti laukelius kaip aprašyta likusiose šios temos skyriuose.</span><span class="sxs-lookup"><span data-stu-id="8f04c-107">You can then set the fields as described in the remaining sections of this topic.</span></span>

## <a name="release-control-tab"></a><span data-ttu-id="8f04c-108">Paleiskite valdiklio skirtuką</span><span class="sxs-lookup"><span data-stu-id="8f04c-108">Release control tab</span></span>

<span data-ttu-id="8f04c-109">Tolesnė lentelė aprašo laukelius, kurie yra prienami **Leidimo valdiklio** skirtuke puslapyje **Inžinerijos keitimo valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="8f04c-109">The following table describes the fields that are available on the **Release control** tab of the **Engineering change management parameters** page.</span></span> <span data-ttu-id="8f04c-110">Šie laukeliai keičia leidimo produkto struktūros procesą.</span><span class="sxs-lookup"><span data-stu-id="8f04c-110">These fields affect the release product structure process.</span></span>

| <span data-ttu-id="8f04c-111">Laukas</span><span class="sxs-lookup"><span data-stu-id="8f04c-111">Field</span></span> | <span data-ttu-id="8f04c-112">aprašymas</span><span class="sxs-lookup"><span data-stu-id="8f04c-112">Description</span></span> |
|---|---|
| <span data-ttu-id="8f04c-113">Prekės numerio taisyklė</span><span class="sxs-lookup"><span data-stu-id="8f04c-113">Item number rule</span></span> | <span data-ttu-id="8f04c-114">Pasirinkite, kaip prekės skaičius turi būti nustatytas, kai produktas yra išleistas juridiniam asmeniui.</span><span class="sxs-lookup"><span data-stu-id="8f04c-114">Select how the item number should be defined when the product is released to a legal entity.</span></span> <span data-ttu-id="8f04c-115">Pasirinkite *Inžinerijos produkto skaičius* jei produkto skaičius gaunančiame juridiniame asmenyje turi atitikti produkto skaičių inžinerijos įmonėje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-115">Select *Engineering product number* if the product number in the receiving legal entity should match the product number in the engineering company.</span></span> <span data-ttu-id="8f04c-116">Pasirinkite *Vietinė prekės skaičiaus seka* jei produktas turi paimti koitą skaičių skaičių sekoje produktų skaičiams gaunančiame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-116">Select *Local item number sequence* if the product should take the next number in the number sequence for product numbers in the receiving legal entity.</span></span> |
| <span data-ttu-id="8f04c-117">KS pavadinimo taisyklė</span><span class="sxs-lookup"><span data-stu-id="8f04c-117">BOM name rule</span></span> | <span data-ttu-id="8f04c-118">Pasirinkite, kaip medžagų važtaraščio pavadinimas (BOM) yra nustatytas, kai produktas gaunamas (išleidžiamas) juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-118">Select how the name of the bill of materials (BOM) is defined when the product is received (released) in a legal entity.</span></span> <span data-ttu-id="8f04c-119">Pasirinkite ar *Inžinerijos pavadinimą* ar *Gavimo prekės skaičius*.</span><span class="sxs-lookup"><span data-stu-id="8f04c-119">Select either *Engineering name* or *Receiving item number*.</span></span> |
| <span data-ttu-id="8f04c-120">Maršruto pavadinimo taisyklė</span><span class="sxs-lookup"><span data-stu-id="8f04c-120">Route name rule</span></span> | <span data-ttu-id="8f04c-121">Pasirinkite, kaip maršruto pavadinimas turi būti nustatytas, kai produkto maršrutas yra gaunamas (išleidžiamas) juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-121">Select how the route name should be defined when the route of a product is received (released) in a legal entity.</span></span> <span data-ttu-id="8f04c-122">Pasirinkite ar *Inžinerijos pavadinimą* ar *Gavimo prekės skaičius*.</span><span class="sxs-lookup"><span data-stu-id="8f04c-122">Select either *Engineering name* or *Receiving item number*.</span></span> |
| <span data-ttu-id="8f04c-123">Vykdyti KS patikrą</span><span class="sxs-lookup"><span data-stu-id="8f04c-123">Run BOM check</span></span> | <span data-ttu-id="8f04c-124">Pasirinkite, ar BOM patikra bus vykdoma, kai produktas gaunamas (išleidžiamas) juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-124">Select whether a BOM check will be run when the product is received (released) in a legal entity.</span></span> |
| <span data-ttu-id="8f04c-125">Neaktyvios KS išleidimo būdas</span><span class="sxs-lookup"><span data-stu-id="8f04c-125">Release behavior of inactive BOM</span></span> | <span data-ttu-id="8f04c-126">Pasirinkite, ar produktas gali būti išleistas, jei yra neįjungtas BOM.</span><span class="sxs-lookup"><span data-stu-id="8f04c-126">Select whether a product can be released if it has an inactive BOM.</span></span> <span data-ttu-id="8f04c-127">Pasirinkite *Priimti*, *Tik įspėti* ar *Neleidžiama*.</span><span class="sxs-lookup"><span data-stu-id="8f04c-127">Select *Accept*, *Warning only*, or *Not allowed*.</span></span> |
| <span data-ttu-id="8f04c-128">Neaktyvaus maršruto išleidimo būdas</span><span class="sxs-lookup"><span data-stu-id="8f04c-128">Release behavior of inactive route</span></span> | <span data-ttu-id="8f04c-129">Pasirinkite, ar produktas gali būti išleistas, jei yra neįjungtas maršrutas.</span><span class="sxs-lookup"><span data-stu-id="8f04c-129">Select whether a product can be released if it has an inactive route.</span></span> <span data-ttu-id="8f04c-130">Pasirinkite *Priimti*, *Tik įspėti* ar *Neleidžiama*.</span><span class="sxs-lookup"><span data-stu-id="8f04c-130">Select *Accept*, *Warning only*, or *Not allowed*.</span></span>|
| <span data-ttu-id="8f04c-131">Produkto priėmimas</span><span class="sxs-lookup"><span data-stu-id="8f04c-131">Product acceptance</span></span> | <span data-ttu-id="8f04c-132">Pasirinkite, ar papildomas priėmimo žingsnis yra būtinas prieš tai, kai produktas gali būti išleistas jurdiniam asmeniui.</span><span class="sxs-lookup"><span data-stu-id="8f04c-132">Select whether an additional step for acceptance is required before the product can be released in the legal entity.</span></span> <span data-ttu-id="8f04c-133">Pasirinkite *Rankinis* tam, kad įtrauktumėte priėmimo žingsnį.</span><span class="sxs-lookup"><span data-stu-id="8f04c-133">Select *Manual* to add the acceptance step.</span></span> <span data-ttu-id="8f04c-134">Tokiu atveju, **Atverkite produkto išleidimų** puslapį, kuris rodys produktus.</span><span class="sxs-lookup"><span data-stu-id="8f04c-134">In this case, the **Open product releases** page will show the products.</span></span> <span data-ttu-id="8f04c-135">Pasirinkite *Automatinis* tam, kad jis rodytų produktą tiesiogiai **Išleisti produktai** puslapyje tiksliniame juridiniame asmenyje iš karto po to, kai produktas išleistas kartu su išleisto produkto struktūra.</span><span class="sxs-lookup"><span data-stu-id="8f04c-135">Select *Automatic* to show the product directly on the **Released products** page in the target legal entity immediately after the product is released together with its release product structure.</span></span> |

## <a name="engineering-change-management-tab"></a><span data-ttu-id="8f04c-136">Inžinerijos keitimo valdymo skirtukas</span><span class="sxs-lookup"><span data-stu-id="8f04c-136">Engineering change management tab</span></span>

<span data-ttu-id="8f04c-137">Tolesnė lentelė aprašo laukelius, kurie yra prienami **Inžinerijos keitimo valdymas** skirtuke puslapyje **Inžinerijos keitimo valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="8f04c-137">The following table describes the fields that are available on the **Engineering change management** tab of the **Engineering change management parameters** page.</span></span> <span data-ttu-id="8f04c-138">Šie nustatymai paveikia inžinerijos keitimo valdymo procesą.</span><span class="sxs-lookup"><span data-stu-id="8f04c-138">These settings affect the engineering change management process.</span></span>

| <span data-ttu-id="8f04c-139">Laukas</span><span class="sxs-lookup"><span data-stu-id="8f04c-139">Field</span></span> | <span data-ttu-id="8f04c-140">aprašymas</span><span class="sxs-lookup"><span data-stu-id="8f04c-140">Description</span></span> |
|---|---|
| <span data-ttu-id="8f04c-141">Kategorija</span><span class="sxs-lookup"><span data-stu-id="8f04c-141">Category</span></span> | <span data-ttu-id="8f04c-142">Nustatytoji kategorija bus naudojama, kai inžinerijos keitimo užklausa sukuriama.</span><span class="sxs-lookup"><span data-stu-id="8f04c-142">The default category that will be used when an engineering change request is created.</span></span> |
| <span data-ttu-id="8f04c-143">Pirmenybė</span><span class="sxs-lookup"><span data-stu-id="8f04c-143">Priority</span></span> | <span data-ttu-id="8f04c-144">Nustatytoji pirmenybė bus naudojama, kai inžinerijos keitimo užklausa sukuriama.</span><span class="sxs-lookup"><span data-stu-id="8f04c-144">The default priority that will be used when an engineering change request is created.</span></span> |
| <span data-ttu-id="8f04c-145">Svarbos taisyklė</span><span class="sxs-lookup"><span data-stu-id="8f04c-145">Severity rule</span></span> | <span data-ttu-id="8f04c-146">Pasirinkite, kaip inžinerijos keitimo užsakymo sunkumas turi būti įsteigtas.</span><span class="sxs-lookup"><span data-stu-id="8f04c-146">Select how the severity of an engineering change order should be established.</span></span> <span data-ttu-id="8f04c-147">Pasirinkite *Rankinis*, jei vartotojas turi įvesti vertę **Sunkumo** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-147">Select *Manual* if the user is expected to enter a value in the **Severity** field.</span></span> <span data-ttu-id="8f04c-148">Rinkitės *Apskaičiuoti* tam, kad sistema apskaičiuotų **Sunkumo** laukelio vertę jums pasirinkus **Skaičiuoti sunkumą** inžinerijos keitimo užsakymo veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-148">Select *Calculate* to have the system calculate the value of the **Severity** field when you select **Calculate severity** on the Action Pane of the engineering change order.</span></span> <span data-ttu-id="8f04c-149">šiuo atveju sistema naudos sunkumo taisykles, kurios nustatytos **Sunkumo taisyklių rinkinio** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-149">In this case, the system will use the severity rules that are defined on the **Severity rule set** page.</span></span> <span data-ttu-id="8f04c-150">Rinkitės *Skaičiuoti automatiškai* tam, kad vertė **Sunkumo** laukelyje būtų skaičiuojama automatiniu būdu ir užpildoma pagal sunkumo taisyklių rinkinius.</span><span class="sxs-lookup"><span data-stu-id="8f04c-150">Select *Calculate automatically* to have the value of the **Severity** field automatically calculated and filled in according to the severity rule sets.</span></span> |
| <span data-ttu-id="8f04c-151">Pakartotinai išleisti paveiktus produktus</span><span class="sxs-lookup"><span data-stu-id="8f04c-151">Re-release impacted products</span></span> | <span data-ttu-id="8f04c-152">Šis laukelis taikomas jums išleidžiant produktus per inžinerijos keitimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="8f04c-152">This field is applicable when you re-release products via an engineering change order.</span></span> <span data-ttu-id="8f04c-153">Jums pasirinkus, ar visi produktai ar tik paveikti produktai turi būti siūlomi **Leidimų** teksto laukelyje.</span><span class="sxs-lookup"><span data-stu-id="8f04c-153">You can select whether all products or only the affected products should be proposed in the **Releases** dialog box.</span></span> |
| <span data-ttu-id="8f04c-154">KS lygiai, kuriuos reikia išleisti</span><span class="sxs-lookup"><span data-stu-id="8f04c-154">BOM levels to release</span></span> | <span data-ttu-id="8f04c-155">BOM lygio gylis leidimo metu.</span><span class="sxs-lookup"><span data-stu-id="8f04c-155">The depth of the BOM level to release.</span></span> <span data-ttu-id="8f04c-156">Jei BOM turi daugiau lygių (tai yra, jei jis gilesnis), tuomet vertė yra nurodyta čia, bus išleisti tik nurodytos vertės didesni lygiai.</span><span class="sxs-lookup"><span data-stu-id="8f04c-156">If the BOM has more levels (that is, if it's deeper) than the value that is specified here, only the levels up through the specified value will be released.</span></span> |