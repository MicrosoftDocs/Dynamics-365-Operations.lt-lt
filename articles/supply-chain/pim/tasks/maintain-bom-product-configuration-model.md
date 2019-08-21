---
title: Prižiūrėti produkto konfigūracijos modelio KS
description: Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f663c28dfcbf6b365e3e88d3a4f6385ce2fcca9f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844398"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="85806-103">Prižiūrėti produkto konfigūracijos modelio KS</span><span class="sxs-lookup"><span data-stu-id="85806-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85806-104">Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="85806-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="85806-105">Šiai procedūrai sukurti naudojamas demonstracinės įmonės USMF aukščiausios kokybės garsiakalbio modelis.</span><span class="sxs-lookup"><span data-stu-id="85806-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="85806-106">Įtraukti KS eilutę</span><span class="sxs-lookup"><span data-stu-id="85806-106">Add a BOM line</span></span>
1. <span data-ttu-id="85806-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="85806-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="85806-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="85806-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="85806-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="85806-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="85806-110">Šiai procedūrai pasirinkite aukščiausios kokybės garsiakalbį.</span><span class="sxs-lookup"><span data-stu-id="85806-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="85806-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="85806-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="85806-112">Išplėskite KS eilučių skyrių.</span><span class="sxs-lookup"><span data-stu-id="85806-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="85806-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="85806-113">Click Add.</span></span>
7. <span data-ttu-id="85806-114">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85806-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="85806-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85806-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="85806-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="85806-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="85806-117">Įtraukti KS eilutės informaciją</span><span class="sxs-lookup"><span data-stu-id="85806-117">Add BOM line details</span></span>
1. <span data-ttu-id="85806-118">Spustelėkite KS eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="85806-118">Click BOM line details.</span></span>
2. <span data-ttu-id="85806-119">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="85806-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="85806-120">Pvz., galite pasirinkti prekę M0055.</span><span class="sxs-lookup"><span data-stu-id="85806-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="85806-121">Kiekvienai KS eilutės ypatybei galite pasirinkti, ar jai priskiriama fiksuota vertė, ar ji susieta su atributu.</span><span class="sxs-lookup"><span data-stu-id="85806-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="85806-122">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="85806-122">Select the Set check box.</span></span>
4. <span data-ttu-id="85806-123">Lauke Skaičiavimas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="85806-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="85806-124">Skaičiavimo ypatybę nustačius į Taip, užtikrinama, kad KS eilutė bus įtraukta į išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="85806-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="85806-125">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="85806-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="85806-126">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="85806-126">Select the Set check box.</span></span>
7. <span data-ttu-id="85806-127">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="85806-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="85806-128">Kiekio laukas nustato, kiek yra prekės, kuri bus įtraukta į KS.</span><span class="sxs-lookup"><span data-stu-id="85806-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="85806-129">Tai gali būti aiškus kandidatas į atributo susiejimą.</span><span class="sxs-lookup"><span data-stu-id="85806-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="85806-130">Spustelėkite skirtuką Dimensija.</span><span class="sxs-lookup"><span data-stu-id="85806-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="85806-131">Patikrinkite, ar kuri nors prekės dimensija yra aktyvi, ir todėl privalo turėti priskirtą vertę arba atributą.</span><span class="sxs-lookup"><span data-stu-id="85806-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="85806-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="85806-132">Click OK.</span></span>

