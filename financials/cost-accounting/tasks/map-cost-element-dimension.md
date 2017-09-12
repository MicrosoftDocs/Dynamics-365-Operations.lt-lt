--- 
title: "Susieti savikainos elemento dimensiją"
description: "Išlaidų kontrolierius gali naudoti šią procedūrą, norėdamas susieti išlaidų elemento dimensiją su išlaidų elemento dimensija juridinio subjekto MXMF."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3ff31db3dbb6da9570bb85bbcaa3b444852d91d7
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="df33a-103">Susieti savikainos elemento dimensiją</span><span class="sxs-lookup"><span data-stu-id="df33a-103">Map a cost element dimension</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df33a-104">Išlaidų kontrolierius gali naudoti šią procedūrą, norėdamas susieti išlaidų elemento dimensiją su išlaidų elemento dimensija juridinio subjekto MXMF.</span><span class="sxs-lookup"><span data-stu-id="df33a-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="df33a-105">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="df33a-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="df33a-106">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų elemento dimensijos.</span><span class="sxs-lookup"><span data-stu-id="df33a-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="df33a-107">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="df33a-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="df33a-108">Šiam pavyzdžiui pasirinkite Išlaidų elementai.</span><span class="sxs-lookup"><span data-stu-id="df33a-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="df33a-109">Spustelėkite Dimensijų susiejimai.</span><span class="sxs-lookup"><span data-stu-id="df33a-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="df33a-110">Spustelėkite Konfigūruoti susiejimus iš šios dimensijos.</span><span class="sxs-lookup"><span data-stu-id="df33a-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="df33a-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="df33a-111">Click New.</span></span>
6. <span data-ttu-id="df33a-112">Lauke Dimensijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df33a-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="df33a-113">Šiame pavyzdyje pasirinkite MXMF išlaidų elementus.</span><span class="sxs-lookup"><span data-stu-id="df33a-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="df33a-114">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="df33a-114">Click New.</span></span>
8. <span data-ttu-id="df33a-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="df33a-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="df33a-116">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df33a-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="df33a-117">Šiame pavyzdyje pasirinkite dimensijos narį 606400 telefono ir fakso išlaidos.</span><span class="sxs-lookup"><span data-stu-id="df33a-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="df33a-118">Lauke Dimensijų nariui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="df33a-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="df33a-119">Šiame pavyzdyje pasirinkite dimensijos narį 6001004 telefonas.</span><span class="sxs-lookup"><span data-stu-id="df33a-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="df33a-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="df33a-120">Click Save.</span></span>


