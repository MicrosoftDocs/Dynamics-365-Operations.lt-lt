---
title: Kurti vietos šabloną
description: Su kiekviena sandėlio vieta turi būti susietas vietos šablonas, kuris nurodo vietos ypatybes, pvz., ar vietoje leidžiamos skirtingos prekės.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9e1217a1105e1d53fc937f927e066e392f1ef14
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847332"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="dde30-103">Kurti vietos šabloną</span><span class="sxs-lookup"><span data-stu-id="dde30-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dde30-104">Su kiekviena sandėlio vieta turi būti susietas vietos šablonas, kuris nurodo vietos ypatybes, pvz., ar vietoje leidžiamos skirtingos prekės.</span><span class="sxs-lookup"><span data-stu-id="dde30-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="dde30-105">Atlikdami šią procedūrą sukursite vietos, kurioje kontrolė pagal numerio lentelę yra nebūtina, šabloną.</span><span class="sxs-lookup"><span data-stu-id="dde30-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="dde30-106">Leisime skirtingas prekes, skirtingas atsargų būsenas ir ciklo skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="dde30-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="dde30-107">Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="dde30-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="dde30-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="dde30-108">Click New.</span></span>
2. <span data-ttu-id="dde30-109">Lauke Vietos šablono ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="dde30-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="dde30-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dde30-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dde30-111">Lauke Vietos formatas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dde30-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="dde30-112">Lauke Vietos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dde30-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="dde30-113">Lauke Rampos valdymo šablono ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dde30-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="dde30-114">Lauke Leisti skirtingas prekes pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="dde30-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="dde30-115">Lauke Leisti įvairias atsargų būsenas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="dde30-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="dde30-116">Lauke Leisti ciklo skaičiavimą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="dde30-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="dde30-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="dde30-117">Click Save.</span></span>
11. <span data-ttu-id="dde30-118">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlis > Vietos profiliai.</span><span class="sxs-lookup"><span data-stu-id="dde30-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

