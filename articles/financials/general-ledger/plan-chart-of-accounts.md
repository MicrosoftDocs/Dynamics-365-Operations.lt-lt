---
title: "Savo sąskaitų plano sudarymas"
description: "Šiame straipsnyje pateikta informacija, kuri padės jums suplanuoti jūsų organizacijos sąskaitų planą."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="a8af2-103">Savo sąskaitų plano sudarymas</span><span class="sxs-lookup"><span data-stu-id="a8af2-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a8af2-104">Šiame straipsnyje pateikta informacija, kuri padės jums suplanuoti jūsų organizacijos sąskaitų planą.</span><span class="sxs-lookup"><span data-stu-id="a8af2-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="a8af2-105">Norėdami sekti ir prižiūrėti finansinę informaciją organizacijoje, galite nustatyti sąskaitų planą.</span><span class="sxs-lookup"><span data-stu-id="a8af2-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="a8af2-106">Sąskaitų planas yra sąskaitų rinkinys, kuris apibrėžia finansinę sistemą.</span><span class="sxs-lookup"><span data-stu-id="a8af2-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="a8af2-107">Norėdami toliau sekti šių sąskaitų operacijas, galite pridėti segmentus, kurie žinomi kaip finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="a8af2-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="a8af2-108">Pavyzdžiui, išlaidų sąskaita gali apimti finansines dimensijas, pavadintas „Padalinys“, „Išlaidų centras“ ir „Paskirtis“.</span><span class="sxs-lookup"><span data-stu-id="a8af2-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="a8af2-109">Vartotojo nustatytos taisyklės, žinomos kaip sąskaitos struktūros ir išplėstinės taisyklės, nurodo, kaip šios finansinės dimensijos yra susietos su pagrindinėmis sąskaitomis ir kitomis finansinėmis dimensijomis ir kaip įvedamos operacijos.</span><span class="sxs-lookup"><span data-stu-id="a8af2-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="a8af2-110">Sąskaitų planas yra susistemintas juridinio subjekto DK sąskaitų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="a8af2-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="a8af2-111">Sąrašas naudojamas norint parengti finansines ataskaitas institucijoms ir savininkams.</span><span class="sxs-lookup"><span data-stu-id="a8af2-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="a8af2-112">Sąskaitos grupuojamos į sąskaitų tipus, o toliau sujungiamos į didesnes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="a8af2-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="a8af2-113">Žvelgiant bendrai, sąskaitos grupuojamos kaip įplaukos ir išlaidos (operacijų sąskaitos) bei turtas ir įsipareigojimai (balanso sąskaitos).</span><span class="sxs-lookup"><span data-stu-id="a8af2-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="a8af2-114">Sąskaitų planu galima dalintis ir juo naudotis gali bet kuris juridinis subjektas organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="a8af2-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="a8af2-115">Sąskaitų planas, kurį naudoja juridinis subjektas, nurodomas puslapyje **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="a8af2-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="a8af2-116">Toliau pateikiami kai kurie veiksniai, į kuriuos privalote atsižvelgti, kai planuojate savo organizacijos sąskaitų plano struktūrą:</span><span class="sxs-lookup"><span data-stu-id="a8af2-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="a8af2-117">Ataskaitų kūrimo reikalavimai šalyje / regione, kuriame yra jūsų organizacija.</span><span class="sxs-lookup"><span data-stu-id="a8af2-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="a8af2-118">Jūsų juridinio subjekto ataskaitų kūrimo reikalavimai</span><span class="sxs-lookup"><span data-stu-id="a8af2-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="a8af2-119">Išorinėms organizacijoms ir jūsų organizacijai reikalingas specifikacijų laipsnis</span><span class="sxs-lookup"><span data-stu-id="a8af2-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="a8af2-120">Sukurkite sąskaitų planą puslapyje **Sąskaitų planas**.</span><span class="sxs-lookup"><span data-stu-id="a8af2-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="a8af2-121">Pagrindines sąskaitas galima sukurti puslapyje **Sąskaitų planas** arba puslapyje **Pagrindinės sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="a8af2-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="a8af2-122">Pagrindinėse sąskaitose nereikėtų naudoti jokių specialių simbolių, kurie naudojami kaip sąskaitų plano skyrikliai.</span><span class="sxs-lookup"><span data-stu-id="a8af2-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="a8af2-123">Jei turite specialų simbolį, kurs yra toks pats, kaip ir jūsų sąskaitų plano skyriklis, gali kilti nestabilumų arba poreikis visada naudoti peržvalgas arba iškeliamąjį objektą, įvedant sąskaitos ir dimensijų kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="a8af2-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="a8af2-124">Daugiau informacijos žr. [Kurti pagrindinę sąskaitą](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="a8af2-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="a8af2-125">Tikslinga susieti pagrindines sąskaitas su pagrindinių sąskaitų kategorijomis, kad galėtumėte išnaudoti numatytąsias finansines ataskaitas nedarydami jokių modifikacijų.</span><span class="sxs-lookup"><span data-stu-id="a8af2-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="a8af2-126">Todėl jūs galite greičiau ir lengviau kurti ir prižiūrėti ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="a8af2-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="a8af2-127">Naudokite puslapį **Konfigūruoti sąskaitų struktūras**, kad sukurtumėte sąskaitų struktūras.</span><span class="sxs-lookup"><span data-stu-id="a8af2-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="a8af2-128">Sąskaitų struktūros apibrėžia galiojančias kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="a8af2-128">Account structures define valid combinations.</span></span> <span data-ttu-id="a8af2-129">Kombinacijos, kartu su pagrindinėmis sąskaitomis, formuoja sąskaitų planą.</span><span class="sxs-lookup"><span data-stu-id="a8af2-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="a8af2-130">Daugiau informacijos žr. [Kurti sąskaitos struktūrą](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="a8af2-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="a8af2-131">**Juridinio subjekto nepaisymai**</span><span class="sxs-lookup"><span data-stu-id="a8af2-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="a8af2-132">Ne visos pagrindinės sąskaitos tinkamos visiems juridiniams subjektams, o kai kurios gali būti aktualios tik tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="a8af2-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="a8af2-133">Tokiu atveju skyrius „Juridinio subjekto nepaisymas“ gali būti naudojamas nustatyti, kurių įmonių pagrindinė sąskaita turi būti sustabdyta, kas jų savininkas ir kiek laiko dimensija yra aktyvi.</span><span class="sxs-lookup"><span data-stu-id="a8af2-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="a8af2-134">Nepaisymai bendrame lygyje negali būti labiau ribojantys nei nepaisymai juridinio subjekto lygyje.</span><span class="sxs-lookup"><span data-stu-id="a8af2-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="a8af2-135">Daugiau informacijos žr. temose: [Finansinės dimensijos](financial-dimensions.md)
[Kurti ir priskirti išplėstinės taisyklės struktūras](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="a8af2-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>



