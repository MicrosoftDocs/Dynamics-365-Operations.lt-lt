--- 
title: "Prižiūrėti produkto konfigūracijos modelio KS"
description: "Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: c017d7719ac6af43b0c8a162080bb753587df030
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="97997-103">Prižiūrėti produkto konfigūracijos modelio KS</span><span class="sxs-lookup"><span data-stu-id="97997-103">Maintain BOM for a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97997-104">Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="97997-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="97997-105">Šiai procedūrai sukurti naudojamas demonstracinės įmonės USMF aukščiausios kokybės garsiakalbio modelis.</span><span class="sxs-lookup"><span data-stu-id="97997-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="97997-106">Įtraukti KS eilutę</span><span class="sxs-lookup"><span data-stu-id="97997-106">Add a BOM line</span></span>
1. <span data-ttu-id="97997-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="97997-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="97997-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="97997-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="97997-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="97997-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="97997-110">Šiai procedūrai pasirinkite aukščiausios kokybės garsiakalbį.</span><span class="sxs-lookup"><span data-stu-id="97997-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="97997-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="97997-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="97997-112">Išplėskite KS eilučių skyrių.</span><span class="sxs-lookup"><span data-stu-id="97997-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="97997-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="97997-113">Click Add.</span></span>
7. <span data-ttu-id="97997-114">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97997-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="97997-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97997-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="97997-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="97997-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="97997-117">Įtraukti KS eilutės informaciją</span><span class="sxs-lookup"><span data-stu-id="97997-117">Add BOM line details</span></span>
1. <span data-ttu-id="97997-118">Spustelėkite KS eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="97997-118">Click BOM line details.</span></span>
2. <span data-ttu-id="97997-119">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97997-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="97997-120">Pvz., galite pasirinkti prekę M0055.</span><span class="sxs-lookup"><span data-stu-id="97997-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="97997-121">Kiekvienai KS eilutės ypatybei galite pasirinkti, ar jai priskiriama fiksuota vertė, ar ji susieta su atributu.</span><span class="sxs-lookup"><span data-stu-id="97997-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="97997-122">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="97997-122">Select the Set check box.</span></span>
4. <span data-ttu-id="97997-123">Lauke Skaičiavimas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="97997-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="97997-124">Skaičiavimo ypatybę nustačius į Taip, užtikrinama, kad KS eilutė bus įtraukta į išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="97997-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="97997-125">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="97997-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="97997-126">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="97997-126">Select the Set check box.</span></span>
7. <span data-ttu-id="97997-127">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="97997-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="97997-128">Kiekio laukas nustato, kiek yra prekės, kuri bus įtraukta į KS.</span><span class="sxs-lookup"><span data-stu-id="97997-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="97997-129">Tai gali būti aiškus kandidatas į atributo susiejimą.</span><span class="sxs-lookup"><span data-stu-id="97997-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="97997-130">Spustelėkite skirtuką Dimensija.</span><span class="sxs-lookup"><span data-stu-id="97997-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="97997-131">Patikrinkite, ar kuri nors prekės dimensija yra aktyvi, ir todėl privalo turėti priskirtą vertę arba atributą.</span><span class="sxs-lookup"><span data-stu-id="97997-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="97997-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="97997-132">Click OK.</span></span>


