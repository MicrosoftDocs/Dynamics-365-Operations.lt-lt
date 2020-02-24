---
title: Kurti interneto kanalą ir nurodyti kanalo atributus
description: Ši procedūra padeda kurti naują interneto kanalą ir įtraukti jį į organizacijos hierarchiją.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bac365217c20bececa1b4ff2b9de12288326dcc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023415"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="c7cf9-103">Kurti interneto kanalą ir nurodyti kanalo atributus</span><span class="sxs-lookup"><span data-stu-id="c7cf9-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c7cf9-104">Ši procedūra padeda kurti naują interneto kanalą ir įtraukti jį į organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="c7cf9-105">Prieš kurdami naują interneto kanalą, turite sukurti organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="c7cf9-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="c7cf9-107">Naujo interneto kanalo kūrimas</span><span class="sxs-lookup"><span data-stu-id="c7cf9-107">Create a new online channel</span></span>
1. <span data-ttu-id="c7cf9-108">Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Interneto parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="c7cf9-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-109">Click New.</span></span>
3. <span data-ttu-id="c7cf9-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c7cf9-111">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="c7cf9-112">Lauke Saugojimo laiko juosta pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="c7cf9-113">Lauke Numatytasis klientas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="c7cf9-114">Lauke Kliento adresų knygelė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="c7cf9-115">Lauke Mokėjimo sąlygos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="c7cf9-116">Lauke Mokėjimo metodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="c7cf9-117">Lauke El. paštu siunčiamo pranešimo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="c7cf9-118">Išplėskite sekciją Finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="c7cf9-119">Lauke „BusinessUnit“ įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="c7cf9-120">Taip pat nustatykite visų kitų numatytųjų dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="c7cf9-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="c7cf9-122">Interneto kanalo įtraukimas į organizacijos hierarchiją</span><span class="sxs-lookup"><span data-stu-id="c7cf9-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="c7cf9-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-123">Close the page.</span></span>
2. <span data-ttu-id="c7cf9-124">Pasirinkite Organizacijos administravimas > Organizacijos > Organizacijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="c7cf9-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c7cf9-126">Spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-126">Click View.</span></span>
5. <span data-ttu-id="c7cf9-127">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-127">Click Edit.</span></span>
    * <span data-ttu-id="c7cf9-128">Galite pasirinkti bet kurį hierarchijos mazgą, į kurį norite įterpti naują kanalą.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="c7cf9-129">Spustelėkite Įterpti.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-129">Click Insert.</span></span>
7. <span data-ttu-id="c7cf9-130">Spustelėkite kanalą Prekyba.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="c7cf9-131">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-131">Click OK.</span></span>
9. <span data-ttu-id="c7cf9-132">Spustelėdami Publikuoti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="c7cf9-133">Lauke Įsigaliojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="c7cf9-134">Spustelėkite Publikuoti.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="c7cf9-135">Užsakymų konfigūravimas norint nustatyti beveik realiuoju laiku teikiamus pranešimus</span><span class="sxs-lookup"><span data-stu-id="c7cf9-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="c7cf9-136">Eikite į Mažmeninė prekyba ir prekyba > Būstinės sąranka > Parametrai > Prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="c7cf9-137">Nustatykite parinkties Naudoti realiojo laiko paslaugą norint sukurti „eCommerce“ užsakymą vertę Taip.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="c7cf9-138">Naudodami 1070 paskirstymo grafiką sinchronizuokite kanalo duomenų bazės pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="c7cf9-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


