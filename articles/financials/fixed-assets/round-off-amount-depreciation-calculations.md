---
title: "Nusidėvėjimo skaičiavimų apvalinimo suma"
description: "Šiame straipsnyje aptariamas laukas Suapvalinti nusidėvėjimą, kurį galima rasti puslapyje Knygos nustatymas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0ad57b076542c38d3c29dba4caacf830de6f7200
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="3a6c3-103">Nusidėvėjimo skaičiavimų apvalinimo suma</span><span class="sxs-lookup"><span data-stu-id="3a6c3-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3a6c3-104">Šiame straipsnyje aptariamas laukas Suapvalinti nusidėvėjimą, kurį galima rasti puslapyje Knygos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="3a6c3-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="3a6c3-105">Nusidėvėjimo sumų apvalinimas nustatomas kiekvienai knygai.</span><span class="sxs-lookup"><span data-stu-id="3a6c3-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="3a6c3-106">Nusidėvėjimo sumų apvalinimas naudojamas ilgalaikio turto nusidėvėjimo profilyje, kuris rodo būsimą ilgalaikio turto nusidėvėjimą ir vertę, ir yra rodomas nusidėvėjimo pasiūlymuose.</span><span class="sxs-lookup"><span data-stu-id="3a6c3-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="3a6c3-107">Įveskite žemiausią leidžiamą knygos nusidėvėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="3a6c3-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="3a6c3-108">Neatsižvelgiant į nustatytą apvalinimą, paskutinio nusidėvėjimo laikotarpio nusidėvėjimo suma nėra suapvalinama.</span><span class="sxs-lookup"><span data-stu-id="3a6c3-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="3a6c3-109">Paskutinio nusidėvėjimo laikotarpio pabaigoje, ilgalaikio turto vertė turi būti 0 (nulis) arba likvidacinė vertė, jei likvidacinė vertė naudojama.</span><span class="sxs-lookup"><span data-stu-id="3a6c3-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="3a6c3-110">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3a6c3-110">Example</span></span>

<span data-ttu-id="3a6c3-111">Apskaičiuotas nusidėvėjimas be apvalinimo yra 2444,44.</span><span class="sxs-lookup"><span data-stu-id="3a6c3-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="3a6c3-112">Kaip parodyta toliau pateikiamoje lentelėje, siūlomos sumos skiriasi, atsižvelgiant į tai, kaip apvalinimas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="3a6c3-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="3a6c3-113">Apvalinimo metodas</span><span class="sxs-lookup"><span data-stu-id="3a6c3-113">Rounding method</span></span> | <span data-ttu-id="3a6c3-114">Nusidėvėjimo suma</span><span class="sxs-lookup"><span data-stu-id="3a6c3-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="3a6c3-115">Apvalinimas 0,1</span><span class="sxs-lookup"><span data-stu-id="3a6c3-115">Rounding 0.1</span></span>    | <span data-ttu-id="3a6c3-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="3a6c3-116">2,444.40</span></span>            |
| <span data-ttu-id="3a6c3-117">Apvalinimas 1,00</span><span class="sxs-lookup"><span data-stu-id="3a6c3-117">Rounding 1.00</span></span>   | <span data-ttu-id="3a6c3-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="3a6c3-118">2,444.00</span></span>            |
| <span data-ttu-id="3a6c3-119">Apvalinimas 10,00</span><span class="sxs-lookup"><span data-stu-id="3a6c3-119">Rounding 10.00</span></span>  | <span data-ttu-id="3a6c3-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="3a6c3-120">2,440.00</span></span>            |
| <span data-ttu-id="3a6c3-121">Apvalinimas 100,00</span><span class="sxs-lookup"><span data-stu-id="3a6c3-121">Rounding 100.00</span></span> | <span data-ttu-id="3a6c3-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="3a6c3-122">2,400.00</span></span>            |






