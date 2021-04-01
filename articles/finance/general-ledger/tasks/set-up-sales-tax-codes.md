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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 594e8f0595ecace748a70860c1ccacaf90b7d279
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222196"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="935f8-103">PVM kodų nustatymas</span><span class="sxs-lookup"><span data-stu-id="935f8-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="935f8-104">Šioje temoje paaiškinama, kaip nustatyti PVM kodus.</span><span class="sxs-lookup"><span data-stu-id="935f8-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="935f8-105">PVM kodai sukurti kiekvienam netiesioginiam mokesčiui ar muitui, kuriuos juridinis subjektas yra įsipareigojęs skaičiuoti, rinkti ir mokėti PVM institucijoms.</span><span class="sxs-lookup"><span data-stu-id="935f8-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="935f8-106">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="935f8-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="935f8-107">Pasirinkite **Mokestis > Netiesioginiai mokesčiai > PVM > PVM kodai**.</span><span class="sxs-lookup"><span data-stu-id="935f8-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="935f8-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="935f8-108">Select **New**.</span></span>
3. <span data-ttu-id="935f8-109">Lauke **PVM kodas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="935f8-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="935f8-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="935f8-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="935f8-111">Pasirinkite **Sudengimo laikotarpis**, kad nurodytumėte, kuriai PVM institucijai ir kuriais intervalais reikia pranešti apie šį PVM ir jį mokėti.</span><span class="sxs-lookup"><span data-stu-id="935f8-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="935f8-112">Pasirinkite **DK registravimo grupė**, kad nurodytumėte pagrindines sąskaitas, kuriose į DK registruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="935f8-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="935f8-113">Išplėskite „FastTab“ skirtuką **Skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="935f8-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="935f8-114">Jis apima kelis laukus, kurie kontroliuoja, kaip bus apskaičiuojamos PVM sumos.</span><span class="sxs-lookup"><span data-stu-id="935f8-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="935f8-115">Tinkamai užpildykite šiuos laukelius.</span><span class="sxs-lookup"><span data-stu-id="935f8-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="935f8-116">Sąsajos viršutinėje dalyje **Veiksmų sritis** pasirinkite **PVM kodas**.</span><span class="sxs-lookup"><span data-stu-id="935f8-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="935f8-117">Pasirinkite **Reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="935f8-117">Select **Values**.</span></span>
10. <span data-ttu-id="935f8-118">Įveskite šio mokesčio kodo reikšmę stulpelyje **Reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="935f8-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="935f8-119">Jei „FastTab“ skirtuke **Skaičiavimas** lauke Kilmė pasirinkta Suma pagal vienetą, kad būtų apskaičiuota PVM suma, reikšmė bus padauginta iš operacijos kiekio.</span><span class="sxs-lookup"><span data-stu-id="935f8-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="935f8-120">Jei mokesčio kodas yra ne vienetinis mokestis, reikšmė yra procentinė dalis, taikoma šio mokesčio kodo kilmei, kad būtų apskaičiuota PVM suma.</span><span class="sxs-lookup"><span data-stu-id="935f8-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="935f8-121">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="935f8-121">Select **Save**.</span></span>
12. <span data-ttu-id="935f8-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="935f8-122">Close the page.</span></span>
13. <span data-ttu-id="935f8-123">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="935f8-123">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]