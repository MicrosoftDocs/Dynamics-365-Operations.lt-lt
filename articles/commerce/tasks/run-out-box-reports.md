---
title: Generuoti ir paleisti parengtas naudoti ataskaitas
description: Naudokite šį užduočių vadovą, kad būstinėje neliktų įvairių darbo vietų ataskaitų bei užklausų ir pardavimų ataskaitų, esančių „Commerce“.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9931a39e4ca2141ed5b43086226c7fcc7cbd7c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023393"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="71eea-103">Generuoti ir paleisti parengtas naudoti ataskaitas</span><span class="sxs-lookup"><span data-stu-id="71eea-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="71eea-104">Naudokite šį užduočių vadovą, kad būstinėje neliktų įvairių darbo vietų ataskaitų bei užklausų ir pardavimų ataskaitų, esančių „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="71eea-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="71eea-105">Kuriant šį įrašą naudojama demonstracinių duomenų įmonė yra USRT.</span><span class="sxs-lookup"><span data-stu-id="71eea-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="71eea-106">Šis įrašas yra skirtas sistemos administratoriaus vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="71eea-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="71eea-107">Ataskaitų paleidimas iš darbo sričių</span><span class="sxs-lookup"><span data-stu-id="71eea-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="71eea-108">Eikite į „Retail and Commerce“ > Produktai ir kategorijos > Kategorijų ir produktų valdymas.</span><span class="sxs-lookup"><span data-stu-id="71eea-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="71eea-109">Spustelėdami rodyklę išplėskite arba sutraukite sekciją Ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="71eea-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="71eea-110">Spustelėkite Populiariausių produktų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="71eea-110">Click Top products report.</span></span>
4. <span data-ttu-id="71eea-111">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="71eea-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="71eea-112">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="71eea-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="71eea-113">Lauke Kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="71eea-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="71eea-114">Medyje pasirinkite „Contoso RetailContoso Retail USA\Central\Houston“.</span><span class="sxs-lookup"><span data-stu-id="71eea-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="71eea-115">Tai rodo numatytąją ataskaitų teikimo organizacijos hierarchiją, skirtą „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="71eea-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="71eea-116">Eikite į Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos tikslai ir pasirinkite „Commerce“ ataskaitų teikimas. Skiltyje „Priskirtos hierarchijos“ patikrinkite hierarchijos pavadinimą, kurio numatytasis stulpelis yra pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="71eea-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="71eea-117">Kaip demonstracinių duomenų dalis (naudojama šiai užduočiai įrašyti), „Parduotuvės pagal regioną“ yra numatytoji organizacijos hierarchija ataskaitų teikimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="71eea-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="71eea-118">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="71eea-118">Click OK.</span></span>
9. <span data-ttu-id="71eea-119">Lauke Rodinys pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="71eea-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="71eea-120">Lauke Pagal pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="71eea-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="71eea-121">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="71eea-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="71eea-122">Paleiskite užklausų ir pardavimų ataskaitas</span><span class="sxs-lookup"><span data-stu-id="71eea-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="71eea-123">Eikite į „Retail and Commerce“ > Užklausos ir ataskaitos > Pardavimų ataskaitos > Kategorijos pardavimų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="71eea-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="71eea-124">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="71eea-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="71eea-125">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="71eea-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="71eea-126">Lauke Kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="71eea-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="71eea-127">Medyje pasirinkite „Contoso RetailContoso Retail USA\West\Seattle“.</span><span class="sxs-lookup"><span data-stu-id="71eea-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="71eea-128">Tai rodo numatytąją ataskaitų teikimo organizacijos hierarchiją, skirtą „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="71eea-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="71eea-129">Eikite į Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos tikslai ir pasirinkite „Commerce“ ataskaitų teikimas. Skiltyje „Priskirtos hierarchijos“ patikrinkite hierarchijos pavadinimą, kurio numatytasis stulpelis yra pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="71eea-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="71eea-130">Kaip demonstracinių duomenų dalis (naudojama šiai užduočiai įrašyti), „Parduotuvės pagal regioną“ yra numatytoji organizacijos hierarchija ataskaitų teikimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="71eea-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="71eea-131">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="71eea-131">Click OK.</span></span>
7. <span data-ttu-id="71eea-132">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="71eea-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="71eea-133">HQ ataskaitų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="71eea-133">Export an HQ reports</span></span>
1. <span data-ttu-id="71eea-134">Eikite į „Retail and Commerce“ > Užklausos ir ataskaitos > Pardavimų ataskaitos > Organizacijos pardavimų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="71eea-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="71eea-135">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="71eea-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="71eea-136">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="71eea-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="71eea-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="71eea-137">Click OK.</span></span>
5. <span data-ttu-id="71eea-138">Spustelėkite Eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="71eea-138">Click Export.</span></span>
6. <span data-ttu-id="71eea-139">Spustelėkite PDF.</span><span class="sxs-lookup"><span data-stu-id="71eea-139">Click PDF.</span></span>

