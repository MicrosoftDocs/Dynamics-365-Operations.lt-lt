--- 
title: "Apdoroti ir sekti šaltinio duomenis"
description: "Visą duomenų apdorojimą vykdo užduotys."
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e476416420875ba0f2401cf251d34977ae84b8f5
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="21471-103">Apdoroti ir sekti šaltinio duomenis</span><span class="sxs-lookup"><span data-stu-id="21471-103">Process and trace source data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21471-104">Visą duomenų apdorojimą vykdo užduotys.</span><span class="sxs-lookup"><span data-stu-id="21471-104">All data processing is run by jobs.</span></span> <span data-ttu-id="21471-105">Kiekvienai užduočiai ir duomenų teikėjui sukuriamas žurnalas dokumentuoti, kad procesas buvo vykdomas, ir kad įrašai buvo apdoroti dabartinėje užduotyje.</span><span class="sxs-lookup"><span data-stu-id="21471-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="21471-106">Naudokite šią procedūrą, norėdami nustatyti duomenų šaltinį, ir tada sekite konkretaus savikainos įrašo kilmę.</span><span class="sxs-lookup"><span data-stu-id="21471-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="21471-107">Šiame įraše naudojama USP2 demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="21471-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="21471-108">Prieš atlikdami šią užduotį įsitikinkite, kad leidžiate tolesnes užduoties nuorodas: „Sukurkite savikainos apskaitos didžiąją knygą“, „Apibrėžkite savikainos kontrolės įtaisus“ ir „Valdykite duomenų šaltinį savikainos apskaitos didžiajai knygai“.</span><span class="sxs-lookup"><span data-stu-id="21471-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="21471-109">Eikite į Savikainos apskaita > Didžiosios knygos nustatymas > Savikainos apskaitos didžiosios knygos.</span><span class="sxs-lookup"><span data-stu-id="21471-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="21471-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="21471-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="21471-111">Pasirinkite savikainos apskaitos didžiąją knygą, kurią sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="21471-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="21471-112">Spustelėkite Faktinės versijos.</span><span class="sxs-lookup"><span data-stu-id="21471-112">Click Actual versions.</span></span>
4. <span data-ttu-id="21471-113">Veiksmų srityje spustelėkite Šaltinio duomenų apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="21471-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="21471-114">Spustelėkite Didžiosios knygos įrašų perkėlimo žurnalai.</span><span class="sxs-lookup"><span data-stu-id="21471-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="21471-115">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="21471-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="21471-116">Spustelėkite Žurnalo įrašai.</span><span class="sxs-lookup"><span data-stu-id="21471-116">Click Journal entries.</span></span>
8. <span data-ttu-id="21471-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="21471-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="21471-118">Spustelėkite Savikainos įrašai.</span><span class="sxs-lookup"><span data-stu-id="21471-118">Click Cost entries.</span></span>
10. <span data-ttu-id="21471-119">Spustelėkite Šaltinio įrašas.</span><span class="sxs-lookup"><span data-stu-id="21471-119">Click Source entry.</span></span>
11. <span data-ttu-id="21471-120">Veiksmų srityje spustelėkite Šaltinio duomenų apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="21471-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="21471-121">Spustelėkite Didžioji knyga.</span><span class="sxs-lookup"><span data-stu-id="21471-121">Click General ledger.</span></span>
13. <span data-ttu-id="21471-122">Lauke Finansinio kalendoriaus laikotarpis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21471-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="21471-123">Šiam pavyzdžiui pasirinkite finansinių 2017 m. 9 laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="21471-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="21471-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="21471-124">Click OK.</span></span>


