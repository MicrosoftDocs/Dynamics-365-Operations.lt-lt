---
title: „Warehouse Management” mobiliųjų įrenginių programėlės veiksmų piktogramų ir pavadinimų priskyrimas
description: Šioje temoje aprašoma, kaip priskirti veiksmų piktogramas ir pavadinimus naujiems ar pritaikytiems užduočių srautams „Warehouse Management” mobiliųjų įrenginių programėlėje.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049369"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="ed6bd-103">„Warehouse Management” mobiliųjų įrenginių programėlės veiksmų piktogramų ir pavadinimų priskyrimas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed6bd-104">Šioje temoje aprašoma, kaip priskirti veiksmų piktogramas ir veiksmų pavadinimus naujiems ar pritaikytiems užduočių srautams „Warehouse Management” mobiliųjų įrenginių programėlėje.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ed6bd-105">Toliau pateikti pavyzdžiai rodo, kaip veiksmų piktogramos ir pavadinimai rodomi „Warehouse Management” mobiliųjų įrenginių programėlėje.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="ed6bd-106">![Veiksmo piktogramos ir veiksmo pavadinimo pavyzdys „Warehouse Management” mobiliųjų įrenginių programėlėje](media/step-icon-example.png "Veiksmo piktogramos ir veiksmo pavadinimo pavyzdys „Warehouse Management” mobiliųjų įrenginių programėlėje")</span><span class="sxs-lookup"><span data-stu-id="ed6bd-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="ed6bd-107">Funkcijos įjungimas jūsų sistemoje</span><span class="sxs-lookup"><span data-stu-id="ed6bd-107">Turn on this feature in your system</span></span>

<span data-ttu-id="ed6bd-108">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ed6bd-109">Administratoriai gali naudoti [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nustatymus tam, kad patikrintų funkcijos būseną ir ją įjungtų.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ed6bd-110">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ed6bd-111">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="ed6bd-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ed6bd-112">**Funkcijos pavadinimas:** *Naujos sandėlio programos vartotojo parametrai, piktogramos ir veiksmų pavadinimai*</span><span class="sxs-lookup"><span data-stu-id="ed6bd-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="ed6bd-113">Standartinės veiksmo ID, klasės ir piktogramos</span><span class="sxs-lookup"><span data-stu-id="ed6bd-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="ed6bd-114">Kiekvienas užduočių srauto veiksmas identifikuojamas pagal veiksmo ID, o kiekvieno veiksmo ID turi atitinkamą veiksmo klasę.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="ed6bd-115">Veiksmo piktograma ir pavadinimas yra nurodyti kiekvienoje veiksmo klasėje.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="ed6bd-116">Veiksmų ID ir veiksmų klasės</span><span class="sxs-lookup"><span data-stu-id="ed6bd-116">Step IDs and step classes</span></span>

<span data-ttu-id="ed6bd-117">Toliau esančioje lentelėje pateikiama kiekvieno šiuo metu prieinamo veiksmo ID ir atitinkama veiksmo klasė.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="ed6bd-118">Pirminio įvesties lauko valdiklio pavadinimas yra naudojamas kaip veiksmo ID.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="ed6bd-119">Pavyzdį, kuriame parodyta, kaip naudojamos šios veiksmų ID ir klasės, rasite „`WHSMobileAppStepInfoBuilder.stepId()`” metodo diegimo straipsnyje [Pavyzdys: Pasirinktinio srauto veiksmų piktogramų ir pavadinimų priskyrimas](#example), pateiktame toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="ed6bd-120">Veiksmo ID</span><span class="sxs-lookup"><span data-stu-id="ed6bd-120">Step ID</span></span> | <span data-ttu-id="ed6bd-121">Veiksmo klasė</span><span class="sxs-lookup"><span data-stu-id="ed6bd-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="ed6bd-122">„BatchDisposition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-122">BatchDisposition</span></span> | <span data-ttu-id="ed6bd-123">„WHSMobileAppStepBatchDisposition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="ed6bd-124">Vežėjas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-124">Carrier</span></span> | <span data-ttu-id="ed6bd-125">„WHSMobileAppStepCarrier”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="ed6bd-126">„CatchWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-126">CatchWeight</span></span> | <span data-ttu-id="ed6bd-127">„WHSMobileAppStepCatchWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ed6bd-128">„CatchWeightQtyOutboundWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="ed6bd-129">„WHSMobileAppStepCatchWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ed6bd-130">„CatchWeightTag”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-130">CatchWeightTag</span></span> | <span data-ttu-id="ed6bd-131">„WHSMobileAppStepCatchWeightTag”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="ed6bd-132">„CatchWeightTagWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="ed6bd-133">„WHSMobileAppStepCatchWeightTagWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="ed6bd-134">„ChangeWarehouseSuccess”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="ed6bd-135">„WHSMobileAppStepChangeWarehouseSuccess”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="ed6bd-136">„CheckDigit”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-136">CheckDigit</span></span> | <span data-ttu-id="ed6bd-137">„WHSMobileAppStepCheckDigit”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="ed6bd-138">„ClusterId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-138">ClusterId</span></span> | <span data-ttu-id="ed6bd-139">„WHSMobileAppStepClusterId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="ed6bd-140">„ClusterPickQtyVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="ed6bd-141">„WHSMobileAppStepQtyVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ed6bd-142">„ClusterPosition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-142">ClusterPosition</span></span> | <span data-ttu-id="ed6bd-143">„WHSMobileAppStepClusterPosition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="ed6bd-144">„ConfigId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-144">ConfigId</span></span> | <span data-ttu-id="ed6bd-145">„WHSMobileAppStepConfigId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="ed6bd-146">Patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-146">Confirmation</span></span> | <span data-ttu-id="ed6bd-147">„WHSMobileAppStepConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="ed6bd-148">„ConsolidateFromLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="ed6bd-149">„WHSMobileAppStepConsolidateFromLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="ed6bd-150">„ConsolidateLPConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="ed6bd-151">„WHSMobileAppStepConsolidateLPConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="ed6bd-152">„ConsolidateToLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="ed6bd-153">„WHSMobileAppStepConsolidateToLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="ed6bd-154">„ContainerType”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-154">ContainerType</span></span> | <span data-ttu-id="ed6bd-155">„WHSMobileAppStepContainerType”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="ed6bd-156">„CountingReasonCode”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-156">CountingReasonCode</span></span> | <span data-ttu-id="ed6bd-157">„WHSMobileAppStepCountingReasonCode”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="ed6bd-158">„CycleCountingAddLPOrFinish”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="ed6bd-159">„WHSMobileAppStepCycleCountingAddLPOrFinish”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="ed6bd-160">„CycleCountQty1”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-160">CycleCountQty1</span></span> | <span data-ttu-id="ed6bd-161">„WHSMobileAppStepCycleCountQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ed6bd-162">„CycleCountQty2”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-162">CycleCountQty2</span></span> | <span data-ttu-id="ed6bd-163">„WHSMobileAppStepCycleCountQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ed6bd-164">„CycleCountQty3”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-164">CycleCountQty3</span></span> | <span data-ttu-id="ed6bd-165">„WHSMobileAppStepCycleCountQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ed6bd-166">„CycleCountQty4”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-166">CycleCountQty4</span></span> | <span data-ttu-id="ed6bd-167">„WHSMobileAppStepCycleCountQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="ed6bd-168">Perdavimas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-168">Disposition</span></span> | <span data-ttu-id="ed6bd-169">„WHSMobileAppStepDisposition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="ed6bd-170">„DriverCheckInConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="ed6bd-171">„WHSMobileAppStepDriverCheckInConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="ed6bd-172">„DriverCheckInId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-172">DriverCheckInId</span></span> | <span data-ttu-id="ed6bd-173">„WHSMobileAppStepDriverCheckInId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="ed6bd-174">„DriverCheckOutConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="ed6bd-175">„WHSMobileAppStepDriverCheckOutConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="ed6bd-176">„DriverCheckOutId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-176">DriverCheckOutId</span></span> | <span data-ttu-id="ed6bd-177">„WHSMobileAppStepDriverCheckOutId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="ed6bd-178">„ExpDate”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-178">ExpDate</span></span> | <span data-ttu-id="ed6bd-179">„WHSMobileAppStepExpDate”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="ed6bd-180">„FromBatchDisposition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-180">FromBatchDisposition</span></span> | <span data-ttu-id="ed6bd-181">„WHSMobileAppStepFromBatchDisposition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="ed6bd-182">„FromInventoryStatus”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-182">FromInventoryStatus</span></span> | <span data-ttu-id="ed6bd-183">„WHSMobileAppStepInventoryStatusFrom”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="ed6bd-184">„FullQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-184">FullQty</span></span> | <span data-ttu-id="ed6bd-185">„WHSMobileAppStepFullQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="ed6bd-186">„InboundPut”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-186">InboundPut</span></span> | <span data-ttu-id="ed6bd-187">„WHSMobileAppStepInboundPut”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="ed6bd-188">„InventBatchId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-188">InventBatchId</span></span> | <span data-ttu-id="ed6bd-189">„WHSMobileAppStepBatch”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="ed6bd-190">„InventColorId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-190">InventColorId</span></span> | <span data-ttu-id="ed6bd-191">„WHSMobileAppStepInventColorId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="ed6bd-192">„InventLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-192">InventLocation</span></span> | <span data-ttu-id="ed6bd-193">„WHSMobileAppStepInventLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="ed6bd-194">„InventLocationId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-194">InventLocationId</span></span> | <span data-ttu-id="ed6bd-195">„WHSMobileAppStepWarehouse”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="ed6bd-196">„InventSerialId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-196">InventSerialId</span></span> | <span data-ttu-id="ed6bd-197">„WHSMobileAppStepInventSerialId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="ed6bd-198">„InventSizeId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-198">InventSizeId</span></span> | <span data-ttu-id="ed6bd-199">„WHSMobileAppStepInventSizeId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="ed6bd-200">„InventStatusId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-200">InventStatusId</span></span> | <span data-ttu-id="ed6bd-201">„WHSMobileAppStepInventStatus”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="ed6bd-202">„InventStyleId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-202">InventStyleId</span></span> | <span data-ttu-id="ed6bd-203">„WHSMobileAppStepInventStyleId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="ed6bd-204">„InventVersionId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-204">InventVersionId</span></span> | <span data-ttu-id="ed6bd-205">„WHSMobileAppStepInventVersionId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="ed6bd-206">„ItemId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-206">ItemId</span></span> | <span data-ttu-id="ed6bd-207">„WHSMobileAppStepItem”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="ed6bd-208">„ITMContainerID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-208">ITMContainerID</span></span> | <span data-ttu-id="ed6bd-209">„ITMMobileAppStepContainerId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="ed6bd-210">„ITMShipmentID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-210">ITMShipmentID</span></span> | <span data-ttu-id="ed6bd-211">„ITMMobileAppStepShipmentId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="ed6bd-212">„KanbanCardId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-212">KanbanCardId</span></span> | <span data-ttu-id="ed6bd-213">„WHSMobileAppStepKanbanCard”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="ed6bd-214">„KanbanCardToEmpty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="ed6bd-215">„WHSMobileAppStepKanbanCardToEmpty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="ed6bd-216">„KanbanOrCardId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-216">KanbanOrCardId</span></span> | <span data-ttu-id="ed6bd-217">„WHSMobileAppStepKanbanCard”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="ed6bd-218">„LicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-218">LicensePlateId</span></span> | <span data-ttu-id="ed6bd-219">„WHSMobileAppStepLicensePlate”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="ed6bd-220">„LoadId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-220">LoadId</span></span> | <span data-ttu-id="ed6bd-221">„WHSMobileAppStepLoadId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="ed6bd-222">„LocationLicensePlatePosition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="ed6bd-223">„WHSMobileAppStepLocationLicensePlatePosition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="ed6bd-224">„LocOrLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-224">LocOrLP</span></span> | <span data-ttu-id="ed6bd-225">„WHSMobileAppStepLocOrLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="ed6bd-226">„LocOrLP_From”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-226">LocOrLP_From</span></span> | <span data-ttu-id="ed6bd-227">„WHSMobileAppStepLocOrLPFrom”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="ed6bd-228">„LocOrLP_To”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-228">LocOrLP_To</span></span> | <span data-ttu-id="ed6bd-229">„WHSMobileAppStepLocOrLPTo”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="ed6bd-230">„LocOrLPCheck”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-230">LocOrLPCheck</span></span> | <span data-ttu-id="ed6bd-231">„WHSMobileAppStepLocOrLPCheck”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="ed6bd-232">„LocVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-232">LocVerification</span></span> | <span data-ttu-id="ed6bd-233">„WHSMobileAppStepLocVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="ed6bd-234">„LPAdjustIn”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-234">LPAdjustIn</span></span> | <span data-ttu-id="ed6bd-235">„WHSMobileAppStepLPAdjustIn”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="ed6bd-236">„LPBreakChildLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-236">LPBreakChildLP</span></span> | <span data-ttu-id="ed6bd-237">„WHSMobileAppStepLPBreakChildLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="ed6bd-238">„LPBreakParentLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-238">LPBreakParentLP</span></span> | <span data-ttu-id="ed6bd-239">„WHSMobileAppStepLPBreakParentLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="ed6bd-240">„LPBuildChildLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-240">LPBuildChildLP</span></span> | <span data-ttu-id="ed6bd-241">„WHSMobileAppStepLPBuildChildLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="ed6bd-242">„LPBuildParentLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-242">LPBuildParentLP</span></span> | <span data-ttu-id="ed6bd-243">„WHSMobileAppStepLPBuildParentLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="ed6bd-244">„LPVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-244">LPVerification</span></span> | <span data-ttu-id="ed6bd-245">„WHSMobileAppStepLPVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="ed6bd-246">„MergeContainerId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-246">MergeContainerId</span></span> | <span data-ttu-id="ed6bd-247">„WHSMobileAppStepMergeContainerId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="ed6bd-248">„MixedLPLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-248">MixedLPLineNum</span></span> | <span data-ttu-id="ed6bd-249">„WHSMobileAppStepMixedLPLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="ed6bd-250">„MobileDeviceQueueMessageCollectionIdentifierId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="ed6bd-251">„WHSMobileAppStepSelectOrder”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="ed6bd-252">„MovementConfirmCancel”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-252">MovementConfirmCancel</span></span> | <span data-ttu-id="ed6bd-253">„WHSMobileAppStepMovementConfirmCancel”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="ed6bd-254">„NewCaptureWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-254">NewCaptureWeight</span></span> | <span data-ttu-id="ed6bd-255">„WHSMobileAppStepCatchWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ed6bd-256">„NewQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-256">NewQty</span></span> | <span data-ttu-id="ed6bd-257">„WHSMobileAppStepNewQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="ed6bd-258">„OutboundCatchWeightTag”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="ed6bd-259">„WHSMobileAppStepCatchWeightTag”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="ed6bd-260">„OutboundPut”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-260">OutboundPut</span></span> | <span data-ttu-id="ed6bd-261">„WHSMobileAppStepOutboundPut”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="ed6bd-262">„OutboundWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-262">OutboundWeight</span></span> | <span data-ttu-id="ed6bd-263">„WHSMobileAppStepCatchWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="ed6bd-264">„OverridePutNewLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-264">OverridePutNewLocation</span></span> | <span data-ttu-id="ed6bd-265">„WHSMobileAppStepOverridePutNewLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="ed6bd-266">„PieceByPieceConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="ed6bd-267">„WHSMobileAppStepQtyVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ed6bd-268">„POLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-268">POLineNum</span></span> | <span data-ttu-id="ed6bd-269">„WHSMobileAppStepPOLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="ed6bd-270">PU numeris</span><span class="sxs-lookup"><span data-stu-id="ed6bd-270">PONum</span></span> | <span data-ttu-id="ed6bd-271">„WHSMobileAppStepPONum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="ed6bd-272">„PositionFull”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-272">PositionFull</span></span> | <span data-ttu-id="ed6bd-273">„WHSMobileAppStepPositionFull”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="ed6bd-274">„PositionFullQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-274">PositionFullQty</span></span> | <span data-ttu-id="ed6bd-275">„WHSMobileAppStepPositionFullQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="ed6bd-276">Stiprumas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-276">Potency</span></span> | <span data-ttu-id="ed6bd-277">„WHSMobileAppStepPotency”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="ed6bd-278">„PrinterName”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-278">PrinterName</span></span> | <span data-ttu-id="ed6bd-279">„WHSMobileAppStepPrinterName”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="ed6bd-280">„ProdId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-280">ProdId</span></span> | <span data-ttu-id="ed6bd-281">„WHSMobileAppStepProdId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="ed6bd-282">„ProdLastPalletConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="ed6bd-283">„WHSMobileAppStepProdLastPalletConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="ed6bd-284">„ProductConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-284">ProductConfirmation</span></span> | <span data-ttu-id="ed6bd-285">„WHSMobileAppStepProductConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="ed6bd-286">„ProductionScrapConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="ed6bd-287">„WHSMobileAppStepProductionScrapConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="ed6bd-288">Dėti</span><span class="sxs-lookup"><span data-stu-id="ed6bd-288">Put</span></span> | <span data-ttu-id="ed6bd-289">„WHSMobileAppStepPut”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="ed6bd-290">„PutawayClusterId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-290">PutawayClusterId</span></span> | <span data-ttu-id="ed6bd-291">„WHSMobileAppStepPutawayClusterId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="ed6bd-292">Kiekis</span><span class="sxs-lookup"><span data-stu-id="ed6bd-292">Qty</span></span> | <span data-ttu-id="ed6bd-293">„WHSMobileAppStepQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="ed6bd-294">„QtyAdjust”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-294">QtyAdjust</span></span> | <span data-ttu-id="ed6bd-295">„WHSMobileAppStepQtyAdjust”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="ed6bd-296">„QtyShort”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-296">QtyShort</span></span> | <span data-ttu-id="ed6bd-297">„WHSMobileAppStepQtyShort”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="ed6bd-298">„QtyToConsume”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-298">QtyToConsume</span></span> | <span data-ttu-id="ed6bd-299">„WHSMobileAppStepQtyToConsume”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="ed6bd-300">„QtyToPick”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-300">QtyToPick</span></span> | <span data-ttu-id="ed6bd-301">„WHSMobileAppStepQtyToPick”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="ed6bd-302">„QtyToPut”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-302">QtyToPut</span></span> | <span data-ttu-id="ed6bd-303">„WHSMobileAppStepQtyToPut”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="ed6bd-304">„QtyToScrap”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-304">QtyToScrap</span></span> | <span data-ttu-id="ed6bd-305">„WHSMobileAppStepQtyToScrap”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="ed6bd-306">„QtyVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-306">QtyVerification</span></span> | <span data-ttu-id="ed6bd-307">„WHSMobileAppStepQtyVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="ed6bd-308">„QtyWithScanningLimit”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="ed6bd-309">„WHSMobileAppStepQtyAdjust”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="ed6bd-310">„ReasonString”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-310">ReasonString</span></span> | <span data-ttu-id="ed6bd-311">„WHSMobileAppStepReasonString”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="ed6bd-312">„RecvLocationId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-312">RecvLocationId</span></span> | <span data-ttu-id="ed6bd-313">„WHSMobileAppStepRecvLocationId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="ed6bd-314">„RemoveContainerId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-314">RemoveContainerId</span></span> | <span data-ttu-id="ed6bd-315">„WHSMobileAppStepRemoveContainerId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="ed6bd-316">„ReprintLabelConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="ed6bd-317">„WHSMobileAppStepReprintLabelConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="ed6bd-318">„RMANum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-318">RMANum</span></span> | <span data-ttu-id="ed6bd-319">„WHSMobileAppStepRMANum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="ed6bd-320">„ShortPickReason”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-320">ShortPickReason</span></span> | <span data-ttu-id="ed6bd-321">„WHSMobileAppStepShortPickReason”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="ed6bd-322">„SortConOrLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-322">SortConOrLP</span></span> | <span data-ttu-id="ed6bd-323">„WHSMobileAppStepSortConOrLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="ed6bd-324">„SortLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-324">SortLicensePlateId</span></span> | <span data-ttu-id="ed6bd-325">„WHSMobileAppStepSortLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="ed6bd-326">„SortPositionId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-326">SortPositionId</span></span> | <span data-ttu-id="ed6bd-327">„WHSMobileAppStepSortPositionId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="ed6bd-328">„SortVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-328">SortVerification</span></span> | <span data-ttu-id="ed6bd-329">„WHSMobileAppStepSortVerification”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="ed6bd-330">„StartLocationId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-330">StartLocationId</span></span> | <span data-ttu-id="ed6bd-331">„WHSMobileAppStepStartLocationId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="ed6bd-332">„StartProdOrderConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="ed6bd-333">„WHSMobileAppStepStartProdOrderConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="ed6bd-334">„TargetLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-334">TargetLicensePlateId</span></span> | <span data-ttu-id="ed6bd-335">„WHSMobileAppStepTargetLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="ed6bd-336">„TOLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-336">TOLineNum</span></span> | <span data-ttu-id="ed6bd-337">„WHSMobileAppStepTOLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="ed6bd-338">„ToLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-338">ToLocation</span></span> | <span data-ttu-id="ed6bd-339">„WHSMobileAppStepToLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="ed6bd-340">„TONum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-340">TONum</span></span> | <span data-ttu-id="ed6bd-341">„WHSMobileAppStepTONum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="ed6bd-342">„ToWarehouse”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-342">ToWarehouse</span></span> | <span data-ttu-id="ed6bd-343">„WHSMobileAppStepWarehouseTo”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="ed6bd-344">„TransportLoadId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-344">TransportLoadId</span></span> | <span data-ttu-id="ed6bd-345">„WHSMobileAppStepTransportLoadId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="ed6bd-346">„WaveLabelId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-346">WaveLabelId</span></span> | <span data-ttu-id="ed6bd-347">„WHSMobileAppStepWaveLabelId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="ed6bd-348">„WaveLblQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-348">WaveLblQty</span></span> | <span data-ttu-id="ed6bd-349">„WHSMobileAppStepWaveLblQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="ed6bd-350">Svoris</span><span class="sxs-lookup"><span data-stu-id="ed6bd-350">Weight</span></span> | <span data-ttu-id="ed6bd-351">„WHSMobileAppStepWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="ed6bd-352">„WeightToConsume”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-352">WeightToConsume</span></span> | <span data-ttu-id="ed6bd-353">„WHSMobileAppStepWeightToConsume”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="ed6bd-354">„WHSAdjustmentType”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-354">WHSAdjustmentType</span></span> | <span data-ttu-id="ed6bd-355">„WHSMobileAppStepWHSAdjustmentType”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="ed6bd-356">„WHSReceivingException”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-356">WHSReceivingException</span></span> | <span data-ttu-id="ed6bd-357">„WHSMobileAppStepWHSReceivingException”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="ed6bd-358">„WHSWorkException”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-358">WHSWorkException</span></span> | <span data-ttu-id="ed6bd-359">„WHSMobileAppStepWHSWorkException”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="ed6bd-360">„WHSWorkLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="ed6bd-361">„WHSMobileAppStepWorkLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="ed6bd-362">„WMSLocationId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-362">WMSLocationId</span></span> | <span data-ttu-id="ed6bd-363">„WHSMobileAppStepLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="ed6bd-364">„WorkId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-364">WorkId</span></span> | <span data-ttu-id="ed6bd-365">„WHSMobileAppStepWorkId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="ed6bd-366">„WorkIdToCancel”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-366">WorkIdToCancel</span></span> | <span data-ttu-id="ed6bd-367">„WHSMobileAppStepWorkIdToCancel”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="ed6bd-368">„WorkLPIdPutawayCluster”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="ed6bd-369">„WHSMobileAppStepWorkLPIdPutawayCluster”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="ed6bd-370">„WorkPoolId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-370">WorkPoolId</span></span> | <span data-ttu-id="ed6bd-371">„WHSMobileAppStepWorkPoolId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="ed6bd-372">„ZoneId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-372">ZoneId</span></span> | <span data-ttu-id="ed6bd-373">„WHSMobileAppStepZoneId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="ed6bd-374">Galimos veiksmų piktogramos</span><span class="sxs-lookup"><span data-stu-id="ed6bd-374">Available step icons</span></span>

<span data-ttu-id="ed6bd-375">Sistemoje yra standartinių veiksmų piktogramų, kurias taip pat galite naudoti atlikdami pasirinktinius veiksmus, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="ed6bd-376">Šiuo metu negalite įkelti pasirinktinių veiksmų piktogramų.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="ed6bd-377">Todėl visada turite pasirinkti vieną iš standartinių veiksmų piktogramų.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="ed6bd-378">Šioje lentelėje rodoma kiekviena šiuo metu prieinama standartinė veiksmo piktograma ir jos pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Apie veiksmo piktogramą"><br><span data-ttu-id="ed6bd-380">Apie</span><span class="sxs-lookup"><span data-stu-id="ed6bd-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Numerio lentelės įtraukimo arba prekės veiksmo piktograma"><br><span data-ttu-id="ed6bd-382">„AddLpOrItem”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Paketų perdavimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-384">„BatchDisposition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Vežėjo veiksmo piktograma"><br><span data-ttu-id="ed6bd-386">Vežėjas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Esamo svorio žymės veiksmo piktograma"><br><span data-ttu-id="ed6bd-388">„CatchWeightTag”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Esamo svorio žymės svorio veiksmo piktograma"><br><span data-ttu-id="ed6bd-390">„CatchWeightTagWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Skaitmens tikrinimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-392">„CheckDigit”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Įsiregistravimo arba išsiregistravimo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-394">„CheckInOutId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Antrinės numerio lentelės veiksmo piktograma"><br><span data-ttu-id="ed6bd-396">„ChildLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Klasterio ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-398">„ClusterId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Klasterio padėties veiksmo piktograma"><br><span data-ttu-id="ed6bd-400">„ClusterPosition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Konfigūracijos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-402">„ConfigId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Sukonfigūruoto lauko veiksmo piktograma"><br><span data-ttu-id="ed6bd-404">„ConfiguredField”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Konfigūravimo arba numerio lentelės veiksmo piktograma"><br><span data-ttu-id="ed6bd-406">„ConOrLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsoliduoja iš numerio lentelės ID veiksmo piktogramos"><br><span data-ttu-id="ed6bd-408">„ConsolidateFromLicensePlateID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsoliduoja į numerio lentelės ID veiksmo piktogramą"><br><span data-ttu-id="ed6bd-410">„ConsolidateToLicensePlateID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Konteinerio tipo veiksmo piktograma"><br><span data-ttu-id="ed6bd-412">„ContainerType”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Inventorizacijos veiksmo piktograma"><br><span data-ttu-id="ed6bd-414">Inventorizacija</span><span class="sxs-lookup"><span data-stu-id="ed6bd-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Inventorizacijos priežasties kodo veiksmo piktograma"><br><span data-ttu-id="ed6bd-416">„CountingReasonCode”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Kilmės šalies kodo veiksmo piktograma"><br><span data-ttu-id="ed6bd-418">„CountryOfOrigin”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Perdavimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-420">Perdavimas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Atlikto veiksmo piktograma"><br><span data-ttu-id="ed6bd-422">Atlikta</span><span class="sxs-lookup"><span data-stu-id="ed6bd-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Vairuotojo įsiregistravimo patvirtinimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-424">„DriverCheckInConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Vairuotojo įsiregistravimo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-426">„DriverCheckInId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Vairuotojo išsiregistravimo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-428">„DriverCheckOutId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Galiojimo datos veiksmo piktograma"><br><span data-ttu-id="ed6bd-430">„ExpDate”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Lauko veiksmo piktograma"><br><span data-ttu-id="ed6bd-432">Laukas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Perdavimo iš paketo veiksmo piktograma"><br><span data-ttu-id="ed6bd-434">„FromBatchDisposition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Būsenos iš atsargų veiksmo piktograma"><br><span data-ttu-id="ed6bd-436">„FromInventoryStatus”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ID atributo veiksmo piktograma"><br><span data-ttu-id="ed6bd-438">„IdAttribute”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Atsargų paketo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-440">„InventBatchID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Atsargų spalvos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-442">„InventColorID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Atsargų vietos veiksmo piktograma"><br><span data-ttu-id="ed6bd-444">„InventLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Atsargų serijos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-446">„InventSerialID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Atsargų dydžio ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-448">„InventSizeID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Atsargų būsenos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-450">„InventStatusID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Atsargų stiliaus ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-452">„InventStyleID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Atsargų versijos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-454">„InventVersionID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Prekės ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-456">„ItemID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM konteinerio ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-458">„ITMContainerID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM siuntos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-460">„ITMShipmentID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="„Kanban” kortelės ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-462">„KanbanCardID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="„Kanban” arba kortelės ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-464">„KanbanOrCardID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Numerio lentelės ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-466">„LicensePlateID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Krovinio ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-468">„LoadId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Vietos numerio lentelės padėties veiksmo piktograma"><br><span data-ttu-id="ed6bd-470">„LocationLicensePlatePosition”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Vietos arba numerio lentelės veiksmo piktograma"><br><span data-ttu-id="ed6bd-472">„LocOrLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Vietos arba numerio lentelės patikrinimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-474">„LocOrLPCheck”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Iš vietos arba numerio lentelės piktograma"><br><span data-ttu-id="ed6bd-476">„LocOrLPFrom”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Į vietą arba numerio lentelę veiksmo piktograma"><br><span data-ttu-id="ed6bd-478">„LocOrLPTo”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Užbaigto ilgo proceso piktograma"><br><span data-ttu-id="ed6bd-480">„LongProcessCompleted”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="Numerio lentelės lūžio pirminės numerio lentelės veiksmo piktograma"><br><span data-ttu-id="ed6bd-482">„LPBreakParentLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Konteinerių suliejimo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-484">„MergeContainerId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Mišrios numerio lentelės eilutės numerio veiksmo piktograma"><br><span data-ttu-id="ed6bd-486">„MixedLPLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Siunčiamo svorio veiksmo piktograma"><br><span data-ttu-id="ed6bd-488">„OutboundWeight”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Savininko veiksmo piktograma"><br><span data-ttu-id="ed6bd-490">Savininkas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Pirminės numerio lentelės veiksmo piktograma"><br><span data-ttu-id="ed6bd-492">„ParentLP”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Patvirtinkite veiksmo piktogramą"><br><span data-ttu-id="ed6bd-494">„PleaseConfirm”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Pirkimo užsakymo eilutės numerio veiksmo piktograma"><br><span data-ttu-id="ed6bd-496">„POLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Pirkimo užsakymo numerio veiksmo piktograma"><br><span data-ttu-id="ed6bd-498">PU numeris</span><span class="sxs-lookup"><span data-stu-id="ed6bd-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Pilnos padėties veiksmo piktograma"><br><span data-ttu-id="ed6bd-500">„PositionFull”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Stiprumo veiksmo piktograma"><br><span data-ttu-id="ed6bd-502">Stiprumas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Spausdintuvo pavadinimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-504">„PrinterName”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Gamybos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-506">„ProdId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Produkto patvirtinimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-508">„ProductConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Padėjimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-510">Dėti</span><span class="sxs-lookup"><span data-stu-id="ed6bd-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Atidėjimo klasterio ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-512">„PutawayClusterId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Kiekio veiksmo piktograma"><br><span data-ttu-id="ed6bd-514">Kiekis</span><span class="sxs-lookup"><span data-stu-id="ed6bd-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Kiekio koregavimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-516">„QtyAdjustIn”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Nevisiškai paimto kiekio veiksmo piktograma"><br><span data-ttu-id="ed6bd-518">„QtyShort”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Suvartotino kiekio veiksmo piktograma"><br><span data-ttu-id="ed6bd-520">„QtyToConsume”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Atidėtino kiekio veiksmo piktograma"><br><span data-ttu-id="ed6bd-522">„QtyToPut”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Nurašytino kiekio veiksmo piktograma"><br><span data-ttu-id="ed6bd-524">„QtyToScrap”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Kiekio patvirtinimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-526">„QuantityConfirmation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Paskelbimo apie baigtą užduotį veiksmo piktograma"><br><span data-ttu-id="ed6bd-528">„RAFEndJob”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Vietos gavimo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-530">„RecvLocationID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Konteinerių šalinimo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-532">„RemoveContainerID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA numerio veiksmo piktograma"><br><span data-ttu-id="ed6bd-534">„RMANum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Užsakymo pasirinkimo veiksmo piktograma"><br><span data-ttu-id="ed6bd-536">„SelectOrder”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Nevisiško paėmimo priežasties veiksmo piktograma"><br><span data-ttu-id="ed6bd-538">„ShortPickReason”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Rikiavimo padėties ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-540">„SortPositionId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Tikslinės numerio lentelės ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-542">„TargetLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Į eilutės numerį veiksmo piktograma"><br><span data-ttu-id="ed6bd-544">„ToLineNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Į vietą veiksmo piktograma"><br><span data-ttu-id="ed6bd-546">„ToLocation”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Į numerį veiksmo piktograma"><br><span data-ttu-id="ed6bd-548">„ToNum”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Į sandėlį veiksmo piktograma"><br><span data-ttu-id="ed6bd-550">„ToWarehouse”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Krovinio transportavimo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-552">„TransportLoadId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Tiekėjo paketo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-554">„VendBatchId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Bangos žymos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-556">„WaveLabelId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Bangos žymos kiekio veiksmo piktograma"><br><span data-ttu-id="ed6bd-558">„WaveLblQty”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Svorio veiksmo piktograma"><br><span data-ttu-id="ed6bd-560">Svoris</span><span class="sxs-lookup"><span data-stu-id="ed6bd-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Suvartotino svorio veiksmo piktograma"><br><span data-ttu-id="ed6bd-562">„WeightToConsume”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS koregavimo tipo veiksmo piktograma"><br><span data-ttu-id="ed6bd-564">„WHSAdjustmentType”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS gavimo išimties veiksmo piktograma"><br><span data-ttu-id="ed6bd-566">„WHSReceivingException”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS vietos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-568">„WMSLocationID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Darbo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-570">„WorkId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Atšauktino darbo ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-572">„WorkIdToCancel”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Darbo numerio lentelės ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-574">„WorkLicensePlateId”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Darbo numerio lentelės atidėjimo klasterio ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-576">„WorkLPIDPutawayCluster”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Darbo telkinio ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-578">„WorkPoolID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Zonos ID veiksmo piktograma"><br><span data-ttu-id="ed6bd-580">„ZoneID”</span><span class="sxs-lookup"><span data-stu-id="ed6bd-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="ed6bd-581">Pavyzdys: Priskirkite pasirinktinio srauto veiksmų piktogramas ir pavadinimus</span><span class="sxs-lookup"><span data-stu-id="ed6bd-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="ed6bd-582">Šiame pavyzdyje paaiškinama, kaip nustatyti pasirinktinio užduočių srauto veiksmų piktogramas ir pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="ed6bd-583">Scenarijus yra sukurtas pagal pasirinktinio užduočių srauto pavyzdį, kuris yra pateiktas ir išsamiau ištyrinėtas šiame tinklaraščio skelbime: [Sandėliavimo mobiliųjų įrenginių programėlės tinkinimas](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="ed6bd-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="ed6bd-584">Užduočių srautas veikia toliau nurodytu būdu:</span><span class="sxs-lookup"><span data-stu-id="ed6bd-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="ed6bd-585">Programoje rodomas puslapis, kuriame darbuotojas paraginamas pateikti konteinerio ID (pavyzdžiui, nuskaitant brūkšninį kodą).</span><span class="sxs-lookup"><span data-stu-id="ed6bd-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="ed6bd-586">Jei konteinerio ID tinkamas, programa atidaro naują puslapį, kuriame darbuotojas yra paraginamas įvesti informaciją apie svorį.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="ed6bd-587">(Jei konteinerio ID netinkamas, darbuotojas grąžinamas į pirmąjį puslapį.)</span><span class="sxs-lookup"><span data-stu-id="ed6bd-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="ed6bd-588">Kai darbuotojas įveda tinkamą svorį, sistema išsaugo svorį ir grąžina darbuotoją į pirmąjį puslapį.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="ed6bd-589">Toliau pateiktoje iliustracijoje vaizduojamas šis užduoties srautas.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="ed6bd-590">![Užduoties srauto diagrama](media/step-icons-example-task-flow.png "Užduoties srauto diagrama")</span><span class="sxs-lookup"><span data-stu-id="ed6bd-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="ed6bd-591">Veiksmo klasės kūrimas konteinerio įvesties puslapiui</span><span class="sxs-lookup"><span data-stu-id="ed6bd-591">Create a step class for the container input page</span></span>

<span data-ttu-id="ed6bd-592">Konteinerio įvesties puslapis leidžia darbuotojui nuskaityti arba įvesti konteinerio ID.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="ed6bd-593">![Konteinerio įvesties puslapis](media/step-icons-example-container-input.png "Konteinerio įvesties puslapis")</span><span class="sxs-lookup"><span data-stu-id="ed6bd-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="ed6bd-594">Konteinerio įvesties puslapyje įvesties lauko valdiklio pavadinimas yra „`ContainerId`”.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="ed6bd-595">Kadangi šio valdiklio pavadinimo nėra [veiksmų ID sąraše](#step-ids-classes), nerasite juo pagrįsto esamo veiksmo.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="ed6bd-596">Todėl turite sukurti veiksmo klasę, atspindinčią veiksmą.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="ed6bd-597">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="ed6bd-598">Veiksmo piktogramos identifikatorius yra saugomas „`defaultStepIcon`” klasės nariui, o veiksmo pavadinimas yra saugomas „`defaultStepTitle`” klasės nariui.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="ed6bd-599">Norėdami priskirti veiksmo piktogramą, nustatykite „`defaultStepIcon`” į vieną iš piktogramos ID, išvardytų skyriuje [Galimos veiksmų piktogramos](#step-icons), esančiame anksčiau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="ed6bd-600">Standartinės arba pasirinktinės veiksmo piktogramos ir pavadinimo naudojimas svorio įvesčiai</span><span class="sxs-lookup"><span data-stu-id="ed6bd-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="ed6bd-601">Svorio įvesties puslapis leidžia darbuotojui įvesti svorį.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="ed6bd-602">![Svorio įvesties puslapis](media/step-icons-example-weight-input.png "Svorio įvesties puslapis")</span><span class="sxs-lookup"><span data-stu-id="ed6bd-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="ed6bd-603">Svorio įvesties puslapio įvesties lauko valdiklio pavadinimas yra „`Weight`”, kuris yra [veiksmų ID sąraše](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="ed6bd-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="ed6bd-604">Todėl, jei jums priimtini veiksmo piktograma ir pavadinimas, apibrėžti „`WHSMobileAppStepWeight`” klasėje, šiame veiksme jums nereikia nieko keisti.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="ed6bd-605">Tačiau, jei norite naudoti kitą šio veiksmo piktogramą ar pavadinimą, galite pakeisti „`stepId()`” arba „`stepInfo()`” metodą daryklės klasėje.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="ed6bd-606">Kiekvienas užduočių srautas turi savo veiksmų informacijos daryklę.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="ed6bd-607">Metodo „stepId()” keitimas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-607">Override the stepId() method</span></span>

<span data-ttu-id="ed6bd-608">Toliau pateiktame pavyzdyje parodomas vienas būdas, kuriuo galite modifikuoti daryklės klasę, pakeisdami „`stepId()`” metodą.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="ed6bd-609">Tada sukuriate veiksmo klasę „`NewWeight`” veiksmui.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="ed6bd-610">Kodas turėtų būti panašus į „`ContainerId`” pavyzdžio kodą, parodytą anksčiau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="ed6bd-611">Metodo „stepInfo()” keitimas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-611">Override the stepInfo() method</span></span>

<span data-ttu-id="ed6bd-612">Toliau pateiktame pavyzdyje parodomas vienas būdas, kuriuo galite modifikuoti daryklės klasę, pakeisdami „`stepInfo()`” metodą.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="ed6bd-613">Tada sukonstruojate „`WHSMobileAppStepInfo`” objektą ir tiesiogiai nustatote piktogramą ir (arba) pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ed6bd-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed6bd-614">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ed6bd-614">Additional resources</span></span>

- [<span data-ttu-id="ed6bd-615">Sandėlio valdymo mobiliųjų įrenginių programėlės diegimas ir prijungimas</span><span class="sxs-lookup"><span data-stu-id="ed6bd-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="ed6bd-616">Mobiliojo įrenginio naudotojo nustatymai</span><span class="sxs-lookup"><span data-stu-id="ed6bd-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
