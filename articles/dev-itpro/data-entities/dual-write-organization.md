---
title: Organizacijos hierarchija Common Data Service
description: Šioje temoje aprašomas organizacinių duomenų integravimas tarp „Finance and Operations“ ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789223"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="8a160-103">Organizacijos hierarchija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="8a160-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="8a160-104">Kadangi „Microsoft Dynamics 365 for Finance and Operations“ yra finansų sistema, *„organizacija“* yra pagrindinė sąvoka, o sistemos sąranka pradedama nuo organizacijos hierarchijos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="8a160-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="8a160-105">Verslo finansai ir operacijos gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="8a160-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="8a160-106">Nors „Common Data Service“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos.</span><span class="sxs-lookup"><span data-stu-id="8a160-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="8a160-107">Kaip „Common Data Service“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="8a160-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="8a160-108">Duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="8a160-108">Data flow</span></span>

<span data-ttu-id="8a160-109">Verslo ekosistema, kurią sudaro „Finance and Operations“ ir „Common Data Service“, toliau turės organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="8a160-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="8a160-110">Ši organizacijos hierarchija pagrįsta „Finance and Operations“, tačiau ji rodoma programoje „Common Data Service“ informaciniais ir išplėtimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="8a160-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="8a160-111">Toliau pateiktame paveikslėlyje pavaizduota organizacijos hierarchijos informacija, kuri rodoma programoje Common Data Service kaip vienpusis duomenų srautas iš „Finance and Operations“ į Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8a160-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Struktūros vaizdas](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="8a160-113">Šablonai</span><span class="sxs-lookup"><span data-stu-id="8a160-113">Templates</span></span>

<span data-ttu-id="8a160-114">Organizacijos hierarchijos objekto schemos prieinamos vienpusiui duomenų sinchronizavimui iš „Finance and Operations“ į Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8a160-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="8a160-115">Prižiūrėti organizacijos hierarchijos paskirtis</span><span class="sxs-lookup"><span data-stu-id="8a160-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="8a160-116">Šis šablonas pateikia organizacijos hierarchijos paskirties objekto vienpusį sinchronizavimą iš „Finance and Operations“ į „Dynamics 365 for Customer Engagement“.</span><span class="sxs-lookup"><span data-stu-id="8a160-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="8a160-117">Šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-117">Source field</span></span> | <span data-ttu-id="8a160-118">Schemos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-118">Map type</span></span> | <span data-ttu-id="8a160-119">Paskirties laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-119">Destination field</span></span>
---|---|---
<span data-ttu-id="8a160-120">Hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="8a160-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="8a160-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="8a160-122">Hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="8a160-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8a160-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="8a160-124">Hierarchijos paskirtis</span><span class="sxs-lookup"><span data-stu-id="8a160-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="8a160-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="8a160-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="8a160-126">Nekintamas</span><span class="sxs-lookup"><span data-stu-id="8a160-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="8a160-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="8a160-127">msdyn\_immutable</span></span>
<span data-ttu-id="8a160-128">Nustatyti kaip numatytąją</span><span class="sxs-lookup"><span data-stu-id="8a160-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="8a160-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="8a160-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="8a160-130">Vidinis organizacijos hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="8a160-131">Šis šablonas pateikia organizacijos hierarchijos tipo objekto vienpusį sinchronizavimą iš „Finance and Operations“ į „Customer Engagement“.</span><span class="sxs-lookup"><span data-stu-id="8a160-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="8a160-132">Šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-132">Source field</span></span> | <span data-ttu-id="8a160-133">Schemos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-133">Map type</span></span> | <span data-ttu-id="8a160-134">Paskirties laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-134">Destination field</span></span>
---|---|---
<span data-ttu-id="8a160-135">PAVADINIMAS</span><span class="sxs-lookup"><span data-stu-id="8a160-135">NAME</span></span> | \> | <span data-ttu-id="8a160-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8a160-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="8a160-137">Vidinis organizacijos hierarchija</span><span class="sxs-lookup"><span data-stu-id="8a160-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="8a160-138">Šis šablonas pateikia organizacijos hierarchijos publikuoto objekto vienpusį sinchronizavimą iš „Finance and Operations“ į „Customer Engagement“.</span><span class="sxs-lookup"><span data-stu-id="8a160-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="8a160-139">Šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-139">Source field</span></span> | <span data-ttu-id="8a160-140">Schemos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-140">Map type</span></span> | <span data-ttu-id="8a160-141">Paskirties laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-141">Destination field</span></span>
---|---|---
<span data-ttu-id="8a160-142">Galioja iki</span><span class="sxs-lookup"><span data-stu-id="8a160-142">VALIDTO</span></span> | \> | <span data-ttu-id="8a160-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="8a160-143">msdyn\_validto</span></span>
<span data-ttu-id="8a160-144">Galioja nuo</span><span class="sxs-lookup"><span data-stu-id="8a160-144">VALIDFROM</span></span> | \> | <span data-ttu-id="8a160-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="8a160-145">msdyn\_validfrom</span></span>
<span data-ttu-id="8a160-146">Hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="8a160-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="8a160-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="8a160-148">Pirminės organizacijos įrašo numeris</span><span class="sxs-lookup"><span data-stu-id="8a160-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="8a160-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="8a160-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="8a160-150">Antrinės organizacijos įrašo numeris</span><span class="sxs-lookup"><span data-stu-id="8a160-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="8a160-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="8a160-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="8a160-152">Hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="8a160-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8a160-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="8a160-154">Antrinės organizacijos įrašo numeris</span><span class="sxs-lookup"><span data-stu-id="8a160-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="8a160-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="8a160-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="8a160-156">Pirminės organizacijos įrašo numeris</span><span class="sxs-lookup"><span data-stu-id="8a160-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="8a160-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="8a160-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="8a160-158">Vidinė organizacija</span><span class="sxs-lookup"><span data-stu-id="8a160-158">Internal Organization</span></span>

<span data-ttu-id="8a160-159">Vidinės organizacijos informacija, esanti „Common Data Service“ gaunama iš dviejų „Finance and Operations“ objektų – **valdymo vieneto** ir **juridinių subjektų**.</span><span class="sxs-lookup"><span data-stu-id="8a160-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="8a160-160">Valdymo vienetas</span><span class="sxs-lookup"><span data-stu-id="8a160-160">Operating unit</span></span>

<span data-ttu-id="8a160-161">Šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-161">Source field</span></span> | <span data-ttu-id="8a160-162">Schemos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-162">Map type</span></span> | <span data-ttu-id="8a160-163">Paskirties laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-163">Destination field</span></span>
---|---|---
<span data-ttu-id="8a160-164">Kalbos ID</span><span class="sxs-lookup"><span data-stu-id="8a160-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="8a160-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="8a160-165">msdyn\_languageid</span></span>
<span data-ttu-id="8a160-166">Vardo pseudonimas</span><span class="sxs-lookup"><span data-stu-id="8a160-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="8a160-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="8a160-167">msdyn\_namealias</span></span>
<span data-ttu-id="8a160-168">PAVADINIMAS</span><span class="sxs-lookup"><span data-stu-id="8a160-168">NAME</span></span> | \> | <span data-ttu-id="8a160-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8a160-169">msdyn\_name</span></span>
<span data-ttu-id="8a160-170">Įrašo numeris</span><span class="sxs-lookup"><span data-stu-id="8a160-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="8a160-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="8a160-171">msdyn\_partynumber</span></span>
<span data-ttu-id="8a160-172">Valdymo vienetų tipai</span><span class="sxs-lookup"><span data-stu-id="8a160-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="8a160-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="8a160-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="8a160-174">Juridinis subjektas</span><span class="sxs-lookup"><span data-stu-id="8a160-174">Legal entity</span></span>

<span data-ttu-id="8a160-175">Šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-175">Source field</span></span> | <span data-ttu-id="8a160-176">Schemos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-176">Map type</span></span> | <span data-ttu-id="8a160-177">Paskirties laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-177">Destination field</span></span>
---|---|---
<span data-ttu-id="8a160-178">Vardo pseudonimas</span><span class="sxs-lookup"><span data-stu-id="8a160-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="8a160-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="8a160-179">msdyn\_namealias</span></span>
<span data-ttu-id="8a160-180">Kalbos ID</span><span class="sxs-lookup"><span data-stu-id="8a160-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="8a160-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="8a160-181">msdyn\_languageid</span></span>
<span data-ttu-id="8a160-182">PAVADINIMAS</span><span class="sxs-lookup"><span data-stu-id="8a160-182">NAME</span></span> | \> | <span data-ttu-id="8a160-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="8a160-183">msdyn\_name</span></span>
<span data-ttu-id="8a160-184">Įrašo numeris</span><span class="sxs-lookup"><span data-stu-id="8a160-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="8a160-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="8a160-185">msdyn\_partynumber</span></span>
<span data-ttu-id="8a160-186">nėra</span><span class="sxs-lookup"><span data-stu-id="8a160-186">none</span></span> | \>\> | <span data-ttu-id="8a160-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="8a160-187">msdyn\_type</span></span>
<span data-ttu-id="8a160-188">Juridinio subjekto ID</span><span class="sxs-lookup"><span data-stu-id="8a160-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="8a160-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="8a160-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="8a160-190">Įmonė</span><span class="sxs-lookup"><span data-stu-id="8a160-190">Company</span></span>

<span data-ttu-id="8a160-191">Pateikia juridinio subjekto (įmonės) informacijos dvikrypį sinchronizavimą tarp „Finance and Operations“ ir „Customer Engagement“.</span><span class="sxs-lookup"><span data-stu-id="8a160-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="8a160-192">Šaltinio laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-192">Source field</span></span> | <span data-ttu-id="8a160-193">Schemos tipas</span><span class="sxs-lookup"><span data-stu-id="8a160-193">Map type</span></span> | <span data-ttu-id="8a160-194">Paskirties laukas</span><span class="sxs-lookup"><span data-stu-id="8a160-194">Destination field</span></span>
---|---|---
<span data-ttu-id="8a160-195">PAVADINIMAS</span><span class="sxs-lookup"><span data-stu-id="8a160-195">NAME</span></span> | = | <span data-ttu-id="8a160-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="8a160-196">cdm\_name</span></span>
<span data-ttu-id="8a160-197">Juridinio subjekto ID</span><span class="sxs-lookup"><span data-stu-id="8a160-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="8a160-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="8a160-198">cdm\_companycode</span></span>
