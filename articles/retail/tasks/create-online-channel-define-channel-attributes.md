--- 
title: "Kurti interneto kanalą ir nurodyti kanalo atributus"
description: "Ši procedūra padeda kurti naują interneto kanalą ir įtraukti jį į organizacijos hierarchiją."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="071a0-103">Kurti interneto kanalą ir nurodyti kanalo atributus</span><span class="sxs-lookup"><span data-stu-id="071a0-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="071a0-104">Ši procedūra padeda kurti naują interneto kanalą ir įtraukti jį į organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="071a0-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="071a0-105">Prieš kurdami naują interneto kanalą, turite sukurti organizacijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="071a0-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="071a0-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="071a0-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="071a0-107">Naujo interneto kanalo kūrimas</span><span class="sxs-lookup"><span data-stu-id="071a0-107">Create a new online channel</span></span>
1. <span data-ttu-id="071a0-108">Pasirinkite Mažmeninė prekyba ir prekyba > Kanalai > Interneto parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="071a0-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="071a0-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="071a0-109">Click New.</span></span>
3. <span data-ttu-id="071a0-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="071a0-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="071a0-111">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="071a0-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="071a0-112">Lauke Saugojimo laiko juosta pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="071a0-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="071a0-113">Lauke Numatytasis klientas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="071a0-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="071a0-114">Lauke Kliento adresų knygelė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="071a0-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="071a0-115">Lauke Mokėjimo sąlygos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="071a0-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="071a0-116">Lauke Mokėjimo metodas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="071a0-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="071a0-117">Lauke El. paštu siunčiamo pranešimo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="071a0-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="071a0-118">Išplėskite sekciją Finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="071a0-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="071a0-119">Lauke „BusinessUnit“ įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="071a0-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="071a0-120">Taip pat nustatykite visų kitų numatytųjų dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="071a0-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="071a0-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="071a0-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="071a0-122">Interneto kanalo įtraukimas į organizacijos hierarchiją</span><span class="sxs-lookup"><span data-stu-id="071a0-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="071a0-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="071a0-123">Close the page.</span></span>
2. <span data-ttu-id="071a0-124">Pasirinkite Organizacijos administravimas > Organizacijos > Organizacijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="071a0-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="071a0-125">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="071a0-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="071a0-126">Spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="071a0-126">Click View.</span></span>
5. <span data-ttu-id="071a0-127">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="071a0-127">Click Edit.</span></span>
    * <span data-ttu-id="071a0-128">Galite pasirinkti bet kurį hierarchijos mazgą, į kurį norite įterpti naują kanalą.</span><span class="sxs-lookup"><span data-stu-id="071a0-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="071a0-129">Spustelėkite Įterpti.</span><span class="sxs-lookup"><span data-stu-id="071a0-129">Click Insert.</span></span>
7. <span data-ttu-id="071a0-130">Spustelėkite Mažmeninės prekybos kanalas.</span><span class="sxs-lookup"><span data-stu-id="071a0-130">Click Retail channel.</span></span>
8. <span data-ttu-id="071a0-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="071a0-131">Click OK.</span></span>
9. <span data-ttu-id="071a0-132">Spustelėdami Publikuoti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="071a0-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="071a0-133">Lauke Įsigaliojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="071a0-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="071a0-134">Spustelėkite Publikuoti.</span><span class="sxs-lookup"><span data-stu-id="071a0-134">Click Publish.</span></span>


