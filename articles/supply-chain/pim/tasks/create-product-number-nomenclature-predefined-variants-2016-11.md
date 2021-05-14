---
title: Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šioje temoje aiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio nomenklatūrą ir kaip ją priskirti tinkamai produkto matmenų grupei.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920662"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="268f9-103">Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="268f9-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="268f9-104">Šioje temoje aiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio nomenklatūrą ir kaip ją priskirti tinkamai produkto matmenų grupei.</span><span class="sxs-lookup"><span data-stu-id="268f9-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="268f9-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="268f9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="268f9-106">Nauja produkto numerių nomenklatūra yra priskiriama produkto dimensijų grupėms Spalva ir Dydis.</span><span class="sxs-lookup"><span data-stu-id="268f9-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="268f9-107">Paprastai šią užduotį atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="268f9-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="268f9-108">Produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="268f9-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="268f9-109">Eikite į **Produkto informacijos valdymas \> Nustatymas \> Bendroji nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="268f9-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="268f9-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="268f9-110">Select **New**.</span></span>
1. <span data-ttu-id="268f9-111">Lauke **Pavadinimas** įveskite nomenklatūros pavadinimą, kuris padės identifikuoti tikslinę produkto matmenų grupę, pavyzdžiui, `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="268f9-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="268f9-112">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="268f9-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="268f9-113">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="268f9-113">Select **Add**.</span></span>
1. <span data-ttu-id="268f9-114">Pažymėkite **Produkto pagrindinį** numerį.</span><span class="sxs-lookup"><span data-stu-id="268f9-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="268f9-115">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="268f9-115">Select **Add**.</span></span>
1. <span data-ttu-id="268f9-116">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="268f9-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="268f9-117">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="268f9-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="268f9-118">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="268f9-118">Select **Add**.</span></span>
1. <span data-ttu-id="268f9-119">Pažymėkite **Spalva**.</span><span class="sxs-lookup"><span data-stu-id="268f9-119">Select **Color**.</span></span>
1. <span data-ttu-id="268f9-120">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="268f9-120">Select **Add**.</span></span>
1. <span data-ttu-id="268f9-121">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="268f9-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="268f9-122">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="268f9-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="268f9-123">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="268f9-123">Select **Add**.</span></span>
1. <span data-ttu-id="268f9-124">Pažymėkite **Dydis**.</span><span class="sxs-lookup"><span data-stu-id="268f9-124">Select **Size**.</span></span>
1. <span data-ttu-id="268f9-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="268f9-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="268f9-126">Nomenklatūros priskyrimas bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="268f9-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="268f9-127">Pažymėkite **Produkto matmenų grupės**.</span><span class="sxs-lookup"><span data-stu-id="268f9-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="268f9-128">Pažymėkite grupę **SizeCol produkto matmuo**.</span><span class="sxs-lookup"><span data-stu-id="268f9-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="268f9-129">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="268f9-129">Select **Edit**.</span></span>
4. <span data-ttu-id="268f9-130">Pažymėkite **Taip** lauke **Naudoti nomenklatūrą**.</span><span class="sxs-lookup"><span data-stu-id="268f9-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="268f9-131">Lauke **Produkto varianto numerio nomenklatūra** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="268f9-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="268f9-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="268f9-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]