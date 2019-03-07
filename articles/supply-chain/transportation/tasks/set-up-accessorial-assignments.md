---
title: Nustatyti papildomų paslaugų priskyrimus
description: Ši procedūra nurodo, kaip nustatyti papildomų paslaugų priskyrimą.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b69bd2029914efd31569c57272339e27ef1bd6a3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "356627"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="76bb8-103">Nustatyti papildomų paslaugų priskyrimus</span><span class="sxs-lookup"><span data-stu-id="76bb8-103">Set up accessorial assignments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76bb8-104">Ši procedūra nurodo, kaip nustatyti papildomų paslaugų priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="76bb8-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="76bb8-105">Paprastai tą daro transportavimo koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="76bb8-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="76bb8-106">Prieš pradėdami naudoti šį vadovą turite įvykdyti vadovą „Nustatyti tranzito punktų papildomų paslaugų mokesčius ir papildomų paslaugų šablonus“.</span><span class="sxs-lookup"><span data-stu-id="76bb8-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="76bb8-107">Nustatyti papildomų paslaugų priskyrimą</span><span class="sxs-lookup"><span data-stu-id="76bb8-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="76bb8-108">Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Papildomų paslaugų priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="76bb8-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="76bb8-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="76bb8-109">Click New.</span></span>
3. <span data-ttu-id="76bb8-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76bb8-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="76bb8-111">Perjunkite skyriaus „Išsami informacija“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="76bb8-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="76bb8-112">Lauke „Tranzito punktas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="76bb8-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="76bb8-113">Sąraše pasirinkite tranzito punktą, kuriam sukūrėte papildomų paslaugų šabloną, kai paleidote vadovą „Nustatyti tranzito punktų papildomų paslaugų mokesčius ir papildomų paslaugų šablonus“.</span><span class="sxs-lookup"><span data-stu-id="76bb8-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="76bb8-114">Lauke „Tranzito punkto papildomų paslaugų ID“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="76bb8-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="76bb8-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="76bb8-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="76bb8-116">Perjunkite skyriaus „Kriterijai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="76bb8-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="76bb8-117">Skyriuje „Kriterijai“ galite pasirinkti tikslius kriterijus, kada turi būti taikomas mokestis, remiantis skirtingomis čia siūlomomis reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="76bb8-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="76bb8-118">Parinkčiai „Taikyti visada“ nustatykite reikšmę „Taip“.</span><span class="sxs-lookup"><span data-stu-id="76bb8-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="76bb8-119">Lauke „Papildomų paslaugų priskyrimo lygis“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="76bb8-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="76bb8-120">Perjunkite skyriaus „Skaičiavimas“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="76bb8-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="76bb8-121">Lauke „Mokesčio už papildomas paslaugas tipas“ pasirinkite „Fiksuotas“.</span><span class="sxs-lookup"><span data-stu-id="76bb8-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="76bb8-122">Mokesčio už papildomas paslaugas tipas nulemia, kaip skaičiuojamas faktinis mokestis.</span><span class="sxs-lookup"><span data-stu-id="76bb8-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="76bb8-123">Šiame pavyzdyje tai mokestis fiksuotas.</span><span class="sxs-lookup"><span data-stu-id="76bb8-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="76bb8-124">Lauke „Mokestis už papildomas paslaugas“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="76bb8-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="76bb8-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="76bb8-125">Click Save.</span></span>

