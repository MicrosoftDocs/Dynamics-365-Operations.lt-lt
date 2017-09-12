---
title: "Papildomas nusidėvėjimas"
description: "Šiame straipsnyje pateikta papildomo nusidėvėjimo funkcijos apžvalga."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 53d05e66670194e38d1d1f748001ba1eac5f7b94
ms.contentlocale: lt-lt
ms.lasthandoff: 06/29/2017


---

# <a name="bonus-depreciation"></a><span data-ttu-id="7c7e1-103">Papildomas nusidėvėjimas</span><span class="sxs-lookup"><span data-stu-id="7c7e1-103">Bonus depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7c7e1-104">Šiame straipsnyje pateikta papildomo nusidėvėjimo funkcijos apžvalga.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="7c7e1-105">Naudodami papildomą nusidėvėjimą, pirmaisiais metais, kai turtas pradedamas eksploatuoti ir ima nusidėvėti, galite pridėti papildomų nusidėvėjimo sumų.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="7c7e1-106">Papildomas nusidėvėjimas turi būti visada apskaičiuojamas pirmiau nei visi kiti nusidėvėjimo skaičiavimai.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="7c7e1-107">Todėl geriausia kartu naudoti papildomą nusidėvėjimą ir knygas, kuriose išjungta funkcija Registruoti DK.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="7c7e1-108">Galite naudoti parinktį **Panaikinti operacijas, kurios neužregistruotos DK**, norėdami naikinti knygų praeities operacijas, kurios DK neregistruotos.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="7c7e1-109">Papildomą nusidėvėjimą galite vėliau nustatyti turto cikle, panaikindami anksčiau užregistruotas nusidėvėjimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="7c7e1-110">Papildomą nusidėvėjimą galite apskaičiuoti naudodami pasiūlymo procesą, arba galite sukurti neautomatines papildomo nusidėvėjimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="7c7e1-111">Negalima kurti papildomo nusidėvėjimo operacijų, jei toje turto nusidėvėjimo knygoje yra nusidėvėjimo operacijų arba koregavimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="7c7e1-112">Kai skaičiuoti papildomam nusidėvėjimui naudojate pasiūlymo procesą, į pagrindo skaičiavimą įtraukiamos visos esamos papildomos operacijos.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="7c7e1-113">Skaičiavimas taip pat apima visus ankstesnius papildomus turto nusidėvėjimus, įvestus neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="7c7e1-114">Jei turtui bus taikomas daugiau nei vienas papildomas nusidėvėjimas, bus laikomasi prioritetų.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="7c7e1-115">Dėl kiekvieno papildomo nusidėvėjimo sumažėja kitas papildomas turto pagrindo nusidėvėjimas.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="7c7e1-116">Skaičiuojant papildomą nusidėvėjimą neatsižvelgiama į turto pagrindo likvidacinę vertę ir jam netaikoma nusidėvėjimo konvencija.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="7c7e1-117">Šiuo metu Jungtinėse Amerikos Valstijose tam tikra nuosavybė yra laikoma nuosavybe, patenkančia į 179 skyrių.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="7c7e1-118">Naudodami 179 skyriaus atskaitymą, iki tam tikros ribos galite atkurti visą tam tikrą nuosavybę arba jos dalį.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="7c7e1-119">Išlaidas galima susigrąžinti, jas išskaitant tais metais, kai nuosavybė pradedama eksploatuoti.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="7c7e1-120">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7c7e1-120">Example</span></span>
<span data-ttu-id="7c7e1-121">Toliau pateiktas papildomas nusidėvėjimas yra susijęs su turto knyga.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="7c7e1-122">**179 skyrius:** 1 000,00, 1 prioritetas</span><span class="sxs-lookup"><span data-stu-id="7c7e1-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="7c7e1-123">**Laisvoji zona:** 30 proc., 2 prioritetas</span><span class="sxs-lookup"><span data-stu-id="7c7e1-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="7c7e1-124">Turto įsigijimo kaina yra 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="7c7e1-125">Kai skaičiuojamas papildomas nusidėvėjimas, pirmoji 179 nusidėvėjimo skyriaus papildomo nusidėvėjimo suma bus 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="7c7e1-126">Kita papildomo nusidėvėjimo suma pagal laisvosios zonos nusidėvėjimą skaičiuojama, kaip parodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="7c7e1-127">Įsigijimo išlaidos – 1 000 (179 skyriaus nusidėvėjimas) × 30 proc. = 1 200</span><span class="sxs-lookup"><span data-stu-id="7c7e1-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="7c7e1-128">Jei papildomo nusidėvėjimo suma yra didesnė už likusias įsigijimo išlaidas, papildomo nusidėvėjimo suma bus laikomas arba apskaičiuotas papildomas nusidėvėjimas, arba likusios įsigijimo išlaidos, t. y. mažesnė suma.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="7c7e1-129">Jei likusios įsigijimo išlaidos yra 0 (nulis) arba mažesnės, papildomo nusidėvėjimo operacijos nebus generuojamos.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="7c7e1-130">Kai papildomas nusidėvėjimas skaičiuojamas naudojant pasiūlymo procesą, sukuriamos visų nusidėvėjimo įrašų, susijusių su turto knyga, papildomo nusidėvėjimo operacijos.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="7c7e1-131">Galite kurti neribotą papildomo nusidėvėjimo įrašų skaičių.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="7c7e1-132">Kai priskirsite tuos įrašus turto grupės knygai, jie bus taikomi turto knygoje.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="7c7e1-133">Papildomas nusidėvėjimas įvedamas arba procentais, arba fiksuota suma.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="7c7e1-134">Kai užregistruosite nusidėvėjimo pasiūlymus, knygoje papildomo nusidėvėjimo operacijos bus registruojamos atskirai nuo nusidėvėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>




