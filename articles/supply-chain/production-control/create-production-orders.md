---
title: "Kurti gamybos užsakymus"
description: "Kai gamybos užsakymas sukurtas, inicijuojamas prašymas pradėti gaminti prekę. Gamybos užsakyme yra informacijos apie tai, kas bus gaminama, norimas gaminti kiekis ir kokia yra numatyta baigimo data. Taip pat pateikiama informacija apie tai, kurios medžiagos naudojamos ir kurio proceso laikytis gaminant prekę."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 58213d4d6e8c29ab6605eb7aa5c6cb9ca6ba4a10
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="create-production-orders"></a><span data-ttu-id="ae25d-105">Kurti gamybos užsakymus</span><span class="sxs-lookup"><span data-stu-id="ae25d-105">Create production orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ae25d-106">Kai gamybos užsakymas sukurtas, inicijuojamas prašymas pradėti gaminti prekę.</span><span class="sxs-lookup"><span data-stu-id="ae25d-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="ae25d-107">Gamybos užsakyme yra informacijos apie tai, kas bus gaminama, norimas gaminti kiekis ir kokia yra numatyta baigimo data.</span><span class="sxs-lookup"><span data-stu-id="ae25d-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="ae25d-108">Taip pat pateikiama informacija apie tai, kurios medžiagos naudojamos ir kurio proceso laikytis gaminant prekę.</span><span class="sxs-lookup"><span data-stu-id="ae25d-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="ae25d-109">Gamybos užsakymas pereina gamybos ciklo etapus.</span><span class="sxs-lookup"><span data-stu-id="ae25d-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="ae25d-110">Kai užsakymas sukurtas, jam priskiriama būsena **Sukurtas**.</span><span class="sxs-lookup"><span data-stu-id="ae25d-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="ae25d-111">Kai užsakymas baigtas, jam priskiriama būsena **Baigtas**.</span><span class="sxs-lookup"><span data-stu-id="ae25d-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="ae25d-112">Parametro nuostata kiekviename etape leidžia naudotojui konfigūruoti kiekvieną veiksmą.</span><span class="sxs-lookup"><span data-stu-id="ae25d-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="ae25d-113">Nuostatą galima nustatyti vienam naudotojui arba visiems naudotojams.</span><span class="sxs-lookup"><span data-stu-id="ae25d-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="ae25d-114">Gamybos komplektavimo specifikacija ir gamybos maršrutas yra pagrindiniai gamybos užsakymo objektai.</span><span class="sxs-lookup"><span data-stu-id="ae25d-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="ae25d-115">Jie į gamybos užsakymą kopijuojami pagal pasirinktą prekę ir kiekį, kurį ketinama gaminti.</span><span class="sxs-lookup"><span data-stu-id="ae25d-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="ae25d-116">Prieš pradedant gamybos užsakymą, galima redaguoti gamybos komplektavimo specifikaciją ir maršrutą.</span><span class="sxs-lookup"><span data-stu-id="ae25d-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="ae25d-117">Gamybos užsakymą galima kurti pagal toliau pateiktus scenarijus.</span><span class="sxs-lookup"><span data-stu-id="ae25d-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="ae25d-118">Sukurtas vykdant bendrąjį planavimą pagal medžiagų poreikį.</span><span class="sxs-lookup"><span data-stu-id="ae25d-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="ae25d-119">Sukurtas tiesiai iš pardavimo užsakymo eilutės arba sukūrus ir įvertinus aukštesnio lygio gamybos užsakymą (iškviestas tiekimas).</span><span class="sxs-lookup"><span data-stu-id="ae25d-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="ae25d-120">Sukurtas rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="ae25d-120">Created manually.</span></span>




