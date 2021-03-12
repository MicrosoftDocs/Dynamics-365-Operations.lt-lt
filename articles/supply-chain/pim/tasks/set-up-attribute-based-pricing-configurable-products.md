---
title: Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2f9a78902ff1a0333c46c8ad9142338678b6e7d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986784"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="3d1ea-103">Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas</span><span class="sxs-lookup"><span data-stu-id="3d1ea-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d1ea-104">Šioje temoje paaiškinta, kaip nustatyti atributais pagrįstą kainodarą.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="3d1ea-105">Būtina sąlyga – reikalingas produkto konfigūracijos modelis, kuriame yra vienas ar daugiau komponentų ir atributų.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="3d1ea-106">Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio produkto modelis demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="3d1ea-107">Paprastai šią procedūrą atlieka produktų vadovas.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="3d1ea-108">Naujo kainos modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="3d1ea-108">Create a new price model</span></span>
1. <span data-ttu-id="3d1ea-109">Pagrindiniame puslapyje pasirinkite **Produkto varianto modelio aprašas**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="3d1ea-110">**Saitų** skyriuje pasirinkite **Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="3d1ea-111">Sąraše pasirinkite eilutę **Aukščiausios klasės garsiakalbis**, bet nepasirinkite vardo nuorodos.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="3d1ea-112">Veiksmų srityje pasirinkite **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="3d1ea-113">Pasirinkite **Kainų modeliai**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-113">Select **Price models**.</span></span>
6. <span data-ttu-id="3d1ea-114">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-114">Select **New**.</span></span>
7. <span data-ttu-id="3d1ea-115">Lauke **Kainos modelio pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="3d1ea-116">Naudokite pavadinimą, pagal kurį modelį būtų lengva identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="3d1ea-117">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="3d1ea-118">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="3d1ea-119">Kainos elementų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="3d1ea-119">Add price elements</span></span>
1. <span data-ttu-id="3d1ea-120">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-120">Select **Edit**.</span></span> <span data-ttu-id="3d1ea-121">Kiekviename produkto modelio komponente gali būti bazinės kainos elementas ir bet koks kainos išraiškos taisyklių skaičius.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="3d1ea-122">Taip pat galite įtraukti kainas skirtingomis valiutomis.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="3d1ea-123">Lauke **Bazinės kainos išraiška** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="3d1ea-124">Pavyzdžiui, įveskite 100.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-124">For example, type 100.</span></span> <span data-ttu-id="3d1ea-125">Bazinės kainos išraiška gali būti skaitinė reikšmė arba ją gali sudaryti aritmetinė formulė, naudojanti vieną ar kelis atributus.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="3d1ea-126">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-126">Select **Add**.</span></span>
4. <span data-ttu-id="3d1ea-127">Lauke **Pavadinimas** įveskite `Rosewood`.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="3d1ea-128">Kainos išraiškos pavadinimas padeda identifikuoti, ką nurodo kainos elementas.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="3d1ea-129">Šiame pavyzdyje kuriame kainos elementą, skirtą raudonmedžio garsiakalbio spintelės apdailos parinkčiai.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="3d1ea-130">Pasirinkite **Redaguoti sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-130">Select **Edit condition**.</span></span> <span data-ttu-id="3d1ea-131">Kainos sąlyga padeda užtikrinti, kad kainos išraiškos elementas yra įtrauktas į pardavimo kainą tik esant konkrečiam atributų deriniui.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="3d1ea-132">Lauke **Apribojimo turinys** įveskite `CabinetFinish=="Rosewood"`.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="3d1ea-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-133">Select **OK**.</span></span>
8. <span data-ttu-id="3d1ea-134">Lauke **Išraiška** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="3d1ea-135">Pavyzdžiui, įveskite `50`.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="3d1ea-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3d1ea-136">Close the page.</span></span>

