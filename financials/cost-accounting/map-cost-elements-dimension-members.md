---
title: "Savikainos elemento dimensijos narių susiejimas į bendrą dimensijos narių rinkinį"
description: "Susiedami skirtingus savikainos elemento dimensijos narius su bendruoju savikainos elemento dimensijos narių rinkiniu jūs suliejate duomenis į bendrąjį analizės tikslais naudojamą formatą."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 9e13fc9fa7e51a1299ca8698f581de979b680a7b
ms.openlocfilehash: b15e251410937ff4f85ecdfaa55ca1a998d1d1ac
ms.contentlocale: lt-lt
ms.lasthandoff: 09/18/2017

---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="af3f8-103">Savikainos elemento dimensijos narių susiejimas į bendrą dimensijos narių rinkinį</span><span class="sxs-lookup"><span data-stu-id="af3f8-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="af3f8-104">Susiedami skirtingus savikainos elemento dimensijos narius su bendruoju savikainos elemento dimensijos narių rinkiniu jūs suliejate duomenis į bendrąjį analizės tikslais naudojamą formatą.</span><span class="sxs-lookup"><span data-stu-id="af3f8-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="af3f8-105">Jeigu esate pasaulinė įmonė ir atitinkate nustatytus apskaitos reikalavimus, galite naudoti kelis sąskaitų planus.</span><span class="sxs-lookup"><span data-stu-id="af3f8-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="af3f8-106">Importuodami savikainos elemento dimensijos narius iš skirtingų sąskaitų planų galite gauti sąskaitų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="af3f8-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="af3f8-107">Tačiau šios sąskaitos iš tiesų gali būti to paties pobūdžio ir jūs ko gero norėsite jas analizuoti ir paskirstyti joms savikainą naudodami bendrąjį formatą.</span><span class="sxs-lookup"><span data-stu-id="af3f8-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="af3f8-108">Susieti savikainos elemento dimensijos narius su bendruoju formatu</span><span class="sxs-lookup"><span data-stu-id="af3f8-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="af3f8-109">Toliau pateikiamame pavyzdyje nurodoma, kaip jūs, kadangi esate savikainos valdytojas, savikainos apskaitoje galite sukurti naują savikainos elemento dimensiją, kurią naudojant savikainos elemento dimensijos nariai iš JAV sąskaitų plano struktūros ir Prancūzijos sąskaitų plano struktūros susiejami su bendruoju savikainos elemento dimensijos narių rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="af3f8-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="af3f8-110">Po to naudodami bendrąjį savikainos elemento dimensijos narių rinkinį galite analizuoti savikainos apskaitos didžiojoje knygoje pateiktus savikainos duomenis iš šių dviejų juridinių subjektų.</span><span class="sxs-lookup"><span data-stu-id="af3f8-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="af3f8-111">Šaltinis: JAV sąskaitų planas</span><span class="sxs-lookup"><span data-stu-id="af3f8-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="af3f8-112">Šaltinis: Prancūzijos sąskaitų planas</span><span class="sxs-lookup"><span data-stu-id="af3f8-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="af3f8-113">Naujas bendrasis savikainos elemento dimensijos narių rinkinys</span><span class="sxs-lookup"><span data-stu-id="af3f8-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="af3f8-114">Savikainos elemento dimensijos nariai importuoti iš JAV sąskaitų plano</span><span class="sxs-lookup"><span data-stu-id="af3f8-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="af3f8-115">Savikainos elemento dimensijos nariai importuoti iš Prancūzijos sąskaitų plano</span><span class="sxs-lookup"><span data-stu-id="af3f8-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="af3f8-116">JAV ir Prancūzijos savikainos elemento dimensijos narių susiejimas su bendruoju rinkiniu</span><span class="sxs-lookup"><span data-stu-id="af3f8-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="af3f8-117">5001: Pardavimai</span><span class="sxs-lookup"><span data-stu-id="af3f8-117">5001: Sales</span></span>                                                           | <span data-ttu-id="af3f8-118">5001: Pardavimai ir reklama</span><span class="sxs-lookup"><span data-stu-id="af3f8-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="af3f8-119">5000: Pardavimai ir reklama</span><span class="sxs-lookup"><span data-stu-id="af3f8-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="af3f8-120">5030: Reklama</span><span class="sxs-lookup"><span data-stu-id="af3f8-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="af3f8-121">6390: atsargų pirkimas\*</span><span class="sxs-lookup"><span data-stu-id="af3f8-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="af3f8-122">7000: Valymo išlaidos</span><span class="sxs-lookup"><span data-stu-id="af3f8-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="af3f8-123">7001: Valymo išlaidos</span><span class="sxs-lookup"><span data-stu-id="af3f8-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="af3f8-124">7001: Kelionės išlaidos</span><span class="sxs-lookup"><span data-stu-id="af3f8-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="af3f8-125">7001: Kelionės išlaidos</span><span class="sxs-lookup"><span data-stu-id="af3f8-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="af3f8-126">\*Atsargų pirkimo Prancūzijos savikainos elemento dimensijos narys nesusietas.</span><span class="sxs-lookup"><span data-stu-id="af3f8-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="af3f8-127">Valiutos konvertavimas</span><span class="sxs-lookup"><span data-stu-id="af3f8-127">Currency conversion</span></span>
<span data-ttu-id="af3f8-128">Įvairūs jūsų naudojami sąskaitų planai gali būti nustatyti naudoti skirtingas valiutas.</span><span class="sxs-lookup"><span data-stu-id="af3f8-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="af3f8-129">Šiuo atveju būtinai nurodykite valiutos keitimo kursą, kad savikainos duomenys būtų apdorojami naudojant teisingą valiutą, nurodytą savikainos apskaitos didžiojoje knygoje, kurioje naudojami savikainos elemento dimensijos nariai.</span><span class="sxs-lookup"><span data-stu-id="af3f8-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="af3f8-130">Kaip nurodoma pirmiau pateiktame pavyzdyje, jeigu savikainos apskaitos didžiojoje knygoje naudojami JAV doleriai (USD), norėdami apdoroti susietų savikainos elemento dimensijos narių operacijas turite sukurti valiutos konvertavimą iš USD į eurus (EUR).</span><span class="sxs-lookup"><span data-stu-id="af3f8-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="af3f8-131">Naujinti susiejimus bet kuriuo metu</span><span class="sxs-lookup"><span data-stu-id="af3f8-131">Update mappings at any time</span></span>
<span data-ttu-id="af3f8-132">Savikainos elemento dimensijos susiejimo apibrėžimus galite atnaujinti bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="af3f8-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="af3f8-133">Kadangi susiejimai įsigalioja ne nuo tam tikros datos, pakeitimai taikomi kitą kartą apdorojant savikainos operacijas arba atliekant savikainos skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="af3f8-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>




