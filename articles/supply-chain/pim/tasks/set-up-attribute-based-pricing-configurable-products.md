---
title: Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 534e9c9332c107afebd814cf2090ecbdf0ec6459
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914704"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="6d840-103">Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas</span><span class="sxs-lookup"><span data-stu-id="6d840-103">Set up attribute-based pricing for configurable products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d840-104">Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą.</span><span class="sxs-lookup"><span data-stu-id="6d840-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="6d840-105">Būtina sąlyga – reikalingas produkto konfigūracijos modelis, kuriame yra vienas ar daugiau komponentų ir atributų.</span><span class="sxs-lookup"><span data-stu-id="6d840-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="6d840-106">Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio produkto modelis demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="6d840-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="6d840-107">Paprastai šią procedūrą atlieka produktų vadovas.</span><span class="sxs-lookup"><span data-stu-id="6d840-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="6d840-108">Naujo kainos modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="6d840-108">Create a new price model</span></span>
1. <span data-ttu-id="6d840-109">Pagrindiniame puslapyje pasirinkite **Produkto varianto modelio aprašas**.</span><span class="sxs-lookup"><span data-stu-id="6d840-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="6d840-110">**Saitų** skyriuje pasirinkite **Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="6d840-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="6d840-111">Sąraše pasirinkite eilutę **Aukštos kokybės garsiakalbis**, tačiau nespustelėkite pavadinimo saito.</span><span class="sxs-lookup"><span data-stu-id="6d840-111">In the list, select the **High End Speaker** line, but don’t select the link for the name.</span></span>
4. <span data-ttu-id="6d840-112">Veiksmų srityje pasirinkite **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="6d840-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="6d840-113">Pasirinkite **Kainų modeliai**.</span><span class="sxs-lookup"><span data-stu-id="6d840-113">Select **Price models**.</span></span>
6. <span data-ttu-id="6d840-114">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6d840-114">Select **New**.</span></span>
7. <span data-ttu-id="6d840-115">Lauke **Kainos modelio pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6d840-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="6d840-116">Naudokite pavadinimą, pagal kurį modelį būtų lengva identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="6d840-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="6d840-117">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6d840-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="6d840-118">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6d840-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="6d840-119">Kainos elementų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="6d840-119">Add price elements</span></span>
1. <span data-ttu-id="6d840-120">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="6d840-120">Select **Edit**.</span></span> <span data-ttu-id="6d840-121">Kiekviename produkto modelio komponente gali būti bazinės kainos elementas ir bet koks kainos išraiškos taisyklių skaičius.</span><span class="sxs-lookup"><span data-stu-id="6d840-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="6d840-122">Taip pat galite įtraukti kainas skirtingomis valiutomis.</span><span class="sxs-lookup"><span data-stu-id="6d840-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="6d840-123">Lauke **Bazinės kainos išraiška** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6d840-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="6d840-124">Pavyzdžiui, įveskite 100.</span><span class="sxs-lookup"><span data-stu-id="6d840-124">For example, type 100.</span></span> <span data-ttu-id="6d840-125">Bazinės kainos išraiška gali būti skaitinė reikšmė arba ją gali sudaryti aritmetinė formulė, naudojanti vieną ar kelis atributus.</span><span class="sxs-lookup"><span data-stu-id="6d840-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="6d840-126">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="6d840-126">Select **Add**.</span></span>
4. <span data-ttu-id="6d840-127">Lauke **Pavadinimas** įveskite `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="6d840-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="6d840-128">Kainos išraiškos pavadinimas padeda identifikuoti, ką nurodo kainos elementas.</span><span class="sxs-lookup"><span data-stu-id="6d840-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="6d840-129">Šiame pavyzdyje kuriame kainos elementą, skirtą raudonmedžio garsiakalbio spintelės apdailos parinkčiai.</span><span class="sxs-lookup"><span data-stu-id="6d840-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="6d840-130">Pasirinkite **Redaguoti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="6d840-130">Select **Edit condition**.</span></span> <span data-ttu-id="6d840-131">Kainos sąlyga padeda užtikrinti, kad kainos išraiškos elementas yra įtrauktas į pardavimo kainą tik esant konkrečiam atributų deriniui.</span><span class="sxs-lookup"><span data-stu-id="6d840-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="6d840-132">Lauke **Apribojimo turinys** įveskite `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="6d840-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="6d840-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6d840-133">Select **OK**.</span></span>
8. <span data-ttu-id="6d840-134">Lauke **Išraiška** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6d840-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="6d840-135">Pavyzdžiui, įveskite `50`.</span><span class="sxs-lookup"><span data-stu-id="6d840-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="6d840-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6d840-136">Close the page.</span></span>

