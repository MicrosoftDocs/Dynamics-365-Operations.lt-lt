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
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3dd941eb4e682e61c8b3d10ef0ccd14239f090c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232718"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="57717-103">Generuoti ir paleisti parengtas naudoti ataskaitas</span><span class="sxs-lookup"><span data-stu-id="57717-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57717-104">Naudokite šį užduočių vadovą, kad būstinėje neliktų įvairių darbo vietų ataskaitų bei užklausų ir pardavimų ataskaitų, esančių „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="57717-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="57717-105">Kuriant šį įrašą naudojama demonstracinių duomenų įmonė yra USRT.</span><span class="sxs-lookup"><span data-stu-id="57717-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="57717-106">Šis įrašas yra skirtas sistemos administratoriaus vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="57717-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="57717-107">Ataskaitų paleidimas iš darbo sričių</span><span class="sxs-lookup"><span data-stu-id="57717-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="57717-108">Eikite į „Retail and Commerce“ > Produktai ir kategorijos > Kategorijų ir produktų valdymas.</span><span class="sxs-lookup"><span data-stu-id="57717-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="57717-109">Spustelėdami rodyklę išplėskite arba sutraukite sekciją Ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="57717-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="57717-110">Spustelėkite Populiariausių produktų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="57717-110">Click Top products report.</span></span>
4. <span data-ttu-id="57717-111">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="57717-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="57717-112">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="57717-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="57717-113">Lauke Kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="57717-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="57717-114">Medyje pasirinkite „Contoso RetailContoso Retail USA\Central\Houston“.</span><span class="sxs-lookup"><span data-stu-id="57717-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="57717-115">Tai rodo numatytąją ataskaitų teikimo organizacijos hierarchiją, skirtą „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="57717-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="57717-116">Eikite į Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos tikslai ir pasirinkite „Commerce“ ataskaitų teikimas. Skiltyje „Priskirtos hierarchijos“ patikrinkite hierarchijos pavadinimą, kurio numatytasis stulpelis yra pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="57717-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="57717-117">Kaip demonstracinių duomenų dalis (naudojama šiai užduočiai įrašyti), „Parduotuvės pagal regioną“ yra numatytoji organizacijos hierarchija ataskaitų teikimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="57717-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="57717-118">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="57717-118">Click OK.</span></span>
9. <span data-ttu-id="57717-119">Lauke Rodinys pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="57717-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="57717-120">Lauke Pagal pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="57717-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="57717-121">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="57717-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="57717-122">Paleiskite užklausų ir pardavimų ataskaitas</span><span class="sxs-lookup"><span data-stu-id="57717-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="57717-123">Eikite į „Retail and Commerce“ > Užklausos ir ataskaitos > Pardavimų ataskaitos > Kategorijos pardavimų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="57717-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="57717-124">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="57717-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="57717-125">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="57717-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="57717-126">Lauke Kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="57717-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="57717-127">Medyje pasirinkite „Contoso RetailContoso Retail USA\West\Seattle“.</span><span class="sxs-lookup"><span data-stu-id="57717-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="57717-128">Tai rodo numatytąją ataskaitų teikimo organizacijos hierarchiją, skirtą „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="57717-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="57717-129">Eikite į Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos tikslai ir pasirinkite „Commerce“ ataskaitų teikimas. Skiltyje „Priskirtos hierarchijos“ patikrinkite hierarchijos pavadinimą, kurio numatytasis stulpelis yra pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="57717-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="57717-130">Kaip demonstracinių duomenų dalis (naudojama šiai užduočiai įrašyti), „Parduotuvės pagal regioną“ yra numatytoji organizacijos hierarchija ataskaitų teikimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="57717-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="57717-131">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="57717-131">Click OK.</span></span>
7. <span data-ttu-id="57717-132">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="57717-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="57717-133">HQ ataskaitų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="57717-133">Export an HQ reports</span></span>
1. <span data-ttu-id="57717-134">Eikite į „Retail and Commerce“ > Užklausos ir ataskaitos > Pardavimų ataskaitos > Organizacijos pardavimų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="57717-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="57717-135">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="57717-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="57717-136">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="57717-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="57717-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="57717-137">Click OK.</span></span>
5. <span data-ttu-id="57717-138">Spustelėkite Eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="57717-138">Click Export.</span></span>
6. <span data-ttu-id="57717-139">Spustelėkite PDF.</span><span class="sxs-lookup"><span data-stu-id="57717-139">Click PDF.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]