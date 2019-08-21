---
title: Prižiūrėti atributų tipus
description: Šioje temoje aprašoma, kaip modulyje „Turto valdymas“ sukurti atributo tipą.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783454"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="bf729-103">Prižiūrėti atributų tipus</span><span class="sxs-lookup"><span data-stu-id="bf729-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="bf729-104">Šioje temoje aprašoma, kaip modulyje „Turto valdymas“ sukurti atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="bf729-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="bf729-105">Atributai naudojami įvairių elementų ypatybėms apibūdinti.</span><span class="sxs-lookup"><span data-stu-id="bf729-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="bf729-106">Kiekviename skirtuke galite nustatyti šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="bf729-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="bf729-107">Funkcinių vietovių tipai</span><span class="sxs-lookup"><span data-stu-id="bf729-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="bf729-108">Funkcinės vietovės</span><span class="sxs-lookup"><span data-stu-id="bf729-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="bf729-109">Turto tipas</span><span class="sxs-lookup"><span data-stu-id="bf729-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="bf729-110">Turtas</span><span class="sxs-lookup"><span data-stu-id="bf729-110">Assets</span></span>

<span data-ttu-id="bf729-111">Atributai, kuriuos galite nustatyti, kinta priklausomai nuo elemento.</span><span class="sxs-lookup"><span data-stu-id="bf729-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="bf729-112">Pavyzdžiui, funkcinei vietovei galite nustatyti vietovės konfigūracijos ir fizinio dydžio atributus.</span><span class="sxs-lookup"><span data-stu-id="bf729-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="bf729-113">Turto tipui arba turtui galite nustatyti variklio tūrio, energijos suvartojimo ir didžiausios apkrovos pajėgumo skirtingomis sąlygomis atributus.</span><span class="sxs-lookup"><span data-stu-id="bf729-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="bf729-114">Atributų tipų kūrimas</span><span class="sxs-lookup"><span data-stu-id="bf729-114">Create attribute types</span></span>

<span data-ttu-id="bf729-115">Galite sukurti savo atributų tipus.</span><span class="sxs-lookup"><span data-stu-id="bf729-115">You can create your own attribute types.</span></span> <span data-ttu-id="bf729-116">Be to, galite perkelti produkto dimensijas iš Microsoft Dynamics 365 for Finance and Operations į puslapį **Attribute types**.</span><span class="sxs-lookup"><span data-stu-id="bf729-116">Additionally, you can transfer product dimensions from Microsoft Dynamics 365 for Finance and Operations to the **Attribute types** page.</span></span>

1. <span data-ttu-id="bf729-117">Pasirinkite **Asset management** \> **Setup** \> **Attribute types**.</span><span class="sxs-lookup"><span data-stu-id="bf729-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="bf729-118">Kai atributus nustatote pirmą kartą, pasirinkite **Create product dimensions**, kad automatiškai perkeltumėte standartines „Finance and Operations“ produkto dimensijas.</span><span class="sxs-lookup"><span data-stu-id="bf729-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard Finance and Operations product dimensions.</span></span>
3. <span data-ttu-id="bf729-119">Pasirinkite **New**, kad sukurtumėte naują atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="bf729-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="bf729-120">Lauke **Attribute type** įveskite atributo tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bf729-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="bf729-121">Lauke **Description** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="bf729-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="bf729-122">Lauke **Vienetas** pasirinkite atitinkamą atributo vienetą, kaip reikalaujama.</span><span class="sxs-lookup"><span data-stu-id="bf729-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="bf729-123">Lauke **Data type**pasirinkite paketo tipą</span><span class="sxs-lookup"><span data-stu-id="bf729-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="bf729-124">Jei duomenų tipu pasirinkote **String**, atlikite šiuos veiksmus, kad šiam atributo tipui sukurtumėte reikšmes:</span><span class="sxs-lookup"><span data-stu-id="bf729-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="bf729-125">Pasirinkite atributo tipą ir pasirinkite **reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="bf729-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="bf729-126">Lauke **Atributo kodas** pasirinkite **Visi**.</span><span class="sxs-lookup"><span data-stu-id="bf729-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="bf729-127">Lauke **Atributo tipas** pasirinkite atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="bf729-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="bf729-128">Lauke **Value** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bf729-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="bf729-129">Lauke **Description** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="bf729-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="bf729-130">Įrašykite įrašą.</span><span class="sxs-lookup"><span data-stu-id="bf729-130">Save the record.</span></span>
    7. <span data-ttu-id="bf729-131">Grįžkite į puslapį **Attribute types**.</span><span class="sxs-lookup"><span data-stu-id="bf729-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="bf729-132">Įrašykite įrašą.</span><span class="sxs-lookup"><span data-stu-id="bf729-132">Save the record.</span></span>

    <span data-ttu-id="bf729-133">Lauke **Funkcinių vietovių tipai** rodomas funkcinių vietovių, kurios naudoja šį atributo tipą, skaičius.</span><span class="sxs-lookup"><span data-stu-id="bf729-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="bf729-134">Lauke **Turto tipai** rodomas jį naudojančių turto tipų skaičius.</span><span class="sxs-lookup"><span data-stu-id="bf729-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
