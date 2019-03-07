---
title: Kurti nusidėvėjimo pasiūlymą
description: Šioje procedūroje aprašoma, kaip veikia nusidėvėjimo paketo pasiūlymai, ir paaiškinama, kaip pasiūlyti ilgalaikio turto nusidėvėjimą.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "361296"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="7364c-103">Kurti nusidėvėjimo pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="7364c-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7364c-104">Šioje procedūroje aprašoma, kaip veikia nusidėvėjimo paketo pasiūlymai, ir paaiškinama, kaip pasiūlyti ilgalaikio turto nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="7364c-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="7364c-105">Ši užduotis naudoja USMF demonstracinių duomenų įmonę ir buhalterio vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="7364c-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="7364c-106">Kurti nusidėvėjimo pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="7364c-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="7364c-107">Pasirinkite Ilgalaikis turtas > Žurnalo įrašai > Kurti nusidėvėjimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="7364c-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="7364c-108">Lauke Žurnalo pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="7364c-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7364c-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7364c-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7364c-110">Lauke Pabaigos data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="7364c-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="7364c-111">Pasirinkite parinktį Sumuoti nusidėvėjimą, kad susumuotumėte mėnesio nusidėvėjimus į vieną žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="7364c-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="7364c-112">Pavyzdžiui., jei reikšmė Pabaigos data yra 2015 m. kovo 31 d., sugeneruojamas toks aprašas: „Nusidėvėjimas nuo 2015 m. sausio 31 d.“.</span><span class="sxs-lookup"><span data-stu-id="7364c-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="7364c-113">Laukas Data pasiūlytose žurnalo eilutėse tada nustatomas kaip 2015 m. kovo 31 d.</span><span class="sxs-lookup"><span data-stu-id="7364c-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="7364c-114">Naudojant parinktį Filtras, nusidėvėjimo pasiūlymą galima filtruoti pagal turtą, turto grupę ar kitus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="7364c-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="7364c-115">Kai naudojate formą Kurti ilgalaikio turto įsigijimo arba nusidėvėjimo pasiūlymus, nusidėvėjimą galite siūlyti paketais.</span><span class="sxs-lookup"><span data-stu-id="7364c-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="7364c-116">Tai rekomenduojama didesniems projektams, kurie naudos daugiau sistemos išteklių.</span><span class="sxs-lookup"><span data-stu-id="7364c-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="7364c-117">Jei pasirenkate paketo parinktį, vis tiek galite per tą laiką užbaigti kitas užduotis.</span><span class="sxs-lookup"><span data-stu-id="7364c-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="7364c-118">Kai siūlote nusidėvėjimą tokiu būdu, nusidėvėjimas apskaičiuojamas ilgalaikio turto vertinimo modeliams.</span><span class="sxs-lookup"><span data-stu-id="7364c-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="7364c-119">Spustelėkite Kurti žurnalą.</span><span class="sxs-lookup"><span data-stu-id="7364c-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="7364c-120">Peržiūrėti nusidėvėjimo įrašus</span><span class="sxs-lookup"><span data-stu-id="7364c-120">Review depreciation entries</span></span>
1. <span data-ttu-id="7364c-121">Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.</span><span class="sxs-lookup"><span data-stu-id="7364c-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="7364c-122">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7364c-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7364c-123">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="7364c-123">Click Lines.</span></span>
4. <span data-ttu-id="7364c-124">Spustelėkite Registruoti.</span><span class="sxs-lookup"><span data-stu-id="7364c-124">Click Post.</span></span>

