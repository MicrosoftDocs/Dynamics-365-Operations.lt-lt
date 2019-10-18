---
title: Nusidėvėjimo pasiūlymo kūrimas
description: Šioje temoje aprašoma, kaip veikia nusidėvėjimo paketo pasiūlymai, ir paaiškinama, kaip pasiūlyti ilgalaikio turto nusidėvėjimą.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90c24e9d89c055ea95ca5f25cd85ef4042476a90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187066"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="91ffb-103">Nusidėvėjimo pasiūlymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="91ffb-103">Create a depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91ffb-104">Šioje temoje aprašoma, kaip veikia nusidėvėjimo paketo pasiūlymai, ir paaiškinama, kaip pasiūlyti ilgalaikio turto nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="91ffb-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="91ffb-105">Ši užduotis naudoja USMF demonstracinių duomenų įmonę ir buhalterio vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="91ffb-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="91ffb-106">Nusidėvėjimo pasiūlymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="91ffb-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="91ffb-107">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Kurti nusidėvėjimo pasiūlymą**.</span><span class="sxs-lookup"><span data-stu-id="91ffb-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="91ffb-108">Lauke **Žurnalo pavadinimas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="91ffb-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="91ffb-109">Lauke **Pabaigos data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="91ffb-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="91ffb-110">Pažymėkite parinktį **Apibendrinti nusidėvėjimą**, kad vienoje žurnalo eilutėje apibendrintumėte mėnesinį nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="91ffb-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="91ffb-111">Pavyzdžiui., jei reikšmė Pabaigos data yra 2015 m. kovo 31 d., sugeneruojamas toks aprašas: „Nusidėvėjimas nuo 2015 m. sausio 31 d.“.</span><span class="sxs-lookup"><span data-stu-id="91ffb-111">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="91ffb-112">Tada lauke **Data** pasiūlytoje žurnalo eilutėje yra nustatyta 2015 m. kovo 31 d.</span><span class="sxs-lookup"><span data-stu-id="91ffb-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="91ffb-113">Nusidėvėjimo pasiūlymą galima filtruoti pagal turtą, turto grupę arba kitus kriterijus naudojant parinktį **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="91ffb-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="91ffb-114">Kai naudojate formą **Kurti ilgalaikio turto įsigijimo arba nusidėvėjimo pasiūlymą**, nusidėvėjimą galite siūlyti paketais.</span><span class="sxs-lookup"><span data-stu-id="91ffb-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="91ffb-115">Tai rekomenduojama didesniems projektams, kurie naudos daugiau sistemos išteklių.</span><span class="sxs-lookup"><span data-stu-id="91ffb-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="91ffb-116">Jei pasirenkate paketo parinktį, vis tiek galite per tą laiką užbaigti kitas užduotis.</span><span class="sxs-lookup"><span data-stu-id="91ffb-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="91ffb-117">Kai siūlote nusidėvėjimą tokiu būdu, nusidėvėjimas apskaičiuojamas ilgalaikio turto vertinimo modeliams.</span><span class="sxs-lookup"><span data-stu-id="91ffb-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="91ffb-118">Pažymėkite **Kurti žurnalą**.</span><span class="sxs-lookup"><span data-stu-id="91ffb-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="91ffb-119">Peržiūrėti nusidėvėjimo įrašus</span><span class="sxs-lookup"><span data-stu-id="91ffb-119">Review depreciation entries</span></span>
1. <span data-ttu-id="91ffb-120">Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="91ffb-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="91ffb-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="91ffb-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="91ffb-122">Pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="91ffb-122">Select **Lines**.</span></span>
4. <span data-ttu-id="91ffb-123">Pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="91ffb-123">Select **Post**.</span></span>

