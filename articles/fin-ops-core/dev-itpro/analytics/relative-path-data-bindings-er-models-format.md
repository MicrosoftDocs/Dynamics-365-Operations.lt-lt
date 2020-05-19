---
title: Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose
description: Naudodami elektroninių ataskaitų (ER) įrankį vartotojai gali nustatyti elektroninio formato struktūras ir tada aprašyti, kaip šias struktūras reikia pildyti naudojant programoje esančius duomenis ir algoritmus.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c08e81b6e2983a8f16104698944820e93ba3852d
ms.sourcegitcommit: 139c8007e68d279d7ca9aa302598217522abb8cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331329"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="6497d-103">Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose</span><span class="sxs-lookup"><span data-stu-id="6497d-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6497d-104">Naudodami elektroninių ataskaitų (ER) įrankį vartotojai gali nustatyti elektroninio formato struktūras ir tada aprašyti, kaip šias struktūras reikia pildyti naudojant programoje esančius duomenis ir algoritmus.</span><span class="sxs-lookup"><span data-stu-id="6497d-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="6497d-105">Daugiau informacijos žr. [Elektroninių ataskaitų (ER) konfigūracijų kūrimas](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="6497d-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="6497d-106">Norėdami nurodyti duomenų srautą, kuriuo bus gaunami „Finance and Operations“ duomenys, ir jį naudoti generuodami elektroninį dokumentą, turite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6497d-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="6497d-107">Susiekite sukonfigūruotus duomenų šaltinius su konkretaus domeno [duomenų modelio](general-electronic-reporting.md#data-model-and-model-mapping-components) elementais.</span><span class="sxs-lookup"><span data-stu-id="6497d-107">Bind configured data sources to elements of the designed domain-specific [data model](general-electronic-reporting.md#data-model-and-model-mapping-components).</span></span> <span data-ttu-id="6497d-108">Modelio struktūra ir pasirinkti duomenų šaltiniai gali būti sudėtingos hierarchinės struktūros dalys.</span><span class="sxs-lookup"><span data-stu-id="6497d-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="6497d-109">Todėl galutinės sąsajos gali būti gana didelės ir jose gali būti daug skirtingų tipų elementų (pavyzdžiui, ryšių, lentelių ir metodų).</span><span class="sxs-lookup"><span data-stu-id="6497d-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="6497d-110">Sąsajas gali tapti sunkiau skaityti ir gana sudėtinga peržiūrėti bei suprasti, ypač ne savininkams.</span><span class="sxs-lookup"><span data-stu-id="6497d-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="6497d-111">Susiekite duomenų modelio elementus su [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentais, kad apibrėžtumėte, kokie duomenų modelio duomenys bus automatiškai įvedami generuojant formato išvestis.</span><span class="sxs-lookup"><span data-stu-id="6497d-111">Bind data model elements with [format](general-electronic-reporting.md#FormatComponentOutbound) components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="6497d-112">Siekiant patobulinti ER susiejimo kūrimo įrankių naudojimą buvo įdiegta [santykinio kelio](er-formula-language.md#relative-path) funkcija.</span><span class="sxs-lookup"><span data-stu-id="6497d-112">To improve usability of ER mapping designers, the [relative path](er-formula-language.md#relative-path) feature has been released.</span></span> <span data-ttu-id="6497d-113">Pagal numatytuosius parametrus visuose naujuose programos egzemplioriuose, kuriuose yra įgalintos ER kūrimo funkcijos („Microsoft“ „Dynamics 365 Finance“, „Microsoft Regulatory Configuration Service“), santykinio kelio rodymo parinktis yra įjungta.</span><span class="sxs-lookup"><span data-stu-id="6497d-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="6497d-114">Įdiegėme santykinio kelio parametrą, kad vartotojai dirbdami su šia ER sąsajų pateiktimi galėtų naudoti visą kelią.</span><span class="sxs-lookup"><span data-stu-id="6497d-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="6497d-115">[![Vartotojo parametrai](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="6497d-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="6497d-116">Įjungus santykinio kelio naudojimo parametrą, vienas simbolis @ pakeičia pirminio elemento kelią dabartinio modelio elemento sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="6497d-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="6497d-117">Visos sąsajos kelias tampa trumpesnis, todėl visą susiejimą galima aiškiau ir lengviau suprasti.</span><span class="sxs-lookup"><span data-stu-id="6497d-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="6497d-118">Daugeliu atvejų norint peržiūrėti visas duomenų modelio sąsajas nereikia papildomai slinkti.</span><span class="sxs-lookup"><span data-stu-id="6497d-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="6497d-119">[![Modelių susiejimo kūrimo įrankis](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="6497d-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="6497d-120">Pradėjus kurti naują ER išraišką reikia įvesti tik vieną simbolį, norint apibrėžti sąsają su pirminio elemento lauku.</span><span class="sxs-lookup"><span data-stu-id="6497d-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="6497d-121">[![Formulės konstruktorius](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="6497d-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="6497d-122">Jei nusprendžiate pakeisti pirminio modelio elemento duomenų šaltinį, kuriam naudojamas absoliutusis kelias, turite rankiniu būdu iš naujo susieti šį modelio elementą, bei visus įdėtuosius elementus su nauju duomenų šaltiniu.</span><span class="sxs-lookup"><span data-stu-id="6497d-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="6497d-123">Kai santykinio kelio naudojimo funkcija yra įjungta ir jūs pasirenkate naują duomenų šaltinį, kurį reikia susieti su pirminiu elementu, jums pasiūloma pasirinktis automatiškai vienu spustelėjimu iš naujo susieti visus įdėtuosius šio pirminio elemento elementus.</span><span class="sxs-lookup"><span data-stu-id="6497d-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="6497d-124">[![Pranešimas pakeisti esamą kelią](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="6497d-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="6497d-125">Jei patvirtinsite įdėtųjų elementų sąsają, naujas pirminis elementas bus įtrauktas į visų įdėtųjų elementų, kuriuose yra esamas pirminis elementas, kelią.</span><span class="sxs-lookup"><span data-stu-id="6497d-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="6497d-126">Ši funkcija nepažeidžia ER sistemos suderinamumo su ankstesnėmis versijomis.</span><span class="sxs-lookup"><span data-stu-id="6497d-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="6497d-127">Visos anksčiau sukurtos ER konfigūracijos veiks naudojant šią naują funkciją. Jums nereikės atnaujinti versijos arba konvertuoti.</span><span class="sxs-lookup"><span data-stu-id="6497d-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="6497d-128">Visi pakeitimai, įdiegti masiškai modifikuojant įdėtųjų elementų sąsajas modelių susiejimuose, įrašomi konfigūracijos pokytyje (pakeitimų sekimas).</span><span class="sxs-lookup"><span data-stu-id="6497d-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="6497d-129">Tai leidžia klientams pritaikyti išvestinę modelio susiejimo versiją bet kokiai naujai jo pagrindinei versijai, modifikuotai naudojant šią naują funkciją.</span><span class="sxs-lookup"><span data-stu-id="6497d-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6497d-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6497d-130">Additional resources</span></span>

[<span data-ttu-id="6497d-131">ER formulės kalba</span><span class="sxs-lookup"><span data-stu-id="6497d-131">ER formula language</span></span>](er-formula-language.md)
