---
title: "Įtraukti faktinę vertę"
description: "Puslapio Prekių modelių grupės „FastTab‟ skirtuko Atsargų modelis žymės langelis Įtraukti faktinę vertę naudojamas nurodyti, ar, skaičiuojant prekės einamąją vidutinę savikainą, atsižvelgiama į faktiškai atnaujintas operacijas."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ea8fe31588dd0768e0651c9e1e332212a00cde2
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="include-physical-value"></a><span data-ttu-id="f28c5-103">Įtraukti faktinę vertę</span><span class="sxs-lookup"><span data-stu-id="f28c5-103">Include physical value</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f28c5-104">Puslapio Prekių modelių grupės „FastTab‟ skirtuko Atsargų modelis žymės langelis Įtraukti faktinę vertę naudojamas nurodyti, ar, skaičiuojant prekės einamąją vidutinę savikainą, atsižvelgiama į faktiškai atnaujintas operacijas.</span><span class="sxs-lookup"><span data-stu-id="f28c5-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="f28c5-105">Žymės langelyje **Įtraukti faktinę vertę** yra tolesnės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="f28c5-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="f28c5-106">Vertė</span><span class="sxs-lookup"><span data-stu-id="f28c5-106">Value</span></span>    | <span data-ttu-id="f28c5-107">Rezultatas</span><span class="sxs-lookup"><span data-stu-id="f28c5-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f28c5-108">Pasirinkta</span><span class="sxs-lookup"><span data-stu-id="f28c5-108">Selected</span></span> | <span data-ttu-id="f28c5-109">Savikainai apskaičiuoti naudojamos tiek fiziškai, tiek finansiškai atnaujintos operacijos.</span><span class="sxs-lookup"><span data-stu-id="f28c5-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="f28c5-110">Apmokėta</span><span class="sxs-lookup"><span data-stu-id="f28c5-110">Cleared</span></span>  | <span data-ttu-id="f28c5-111">Skaičiuoti einamajai vidutinei savikainai naudojamos tik finansiškai atnaujintos operacijos.</span><span class="sxs-lookup"><span data-stu-id="f28c5-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="f28c5-112">Žymės langelio poveikis šiek tiek skiriasi – jis priklauso nuo jūsų naudojamo atsargų modelio.</span><span class="sxs-lookup"><span data-stu-id="f28c5-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="f28c5-113">Jei, naudodami atsargų modelį FIFO (pirmiausiai gaunama, pirmiausiai išduodama), LIFO (vėliausiai gaunama, pirmiausiai išduodama) arba LIFO data, pasirenkate žymės langelį **Įtraukti faktinę vertę**, uždarant atsargas taip pat pakoreguojamos faktiškai atnaujintos operacijos.</span><span class="sxs-lookup"><span data-stu-id="f28c5-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="f28c5-114">Jei, naudodami šiuos atsargų modelius, žymės langelio **Įtraukti faktinę vertę** nepasirenkante, uždarant atsargas sudengiamos tik finansiškai atnaujintos operacijos.</span><span class="sxs-lookup"><span data-stu-id="f28c5-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="f28c5-115">Kai naudojate svertinį vidurkį arba svertinio vidurkio datos atsargų modelį, atsargų uždarymas sudengia tik finansiškai atnaujintas operacijas, nesvarbu, ar pažymėjote žymės langelį **Įtraukti fizinę vertę**.</span><span class="sxs-lookup"><span data-stu-id="f28c5-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="f28c5-116">**1 pavyzdys** Pažymėjote žymės langelį **Įtraukti faktinę vertę** ir gaunate tolesnius pirkimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="f28c5-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="f28c5-117">Pirkimo užsakymą, kurio kiekis – 2, o savikaina – 10,00 USD, kurio važtaraštis atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="f28c5-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="f28c5-118">Pirkimo užsakymą, kurio kiekis – 3, o savikaina – 12,00 USD, kurio sąskaita faktūra atnaujinta.</span><span class="sxs-lookup"><span data-stu-id="f28c5-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="f28c5-119">Šiuo atveju einamoji vidutinė savikaina bus 11,20 USD, nes tiek fiziškai, tiek finansiškai atnaujintos operacijos naudojamos savikainai apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="f28c5-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="f28c5-120">**2 pavyzdys** Žymės langelio **Įtraukti faktinę vertę** nepažymėjote ir, nustatant prekes, savikaina yra 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="f28c5-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="f28c5-121">Gaunate pirkimo užsakymą, kurio kiekis – 20, o savikaina – 12,00 USD, kurio važtaraštis atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="f28c5-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="f28c5-122">Kai pardavimo užsakymas užregistruojamas, užregistruotoji savikaina yra 10,00 USD, nes į einamąją vidutinę savikainą neįtrauktos faktiškai užregistruotos operacijos.</span><span class="sxs-lookup"><span data-stu-id="f28c5-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="f28c5-123">**Pastaba.** Palyginimui, jei šios prekės žymės langelį **Įtraukti faktinę vertę** pažymėsite, kai registruojamas pardavimo užsakymas, užregistruotoji savikaina bus 12,00 USD.</span><span class="sxs-lookup"><span data-stu-id="f28c5-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>




