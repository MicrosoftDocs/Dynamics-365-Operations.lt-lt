---
title: Papildomo nusidėvėjimo nustatymas
description: Šioje procedūroje parodoma, kaip sukurti specialiąją nusidėvėjimo nuolaidą ir ją susieti su ilgalaikio turto knyga.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fed9f09b4e37da00a5d78fa088e8814db48456b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968934"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="037bc-103">Papildomo nusidėvėjimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="037bc-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="037bc-104">Šioje procedūroje parodoma, kaip sukurti specialiąją nusidėvėjimo nuolaidą ir ją susieti su ilgalaikio turto knyga.</span><span class="sxs-lookup"><span data-stu-id="037bc-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="037bc-105">Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="037bc-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="037bc-106">Kurti specialiąją nusidėvėjimo nuolaidą</span><span class="sxs-lookup"><span data-stu-id="037bc-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="037bc-107">Pasirinkite Ilgalaikis turtas > Nustatymas > Specialioji nusidėvėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="037bc-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="037bc-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="037bc-108">Click New.</span></span>
3. <span data-ttu-id="037bc-109">Lauke Specialioji nusidėvėjimo nuolaida surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="037bc-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="037bc-110">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="037bc-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="037bc-111">Lauke Procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="037bc-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="037bc-112">Jei nebuvo nurodytas procentas, nustatykite sumą.</span><span class="sxs-lookup"><span data-stu-id="037bc-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="037bc-113">Specialiosios nusidėvėjimo nuolaidos susiejimas su ilgalaikio turto grupės knyga</span><span class="sxs-lookup"><span data-stu-id="037bc-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="037bc-114">Pasirinkite Ilgalaikis turtas > Nustatymas > Ilgalaikio turto grupės.</span><span class="sxs-lookup"><span data-stu-id="037bc-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="037bc-115">Sąraše pasirinkite su specialiąja nusidėvėjimo nuolaida susietą ilgalaikio turto grupę.</span><span class="sxs-lookup"><span data-stu-id="037bc-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="037bc-116">Spustelėkite Knygos.</span><span class="sxs-lookup"><span data-stu-id="037bc-116">Click Books.</span></span>
4. <span data-ttu-id="037bc-117">Sąraše pasirinkite su specialiąja nusidėvėjimo nuolaida susietą knygą.</span><span class="sxs-lookup"><span data-stu-id="037bc-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="037bc-118">Spustelėkite Specialioji nusidėvėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="037bc-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="037bc-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="037bc-119">Click New.</span></span>
7. <span data-ttu-id="037bc-120">Lauke Specialioji nusidėvėjimo nuolaida įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="037bc-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="037bc-121">Pagal numatytąsias nuostatas naudojamas specialiosios nusidėvėjimo nuolaidos sąrankoje nustatytas procentas ar suma.</span><span class="sxs-lookup"><span data-stu-id="037bc-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="037bc-122">Lauke Prioritetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="037bc-122">In the Priority field, enter a number.</span></span>

