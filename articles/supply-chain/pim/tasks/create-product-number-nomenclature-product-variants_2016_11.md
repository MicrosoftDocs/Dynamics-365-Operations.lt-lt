---
title: Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ea30dc107213b1a2c6b2a109188066a6ea82159
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921016"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="d51a3-103">Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="d51a3-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d51a3-104">Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto.</span><span class="sxs-lookup"><span data-stu-id="d51a3-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="d51a3-105">Šioje procedūroje taip pat parodoma, kaip galima kurti konfigūravimo nomenklatūrą, skirtą produkto konfigūravimo modelio komponentui.</span><span class="sxs-lookup"><span data-stu-id="d51a3-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="d51a3-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="d51a3-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d51a3-107">Nauja produkto numerių nomenklatūrą yra priskiriama bendrajam produktui D0004.</span><span class="sxs-lookup"><span data-stu-id="d51a3-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="d51a3-108">Paprastai šią užduotį atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="d51a3-108">This task would typically be done by a product designer.</span></span>

## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="d51a3-109">Produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="d51a3-109">Create a product number nomenclature</span></span>

1. <span data-ttu-id="d51a3-110">Eikite į **Produkto informacijos valdymas \> Nustatymas \> Bendroji nomenklatūra**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-110">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="d51a3-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-111">Select **New**.</span></span>
1. <span data-ttu-id="d51a3-112">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="d51a3-113">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-113">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="d51a3-114">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-114">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-115">Pažymėkite **Produkto pagrindinį** numerį.</span><span class="sxs-lookup"><span data-stu-id="d51a3-115">Select **Product master number**.</span></span>
1. <span data-ttu-id="d51a3-116">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-116">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-117">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-117">Select **Text constant**.</span></span>
1. <span data-ttu-id="d51a3-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-118">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-119">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-119">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d51a3-120">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-120">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-121">Pasirinkti **konfigūraciją**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-121">Select **Configuration**.</span></span>
1. <span data-ttu-id="d51a3-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d51a3-122">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="d51a3-123">Produkto numerių nomenklatūros priskyrimas bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="d51a3-123">Assign the product number nomenclature to a product master</span></span>

1. <span data-ttu-id="d51a3-124">Eikite į **Produkto informacijos valdymas \> Produktai \> Bendrieji produktai**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-124">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="d51a3-125">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="d51a3-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d51a3-126">Pvz., filtruokite lauką **Produkto numeris** naudodami reikšmę D.</span><span class="sxs-lookup"><span data-stu-id="d51a3-126">For example, filter on the **Product number** field with a value of 'D'.</span></span>
1. <span data-ttu-id="d51a3-127">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d51a3-127">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="d51a3-128">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-128">Select **Edit**.</span></span>
1. <span data-ttu-id="d51a3-129">Pažymėkite *Taip* lauke **Naudoti nomenklatūrą**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-129">Select *Yes* in the **Use nomenclature** field.</span></span>
1. <span data-ttu-id="d51a3-130">Lauke **Produkto varianto numerio nomenklatūra** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-130">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
1. <span data-ttu-id="d51a3-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d51a3-131">Close the page.</span></span>
1. <span data-ttu-id="d51a3-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d51a3-132">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="d51a3-133">Produkto konfigūracijos modelio komponento nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="d51a3-133">Create nomenclature for a product configuration model component</span></span>

1. <span data-ttu-id="d51a3-134">Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-134">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="d51a3-135">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d51a3-135">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="d51a3-136">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="d51a3-136">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="d51a3-137">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-137">Select **Edit**.</span></span>
1. <span data-ttu-id="d51a3-138">Lauke *Naudoti* onfigūracijos nomenklatūrą pasirinkite **Taip** .</span><span class="sxs-lookup"><span data-stu-id="d51a3-138">Select *Yes* in the **Use configuration nomenclature** field.</span></span>
1. <span data-ttu-id="d51a3-139">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-139">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-140">Rinkitės **Atributo vertė**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-140">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d51a3-141">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-141">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-142">Lauke **Atributas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-142">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d51a3-143">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-143">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-144">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-144">Select **Text constant**.</span></span>
1. <span data-ttu-id="d51a3-145">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-145">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-146">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-146">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d51a3-147">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-147">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-148">Rinkitės **Atributo vertė**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-148">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d51a3-149">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-149">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-150">Lauke **Atributas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-150">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d51a3-151">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-151">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-152">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-152">Select **Text constant**.</span></span>
1. <span data-ttu-id="d51a3-153">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-153">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-154">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-154">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d51a3-155">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-155">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-156">Rinkitės **Atributo vertė**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-156">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d51a3-157">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-157">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-158">Lauke **Atributas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-158">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d51a3-159">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-159">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-160">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-160">Select **Text constant**.</span></span>
1. <span data-ttu-id="d51a3-161">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-161">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-162">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-162">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d51a3-163">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-163">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-164">Rinkitės **Atributo vertė**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-164">Select **Attribute value**.</span></span>
1. <span data-ttu-id="d51a3-165">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-165">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-166">Lauke **Atributas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-166">In the **Attribute** field, enter or select a value.</span></span>
1. <span data-ttu-id="d51a3-167">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-167">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-168">Pažymėkite **Teksto konstanta**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-168">Select **Text constant**.</span></span>
1. <span data-ttu-id="d51a3-169">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-169">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-170">Lauke **Tekstas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-170">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="d51a3-171">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-171">Select **Add**.</span></span>
1. <span data-ttu-id="d51a3-172">Pasirinkite **Numeravimo sekos vertę**.</span><span class="sxs-lookup"><span data-stu-id="d51a3-172">Select **Number sequence value**.</span></span>
1. <span data-ttu-id="d51a3-173">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-173">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="d51a3-174">Lauke **Numeravimo seka** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d51a3-174">In the **Number sequence** field, enter or select a value.</span></span>
1. <span data-ttu-id="d51a3-175">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d51a3-175">Close the page.</span></span>
1. <span data-ttu-id="d51a3-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d51a3-176">Close the page.</span></span>
1. <span data-ttu-id="d51a3-177">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d51a3-177">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]