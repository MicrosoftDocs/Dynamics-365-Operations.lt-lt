---
title: Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921246"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="e39a1-103">Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas</span><span class="sxs-lookup"><span data-stu-id="e39a1-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e39a1-104">Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą.</span><span class="sxs-lookup"><span data-stu-id="e39a1-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="e39a1-105">Būtina sąlyga – reikalingas produkto konfigūracijos modelis, kuriame yra vienas ar daugiau komponentų ir atributų.</span><span class="sxs-lookup"><span data-stu-id="e39a1-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="e39a1-106">Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio produkto modelis demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="e39a1-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="e39a1-107">Paprastai šią procedūrą atlieka produktų vadovas.</span><span class="sxs-lookup"><span data-stu-id="e39a1-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="e39a1-108">Naujo kainos modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="e39a1-108">Create a new price model</span></span>

1. <span data-ttu-id="e39a1-109">Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="e39a1-110">Sąraše pasirinkite eilutę **Aukščiausios klasės garsiakalbis**, bet nepasirinkite vardo nuorodos.</span><span class="sxs-lookup"><span data-stu-id="e39a1-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="e39a1-111">Veiksmų srityje pasirinkite **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="e39a1-112">Pasirinkite **Kainų modeliai**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-112">Select **Price models**.</span></span>
1. <span data-ttu-id="e39a1-113">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-113">Select **New**.</span></span>
1. <span data-ttu-id="e39a1-114">Lauke **Kainos modelio pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e39a1-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="e39a1-115">Naudokite pavadinimą, pagal kurį modelį būtų lengva identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="e39a1-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="e39a1-116">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e39a1-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="e39a1-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="e39a1-118">Kainos elementų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="e39a1-118">Add price elements</span></span>

1. <span data-ttu-id="e39a1-119">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-119">Select **Edit**.</span></span> <span data-ttu-id="e39a1-120">Kiekviename produkto modelio komponente gali būti bazinės kainos elementas ir bet koks kainos išraiškos taisyklių skaičius.</span><span class="sxs-lookup"><span data-stu-id="e39a1-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="e39a1-121">Taip pat galite įtraukti kainas skirtingomis valiutomis.</span><span class="sxs-lookup"><span data-stu-id="e39a1-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="e39a1-122">Lauke **Bazinės kainos išraiška** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e39a1-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="e39a1-123">Pavyzdžiui, įveskite 100.</span><span class="sxs-lookup"><span data-stu-id="e39a1-123">For example, type 100.</span></span> <span data-ttu-id="e39a1-124">Bazinės kainos išraiška gali būti skaitinė reikšmė arba ją gali sudaryti aritmetinė formulė, naudojanti vieną ar kelis atributus.</span><span class="sxs-lookup"><span data-stu-id="e39a1-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="e39a1-125">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-125">Select **Add**.</span></span>
4. <span data-ttu-id="e39a1-126">Lauke **Pavadinimas** įveskite `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="e39a1-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="e39a1-127">Kainos išraiškos pavadinimas padeda identifikuoti, ką nurodo kainos elementas.</span><span class="sxs-lookup"><span data-stu-id="e39a1-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="e39a1-128">Šiame pavyzdyje kuriame kainos elementą, skirtą raudonmedžio garsiakalbio spintelės apdailos parinkčiai.</span><span class="sxs-lookup"><span data-stu-id="e39a1-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="e39a1-129">Pasirinkite **Redaguoti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-129">Select **Edit condition**.</span></span> <span data-ttu-id="e39a1-130">Kainos sąlyga padeda užtikrinti, kad kainos išraiškos elementas yra įtrauktas į pardavimo kainą tik esant konkrečiam atributų deriniui.</span><span class="sxs-lookup"><span data-stu-id="e39a1-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="e39a1-131">Lauke **Apribojimo turinys** įveskite `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="e39a1-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="e39a1-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e39a1-132">Select **OK**.</span></span>
8. <span data-ttu-id="e39a1-133">Lauke **Išraiška** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e39a1-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="e39a1-134">Pavyzdžiui, įveskite `50`.</span><span class="sxs-lookup"><span data-stu-id="e39a1-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="e39a1-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="e39a1-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]