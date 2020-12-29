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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433504"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="3f1f8-104">Išlaidų skaičiavimo lygis</span><span class="sxs-lookup"><span data-stu-id="3f1f8-104">Cost calculation level</span></span>

<span data-ttu-id="3f1f8-105">Į komplektavimo specifikacijos (KS) lygio, vadinamo **Išlaidų skaičiavimo lygiu**, skaičiavimus neįtraukti gamybos užsakymai ir paketiniai užsakymai.</span><span class="sxs-lookup"><span data-stu-id="3f1f8-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="3f1f8-106">Sistema naudoja šį lygį, kai atlieka išlaidų skaičiavimus įkainojimo versijose.</span><span class="sxs-lookup"><span data-stu-id="3f1f8-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="3f1f8-107">Tokiuose procesuose, kaip perskaičiavimas ir atsargų uždarymas, sistema naudoja KS lygį **Įkainojimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="3f1f8-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="3f1f8-108">Toliau pateiktas paprastas scenarijus parodo skirtumus tarp KS lygio **Išlaidų skaičiavimo lygis** ir KS lygio **Įkainojimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="3f1f8-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="3f1f8-109">Turite tris produktus: A, B ir C. C produktas yra B produkto komponentas, o B produktas – A produkto komponentas.</span><span class="sxs-lookup"><span data-stu-id="3f1f8-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="3f1f8-110">**Įkainojimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="3f1f8-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="3f1f8-111">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="3f1f8-111">**Product A:** 0</span></span>
    - <span data-ttu-id="3f1f8-112">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="3f1f8-112">**Product B:** 1</span></span>
    - <span data-ttu-id="3f1f8-113">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="3f1f8-113">**Product C:** 2</span></span>

- <span data-ttu-id="3f1f8-114">**Išlaidų skaičiavimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="3f1f8-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="3f1f8-115">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="3f1f8-115">**Product A:** 0</span></span>
    - <span data-ttu-id="3f1f8-116">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="3f1f8-116">**Product B:** 1</span></span>
    - <span data-ttu-id="3f1f8-117">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="3f1f8-117">**Product C:** 2</span></span>

<span data-ttu-id="3f1f8-118">Tada sukuriamas C produkto gamybos užsakymas, o A produktas įtraukiamas į gamybos užsakymo KS.</span><span class="sxs-lookup"><span data-stu-id="3f1f8-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="3f1f8-119">Įvertinus užsakymą, KS lygiai atnaujinami, kaip nurodyta toliau:</span><span class="sxs-lookup"><span data-stu-id="3f1f8-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="3f1f8-120">**Įkainojimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="3f1f8-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="3f1f8-121">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="3f1f8-121">**Product B:** 1</span></span>
    - <span data-ttu-id="3f1f8-122">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="3f1f8-122">**Product C:** 2</span></span>
    - <span data-ttu-id="3f1f8-123">**A produktas:** 3</span><span class="sxs-lookup"><span data-stu-id="3f1f8-123">**Product A:** 3</span></span>

- <span data-ttu-id="3f1f8-124">**Išlaidų skaičiavimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="3f1f8-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="3f1f8-125">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="3f1f8-125">**Product A:** 0</span></span>
    - <span data-ttu-id="3f1f8-126">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="3f1f8-126">**Product B:** 1</span></span>
    - <span data-ttu-id="3f1f8-127">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="3f1f8-127">**Product C:** 2</span></span>

<span data-ttu-id="3f1f8-128">Taip užtikrinama, kad gamybos užsakymo KS pakeitimai neturėtų įtakos būsimiems išlaidų skaičiavimams.</span><span class="sxs-lookup"><span data-stu-id="3f1f8-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
