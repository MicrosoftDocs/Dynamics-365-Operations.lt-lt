---
title: „Commerce“ hierarchijos
description: Šioje temoje aprašomos „Dynamics 365 Commerce“ hierarchijos.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 94b391ab5028f76debb75d25ac9469e25361cb12
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979621"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="cea0d-103">„Commerce“ hierarchijos</span><span class="sxs-lookup"><span data-stu-id="cea0d-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cea0d-104">Šioje temoje aprašomos „Dynamics 365 Commerce“ hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="cea0d-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cea0d-105">Galite sukurti kategorijų hierarchiją, kad galėtumėte tvarkyti produktus, kuriuos parduodate per kanalus.</span><span class="sxs-lookup"><span data-stu-id="cea0d-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="cea0d-106">Produktų klasifikavimui ar grupavimui galite naudoti produktų hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="cea0d-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="cea0d-107">Tada šiuos produktus galite naudoti produktų asortimentams ir klientų lojalumo programoms kurti.</span><span class="sxs-lookup"><span data-stu-id="cea0d-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="cea0d-108">Taip pat galite priskirti produkto atributus ir ypatybes, priskirti kainų struktūrą, įtraukti produktus į produktų akcijas ir naudoti produktus ataskaitoms teikti.</span><span class="sxs-lookup"><span data-stu-id="cea0d-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="cea0d-109">Galite sukurti vieną kategorijų hierarchiją, kad būtų pavaizduoti visi jūsų organizacijos produktai ir kategorijos, tada galite naudoti tą kategorijų hierarchiją kitiems tikslams.</span><span class="sxs-lookup"><span data-stu-id="cea0d-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="cea0d-110">Arba galite sukurti kelias kategorijų hierarchijas specialiais tikslais, pvz., produktų akcijoms.</span><span class="sxs-lookup"><span data-stu-id="cea0d-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="cea0d-111">Sukurdami produktų hierarchiją, turite priskirti kategorijos hierarchijos tipą, kad nustatytumėte kategorijų hierarchijos tikslą.</span><span class="sxs-lookup"><span data-stu-id="cea0d-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="cea0d-112">Pavyzdžiui, kai naršote produktus pagal kategorijas internete arba elektroniniame kasos aparate (EKA), nurodomos tik tos produktų hierarchijos, kurioms priskirtas tipas **„Commerce“ naršymo hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="cea0d-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="cea0d-113">Hierarchijos tipai</span><span class="sxs-lookup"><span data-stu-id="cea0d-113">Hierarchy types</span></span>

<span data-ttu-id="cea0d-114">Toliau nurodytoje lentelėje pateikiami galimi kategorijų hierarchijų tipai ir bendra kiekvieno tipo funkcija.</span><span class="sxs-lookup"><span data-stu-id="cea0d-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="cea0d-115">Kategorijų hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="cea0d-115">Category hierarchy type</span></span>       | <span data-ttu-id="cea0d-116">Paskirtis</span><span class="sxs-lookup"><span data-stu-id="cea0d-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="cea0d-117">Produktų hierarchija</span><span class="sxs-lookup"><span data-stu-id="cea0d-117">Product hierarchy</span></span>      | <span data-ttu-id="cea0d-118">Naudokite šį hierarchijos tipą, norėdami nurodyti bendrą savo organizacijos produktų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="cea0d-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="cea0d-119">Šio tipo hierarchiją galite naudoti reklamavimo, kainų nustatymo ir akcijų, ataskaitų teikimo ir asortimento planavimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="cea0d-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="cea0d-120">Šiam hierarchijos tipui galima priskirti tik vieną produkto hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="cea0d-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="cea0d-121">Papildoma hierarchija</span><span class="sxs-lookup"><span data-stu-id="cea0d-121">Supplemental hierarchy</span></span> | <span data-ttu-id="cea0d-122">Šį hierarchijos tipą naudokite bet kokioms papildomoms kategorijų hierarchijoms, kurias norite sukurti.</span><span class="sxs-lookup"><span data-stu-id="cea0d-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="cea0d-123">Pvz., pavasarį vykdote maudymosi kostiumėlių akciją.</span><span class="sxs-lookup"><span data-stu-id="cea0d-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="cea0d-124">Todėl maudymosi produktus įtraukiate į atskirą kategorijų hierarchiją ir akcijos kainas pritaikote skirtingoms produktų kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="cea0d-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="cea0d-125">Naršymo hierarchija</span><span class="sxs-lookup"><span data-stu-id="cea0d-125">Navigation hierarchy</span></span>   | <span data-ttu-id="cea0d-126">Naudokite šio tipo hierarchiją, norėdami grupuoti ir tvarkyti produktus į kategorijas, kad produktus būtų galima naršyti internete arba EKA.</span><span class="sxs-lookup"><span data-stu-id="cea0d-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="cea0d-127">Naudodami kategorijų hierarchiją savo produktams struktūruoti, galite nustatyti ir prižiūrėti produkto atributus ir savybes kategorijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="cea0d-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="cea0d-128">Šie atributai ir ypatybės apima produktų dimensijų ir EKA parametrus.</span><span class="sxs-lookup"><span data-stu-id="cea0d-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="cea0d-129">Visiems produktams, kuriuos priskiriate kategorijoms, automatiškai priskiriami jūsų nurodyti atributai ir ypatybės.</span><span class="sxs-lookup"><span data-stu-id="cea0d-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="cea0d-130">Taip pat galite nukopijuoti bet kurio produkto ypatybių parametrus, norėdami vienu metu padidinti pasirinktos kategorijos produktų skaičių.</span><span class="sxs-lookup"><span data-stu-id="cea0d-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
