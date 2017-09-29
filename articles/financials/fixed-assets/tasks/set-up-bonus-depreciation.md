--- 
title: "Papildomo nusidėvėjimo nustatymas"
description: "Šioje procedūroje parodoma, kaip sukurti specialiąją nusidėvėjimo nuolaidą ir ją susieti su ilgalaikio turto knyga."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7e6ebb13084626b477b6e0b24acdc09e2c0d3d6d
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="d4fee-103">Papildomo nusidėvėjimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d4fee-103">Set up bonus depreciation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4fee-104">Šioje procedūroje parodoma, kaip sukurti specialiąją nusidėvėjimo nuolaidą ir ją susieti su ilgalaikio turto knyga.</span><span class="sxs-lookup"><span data-stu-id="d4fee-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="d4fee-105">Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="d4fee-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="d4fee-106">Kurti specialiąją nusidėvėjimo nuolaidą</span><span class="sxs-lookup"><span data-stu-id="d4fee-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="d4fee-107">Pasirinkite Ilgalaikis turtas > Nustatymas > Specialioji nusidėvėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="d4fee-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="d4fee-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d4fee-108">Click New.</span></span>
3. <span data-ttu-id="d4fee-109">Lauke Specialioji nusidėvėjimo nuolaida surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4fee-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="d4fee-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4fee-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d4fee-111">Lauke Procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d4fee-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="d4fee-112">Jei nebuvo nurodytas procentas, nustatykite sumą.</span><span class="sxs-lookup"><span data-stu-id="d4fee-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="d4fee-113">Specialiosios nusidėvėjimo nuolaidos susiejimas su ilgalaikio turto grupės knyga</span><span class="sxs-lookup"><span data-stu-id="d4fee-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="d4fee-114">Pasirinkite Ilgalaikis turtas > Nustatymas > Ilgalaikio turto grupės.</span><span class="sxs-lookup"><span data-stu-id="d4fee-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="d4fee-115">Sąraše pasirinkite su specialiąja nusidėvėjimo nuolaida susietą ilgalaikio turto grupę.</span><span class="sxs-lookup"><span data-stu-id="d4fee-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="d4fee-116">Spustelėkite Knygos.</span><span class="sxs-lookup"><span data-stu-id="d4fee-116">Click Books.</span></span>
4. <span data-ttu-id="d4fee-117">Sąraše pasirinkite su specialiąja nusidėvėjimo nuolaida susietą knygą.</span><span class="sxs-lookup"><span data-stu-id="d4fee-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="d4fee-118">Spustelėkite Specialioji nusidėvėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="d4fee-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="d4fee-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d4fee-119">Click New.</span></span>
7. <span data-ttu-id="d4fee-120">Lauke Specialioji nusidėvėjimo nuolaida įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4fee-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="d4fee-121">Pagal numatytąsias nuostatas naudojamas specialiosios nusidėvėjimo nuolaidos sąrankoje nustatytas procentas ar suma.</span><span class="sxs-lookup"><span data-stu-id="d4fee-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="d4fee-122">Lauke Prioritetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d4fee-122">In the Priority field, enter a number.</span></span>

