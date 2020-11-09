---
title: Eksperimento prijungimas ir variacijų redagavimas
description: Šioje temoje aprašoma, kaip prijungti eksperimentą prie „Dynamics 365 Commerce” trečiosios šalies paslaugoje ir kaip redaguoti eksperimento variacijas.
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
ms.openlocfilehash: 030640ba8907ae52c198ac96ad2c243b533d8c53
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096972"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="6ecee-103">Eksperimento prijungimas ir variacijų redagavimas</span><span class="sxs-lookup"><span data-stu-id="6ecee-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="6ecee-104">Šioje temoje aprašoma, kaip prijungti jūsų eksperimentą „Commerce” ir atlikti variacijų keitimus, kad jos sutaptų su jūsų hipoteze.</span><span class="sxs-lookup"><span data-stu-id="6ecee-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="6ecee-105">Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="6ecee-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="6ecee-106">Papildomi veiksmai aprašomi kitose temose.</span><span class="sxs-lookup"><span data-stu-id="6ecee-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="6ecee-107">[ ![Vartotojo eksperimentavimo kelionė – prijungimas ir redagavimas](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="6ecee-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="6ecee-108">[Nustatę jūsų eksperimentą](experimentation-setup.md) trečiosios šalies paslaugoje, prijungsite eksperimentą „Dynamics 365 Commerce” ir redaguosite eksperimento variacijas.</span><span class="sxs-lookup"><span data-stu-id="6ecee-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="6ecee-109">Planavimo aplinkybės</span><span class="sxs-lookup"><span data-stu-id="6ecee-109">Planning considerations</span></span>

<span data-ttu-id="6ecee-110">Prieš prijungdami jūsų eksperimentą „Commerce”, turite priimti tam tikrus sprendimus, kurie turi įtakos tam, kaip „Commerce” valdo jūsų turinį.</span><span class="sxs-lookup"><span data-stu-id="6ecee-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="6ecee-111">Jūsų eksperimento aprėpties nustatymas</span><span class="sxs-lookup"><span data-stu-id="6ecee-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="6ecee-112">Kai prijungiate eksperimentą, esate raginami nustatyti eksperimento aprėptį.</span><span class="sxs-lookup"><span data-stu-id="6ecee-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="6ecee-113">Eksperimentai nustatomi kaip **dalinės** aprėpties arba **visos** aprėpties.</span><span class="sxs-lookup"><span data-stu-id="6ecee-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="6ecee-114">Pasirinkite **dalinę** , jei norite atlikti konkrečios puslapio dalies eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="6ecee-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="6ecee-115">Jei pasirinksite šią parinktį, turite nurodyti, kurie moduliai yra įtraukti į eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="6ecee-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="6ecee-116">Keitimai, atliekami numatytojo puslapio arba fragmento dalims, kurios nėra susijusios su eksperimentu, automatiškai sinchronizuojami skirtingose variacijose.</span><span class="sxs-lookup"><span data-stu-id="6ecee-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="6ecee-117">Pasirinkite **visą** aprėptį, jei norite atlikti viso puslapio ar fragmento eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="6ecee-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="6ecee-118">Sukuriamos atskiros numatytojo puslapio arba fragmento kopijos.</span><span class="sxs-lookup"><span data-stu-id="6ecee-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="6ecee-119">Jums nereikės pasirinkti, kuriuos modulius įtraukti į eksperimentą, nes galima keisti visą redagavimo paviršių.</span><span class="sxs-lookup"><span data-stu-id="6ecee-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="6ecee-120">Jei reikia, galite įtraukti, naikinti arba pertvarkyti modulius.</span><span class="sxs-lookup"><span data-stu-id="6ecee-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="6ecee-121">Tačiau, jei atliekami bet kokie numatytojo puslapio arba fragmento, su kuriuo susietas eksperimentas, keitimai, šiuos keitimus reikia sinchronizuoti neautomatiniu būdu visose variacijose.</span><span class="sxs-lookup"><span data-stu-id="6ecee-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="6ecee-122">Jei susiejate jūsų eksperimentą su puslapiu, naudojančiu maketą, galite nurodyti tik **visą** eksperimento aprėptį.</span><span class="sxs-lookup"><span data-stu-id="6ecee-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="6ecee-123">Nuspręskite, ar norite suplanuoti, kada publikuoti eksperimentą</span><span class="sxs-lookup"><span data-stu-id="6ecee-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="6ecee-124">Jei norite suplanuoti, kada publikuoti eksperimentą jūsų aktyvioje svetainėje, įsitikinkite, kad turinys, kurį norite susieti su eksperimentu, yra publikavimo grupėje *prieš* eksperimento prijungimą.</span><span class="sxs-lookup"><span data-stu-id="6ecee-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="6ecee-125">Daugiau informacijos apie publikavimo grupes, žr. [Darbas su publikavimo grupėmis](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="6ecee-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="6ecee-126">Jūsų eksperimento prijungimas</span><span class="sxs-lookup"><span data-stu-id="6ecee-126">Connect your experiment</span></span>
<span data-ttu-id="6ecee-127">Norėdami prijungti eksperimentą, paleiskite vedlį **Eksperimento prijungimas**.</span><span class="sxs-lookup"><span data-stu-id="6ecee-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="6ecee-128">Vedlys padeda atlikti veiksmus, reikalingus norint prijungti jūsų eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="6ecee-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="6ecee-129">Kai baigsite naudotis vedliu, jūsų eksperimentas bus prijungtas, o variacijos sukurtos ir paruoštos redaguoti.</span><span class="sxs-lookup"><span data-stu-id="6ecee-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="6ecee-130">Norėdami pradėti jūsų eksperimento prijungimą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ecee-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6ecee-131">Norėdami paleisti vedlį **Prijungti eksperimentą** , kairiojoje naršymo srityje pasirinkite **Eksperimentai** , tada pasirinkite **Prijungti**.</span><span class="sxs-lookup"><span data-stu-id="6ecee-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="6ecee-132">Taip pat galite pasiekti vedlį iš puslapio arba fragmento rengyklės redaguodami eksperimentą ir komandų juostoje pasirinkdami **Prijungti eksperimentą**.</span><span class="sxs-lookup"><span data-stu-id="6ecee-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ecee-133">Puslapį galima prijungti tik prie vieno eksperimento vienu metu.</span><span class="sxs-lookup"><span data-stu-id="6ecee-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="6ecee-134">Norėdami prijungti puslapį prie kito eksperimento, pirmiausia panaikinkite eksperimentą, prie kurio puslapis šiuo metu prijungtas.</span><span class="sxs-lookup"><span data-stu-id="6ecee-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="6ecee-135">Pasirinkite puslapį arba fragmentą, kurio eksperimentą norite vykdyti.</span><span class="sxs-lookup"><span data-stu-id="6ecee-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="6ecee-136">Nustatykite eksperimento aprėptį į **dalinę** arba **visą** , atsižvelgdami į pasirinkimą, kurį atlikote pirmesniame skyriuje [Jūsų eksperimento aprėpties nustatymas](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="6ecee-136">Set the experimentation scope to **partial** or **entire** , based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="6ecee-137">Jei norite vykdyti viso puslapio ar fragmento eksperimentą, turite įjungti funkcijos vėliavėlę **Puslapių ar fragmentų eksperimentų vykdymas**.</span><span class="sxs-lookup"><span data-stu-id="6ecee-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="6ecee-138">Daugiau informacijos ieškokite temoje [Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6ecee-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="6ecee-139">Paskutinio vedlio veiksmo metu pasirinkite **Generuoti variacijas ir išjungti vedlį**.</span><span class="sxs-lookup"><span data-stu-id="6ecee-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="6ecee-140">Sukuriamos eksperimento variacijos.</span><span class="sxs-lookup"><span data-stu-id="6ecee-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="6ecee-141">Jūsų variacijų redagavimas</span><span class="sxs-lookup"><span data-stu-id="6ecee-141">Edit your variations</span></span>
<span data-ttu-id="6ecee-142">Išjungus vedlį, sukuriamos variacijos.</span><span class="sxs-lookup"><span data-stu-id="6ecee-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="6ecee-143">Redakuokite variacijas, kad jos atitiktų eksperimento hipotezės pasirinkimus, kuriuos turite patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="6ecee-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="6ecee-144">Pasirinkite vieną iš toliau pateiktų procedūrų, atitinkančių jūsų eksperimento aprėptį, kurią pasirinkote pirmesniame skyriuje [Jūsų eksperimento aprėpties nustatymas](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="6ecee-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="6ecee-145">Eksperimentų, kurių aprėptis dalinė, variacijų redagavimas</span><span class="sxs-lookup"><span data-stu-id="6ecee-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="6ecee-146">Atlikite toliau pateiktus veiksmus, jei nurodėte **dalinę** jūsų eksperimento aprėptį vedlyje **Eksperimento prijungimas**.</span><span class="sxs-lookup"><span data-stu-id="6ecee-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="6ecee-147">Rengyklės rodinyje naudokite variacijų išplečiamąjį meniu, esantį po komandų juosta, norėdami redaguoti kiekvieną variaciją pagal jūsų pradinę hipotezę.</span><span class="sxs-lookup"><span data-stu-id="6ecee-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="6ecee-148">Taip pat galite nustatyti kontrolinę arba bazinę variaciją, palikdami vieną iš variacijų nepakeistą.</span><span class="sxs-lookup"><span data-stu-id="6ecee-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="6ecee-149">Pasirinkite modulį, su kuriuo bus eksperimentuojama, pasirinkite elipsę (...) ir tada pasirinkite **Įtraukti į eksperimentą**.</span><span class="sxs-lookup"><span data-stu-id="6ecee-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="6ecee-150">Eksperimentų, kurių aprėptis visa, variacijų redagavimas</span><span class="sxs-lookup"><span data-stu-id="6ecee-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="6ecee-151">Jei nurodėte **visą** jūsų eksperimento aprėptį vedlyje **Eksperimento prijungimas** , rengyklės rodinyje naudokite variacijų išplečiamąjį meniu, esantį po komandų juosta, norėdami redaguoti kiekvieną variaciją pagal jūsų pradinę hipotezę.</span><span class="sxs-lookup"><span data-stu-id="6ecee-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="6ecee-152">Bet kuriuo atveju galite nustatyti kontrolinę arba bazinę variaciją, palikdami vieną iš variacijų nepakeistą.</span><span class="sxs-lookup"><span data-stu-id="6ecee-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="6ecee-153">Ankstesnis veiksmas</span><span class="sxs-lookup"><span data-stu-id="6ecee-153">Previous step</span></span>
[<span data-ttu-id="6ecee-154">Eksperimento nustatymas</span><span class="sxs-lookup"><span data-stu-id="6ecee-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="6ecee-155">Kitas veiksmas</span><span class="sxs-lookup"><span data-stu-id="6ecee-155">Next step</span></span>
[<span data-ttu-id="6ecee-156">Eksperimento peržiūra ir publikavimas</span><span class="sxs-lookup"><span data-stu-id="6ecee-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
