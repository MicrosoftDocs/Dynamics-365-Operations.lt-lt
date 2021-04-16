---
title: Pagamintų prekių standartinių savikainų paruošimas priežiūrai
description: Šioje temoje aprašomi pasiruošimo tvarkyti pagamintų prekių išlaidas veiksmai.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6944782ac236a3f414b1cadfb12b0f0d8c1115b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821518"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="80bbd-103">Pagamintų prekių standartinių savikainų paruošimas priežiūrai</span><span class="sxs-lookup"><span data-stu-id="80bbd-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80bbd-104">Šioje temoje aprašomi pasiruošimo tvarkyti pagamintų prekių išlaidas veiksmai.</span><span class="sxs-lookup"><span data-stu-id="80bbd-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="80bbd-105">Pagamintų prekių veiksmai šiek tiek skiriasi nuo įsigytų prekių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="80bbd-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="80bbd-106">Strategijos, priskirtos pagamintoms prekėms, gali paveikti pirminių pagamintų prekių išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="80bbd-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="80bbd-107">Norėdami pasiruošti tvarkyti pagamintų prekių išlaidas, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80bbd-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="80bbd-108">Pagamintai prekei priskirkite prekių modelio grupę.</span><span class="sxs-lookup"><span data-stu-id="80bbd-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="80bbd-109">Prekių modelio grupė nustato, kad bus naudojamos standartinės išlaidos.</span><span class="sxs-lookup"><span data-stu-id="80bbd-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="80bbd-110">Pagamintai prekei priskirkite prekių grupę.</span><span class="sxs-lookup"><span data-stu-id="80bbd-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="80bbd-111">Prekių grupėje yra DK sąskaitos, taikomos pagamintai prekei.</span><span class="sxs-lookup"><span data-stu-id="80bbd-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="80bbd-112">DK sąskaitose pagamintai prekei su standartinių išlaidų atsargų modeliu yra keletas gamybos nuokrypių, išlaidų pokyčio nuokrypis ir atsargų išlaidų perkainojimas.</span><span class="sxs-lookup"><span data-stu-id="80bbd-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="80bbd-113">Prekei priskirti atsargų matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="80bbd-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="80bbd-114">Prekės išlaidos visada išreiškiamos prekės atsargų matavimo vienetu.</span><span class="sxs-lookup"><span data-stu-id="80bbd-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="80bbd-115">Pagamintai prekei nepriskirkite išlaidų grupės, nebent prekė bus laikoma įsigyta preke.</span><span class="sxs-lookup"><span data-stu-id="80bbd-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="80bbd-116">Pagamintai prekei priskirkite komplektavimo specifikacijos (KS) skaičiavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="80bbd-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="80bbd-117">Prekės KS skaičiavimo grupė apibrėžia taikomas įspėjimo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="80bbd-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="80bbd-118">Taip, skaičiuojant KS, gali būti generuojami perspėjimo pranešimai apie galimus skaičiavimo klaidų šaltinius.</span><span class="sxs-lookup"><span data-stu-id="80bbd-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="80bbd-119">Pavyzdžiui, perspėjimo pranešimas gali nustatyti, kada aktyvios KS ar maršruto nėra.</span><span class="sxs-lookup"><span data-stu-id="80bbd-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="80bbd-120">KS skaičiavimo grupėje yra išskleidimo stabdymo strategija, nurodanti, kada pagamintą prekę reikia laikyti įsigyta preke.</span><span class="sxs-lookup"><span data-stu-id="80bbd-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="80bbd-121">Jei pagamintos prekės išlaidos yra pastovios, jai priskirkite standartinį užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="80bbd-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="80bbd-122">Standartinis užsakymo kiekis yra apskaitos partijos dydis pastovioms išlaidoms amortizuoti.</span><span class="sxs-lookup"><span data-stu-id="80bbd-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="80bbd-123">Pastovių išlaidų pavyzdžiai – nukreipimo operacijų nustatymo laikas ir pastovus komponentų kiekis komplektavimo specifikacijoje.</span><span class="sxs-lookup"><span data-stu-id="80bbd-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="80bbd-124">Apibrėžkite pagamintos prekės KS.</span><span class="sxs-lookup"><span data-stu-id="80bbd-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="80bbd-125">Viena ar daugiau KS versijų gali būti apibrėžta pagamintai prekei.</span><span class="sxs-lookup"><span data-stu-id="80bbd-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="80bbd-126">Patikrinkite, ar jūsų pageidaujamos versijos yra pažymėtos kaip patvirtintos ir aktyvios bei kad jų įsigaliojimo datos yra tokios, kokių pageidaujate.</span><span class="sxs-lookup"><span data-stu-id="80bbd-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="80bbd-127">KS versija gali būti skirta visai įmonei arba konkrečiai teritorijai.</span><span class="sxs-lookup"><span data-stu-id="80bbd-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="80bbd-128">Apibrėžkite pagamintos prekės nukreipimą.</span><span class="sxs-lookup"><span data-stu-id="80bbd-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="80bbd-129">Viena ar daugiau maršrutų versijų gali būti apibrėžta pagamintai prekei.</span><span class="sxs-lookup"><span data-stu-id="80bbd-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="80bbd-130">Patikrinkite, ar jūsų pageidaujamos versijos yra pažymėtos kaip patvirtintos ir aktyvios bei kad jų įsigaliojimo datos yra tokios, kokių pageidaujate.</span><span class="sxs-lookup"><span data-stu-id="80bbd-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="80bbd-131">Maršruto versija turi būti skirta konkrečiai teritorijai.</span><span class="sxs-lookup"><span data-stu-id="80bbd-131">The route version must be site-specific.</span></span>

<span data-ttu-id="80bbd-132">Jei norite įkainodami naudoti nukreipimo informaciją, reikia atlikti papildomus paruošiamuosius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80bbd-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="80bbd-133">Pavyzdžiui, išlaidų kategorijos, priskirtos nukreipimo operacijoms, turi būti teisingos ir baigtos.</span><span class="sxs-lookup"><span data-stu-id="80bbd-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="80bbd-134">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="80bbd-134">Related topics</span></span>
--------

[<span data-ttu-id="80bbd-135">Pastovių pagamintos prekės išlaidų amortizavimas</span><span class="sxs-lookup"><span data-stu-id="80bbd-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="80bbd-136">Produktų, kuriuos galima gaminti arba įsigyti, nustatymas</span><span class="sxs-lookup"><span data-stu-id="80bbd-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]