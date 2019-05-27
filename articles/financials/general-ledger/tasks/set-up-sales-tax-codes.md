---
title: Nustatyti PVM kodus
description: PVM kodai sukurti kiekvienam netiesioginiam mokesčiui ar muitui, kuriuos juridinis subjektas yra įsipareigojęs skaičiuoti, rinkti ir mokėti PVM institucijoms.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571588"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="ddfda-103">Nustatyti PVM kodus</span><span class="sxs-lookup"><span data-stu-id="ddfda-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ddfda-104">PVM kodai sukurti kiekvienam netiesioginiam mokesčiui ar muitui, kuriuos juridinis subjektas yra įsipareigojęs skaičiuoti, rinkti ir mokėti PVM institucijoms.</span><span class="sxs-lookup"><span data-stu-id="ddfda-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="ddfda-105">Šioje užduotyje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="ddfda-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="ddfda-106">Pasirinkite Mokestis > Netiesioginiai mokesčiai > PVM > PVM kodai.</span><span class="sxs-lookup"><span data-stu-id="ddfda-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="ddfda-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ddfda-107">Click New.</span></span>
3. <span data-ttu-id="ddfda-108">Lauke PVM kodas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ddfda-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="ddfda-109">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ddfda-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ddfda-110">Pasirinkite Sudengimo laikotarpis, kad nurodytumėte, kuriai PVM institucijai ir kuriais intervalais reikia pranešti apie šį PVM ir jį mokėti.</span><span class="sxs-lookup"><span data-stu-id="ddfda-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="ddfda-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ddfda-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ddfda-112">Pasirinkite DK registravimo grupė, kad nurodytumėte pagrindines sąskaitas, kuriose į DK registruoti PVM.</span><span class="sxs-lookup"><span data-stu-id="ddfda-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="ddfda-113">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ddfda-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ddfda-114">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ddfda-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ddfda-115">Išplėskite „FastTab‟ Skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="ddfda-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="ddfda-116">„FastTab‟ Skaičiavimas yra keli laukai, kurie kontroliuoja, kaip bus apskaičiuojamos PVM sumos.</span><span class="sxs-lookup"><span data-stu-id="ddfda-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="ddfda-117">Veiksmų srityje spustelėkite PVM kodas.</span><span class="sxs-lookup"><span data-stu-id="ddfda-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="ddfda-118">Spustelėkite Reikšmės.</span><span class="sxs-lookup"><span data-stu-id="ddfda-118">Click Values.</span></span>
13. <span data-ttu-id="ddfda-119">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ddfda-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="ddfda-120">Įveskite šio mokesčio kodo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ddfda-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="ddfda-121">Jei „FastTab‟ Skaičiavimas, lauke Kilmė pasirinkta Suma pagal vienetą, kad būtų apskaičiuota PVM suma, reikšmė bus padauginta iš operacijos kiekio.</span><span class="sxs-lookup"><span data-stu-id="ddfda-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="ddfda-122">Jei mokesčio kodas yra ne vienetinis mokestis, reikšmė yra procentinė dalis, taikoma šio mokesčio kodo kilmei, kad būtų apskaičiuota PVM suma.</span><span class="sxs-lookup"><span data-stu-id="ddfda-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="ddfda-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ddfda-123">Click Save.</span></span>
16. <span data-ttu-id="ddfda-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ddfda-124">Close the page.</span></span>
17. <span data-ttu-id="ddfda-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ddfda-125">Click Save.</span></span>

