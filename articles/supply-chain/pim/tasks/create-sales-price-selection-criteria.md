---
title: Pardavimo kainos pasirinkimo kriterijų kūrimas
description: Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae444008e550d808a02d55dad02cc1b52874f0d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985466"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="d02f8-103">Pardavimo kainos pasirinkimo kriterijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="d02f8-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d02f8-104">Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams.</span><span class="sxs-lookup"><span data-stu-id="d02f8-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="d02f8-105">Norint paleisti šią procedūrą, reikia, kad būtų galimas bent vienas pardavimo kainos modelis.</span><span class="sxs-lookup"><span data-stu-id="d02f8-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="d02f8-106">Šiame pavyzdyje naudojamas kainos modelio, skirtas demonstracinių duomenų įmonės USMF garsiakalbio sprendimo pardavimo kainos modeliui.</span><span class="sxs-lookup"><span data-stu-id="d02f8-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="d02f8-107">Paprastai šią procedūrą atlieka produktų vadovas.</span><span class="sxs-lookup"><span data-stu-id="d02f8-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="d02f8-108">Naujo esamo pardavimo kainos modelio kriterijaus įtraukimas</span><span class="sxs-lookup"><span data-stu-id="d02f8-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="d02f8-109">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="d02f8-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="d02f8-110">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="d02f8-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="d02f8-111">Sąraše pasirinkite garsiakalbio sprendimo produkto modelio eilutę, bet nespustelėkite modelio pavadinimo nuorodos.</span><span class="sxs-lookup"><span data-stu-id="d02f8-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="d02f8-112">Veiksmų srityje spustelėkite Modelis.</span><span class="sxs-lookup"><span data-stu-id="d02f8-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="d02f8-113">Spustelėkite Kainos modelio kriterijai.</span><span class="sxs-lookup"><span data-stu-id="d02f8-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="d02f8-114">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d02f8-114">Click New.</span></span>
7. <span data-ttu-id="d02f8-115">Lauke Pavadinimas įveskite „10 klientų grupė“.</span><span class="sxs-lookup"><span data-stu-id="d02f8-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="d02f8-116">Kainos modelio kriterijaus pavadinimas padeda nustatyti pagrindinius pasirinkimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="d02f8-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="d02f8-117">Lauke Kainos modelis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d02f8-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="d02f8-118">Lauke Užsakymo tipas pasirinkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="d02f8-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="d02f8-119">Užsakymo tipas nustato duomenų bazės laukus, kuriuos bus galima naudoti teikiant pasirinkimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="d02f8-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="d02f8-120">Lauke Galioja nuo įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d02f8-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="d02f8-121">Lauke Galioja iki įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d02f8-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="d02f8-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d02f8-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="d02f8-123">Pasirinkimo kriterijų užklausos kūrimas</span><span class="sxs-lookup"><span data-stu-id="d02f8-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="d02f8-124">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="d02f8-124">Click Edit.</span></span>
2. <span data-ttu-id="d02f8-125">Lauke Lentelė pasirinkite Klientai.</span><span class="sxs-lookup"><span data-stu-id="d02f8-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="d02f8-126">Lauke Laukas pasirinkite Klientų grupė.</span><span class="sxs-lookup"><span data-stu-id="d02f8-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="d02f8-127">Šiame pavyzdyje nustatydami pasirinkimo kriterijus mes naudosime konkrečią klientų grupę.</span><span class="sxs-lookup"><span data-stu-id="d02f8-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="d02f8-128">Lauke Kriterijai pasirinkite 10 klientų grupė.</span><span class="sxs-lookup"><span data-stu-id="d02f8-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="d02f8-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d02f8-129">Click OK.</span></span>

