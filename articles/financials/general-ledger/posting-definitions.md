---
title: "Registravimo aprašai"
description: "Šiame straipsnyje pateikta informacija apie registravimo aprašus ir kaip juos nustatyti ir susieti. Palaikomiems registravimo tipams ir dokumentams galite naudoti registravimo aprašus vietoj registravimo šablonų, kad klasifikuotumėte pagrindines sąskaitas ir finansines dimensijas apskaitos įrašuose."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0148bd65bad2b5c947287d18289c08c7ef7f476f
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="posting-definitions"></a><span data-ttu-id="09094-104">Registravimo aprašai</span><span class="sxs-lookup"><span data-stu-id="09094-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09094-105">Šiame straipsnyje pateikta informacija apie registravimo aprašus ir kaip juos nustatyti ir susieti.</span><span class="sxs-lookup"><span data-stu-id="09094-105">This article provides information about posting definitions, and how to define and link them.</span></span> <span data-ttu-id="09094-106">Palaikomiems registravimo tipams ir dokumentams galite naudoti registravimo aprašus vietoj registravimo šablonų, kad klasifikuotumėte pagrindines sąskaitas ir finansines dimensijas apskaitos įrašuose.</span><span class="sxs-lookup"><span data-stu-id="09094-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span>

<span data-ttu-id="09094-107">Palaikomiems registravimo tipams ir dokumentams galite naudoti registravimo aprašus vietoj registravimo šablonų, kad klasifikuotumėte pagrindines sąskaitas ir finansines dimensijas apskaitos įrašuose.</span><span class="sxs-lookup"><span data-stu-id="09094-107">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="09094-108">Galite peržiūrėti palaikomus dokumentus ir registravimo tipus puslapyje **Operacijų registravimo aprašai**.</span><span class="sxs-lookup"><span data-stu-id="09094-108">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="09094-109">Norėdami pradėti naudoti registravimo aprašus, pasirinkite parinktį**Naudoti registravimo aprašus** puslapyje **DK parametrai**.</span><span class="sxs-lookup"><span data-stu-id="09094-109">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="09094-110">Net kai naudojate registravimo aprašus, turite dar nustatyti pradinių įrašų ir nepalaikomų registravimo tipų bei dokumentų registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="09094-110">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="09094-111">Naudokite registravimo aprašus norėdami įjungti pirkimo užsakymų biudžeto rezervavimo apskaitą ir pirkimo paraiškų preliminaraus biudžeto rezervavimo apskaitą.</span><span class="sxs-lookup"><span data-stu-id="09094-111">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="09094-112">Registravimo aprašų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="09094-112">Defining posting definitions</span></span>
<span data-ttu-id="09094-113">Naudokite puslapį**Registravimo aprašai**, kad nurodytumėte gretinimo kriterijus ir apibrėžtumėte įrašus, kurie turėtų būti sugeneruoti įvykus sugretinimui.</span><span class="sxs-lookup"><span data-stu-id="09094-113">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="09094-114">Pradinių įrašų gretinimo kriterijai įvertinami kaip apskaitos paskirstymai.</span><span class="sxs-lookup"><span data-stu-id="09094-114">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="09094-115">Puslapyje **Registravimo aprašai** taip pat galite priskirti prioriteto numerius įrašų eilutėms, taip kontroliuodami eilučių įvertinimo tvarką.</span><span class="sxs-lookup"><span data-stu-id="09094-115">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="09094-116">Pirma įvertinamos eilutės, kurių prioriteto numeris mažiausias.</span><span class="sxs-lookup"><span data-stu-id="09094-116">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="09094-117">Pvz., įvertinamos visos eilutės, kurių prioritetas yra 1, tada eilutės, kurių prioritetas yra 2 ir t. t.</span><span class="sxs-lookup"><span data-stu-id="09094-117">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="09094-118">Radus atitikmenį kiti gretinimo kriterijai ignoruojami.</span><span class="sxs-lookup"><span data-stu-id="09094-118">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="09094-119">Be to, sugeneruotus įrašus kuria tik pradinę operaciją atitinkančioje grupėje esantys kriterijai.</span><span class="sxs-lookup"><span data-stu-id="09094-119">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="09094-120">Savo registravimo aprašus galite patikrinti naudodami vedlį **Tikrinti registravimo aprašą**.</span><span class="sxs-lookup"><span data-stu-id="09094-120">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="09094-121">Nurodę registravimo aprašo pradinio įrašo pavyzdį, pamatysite sugeneruotus įrašus.</span><span class="sxs-lookup"><span data-stu-id="09094-121">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="09094-122">Galite naudoti registravimo aprašų versijas kartu su įsigaliojimo datomis.</span><span class="sxs-lookup"><span data-stu-id="09094-122">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="09094-123">Pvz., galite sukurti būsimą registravimo aprašo versiją, kad užregistruotumėte kitą DK sąskaitą į naujus finansinius metus.</span><span class="sxs-lookup"><span data-stu-id="09094-123">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="09094-124">Naudokite puslapį **Operacijų registravimo aprašai**, kad priskirtumėte registravimo aprašus operacijų tipams.</span><span class="sxs-lookup"><span data-stu-id="09094-124">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="09094-125">Registravimo aprašų susiejimas</span><span class="sxs-lookup"><span data-stu-id="09094-125">Linking posting definitions</span></span>
<span data-ttu-id="09094-126">Kai kuriate registravimo aprašus, galite susieti vieną registravimo aprašą su kitu.</span><span class="sxs-lookup"><span data-stu-id="09094-126">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="09094-127">Tada, be dabartinio registravimo aprašo kriterijų, atsižvelgiama ir į jūsų susieto aprašo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="09094-127">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="09094-128">Ši funkcija padeda sutaupyti laiko, nes nereikės iš naujo įvesti dabartinio registravimo aprašo kriterijų „FastTab“ **Įrašai** puslapyje **Registravimo aprašai**, jei šias eilutes jau įvedėte kitam aprašui.</span><span class="sxs-lookup"><span data-stu-id="09094-128">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="09094-129">Į diagramas arba lenteles įtraukite visus saitus, kuriuos galite naudoti.</span><span class="sxs-lookup"><span data-stu-id="09094-129">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="09094-130">Norėdami išvengti konfliktų su dabartiniu registravimo aprašu, įsitikinkite, kad visuose registravimo aprašuose esančios eilutės yra unikalios.</span><span class="sxs-lookup"><span data-stu-id="09094-130">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="09094-131">Kuriant saitus registravimo aprašuose taikomi šie apribojimai:</span><span class="sxs-lookup"><span data-stu-id="09094-131">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="09094-132">Registravimo aprašas gali būti susietas su kitu registravimo aprašu arba kitas registravimo aprašas gali būti susietas su pirmuoju, bet ne abu vienu metu.</span><span class="sxs-lookup"><span data-stu-id="09094-132">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="09094-133">Tačiau vieną registravimo aprašą galima susieti su keliais registravimo aprašais.</span><span class="sxs-lookup"><span data-stu-id="09094-133">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="09094-134">Galite nustatyti saitus tik tarp tarp tame pačiame modulyje esančių registravimo aprašų.</span><span class="sxs-lookup"><span data-stu-id="09094-134">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="09094-135">Galite priskirti registravimo aprašą bet kokiam operacijos tipui, bet operacijos tipas turi būti tame pačiame modulyje kaip ir registravimo aprašas.</span><span class="sxs-lookup"><span data-stu-id="09094-135">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="09094-136">Naudokite puslapį **Operacijų registravimo aprašai** norėdami pamatyti, kuriame modulyje yra operacijos tipas.</span><span class="sxs-lookup"><span data-stu-id="09094-136">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="09094-137">Daugiau informacijos ieškokite [Registravimo aprašų pavyzdžiai](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="09094-137">For more information, see [Posting definitions examples](example-posting-definitions.md).</span></span> 



