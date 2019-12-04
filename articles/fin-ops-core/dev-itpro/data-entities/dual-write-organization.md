---
title: Organizacijos hierarchija Common Data Service
description: Šioje temoje aprašomas organizacinių duomenų integravimas tarp „Finance and Operations“ programų ir „Common Data Service“.
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
ms.openlocfilehash: 9efc63c385c31a6d8848d016c1a8689460908dcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769665"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="6feee-103">Organizacijos hierarchija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6feee-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6feee-104">Kadangi „Dynamics 365 Finance“ yra finansų sistema, *„organizacija“* yra pagrindinė sąvoka, o sistemos sąranka pradedama nuo organizacijos hierarchijos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="6feee-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="6feee-105">Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="6feee-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="6feee-106">Nors „Common Data Service“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos.</span><span class="sxs-lookup"><span data-stu-id="6feee-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="6feee-107">Kaip „Common Data Service“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="6feee-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="6feee-108">Duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="6feee-108">Data flow</span></span>

<span data-ttu-id="6feee-109">Verslo ekosistema, kurią sudaro „Finance and Operations“ programos ir „Common Data Service“, toliau turės organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="6feee-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="6feee-110">Ši organizacijos hierarchija pagrįsta „Finance and Operations“ programomis, tačiau ji rodoma programoje „Common Data Service“ informaciniais ir išplėtimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="6feee-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="6feee-111">Toliau pateiktame paveikslėlyje pavaizduota organizacijos hierarchijos informacija, kuri rodoma programoje „Common Data Service” kaip vienpusis duomenų srautas iš „Finance and Operations“ programų į „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="6feee-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Struktūros vaizdas](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="6feee-113">Šablonai</span><span class="sxs-lookup"><span data-stu-id="6feee-113">Templates</span></span>

<span data-ttu-id="6feee-114">Organizacijos hierarchijos objekto schemos prieinamos vienpusiui duomenų sinchronizavimui iš „Finance and Operations“ programų į „Common Data Service”.</span><span class="sxs-lookup"><span data-stu-id="6feee-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="6feee-115">Šablonai</span><span class="sxs-lookup"><span data-stu-id="6feee-115">Templates</span></span>

<span data-ttu-id="6feee-116">Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="6feee-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="6feee-117">Kaip parodyta toliau esančioje lentelėje, sukurtas objektų schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="6feee-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="6feee-118">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="6feee-118">Finance and Operations</span></span> | <span data-ttu-id="6feee-119">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="6feee-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="6feee-120">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="6feee-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="6feee-121">Organizacijos hierarchijos tikslai</span><span class="sxs-lookup"><span data-stu-id="6feee-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="6feee-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="6feee-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="6feee-123">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchijos paskirtis.</span><span class="sxs-lookup"><span data-stu-id="6feee-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="6feee-124">Organizacijos hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="6feee-124">Organization hierarchy type</span></span> | <span data-ttu-id="6feee-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="6feee-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="6feee-126">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchijos tipas.</span><span class="sxs-lookup"><span data-stu-id="6feee-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="6feee-127">Organizacijos hierarchija – publikuota</span><span class="sxs-lookup"><span data-stu-id="6feee-127">Organization hierarchy - published</span></span> | <span data-ttu-id="6feee-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="6feee-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="6feee-129">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchija publikuota.</span><span class="sxs-lookup"><span data-stu-id="6feee-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="6feee-130">Valdymo vienetas</span><span class="sxs-lookup"><span data-stu-id="6feee-130">Operating unit</span></span> | <span data-ttu-id="6feee-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="6feee-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="6feee-132">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="6feee-132">Legal entities</span></span> | <span data-ttu-id="6feee-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="6feee-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="6feee-134">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="6feee-134">Legal entities</span></span> | <span data-ttu-id="6feee-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="6feee-135">cdm_companies</span></span> | <span data-ttu-id="6feee-136">Suteikiama juridinio subjekto (įmonės) informacijos dvikrypčio sinchronizavimo galimybė.</span><span class="sxs-lookup"><span data-stu-id="6feee-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](dual-write/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](dual-write/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](dual-write/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="6feee-137">Vidinė organizacija</span><span class="sxs-lookup"><span data-stu-id="6feee-137">Internal Organization</span></span>

<span data-ttu-id="6feee-138">Vidinės organizacijos informacija, esanti „Common Data Service“ gaunama iš dviejų objektų – **valdymo vieneto** ir **juridinių subjektų**.</span><span class="sxs-lookup"><span data-stu-id="6feee-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](dual-write/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](dual-write/LegalEntities-Companies.md)]

