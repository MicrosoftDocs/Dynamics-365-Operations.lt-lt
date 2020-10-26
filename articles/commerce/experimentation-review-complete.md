---
title: Variacijos skatinimas ir eksperimento užbaigimas
description: Šioje temoje aprašoma, kaip skatinti sėkmingą variaciją ir užbaigti eksperimentą „Dynamics 365 Commerce”.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930248"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="87a84-103">Variacijos skatinimas ir eksperimento užbaigimas</span><span class="sxs-lookup"><span data-stu-id="87a84-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="87a84-104">Šioje temoje aprašoma, kaip skatinti variacijas, pateikusias geriausius rezultatus jūsų eksperimento metu, ir kaip užbaigti eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="87a84-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="87a84-105">Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="87a84-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="87a84-106">Papildomi veiksmai aprašomi kitose temose.</span><span class="sxs-lookup"><span data-stu-id="87a84-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="87a84-107">[ ![Vartotojo eksperimentavimo kelionė – peržiūra ir užbaigimas](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="87a84-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="87a84-108">[Įvykdę eksperimentą](experimentation-run-monitor.md) ir surinkę pakankamai duomenų, kad nustatytumėte, kurią variaciją naudosite jūsų aktyvioje svetainėje, skatinsite variaciją ir užbaigsite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="87a84-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="87a84-109">Variacijos skatinimas</span><span class="sxs-lookup"><span data-stu-id="87a84-109">Promote a variation</span></span>
<span data-ttu-id="87a84-110">Norėdami nuspręsti, kuri variacija pateikė geriausius rezultatus, naudokite duomenis ir analizę, susijusius su trečiosios šalies paslaugos eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="87a84-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="87a84-111">Norėdami pakeisti dabartinį aktyvios svetainės turinį laimėjusia variacija, kad ji būtų pasiekiama visiems jūsų svetainės vartotojams, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="87a84-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="87a84-112">Eikite į svetainių daryklės skirtuką **Eksperimentai** ir pasirinkite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="87a84-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="87a84-113">Viršutinėje juostoje pasirinkite **Užbaigti eksperimentą**.</span><span class="sxs-lookup"><span data-stu-id="87a84-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="87a84-114">Dialogo meniu **Užbaigti eksperimentą** pasirinkite **Peržiūrėti eksperimento duomenis**.</span><span class="sxs-lookup"><span data-stu-id="87a84-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="87a84-115">Atidaroma trečiosios šalies paslauga, kurioje galite patvirtinti metriką ir nustatyti, kuri variacija pateikė geriausius duomenis.</span><span class="sxs-lookup"><span data-stu-id="87a84-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="87a84-116">Svetainių daryklės dialogo meniu **Užbaigti eksperimentą** pasirinkite laimėjusią variaciją ir pasirinkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="87a84-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="87a84-117">Atidarykite trečiosios šalies paslaugą ir sustabdykite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="87a84-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="87a84-118">Svetainių daryklėje pasirinkite **Baigti**, norėdami perrašyti pradinį aktyvų puslapį ir publikuoti laimėjusią variaciją, kad jis būtų pasiekiama visiems jūsų svetainės vartotojams.</span><span class="sxs-lookup"><span data-stu-id="87a84-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="87a84-119">Jei pasirinksite palikti dabartinį aktyvų puslapį ir nepublikuoti variacijos, pasirinkite **Publikuoti pradinį puslapį iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="87a84-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="87a84-120">Eksperimento naikinimas</span><span class="sxs-lookup"><span data-stu-id="87a84-120">Delete your experiment</span></span>
<span data-ttu-id="87a84-121">Nors nėra būtina panaikinti baigtą eksperimentą „Commerce”, galite jį panaikinti, norėdami taupyti vietą arba išvalyti jūsų darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="87a84-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="87a84-122">Norėdami panaikinti eksperimentą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="87a84-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="87a84-123">Eikite į svetainių daryklės skirtuką **Eksperimentai** ir pasirinkite eksperimentą.</span><span class="sxs-lookup"><span data-stu-id="87a84-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="87a84-124">Jei eksperimentas vis dar aktyvus, prieš tęsdami, sustabdykite eksperimentą trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="87a84-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="87a84-125">Norėdami pašalinti variacijos turinį iš aktyvios svetainės, komandų juostoje pasirinkite **Panaikinti publikavimą**.</span><span class="sxs-lookup"><span data-stu-id="87a84-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="87a84-126">Norėdami panaikinti eksperimentą, komandų juostoje pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="87a84-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="87a84-127">Ankstesnis veiksmas</span><span class="sxs-lookup"><span data-stu-id="87a84-127">Previous step</span></span>
[<span data-ttu-id="87a84-128">Eksperimento vykdymas ir stebėjimas</span><span class="sxs-lookup"><span data-stu-id="87a84-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
