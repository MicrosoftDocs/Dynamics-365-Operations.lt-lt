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
ms.openlocfilehash: 0d148fa36a116860af8c44043d90759b8a2d76fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140766"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="00745-103">Generuoti ir paleisti parengtas naudoti ataskaitas</span><span class="sxs-lookup"><span data-stu-id="00745-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00745-104">Naudokite šį užduočių vadovą, kad būstinėje neliktų įvairių darbo vietų ataskaitų bei užklausų ir pardavimų ataskaitų, esančių „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="00745-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="00745-105">Kuriant šį įrašą naudojama demonstracinių duomenų įmonė yra USRT.</span><span class="sxs-lookup"><span data-stu-id="00745-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="00745-106">Šis įrašas yra skirtas sistemos administratoriaus vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="00745-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="00745-107">Ataskaitų paleidimas iš darbo sričių</span><span class="sxs-lookup"><span data-stu-id="00745-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="00745-108">Eikite į „Retail and Commerce“ > Produktai ir kategorijos > Kategorijų ir produktų valdymas.</span><span class="sxs-lookup"><span data-stu-id="00745-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="00745-109">Spustelėdami rodyklę išplėskite arba sutraukite sekciją Ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="00745-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="00745-110">Spustelėkite Populiariausių produktų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="00745-110">Click Top products report.</span></span>
4. <span data-ttu-id="00745-111">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="00745-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="00745-112">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="00745-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="00745-113">Lauke Kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="00745-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="00745-114">Medyje pasirinkite „Contoso RetailContoso Retail USA\Central\Houston“.</span><span class="sxs-lookup"><span data-stu-id="00745-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="00745-115">Tai rodo numatytąją ataskaitų teikimo organizacijos hierarchiją, skirtą „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="00745-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="00745-116">Eikite į Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos tikslai ir pasirinkite „Commerce“ ataskaitų teikimas. Skiltyje „Priskirtos hierarchijos“ patikrinkite hierarchijos pavadinimą, kurio numatytasis stulpelis yra pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="00745-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="00745-117">Kaip demonstracinių duomenų dalis (naudojama šiai užduočiai įrašyti), „Parduotuvės pagal regioną“ yra numatytoji organizacijos hierarchija ataskaitų teikimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="00745-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="00745-118">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="00745-118">Click OK.</span></span>
9. <span data-ttu-id="00745-119">Lauke Rodinys pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="00745-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="00745-120">Lauke Pagal pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="00745-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="00745-121">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="00745-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="00745-122">Paleiskite užklausų ir pardavimų ataskaitas</span><span class="sxs-lookup"><span data-stu-id="00745-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="00745-123">Eikite į „Retail and Commerce“ > Užklausos ir ataskaitos > Pardavimų ataskaitos > Kategorijos pardavimų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="00745-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="00745-124">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="00745-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="00745-125">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="00745-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="00745-126">Lauke Kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="00745-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="00745-127">Medyje pasirinkite „Contoso RetailContoso Retail USA\West\Seattle“.</span><span class="sxs-lookup"><span data-stu-id="00745-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="00745-128">Tai rodo numatytąją ataskaitų teikimo organizacijos hierarchiją, skirtą „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="00745-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="00745-129">Eikite į Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos tikslai ir pasirinkite „Commerce“ ataskaitų teikimas. Skiltyje „Priskirtos hierarchijos“ patikrinkite hierarchijos pavadinimą, kurio numatytasis stulpelis yra pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="00745-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="00745-130">Kaip demonstracinių duomenų dalis (naudojama šiai užduočiai įrašyti), „Parduotuvės pagal regioną“ yra numatytoji organizacijos hierarchija ataskaitų teikimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="00745-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="00745-131">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="00745-131">Click OK.</span></span>
7. <span data-ttu-id="00745-132">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="00745-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="00745-133">HQ ataskaitų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="00745-133">Export an HQ reports</span></span>
1. <span data-ttu-id="00745-134">Eikite į „Retail and Commerce“ > Užklausos ir ataskaitos > Pardavimų ataskaitos > Organizacijos pardavimų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="00745-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="00745-135">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="00745-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="00745-136">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="00745-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="00745-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="00745-137">Click OK.</span></span>
5. <span data-ttu-id="00745-138">Spustelėkite Eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="00745-138">Click Export.</span></span>
6. <span data-ttu-id="00745-139">Spustelėkite PDF.</span><span class="sxs-lookup"><span data-stu-id="00745-139">Click PDF.</span></span>

