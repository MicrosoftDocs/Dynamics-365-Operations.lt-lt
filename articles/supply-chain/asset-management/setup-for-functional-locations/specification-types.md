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
ms.openlocfilehash: 067d1085d9afa04cb76b78393a8a8b9834ce4d8c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250949"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="32fb0-103">Prižiūrėti atributų tipus</span><span class="sxs-lookup"><span data-stu-id="32fb0-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="32fb0-104">Šioje temoje aprašoma, kaip modulyje „Turto valdymas“ sukurti atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="32fb0-105">Atributai naudojami įvairių elementų ypatybėms apibūdinti.</span><span class="sxs-lookup"><span data-stu-id="32fb0-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="32fb0-106">Kiekviename skirtuke galite nustatyti šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="32fb0-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="32fb0-107">Funkcinių vietovių tipai</span><span class="sxs-lookup"><span data-stu-id="32fb0-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="32fb0-108">Funkcinės vietovės</span><span class="sxs-lookup"><span data-stu-id="32fb0-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="32fb0-109">Turto tipas</span><span class="sxs-lookup"><span data-stu-id="32fb0-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="32fb0-110">Turtas</span><span class="sxs-lookup"><span data-stu-id="32fb0-110">Assets</span></span>

<span data-ttu-id="32fb0-111">Atributai, kuriuos galite nustatyti, kinta priklausomai nuo elemento.</span><span class="sxs-lookup"><span data-stu-id="32fb0-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="32fb0-112">Pavyzdžiui, funkcinei vietovei galite nustatyti vietovės konfigūracijos ir fizinio dydžio atributus.</span><span class="sxs-lookup"><span data-stu-id="32fb0-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="32fb0-113">Turto tipui arba turtui galite nustatyti variklio tūrio, energijos suvartojimo ir didžiausios apkrovos pajėgumo skirtingomis sąlygomis atributus.</span><span class="sxs-lookup"><span data-stu-id="32fb0-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="32fb0-114">Atributų tipų kūrimas</span><span class="sxs-lookup"><span data-stu-id="32fb0-114">Create attribute types</span></span>

<span data-ttu-id="32fb0-115">Galite sukurti savo atributų tipus.</span><span class="sxs-lookup"><span data-stu-id="32fb0-115">You can create your own attribute types.</span></span> <span data-ttu-id="32fb0-116">Be to, galite perkelti produkto dimensijas į puslapį **Atributų tipai**.</span><span class="sxs-lookup"><span data-stu-id="32fb0-116">Additionally, you can transfer product dimensions to the **Attribute types** page.</span></span>

1. <span data-ttu-id="32fb0-117">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Atributų tipai**.</span><span class="sxs-lookup"><span data-stu-id="32fb0-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="32fb0-118">Kai atributų tipus nustatote pirmą kartą, pasirinkite **Kurti produkto dimensijas**, kad automatiškai perkeltumėte standartines produkto dimensijas.</span><span class="sxs-lookup"><span data-stu-id="32fb0-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard product dimensions.</span></span>
3. <span data-ttu-id="32fb0-119">Pasirinkite **Naujas**, kad sukurtumėte naują atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="32fb0-120">Lauke **Atributo tipas** įveskite atributo tipo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="32fb0-121">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="32fb0-122">Lauke **Vienetas** pasirinkite atitinkamą atributo vienetą, kaip reikalaujama.</span><span class="sxs-lookup"><span data-stu-id="32fb0-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="32fb0-123">Lauke **Duomenų tipas** pasirinkite vieneto tipą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="32fb0-124">Jei duomenų tipu pasirinkote **Eilutė**, atlikite šiuos veiksmus, kad šiam atributo tipui sukurtumėte reikšmes:</span><span class="sxs-lookup"><span data-stu-id="32fb0-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="32fb0-125">Pasirinkite atributo tipą ir pasirinkite **Reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="32fb0-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="32fb0-126">Lauke **Atributo kodas** pasirinkite **Visi**.</span><span class="sxs-lookup"><span data-stu-id="32fb0-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="32fb0-127">Lauke **Atributo tipas** pasirinkite atributo tipą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="32fb0-128">Lauke **Reikšmė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="32fb0-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="32fb0-129">Lauke **Aprašymas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="32fb0-130">Įrašykite įrašą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-130">Save the record.</span></span>
    7. <span data-ttu-id="32fb0-131">Grįžkite į puslapį **Atributų tipai**.</span><span class="sxs-lookup"><span data-stu-id="32fb0-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="32fb0-132">Įrašykite įrašą.</span><span class="sxs-lookup"><span data-stu-id="32fb0-132">Save the record.</span></span>

    <span data-ttu-id="32fb0-133">Lauke **Funkcinių vietovių tipai** rodomas funkcinių vietovių, kurios naudoja šį atributo tipą, skaičius.</span><span class="sxs-lookup"><span data-stu-id="32fb0-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="32fb0-134">Lauke **Turto tipai** rodomas jį naudojančių turto tipų skaičius.</span><span class="sxs-lookup"><span data-stu-id="32fb0-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
