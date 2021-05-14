---
title: Pardavimo kainos pasirinkimo kriterijų kūrimas
description: Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920536"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="173c0-103">Pardavimo kainos pasirinkimo kriterijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="173c0-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="173c0-104">Šioje procedūroje parodoma, kaip kurti pardavimo kainos pasirinkimo kriterijus, skirtus atributais pagrįstiems pardavimo kainos modeliams.</span><span class="sxs-lookup"><span data-stu-id="173c0-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="173c0-105">Norint paleisti šią procedūrą, reikia, kad būtų galimas bent vienas pardavimo kainos modelis.</span><span class="sxs-lookup"><span data-stu-id="173c0-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="173c0-106">Šiame pavyzdyje naudojamas kainos modelio, skirtas demonstracinių duomenų įmonės USMF garsiakalbio sprendimo pardavimo kainos modeliui.</span><span class="sxs-lookup"><span data-stu-id="173c0-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="173c0-107">Paprastai šią procedūrą atlieka produktų vadovas.</span><span class="sxs-lookup"><span data-stu-id="173c0-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="173c0-108">Naujo esamo pardavimo kainos modelio kriterijaus įtraukimas</span><span class="sxs-lookup"><span data-stu-id="173c0-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="173c0-109">Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="173c0-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="173c0-110">Sąraše pasirinkite garsiakalbio sprendimo produkto modelio eilutę, bet rinkitės modelio pavadinimo nuorodos.</span><span class="sxs-lookup"><span data-stu-id="173c0-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="173c0-111">Veiksmų srityje pasirinkite **Modelis**.</span><span class="sxs-lookup"><span data-stu-id="173c0-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="173c0-112">Rinkitės **Kainos modelio kriterijus**.</span><span class="sxs-lookup"><span data-stu-id="173c0-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="173c0-113">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="173c0-113">Select **New**.</span></span>
1. <span data-ttu-id="173c0-114">Lauke **Pavadinimas** įveskite „10 klientų grupė“.</span><span class="sxs-lookup"><span data-stu-id="173c0-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="173c0-115">Kainos modelio kriterijaus pavadinimas padeda nustatyti pagrindinius pasirinkimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="173c0-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="173c0-116">Lauke **Kainos modelis** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="173c0-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="173c0-117">Lauke **Užsakymo tipas** pasirinkite *Pardavimo užsakymas*.</span><span class="sxs-lookup"><span data-stu-id="173c0-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="173c0-118">Užsakymo tipas nustato duomenų bazės laukus, kuriuos bus galima naudoti teikiant pasirinkimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="173c0-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="173c0-119">Lauke **Galioja nuo** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="173c0-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="173c0-120">Lauke **Galioja iki** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="173c0-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="173c0-121">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="173c0-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="173c0-122">Pasirinkimo kriterijų užklausos kūrimas</span><span class="sxs-lookup"><span data-stu-id="173c0-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="173c0-123">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="173c0-123">Select **Edit**.</span></span>
2. <span data-ttu-id="173c0-124">Lauke **Lentelė** pasirinkite *Klientai*.</span><span class="sxs-lookup"><span data-stu-id="173c0-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="173c0-125">Lauke **Laukas** pasirinkite *Klientų grupė*.</span><span class="sxs-lookup"><span data-stu-id="173c0-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="173c0-126">Šiame pavyzdyje nustatydami pasirinkimo kriterijus mes naudosime konkrečią klientų grupę.</span><span class="sxs-lookup"><span data-stu-id="173c0-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="173c0-127">Lauke **Kriterijai** pasirinkite *10 klientų grupė*.</span><span class="sxs-lookup"><span data-stu-id="173c0-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="173c0-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="173c0-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]