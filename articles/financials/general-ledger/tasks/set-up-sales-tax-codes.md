---
title: PVM kodų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti užsakymų sulaikymo kodus Dynamics 365 for Finance and Operations.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3419c6b569093d717158e80bd9bc01054d82bff9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834835"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="481de-103">PVM kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="481de-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="481de-104">Šioje temoje paaiškinama, kaip nustatyti užsakymų sulaikymo kodus Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="481de-104">This topic explains how to set up sales tax codes in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="481de-105">PVM kodai sukurti kiekvienam netiesioginiam mokesčiui ar muitui, kuriuos juridinis subjektas yra įsipareigojęs skaičiuoti, rinkti ir mokėti PVM institucijoms.</span><span class="sxs-lookup"><span data-stu-id="481de-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="481de-106">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="481de-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="481de-107">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > PVM > PVM kodai**.</span><span class="sxs-lookup"><span data-stu-id="481de-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="481de-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="481de-108">Select **New**.</span></span>
3. <span data-ttu-id="481de-109">Lauke **Sales tax code**surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="481de-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="481de-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="481de-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="481de-111">Pasirinkite **Settlement period**, kad nurodytumėte, kuriai PVM institucijai ir kuriais intervalais reikia pranešti apie šį PVM ir jį mokėti.</span><span class="sxs-lookup"><span data-stu-id="481de-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="481de-112">Pasirinkite **Ledger posting group**, kad nurodytumėte pagrindines sąskaitas, kuriose į DK registruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="481de-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="481de-113">Išplėskite **Calculation** FastTab.</span><span class="sxs-lookup"><span data-stu-id="481de-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="481de-114">„FastTab‟ Skaičiavimas yra keli laukai, kurie kontroliuoja, kaip bus apskaičiuojamos PVM sumos.</span><span class="sxs-lookup"><span data-stu-id="481de-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="481de-115">Tinkamai užpildykite šiuos laukelius.</span><span class="sxs-lookup"><span data-stu-id="481de-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="481de-116">Sąsajos viršutinėje dalyje esančioje **Veiksmų srityje** pasirinkite **PVM kodas**.</span><span class="sxs-lookup"><span data-stu-id="481de-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="481de-117">Pasirinkite **Reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="481de-117">Select **Values**.</span></span>
10. <span data-ttu-id="481de-118">Įveskite šio mokesčio kodo reikšmę stulpelyje **value**.</span><span class="sxs-lookup"><span data-stu-id="481de-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="481de-119">Jei „FastTab‟ **Calculation**, lauke Kilmė pasirinkta Suma pagal vienetą, kad būtų apskaičiuota PVM suma, reikšmė bus padauginta iš operacijos kiekio.</span><span class="sxs-lookup"><span data-stu-id="481de-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="481de-120">Jei mokesčio kodas yra ne vienetinis mokestis, reikšmė yra procentinė dalis, taikoma šio mokesčio kodo kilmei, kad būtų apskaičiuota PVM suma.</span><span class="sxs-lookup"><span data-stu-id="481de-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="481de-121">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="481de-121">Select **Save**.</span></span>
12. <span data-ttu-id="481de-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="481de-122">Close the page.</span></span>
13. <span data-ttu-id="481de-123">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="481de-123">Select **Save**.</span></span>

