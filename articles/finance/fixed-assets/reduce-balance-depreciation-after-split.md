---
title: Mažėjančios vertės nusidėvėjimas po skaidymo
description: Šioje temoje aprašomas metodas, naudojamas ilgalaikiam turtui nusidėvėjimui skaičiuoti po to, kai turtas skaidomas naudojant sumažinimo balanso metodą.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea89d54b9b8287d9c81b75a99c5808b5deb05cef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976096"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="1368f-103">Mažėjančios vertės nusidėvėjimas po skaidymo</span><span class="sxs-lookup"><span data-stu-id="1368f-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1368f-104">Šioje temoje aprašomas metodas, naudojamas ilgalaikiam turtui nusidėvėjimui skaičiuoti po to, kai turtas skaidomas į kitą turtą naudojant sumažinimo balanso metodą.</span><span class="sxs-lookup"><span data-stu-id="1368f-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="1368f-105">Turto knygoje sukonfigūruoti nusidėvėjimo metai yra finansiniai metai.</span><span class="sxs-lookup"><span data-stu-id="1368f-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="1368f-106">Norėdami daugiau informacijos žr. [Balanso nusidėvėjimo mažinimas](reduce-balance-depreciation.md) ir [Ilgalaikio turto skaidymas](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="1368f-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="1368f-107">Jei jūs skaidote ilgalaikį turtą per ataskaitinį laikotarpį, kuris yra vėlesnis už turto įsigijimo laikotarpį, sumažintas balanso nusidėvėjimas bus skaičiuojamas pagal praėjusių metų turto balansinę vertę (NBV).</span><span class="sxs-lookup"><span data-stu-id="1368f-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="1368f-108">Taip pat bus atsižvelgiama į įsigijimo ir nusidėvėjimo nustatymo operacijas, sugeneruotas iš operacijos, kuri skaido turtą.</span><span class="sxs-lookup"><span data-stu-id="1368f-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="1368f-109">Taip daroma prielaida, kad turtas buvo įsigytas per vienerius finansinius metus ir padalintas į vėlesnius finansinius metus.</span><span class="sxs-lookup"><span data-stu-id="1368f-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="1368f-110">Suma, kuri turi būti nusidėvėjama pradiniam turtui, kai skaidymas atitinka turto NBV prieš tai, kai turtas buvo suskaidytas, ir pirkimo ir nusidėvėjimo derinimo operacija, užregistruota išskaidyti.</span><span class="sxs-lookup"><span data-stu-id="1368f-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="1368f-111">Pavyzdžiui, šios sąlygos galioja.</span><span class="sxs-lookup"><span data-stu-id="1368f-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="1368f-112">Ataskaitinis laikotarpis yra nuo birželio 30 d. iki liepos 1 d.</span><span class="sxs-lookup"><span data-stu-id="1368f-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="1368f-113">Mažėjančios vertės procentas yra 18 proc., o turtas įsigytas 2019 m. birželį, kai įsigijimo kaina buvo 10 000 USD.</span><span class="sxs-lookup"><span data-stu-id="1368f-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="1368f-114">Pirmųjų finansinių metų nusidėvėjimas lygus 18 000 USD, mėnesinis nusidėvėjimas yra lygus 150 USD, o turtas nusidėvimas iki 2019 m. lapkričio, suma – 738,75 USD.</span><span class="sxs-lookup"><span data-stu-id="1368f-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="1368f-115">2019 m. lapkritį 80 procentų turto išskaidoma į kitą ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="1368f-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="1368f-116">[![Mažėjančios vertės nusidėvėjimas po skaidymo](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="1368f-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="1368f-117">Pradinio turto nusidėvėjimo suma yra 1822,25 USD.</span><span class="sxs-lookup"><span data-stu-id="1368f-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="1368f-118">Ši suma yra lygi NBV prieš registruojant išskaidytą operaciją (9111,25 USD), pridėjus įsigijimo suderinimą, sugeneruotą registruojant skaidymo operaciją (–8000 USD), pridėjus nusidėvėjimo suderinimą, sugeneruotą per išskaidytą operaciją (711 USD).</span><span class="sxs-lookup"><span data-stu-id="1368f-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="1368f-119">Todėl antraisiais metais nusidėvėjimas yra (1822,25 × 18 proc.) ÷ 12 = 27,33 USD.</span><span class="sxs-lookup"><span data-stu-id="1368f-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="1368f-120">Pirmaisiais metais naujo ilgalaikio turto nusidėvėjimo suma yra (8000 × 18 proc.) ÷ 12 = 120 USD.</span><span class="sxs-lookup"><span data-stu-id="1368f-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>
