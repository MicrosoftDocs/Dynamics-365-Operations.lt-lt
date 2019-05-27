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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bc7705b7db46af8fbe8bf9e78a878a53249b452
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560914"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="aebae-103">Kurti vietos šabloną</span><span class="sxs-lookup"><span data-stu-id="aebae-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aebae-104">Su kiekviena sandėlio vieta turi būti susietas vietos šablonas, kuris nurodo vietos ypatybes, pvz., ar vietoje leidžiamos skirtingos prekės.</span><span class="sxs-lookup"><span data-stu-id="aebae-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="aebae-105">Atlikdami šią procedūrą sukursite vietos, kurioje kontrolė pagal numerio lentelę yra nebūtina, šabloną.</span><span class="sxs-lookup"><span data-stu-id="aebae-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="aebae-106">Leisime skirtingas prekes, skirtingas atsargų būsenas ir ciklo skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="aebae-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="aebae-107">Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="aebae-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="aebae-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="aebae-108">Click New.</span></span>
2. <span data-ttu-id="aebae-109">Lauke Vietos šablono ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="aebae-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="aebae-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aebae-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="aebae-111">Lauke Vietos formatas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aebae-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="aebae-112">Lauke Vietos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aebae-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="aebae-113">Lauke Rampos valdymo šablono ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="aebae-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="aebae-114">Lauke Leisti skirtingas prekes pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="aebae-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="aebae-115">Lauke Leisti įvairias atsargų būsenas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="aebae-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="aebae-116">Lauke Leisti ciklo skaičiavimą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="aebae-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="aebae-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="aebae-117">Click Save.</span></span>
11. <span data-ttu-id="aebae-118">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlis > Vietos profiliai.</span><span class="sxs-lookup"><span data-stu-id="aebae-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

