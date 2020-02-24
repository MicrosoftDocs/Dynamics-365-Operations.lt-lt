---
title: Organizacijos hierarchija Common Data Service
description: Šioje temoje aprašomas organizacijos duomenų integravimas tarp programų „Finance and Operations“ ir „Common Data Service“.
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
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019918"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="af468-103">Organizacijos hierarchija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="af468-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="af468-104">Kadangi „Dynamics 365 Finance“ yra finansų sistema, *„organizacija“* yra pagrindinė sąvoka, o sistemos sąranka pradedama nuo organizacijos hierarchijos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="af468-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="af468-105">Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="af468-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="af468-106">Nors „Common Data Service“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos.</span><span class="sxs-lookup"><span data-stu-id="af468-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="af468-107">Kaip „Common Data Service“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="af468-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="af468-108">Duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="af468-108">Data flow</span></span>

<span data-ttu-id="af468-109">Verslo ekosistema, kurią sudaro programos „Finance and Operations“ ir „Common Data Service“, ir toliau turės organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="af468-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="af468-110">Ši organizacijos hierarchija yra sukurta programose „Finance and Operations“, tačiau ji rodoma ir „Common Data Service“ informacijos ir išplėtimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="af468-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="af468-111">Toliau pateiktoje iliustracijoje parodyta organizacijos hierarchijos informacija, kuri rodoma „Common Data Service“ kaip vienpusis duomenų srautas iš programų „Finance and Operations“ į „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="af468-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Struktūros vaizdas](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="af468-113">Šablonai</span><span class="sxs-lookup"><span data-stu-id="af468-113">Templates</span></span>

<span data-ttu-id="af468-114">Organizacijos hierarchijos objektų schemos yra prieinamos duomenų sinchronizavimui į vieną pusę iš programų „Finance and Operations“ į „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="af468-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="af468-115">Šablonai</span><span class="sxs-lookup"><span data-stu-id="af468-115">Templates</span></span>

<span data-ttu-id="af468-116">Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="af468-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="af468-117">Kaip parodyta toliau esančioje lentelėje, sukurtas objektų schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="af468-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="af468-118">„Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="af468-118">Finance and Operations</span></span> | <span data-ttu-id="af468-119">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="af468-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="af468-120">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="af468-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="af468-121">Organizacijos hierarchijos tikslai</span><span class="sxs-lookup"><span data-stu-id="af468-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="af468-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="af468-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="af468-123">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchijos paskirtis.</span><span class="sxs-lookup"><span data-stu-id="af468-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="af468-124">Organizacijos hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="af468-124">Organization hierarchy type</span></span> | <span data-ttu-id="af468-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="af468-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="af468-126">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchijos tipas.</span><span class="sxs-lookup"><span data-stu-id="af468-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="af468-127">Organizacijos hierarchija – publikuota</span><span class="sxs-lookup"><span data-stu-id="af468-127">Organization hierarchy - published</span></span> | <span data-ttu-id="af468-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="af468-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="af468-129">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchija publikuota.</span><span class="sxs-lookup"><span data-stu-id="af468-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="af468-130">Valdymo vienetas</span><span class="sxs-lookup"><span data-stu-id="af468-130">Operating unit</span></span> | <span data-ttu-id="af468-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="af468-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="af468-132">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="af468-132">Legal entities</span></span> | <span data-ttu-id="af468-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="af468-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="af468-134">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="af468-134">Legal entities</span></span> | <span data-ttu-id="af468-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="af468-135">cdm_companies</span></span> | <span data-ttu-id="af468-136">Suteikiama juridinio subjekto (įmonės) informacijos dvikrypčio sinchronizavimo galimybė.</span><span class="sxs-lookup"><span data-stu-id="af468-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="af468-137">Vidinė organizacija</span><span class="sxs-lookup"><span data-stu-id="af468-137">Internal Organization</span></span>

<span data-ttu-id="af468-138">Vidinės organizacijos informacija, esanti „Common Data Service“ gaunama iš dviejų objektų – **valdymo vieneto** ir **juridinių subjektų**.</span><span class="sxs-lookup"><span data-stu-id="af468-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

