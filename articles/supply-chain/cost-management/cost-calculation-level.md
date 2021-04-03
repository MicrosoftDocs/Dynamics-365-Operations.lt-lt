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
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251031"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="b46d1-104">Išlaidų skaičiavimo lygis</span><span class="sxs-lookup"><span data-stu-id="b46d1-104">Cost calculation level</span></span>

<span data-ttu-id="b46d1-105">Į komplektavimo specifikacijos (KS) lygio, vadinamo **Išlaidų skaičiavimo lygiu**, skaičiavimus neįtraukti gamybos užsakymai ir paketiniai užsakymai.</span><span class="sxs-lookup"><span data-stu-id="b46d1-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="b46d1-106">Sistema naudoja šį lygį, kai atlieka išlaidų skaičiavimus įkainojimo versijose.</span><span class="sxs-lookup"><span data-stu-id="b46d1-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="b46d1-107">Tokiuose procesuose, kaip perskaičiavimas ir atsargų uždarymas, sistema naudoja KS lygį **Įkainojimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="b46d1-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="b46d1-108">Toliau pateiktas paprastas scenarijus parodo skirtumus tarp KS lygio **Išlaidų skaičiavimo lygis** ir KS lygio **Įkainojimo lygis**.</span><span class="sxs-lookup"><span data-stu-id="b46d1-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="b46d1-109">Turite tris produktus: A, B ir C. C produktas yra B produkto komponentas, o B produktas – A produkto komponentas.</span><span class="sxs-lookup"><span data-stu-id="b46d1-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="b46d1-110">**Įkainojimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="b46d1-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="b46d1-111">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="b46d1-111">**Product A:** 0</span></span>
    - <span data-ttu-id="b46d1-112">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="b46d1-112">**Product B:** 1</span></span>
    - <span data-ttu-id="b46d1-113">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="b46d1-113">**Product C:** 2</span></span>

- <span data-ttu-id="b46d1-114">**Išlaidų skaičiavimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="b46d1-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="b46d1-115">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="b46d1-115">**Product A:** 0</span></span>
    - <span data-ttu-id="b46d1-116">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="b46d1-116">**Product B:** 1</span></span>
    - <span data-ttu-id="b46d1-117">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="b46d1-117">**Product C:** 2</span></span>

<span data-ttu-id="b46d1-118">Tada sukuriamas C produkto gamybos užsakymas, o A produktas įtraukiamas į gamybos užsakymo KS.</span><span class="sxs-lookup"><span data-stu-id="b46d1-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="b46d1-119">Įvertinus užsakymą, KS lygiai atnaujinami, kaip nurodyta toliau:</span><span class="sxs-lookup"><span data-stu-id="b46d1-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="b46d1-120">**Įkainojimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="b46d1-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="b46d1-121">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="b46d1-121">**Product B:** 1</span></span>
    - <span data-ttu-id="b46d1-122">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="b46d1-122">**Product C:** 2</span></span>
    - <span data-ttu-id="b46d1-123">**A produktas:** 3</span><span class="sxs-lookup"><span data-stu-id="b46d1-123">**Product A:** 3</span></span>

- <span data-ttu-id="b46d1-124">**Išlaidų skaičiavimo lygis** priskiria šiuos KS lygius:</span><span class="sxs-lookup"><span data-stu-id="b46d1-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="b46d1-125">**A produktas:** 0</span><span class="sxs-lookup"><span data-stu-id="b46d1-125">**Product A:** 0</span></span>
    - <span data-ttu-id="b46d1-126">**B produktas:** 1</span><span class="sxs-lookup"><span data-stu-id="b46d1-126">**Product B:** 1</span></span>
    - <span data-ttu-id="b46d1-127">**C produktas:** 2</span><span class="sxs-lookup"><span data-stu-id="b46d1-127">**Product C:** 2</span></span>

<span data-ttu-id="b46d1-128">Taip užtikrinama, kad gamybos užsakymo KS pakeitimai neturėtų įtakos būsimiems išlaidų skaičiavimams.</span><span class="sxs-lookup"><span data-stu-id="b46d1-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]