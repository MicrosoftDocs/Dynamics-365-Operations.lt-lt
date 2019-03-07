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
ms.openlocfilehash: 156972cdbf4ffb02b01b00972cc83d003d941378
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "326359"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="60a91-103">Produkto ciklo būsenos kūrimas norint pašalinti produktus iš bendrojo planavimo</span><span class="sxs-lookup"><span data-stu-id="60a91-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60a91-104">Ši procedūra nurodo, kaip sukurti naują produkto gyvavimo ciklo būseną, kuriai nepriskiriami produktai iš bendrojo planavimo ir lygio KS skaičiavimo.</span><span class="sxs-lookup"><span data-stu-id="60a91-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="60a91-105">Kurti nebenaudojamą būseną</span><span class="sxs-lookup"><span data-stu-id="60a91-105">Create an obsolete state</span></span>
1. <span data-ttu-id="60a91-106">Eikite į Produkto informacijos valdymas > Sąranka > Produkto ciklo būsena.</span><span class="sxs-lookup"><span data-stu-id="60a91-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="60a91-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="60a91-107">Click New.</span></span>
3. <span data-ttu-id="60a91-108">Lauke Būsena įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60a91-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="60a91-109">Lauke Suaktyvinta planavimui pažymėkite Ne.</span><span class="sxs-lookup"><span data-stu-id="60a91-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="60a91-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60a91-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="60a91-111">Susieti nebenaudojamą būseną su išleistu produktu</span><span class="sxs-lookup"><span data-stu-id="60a91-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="60a91-112">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="60a91-112">Close the page.</span></span>
2. <span data-ttu-id="60a91-113">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="60a91-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="60a91-114">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="60a91-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="60a91-115">Pvz., filtruokite lauką Ieškos pavadinimas nurodydami reikšmę „M00“.</span><span class="sxs-lookup"><span data-stu-id="60a91-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="60a91-116">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="60a91-116">Click Edit.</span></span>
5. <span data-ttu-id="60a91-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="60a91-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="60a91-118">Lauke Produkto ciklo būsena įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="60a91-118">In the Product lifecycle state field, enter or select a value.</span></span>

