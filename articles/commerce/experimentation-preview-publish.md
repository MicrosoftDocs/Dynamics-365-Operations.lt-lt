---
title: Eksperimento peržiūra ir publikavimas
description: Šioje temoje aprašoma, kaip peržiūrėti ir publikuoti eksperimentą iš „Dynamics 365 Commerce”.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097121"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="a7560-103">Eksperimento peržiūra ir publikavimas</span><span class="sxs-lookup"><span data-stu-id="a7560-103">Preview and publish an experiment</span></span>

<span data-ttu-id="a7560-104">Šioje temoje aprašoma, kaip peržiūrėti ir publikuoti jūsų eksperimentą „Dynamics 365 Commerce” po to, kai [prijungėte eksperimentą ir redagavote variacijas](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="a7560-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="a7560-105">Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="a7560-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a7560-106">Papildomi veiksmai aprašomi kitose temose.</span><span class="sxs-lookup"><span data-stu-id="a7560-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="a7560-107">[ ![Vartotojo eksperimentavimo kelionė – peržiūra ir publikavimas](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a7560-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="a7560-108">Jūsų eksperimento variacijų peržiūra</span><span class="sxs-lookup"><span data-stu-id="a7560-108">Preview your experiment variations</span></span>
<span data-ttu-id="a7560-109">Galite peržiūrėti jūsų variacijas ir jas redaguoti, kad jos atrodytų taip, kaip norite.</span><span class="sxs-lookup"><span data-stu-id="a7560-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="a7560-110">Norėdami peržiūrėti jūsų eksperimento variacijas „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a7560-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a7560-111">Po komandų juosta esančiame išplečiamajame variacijų meniu pasirinkite turinį, kurį norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="a7560-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="a7560-112">Komandų juostoje pasirinkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="a7560-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="a7560-113">Rodoma peržiūra, kaip turinys atrodys, kai jis bus publikuotas.</span><span class="sxs-lookup"><span data-stu-id="a7560-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="a7560-114">Norėdami peržiūrėti kitą variaciją, pasirinkite ją iš variacijų išplečiamojo meniu ir pasirinkite **Peržiūra** dar kartą.</span><span class="sxs-lookup"><span data-stu-id="a7560-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="a7560-115">Jūsų eksperimento publikavimas</span><span class="sxs-lookup"><span data-stu-id="a7560-115">Publish your experiment</span></span>
<span data-ttu-id="a7560-116">Jei nenaudojate publikavimo grupės, kad suplanuotumėte, kada eksperimentas bus publikuotas, o norite publikuoti iš karto, komandų juostoje pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="a7560-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="a7560-117">Bus publikuotos visos eksperimentui priklausančios variacijos.</span><span class="sxs-lookup"><span data-stu-id="a7560-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="a7560-118">Jei puslapyje yra nepublikuotas URL, pirmiausia turite publikuoti URL, kitaip jis nebus matomas jūsų svetainės vartotojams.</span><span class="sxs-lookup"><span data-stu-id="a7560-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="a7560-119">Daugiau informacijos žr. [Puslapio įrašymas, peržiūra ir publikavimas](save-preview-publish-page.md).</span><span class="sxs-lookup"><span data-stu-id="a7560-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="a7560-120">Publikavimo grupių naudojimas suplanuoti, kada eksperimentas bus publikuotas</span><span class="sxs-lookup"><span data-stu-id="a7560-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="a7560-121">Galima suplanuoti variacijų, sukurtų svetainių daryklėje, publikavimą naudojant publikavimo grupę.</span><span class="sxs-lookup"><span data-stu-id="a7560-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="a7560-122">Publikavimo grupėje galite prijungti puslapį ar fragmentą prie jūsų eksperimento, kairiojoje naršymo srityje pasirinkdami **Eksperimentai**.</span><span class="sxs-lookup"><span data-stu-id="a7560-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="a7560-123">Taip pat galite tai atlikti pasirinkdami **Puslapiai** arba **Fragmentai** ir vadovaudamiesi instrukcijomis, pateiktomis [Eksperimento prijungimas ir variacijų redagavimas](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="a7560-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="a7560-124">Informacijos apie publikavimo grupes, žr. [Darbas su publikavimo grupėmis](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="a7560-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="a7560-125">Naudojant publikavimo grupes su eksperimentais, yra svarbių dalykų, kuriuos reikia žinoti.</span><span class="sxs-lookup"><span data-stu-id="a7560-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="a7560-126">Kai įtraukiate puslapį ar fragmentą, kuriame vykdomas eksperimentas, į publikavimo grupę, eksperimentas bus pašalintas iš puslapio ar fragmento publikavimo grupėje.</span><span class="sxs-lookup"><span data-stu-id="a7560-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="a7560-127">Eksperimentai, prijungti prie aktyvios svetainės svetainės puslapių, nėra pasiekiami publikavimo grupių puslapiuose (ir atvirkščiai).</span><span class="sxs-lookup"><span data-stu-id="a7560-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="a7560-128">Be to, aktyvios svetainės puslapiai, kuriuose vykdomi eksperimentai, nėra pasiekiami kituose publikavimo grupių eksperimentuose (ir atvirkščiai).</span><span class="sxs-lookup"><span data-stu-id="a7560-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="a7560-129">Publikuojant arba planuojant publikavimo grupę, visas publikavimo grupės turinys publikuojamas, neatsižvelgiant į tai, ar yra eksperimentas, susietas su publikavimo grupe.</span><span class="sxs-lookup"><span data-stu-id="a7560-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="a7560-130">Kadangi publikavimo grupė ir toliau išlieka po to, kai ji publikuojama aktyvioje svetainėje, eksperimentai publikavimo grupėje taip pat išlieka.</span><span class="sxs-lookup"><span data-stu-id="a7560-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="a7560-131">Todėl negalėsite susieti kitų eksperimentų su tuo pačiu puslapiu ar fragmentu.</span><span class="sxs-lookup"><span data-stu-id="a7560-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="a7560-132">Norėdami išvengti šio apribojimo, panaikinkite visas publikavimo grupes, kuriose yra išlikusių eksperimentų.</span><span class="sxs-lookup"><span data-stu-id="a7560-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="a7560-133">Taip pat, jei norite panaikinti aktyvios svetainės eksperimentą, kuris taip pat yra publikavimo grupėje, pirmiausia panaikinkite jį iš publikavimo grupės.</span><span class="sxs-lookup"><span data-stu-id="a7560-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="a7560-134">Ankstesnis veiksmas</span><span class="sxs-lookup"><span data-stu-id="a7560-134">Previous step</span></span>
[<span data-ttu-id="a7560-135">Eksperimento prijungimas ir redagavimas</span><span class="sxs-lookup"><span data-stu-id="a7560-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="a7560-136">Kitas veiksmas</span><span class="sxs-lookup"><span data-stu-id="a7560-136">Next step</span></span>
[<span data-ttu-id="a7560-137">Eksperimento vykdymas ir stebėjimas</span><span class="sxs-lookup"><span data-stu-id="a7560-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
