---
title: Prižiūrėti atributų tipus
description: Šioje temoje aprašoma, kaip modulyje „Turto valdymas“ sukurti atributo tipą.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 469bcb16bb3099ffabdccfb026f0414de0213aaa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433891"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="f2c3a-103">Prižiūrėti atributų tipus</span><span class="sxs-lookup"><span data-stu-id="f2c3a-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f2c3a-104">Šioje temoje aprašoma, kaip modulyje „Turto valdymas“ sukurti atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="f2c3a-105">Atributai naudojami įvairių elementų ypatybėms apibūdinti.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="f2c3a-106">Kiekviename skirtuke galite nustatyti šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="f2c3a-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="f2c3a-107">Funkcinių vietų tipai</span><span class="sxs-lookup"><span data-stu-id="f2c3a-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="f2c3a-108">Funkcinių vietų kūrimas</span><span class="sxs-lookup"><span data-stu-id="f2c3a-108">Create functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="f2c3a-109">Turto tipai</span><span class="sxs-lookup"><span data-stu-id="f2c3a-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="f2c3a-110">Turtas</span><span class="sxs-lookup"><span data-stu-id="f2c3a-110">Assets</span></span>

<span data-ttu-id="f2c3a-111">Atributai, kuriuos galite nustatyti, kinta priklausomai nuo elemento.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="f2c3a-112">Pavyzdžiui, funkcinei vietovei galite nustatyti vietovės konfigūracijos ir fizinio dydžio atributus.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="f2c3a-113">Turto tipui arba turtui galite nustatyti variklio tūrio, energijos suvartojimo ir didžiausios apkrovos pajėgumo skirtingomis sąlygomis atributus.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="f2c3a-114">Atributų tipų kūrimas</span><span class="sxs-lookup"><span data-stu-id="f2c3a-114">Create attribute types</span></span>

<span data-ttu-id="f2c3a-115">Galite sukurti savo atributų tipus.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-115">You can create your own attribute types.</span></span> <span data-ttu-id="f2c3a-116">Be to, galite perkelti produkto dimensijas į puslapį **Atributų tipai**.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="f2c3a-117">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Atributų tipai**.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="f2c3a-118">Kai atributų tipus nustatote pirmą kartą, pasirinkite **Kurti produkto dimensijas**, kad automatiškai perkeltumėte standartines produkto dimensijas.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="f2c3a-119">Pasirinkite **Naujas**, kad sukurtumėte naują atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="f2c3a-120">Lauke **Atributo tipas** įveskite atributo tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="f2c3a-121">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="f2c3a-122">Lauke **Vienetas** pasirinkite atitinkamą atributo vienetą, kaip reikalaujama.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="f2c3a-123">Lauke **Duomenų tipas** pasirinkite vieneto tipą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="f2c3a-124">Jei duomenų tipu pasirinkote **Eilutė**, atlikite šiuos veiksmus, kad šiam atributo tipui sukurtumėte reikšmes:</span><span class="sxs-lookup"><span data-stu-id="f2c3a-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="f2c3a-125">Pasirinkite atributo tipą ir pasirinkite **Reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="f2c3a-126">Lauke **Atributo kodas** pasirinkite **Visi**.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="f2c3a-127">Lauke **Atributo tipas** pasirinkite atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="f2c3a-128">Lauke **Reikšmė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="f2c3a-129">Lauke **Aprašymas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="f2c3a-130">Įrašykite įrašą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-130">Save the record.</span></span>
    7. <span data-ttu-id="f2c3a-131">Grįžkite į puslapį **Atributų tipai**.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="f2c3a-132">Įrašykite įrašą.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-132">Save the record.</span></span>

    <span data-ttu-id="f2c3a-133">Lauke **Funkcinių vietovių tipai** rodomas funkcinių vietovių, kurios naudoja šį atributo tipą, skaičius.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="f2c3a-134">Lauke **Turto tipai** rodomas jį naudojančių turto tipų skaičius.</span><span class="sxs-lookup"><span data-stu-id="f2c3a-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
