---
title: Bendrieji gamybos nuokrypių šaltiniai
description: Šis straipsnis paaiškina įvairius įprastus kiekvieno gamybos nuokrypio tipo šaltinius.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da09e24d7ed041686385b8239287288228d3668e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201967"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="c2927-103">Bendrieji gamybos nuokrypių šaltiniai</span><span class="sxs-lookup"><span data-stu-id="c2927-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2927-104">Šis straipsnis paaiškina įvairius įprastus kiekvieno gamybos nuokrypio tipo šaltinius.</span><span class="sxs-lookup"><span data-stu-id="c2927-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="c2927-105">Štai keletas įprastų **partijos dydžio** nuokrypio šaltinių:</span><span class="sxs-lookup"><span data-stu-id="c2927-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="c2927-106">Gamybos užsakymo prekių kiekis skiriasi nuo skaičiavimo kiekio, naudojamo atliekant standartinį išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="c2927-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="c2927-107">Šis kiekis sudaro amortizuojamų pastovių išlaidų pagrindą.</span><span class="sxs-lookup"><span data-stu-id="c2927-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="c2927-108">Gamybos užsakymo pastovių išlaidų vertė skiriasi nuo pastovių išlaidų, naudojamų atliekant standartinį išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="c2927-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="c2927-109">Gamybos užsakymo pastovios išlaidos gali skirtis dėl keleto priežasčių.</span><span class="sxs-lookup"><span data-stu-id="c2927-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="c2927-110">Pvz., pastovios išlaidos gali atspindėti šiuos veiksnius:</span><span class="sxs-lookup"><span data-stu-id="c2927-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="c2927-111">rankiniu būdu atlikti gamybos komplektavimo specifikacijų (KS) arba maršruto keitimai;</span><span class="sxs-lookup"><span data-stu-id="c2927-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="c2927-112">skirtingos KS versijos arba maršruto versijos pasirinkimas kuriant gamybos užsakymą;</span><span class="sxs-lookup"><span data-stu-id="c2927-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="c2927-113">suplanuoti prekei priskirtos KS versijos arba maršruto versijos inžineriniai pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="c2927-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="c2927-114">Štai keletas įprastų **gamybos kainos** nuokrypio šaltinių:</span><span class="sxs-lookup"><span data-stu-id="c2927-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="c2927-115">Paskelbto maršruto planavimo operacijos išlaidų kategorija (ir išlaidų kategorijos kaina) skiriasi nuo išlaidų kategorijos, naudojamos atliekant standartinį išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="c2927-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="c2927-116">Išlaidų kategorijos kainos aktyvios išlaidos skiriasi nuo išlaidų kategorijos kainos, naudojamos atliekant standartinį išlaidų skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="c2927-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="c2927-117">Štai keletas įprastų **gamybos kiekio** nuokrypio šaltinių:</span><span class="sxs-lookup"><span data-stu-id="c2927-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="c2927-118">Medžiagos komponento išdavimas per didelis arba per mažas.</span><span class="sxs-lookup"><span data-stu-id="c2927-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="c2927-119">Maršruto planavimo operacijos ataskaitos laikas per ilgas arba per trumpas.</span><span class="sxs-lookup"><span data-stu-id="c2927-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="c2927-120">Gaunamas pirminės prekės kiekis lyginant su užsakymo kiekiu per didelis arba per mažas.</span><span class="sxs-lookup"><span data-stu-id="c2927-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="c2927-121">Tačiau komponentus išduodate ir ataskaitas apie operacijas teikiate visas, pagal gamybos užsakymo kiekį.</span><span class="sxs-lookup"><span data-stu-id="c2927-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="c2927-122">Štai keletas įprastų **gamybos pakaitalo** nuokrypio šaltinių:</span><span class="sxs-lookup"><span data-stu-id="c2927-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="c2927-123">Medžiagos komponento, neįtraukto į gamybos KS, išdavimas.</span><span class="sxs-lookup"><span data-stu-id="c2927-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="c2927-124">Komponento įtraukimas į gamybos KS rankiniu būdu ir šio komponento paskelbimas sunaudotu.</span><span class="sxs-lookup"><span data-stu-id="c2927-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="c2927-125">Prekės paskelbimas sunaudota, kai ji nėra rankiniu būdu įtraukiama į gamybos KS.</span><span class="sxs-lookup"><span data-stu-id="c2927-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="c2927-126">Operacijos įtraukimas į gamybos maršrutą rankiniu būdu ir šios operacijos paskelbimas sunaudota.</span><span class="sxs-lookup"><span data-stu-id="c2927-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="c2927-127">Sukūrę gamybos užsakymą, pasirenkate KS versiją, kuri skiriasi nuo standartiniame skaičiavime naudojamos KS versijos.</span><span class="sxs-lookup"><span data-stu-id="c2927-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="c2927-128">Sukūrę gamybos užsakymą, pasirenkate maršruto versiją, kuri skiriasi nuo standartiniame išlaidų skaičiavime naudojamos KS versijos.</span><span class="sxs-lookup"><span data-stu-id="c2927-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>




