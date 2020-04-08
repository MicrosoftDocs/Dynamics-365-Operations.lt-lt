---
title: Nustatyti tranzito punktų papildomų paslaugų išlaidas ir papildomų paslaugų šablonus
description: Ši procedūra nurodo, kaip sukurti tranzito punkto papildomų paslaugų šabloną ir jį panaudoti tranzito punkto papildomų paslaugų mokesčiui sukurti.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 1ea59326a85d97d53795104f80486f2fac24148a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148531"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="a2522-103">Nustatyti tranzito punktų papildomų paslaugų išlaidas ir papildomų paslaugų šablonus</span><span class="sxs-lookup"><span data-stu-id="a2522-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2522-104">Ši procedūra nurodo, kaip sukurti tranzito punkto papildomų paslaugų šabloną ir jį panaudoti tranzito punkto papildomų paslaugų mokesčiui sukurti.</span><span class="sxs-lookup"><span data-stu-id="a2522-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="a2522-105">Procedūra naudoja USMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="a2522-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="a2522-106">Šį nustatymą paprastai atlieka transportavimo koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="a2522-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="a2522-107">Pagrindinio tranzito punkto nustatymas</span><span class="sxs-lookup"><span data-stu-id="a2522-107">Set up a hub master</span></span>
1. <span data-ttu-id="a2522-108">Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Papildomų paslaugų šablonai.</span><span class="sxs-lookup"><span data-stu-id="a2522-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="a2522-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a2522-109">Click New.</span></span>
3. <span data-ttu-id="a2522-110">Lauke „Papildomų paslaugų šablonas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a2522-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="a2522-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a2522-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a2522-112">Lauke „Papildomų paslaugų tipas“ pasirinkite „Tranzito punktas“.</span><span class="sxs-lookup"><span data-stu-id="a2522-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="a2522-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a2522-113">Click Save.</span></span>
7. <span data-ttu-id="a2522-114">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a2522-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="a2522-115">Nustatyti tranzito punkto papildomų paslaugų mokestį</span><span class="sxs-lookup"><span data-stu-id="a2522-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="a2522-116">Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Tranzito punkto papildomų paslaugų mokesčiai.</span><span class="sxs-lookup"><span data-stu-id="a2522-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="a2522-117">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a2522-117">Click New.</span></span>
3. <span data-ttu-id="a2522-118">Lauke „Tranzito punkto papildomų paslaugų ID“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a2522-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="a2522-119">Lauke „Tranzito punktas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a2522-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a2522-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a2522-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="a2522-121">Lauke „Tranzito punkto padėtis“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a2522-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="a2522-122">Galite sukurti mokestį už paėmimą arba atidavimą.</span><span class="sxs-lookup"><span data-stu-id="a2522-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="a2522-123">Atsižvelgiant į jūsų pasirinkimą, mokestis bus taikomas atitinkamam transportavimo segmentui jūsų maršrute.</span><span class="sxs-lookup"><span data-stu-id="a2522-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="a2522-124">Lauke „Papildomų paslaugų šablonas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a2522-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a2522-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a2522-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a2522-126">Pasirinkite šabloną, kurį ką tik sukurėte.</span><span class="sxs-lookup"><span data-stu-id="a2522-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="a2522-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a2522-127">Click Save.</span></span>
10. <span data-ttu-id="a2522-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a2522-128">Close the page.</span></span>

