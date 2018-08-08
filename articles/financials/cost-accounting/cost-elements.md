---
title: Savikainos elemento dimensijos
description: "Kaip vienas iš pagrindinių ramsčių savikainos apskaitoje norint kategorizuoti ir sekti išlaidų srautą naudojamos savikainos elemento dimensijos."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: c703d1a9ae36d4342dc652d70dd82379187057c1
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="cost-element-dimensions"></a><span data-ttu-id="3774c-103">Savikainos elemento dimensijos</span><span class="sxs-lookup"><span data-stu-id="3774c-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3774c-104">Kaip vienas iš pagrindinių ramsčių savikainos apskaitoje norint kategorizuoti ir sekti išlaidų srautą naudojamos savikainos elemento dimensijos.</span><span class="sxs-lookup"><span data-stu-id="3774c-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="3774c-105">Savikainos elementas sąskaitų plane atitinka su savikaina susijusį elementą.</span><span class="sxs-lookup"><span data-stu-id="3774c-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="3774c-106">Iš esmės jis gali būti bet kokio tipo žemiausio verslo lygio elementas, į kurį gali būti nukreiptas išlaidų srautas.</span><span class="sxs-lookup"><span data-stu-id="3774c-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="3774c-107">Savikainos elementai kaip sąvokos intervalas nuo DK sąskaitų iki visų su savikaina susijusių išteklių.</span><span class="sxs-lookup"><span data-stu-id="3774c-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="3774c-108">Šiuo metu išlaidų apskaita palaiko DK sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="3774c-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="3774c-109">Dviejų tipų savikainos elementai</span><span class="sxs-lookup"><span data-stu-id="3774c-109">Two types of cost elements</span></span>
<span data-ttu-id="3774c-110">Yra dviejų tipų savikainos elementai: pirminiai savikainos elementai ir antriniai savikainos elementai.</span><span class="sxs-lookup"><span data-stu-id="3774c-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="3774c-111">Toliau pateikiamoje lentelėje aprašomi šių dviejų tipų skirtumai.</span><span class="sxs-lookup"><span data-stu-id="3774c-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3774c-112"><strong>Pirminiai savikainos elementai</strong></span><span class="sxs-lookup"><span data-stu-id="3774c-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="3774c-113"><strong>Antriniai savikainos elementai</strong></span><span class="sxs-lookup"><span data-stu-id="3774c-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3774c-114">Pirminiai savikainos elementai atitinka išlaidų srautą iš finansinės apskaitos į išlaidų apskaitą.</span><span class="sxs-lookup"><span data-stu-id="3774c-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="3774c-115">Savikainos elemento struktūra atitinka pelno ir nuostolio sąskaitos struktūrą didžiojoje knygoje, kai savikainos elementas gali atitikti pagrindinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="3774c-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="3774c-116">Ne visos pagrindinės sąskaitos būtinai turi būti pateikiamos kaip savikainos elementai priklausomai nuo verslo poreikių.</span><span class="sxs-lookup"><span data-stu-id="3774c-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="3774c-117">Pirminių savikainos elementų pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="3774c-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="3774c-118">Parduotų prekių savikaina (COG)</span><span class="sxs-lookup"><span data-stu-id="3774c-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="3774c-119">Netiesioginės medžiagų išlaidos</span><span class="sxs-lookup"><span data-stu-id="3774c-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="3774c-120">Personalo išlaidos</span><span class="sxs-lookup"><span data-stu-id="3774c-120">Personnel costs</span></span></li>
<li><span data-ttu-id="3774c-121">Energijos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3774c-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="3774c-122">Antriniai savikainos elementai atitinka vidinių išlaidų srautą, nes šios išlaidos sukurtos ir naudojamos tik savikainos apskaitoje.</span><span class="sxs-lookup"><span data-stu-id="3774c-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="3774c-123">Jie naudojami norint užtikrinti, kad būtų galima atsekti išlaidų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="3774c-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="3774c-124">Šie savikainos elementai naudojami savikainos paskirstymuose ir skaičiuojant papildomas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="3774c-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="3774c-125">Antrinių savikainos elementų pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="3774c-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="3774c-126">Gamybos išlaidos</span><span class="sxs-lookup"><span data-stu-id="3774c-126">Production costs</span></span></li>
<li><span data-ttu-id="3774c-127">Pridėtinės išlaidos už gamybą, medžiagas ir rinkodarą</span><span class="sxs-lookup"><span data-stu-id="3774c-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="3774c-128">Savikainos elemento dimensijos ir savikainos elemento dimensijos nariai</span><span class="sxs-lookup"><span data-stu-id="3774c-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="3774c-129">Savikainos elementai vadinami *savikainos elemento dimensijos*.</span><span class="sxs-lookup"><span data-stu-id="3774c-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="3774c-130">Atskiros dimensijos vertės vadinamos *savikainos elemento dimensijos nariai*.</span><span class="sxs-lookup"><span data-stu-id="3774c-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="3774c-131">Pavyzdžiui, jūs turite JAV sąskaitų plano struktūrą (COA), kuri yra jūsų privalomųjų ataskaitų pagrindas.</span><span class="sxs-lookup"><span data-stu-id="3774c-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="3774c-132">Ši COA naudojama kaip savikainos elemento dimensija.</span><span class="sxs-lookup"><span data-stu-id="3774c-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="3774c-133">Sąskaitas, kurios yra pirminiai savikainos elementai, savikainos apskaitoje atitinka savikainos elemento dimensijos nariai.</span><span class="sxs-lookup"><span data-stu-id="3774c-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="3774c-134">Toliau pateikiamoje ekrano nuotraukoje pavaizduotas pagrindinių sąskaitų pavyzdys, kai pagrindinės sąskaitos yra savikainos elemento dimensija su savo faktinėmis pagrindinėmis sąskaitomis, kurios yra savikainos elemento dimensijos nariai.</span><span class="sxs-lookup"><span data-stu-id="3774c-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="3774c-135">[![savikainos elemento dimensijos](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="3774c-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="3774c-136">Savikainos elemento dimensijos narių importavimas naudojant duomenų jungtis</span><span class="sxs-lookup"><span data-stu-id="3774c-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="3774c-137">Norėdami supaprastinti savikainos apskaitos savikainos elemento dimensijos narius, kad galėtumėte gauti pirminės savikainos elementus iš vienos ar kelių šaltinio sistemų, galite naudoti iš anksto parengtas duomenų jungtis arba savo pasirinktas jungtis.</span><span class="sxs-lookup"><span data-stu-id="3774c-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="3774c-138">Diegimo aplinkybės</span><span class="sxs-lookup"><span data-stu-id="3774c-138">Implementation considerations</span></span>
<span data-ttu-id="3774c-139">Kadangi savikainos elementai atitinka žemiausią savikainos informacijos lygį, diegdami savikainos elementų struktūrą turėtumėte įsitikinti, kad pateikti visi savikainos elementai, kurių reikia norint paruošti vadovybės ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="3774c-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="3774c-140">Gali būti sunku rasti išlaidų kontrolei tinkantį išlaidų elementų skaičių.</span><span class="sxs-lookup"><span data-stu-id="3774c-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="3774c-141">Turint tūkstančius išlaidų elementų gali būti sunku valdyti kiekvieną išlaidų elementą atskirai.</span><span class="sxs-lookup"><span data-stu-id="3774c-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="3774c-142">Arba galite grupuoti išlaidų elementus ir valdyti išlaidų kontrolę sudėtiniu lygmeniu.</span><span class="sxs-lookup"><span data-stu-id="3774c-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>




