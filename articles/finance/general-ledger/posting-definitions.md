---
title: Registravimo aprašai
description: Šiame straipsnyje pateikta informacija apie registravimo aprašus ir kaip juos nustatyti ir susieti. Palaikomiems registravimo tipams ir dokumentams galite naudoti registravimo aprašus vietoj registravimo šablonų, kad klasifikuotumėte pagrindines sąskaitas ir finansines dimensijas apskaitos įrašuose.
author: ShylaThompson
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22a7b0acae02738e4f14905edb13fac1da0d0213
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770602"
---
# <a name="posting-definitions"></a><span data-ttu-id="c8026-104">Registravimo aprašai</span><span class="sxs-lookup"><span data-stu-id="c8026-104">Posting definitions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8026-105">Šiame straipsnyje pateikta informacija apie registravimo aprašus ir kaip juos nustatyti ir susieti.</span><span class="sxs-lookup"><span data-stu-id="c8026-105">This article provides information about posting definitions, and how to define and link them.</span></span>
<span data-ttu-id="c8026-106">Palaikomiems registravimo tipams ir dokumentams galite naudoti registravimo aprašus vietoj registravimo šablonų, kad klasifikuotumėte pagrindines sąskaitas ir finansines dimensijas apskaitos įrašuose.</span><span class="sxs-lookup"><span data-stu-id="c8026-106">For supported posting types and documents, you can use posting definitions instead of posting profiles to classify main accounts and financial dimensions on accounting entries.</span></span> <span data-ttu-id="c8026-107">Galite peržiūrėti palaikomus dokumentus ir registravimo tipus puslapyje **Operacijų registravimo aprašai**.</span><span class="sxs-lookup"><span data-stu-id="c8026-107">You can view the supported documents and posting types on the **Transaction posting definitions** page.</span></span> 

<span data-ttu-id="c8026-108">Norėdami pradėti naudoti registravimo aprašus, pasirinkite parinktį**Naudoti registravimo aprašus** puslapyje **DK parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c8026-108">To start using posting definitions, select the **Use posting definitions** option on the **General ledger parameters** page.</span></span> <span data-ttu-id="c8026-109">Net kai naudojate registravimo aprašus, turite dar nustatyti pradinių įrašų ir nepalaikomų registravimo tipų bei dokumentų registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="c8026-109">Even when you use posting definitions, you must still define posting profiles for the originating entries and non-supported posting types and documents.</span></span> 

<span data-ttu-id="c8026-110">Naudokite registravimo aprašus norėdami įjungti pirkimo užsakymų biudžeto rezervavimo apskaitą ir pirkimo paraiškų preliminaraus biudžeto rezervavimo apskaitą.</span><span class="sxs-lookup"><span data-stu-id="c8026-110">You must use posting definitions in order to enable encumbrance accounting for purchase orders and pre-encumbrance accounting for purchase requisitions.</span></span>

## <a name="defining-posting-definitions"></a><span data-ttu-id="c8026-111">Registravimo aprašų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="c8026-111">Defining posting definitions</span></span>
<span data-ttu-id="c8026-112">Naudokite puslapį**Registravimo aprašai**, kad nurodytumėte gretinimo kriterijus ir apibrėžtumėte įrašus, kurie turėtų būti sugeneruoti įvykus sugretinimui.</span><span class="sxs-lookup"><span data-stu-id="c8026-112">Use the **Posting definitions** page to specify the match criteria and define the entries that should be generated when a match occurs.</span></span> <span data-ttu-id="c8026-113">Pradinių įrašų gretinimo kriterijai įvertinami kaip apskaitos paskirstymai.</span><span class="sxs-lookup"><span data-stu-id="c8026-113">The match criteria are evaluated for the originating entries as accounting distributions.</span></span> 

<span data-ttu-id="c8026-114">Puslapyje **Registravimo aprašai** taip pat galite priskirti prioriteto numerius įrašų eilutėms, taip kontroliuodami eilučių įvertinimo tvarką.</span><span class="sxs-lookup"><span data-stu-id="c8026-114">On the **Posting definitions** page, you can also assign priority numbers to entry lines to control the order in which the lines are evaluated.</span></span> <span data-ttu-id="c8026-115">Pirma įvertinamos eilutės, kurių prioriteto numeris mažiausias.</span><span class="sxs-lookup"><span data-stu-id="c8026-115">The lines that have the lowest priority number are evaluated first.</span></span> <span data-ttu-id="c8026-116">Pvz., įvertinamos visos eilutės, kurių prioritetas yra 1, tada eilutės, kurių prioritetas yra 2 ir t. t.</span><span class="sxs-lookup"><span data-stu-id="c8026-116">For example, all lines that have a priority of 1 are evaluated, and then lines that have a priority of 2, and so on.</span></span> <span data-ttu-id="c8026-117">Radus atitikmenį kiti gretinimo kriterijai ignoruojami.</span><span class="sxs-lookup"><span data-stu-id="c8026-117">When a match is found, the other match criteria are ignored.</span></span> <span data-ttu-id="c8026-118">Be to, sugeneruotus įrašus kuria tik pradinę operaciją atitinkančioje grupėje esantys kriterijai.</span><span class="sxs-lookup"><span data-stu-id="c8026-118">Additionally, only the criteria in the group that match the originating transaction create generated entries.</span></span> 

<span data-ttu-id="c8026-119">Savo registravimo aprašus galite patikrinti naudodami vedlį **Tikrinti registravimo aprašą**.</span><span class="sxs-lookup"><span data-stu-id="c8026-119">You can validate your posting definitions by using the **Test posting definition** wizard.</span></span> <span data-ttu-id="c8026-120">Nurodę registravimo aprašo pradinio įrašo pavyzdį, pamatysite sugeneruotus įrašus.</span><span class="sxs-lookup"><span data-stu-id="c8026-120">After you define a sample originating entry for a posting definition, you'll see the generated entries.</span></span> 

<span data-ttu-id="c8026-121">Galite naudoti registravimo aprašų versijas kartu su įsigaliojimo datomis.</span><span class="sxs-lookup"><span data-stu-id="c8026-121">You can use posting definition versions together with effective dates.</span></span> <span data-ttu-id="c8026-122">Pvz., galite sukurti būsimą registravimo aprašo versiją, kad užregistruotumėte kitą DK sąskaitą į naujus finansinius metus.</span><span class="sxs-lookup"><span data-stu-id="c8026-122">For example, you can create a future version of a posting definition to post to a different ledger account in a new fiscal year.</span></span> 

<span data-ttu-id="c8026-123">Naudokite puslapį **Operacijų registravimo aprašai**, kad priskirtumėte registravimo aprašus operacijų tipams.</span><span class="sxs-lookup"><span data-stu-id="c8026-123">Use the **Transaction posting definitions** page to assign posting definitions to transaction types.</span></span>

## <a name="linking-posting-definitions"></a><span data-ttu-id="c8026-124">Registravimo aprašų susiejimas</span><span class="sxs-lookup"><span data-stu-id="c8026-124">Linking posting definitions</span></span>
<span data-ttu-id="c8026-125">Kai kuriate registravimo aprašus, galite susieti vieną registravimo aprašą su kitu.</span><span class="sxs-lookup"><span data-stu-id="c8026-125">You can link from one posting definition to another when you create posting definitions.</span></span> <span data-ttu-id="c8026-126">Tada, be dabartinio registravimo aprašo kriterijų, atsižvelgiama ir į jūsų susieto aprašo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="c8026-126">The criteria for the definition that you linked to are then considered in addition to the criteria for the current posting definition.</span></span> <span data-ttu-id="c8026-127">Ši funkcija padeda sutaupyti laiko, nes nereikės iš naujo įvesti dabartinio registravimo aprašo kriterijų „FastTab“ **Įrašai** puslapyje **Registravimo aprašai**, jei šias eilutes jau įvedėte kitam aprašui.</span><span class="sxs-lookup"><span data-stu-id="c8026-127">This feature helps save you time, because you don't have to reenter criteria on the **Entries** FastTab on the **Posting definitions** page for the current posting definition if you already entered those lines for another definition.</span></span> 

<span data-ttu-id="c8026-128">Į diagramas arba lenteles įtraukite visus saitus, kuriuos galite naudoti.</span><span class="sxs-lookup"><span data-stu-id="c8026-128">In the diagrams or tables, include any links that you might use.</span></span> <span data-ttu-id="c8026-129">Norėdami išvengti konfliktų su dabartiniu registravimo aprašu, įsitikinkite, kad visuose registravimo aprašuose esančios eilutės yra unikalios.</span><span class="sxs-lookup"><span data-stu-id="c8026-129">To avoid conflicts with the current posting definition, make sure that the lines in any posting definitions that you link to are unique.</span></span> 

<span data-ttu-id="c8026-130">Kuriant saitus registravimo aprašuose taikomi šie apribojimai:</span><span class="sxs-lookup"><span data-stu-id="c8026-130">The following restrictions apply when you create links in posting definitions:</span></span>

-   <span data-ttu-id="c8026-131">Registravimo aprašas gali būti susietas su kitu registravimo aprašu arba kitas registravimo aprašas gali būti susietas su pirmuoju, bet ne abu vienu metu.</span><span class="sxs-lookup"><span data-stu-id="c8026-131">A given posting definition can either link to another posting definition or be linked to from another posting definition, but not both.</span></span> <span data-ttu-id="c8026-132">Tačiau vieną registravimo aprašą galima susieti su keliais registravimo aprašais.</span><span class="sxs-lookup"><span data-stu-id="c8026-132">However, a posting definition can link to multiple posting definitions.</span></span>
-   <span data-ttu-id="c8026-133">Galite nustatyti saitus tik tarp tarp tame pačiame modulyje esančių registravimo aprašų.</span><span class="sxs-lookup"><span data-stu-id="c8026-133">You can set up links only among posting definitions that are in the same module.</span></span>
-   <span data-ttu-id="c8026-134">Galite priskirti registravimo aprašą bet kokiam operacijos tipui, bet operacijos tipas turi būti tame pačiame modulyje kaip ir registravimo aprašas.</span><span class="sxs-lookup"><span data-stu-id="c8026-134">You can assign a posting definition to any transaction type, but the transaction type must be in the same module as the posting definition.</span></span> <span data-ttu-id="c8026-135">Naudokite puslapį **Operacijų registravimo aprašai** norėdami pamatyti, kuriame modulyje yra operacijos tipas.</span><span class="sxs-lookup"><span data-stu-id="c8026-135">Use the **Transaction posting definitions** page to see what module a transaction type is in.</span></span>


<span data-ttu-id="c8026-136">Daugiau informacijos ieškokite [Registravimo aprašo pavyzdžiai](example-posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="c8026-136">For more information, see [Posting definition examples](example-posting-definitions.md).</span></span> 


