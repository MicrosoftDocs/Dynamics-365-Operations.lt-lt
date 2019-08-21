---
title: Suplanuoti gamybos užsakymą
description: Šioje procedūroje nurodoma, kaip planuoti gamybos užsakymą.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6fa2ea9d38c4f4d00f742ccfbf714c237f0ce4d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843462"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="71449-103">Suplanuoti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="71449-103">Schedule a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71449-104">Šioje procedūroje nurodoma, kaip planuoti gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="71449-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="71449-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="71449-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="71449-106">Tai yra trečioji procedūra iš septynių, kurioje paaiškinamas gamybos užsakymo ciklas.</span><span class="sxs-lookup"><span data-stu-id="71449-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="71449-107">Suplanuoti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="71449-107">Schedule a production order</span></span>
1. <span data-ttu-id="71449-108">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="71449-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="71449-109">Pasirinkite gamybos užsakymą, kurio būsena yra Įvertintas.</span><span class="sxs-lookup"><span data-stu-id="71449-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="71449-110">Veiksmų srityje spustelėkite Grafikas.</span><span class="sxs-lookup"><span data-stu-id="71449-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="71449-111">Spustelėkite Planuoti užduotis.</span><span class="sxs-lookup"><span data-stu-id="71449-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="71449-112">Šiame puslapyje nustatomi planavimo parametrai.</span><span class="sxs-lookup"><span data-stu-id="71449-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="71449-113">Galite nustatyti konkrečių arba visų vartotojų parametrus.</span><span class="sxs-lookup"><span data-stu-id="71449-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="71449-114">Lauke Planavimo kryptis pasirinkite „Pirmyn nuo šiandien‟.</span><span class="sxs-lookup"><span data-stu-id="71449-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="71449-115">Lauke Planavimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="71449-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="71449-116">Pažymėkite arba panaikinkite žymės langelio Ribotas pajėgumas žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="71449-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="71449-117">Pažymėkite arba panaikinkite žymės langelio Ribotas medžiagos žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="71449-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="71449-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="71449-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="71449-119">Peržiūrėti planavimo rezultatus</span><span class="sxs-lookup"><span data-stu-id="71449-119">View the scheduling results</span></span>
1. <span data-ttu-id="71449-120">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="71449-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="71449-121">Spustelėkite Visos užduotys.</span><span class="sxs-lookup"><span data-stu-id="71449-121">Click All jobs.</span></span>
    * <span data-ttu-id="71449-122">Šiame puslapyje rodomos suplanuotos užduotys, kurias ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="71449-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="71449-123">Išplėskite arba sutraukite sekciją Planavimas.</span><span class="sxs-lookup"><span data-stu-id="71449-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="71449-124">„Fasttab“ Planavimas galite peržiūrėti suplanuotus datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="71449-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="71449-125">Spustelėkite Užklausos.</span><span class="sxs-lookup"><span data-stu-id="71449-125">Click Inquiries.</span></span>
5. <span data-ttu-id="71449-126">Spustelėkite Pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="71449-126">Click Capacity load.</span></span>
    * <span data-ttu-id="71449-127">Puslapyje Pajėgumas rodomi užduočių planavimo metu rezervuotas pajėgumas, bendras šiuo metu rezervuotų ištekliaus valandų skaičius ir likusių ištekliaus valandų, kurias galima vykdyti užduočių planavimą, skaičius.</span><span class="sxs-lookup"><span data-stu-id="71449-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="71449-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="71449-128">Close the page.</span></span>
7. <span data-ttu-id="71449-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="71449-129">Close the page.</span></span>

