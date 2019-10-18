---
title: PVM kodų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti užsakymų sulaikymo kodus Dynamics 365 Finance.
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
ms.openlocfilehash: 45a4a7a20b20961d707e43b35d61c10a08c74943
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185985"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="994bf-103">PVM kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="994bf-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="994bf-104">Šioje temoje paaiškinama, kaip nustatyti PVM kodus.</span><span class="sxs-lookup"><span data-stu-id="994bf-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="994bf-105">PVM kodai sukurti kiekvienam netiesioginiam mokesčiui ar muitui, kuriuos juridinis subjektas yra įsipareigojęs skaičiuoti, rinkti ir mokėti PVM institucijoms.</span><span class="sxs-lookup"><span data-stu-id="994bf-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="994bf-106">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="994bf-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="994bf-107">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > PVM > PVM kodai**.</span><span class="sxs-lookup"><span data-stu-id="994bf-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="994bf-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="994bf-108">Select **New**.</span></span>
3. <span data-ttu-id="994bf-109">Lauke **PVM kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="994bf-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="994bf-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="994bf-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="994bf-111">Pasirinkite **Sudengimo laikotarpis**, kad nurodytumėte, kuriai PVM institucijai ir kuriais intervalais reikia pranešti apie šį PVM ir jį mokėti.</span><span class="sxs-lookup"><span data-stu-id="994bf-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="994bf-112">Pasirinkite **DK registravimo grupė**, kad nurodytumėte pagrindines sąskaitas, kuriose į DK registruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="994bf-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="994bf-113">Išplėskite „FastTab“ skirtuką **Skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="994bf-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="994bf-114">Jis apima kelis laukus, kurie kontroliuoja, kaip bus apskaičiuojamos PVM sumos.</span><span class="sxs-lookup"><span data-stu-id="994bf-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="994bf-115">Tinkamai užpildykite šiuos laukelius.</span><span class="sxs-lookup"><span data-stu-id="994bf-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="994bf-116">Sąsajos viršutinėje dalyje **Veiksmų sritis** pasirinkite **PVM kodas**.</span><span class="sxs-lookup"><span data-stu-id="994bf-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="994bf-117">Pasirinkite **Reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="994bf-117">Select **Values**.</span></span>
10. <span data-ttu-id="994bf-118">Įveskite šio mokesčio kodo reikšmę stulpelyje **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="994bf-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="994bf-119">Jei „FastTab“ skirtuke **Skaičiavimas** lauke Kilmė pasirinkta Suma pagal vienetą, kad būtų apskaičiuota PVM suma, reikšmė bus padauginta iš operacijos kiekio.</span><span class="sxs-lookup"><span data-stu-id="994bf-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="994bf-120">Jei mokesčio kodas yra ne vienetinis mokestis, reikšmė yra procentinė dalis, taikoma šio mokesčio kodo kilmei, kad būtų apskaičiuota PVM suma.</span><span class="sxs-lookup"><span data-stu-id="994bf-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="994bf-121">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="994bf-121">Select **Save**.</span></span>
12. <span data-ttu-id="994bf-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="994bf-122">Close the page.</span></span>
13. <span data-ttu-id="994bf-123">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="994bf-123">Select **Save**.</span></span>

