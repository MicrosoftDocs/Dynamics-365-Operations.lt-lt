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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000739"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="ab1cb-103">Organizacijos hierarchija Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ab1cb-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab1cb-104">Kadangi „Dynamics 365 Finance“ yra finansų sistema, *„organizacija“* yra pagrindinė sąvoka, o sistemos sąranka pradedama nuo organizacijos hierarchijos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="ab1cb-105">Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="ab1cb-106">Nors „Common Data Service“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="ab1cb-107">Kaip „Common Data Service“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="ab1cb-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="ab1cb-108">Duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="ab1cb-108">Data flow</span></span>

<span data-ttu-id="ab1cb-109">Verslo ekosistema, kurią sudaro programos „Finance and Operations“ ir „Common Data Service“, ir toliau turės organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="ab1cb-110">Ši organizacijos hierarchija yra sukurta programose „Finance and Operations“, tačiau ji rodoma ir „Common Data Service“ informacijos ir išplėtimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="ab1cb-111">Toliau pateiktoje iliustracijoje parodyta organizacijos hierarchijos informacija, kuri rodoma „Common Data Service“ kaip vienpusis duomenų srautas iš programų „Finance and Operations“ į „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Struktūros vaizdas](media/dual-write-data-flow.png)

<span data-ttu-id="ab1cb-113">Organizacijos hierarchijos objektų schemos yra prieinamos duomenų sinchronizavimui į vieną pusę iš programų „Finance and Operations“ į „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="ab1cb-114">Šablonai</span><span class="sxs-lookup"><span data-stu-id="ab1cb-114">Templates</span></span>

<span data-ttu-id="ab1cb-115">Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="ab1cb-116">Kaip parodyta toliau esančioje lentelėje, sukurtas objektų schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="ab1cb-117">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="ab1cb-117">Finance and Operations apps</span></span> | <span data-ttu-id="ab1cb-118">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="ab1cb-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="ab1cb-119">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ab1cb-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="ab1cb-120">Organizacijos hierarchijos tikslai</span><span class="sxs-lookup"><span data-stu-id="ab1cb-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="ab1cb-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="ab1cb-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="ab1cb-122">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchijos paskirtis.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="ab1cb-123">Organizacijos hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="ab1cb-123">Organization hierarchy type</span></span> | <span data-ttu-id="ab1cb-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="ab1cb-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="ab1cb-125">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchijos tipas.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="ab1cb-126">Organizacijos hierarchija – publikuota</span><span class="sxs-lookup"><span data-stu-id="ab1cb-126">Organization hierarchy - published</span></span> | <span data-ttu-id="ab1cb-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="ab1cb-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="ab1cb-128">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti objektą Organizacijos hierarchija publikuota.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="ab1cb-129">Valdymo vienetas</span><span class="sxs-lookup"><span data-stu-id="ab1cb-129">Operating unit</span></span> | <span data-ttu-id="ab1cb-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="ab1cb-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="ab1cb-131">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="ab1cb-131">Legal entities</span></span> | <span data-ttu-id="ab1cb-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="ab1cb-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="ab1cb-133">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="ab1cb-133">Legal entities</span></span> | <span data-ttu-id="ab1cb-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="ab1cb-134">cdm_companies</span></span> | <span data-ttu-id="ab1cb-135">Suteikiama juridinio subjekto (įmonės) informacijos dvikrypčio sinchronizavimo galimybė.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="ab1cb-136">Vidinė organizacija</span><span class="sxs-lookup"><span data-stu-id="ab1cb-136">Internal Organization</span></span>

<span data-ttu-id="ab1cb-137">Vidinės organizacijos informacija, esanti „Common Data Service“ gaunama iš dviejų objektų – **valdymo vieneto** ir **juridinių subjektų**.</span><span class="sxs-lookup"><span data-stu-id="ab1cb-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
