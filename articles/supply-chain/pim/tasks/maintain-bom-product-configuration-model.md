---
title: Prižiūrėti produkto konfigūracijos modelio KS
description: Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49aa17aa376f8536e9d2290292f877d314c2c078
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818018"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="ffa35-103">Prižiūrėti produkto konfigūracijos modelio KS</span><span class="sxs-lookup"><span data-stu-id="ffa35-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffa35-104">Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="ffa35-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="ffa35-105">Šiai procedūrai sukurti naudojamas demonstracinės įmonės USMF aukščiausios kokybės garsiakalbio modelis.</span><span class="sxs-lookup"><span data-stu-id="ffa35-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="ffa35-106">Įtraukti KS eilutę</span><span class="sxs-lookup"><span data-stu-id="ffa35-106">Add a BOM line</span></span>
1. <span data-ttu-id="ffa35-107">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="ffa35-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ffa35-108">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="ffa35-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="ffa35-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ffa35-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ffa35-110">Šiai procedūrai pasirinkite aukščiausios kokybės garsiakalbį.</span><span class="sxs-lookup"><span data-stu-id="ffa35-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="ffa35-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ffa35-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ffa35-112">Išplėskite KS eilučių skyrių.</span><span class="sxs-lookup"><span data-stu-id="ffa35-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="ffa35-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="ffa35-113">Click Add.</span></span>
7. <span data-ttu-id="ffa35-114">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ffa35-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="ffa35-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ffa35-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="ffa35-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ffa35-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="ffa35-117">Įtraukti KS eilutės informaciją</span><span class="sxs-lookup"><span data-stu-id="ffa35-117">Add BOM line details</span></span>
1. <span data-ttu-id="ffa35-118">Spustelėkite KS eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="ffa35-118">Click BOM line details.</span></span>
2. <span data-ttu-id="ffa35-119">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ffa35-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="ffa35-120">Pvz., galite pasirinkti prekę M0055.</span><span class="sxs-lookup"><span data-stu-id="ffa35-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="ffa35-121">Kiekvienai KS eilutės ypatybei galite pasirinkti, ar jai priskiriama fiksuota vertė, ar ji susieta su atributu.</span><span class="sxs-lookup"><span data-stu-id="ffa35-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="ffa35-122">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="ffa35-122">Select the Set check box.</span></span>
4. <span data-ttu-id="ffa35-123">Lauke Skaičiavimas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="ffa35-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="ffa35-124">Skaičiavimo ypatybę nustačius į Taip, užtikrinama, kad KS eilutė bus įtraukta į išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="ffa35-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="ffa35-125">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="ffa35-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="ffa35-126">Pažymėkite žymės langelį Nustatyti.</span><span class="sxs-lookup"><span data-stu-id="ffa35-126">Select the Set check box.</span></span>
7. <span data-ttu-id="ffa35-127">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ffa35-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ffa35-128">Kiekio laukas nustato, kiek yra prekės, kuri bus įtraukta į KS.</span><span class="sxs-lookup"><span data-stu-id="ffa35-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="ffa35-129">Tai gali būti aiškus kandidatas į atributo susiejimą.</span><span class="sxs-lookup"><span data-stu-id="ffa35-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="ffa35-130">Spustelėkite skirtuką Dimensija.</span><span class="sxs-lookup"><span data-stu-id="ffa35-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="ffa35-131">Patikrinkite, ar kuri nors prekės dimensija yra aktyvi, ir todėl privalo turėti priskirtą vertę arba atributą.</span><span class="sxs-lookup"><span data-stu-id="ffa35-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="ffa35-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ffa35-132">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]