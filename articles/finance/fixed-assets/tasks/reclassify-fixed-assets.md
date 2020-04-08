---
title: Perklasifikuoti ilgalaikį turtą
description: Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cdcb9c337440b8fa9de2bdeb78d3b2d118e91ca
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138282"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="aef12-103">Perklasifikuoti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="aef12-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aef12-104">Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį.</span><span class="sxs-lookup"><span data-stu-id="aef12-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="aef12-105">Kai perklasifikuojamas ilgalaikis turtas:</span><span class="sxs-lookup"><span data-stu-id="aef12-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="aef12-106">Visos esamo ilgalaikio turto knygos sukuriamos naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="aef12-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="aef12-107">Bet kokia informacija, kuri buvo nustatyta pradiniam ilgalaikiam turtui, yra nukopijuojama naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="aef12-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="aef12-108">Pradinio ilgalaikio turto knygų būsena yra Uždaryta.</span><span class="sxs-lookup"><span data-stu-id="aef12-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="aef12-109">Naujose ilgalaikio turto knygose perklasifikavimo data yra lauke **Įsigijimo data**.</span><span class="sxs-lookup"><span data-stu-id="aef12-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="aef12-110">Data, esanti lauke **Nusidėvėjimo vykdymo data**, yra nukopijuota iš pradinės informacijos apie turtą.</span><span class="sxs-lookup"><span data-stu-id="aef12-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="aef12-111">Jei nusidėvėjimas jau prasidėjo, lauke **Paskutinio nusidėvėjimo vykdymo data** rodoma perklasifikavimo data.</span><span class="sxs-lookup"><span data-stu-id="aef12-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="aef12-112">Esamos pradinio ilgalaikio turto operacijos yra atšaukiamos ir iš naujo generuojamos naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="aef12-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="aef12-113">Atlikite šiuos veiksmus, norėdami perklasifikuoti ilgalaikį turtą:</span><span class="sxs-lookup"><span data-stu-id="aef12-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="aef12-114">Pasirinkite **Ilgalaikis turtas > Periodinės užduotys > Perklasifikavimas.**</span><span class="sxs-lookup"><span data-stu-id="aef12-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="aef12-115">Lauke **Ilgalaikio turto grupė** pasirinkite grupę, kurią norite perklasifikuoti.</span><span class="sxs-lookup"><span data-stu-id="aef12-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="aef12-116">Lauke **Ilgalaikio turto numeris** pasirinkite ilgalaikį turtą, kurį norite perklasifikuoti.</span><span class="sxs-lookup"><span data-stu-id="aef12-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="aef12-117">Lauke **Nauja ilgalaikio turto grupė** pasirinkite grupę ilgalaikiam turtui perkelti.</span><span class="sxs-lookup"><span data-stu-id="aef12-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="aef12-118">Jei naujai ilgalaikio turto grupei pridedama numeracija, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš naujos ilgalaikio turto grupės numeracijos.</span><span class="sxs-lookup"><span data-stu-id="aef12-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="aef12-119">Priešingu atveju, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš numeracijos, nustatytos **ilgalaikio turto parametrų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="aef12-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="aef12-120">Jei numeracija **ilgalaikio turto parametrų** puslapyje nenustatyta, lauke **Naujas ilgalaikio turto numeris** įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="aef12-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="aef12-121">Lauke **Perklasifikavimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="aef12-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="aef12-122">Lauke **Kvitų serijos** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aef12-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="aef12-123">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="aef12-123">Click **OK**.</span></span>
