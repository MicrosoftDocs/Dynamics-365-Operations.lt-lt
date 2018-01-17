--- 
title: "Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas"
description: "Šioje procedūroje parodoma, kaip nustatyti atributais pagrįstą kainodarą."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b4cddb3427e3e94d9db9a095a8e8c60bdeb9cc95
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="abc69-103">Atributais pagrįstos konfigūruojamų produktų kainodaros nustatymas</span><span class="sxs-lookup"><span data-stu-id="abc69-103">Set up attribute-based pricing for configurable products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="abc69-104">Šioje procedūroje parodoma, kaip nustatyti atributais pagrįstą kainodarą.</span><span class="sxs-lookup"><span data-stu-id="abc69-104">This procedure shows how to set up attribute-based pricing.</span></span> <span data-ttu-id="abc69-105">Būtina sąlyga – reikalingas produkto konfigūracijos modelis, kuriame yra vienas ar daugiau komponentų ir atributų.</span><span class="sxs-lookup"><span data-stu-id="abc69-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="abc69-106">Šiame pavyzdyje naudojamas aukščiausios klasės garsiakalbio produkto modelis demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="abc69-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="abc69-107">Paprastai šią procedūrą atlieka produktų vadovas.</span><span class="sxs-lookup"><span data-stu-id="abc69-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="abc69-108">Naujo kainos modelio kūrimas</span><span class="sxs-lookup"><span data-stu-id="abc69-108">Create a new price model</span></span>
1. <span data-ttu-id="abc69-109">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="abc69-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="abc69-110">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="abc69-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="abc69-111">Sąraše pasirinkite aukščiausios kokybės garsiakalbio eilutę, bet nespustelėkite pavadinimo nuorodos.</span><span class="sxs-lookup"><span data-stu-id="abc69-111">In the list, select the High End Speaker line, but don’t click the link for the name.</span></span>
4. <span data-ttu-id="abc69-112">Veiksmų srityje spustelėkite Modelis.</span><span class="sxs-lookup"><span data-stu-id="abc69-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="abc69-113">Spustelėkite Kainos modeliai.</span><span class="sxs-lookup"><span data-stu-id="abc69-113">Click Price models.</span></span>
6. <span data-ttu-id="abc69-114">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="abc69-114">Click New.</span></span>
7. <span data-ttu-id="abc69-115">Lauke Kainos modelio pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="abc69-115">In the Price model name field, type a value.</span></span>
    * <span data-ttu-id="abc69-116">Naudokite pavadinimą, pagal kurį modelį būtų lengva identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="abc69-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="abc69-117">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="abc69-117">In the Description field, type a value.</span></span>
9. <span data-ttu-id="abc69-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="abc69-118">Click Save.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="abc69-119">Kainos elementų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="abc69-119">Add price elements</span></span>
1. <span data-ttu-id="abc69-120">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="abc69-120">Click Edit.</span></span>
    * <span data-ttu-id="abc69-121">Kiekviename produkto modelio komponente gali būti bazinės kainos elementas ir bet koks kainos išraiškos taisyklių skaičius.</span><span class="sxs-lookup"><span data-stu-id="abc69-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="abc69-122">Taip pat galite įtraukti kainas skirtingomis valiutomis.</span><span class="sxs-lookup"><span data-stu-id="abc69-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="abc69-123">Lauke Bazinės kainos išraiška įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="abc69-123">In the Base price expression field, type a value.</span></span>
    * <span data-ttu-id="abc69-124">Pavyzdžiui, įveskite 100.</span><span class="sxs-lookup"><span data-stu-id="abc69-124">For example, type 100.</span></span>   <span data-ttu-id="abc69-125">Bazinės kainos išraiška gali būti skaitinė reikšmė arba ją gali sudaryti aritmetinė formulė, naudojanti vieną ar kelis atributus.</span><span class="sxs-lookup"><span data-stu-id="abc69-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="abc69-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="abc69-126">Click Add.</span></span>
4. <span data-ttu-id="abc69-127">Lauke Pavadinimas įveskite Raudonmedžio.</span><span class="sxs-lookup"><span data-stu-id="abc69-127">In the Name field, type ‘Rosewood’.</span></span>
    * <span data-ttu-id="abc69-128">Kainos išraiškos pavadinimas padeda identifikuoti, ką nurodo kainos elementas.</span><span class="sxs-lookup"><span data-stu-id="abc69-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="abc69-129">Šiame pavyzdyje kuriame kainos elementą, skirtą raudonmedžio garsiakalbio spintelės apdailos parinkčiai.</span><span class="sxs-lookup"><span data-stu-id="abc69-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="abc69-130">Spustelėkite Redaguoti sąlygą.</span><span class="sxs-lookup"><span data-stu-id="abc69-130">Click Edit condition.</span></span>
    * <span data-ttu-id="abc69-131">Kainos sąlyga padeda užtikrinti, kad kainos išraiškos elementas yra įtrauktas į pardavimo kainą tik esant konkrečiam atributų deriniui.</span><span class="sxs-lookup"><span data-stu-id="abc69-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="abc69-132">Lauke ConstraintBody įveskite CabinetFinish=="Rosewood".</span><span class="sxs-lookup"><span data-stu-id="abc69-132">In the ConstraintBody field, enter 'CabinetFinish=="Rosewood"'.</span></span>
7. <span data-ttu-id="abc69-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="abc69-133">Click OK.</span></span>
8. <span data-ttu-id="abc69-134">Lauke Išraiška įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="abc69-134">In the Expression field, type a value.</span></span>
    * <span data-ttu-id="abc69-135">Pavyzdžiui, įveskite 50.</span><span class="sxs-lookup"><span data-stu-id="abc69-135">For example, type 50.</span></span>  
9. <span data-ttu-id="abc69-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abc69-136">Close the page.</span></span>
10. <span data-ttu-id="abc69-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abc69-137">Close the page.</span></span>


