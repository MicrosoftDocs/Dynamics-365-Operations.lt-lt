---
title: Organizacijos hierarchija Dataverse
description: Šioje temoje aprašomas organizacijos duomenų integravimas tarp programų „Finance and Operations“ ir „Dataverse“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f265d49a87383e2abf129b8d1d67567fc4b9e0de
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559584"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="656e1-103">Organizacijos hierarchija Dataverse</span><span class="sxs-lookup"><span data-stu-id="656e1-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="656e1-104">Kadangi „Dynamics 365 Finance“ yra finansų sistema, *„organizacija“* yra pagrindinė sąvoka, o sistemos sąranka pradedama nuo organizacijos hierarchijos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="656e1-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="656e1-105">Verslo finansai gali būti stebimi organizacijos lygiu ir taip pat bet kuriuo organizacijos hierarchijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="656e1-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="656e1-106">Nors „Dataverse“ neturi organizacijos hierarchijos sąvokos, joje yra kelios laisvos sąvokos, pvz., visų pardavimo įplaukos.</span><span class="sxs-lookup"><span data-stu-id="656e1-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="656e1-107">Kaip „Dataverse“ integravimo dalis, organizacijos hierarchijos duomenų struktūra įtraukiamą į „Dataverse“</span><span class="sxs-lookup"><span data-stu-id="656e1-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="656e1-108">Duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="656e1-108">Data flow</span></span>

<span data-ttu-id="656e1-109">Verslo ekosistema, kurią sudaro programos „Finance and Operations“ ir „Dataverse“, ir toliau turės organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="656e1-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="656e1-110">Ši organizacijos hierarchija yra sukurta programose „Finance and Operations“, tačiau ji rodoma ir „Dataverse“ informacijos ir išplėtimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="656e1-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="656e1-111">Toliau pateiktoje iliustracijoje parodyta organizacijos hierarchijos informacija, kuri rodoma „Dataverse“ kaip vienpusis duomenų srautas iš programų „Finance and Operations“ į „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="656e1-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Struktūros vaizdas](media/dual-write-data-flow.png)

<span data-ttu-id="656e1-113">Organizacijos hierarchijos lentelių schemos yra prieinamos duomenų sinchronizavimui į vieną pusę iš programų „Finance and Operations“ į „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="656e1-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="656e1-114">Šablonai</span><span class="sxs-lookup"><span data-stu-id="656e1-114">Templates</span></span>

<span data-ttu-id="656e1-115">Produkto informacija apima visą su produktu ir jo apibrėžtimi susijusią informaciją, pvz., produkto dimensijas arba sekimo ir saugojimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="656e1-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="656e1-116">Kaip parodyta toliau esančioje lentelėje, sukurtas lentelių schemų rinkinys, skirtas produktų ir susijusios informacijos sinchronizavimui.</span><span class="sxs-lookup"><span data-stu-id="656e1-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="656e1-117">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="656e1-117">Finance and Operations apps</span></span> | <span data-ttu-id="656e1-118">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="656e1-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="656e1-119">aprašymas</span><span class="sxs-lookup"><span data-stu-id="656e1-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="656e1-120">Organizacijos hierarchijos tikslai</span><span class="sxs-lookup"><span data-stu-id="656e1-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="656e1-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="656e1-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="656e1-122">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchijos paskirtis.</span><span class="sxs-lookup"><span data-stu-id="656e1-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="656e1-123">Organizacijos hierarchijos tipas</span><span class="sxs-lookup"><span data-stu-id="656e1-123">Organization hierarchy type</span></span> | <span data-ttu-id="656e1-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="656e1-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="656e1-125">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchijos tipas.</span><span class="sxs-lookup"><span data-stu-id="656e1-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="656e1-126">Organizacijos hierarchija – publikuota</span><span class="sxs-lookup"><span data-stu-id="656e1-126">Organization hierarchy - published</span></span> | <span data-ttu-id="656e1-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="656e1-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="656e1-128">Naudojant šį šabloną, galimai vienpusiškai sinchronizuoti lentelę Organizacijos hierarchija publikuota.</span><span class="sxs-lookup"><span data-stu-id="656e1-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="656e1-129">Valdymo vienetas</span><span class="sxs-lookup"><span data-stu-id="656e1-129">Operating unit</span></span> | <span data-ttu-id="656e1-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="656e1-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="656e1-131">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="656e1-131">Legal entities</span></span> | <span data-ttu-id="656e1-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="656e1-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="656e1-133">Juridiniai subjektai</span><span class="sxs-lookup"><span data-stu-id="656e1-133">Legal entities</span></span> | <span data-ttu-id="656e1-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="656e1-134">cdm_companies</span></span> | <span data-ttu-id="656e1-135">Suteikiama juridinio subjekto (įmonės) informacijos dvikrypčio sinchronizavimo galimybė.</span><span class="sxs-lookup"><span data-stu-id="656e1-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="656e1-136">Vidinė organizacija</span><span class="sxs-lookup"><span data-stu-id="656e1-136">Internal Organization</span></span>

<span data-ttu-id="656e1-137">Vidinės organizacijos informacija, esanti „Dataverse“ gaunama iš dviejų lentelių – **valdymo vieneto** ir **juridinių subjektų**.</span><span class="sxs-lookup"><span data-stu-id="656e1-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]