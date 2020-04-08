---
title: Pardavimo ir mokėjimų internetu registravimas
description: Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140789"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="b2ac5-103">Pardavimo ir mokėjimų internetu registravimas</span><span class="sxs-lookup"><span data-stu-id="b2ac5-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2ac5-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="b2ac5-105">Internetinių pardavimo ir mokėjimų registravimas apima du etapus.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="b2ac5-106">Internetinių „Commerce“ operacijų duomenų rinkimas būstinėje.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="b2ac5-107">Sinchronizuojant užsakymus, siekiant sukurti pardavimo užsakymus buveinėje.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="b2ac5-108">Internetinių operacijų duomenis galite rinkti rankiniu būdu paleidę P užduotį arba sukurdami pasikartojančią paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="b2ac5-109">Gavimo užduoties vykdymas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="b2ac5-109">Manually running the P-job</span></span>

1. <span data-ttu-id="b2ac5-110">Eikite į Visos darbo sritys > „Retail and Commerce IT“.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="b2ac5-111">Spustelėkite paskirstymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="b2ac5-112">Pasirinkite P-0001.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-112">Select P-0001.</span></span>
4. <span data-ttu-id="b2ac5-113">Jei reikia, pritaikykite kanalo duomenų bazės grupes.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="b2ac5-114">Spustelėkite Paleisti dabar.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-114">Click Run now.</span></span>
6. <span data-ttu-id="b2ac5-115">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="b2ac5-116">Pasikartojančios gavimo užduoties planavimas</span><span class="sxs-lookup"><span data-stu-id="b2ac5-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="b2ac5-117">Eikite į Visos darbo sritys > „Retail and Commerce IT“.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="b2ac5-118">Spustelėkite paskirstymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="b2ac5-119">Pasirinkite P-0001.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-119">Select P-0001.</span></span>
4. <span data-ttu-id="b2ac5-120">Spustelėkite Kurti paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-120">Click Create batch job.</span></span>
5. <span data-ttu-id="b2ac5-121">Spustelėkite Veikti fone.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-121">Click Run in the background.</span></span>
5. <span data-ttu-id="b2ac5-122">Įgalinkite paketinį vykdymą.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="b2ac5-123">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-123">Click Recurrence..</span></span>
7. <span data-ttu-id="b2ac5-124">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-124">Select the No end date option.</span></span>
8. <span data-ttu-id="b2ac5-125">Lauke Skaičius įveskite paleisčių per minutę intervalą.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="b2ac5-126">Įprastai nurodoma 5-10.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="b2ac5-127">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-127">Click OK.</span></span>
10. <span data-ttu-id="b2ac5-128">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-128">Click OK.</span></span>

<span data-ttu-id="b2ac5-129">Užsakymai gali būti sinchronizuojami rankiniu būdu paleidžiant „Sinchronizuoti užsakymus“ užduotį arba sukuriant pasikartojančią paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="b2ac5-130">Užsakymo sinchronizacijos paleidimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="b2ac5-130">Manually running order synchronization</span></span> 

<span data-ttu-id="b2ac5-131">Norėdami rankiniu būdu vieną kartą paleisti „Sinchronizuoti užsakymus“ užduotį, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="b2ac5-132">Eikite į Visos darbo sritys > Parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="b2ac5-133">Spustelėkite Sinchronizuoti užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="b2ac5-134">Lauke Organizacijos hierarchija pasirinkite „Parduotuvės pagal regioną“.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="b2ac5-135">Pasirinkite konkrečią interneto parduotuvę arba pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="b2ac5-136">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="b2ac5-137">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="b2ac5-138">Išjunkite paketinį vykdymą</span><span class="sxs-lookup"><span data-stu-id="b2ac5-138">Disable Batch processing</span></span>
6. <span data-ttu-id="b2ac5-139">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-139">Click Recurrence.</span></span>
7. <span data-ttu-id="b2ac5-140">Pasirinkite parinktį Baigto po.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-140">Select End After option</span></span>
8. <span data-ttu-id="b2ac5-141">Lauke Baigti po įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="b2ac5-142">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-142">Click OK.</span></span>
10. <span data-ttu-id="b2ac5-143">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="b2ac5-144">Pasikartojančio užsakymų sinchronizavimo planavimas</span><span class="sxs-lookup"><span data-stu-id="b2ac5-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="b2ac5-145">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="b2ac5-146">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="b2ac5-147">Eikite į Visos darbo sritys > Parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="b2ac5-148">Spustelėkite Sinchronizuoti užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="b2ac5-149">Lauke Organizacijos hierarchija pasirinkite „Parduotuvės pagal regioną“.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="b2ac5-150">Pasirinkite konkrečią interneto parduotuvę arba pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="b2ac5-151">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="b2ac5-152">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="b2ac5-153">Įgalinkite paketinį vykdymą</span><span class="sxs-lookup"><span data-stu-id="b2ac5-153">Enable Batch processing</span></span>
6. <span data-ttu-id="b2ac5-154">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-154">Click Recurrence.</span></span>
7. <span data-ttu-id="b2ac5-155">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-155">Select the No end date option.</span></span>
8. <span data-ttu-id="b2ac5-156">Lauke Skaičius įveskite paleisčių per minutę intervalą.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="b2ac5-157">Įprastai nurodoma 2-20</span><span class="sxs-lookup"><span data-stu-id="b2ac5-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="b2ac5-158">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-158">Click OK.</span></span>
10. <span data-ttu-id="b2ac5-159">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="b2ac5-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="b2ac5-160">Proceso duomenų objektai</span><span class="sxs-lookup"><span data-stu-id="b2ac5-160">Data entities involved in the process</span></span>

- <span data-ttu-id="b2ac5-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="b2ac5-161">RetailTransactionTable</span></span>
- <span data-ttu-id="b2ac5-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="b2ac5-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="b2ac5-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="b2ac5-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="b2ac5-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="b2ac5-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="b2ac5-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="b2ac5-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="b2ac5-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="b2ac5-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="b2ac5-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="b2ac5-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="b2ac5-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="b2ac5-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="b2ac5-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="b2ac5-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="b2ac5-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="b2ac5-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="b2ac5-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="b2ac5-171">RetailTransactionAttributeTrans</span></span>
