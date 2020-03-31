---
title: Naujos produkto hierarchijos kūrimas
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ sukuti naują produkto hierarchiją.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 724ec2e5af7837d574298d662911cd9c6ee9e9f2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070426"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="5c900-103">Naujos produkto hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="5c900-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5c900-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ sukuti naują produkto hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="5c900-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c900-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="5c900-105">Overview</span></span>

<span data-ttu-id="5c900-106">„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus.</span><span class="sxs-lookup"><span data-stu-id="5c900-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="5c900-107">Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis).</span><span class="sxs-lookup"><span data-stu-id="5c900-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="5c900-108">Kiekviename mažmeninės prekybos parduotuvės kanale gali būti naudojami savi mokėjimo būdai, kainų grupės, elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai.</span><span class="sxs-lookup"><span data-stu-id="5c900-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="5c900-109">Prieš kurdami mažmeninės prekybos parduotuvės kanalą, turite nustatyti visus šiuos elementus.</span><span class="sxs-lookup"><span data-stu-id="5c900-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="5c900-110">Prekybos produktų hierarchija naudojama norint nurodyti bendrą organizacijos produktų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="5c900-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="5c900-111">Prekybos produktų hierarchiją galite naudoti reklamavimo, kainų nustatymo ir akcijų, ataskaitų teikimo ir asortimento planavimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="5c900-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="5c900-112">Vienai organizacijai galima priskirti tik vieną prekybos produktų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="5c900-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="5c900-113">Produkto hierarchijos kūrimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5c900-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="5c900-114">Norėdami sukurti ir sukonfigūruoti prekybos produktų hierarchiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5c900-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5c900-115">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Prekybos produktų hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="5c900-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="5c900-116">Jei hierarchijos dar nėra, pasirinkę **Veiksmų sritis**, pasirinkite **Nauja**, norėdami sukurti hierarchijos šakninį katalogą.</span><span class="sxs-lookup"><span data-stu-id="5c900-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="5c900-117">Srityje **Bendra** atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5c900-117">Under **General**:</span></span>
    1. <span data-ttu-id="5c900-118">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5c900-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="5c900-119">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="5c900-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="5c900-120">Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5c900-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="5c900-121">Parinktyje **Aktyvusis** nustatykite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="5c900-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="5c900-122">Hierarchijos mazgų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="5c900-122">Add hierarchy nodes</span></span>

<span data-ttu-id="5c900-123">Norėdami įtraukti hierarchijos mazgų, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5c900-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="5c900-124">Veiksmų srityje pasirinkite **Redaguoti kategorijų hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="5c900-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="5c900-125">Pasirinkite pirminį mazgą, į kurį norite įtraukti naują mazgą, tada pasirinkite **Naujas kategorijos mazgas**.</span><span class="sxs-lookup"><span data-stu-id="5c900-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="5c900-126">Skyriuje **Bendra** pateikite **Pavadinimas**, **Aprašas**, **Patogus pavadinimas** ir **Raktažodžiai**.</span><span class="sxs-lookup"><span data-stu-id="5c900-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="5c900-127">Srityje **Bendra** atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5c900-127">Under **General**:</span></span>
    1. <span data-ttu-id="5c900-128">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5c900-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="5c900-129">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="5c900-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="5c900-130">Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5c900-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="5c900-131">Langelyje **Raktažodžiai** įveskite atitinkamus raktažodžius.</span><span class="sxs-lookup"><span data-stu-id="5c900-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="5c900-132">Langelyje **Rodymo tvarka** įveskite rodymo tvarkos numerį (nebūtina).</span><span class="sxs-lookup"><span data-stu-id="5c900-132">In the **Display order**box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="5c900-133">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="5c900-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="5c900-134">Norėdami įtraukti papildomų mazgų, pakartokite pirmiau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5c900-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="5c900-135">Toliau pateiktame vaizde parodytas naujo produkto hierarchijos mazgo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="5c900-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Produkto hierarchijos kūrimas](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="5c900-137">Kiti parametrai</span><span class="sxs-lookup"><span data-stu-id="5c900-137">Other settings</span></span>

<span data-ttu-id="5c900-138">Kategorijos atributų grupes taip pat galima priskirti kiekvienai grupei, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="5c900-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="5c900-139">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5c900-139">Additional resources</span></span>

[<span data-ttu-id="5c900-140">prekybos hierarchijos</span><span class="sxs-lookup"><span data-stu-id="5c900-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="5c900-141">Produktų kategorijų ir produktų valdymas </span><span class="sxs-lookup"><span data-stu-id="5c900-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="5c900-142">Prekybos objektų rūšiavimo tvarkos keitimas</span><span class="sxs-lookup"><span data-stu-id="5c900-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)