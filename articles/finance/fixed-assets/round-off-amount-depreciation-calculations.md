---
title: Nusidėvėjimo skaičiavimų apvalinimo suma
description: Šiame straipsnyje aptariamas laukas Suapvalinti nusidėvėjimą, kurį galima rasti puslapyje Knygos nustatymas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40fd019b1b5900fbd15866d9d3c32ed6d88147b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446049"
---
# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="f3cdb-103">Nusidėvėjimo skaičiavimų apvalinimo suma</span><span class="sxs-lookup"><span data-stu-id="f3cdb-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3cdb-104">Šiame straipsnyje aptariamas laukas Suapvalinti nusidėvėjimą, kurį galima rasti puslapyje Knygos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="f3cdb-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="f3cdb-105">Nusidėvėjimo sumų apvalinimas nustatomas kiekvienai knygai.</span><span class="sxs-lookup"><span data-stu-id="f3cdb-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="f3cdb-106">Nusidėvėjimo sumų apvalinimas naudojamas ilgalaikio turto nusidėvėjimo profilyje, kuris rodo būsimą ilgalaikio turto nusidėvėjimą ir vertę, ir yra rodomas nusidėvėjimo pasiūlymuose.</span><span class="sxs-lookup"><span data-stu-id="f3cdb-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="f3cdb-107">Įveskite žemiausią leidžiamą knygos nusidėvėjimo sumą.</span><span class="sxs-lookup"><span data-stu-id="f3cdb-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="f3cdb-108">Neatsižvelgiant į nustatytą apvalinimą, paskutinio nusidėvėjimo laikotarpio nusidėvėjimo suma nėra suapvalinama.</span><span class="sxs-lookup"><span data-stu-id="f3cdb-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="f3cdb-109">Paskutinio nusidėvėjimo laikotarpio pabaigoje, ilgalaikio turto vertė turi būti 0 (nulis) arba likvidacinė vertė, jei likvidacinė vertė naudojama.</span><span class="sxs-lookup"><span data-stu-id="f3cdb-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="f3cdb-110">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f3cdb-110">Example</span></span>

<span data-ttu-id="f3cdb-111">Apskaičiuotas nusidėvėjimas be apvalinimo yra 2444,44.</span><span class="sxs-lookup"><span data-stu-id="f3cdb-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="f3cdb-112">Kaip parodyta toliau pateikiamoje lentelėje, siūlomos sumos skiriasi, atsižvelgiant į tai, kaip apvalinimas nustatytas.</span><span class="sxs-lookup"><span data-stu-id="f3cdb-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="f3cdb-113">Apvalinimo metodas</span><span class="sxs-lookup"><span data-stu-id="f3cdb-113">Rounding method</span></span> | <span data-ttu-id="f3cdb-114">Nusidėvėjimo suma</span><span class="sxs-lookup"><span data-stu-id="f3cdb-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="f3cdb-115">Apvalinimas 0,1</span><span class="sxs-lookup"><span data-stu-id="f3cdb-115">Rounding 0.1</span></span>    | <span data-ttu-id="f3cdb-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="f3cdb-116">2,444.40</span></span>            |
| <span data-ttu-id="f3cdb-117">Apvalinimas 1,00</span><span class="sxs-lookup"><span data-stu-id="f3cdb-117">Rounding 1.00</span></span>   | <span data-ttu-id="f3cdb-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="f3cdb-118">2,444.00</span></span>            |
| <span data-ttu-id="f3cdb-119">Apvalinimas 10,00</span><span class="sxs-lookup"><span data-stu-id="f3cdb-119">Rounding 10.00</span></span>  | <span data-ttu-id="f3cdb-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="f3cdb-120">2,440.00</span></span>            |
| <span data-ttu-id="f3cdb-121">Apvalinimas 100,00</span><span class="sxs-lookup"><span data-stu-id="f3cdb-121">Rounding 100.00</span></span> | <span data-ttu-id="f3cdb-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="f3cdb-122">2,400.00</span></span>            |





