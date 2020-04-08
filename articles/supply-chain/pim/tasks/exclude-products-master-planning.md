---
title: Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo
description: Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62de37b5a84a1771b77ef2566942b7ffe8895f16
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149946"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="52f72-103">Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo</span><span class="sxs-lookup"><span data-stu-id="52f72-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52f72-104">Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo.</span><span class="sxs-lookup"><span data-stu-id="52f72-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="52f72-105">Kurti nebenaudojamą būseną</span><span class="sxs-lookup"><span data-stu-id="52f72-105">Create an obsolete state</span></span>
1. <span data-ttu-id="52f72-106">Eikite į Produkto informacijos valdymas > Sąranka > Produkto ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="52f72-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="52f72-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="52f72-107">Click New.</span></span>
3. <span data-ttu-id="52f72-108">Lauke Būsena įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="52f72-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="52f72-109">Lauke Suaktyvinta planavimui pažymėkite Ne.</span><span class="sxs-lookup"><span data-stu-id="52f72-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="52f72-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="52f72-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="52f72-111">Susieti nebenaudojamą būseną su išleistu produktu</span><span class="sxs-lookup"><span data-stu-id="52f72-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="52f72-112">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="52f72-112">Close the page.</span></span>
2. <span data-ttu-id="52f72-113">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="52f72-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="52f72-114">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="52f72-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="52f72-115">Pvz., filtruokite lauką Ieškos pavadinimas nurodydami reikšmę „M00“.</span><span class="sxs-lookup"><span data-stu-id="52f72-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="52f72-116">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="52f72-116">Click Edit.</span></span>
5. <span data-ttu-id="52f72-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="52f72-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="52f72-118">Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="52f72-118">In the Product lifecycle state field, enter or select a value.</span></span>

