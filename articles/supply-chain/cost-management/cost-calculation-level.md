---
title: Išlaidų skaičiavimo lygis
description: Šioje temoje aprašomas komplektavimo specifikacijų (KS) lygis, kuris pavadintas išlaidų skaičiavimo lygiu. Į šio KS lygio skaičiavimus neįtraukti gamybos ir paketiniai užsakymai.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967737"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="f7564-104">Išlaidų skaičiavimo lygis</span><span class="sxs-lookup"><span data-stu-id="f7564-104">Cost calculation level</span></span>

<span data-ttu-id="f7564-105">Į komplektavimo specifikacijos (KS) lygio, vadinamo **Išlaidų skaičiavimo lygiu**, skaičiavimus neįtraukti gamybos užsakymai ir paketiniai užsakymai.</span><span class="sxs-lookup"><span data-stu-id="f7564-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="f7564-106">Sistema naudoja šį lygį, kai atlieka išlaidų skaičiavimus įkainojimo versijose.</span><span class="sxs-lookup"><span data-stu-id="f7564-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="f7564-107">Tokiuose procesuose, kaip perskaičiavimas ir atsargų uždarymas, sistema naudoja KS lygį **Įkainojimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="f7564-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="f7564-108">Toliau pateiktas paprastas scenarijus parodo skirtumus tarp KS lygio **Išlaidų skaičiavimo lygis** ir KS lygio **Įkainojimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="f7564-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="f7564-109">Turite tris produktus: A, B ir C. C produktas yra B produkto komponentas, o B produktas – A produkto komponentas.</span><span class="sxs-lookup"><span data-stu-id="f7564-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="f7564-110">**Įkainojimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="f7564-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="f7564-111">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="f7564-111">**Product A:** 0</span></span>
    - <span data-ttu-id="f7564-112">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="f7564-112">**Product B:** 1</span></span>
    - <span data-ttu-id="f7564-113">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="f7564-113">**Product C:** 2</span></span>

- <span data-ttu-id="f7564-114">**Išlaidų skaičiavimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="f7564-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="f7564-115">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="f7564-115">**Product A:** 0</span></span>
    - <span data-ttu-id="f7564-116">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="f7564-116">**Product B:** 1</span></span>
    - <span data-ttu-id="f7564-117">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="f7564-117">**Product C:** 2</span></span>

<span data-ttu-id="f7564-118">Tada sukuriamas C produkto gamybos užsakymas, o A produktas įtraukiamas į gamybos užsakymo KS.</span><span class="sxs-lookup"><span data-stu-id="f7564-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="f7564-119">Įvertinus užsakymą, KS lygiai atnaujinami, kaip nurodyta toliau:</span><span class="sxs-lookup"><span data-stu-id="f7564-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="f7564-120">**Įkainojimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="f7564-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="f7564-121">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="f7564-121">**Product B:** 1</span></span>
    - <span data-ttu-id="f7564-122">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="f7564-122">**Product C:** 2</span></span>
    - <span data-ttu-id="f7564-123">**A produktas:** 3</span><span class="sxs-lookup"><span data-stu-id="f7564-123">**Product A:** 3</span></span>

- <span data-ttu-id="f7564-124">**Išlaidų skaičiavimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="f7564-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="f7564-125">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="f7564-125">**Product A:** 0</span></span>
    - <span data-ttu-id="f7564-126">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="f7564-126">**Product B:** 1</span></span>
    - <span data-ttu-id="f7564-127">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="f7564-127">**Product C:** 2</span></span>

<span data-ttu-id="f7564-128">Taip užtikrinama, kad gamybos užsakymo KS pakeitimai neturėtų įtakos būsimiems išlaidų skaičiavimams.</span><span class="sxs-lookup"><span data-stu-id="f7564-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
