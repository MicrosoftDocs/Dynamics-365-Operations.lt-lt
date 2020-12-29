---
title: Kopijuoti sudėtinius produktus iš esamos formulės versijos
description: Ši procedūra nurodo, kaip kopijuoti sudėtinius produktus iš esamos formulės versijos į kitokią patvirtinto produkto formulę.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b70ccbdac2061baf3896ecbd9449da3c38842a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433321"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="a3b0b-103">Kopijuoti sudėtinius produktus iš esamos formulės versijos</span><span class="sxs-lookup"><span data-stu-id="a3b0b-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3b0b-104">Ši procedūra nurodo, kaip kopijuoti sudėtinius produktus iš esamos formulės versijos į kitokią patvirtinto produkto formulę.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="a3b0b-105">Būtina sąlyga, kad bent viena formulės versija būtų susieta su sudėtiniais produktais.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="a3b0b-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonės USP2.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="a3b0b-107">Rasti patvirtinta produktą</span><span class="sxs-lookup"><span data-stu-id="a3b0b-107">Find a released product</span></span>
1. <span data-ttu-id="a3b0b-108">Eikite į Išleisti produktai.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-108">Go to Released products.</span></span>
2. <span data-ttu-id="a3b0b-109">Spustelėkite Rodyti filtrus.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-109">Click Show filters.</span></span>
    * <span data-ttu-id="a3b0b-110">Ketinate į filtro dialogo langą įtraukti lauką Gamybos tipas.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="a3b0b-111">Norėdami įtraukti lauką Gamybos tipas, spustelėkite Įtraukti filtro lauką.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="a3b0b-112">Atlikdami kitą veiksmą, prieš pasirinkdami Taikyti, lauke Gamybos tipas turite įvesti formulę.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="a3b0b-113">Taip nustatomas išleistų produktų sąrašo filtras.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="a3b0b-114">Lauke Gamybos tipas rankiniu būdu įveskite formulę.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="a3b0b-115">Spustelėkite Taikyti.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="a3b0b-116">Pasirinkti patvirtintą produktą</span><span class="sxs-lookup"><span data-stu-id="a3b0b-116">Select a released product</span></span>
1. <span data-ttu-id="a3b0b-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="a3b0b-118">Spustelėkite Formulės versijos.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-118">Click Formula versions.</span></span>
    * <span data-ttu-id="a3b0b-119">Inžinerijos veiksmų srityje spustelėkite Formulės versijas.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="a3b0b-120">Kopijuoti sudėtinius produktus</span><span class="sxs-lookup"><span data-stu-id="a3b0b-120">Copy co-products</span></span>
1. <span data-ttu-id="a3b0b-121">Veiksmų srityje spustelėkite Formulės versija.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="a3b0b-122">Spustelėkite Sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-122">Click Co-products.</span></span>
3. <span data-ttu-id="a3b0b-123">Spustelėkite Kopijuoti.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-123">Click Copy.</span></span>
4. <span data-ttu-id="a3b0b-124">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="a3b0b-125">Lauke Formulės versija įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="a3b0b-126">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-126">Click OK.</span></span>
7. <span data-ttu-id="a3b0b-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a3b0b-127">Close the page.</span></span>

