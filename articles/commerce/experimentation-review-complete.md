---
title: Variacijos skatinimas ir eksperimento užbaigimas
description: Šioje temoje aprašoma, kaip skatinti sėkmingą variaciją ir užbaigti eksperimentą „Dynamics 365 Commerce”.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 25cccbeae5c263a3032eeebf2fc5335e22c1415a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009933"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="ad933-103">Variacijos skatinimas ir eksperimento užbaigimas</span><span class="sxs-lookup"><span data-stu-id="ad933-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="ad933-104">Šioje temoje aprašoma, kaip skatinti variacijas, pateikusias geriausius rezultatus jūsų eksperimento metu, ir kaip užbaigti eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="ad933-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="ad933-105">Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="ad933-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ad933-106">Papildomi veiksmai aprašomi kitose temose.</span><span class="sxs-lookup"><span data-stu-id="ad933-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="ad933-107">[ ![Vartotojo eksperimentavimo kelionė – peržiūra ir užbaigimas](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ad933-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="ad933-108">[Įvykdę eksperimentą](experimentation-run-monitor.md) ir surinkę pakankamai duomenų, kad nustatytumėte, kurią variaciją naudosite jūsų aktyvioje svetainėje, skatinsite variaciją ir užbaigsite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="ad933-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="ad933-109">Variacijos skatinimas</span><span class="sxs-lookup"><span data-stu-id="ad933-109">Promote a variation</span></span>
<span data-ttu-id="ad933-110">Norėdami nuspręsti, kuri variacija pateikė geriausius rezultatus, naudokite duomenis ir analizę, susijusius su trečiosios šalies paslaugos eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="ad933-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="ad933-111">Tada galite jį skatinti pakeisdami dabartinį aktyvios svetainės turinį laimėjusia variacija, kad ji būtų pasiekiama visiems jūsų svetainės vartotojams.</span><span class="sxs-lookup"><span data-stu-id="ad933-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="ad933-112">Norėdami skatinti laimėjusią variaciją, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ad933-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="ad933-113">„Commerce” svetainių daryklės kairiojoje naršymo srityje pasirinkite **Eksperimentai** ir tada pasirinkite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="ad933-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="ad933-114">Komandų juostoje pasirinkite **Užbaigti eksperimentą**.</span><span class="sxs-lookup"><span data-stu-id="ad933-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="ad933-115">Dialogo lange **Užbaigti eksperimentą** pasirinkite **Peržiūrėti eksperimento duomenis**.</span><span class="sxs-lookup"><span data-stu-id="ad933-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="ad933-116">Atidaroma trečiosios šalies paslauga, kurioje galite patvirtinti metriką ir nustatyti, kuri variacija pateikė geriausius duomenis.</span><span class="sxs-lookup"><span data-stu-id="ad933-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="ad933-117">Dialogo lange **Užbaigti eksperimentą** pasirinkite laimėjusią variaciją ir pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="ad933-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="ad933-118">Atidarykite trečiosios šalies paslaugą ir sustabdykite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="ad933-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="ad933-119">Svetainių daryklėje pasirinkite **Baigti**, norėdami perrašyti pradinį aktyvų puslapį ir publikuoti laimėjusią variaciją, kad jis būtų pasiekiama visiems jūsų svetainės vartotojams.</span><span class="sxs-lookup"><span data-stu-id="ad933-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="ad933-120">Jei pasirinksite palikti dabartinį aktyvų puslapį ir nepublikuoti variacijos, pasirinkite **Publikuoti pradinį puslapį iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="ad933-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="ad933-121">Eksperimento naikinimas</span><span class="sxs-lookup"><span data-stu-id="ad933-121">Delete your experiment</span></span>
<span data-ttu-id="ad933-122">Nors nėra būtina panaikinti baigtą eksperimentą „Commerce”, galite jį panaikinti, norėdami taupyti vietą arba išvalyti jūsų darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="ad933-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="ad933-123">Norėdami panaikinti eksperimentą „Commerce” svetainių daryklėje, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ad933-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad933-124">Kairiojoje naršymo srityje pasirinkite **Eksperimentai** ir tada pasirinkite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="ad933-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="ad933-125">Jei eksperimentas vis dar aktyvus, prieš tęsdami, sustabdykite eksperimentą trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="ad933-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="ad933-126">Norėdami pašalinti variacijos turinį iš aktyvios svetainės, komandų juostoje pasirinkite **Panaikinti publikavimą**.</span><span class="sxs-lookup"><span data-stu-id="ad933-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="ad933-127">Norėdami panaikinti eksperimentą, pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="ad933-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="ad933-128">Ankstesnis veiksmas</span><span class="sxs-lookup"><span data-stu-id="ad933-128">Previous step</span></span>
[<span data-ttu-id="ad933-129">Eksperimento vykdymas ir stebėjimas</span><span class="sxs-lookup"><span data-stu-id="ad933-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
