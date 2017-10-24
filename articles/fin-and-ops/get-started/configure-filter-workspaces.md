---
title: "Darbo sričių konfigūravimas ir filtravimas"
description: "Šiame straipsnyje pateikiama apžvalga apie tai, kaip konfigūruoti ir filtruoti darbo sritis."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 754cd81a4550318de7003d847fafb2bcc7414b32
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="configure-and-filter-workspaces"></a><span data-ttu-id="04554-103">Darbo sričių konfigūravimas ir filtravimas</span><span class="sxs-lookup"><span data-stu-id="04554-103">Configure and filter workspaces</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="04554-104">Šiame straipsnyje pateikiama apžvalga apie tai, kaip konfigūruoti ir filtruoti darbo sritis.</span><span class="sxs-lookup"><span data-stu-id="04554-104">This article provides an overview about how to configure and filter workspaces.</span></span>

<a name="configuring-a-workspace"></a><span data-ttu-id="04554-105">Darbo srities konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="04554-105">Configuring a workspace</span></span>
-----------------------

<span data-ttu-id="04554-106">Galite keisti kai kurių darbo sričių išvaizdą ir veikimą, atnaujinę parametrus, taikomus visai sričiai.</span><span class="sxs-lookup"><span data-stu-id="04554-106">You can change the appearance and behavior of some workspaces by updating settings that apply to the whole workspace.</span></span> <span data-ttu-id="04554-107">Kai galima konfigūruoti darbo sritį, Veiksmų srityje yra mygtukas, kuris nurodo jį spustelėti, norint atlikti konfigūracijos pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="04554-107">When a workspace can be configured, the Action Pane includes a button that instructs you to click it to make configuration changes.</span></span> <span data-ttu-id="04554-108">Pvz., toliau pateikiamoje iliustracijoje mygtukas pavadintas **Konfigūruoti mano darbo sritį**.</span><span class="sxs-lookup"><span data-stu-id="04554-108">For example, in the following illustration, the button is named **Configure my workspace**.</span></span> 

<span data-ttu-id="04554-109">[![configure-and-filter-workspaces](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="04554-109">[![configure-and-filter-workspaces](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)</span></span>   

<span data-ttu-id="04554-110">Spustelėjus mygtuką, atidaromas dialogo langas, kuriame galite modifikuoti iš anksto nustatytus darbo srities parametrus.</span><span class="sxs-lookup"><span data-stu-id="04554-110">When you click the button, a dialog appears, where you can modify the predefined settings for the workspace.</span></span> <span data-ttu-id="04554-111">Šiame dialogo lange matomi konkretūs parametrai skiriasi kiekvienoje darbo srityje, ir priklauso nuo darbo srityje esančių konkrečių valdiklių bei verslo duomenų.</span><span class="sxs-lookup"><span data-stu-id="04554-111">The specific settings that you see in this dialog vary by workspace, and depend on the specific controls and business data that are available in the workspace.</span></span> 

<span data-ttu-id="04554-112">[![configure-my-workspace](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span><span class="sxs-lookup"><span data-stu-id="04554-112">[![configure-my-workspace](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)</span></span>

## <a name="filtering-a-workspace"></a><span data-ttu-id="04554-113">Darbo srities filtravimas</span><span class="sxs-lookup"><span data-stu-id="04554-113">Filtering a workspace</span></span>
<span data-ttu-id="04554-114">Daugelyje sričių leidžiama filtruoti juose rodomą turinį.</span><span class="sxs-lookup"><span data-stu-id="04554-114">Many workspaces let you filter the content that appears in them.</span></span> <span data-ttu-id="04554-115">Galimi valdikliai leidžia filtruoti visą darbo srities turinį arba tik konkrečiame darbo srities skyriuje esantį turinį.</span><span class="sxs-lookup"><span data-stu-id="04554-115">The controls that are available might let you filter all the content in the workspace or only the content in a specific section of the workspace.</span></span> <span data-ttu-id="04554-116">Darbo sričių filtrai gali būti peržvalgos, pasirinktinio įvedimo laukai, laisvos formos teksto laukai ar kitų tipų valdikliai.</span><span class="sxs-lookup"><span data-stu-id="04554-116">The filters on workspaces can be lookups, combo boxes, free-form text fields, or other types of controls.</span></span> <span data-ttu-id="04554-117">Tačiau visų tipų filtrų poveikis yra toks pat, kaip aprašyta tolesniuose skyriuose.</span><span class="sxs-lookup"><span data-stu-id="04554-117">However, every type of filter has the same effects, as described in the following sections.</span></span>

### <a name="workspace-wide-filters"></a><span data-ttu-id="04554-118">Visos darbo srities filtrai</span><span class="sxs-lookup"><span data-stu-id="04554-118">Workspace-wide filters</span></span>

<span data-ttu-id="04554-119">Naudodami visos darbo srities filtrą, galite filtruoti visą darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="04554-119">You can filter the whole workspace by using a workspace-wide filter.</span></span> <span data-ttu-id="04554-120">Visos darbo srities filtrą rasite viršutiniame kairiajame darbo srities kampe.</span><span class="sxs-lookup"><span data-stu-id="04554-120">A workspace-wide filter appears in the upper-left corner of the workspace.</span></span> <span data-ttu-id="04554-121">Išplečiamajame filtro sąraše pasirinkus konkrečią vertę, darbo srities turinys filtruojamas pagal tą pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="04554-121">When you select a specific value in the drop-down list, the contents of the workspace are filtered based on that selection.</span></span> 

<span data-ttu-id="04554-122">[![workspace-filter](./media/workspace-filter.png)](./media/workspace-filter.png)</span><span class="sxs-lookup"><span data-stu-id="04554-122">[![workspace-filter](./media/workspace-filter.png)](./media/workspace-filter.png)</span></span> 

<span data-ttu-id="04554-123">Kai, norėdami atidaryti filtrą, jį spustelėsite, jums bus pateiktos kelios pasirinktys.</span><span class="sxs-lookup"><span data-stu-id="04554-123">When you click to open the filter, you're presented with several options.</span></span> 

<span data-ttu-id="04554-124">[![workspace-filter-expanded](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span><span class="sxs-lookup"><span data-stu-id="04554-124">[![workspace-filter-expanded](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)</span></span> 

<span data-ttu-id="04554-125">Pasirinkite pasirinktį, pagal kurią turėtų būti filtruojama darbo sritis.</span><span class="sxs-lookup"><span data-stu-id="04554-125">Select an option to filter the workspace based on that option.</span></span>

### <a name="workspace-section-filters"></a><span data-ttu-id="04554-126">Darbo srities dalių filtrai</span><span class="sxs-lookup"><span data-stu-id="04554-126">Workspace section filters</span></span>

<span data-ttu-id="04554-127">Jei atskiruose darbo srities skyriuose yra filtrai, galite filtruoti kiekvieną sritį atskirai.</span><span class="sxs-lookup"><span data-stu-id="04554-127">If individual sections of the workspace have filters, you can filter each section separately.</span></span> <span data-ttu-id="04554-128">Toliau pateikiamoje iliustracijoje filtras (laukas, kuriame yra tekstas „Filtras), yra laisvos formos teksto laiko filtro pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="04554-128">In the following illustration, the filter (the field that contains the text "Filter") is an example of a free-form text field filter.</span></span> 

<span data-ttu-id="04554-129">[![workspace-section-filters](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span><span class="sxs-lookup"><span data-stu-id="04554-129">[![workspace-section-filters](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)</span></span> 

<span data-ttu-id="04554-130">Kaip ir su visos darbo srities filtru, pasirinkite arba įveskite vertę į lauką, norėdami filtruoti skyriaus turinį.</span><span class="sxs-lookup"><span data-stu-id="04554-130">As with a workspace-wide filter, select or enter a value in the field to filter the contents of the section.</span></span>




