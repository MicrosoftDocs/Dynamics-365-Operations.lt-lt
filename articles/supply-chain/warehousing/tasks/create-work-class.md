---
title: Kurti darbo klasę
description: Ši procedūra nurodo, kaip nustatyti darbo klasę.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed9b72d891df4d40213d4854da6b09bd9876effa
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433951"
---
# <a name="create-a-work-class"></a><span data-ttu-id="fd581-103">Kurti darbo klasę</span><span class="sxs-lookup"><span data-stu-id="fd581-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fd581-104">Ši procedūra nurodo, kaip nustatyti darbo klasę.</span><span class="sxs-lookup"><span data-stu-id="fd581-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="fd581-105">Darbo klasės naudojamos nukreipti ir (arba) apriboti darbo tipo užsakymo eilutes, kurias sandėlio darbuotojas gali apdoroti mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="fd581-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="fd581-106">Eilutės, kurias darbuotojas gali apdoroti, nustatomos pagal mobiliojo įrenginio meniu elementų darbo klases, prie kurių prieigą turi sandėlio darbuotojas, ir pagal darbo klasę, kuri nurodyta darbo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="fd581-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="fd581-107">Darbo klases taip pat galima naudoti tikrinant padėjimo vietą darbo užsakymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="fd581-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="fd581-108">Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="fd581-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="fd581-109">Ši procedūra skirta sandėlio vadovui.</span><span class="sxs-lookup"><span data-stu-id="fd581-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="fd581-110">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="fd581-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="fd581-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fd581-111">Click New.</span></span>
3. <span data-ttu-id="fd581-112">Lauke Darbo klasės ID surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fd581-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="fd581-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fd581-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fd581-114">Lauke Darbo užsakymo tipas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="fd581-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="fd581-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fd581-115">Click New.</span></span>
7. <span data-ttu-id="fd581-116">Lauke „Vietos tipas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fd581-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="fd581-117">Jei pasirinksite vietos tipą, tai apribos vietas, kur galima padėti prekes po to, kai jos bus paimtos.</span><span class="sxs-lookup"><span data-stu-id="fd581-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="fd581-118">Šis nustatymas naudojamas tuomet, kai vietos nurodymas bando rasti vietą, arba kai sandėlio darbuotojas rankiniu būdu nurodo mobiliojo įrenginio meniu elemento vietą.</span><span class="sxs-lookup"><span data-stu-id="fd581-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="fd581-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fd581-119">Close the page.</span></span>

