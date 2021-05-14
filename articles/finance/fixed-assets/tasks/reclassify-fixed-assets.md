---
title: Perklasifikuoti ilgalaikį turtą
description: Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944719"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="b88c1-103">Perklasifikuoti ilgalaikį turtą</span><span class="sxs-lookup"><span data-stu-id="b88c1-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b88c1-104">Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį.</span><span class="sxs-lookup"><span data-stu-id="b88c1-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="b88c1-105">Kai perklasifikuojamas ilgalaikis turtas:</span><span class="sxs-lookup"><span data-stu-id="b88c1-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="b88c1-106">Visos esamo ilgalaikio turto knygos sukuriamos naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="b88c1-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="b88c1-107">Bet kokia informacija, kuri buvo nustatyta pradiniam ilgalaikiam turtui, yra nukopijuojama naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="b88c1-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="b88c1-108">Pradinio ilgalaikio turto knygų būsena yra Uždaryta.</span><span class="sxs-lookup"><span data-stu-id="b88c1-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="b88c1-109">Naujose ilgalaikio turto knygose perklasifikavimo data yra lauke **Įsigijimo data**.</span><span class="sxs-lookup"><span data-stu-id="b88c1-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="b88c1-110">Data, esanti lauke **Nusidėvėjimo vykdymo data**, yra nukopijuota iš pradinės informacijos apie turtą.</span><span class="sxs-lookup"><span data-stu-id="b88c1-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="b88c1-111">Jei nusidėvėjimas jau prasidėjo, lauke **Paskutinio nusidėvėjimo vykdymo data** rodoma perklasifikavimo data.</span><span class="sxs-lookup"><span data-stu-id="b88c1-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="b88c1-112">Esamos pradinio ilgalaikio turto operacijos yra atšaukiamos ir iš naujo generuojamos naujam ilgalaikiam turtui.</span><span class="sxs-lookup"><span data-stu-id="b88c1-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="b88c1-113">Perklasifikuota, kai perkėlimo operacija yra perklasifikuota, sistema veiksmų centre rodys pranešimą, nurodantį, kad perkėlimo operacija nebuvo įvykdyta **perklasifikavimo** proceso metu.</span><span class="sxs-lookup"><span data-stu-id="b88c1-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="b88c1-114">Būtina užbaigti perkėlimo operaciją, kad esamos perklasifikavimo operacijos būtų perkeltos į atitinkamas finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="b88c1-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="b88c1-115">Perklasifikavimo proceso metu sistema vykdo toliau nurodytus veiksmus, kad perklasifikuos turto balansą iš pradinio turto į naują turtą.</span><span class="sxs-lookup"><span data-stu-id="b88c1-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="b88c1-116">Perklasifikavimo proceso metu duomenys nukopijuojami iš pradinės ilgalaikio turto knygos į naują ilgalaikio turto knygą.</span><span class="sxs-lookup"><span data-stu-id="b88c1-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="b88c1-117">Perklasifikavimo operacija naudoja pradinio užregistruoto įsigijimo informaciją, kuri apima finansinės dimensijos informaciją, įtrauktą į įsigijimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="b88c1-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="b88c1-118">Tuo pat metu perklasifikavimo procesas atšaukia pradinio turto įsigijimo ir turto perkėlimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="b88c1-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="b88c1-119">Šioje diagramoje ir procedūroje pateikiamas perklasifikavimo proceso pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="b88c1-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="b88c1-120">[![Perklasifikavimo proceso diagrama](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="b88c1-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="b88c1-121">Atlikite šiuos veiksmus, norėdami perklasifikuoti ilgalaikį turtą:</span><span class="sxs-lookup"><span data-stu-id="b88c1-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="b88c1-122">Pasirinkite **Ilgalaikis turtas > Periodinės užduotys > Perklasifikavimas.**</span><span class="sxs-lookup"><span data-stu-id="b88c1-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="b88c1-123">Lauke **Ilgalaikio turto grupė** pasirinkite grupę, kurią norite perklasifikuoti.</span><span class="sxs-lookup"><span data-stu-id="b88c1-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="b88c1-124">Lauke **Ilgalaikio turto numeris** pasirinkite ilgalaikį turtą, kurį norite perklasifikuoti.</span><span class="sxs-lookup"><span data-stu-id="b88c1-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="b88c1-125">Lauke **Nauja ilgalaikio turto grupė** pasirinkite grupę ilgalaikiam turtui perkelti.</span><span class="sxs-lookup"><span data-stu-id="b88c1-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="b88c1-126">Jei naujai ilgalaikio turto grupei pridedama numeracija, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš naujos ilgalaikio turto grupės numeracijos.</span><span class="sxs-lookup"><span data-stu-id="b88c1-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="b88c1-127">Priešingu atveju, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš numeracijos, nustatytos **ilgalaikio turto parametrų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="b88c1-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="b88c1-128">Jei numeracija **ilgalaikio turto parametrų** puslapyje nenustatyta, lauke **Naujas ilgalaikio turto numeris** įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="b88c1-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="b88c1-129">Lauke **Perklasifikavimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b88c1-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="b88c1-130">Lauke **Kvitų serijos** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b88c1-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="b88c1-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b88c1-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
