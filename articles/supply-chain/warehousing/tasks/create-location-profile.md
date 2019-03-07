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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "361388"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="c2989-103">Kurti vietos šabloną</span><span class="sxs-lookup"><span data-stu-id="c2989-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c2989-104">Su kiekviena sandėlio vieta turi būti susietas vietos šablonas, kuris nurodo vietos ypatybes, pvz., ar vietoje leidžiamos skirtingos prekės.</span><span class="sxs-lookup"><span data-stu-id="c2989-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="c2989-105">Atlikdami šią procedūrą sukursite vietos, kurioje kontrolė pagal numerio lentelę yra nebūtina, šabloną.</span><span class="sxs-lookup"><span data-stu-id="c2989-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="c2989-106">Leisime skirtingas prekes, skirtingas atsargų būsenas ir ciklo skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="c2989-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="c2989-107">Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="c2989-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="c2989-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c2989-108">Click New.</span></span>
2. <span data-ttu-id="c2989-109">Lauke Vietos šablono ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="c2989-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="c2989-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c2989-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c2989-111">Lauke Vietos formatas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c2989-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="c2989-112">Lauke Vietos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c2989-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="c2989-113">Lauke Rampos valdymo šablono ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c2989-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="c2989-114">Lauke Leisti skirtingas prekes pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c2989-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="c2989-115">Lauke Leisti įvairias atsargų būsenas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c2989-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="c2989-116">Lauke Leisti ciklo skaičiavimą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="c2989-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="c2989-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c2989-117">Click Save.</span></span>
11. <span data-ttu-id="c2989-118">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlis > Vietos profiliai.</span><span class="sxs-lookup"><span data-stu-id="c2989-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

