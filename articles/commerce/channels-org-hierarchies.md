---
title: Organizacijų hierarchijų nustatymas
description: Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Commerce“ organizacijos hierarchijas.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800572"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="80d60-103">Organizacijų hierarchijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="80d60-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="80d60-104">Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Commerce“ organizacijos hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="80d60-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="80d60-105">Prieš kurdami kanalus turite įsitikinti, kad jums reikia nustatyti organizacijos hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="80d60-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="80d60-106">Naudodami organizacijos hierarchijas galite peržiūrėti informaciją apie įvairius savo įmonės aspektus ir sukurti atitinkamas ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="80d60-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="80d60-107">Pavyzdžiui, galite nustatyti vieną hierarchiją, skirtą mokesčių, juridinėms arba privalomoms ataskaitoms kurti.</span><span class="sxs-lookup"><span data-stu-id="80d60-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="80d60-108">Tada galite nustatyti kitą hierarchiją, kad būtų kuriamos finansinės informacijos, kurios nebūtina pateikti, bet kuri naudojama vidaus ataskaitose, ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="80d60-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="80d60-109">Prieš kurdami organizacijos hierarchiją turite sukurti organizacijas.</span><span class="sxs-lookup"><span data-stu-id="80d60-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="80d60-110">Daugiau informacijos žr. [Juridinių subjektų kūrimas](channels-legal-entities.md) arba [Valdymo vienetų kūrimas](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="80d60-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="80d60-111">Daugiau informacijos ieškokite šiose temose.</span><span class="sxs-lookup"><span data-stu-id="80d60-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="80d60-112">Organizacijų ir organizacijų hierarchijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="80d60-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="80d60-113">Organizacijos hierarchijos planavimas</span><span class="sxs-lookup"><span data-stu-id="80d60-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="80d60-114">Organizacijos hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="80d60-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="80d60-115">Organizacijos hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="80d60-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="80d60-116">Norėdami sukurti organizacijos hierarchiją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80d60-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="80d60-117">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Organizacijos hierarchijos**.</span><span class="sxs-lookup"><span data-stu-id="80d60-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="80d60-118">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="80d60-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="80d60-119">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="80d60-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="80d60-120">Skyriuje **Tikslas** pasirinkite **Priskirti tikslą**.</span><span class="sxs-lookup"><span data-stu-id="80d60-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="80d60-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="80d60-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="80d60-122">Pasirinkite paskirtį, priskirtiną jūsų organizacijos hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="80d60-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="80d60-123">Skyriuje **Priskirtos hierarchijos** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="80d60-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="80d60-124">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="80d60-124">In the list, mark the selected row.</span></span> <span data-ttu-id="80d60-125">Suraskite ką tik savo sukurtą hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="80d60-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="80d60-126">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="80d60-126">Select **OK**.</span></span>

<span data-ttu-id="80d60-127">Toliau pateiktame paveiksle rodomas organizacijos hierarchijos, sukurtos fiktyviam „Adventure Works“ parduotuvių tinklui, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="80d60-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![Organizacijos hierarchijos pavyzdys](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="80d60-129">Organizacijų įtraukimas į hierarchiją</span><span class="sxs-lookup"><span data-stu-id="80d60-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="80d60-130">Norėdami įtraukti organizacijas į hierarchiją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80d60-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="80d60-131">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="80d60-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="80d60-132">Pasirinkite savo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="80d60-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="80d60-133">Veiksmų srityje pasirinkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="80d60-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="80d60-134">Pagal poreikį įtraukite organizacijų.</span><span class="sxs-lookup"><span data-stu-id="80d60-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="80d60-135">Norėdami įtraukti organizaciją, pasirinkite **Redaguoti** ir pasirinkite **Įterpti**.</span><span class="sxs-lookup"><span data-stu-id="80d60-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="80d60-136">Atlikę visus norimus pakeitimus, galite įrašyti juodraštį ir publikuoti pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="80d60-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="80d60-137">Toliau pateiktame paveiksle rodomas juridinis subjektas, įtrauktas į hierarchijos šaknį su keturiais išlaidų centrais, skirtais kanalams „Prekybos centras“, „Parduotuvė“, „Internetinė parduotuvė“ ir „Skambučių centras“.</span><span class="sxs-lookup"><span data-stu-id="80d60-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="80d60-138">Po to į kiekvieną galima įtraukti įvairius mažmeninės prekybos, skambučių centro ir internetinės parduotuvės kanalus.</span><span class="sxs-lookup"><span data-stu-id="80d60-138">Various retail, call center and online channels can then be added to each.</span></span>

![Hierarchijos konstruktoriaus pavyzdys](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="80d60-140">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="80d60-140">Additional resources</span></span>

[<span data-ttu-id="80d60-141">Organizacijų ir organizacijų hierarchijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="80d60-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="80d60-142">Organizacijos hierarchijos planavimas</span><span class="sxs-lookup"><span data-stu-id="80d60-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="80d60-143">Juridinių subjektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="80d60-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="80d60-144">Valdymo vienetų kūrimas</span><span class="sxs-lookup"><span data-stu-id="80d60-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="80d60-145">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="80d60-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="80d60-146">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="80d60-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
