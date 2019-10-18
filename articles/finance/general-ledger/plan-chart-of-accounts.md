---
title: Sąskaitų plano rengimas
description: Šioje temoje pateikta informacija, kuri padės jums suplanuoti jūsų organizacijos sąskaitų planą.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 007b634c18ce897160aea38e05c9a73a64dd3917
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186376"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="b5413-103">Sąskaitų plano rengimas</span><span class="sxs-lookup"><span data-stu-id="b5413-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5413-104">Šioje temoje pateikta informacija, kuri padės jums suplanuoti jūsų organizacijos sąskaitų planą.</span><span class="sxs-lookup"><span data-stu-id="b5413-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="b5413-105">Norėdami sekti ir prižiūrėti finansinę informaciją organizacijoje, galite nustatyti sąskaitų planą.</span><span class="sxs-lookup"><span data-stu-id="b5413-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="b5413-106">Sąskaitų planas yra sąskaitų rinkinys, kuris apibrėžia finansinę sistemą.</span><span class="sxs-lookup"><span data-stu-id="b5413-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="b5413-107">Norėdami toliau sekti šių sąskaitų operacijas, galite pridėti segmentus.</span><span class="sxs-lookup"><span data-stu-id="b5413-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="b5413-108">Šie segmentai vadinami finansinėmis dimensijomis.</span><span class="sxs-lookup"><span data-stu-id="b5413-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="b5413-109">Pavyzdžiui, išlaidų sąskaita gali apimti finansines dimensijas, pavadintas „Padalinys“, „Išlaidų centras“ ir „Paskirtis“.</span><span class="sxs-lookup"><span data-stu-id="b5413-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="b5413-110">Vartotojo nustatytos taisyklės nurodo, kaip šios finansinės dimensijos yra susietos su pagrindinėmis sąskaitomis ir kitomis finansinėmis dimensijomis ir kaip įvedamos operacijos.</span><span class="sxs-lookup"><span data-stu-id="b5413-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="b5413-111">Šios vartotojo nustatytos taisyklės žinomos kaip sąskaitos struktūros ir išplėstinės taisyklės.</span><span class="sxs-lookup"><span data-stu-id="b5413-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="b5413-112">Sąskaitų planas yra susistemintas juridinio subjekto DK sąskaitų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="b5413-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="b5413-113">Sąrašas naudojamas norint parengti finansines ataskaitas institucijoms ir savininkams.</span><span class="sxs-lookup"><span data-stu-id="b5413-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="b5413-114">Pirmiausia sąskaitos grupuojamos į sąskaitų tipus, o tada sujungiamos į didesnes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="b5413-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="b5413-115">Žvelgiant bendrai, sąskaitos grupuojamos kaip įplaukos ir išlaidos (operacijų sąskaitos) bei turtas ir įsipareigojimai (balanso sąskaitos).</span><span class="sxs-lookup"><span data-stu-id="b5413-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="b5413-116">Sąskaitų planu galima dalintis ir juo naudotis gali bet kuris juridinis subjektas organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="b5413-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="b5413-117">Sąskaitų planas, kurį naudoja juridinis subjektas, nurodomas puslapyje **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="b5413-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="b5413-118">Toliau pateikiami kai kurie veiksniai, į kuriuos privalote atsižvelgti, kai planuojate savo organizacijos sąskaitų plano struktūrą:</span><span class="sxs-lookup"><span data-stu-id="b5413-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="b5413-119">Ataskaitų kūrimo reikalavimai šalyje arba regione, kuriame yra jūsų organizacija.</span><span class="sxs-lookup"><span data-stu-id="b5413-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="b5413-120">Jūsų juridinio subjekto ataskaitų kūrimo reikalavimai</span><span class="sxs-lookup"><span data-stu-id="b5413-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="b5413-121">Išorinėms organizacijoms ir jūsų organizacijai reikalingas specifikacijų laipsnis</span><span class="sxs-lookup"><span data-stu-id="b5413-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="b5413-122">Kurkite sąskaitų planą puslapyje **Sąskaitų planas**.</span><span class="sxs-lookup"><span data-stu-id="b5413-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="b5413-123">Galite kurti pagrindines sąskaitas puslapyje **Sąskaitų planas** arba puslapyje **Pagrindinės sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="b5413-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="b5413-124">Pagrindinėse sąskaitose nereikėtų naudoti jokių specialių simbolių, kurie naudojami kaip sąskaitų plano skyrikliai.</span><span class="sxs-lookup"><span data-stu-id="b5413-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="b5413-125">Kitu atveju gali kilti nestabilumų arba poreikis visada naudoti peržvalgas arba dialogo langą, įvedant sąskaitos ir dimensijų kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="b5413-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="b5413-126">Daugiau informacijos žr. [Kurti pagrindinę sąskaitą](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="b5413-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b5413-127">„Dynamics 365 for Finance and Operations“ 8.0 versijoje (2018 m. balandžio mėn.) galite modifikuoti sąskaitų plano skyriklį iš puslapio **DK parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b5413-127">In Dynamics 365 for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="b5413-128">Tikslinga susieti pagrindines sąskaitas su pagrindinių sąskaitų kategorijomis, kad galėtumėte išnaudoti numatytąsias finansines ataskaitas nedarydami jokių modifikacijų.</span><span class="sxs-lookup"><span data-stu-id="b5413-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="b5413-129">Todėl jūs galite greičiau ir lengviau kurti ir prižiūrėti ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="b5413-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="b5413-130">Naudokite puslapį **Sąskaitų struktūrų konfigūravimas**, kad sukurtumėte sąskaitų struktūras.</span><span class="sxs-lookup"><span data-stu-id="b5413-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="b5413-131">Sąskaitų struktūros apibrėžia galiojančias kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="b5413-131">Account structures define valid combinations.</span></span> <span data-ttu-id="b5413-132">Šios kombinacijos, kartu su pagrindinėmis sąskaitomis, formuoja sąskaitų planą.</span><span class="sxs-lookup"><span data-stu-id="b5413-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="b5413-133">Daugiau informacijos žr. [Kurti sąskaitos struktūrą](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="b5413-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="b5413-134">**Juridinio subjekto nepaisymai**</span><span class="sxs-lookup"><span data-stu-id="b5413-134">**Legal entity overrides**</span></span>

<span data-ttu-id="b5413-135">Ne visos pagrindinės sąskaitos tinkamos visiems juridiniams subjektams, o kai kurios pagrindinės sąskaitos gali būti aktualios tik tam tikrą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="b5413-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="b5413-136">Tokiais atvejais skiltį **Juridinio subjekto nepaisymas** galite naudoti norėdami nustatyti, kuriose įmonėse pagrindinės sąskaitos turi būti sustabdytos, kas jų savininkas ir kurį laikotarpį dimensija yra aktyvi.</span><span class="sxs-lookup"><span data-stu-id="b5413-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="b5413-137">Nepaisymai bendrame lygyje negali būti labiau ribojantys nei nepaisymai juridinio subjekto lygyje.</span><span class="sxs-lookup"><span data-stu-id="b5413-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="b5413-138">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="b5413-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b5413-139">Finansinės dimensijos</span><span class="sxs-lookup"><span data-stu-id="b5413-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="b5413-140">Kurti ir priskirti išplėstinės taisyklės struktūras</span><span class="sxs-lookup"><span data-stu-id="b5413-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)
