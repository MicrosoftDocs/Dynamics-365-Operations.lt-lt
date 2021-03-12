---
title: Vietos šablono kūrimas
description: Šioje temoje aiškinama, kaip sukurti vietos profilį Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bd5924447c0af21b5b26a2dc9098cf245b7ee12
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977268"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="f7186-103">Vietos šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7186-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7186-104">Šioje temoje aiškinama, kaip sukurti vietos profilį Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f7186-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f7186-105">Su kiekviena sandėlio vieta turi būti susietas vietos šablonas, kuris nurodo vietos ypatybes, pvz., ar vietoje leidžiamos skirtingos prekės.</span><span class="sxs-lookup"><span data-stu-id="f7186-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="f7186-106">Atlikdami šią procedūrą sukursite vietos, kurioje kontrolė pagal numerio lentelę yra nebūtina, šabloną.</span><span class="sxs-lookup"><span data-stu-id="f7186-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="f7186-107">Leisime skirtingas prekes, skirtingas atsargų būsenas ir ciklo skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="f7186-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="f7186-108">Šią procedūrą galite naudoti USMF demonstracinių duomenų įmonėje.</span><span class="sxs-lookup"><span data-stu-id="f7186-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="f7186-109">Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Sąranka > Sandėlio > Vietos profilis**.</span><span class="sxs-lookup"><span data-stu-id="f7186-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="f7186-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f7186-110">Select **New**.</span></span>
3. <span data-ttu-id="f7186-111">Lauke **Vietos profilio ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f7186-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="f7186-112">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f7186-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="f7186-113">Lauke **Vietos formatas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f7186-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="f7186-114">Lauke **Vietos tipas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f7186-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="f7186-115">Lauke **Dokumento valdymo profilio ID** įveskite arba pažymėkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f7186-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="f7186-116">Pažymėkite **Taip** lauke **Leisti mišrius elementus**.</span><span class="sxs-lookup"><span data-stu-id="f7186-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="f7186-117">Pažymėkite **Taip** lauke **Leisti mišrias atsargų būsenas**.</span><span class="sxs-lookup"><span data-stu-id="f7186-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="f7186-118">Pažymėkite **Taip** lauke **Leisti ciklo skaičiavimą**.</span><span class="sxs-lookup"><span data-stu-id="f7186-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="f7186-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f7186-119">Select **Save**.</span></span>

