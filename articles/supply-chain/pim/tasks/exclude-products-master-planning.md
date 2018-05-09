--- 
title: "Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo"
description: "Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 127bdf9ad1664f3ff8179075e7a3f78e39a5e1a2
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="b6355-103">Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo</span><span class="sxs-lookup"><span data-stu-id="b6355-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6355-104">Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo.</span><span class="sxs-lookup"><span data-stu-id="b6355-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="b6355-105">Kurti nebenaudojamą būseną</span><span class="sxs-lookup"><span data-stu-id="b6355-105">Create an obsolete state</span></span>
1. <span data-ttu-id="b6355-106">Eikite į Produkto informacijos valdymas > Sąranka > Produkto ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="b6355-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="b6355-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b6355-107">Click New.</span></span>
3. <span data-ttu-id="b6355-108">Lauke Būsena įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6355-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="b6355-109">Lauke Suaktyvinta planavimui pažymėkite Ne.</span><span class="sxs-lookup"><span data-stu-id="b6355-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="b6355-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6355-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="b6355-111">Susieti nebenaudojamą būseną su išleistu produktu</span><span class="sxs-lookup"><span data-stu-id="b6355-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="b6355-112">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b6355-112">Close the page.</span></span>
2. <span data-ttu-id="b6355-113">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="b6355-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="b6355-114">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="b6355-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b6355-115">Pvz., filtruokite lauką Ieškos pavadinimas nurodydami reikšmę „M00“.</span><span class="sxs-lookup"><span data-stu-id="b6355-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="b6355-116">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="b6355-116">Click Edit.</span></span>
5. <span data-ttu-id="b6355-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b6355-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b6355-118">Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6355-118">In the Product lifecycle state field, enter or select a value.</span></span>


