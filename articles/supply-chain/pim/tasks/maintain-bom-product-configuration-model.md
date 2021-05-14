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
ms.openlocfilehash: b4ad73265e321b6339c061a7866b55cb2769954b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921322"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="4439b-103">Prižiūrėti produkto konfigūracijos modelio KS</span><span class="sxs-lookup"><span data-stu-id="4439b-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4439b-104">Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis.</span><span class="sxs-lookup"><span data-stu-id="4439b-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="4439b-105">Šiai procedūrai sukurti naudojamas demonstracinės įmonės USMF aukščiausios kokybės garsiakalbio modelis.</span><span class="sxs-lookup"><span data-stu-id="4439b-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>

## <a name="add-a-bom-line"></a><span data-ttu-id="4439b-106">Įtraukti KS eilutę</span><span class="sxs-lookup"><span data-stu-id="4439b-106">Add a BOM line</span></span>

1. <span data-ttu-id="4439b-107">Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="4439b-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="4439b-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="4439b-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4439b-109">Šiai procedūrai pasirinkite aukščiausios kokybės garsiakalbį.</span><span class="sxs-lookup"><span data-stu-id="4439b-109">Select the High end speaker for this procedure.</span></span>  
1. <span data-ttu-id="4439b-110">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4439b-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="4439b-111">Išplėskite **BOM eilučių** skyrių.</span><span class="sxs-lookup"><span data-stu-id="4439b-111">Expand the **BOM lines** section.</span></span>
1. <span data-ttu-id="4439b-112">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="4439b-112">Select **Add**.</span></span>
1. <span data-ttu-id="4439b-113">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4439b-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="4439b-114">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4439b-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="4439b-115">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4439b-115">Select **Save**.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="4439b-116">Įtraukti KS eilutės informaciją</span><span class="sxs-lookup"><span data-stu-id="4439b-116">Add BOM line details</span></span>

1. <span data-ttu-id="4439b-117">Pasirinkite **BOM eilutės** informaciją.</span><span class="sxs-lookup"><span data-stu-id="4439b-117">Select **BOM line details**.</span></span>
2. <span data-ttu-id="4439b-118">Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4439b-118">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="4439b-119">Pvz., galite pasirinkti prekę M0055.</span><span class="sxs-lookup"><span data-stu-id="4439b-119">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="4439b-120">Kiekvienai KS eilutės ypatybei galite pasirinkti, ar jai priskiriama fiksuota vertė, ar ji susieta su atributu.</span><span class="sxs-lookup"><span data-stu-id="4439b-120">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="4439b-121">Pažymėkite **Nustatyti** laukelį.</span><span class="sxs-lookup"><span data-stu-id="4439b-121">Select the **Set** check box.</span></span>
4. <span data-ttu-id="4439b-122">Lauke *Skaičiavimas* pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4439b-122">Select *Yes* in the **Calculation** field.</span></span>
    * <span data-ttu-id="4439b-123">Skaičiavimo **ypatybę** nustačius į *Taip* užtikrinama, kad KS eilutė bus įtraukta į išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="4439b-123">Setting the **Calculation** property to *Yes* ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="4439b-124">Pasirinkite skirtuką **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="4439b-124">Select the **Setup** tab.</span></span>
6. <span data-ttu-id="4439b-125">Pažymėkite **Nustatyti** laukelį.</span><span class="sxs-lookup"><span data-stu-id="4439b-125">Select the **Set** check box.</span></span>
7. <span data-ttu-id="4439b-126">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="4439b-126">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="4439b-127">Kiekio laukas nustato, kiek yra prekės, kuri bus įtraukta į KS.</span><span class="sxs-lookup"><span data-stu-id="4439b-127">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="4439b-128">Tai gali būti aiškus kandidatas į atributo susiejimą.</span><span class="sxs-lookup"><span data-stu-id="4439b-128">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="4439b-129">Pažymėkite skirtuką **Matmenys**.</span><span class="sxs-lookup"><span data-stu-id="4439b-129">Select the **Dimension** tab.</span></span>
    * <span data-ttu-id="4439b-130">Patikrinkite, ar kuri nors prekės dimensija yra aktyvi, ir todėl privalo turėti priskirtą vertę arba atributą.</span><span class="sxs-lookup"><span data-stu-id="4439b-130">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="4439b-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="4439b-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]