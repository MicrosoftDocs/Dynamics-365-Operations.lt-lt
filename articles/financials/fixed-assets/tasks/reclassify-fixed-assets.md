---
title: Perklasifikuoti ilgalaikį turtą
description: Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8e289e2c18fd28829fb4b749933ae1d84e0b631
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "323300"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="5d344-103">Perklasifikuoti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="5d344-103">Reclassify fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d344-104">Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį.</span><span class="sxs-lookup"><span data-stu-id="5d344-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="5d344-105">Kai perklasifikuojamas ilgalaikis turtas:</span><span class="sxs-lookup"><span data-stu-id="5d344-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="5d344-106">• Visi esamo ilgalaikio turto vertinimo modeliai sukuriami naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="5d344-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="5d344-107">Bet kokia informacija, kuri buvo nustatyta pradiniam ilgalaikiam turtui, yra nukopijuojama naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="5d344-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="5d344-108">Pradinio ilgalaikio turto vertinimo modelių būsena yra Uždaryta.</span><span class="sxs-lookup"><span data-stu-id="5d344-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="5d344-109">• Naujuose ilgalaikio turto vertinimo modeliuose perklasifikavimo data yra lauke Įsigijimo data.</span><span class="sxs-lookup"><span data-stu-id="5d344-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="5d344-110">Data, esanti lauke Nusidėvėjimo vykdymo data, yra nukopijuota iš pradinės informacijos apie turtą.</span><span class="sxs-lookup"><span data-stu-id="5d344-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="5d344-111">Jei nusidėvėjimas jau prasidėjo, lauke Paskutinio nusidėvėjimo vykdymo data rodoma perklasifikavimo data.</span><span class="sxs-lookup"><span data-stu-id="5d344-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="5d344-112">• Esamos pradinio ilgalaikio turto operacijos yra atšaukiamos ir iš naujo generuojamos naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="5d344-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="5d344-113">Pasirinkite Ilgalaikis turtas > Periodinės užduotys > Perklasifikavimas.</span><span class="sxs-lookup"><span data-stu-id="5d344-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="5d344-114">Lauke Ilgalaikio turto grupė pasirinkite grupę, kurią norite perklasifikuoti.</span><span class="sxs-lookup"><span data-stu-id="5d344-114">In the Fixed asset group field, select the group to reclassify.</span></span>
3. <span data-ttu-id="5d344-115">Lauke Ilgalaikio turto numeris pasirinkite ilgalaikį turtą, kurį norite perklasifikuoti.</span><span class="sxs-lookup"><span data-stu-id="5d344-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="5d344-116">Lauke Nauja ilgalaikio turto grupė pasirinkite grupę ilgalaikiam turtui perkelti.</span><span class="sxs-lookup"><span data-stu-id="5d344-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="5d344-117">Jei naujai ilgalaikio turto grupei pridedama numeracija, naujo ilgalaikio turto numerio lauke atnaujinamas numeris iš naujos ilgalaikio turto grupės numeracijos.</span><span class="sxs-lookup"><span data-stu-id="5d344-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="5d344-118">Priešingu atveju, naujo ilgalaikio turto numerio lauke atnaujinamas numeris iš numeracijos, nustatytos ilgalaikio turto parametrų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="5d344-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="5d344-119">Jei numeracija ilgalaikio turto parametrų puslapyje nenustatyta, lauke Naujas ilgalaikio turto numeris įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="5d344-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="5d344-120">Lauke Perklasifikavimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="5d344-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="5d344-121">Lauke Kvitų serijos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5d344-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="5d344-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="5d344-122">Click OK.</span></span>

