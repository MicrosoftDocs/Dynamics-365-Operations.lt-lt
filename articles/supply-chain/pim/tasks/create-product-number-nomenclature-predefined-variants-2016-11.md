---
title: Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šiame vadove parodoma, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerių nomenklatūrą ir kaip ją priskirti atitinkamai produkto dimensijų grupei.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550588"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="ac4a6-103">Iš anksto nustatytų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="ac4a6-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac4a6-104">Šiame vadove parodoma, kaip nustatyti iš anksto nustatytų produkto variantų produkto numerių nomenklatūrą ir kaip ją priskirti atitinkamai produkto dimensijų grupei.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="ac4a6-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ac4a6-106">Nauja produkto numerių nomenklatūra yra priskiriama produkto dimensijų grupėms Spalva ir Dydis.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="ac4a6-107">Paprastai šią užduotį atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="ac4a6-108">Produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="ac4a6-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="ac4a6-109">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ac4a6-110">Spustelėkite Produkto nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="ac4a6-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-111">Click New.</span></span>
4. <span data-ttu-id="ac4a6-112">Lauke Pavadinimas įveskite nomenklatūros pavadinimą, kuris padeda nustatyti tikslinę produkto dimensijų grupę, pavyzdžiui, ColorSize.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="ac4a6-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ac4a6-114">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-114">Click Add.</span></span>
7. <span data-ttu-id="ac4a6-115">Spustelėkite Bendrojo produkto numeris.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-115">Click Product master number.</span></span>
8. <span data-ttu-id="ac4a6-116">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-116">Click Add.</span></span>
9. <span data-ttu-id="ac4a6-117">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-117">Click Text constant.</span></span>
10. <span data-ttu-id="ac4a6-118">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="ac4a6-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-119">Click Add.</span></span>
12. <span data-ttu-id="ac4a6-120">Spustelėkite Spalva.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-120">Click Color.</span></span>
13. <span data-ttu-id="ac4a6-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-121">Click Add.</span></span>
14. <span data-ttu-id="ac4a6-122">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-122">Click Text constant.</span></span>
15. <span data-ttu-id="ac4a6-123">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="ac4a6-124">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-124">Click Add.</span></span>
17. <span data-ttu-id="ac4a6-125">Spustelėkite Dydis.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-125">Click Size.</span></span>
18. <span data-ttu-id="ac4a6-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="ac4a6-127">Nomenklatūros priskyrimas bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="ac4a6-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="ac4a6-128">Spustelėkite Produkto dimensijų grupės.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="ac4a6-129">Pasirinkite produkto dimensijų grupę SizeCol.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="ac4a6-130">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-130">Click Edit.</span></span>
4. <span data-ttu-id="ac4a6-131">Lauke Naudoti nomenklatūrą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="ac4a6-132">Lauke Produkto varianto numerių nomenklatūra įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="ac4a6-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ac4a6-133">Close the page.</span></span>

