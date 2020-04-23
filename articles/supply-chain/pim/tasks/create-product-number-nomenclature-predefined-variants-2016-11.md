---
title: Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šioje temoje aiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio nomenklatūrą ir kaip ją priskirti tinkamai produkto matmenų grupei.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c39d383c15bcc838e09bc417f7e961c3647828da
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213290"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="1bbe2-103">Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="1bbe2-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1bbe2-104">Šioje temoje aiškinama, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerio nomenklatūrą ir kaip ją priskirti tinkamai produkto matmenų grupei.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="1bbe2-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1bbe2-106">Nauja produkto numerių nomenklatūra yra priskiriama produkto dimensijų grupėms Spalva ir Dydis.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="1bbe2-107">Paprastai šią užduotį atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="1bbe2-108">Produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="1bbe2-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="1bbe2-109">Pažymėkite **Produkto varianto modelio aprašas**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="1bbe2-110">Pažymėkite **Produkto nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="1bbe2-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-111">Select **New**.</span></span>
4. <span data-ttu-id="1bbe2-112">Lauke **Pavadinimas** įveskite nomenklatūros pavadinimą, kuris padės identifikuoti tikslinę produkto matmenų grupę, pavyzdžiui, `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="1bbe2-113">Lauke **Aprašo laukas**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="1bbe2-114">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-114">Select **Add**.</span></span>
7. <span data-ttu-id="1bbe2-115">Pažymėkite **Produkto pagrindinį** numerį.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="1bbe2-116">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-116">Select **Add**.</span></span>
9. <span data-ttu-id="1bbe2-117">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="1bbe2-118">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="1bbe2-119">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-119">Select **Add**.</span></span>
12. <span data-ttu-id="1bbe2-120">Pažymėkite **Spalva**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-120">Select **Color**.</span></span>
13. <span data-ttu-id="1bbe2-121">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-121">Select **Add**.</span></span>
14. <span data-ttu-id="1bbe2-122">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="1bbe2-123">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="1bbe2-124">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-124">Select **Add**.</span></span>
17. <span data-ttu-id="1bbe2-125">Pažymėkite **Dydis**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-125">Select **Size**.</span></span>
18. <span data-ttu-id="1bbe2-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="1bbe2-127">Nomenklatūros priskyrimas bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="1bbe2-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="1bbe2-128">Pažymėkite **Produkto matmenų grupės**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="1bbe2-129">Pažymėkite grupę **SizeCol produkto matmuo**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="1bbe2-130">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-130">Select **Edit**.</span></span>
4. <span data-ttu-id="1bbe2-131">Pažymėkite **Taip** lauke **Naudoti nomenklatūrą**.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="1bbe2-132">Lauke **Produkto varianto numerio nomenklatūra** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="1bbe2-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1bbe2-133">Close the page.</span></span>

