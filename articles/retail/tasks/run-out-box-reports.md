---
title: Generuoti ir paleisti parengtas naudoti ataskaitas
description: Naudokite šį užduočių vadovą, norėdami vykdyti parengtas naudoti ataskaitas pagrindinėje būstinėje iš skirtingų darbo sričių ir vykdyti užklausų bei pardavimo ataskaitas, esančias „Retail & Commerce“.
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
ms.openlocfilehash: afd4509bc9bdff345e48a590a12cc84ae25aebb8
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018441"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="665bd-103">Generuoti ir paleisti parengtas naudoti ataskaitas</span><span class="sxs-lookup"><span data-stu-id="665bd-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="665bd-104">Naudokite šį užduočių vadovą, norėdami vykdyti parengtas naudoti ataskaitas pagrindinėje būstinėje iš skirtingų darbo sričių ir vykdyti užklausų bei pardavimo ataskaitas, esančias „Retail & Commerce“.</span><span class="sxs-lookup"><span data-stu-id="665bd-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="665bd-105">Kuriant šį įrašą naudojama demonstracinių duomenų įmonė yra USRT.</span><span class="sxs-lookup"><span data-stu-id="665bd-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="665bd-106">Šis įrašas yra skirtas sistemos administratoriaus vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="665bd-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="665bd-107">Ataskaitų paleidimas iš darbo sričių</span><span class="sxs-lookup"><span data-stu-id="665bd-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="665bd-108">Pasirinkite Mažmeninė prekyba ir prekyba > Produktai ir kategorijos > Kategorijų ir produktų valdymas.</span><span class="sxs-lookup"><span data-stu-id="665bd-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="665bd-109">Spustelėdami rodyklę išplėskite arba sutraukite sekciją Ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="665bd-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="665bd-110">Spustelėkite Populiariausių produktų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="665bd-110">Click Top products report.</span></span>
4. <span data-ttu-id="665bd-111">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="665bd-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="665bd-112">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="665bd-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="665bd-113">Lauke Kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="665bd-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="665bd-114">Medyje pasirinkite „Contoso RetailContoso Retail USA\Central\Houston“.</span><span class="sxs-lookup"><span data-stu-id="665bd-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="665bd-115">Čia rodoma numatytąją mažmeninės prekybos organizacijos hierarchija (mažmeninės prekybos ataskaitų teikimo tikslais).</span><span class="sxs-lookup"><span data-stu-id="665bd-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="665bd-116">Eikite į Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos tikslai ir pasirinkite Mažmeninės prekybos ataskaitų teikimas ir po dalimi Priskirtos hierarchijos patikrinkite hierarchijos, kurios stulpelis Numatytasis tikrinamas, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="665bd-116">Go to Organization administration >  Organizations > Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="665bd-117">Peržiūrėdami demonstracinius duomenis (naudojamus šiame užduoties įraše) pastebėsite, kad parinktis Mažmeninės prekybos parduotuvės pagal regioną yra numatytoji organizacijos hierarchija mažmeninės prekybos ataskaitų tikslais.</span><span class="sxs-lookup"><span data-stu-id="665bd-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="665bd-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="665bd-118">Click OK.</span></span>
9. <span data-ttu-id="665bd-119">Lauke Rodinys pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="665bd-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="665bd-120">Lauke Pagal pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="665bd-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="665bd-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="665bd-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="665bd-122">Paleiskite ataskaitas iš užklausų ir pardavimo ataskaitų, esančių po programos „Retail & Commerce“ saitu.</span><span class="sxs-lookup"><span data-stu-id="665bd-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="665bd-123">Pasirinkite Mažmeninė prekyba ir prekyba > Užklausos ir ataskaitos > Pardavimo ataskaitos > Kategorijos pardavimo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="665bd-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="665bd-124">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="665bd-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="665bd-125">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="665bd-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="665bd-126">Lauke Kanalas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="665bd-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="665bd-127">Medyje pasirinkite „Contoso RetailContoso Retail USA\West\Seattle“.</span><span class="sxs-lookup"><span data-stu-id="665bd-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="665bd-128">Čia rodoma numatytąją mažmeninės prekybos organizacijos hierarchija (mažmeninės prekybos ataskaitų teikimo tikslais).</span><span class="sxs-lookup"><span data-stu-id="665bd-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="665bd-129">Eikite į Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos tikslai ir pasirinkite Mažmeninės prekybos ataskaitų teikimas ir po dalimi Priskirtos hierarchijos patikrinkite hierarchijos, kurios stulpelis Numatytasis tikrinamas, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="665bd-129">Go to Organization administration  > Organizations > Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="665bd-130">Peržiūrėdami demonstracinius duomenis (naudojamus šiame užduoties įraše) pastebėsite, kad parinktis Mažmeninės prekybos parduotuvės pagal regioną yra numatytoji organizacijos hierarchija mažmeninės prekybos ataskaitų tikslais.</span><span class="sxs-lookup"><span data-stu-id="665bd-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="665bd-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="665bd-131">Click OK.</span></span>
7. <span data-ttu-id="665bd-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="665bd-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="665bd-133">HQ ataskaitų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="665bd-133">Export an HQ reports</span></span>
1. <span data-ttu-id="665bd-134">Pasirinkite Mažmeninė prekyba ir prekyba > Užklausos ir ataskaitos > Pardavimo ataskaitos > Organizacijos pardavimo ataskaita.</span><span class="sxs-lookup"><span data-stu-id="665bd-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="665bd-135">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="665bd-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="665bd-136">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="665bd-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="665bd-137">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="665bd-137">Click OK.</span></span>
5. <span data-ttu-id="665bd-138">Spustelėkite Eksportuoti.</span><span class="sxs-lookup"><span data-stu-id="665bd-138">Click Export.</span></span>
6. <span data-ttu-id="665bd-139">Spustelėkite PDF.</span><span class="sxs-lookup"><span data-stu-id="665bd-139">Click PDF.</span></span>

