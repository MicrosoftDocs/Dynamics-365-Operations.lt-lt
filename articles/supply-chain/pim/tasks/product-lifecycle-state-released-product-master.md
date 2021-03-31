---
title: Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui
description: Ši procedūra nurodo, kaip priskirti produkto ciklo būseną išleistam bendrajam produktui ir jo variantams.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a5d7f6532e3c0b61fcc5758f383257d4a9a09b5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226742"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="25b74-103">Produkto ciklo būsenos priskyrimas išleistam bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="25b74-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25b74-104">Ši procedūra nurodo, kaip priskirti produkto ciklo būseną išleistam bendrajam produktui ir jo variantams.</span><span class="sxs-lookup"><span data-stu-id="25b74-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="25b74-105">Būtina sąlyga: pirmiausia turite paleisti užduočių vedlį „Kurti naują produkto ciklo būseną“, kad įsitikintumėte, jog prieš paleidžiant šį užduočių vedlį yra sukurta bent viena produkto ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="25b74-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="25b74-106">Rasti išleistą bendrąjį produktą</span><span class="sxs-lookup"><span data-stu-id="25b74-106">Find a released product master</span></span>
1. <span data-ttu-id="25b74-107">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="25b74-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="25b74-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="25b74-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="25b74-109">Nurodytas bendrojo produkto potipis Bendrasis produktas.</span><span class="sxs-lookup"><span data-stu-id="25b74-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="25b74-110">Atnaujinti ciklo būseną</span><span class="sxs-lookup"><span data-stu-id="25b74-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="25b74-111">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="25b74-111">Click Edit.</span></span>
2. <span data-ttu-id="25b74-112">Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25b74-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="25b74-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25b74-113">Click Save.</span></span>
4. <span data-ttu-id="25b74-114">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="25b74-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="25b74-115">Pasirinkus Taip visų susijusio išleisto produkto variantų, kurių pradinė būsena tokia pati kaip išleisto bendrojo produkto, būsena taip pat atnaujinamą į naują produkto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="25b74-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="25b74-116">Pasirinkus Ne išsaugoma faktinė visų variantų būsena.</span><span class="sxs-lookup"><span data-stu-id="25b74-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="25b74-117">Variantai, kurių produkto ciklo būsena skiriasi nuo išleisto bendrojo produkto būsenos, neatnaujinami.</span><span class="sxs-lookup"><span data-stu-id="25b74-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="25b74-118">Patvirtinti variantų ciklo būseną</span><span class="sxs-lookup"><span data-stu-id="25b74-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="25b74-119">Spustelėkite Išleistų produktų variantai.</span><span class="sxs-lookup"><span data-stu-id="25b74-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="25b74-120">Atkreipkite dėmesį į tai, kad visi variantai įgavo pasirinktą bendrojo produkto ciklo būseną.</span><span class="sxs-lookup"><span data-stu-id="25b74-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="25b74-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25b74-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="25b74-122">Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25b74-122">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]