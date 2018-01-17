---
title: "Vienetų paėmimo patvirtinimas"
description: "Šioje temoje aprašoma, kaip nustatyti ir taikyti vienetų paėmimo patvirtinimą iš mobiliojo įrenginio."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b1868851d22f41d3278cd9574a48bdf062185012
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="piece-picking-confirmation"></a><span data-ttu-id="b3fce-103">Vienetų paėmimo patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="b3fce-103">Piece picking confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b3fce-104">Vienetų paėmimas suteikia galimybę patvirtinti kiekvieną atsargų vienetą naudojant paėmimo ir skaičiavimo darbą mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="b3fce-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="b3fce-105">Paėmimų atveju galite patvirtinti darbo kiekį, kuris bus atliktas neviršijant kiekio, nurodyto paimtinam darbui.</span><span class="sxs-lookup"><span data-stu-id="b3fce-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="b3fce-106">Skaičiavimo darbo atveju galite nuskaityti atsargas, kurias skaičiuojate, ir sekti bendrą sumą.</span><span class="sxs-lookup"><span data-stu-id="b3fce-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="b3fce-107">Kai įgalinate vienetų paėmimą, automatiškai pasirenkamas produkto patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="b3fce-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="b3fce-108">Darbo tipo paėmimų atveju įgalinamas maksimalus vienetų skaičius.</span><span class="sxs-lookup"><span data-stu-id="b3fce-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="b3fce-109">Tai leidžia nustatyti maksimalų skaičių vienetų, kurie turi būti patvirtinti darbo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="b3fce-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="b3fce-110">Didžiausias kiekis paremtas dabartiniu darbo vienetu, kuris yra vykdomas.</span><span class="sxs-lookup"><span data-stu-id="b3fce-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="b3fce-111">Skaičiavimo darbo tipo atveju negalima nustatyti maksimalaus skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="b3fce-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="b3fce-112">Taip pat galite naudoti kiekį ir matavimo vienetą (MV), susietą su nuskaitytu brūkšniniu kodu.</span><span class="sxs-lookup"><span data-stu-id="b3fce-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="b3fce-113">Tai veiks gaunant gavimo srautus, įskaitant mišraus numerio lentelių gavimą, pirkimo užsakymo prekę, perkėlimo užsakymo prekę ir krovinio prekę.</span><span class="sxs-lookup"><span data-stu-id="b3fce-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="b3fce-114">Tai taip pat veikia dalių paėmimo atveju, kai nuskaičius brūkšninį kodą prie patvirtintų vienetų bendro skaičiaus bus pridėtas kiekis bei konvertuojami brūkšninio kodo MV ir darbo vienetas.</span><span class="sxs-lookup"><span data-stu-id="b3fce-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="b3fce-115">Jei skaičiuojant brūkšninio kodo MV patvirtinama, kad sekų grupės skaičiavimui kiekis leidžiamas, kiekis pridedamas prie bendros sumos.</span><span class="sxs-lookup"><span data-stu-id="b3fce-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="b3fce-116">Kai taikoma</span><span class="sxs-lookup"><span data-stu-id="b3fce-116">Where it applies</span></span>

<span data-ttu-id="b3fce-117">Vienetų paėmimas veikia visų skaičiavimo darbų atveju ir pradinio bet kurio tipo darbo paėmimo atveju.</span><span class="sxs-lookup"><span data-stu-id="b3fce-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="b3fce-118">Vienetų paėmimas netaikomas, jei prekė kontroliuojama pagal serijos numerius arba jei tai yra gamybos, arba „kanban“ paėmimas iš numerio lentelės (LP) vietos ir prekė nustatyta išdėstyti.</span><span class="sxs-lookup"><span data-stu-id="b3fce-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="b3fce-119">Nustatyti vienetų paėmimą</span><span class="sxs-lookup"><span data-stu-id="b3fce-119">Set up piece picking</span></span>

1.  <span data-ttu-id="b3fce-120">Mobiliojo įrenginio meniu elemente atidarykite darbo patvirtinimo sąrankos formą: Sandėlio valdymas > **Sandėlio valdymas** > **Sąranka** > **Mobilusis įrenginys** > **Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="b3fce-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="b3fce-121">Mobiliojo įrenginio meniu elemente atidarykite Darbo patvirtinimo sąranka.</span><span class="sxs-lookup"><span data-stu-id="b3fce-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="b3fce-122">Kai darbo tipas yra paėmimas arba skaičiavimas, galima pasirinkti šias parinktis.</span><span class="sxs-lookup"><span data-stu-id="b3fce-122">The following options become available for selection when the work type is pick or counting.</span></span>

| <span data-ttu-id="b3fce-123">Parinktis</span><span class="sxs-lookup"><span data-stu-id="b3fce-123">Option</span></span>        | <span data-ttu-id="b3fce-124">aprašymas</span><span class="sxs-lookup"><span data-stu-id="b3fce-124">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="b3fce-125">Vienetų paėmimo patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="b3fce-125">Piece picking confirmation</span></span>   | <span data-ttu-id="b3fce-126">Pasiekiama paėmimo ir skaičiavimo darbo tipų atveju.</span><span class="sxs-lookup"><span data-stu-id="b3fce-126">Available for pick and counting work types.</span></span> <span data-ttu-id="b3fce-127">Automatiškai pasirenkamas produkto patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="b3fce-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="b3fce-128">Suteikia galimybę mobiliuoju įrenginiu patvirtinti kiekvieną atsargų vienetą.</span><span class="sxs-lookup"><span data-stu-id="b3fce-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> | 
| <span data-ttu-id="b3fce-129">Maksimalus vienetų skaičius</span><span class="sxs-lookup"><span data-stu-id="b3fce-129">Maximum number of pieces</span></span>     | <span data-ttu-id="b3fce-130">Pasiekiama paėmimo darbo atveju, jei įgalintas vienetų paėmimo patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="b3fce-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="b3fce-131">Nustato vienetų, kuriuos turite patvirtinti, skaičiaus apribojimus.</span><span class="sxs-lookup"><span data-stu-id="b3fce-131">Sets a limit to the number of pieces that you must confirm.</span></span> |  

