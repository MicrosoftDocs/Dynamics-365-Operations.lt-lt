---
title: Kurti konfigūracijos taisykles
description: Šia procedūra sukuriamos konfigūracijos taisyklės, pagal kurias, naudojant konfigūravimą pagal dimensijas, būtų galima taikyti arba neleisti taikyti tam tikrų KS eilučių kombinacijų.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d75e9ecaa814085e8fce1836125553511cf4f48b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999736"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="f2368-103">Kurti konfigūracijos taisykles</span><span class="sxs-lookup"><span data-stu-id="f2368-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2368-104">Šia procedūra sukuriamos konfigūracijos taisyklės, pagal kurias, naudojant konfigūravimą pagal dimensijas, būtų galima taikyti arba neleisti taikyti tam tikrų KS eilučių kombinacijų.</span><span class="sxs-lookup"><span data-stu-id="f2368-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="f2368-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="f2368-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f2368-106">Tai yra septintoji iš aštuonių procedūrų, kuriomis paaiškinama, kaip kurti konfigūravimo pagal dimensijas kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="f2368-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="f2368-107">Pasirinkite Produkto informacijos valdymas > Komplektavimo specifikacijos ir formulės > Komplektavimo specifikacijos.</span><span class="sxs-lookup"><span data-stu-id="f2368-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="f2368-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f2368-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f2368-109">Raskite ir pasirinkite konfigūravimo pagal dimensijas KS.</span><span class="sxs-lookup"><span data-stu-id="f2368-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="f2368-110">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="f2368-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="f2368-111">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="f2368-111">Click Change view.</span></span>
5. <span data-ttu-id="f2368-112">Spustelėkite antraštės rodinį.</span><span class="sxs-lookup"><span data-stu-id="f2368-112">Click Header view.</span></span>
    * <span data-ttu-id="f2368-113">Atidarykite antraštės rodinį, kad pasiektumėte konfigūracijos maršrutą „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="f2368-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="f2368-114">Išplėskite arba sutraukite sekciją Konfigūracijos maršrutas.</span><span class="sxs-lookup"><span data-stu-id="f2368-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="f2368-115">Konfigūracijos maršrutas „FastTab“ turi būti išplėstiniame režime.</span><span class="sxs-lookup"><span data-stu-id="f2368-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="f2368-116">Spustelėkite „Konfigūracijos taisyklės“.</span><span class="sxs-lookup"><span data-stu-id="f2368-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="f2368-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="f2368-117">Click New.</span></span>
9. <span data-ttu-id="f2368-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f2368-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="f2368-119">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f2368-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f2368-120">Rodomos prekės esamoje konfigūracijos grupėje.</span><span class="sxs-lookup"><span data-stu-id="f2368-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="f2368-121">Pasirinkite tą, kuri atitinka taisyklės sąlygą.</span><span class="sxs-lookup"><span data-stu-id="f2368-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="f2368-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f2368-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f2368-123">Lauke Metodas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f2368-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="f2368-124">Įmanoma žymėti arba atžymėti prekę iš kitos konfigūracijos grupės.</span><span class="sxs-lookup"><span data-stu-id="f2368-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="f2368-125">Lauke „Išvestinė grupė“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f2368-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f2368-126">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f2368-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f2368-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f2368-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f2368-128">Pasirinkite norimą konfigūracijos grupę.</span><span class="sxs-lookup"><span data-stu-id="f2368-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="f2368-129">Lauke „Išvestinės prekės numeris“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f2368-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="f2368-130">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f2368-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f2368-131">Pasirinkite prekės numerį, kuris bus pažymėtas arba atžymėtas, atsižvelgiant į pasirinktą metodą.</span><span class="sxs-lookup"><span data-stu-id="f2368-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="f2368-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f2368-132">Close the page.</span></span>

