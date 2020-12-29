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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414389"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="9efe3-103">Pardavimo ir mokėjimų internetu registravimas</span><span class="sxs-lookup"><span data-stu-id="9efe3-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9efe3-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="9efe3-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="9efe3-105">Internetinių pardavimo ir mokėjimų registravimas apima du etapus.</span><span class="sxs-lookup"><span data-stu-id="9efe3-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="9efe3-106">Internetinių „Commerce“ operacijų duomenų rinkimas būstinėje.</span><span class="sxs-lookup"><span data-stu-id="9efe3-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="9efe3-107">Sinchronizuojant užsakymus, siekiant sukurti pardavimo užsakymus buveinėje.</span><span class="sxs-lookup"><span data-stu-id="9efe3-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="9efe3-108">Internetinių operacijų duomenis galite rinkti rankiniu būdu paleidę P užduotį arba sukurdami pasikartojančią paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="9efe3-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="9efe3-109">Gavimo užduoties vykdymas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="9efe3-109">Manually running the P-job</span></span>

1. <span data-ttu-id="9efe3-110">Eikite į Visos darbo sritys > „Retail and Commerce IT“.</span><span class="sxs-lookup"><span data-stu-id="9efe3-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="9efe3-111">Spustelėkite paskirstymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="9efe3-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="9efe3-112">Pasirinkite P-0001.</span><span class="sxs-lookup"><span data-stu-id="9efe3-112">Select P-0001.</span></span>
4. <span data-ttu-id="9efe3-113">Jei reikia, pritaikykite kanalo duomenų bazės grupes.</span><span class="sxs-lookup"><span data-stu-id="9efe3-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="9efe3-114">Spustelėkite Paleisti dabar.</span><span class="sxs-lookup"><span data-stu-id="9efe3-114">Click Run now.</span></span>
6. <span data-ttu-id="9efe3-115">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="9efe3-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="9efe3-116">Pasikartojančios gavimo užduoties planavimas</span><span class="sxs-lookup"><span data-stu-id="9efe3-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="9efe3-117">Eikite į Visos darbo sritys > „Retail and Commerce IT“.</span><span class="sxs-lookup"><span data-stu-id="9efe3-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="9efe3-118">Spustelėkite paskirstymo grafiką.</span><span class="sxs-lookup"><span data-stu-id="9efe3-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="9efe3-119">Pasirinkite P-0001.</span><span class="sxs-lookup"><span data-stu-id="9efe3-119">Select P-0001.</span></span>
4. <span data-ttu-id="9efe3-120">Spustelėkite Kurti paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="9efe3-120">Click Create batch job.</span></span>
5. <span data-ttu-id="9efe3-121">Spustelėkite Veikti fone.</span><span class="sxs-lookup"><span data-stu-id="9efe3-121">Click Run in the background.</span></span>
5. <span data-ttu-id="9efe3-122">Įgalinkite paketinį vykdymą.</span><span class="sxs-lookup"><span data-stu-id="9efe3-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="9efe3-123">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="9efe3-123">Click Recurrence..</span></span>
7. <span data-ttu-id="9efe3-124">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="9efe3-124">Select the No end date option.</span></span>
8. <span data-ttu-id="9efe3-125">Lauke Skaičius įveskite paleisčių per minutę intervalą.</span><span class="sxs-lookup"><span data-stu-id="9efe3-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="9efe3-126">Įprastai nurodoma 5-10.</span><span class="sxs-lookup"><span data-stu-id="9efe3-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="9efe3-127">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9efe3-127">Click OK.</span></span>
10. <span data-ttu-id="9efe3-128">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9efe3-128">Click OK.</span></span>

<span data-ttu-id="9efe3-129">Užsakymai gali būti sinchronizuojami rankiniu būdu paleidžiant „Sinchronizuoti užsakymus“ užduotį arba sukuriant pasikartojančią paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="9efe3-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="9efe3-130">Užsakymo sinchronizacijos paleidimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="9efe3-130">Manually running order synchronization</span></span> 

<span data-ttu-id="9efe3-131">Norėdami rankiniu būdu vieną kartą paleisti „Sinchronizuoti užsakymus“ užduotį, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="9efe3-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="9efe3-132">Eikite į Visos darbo sritys > Parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="9efe3-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="9efe3-133">Spustelėkite Sinchronizuoti užsakymus.</span><span class="sxs-lookup"><span data-stu-id="9efe3-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="9efe3-134">Lauke Organizacijos hierarchija pasirinkite „Parduotuvės pagal regioną“.</span><span class="sxs-lookup"><span data-stu-id="9efe3-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="9efe3-135">Pasirinkite konkrečią interneto parduotuvę arba pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="9efe3-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="9efe3-136">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="9efe3-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="9efe3-137">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="9efe3-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="9efe3-138">Išjunkite paketinį vykdymą</span><span class="sxs-lookup"><span data-stu-id="9efe3-138">Disable Batch processing</span></span>
6. <span data-ttu-id="9efe3-139">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="9efe3-139">Click Recurrence.</span></span>
7. <span data-ttu-id="9efe3-140">Pasirinkite parinktį Baigto po.</span><span class="sxs-lookup"><span data-stu-id="9efe3-140">Select End After option</span></span>
8. <span data-ttu-id="9efe3-141">Lauke Baigti po įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="9efe3-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="9efe3-142">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9efe3-142">Click OK.</span></span>
10. <span data-ttu-id="9efe3-143">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9efe3-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="9efe3-144">Pasikartojančio užsakymų sinchronizavimo planavimas</span><span class="sxs-lookup"><span data-stu-id="9efe3-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="9efe3-145">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančią paketinę užduotį, norint kurti internetinės parduotuvės operacijų pardavimo užsakymus ir mokėjimus.</span><span class="sxs-lookup"><span data-stu-id="9efe3-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="9efe3-146">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="9efe3-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9efe3-147">Eikite į Visos darbo sritys > Parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="9efe3-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="9efe3-148">Spustelėkite Sinchronizuoti užsakymus.</span><span class="sxs-lookup"><span data-stu-id="9efe3-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="9efe3-149">Lauke Organizacijos hierarchija pasirinkite „Parduotuvės pagal regioną“.</span><span class="sxs-lookup"><span data-stu-id="9efe3-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="9efe3-150">Pasirinkite konkrečią interneto parduotuvę arba pasirinkite mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="9efe3-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="9efe3-151">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="9efe3-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="9efe3-152">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="9efe3-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="9efe3-153">Įgalinkite paketinį vykdymą</span><span class="sxs-lookup"><span data-stu-id="9efe3-153">Enable Batch processing</span></span>
6. <span data-ttu-id="9efe3-154">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="9efe3-154">Click Recurrence.</span></span>
7. <span data-ttu-id="9efe3-155">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="9efe3-155">Select the No end date option.</span></span>
8. <span data-ttu-id="9efe3-156">Lauke Skaičius įveskite paleisčių per minutę intervalą.</span><span class="sxs-lookup"><span data-stu-id="9efe3-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="9efe3-157">Įprastai nurodoma 2-20</span><span class="sxs-lookup"><span data-stu-id="9efe3-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="9efe3-158">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9efe3-158">Click OK.</span></span>
10. <span data-ttu-id="9efe3-159">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="9efe3-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="9efe3-160">Proceso duomenų objektai</span><span class="sxs-lookup"><span data-stu-id="9efe3-160">Data entities involved in the process</span></span>

- <span data-ttu-id="9efe3-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="9efe3-161">RetailTransactionTable</span></span>
- <span data-ttu-id="9efe3-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="9efe3-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="9efe3-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="9efe3-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="9efe3-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="9efe3-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="9efe3-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="9efe3-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="9efe3-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="9efe3-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="9efe3-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="9efe3-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="9efe3-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="9efe3-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="9efe3-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="9efe3-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="9efe3-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="9efe3-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="9efe3-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="9efe3-171">RetailTransactionAttributeTrans</span></span>
