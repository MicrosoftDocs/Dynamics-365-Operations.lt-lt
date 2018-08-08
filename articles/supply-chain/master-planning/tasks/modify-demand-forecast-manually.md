--- 
title: "Modifikuoti poreikio prognozę neautomatiškai"
description: "Ši procedūra nurodo, kaip modifikuoti prekės prognozę."
author: ShylaThompson
manager: AnnBe
ms.date: 11/15/2016
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
ms.openlocfilehash: 72080dc7782320e82a3eabf7498c816495721b2d
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="b563c-103">Modifikuoti poreikio prognozę neautomatiškai</span><span class="sxs-lookup"><span data-stu-id="b563c-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b563c-104">Ši procedūra nurodo, kaip modifikuoti prekės prognozę.</span><span class="sxs-lookup"><span data-stu-id="b563c-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="b563c-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="b563c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b563c-106">Šis įrašas skirtas gamybos planuotojui.</span><span class="sxs-lookup"><span data-stu-id="b563c-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="b563c-107">Modifikuoti prekės prognozę</span><span class="sxs-lookup"><span data-stu-id="b563c-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="b563c-108">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="b563c-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b563c-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b563c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b563c-110">Pasirinkite prekę, kurios prognozę norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="b563c-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="b563c-111">Pvz., galite pasirinkti prekę D0001.</span><span class="sxs-lookup"><span data-stu-id="b563c-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="b563c-112">Veiksmų srityje spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="b563c-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="b563c-113">Spustelėkite Poreikio prognozė.</span><span class="sxs-lookup"><span data-stu-id="b563c-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="b563c-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b563c-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b563c-115">Jei nėra prognozės eilučių, sukurkite naują eilutę .</span><span class="sxs-lookup"><span data-stu-id="b563c-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="b563c-116">programų juostoje spustelėję Nauja.</span><span class="sxs-lookup"><span data-stu-id="b563c-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="b563c-117">Lauke „Pardavimų kiekis“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b563c-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="b563c-118">Šis skaičius reprezentuoja prognozuojamą prekės kiekį.</span><span class="sxs-lookup"><span data-stu-id="b563c-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="b563c-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b563c-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="b563c-120">Modifikuoti prognozę „Excel“ programoje</span><span class="sxs-lookup"><span data-stu-id="b563c-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="b563c-121">Spustelėkite „Atidaryti naudojant „Microsoft Office“.</span><span class="sxs-lookup"><span data-stu-id="b563c-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="b563c-122">Spustelėkite „Redaguoti poreikio prognozę „Excel“ programoje“.</span><span class="sxs-lookup"><span data-stu-id="b563c-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="b563c-123">„Excel“ programoje galite pridėti, ištrinti ir redaguoti poreikio prognozės eilutes.</span><span class="sxs-lookup"><span data-stu-id="b563c-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="b563c-124">Jei negalite matyti duomenų „Excel“, turite prisijungti prie „Microsoft Dynamics 365 for Finance and Operations“ ir įjungti parinktį „Likti prisijungus", taip pat turite pasitikėti duomenų ryšio programa.</span><span class="sxs-lookup"><span data-stu-id="b563c-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


