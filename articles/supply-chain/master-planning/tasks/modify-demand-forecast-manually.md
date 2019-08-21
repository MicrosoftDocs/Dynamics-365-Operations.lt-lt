---
title: Modifikuoti poreikio prognozę neautomatiškai
description: Ši procedūra nurodo, kaip modifikuoti prekės prognozę.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca6b881bc094b68d1bbf8c7c20b65418e42b28e3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835880"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="ce933-103">Modifikuoti poreikio prognozę neautomatiškai</span><span class="sxs-lookup"><span data-stu-id="ce933-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce933-104">Ši procedūra nurodo, kaip modifikuoti prekės prognozę.</span><span class="sxs-lookup"><span data-stu-id="ce933-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="ce933-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="ce933-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ce933-106">Šis įrašas skirtas gamybos planuotojui.</span><span class="sxs-lookup"><span data-stu-id="ce933-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="ce933-107">Modifikuoti prekės prognozę</span><span class="sxs-lookup"><span data-stu-id="ce933-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="ce933-108">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="ce933-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ce933-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ce933-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ce933-110">Pasirinkite prekę, kurios prognozę norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="ce933-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="ce933-111">Pvz., galite pasirinkti prekę D0001.</span><span class="sxs-lookup"><span data-stu-id="ce933-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="ce933-112">Veiksmų srityje spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="ce933-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="ce933-113">Spustelėkite Poreikio prognozė.</span><span class="sxs-lookup"><span data-stu-id="ce933-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="ce933-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ce933-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ce933-115">Jei nėra prognozės eilučių, sukurkite naują eilutę .</span><span class="sxs-lookup"><span data-stu-id="ce933-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="ce933-116">programų juostoje spustelėję Nauja.</span><span class="sxs-lookup"><span data-stu-id="ce933-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="ce933-117">Lauke „Pardavimų kiekis“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ce933-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="ce933-118">Šis skaičius reprezentuoja prognozuojamą prekės kiekį.</span><span class="sxs-lookup"><span data-stu-id="ce933-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="ce933-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ce933-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="ce933-120">Modifikuoti prognozę „Excel“ programoje</span><span class="sxs-lookup"><span data-stu-id="ce933-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="ce933-121">Spustelėkite Atidaryti programoje „Microsoft Office“.</span><span class="sxs-lookup"><span data-stu-id="ce933-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="ce933-122">Spustelėkite „Redaguoti poreikio prognozę „Excel“ programoje“.</span><span class="sxs-lookup"><span data-stu-id="ce933-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="ce933-123">„Excel“ programoje galite pridėti, ištrinti ir redaguoti poreikio prognozės eilutes.</span><span class="sxs-lookup"><span data-stu-id="ce933-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="ce933-124">Jei negalite matyti duomenų „Excel“, turite prisijungti prie Microsoft Dynamics 365 for Finance and Operations redakcijos įmonei ir įjungti parinktį „Palikite mane prisijungusį", taip pat turite pasitikėti duomenų ryšio programa.</span><span class="sxs-lookup"><span data-stu-id="ce933-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

