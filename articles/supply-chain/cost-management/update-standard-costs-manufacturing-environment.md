---
title: "Standartinių gamybos aplinkos išlaidų atnaujinimas"
description: "Šiame straipsnyje patariama, kaip atnaujinti standartines išlaidas gamybos aplinkoje."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9ad13071c3e0c3a294e9d4413de160a58559640
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="537cb-103">Standartinių gamybos aplinkos išlaidų atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="537cb-103">Update standard costs in a manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="537cb-104">Šiame straipsnyje patariama, kaip atnaujinti standartines išlaidas gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="537cb-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="537cb-105">Atnaujinimai gali atspindėti naujas prekes, išlaidų kategorijas ar netiesioginių išlaidų skaičiavimo formules.</span><span class="sxs-lookup"><span data-stu-id="537cb-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="537cb-106">Jie taip pat gali atspindėti taisymus ir išlaidų pokyčius.</span><span class="sxs-lookup"><span data-stu-id="537cb-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="537cb-107">Atnaujinimo tipas lemia veiksmus, kuriuos turite atlikti norėdami atnaujinti standartines išlaidas, kaip parodyta šiuose pavyzdžiuose:</span><span class="sxs-lookup"><span data-stu-id="537cb-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="537cb-108">Įveskite numatomus nupirktų prekių standartinių išlaidų keitimus, tada atitinkama data pakeiskite prekės išlaidų įrašų būseną į **Aktyvi**.</span><span class="sxs-lookup"><span data-stu-id="537cb-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="537cb-109">Tačiau neperskaičiuokite pagamintų prekių, naudojančių nupirktas prekes, išlaidų.</span><span class="sxs-lookup"><span data-stu-id="537cb-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="537cb-110">Įveskite naujai nupirktos prekės standartines išlaidas, bet neperskaičiuokite pagamintų prekių, turinčių komplektavimo specifikacijos (KS) versiją, kurios vienas iš komponentų yra naujai nupirkta prekė, išlaidų.</span><span class="sxs-lookup"><span data-stu-id="537cb-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="537cb-111">Pataisykite ir pakeiskite nupirktos prekės išlaidas arba pakeiskite nupirktai prekei priskirtą išlaidų grupę bei apskaičiuokite visų pagamintų prekių, turinčių KS versiją, kurios vienas iš komponentų yra nupirkta prekė, išlaidas.</span><span class="sxs-lookup"><span data-stu-id="537cb-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="537cb-112">Pakeiskite išlaidų kategorijos išlaidas ir apskaičiuokite visų pagamintų prekių, turinčių maršruto versiją, kurioje yra išlaidų kategoriją naudojančios maršruto planavimo operacijos, išlaidas.</span><span class="sxs-lookup"><span data-stu-id="537cb-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="537cb-113">Pakeiskite išlaidų kategorijas, priskirtas maršruto planavimo operacijoms arba išlaidų grupei, kuri priskirta išlaidų kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="537cb-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="537cb-114">Tada apskaičiuokite visų pagamintų prekių, turinčių maršruto versiją, kurioje yra išlaidų kategoriją naudojančios maršruto planavimo operacijos, išlaidas.</span><span class="sxs-lookup"><span data-stu-id="537cb-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="537cb-115">Pakeiskite netiesioginių išlaidų skaičiavimo formulę bei apskaičiuokite visų pagamintų prekių, kurias paveikė keitimas, išlaidas.</span><span class="sxs-lookup"><span data-stu-id="537cb-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="537cb-116">Pakeiskite arba pridėkite gamybos teritoriją pagamintai prekei ir apskaičiuokite pagamintos prekės išlaidas teritorijai.</span><span class="sxs-lookup"><span data-stu-id="537cb-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="537cb-117">Apskaičiuokite, arba perskaičiuokite, pagamintos prekės išlaidas ir perskaičiuokite visų pagamintų prekių, turinčių KS versiją, kurios vienas iš komponentų yra pagaminta prekė, išlaidas.</span><span class="sxs-lookup"><span data-stu-id="537cb-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="537cb-118">Apskaičiuokite naujai pagamintos prekės išlaidas, atsižvelgdami į nurodytą, patvirtintą ir aktyvią KS ir maršruto informaciją.</span><span class="sxs-lookup"><span data-stu-id="537cb-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="537cb-119">Kiekvienu atveju reikia kruopščiai įvertinti, kaip atnaujinti standartines išlaidas.</span><span class="sxs-lookup"><span data-stu-id="537cb-119">Each case requires careful consideration about how to update standard costs.</span></span>




