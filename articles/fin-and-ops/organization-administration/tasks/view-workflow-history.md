---
title: Darbo eigos retrospektyvos peržiūra
description: Atlikite šiuos veiksmus, jei norite peržiūrėti dokumento, pateikto darbo eigos sistemai apdoroti ir patvirtinti, būseną.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738793"
---
# <a name="view-workflow-history"></a><span data-ttu-id="cb4ed-103">Darbo eigos retrospektyvos peržiūra</span><span class="sxs-lookup"><span data-stu-id="cb4ed-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb4ed-104">Atlikite šiuos veiksmus, jei norite peržiūrėti dokumento, pateikto darbo eigos sistemai apdoroti ir patvirtinti, būseną.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="cb4ed-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="cb4ed-106">Eikite į **Naršymo sritis > Moduliai > Bendra > Užklausos > Darbo eiga > Darbo eigos istorija**.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="cb4ed-107">Naudokite šią formą, jei norite peržiūrėti dokumento, pateikto darbo eigos sistemai apdoroti ir patvirtinti, būseną.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="cb4ed-108">**Instance ID** yra vykdomas darbo eigos egzemplioriaus identifikavimo kodas arba įvykdytas dokumentas.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="cb4ed-109">**Status** yra dokumento darbo eigos būsena.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="cb4ed-110">**Workflow ID** yra vykdomas darbo eigos identifikavimo kodas arba įvykdytas dokumentas.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="cb4ed-111">**Document** yra dokumento identifikavimo kodas.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="cb4ed-112">**Document type** yra apdoroti pateikto dokumento tipas.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="cb4ed-113">**Workflow** yra vykdomas darbo eigos pavadinimas arba įvykdytas dokumentas.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="cb4ed-114">**Version** yra vykdomas darbo eigos versijos pavadinimas arba įvykdytas dokumentas.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="cb4ed-115">**Created date and time** yra pateikto dokumento data ir laikas.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="cb4ed-116">**Elapsed time** yra laikas, praėjęs po dokumento pateikimo.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="cb4ed-117">Spustelėjus mygtuką **Resume** galima tęsti pasirinkto dokumento darbo eigos procesą.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="cb4ed-118">Spustelėjus mygtuką **Recall** galima atšaukti pasirinktą dokumentą, kol jis neapdorotas.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="cb4ed-119">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="cb4ed-120">Įsitikinkite, kad dalis **Work items** yra išskleista.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="cb4ed-121">Šioje dalyje galite peržiūrėti su pasirinktu dokumentu susietus darbo elementus.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="cb4ed-122">Pavyzdžiui, gali būti baigta užduotis arba galima patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="cb4ed-123">Spustelėjus mygtuką **Reassign** iš naujo atidaromas dialogo langas, kuriame galima iš naujo priskirti darbo elementą kitam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="cb4ed-124">Įsitikinkite, kad dalis **Tracking details** yra išskleista.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="cb4ed-125">Šioje dalyje galite peržiūrėti pasirinkto dokumento darbo eigos retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="cb4ed-125">In this section you can view the workflow history of the selected document.</span></span>  

