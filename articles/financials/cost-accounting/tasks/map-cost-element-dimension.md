---
title: Susieti savikainos elemento dimensiją
description: Išlaidų kontrolierius gali naudoti šią procedūrą, norėdamas susieti išlaidų elemento dimensiją su išlaidų elemento dimensija juridinio subjekto MXMF.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b9f6a5b71349d404fe9621b58f58aab843a71f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570698"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="56faa-103">Susieti savikainos elemento dimensiją</span><span class="sxs-lookup"><span data-stu-id="56faa-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56faa-104">Išlaidų kontrolierius gali naudoti šią procedūrą, norėdamas susieti išlaidų elemento dimensiją su išlaidų elemento dimensija juridinio subjekto MXMF.</span><span class="sxs-lookup"><span data-stu-id="56faa-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="56faa-105">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="56faa-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="56faa-106">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų elemento dimensijos.</span><span class="sxs-lookup"><span data-stu-id="56faa-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="56faa-107">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="56faa-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="56faa-108">Šiam pavyzdžiui pasirinkite Išlaidų elementai.</span><span class="sxs-lookup"><span data-stu-id="56faa-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="56faa-109">Spustelėkite Dimensijų susiejimai.</span><span class="sxs-lookup"><span data-stu-id="56faa-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="56faa-110">Spustelėkite Konfigūruoti susiejimus iš šios dimensijos.</span><span class="sxs-lookup"><span data-stu-id="56faa-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="56faa-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="56faa-111">Click New.</span></span>
6. <span data-ttu-id="56faa-112">Lauke Dimensijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56faa-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="56faa-113">Šiame pavyzdyje pasirinkite MXMF išlaidų elementus.</span><span class="sxs-lookup"><span data-stu-id="56faa-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="56faa-114">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="56faa-114">Click New.</span></span>
8. <span data-ttu-id="56faa-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="56faa-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="56faa-116">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56faa-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="56faa-117">Šiame pavyzdyje pasirinkite dimensijos narį 606400 telefono ir fakso išlaidos.</span><span class="sxs-lookup"><span data-stu-id="56faa-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="56faa-118">Lauke Dimensijų nariui įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="56faa-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="56faa-119">Šiame pavyzdyje pasirinkite dimensijos narį 6001004 telefonas.</span><span class="sxs-lookup"><span data-stu-id="56faa-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="56faa-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="56faa-120">Click Save.</span></span>

