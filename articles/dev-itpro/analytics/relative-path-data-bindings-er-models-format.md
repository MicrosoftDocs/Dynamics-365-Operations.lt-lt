---
title: Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6582cca9b912868f88de2770a17cbb6e67328660
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726557"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="a285a-103">Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose</span><span class="sxs-lookup"><span data-stu-id="a285a-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a285a-104">Naudodami elektroninių ataskaitų (ER) įrankį vartotojai gali nustatyti elektroninio formato struktūras ir tada aprašyti, kaip šias struktūras reikia pildyti naudojant „Dynamics 365 for Finance and Operations“ esančius duomenis ir algoritmus.</span><span class="sxs-lookup"><span data-stu-id="a285a-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a285a-105">Daugiau informacijos žr. [Elektroninių ataskaitų (ER) konfigūracijų kūrimas](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="a285a-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="a285a-106">Norėdami nurodyti duomenų srautą, kuriuo bus gaunami „Finance and Operations“ duomenys, ir jį naudoti generuodami elektroninį dokumentą, turite atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a285a-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="a285a-107">Susiekite sukonfigūruotus duomenų šaltinius su konkretaus domeno duomenų modelio elementais.</span><span class="sxs-lookup"><span data-stu-id="a285a-107">Bind configured data sources to elements of the designed domain-specific data model.</span></span> <span data-ttu-id="a285a-108">Modelio struktūra ir pasirinkti duomenų šaltiniai gali būti sudėtingos hierarchinės struktūros dalys.</span><span class="sxs-lookup"><span data-stu-id="a285a-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="a285a-109">Todėl galutinės sąsajos gali būti gana didelės ir jose gali būti daug skirtingų tipų elementų (pavyzdžiui, ryšių, lentelių ir metodų).</span><span class="sxs-lookup"><span data-stu-id="a285a-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="a285a-110">Sąsajas gali tapti sunkiau skaityti ir gana sudėtinga peržiūrėti bei suprasti, ypač ne savininkams.</span><span class="sxs-lookup"><span data-stu-id="a285a-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="a285a-111">Susiekite duomenų modelio elementus su formato komponentais, kad apibrėžtumėte, kokie duomenų modelio duomenys bus automatiškai įvedami generuojant formato išvestis.</span><span class="sxs-lookup"><span data-stu-id="a285a-111">Bind data model elements with format components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="a285a-112">Siekiant patobulinti ER susiejimo kūrimo įrankių naudojimą buvo įdiegta santykinio kelio funkcija.</span><span class="sxs-lookup"><span data-stu-id="a285a-112">To improve usability of ER mapping designers, the relative path feature has been released.</span></span> <span data-ttu-id="a285a-113">Pagal numatytuosius parametrus visuose naujuose „Finance and Operations“ egzemplioriuose, kuriuose yra įgalintos ER kūrimo funkcijos („Microsoft Dynamics 365 for Finance and Operations“, „Microsoft Regulatory Configuration Service“), santykinio kelio rodymo parinktis yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="a285a-113">By default, the relative path representation option is turned on for any new instance of Finance and Operations where ER design experience is enabled (Microsoft Dynamics 365 for Finance and operations, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="a285a-114">Įdiegėme santykinio kelio parametrą, kad vartotojai dirbdami su šia ER sąsajų pateiktimi galėtų naudoti visą kelią.</span><span class="sxs-lookup"><span data-stu-id="a285a-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="a285a-115">[![Vartotojo parametrai](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="a285a-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="a285a-116">Įjungus santykinio kelio naudojimo parametrą, vienas simbolis @ pakeičia pirminio elemento kelią dabartinio modelio elemento sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="a285a-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="a285a-117">Visos sąsajos kelias tampa trumpesnis, todėl visą susiejimą galima aiškiau ir lengviau suprasti.</span><span class="sxs-lookup"><span data-stu-id="a285a-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="a285a-118">Daugeliu atvejų norint peržiūrėti visas duomenų modelio sąsajas nereikia papildomai slinkti.</span><span class="sxs-lookup"><span data-stu-id="a285a-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="a285a-119">[![Modelių susiejimo kūrimo įrankis](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="a285a-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="a285a-120">Pradėjus kurti naują ER išraišką reikia įvesti tik vieną simbolį, norint apibrėžti sąsają su pirminio elemento lauku.</span><span class="sxs-lookup"><span data-stu-id="a285a-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="a285a-121">[![Formulės konstruktorius](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="a285a-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="a285a-122">Jei nusprendžiate pakeisti pirminio modelio elemento duomenų šaltinį, kuriam naudojamas absoliutusis kelias, turite rankiniu būdu iš naujo susieti šį modelio elementą, bei visus įdėtuosius elementus su nauju duomenų šaltiniu.</span><span class="sxs-lookup"><span data-stu-id="a285a-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="a285a-123">Kai santykinio kelio naudojimo funkcija yra įjungta ir jūs pasirenkate naują duomenų šaltinį, kurį reikia susieti su pirminiu elementu, jums pasiūloma pasirinktis automatiškai vienu spustelėjimu iš naujo susieti visus įdėtuosius šio pirminio elemento elementus.</span><span class="sxs-lookup"><span data-stu-id="a285a-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="a285a-124">[![Pranešimas pakeisti esamą kelią](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="a285a-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="a285a-125">Jei patvirtinsite įdėtųjų elementų sąsają, naujas pirminis elementas bus įtrauktas į visų įdėtųjų elementų, kuriuose yra esamas pirminis elementas, kelią.</span><span class="sxs-lookup"><span data-stu-id="a285a-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="a285a-126">Ši funkcija nepažeidžia ER sistemos suderinamumo su ankstesnėmis versijomis.</span><span class="sxs-lookup"><span data-stu-id="a285a-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="a285a-127">Visos anksčiau sukurtos ER konfigūracijos veiks naudojant šią naują funkciją. Jums nereikės atnaujinti versijos arba konvertuoti.</span><span class="sxs-lookup"><span data-stu-id="a285a-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="a285a-128">Visi pakeitimai, įdiegti masiškai modifikuojant įdėtųjų elementų sąsajas modelių susiejimuose, įrašomi konfigūracijos pokytyje (pakeitimų sekimas).</span><span class="sxs-lookup"><span data-stu-id="a285a-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="a285a-129">Tai leidžia klientams pritaikyti išvestinę modelio susiejimo versiją bet kokiai naujai jo pagrindinei versijai, modifikuotai naudojant šią naują funkciją.</span><span class="sxs-lookup"><span data-stu-id="a285a-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>
