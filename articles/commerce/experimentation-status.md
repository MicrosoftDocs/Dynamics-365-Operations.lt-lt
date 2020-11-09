---
title: Eksperimento būsenos peržiūra
description: Šioje temoje paaiškinama, kokia yra eksperimento būsena eksperimento ciklo metu „Dynamics 365 Commerce”.
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
ms.openlocfilehash: eea67ddc1718902198b74614ee1a910fc6e29c1d
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097075"
---
# <a name="review-the-status-of-an-experiment"></a><span data-ttu-id="22fdf-103">Eksperimento būsenos peržiūra</span><span class="sxs-lookup"><span data-stu-id="22fdf-103">Review the status of an experiment</span></span>
<span data-ttu-id="22fdf-104">Yra daug veiksmų, susijusių su eksperimento nustatymu ir vykdymu „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="22fdf-104">There are many steps involved in setting up and running an experiment in Dynamics 365 Commerce.</span></span> <span data-ttu-id="22fdf-105">Informacijos apie eksperimento ciklą žr. [Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22fdf-105">For information about the experimentation lifecycle, see [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="22fdf-106">Norėdami sužinoti, kurioje ciklo vietoje yra eksperimentas, „Commerce” svetainių daryklės kairiojoje naršymo srityje pasirinkite **Eksperimentai**.</span><span class="sxs-lookup"><span data-stu-id="22fdf-106">To learn where an experiment is in the lifecycle, in Commerce site builder select **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="22fdf-107">„Commerce“ ir trečiosios šalies paslaugoje, kuri naudojama eksperimentams kurti, variacijoms priskirti ir duomenims analizuoti, rodomas eksperimentų sąrašas su kiekvieno eksperimento būsena.</span><span class="sxs-lookup"><span data-stu-id="22fdf-107">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service that is being used to enable the creation of experiments, assign variations, and analyze data.</span></span>

<span data-ttu-id="22fdf-108">Stulpelyje **„Commerce” būsena** gali būti rodomos toliau pateiktos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="22fdf-108">In the **Commerce status** column, the following values may be displayed.</span></span> 
- <span data-ttu-id="22fdf-109">**Juodraštis** – eksperimentas prijungtas prie „Commerce” puslapio arba fragmento ir yra redaguojamas.</span><span class="sxs-lookup"><span data-stu-id="22fdf-109">**Draft** - The experiment is connected to a page or fragment in Commerce and is being edited.</span></span>
- <span data-ttu-id="22fdf-110">**Publikuota** – eksperimento variacijos paruoštos rodymui jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="22fdf-110">**Published** - The experiment variations are ready to be displayed on your website.</span></span> <span data-ttu-id="22fdf-111">Jei eksperimentas vykdomas trečiosios šalies paslaugoje, svetainės vartotojai matys puslapio ar fragmento variaciją kaip pasirinktą trečiosios šalies paslaugos.</span><span class="sxs-lookup"><span data-stu-id="22fdf-111">If the experiment is running in the third-party service, website users will see a variation of the page or fragment as selected by the third-party service.</span></span>
- <span data-ttu-id="22fdf-112">**Nepublikuota** – eksperimentas nebėra pasiekiamas jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="22fdf-112">**Unpublished** - The experiment is no longer available on your website.</span></span> <span data-ttu-id="22fdf-113">Svetainės vartotojai matys tik numatytąją puslapio ar fragmento versiją, net jei eksperimentas vykdomas trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="22fdf-113">Website users will only see the default version of the page or fragment even if the experiment is running in the third-party service.</span></span>
- <span data-ttu-id="22fdf-114">**Baigta** – eksperimentas buvo įvykdytas ir visiems svetainės vartotojams buvo skatinama variacija.</span><span class="sxs-lookup"><span data-stu-id="22fdf-114">**Completed** - The experiment has run its course and a variation was promoted to live for all website users.</span></span>

<span data-ttu-id="22fdf-115">Taip pat **trečiosios šalies būsenos** stulpelyje gali būti rodomos toliau nurodytos reikšmės, nurodančios, kokia yra eksperimentų būsena trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="22fdf-115">Similarly, in the **third-party status** column, the following values may be displayed to indicate what status the experiments are in the third-party service.</span></span>
- <span data-ttu-id="22fdf-116">**Juodraštis** – eksperimentas nustatytas trečiosios šalies paslaugoje, bet nepradėtas.</span><span class="sxs-lookup"><span data-stu-id="22fdf-116">**Draft** - The experiment is set up in the third-party service but hasn't been started.</span></span>
- <span data-ttu-id="22fdf-117">**Vykdoma** – eksperimentas buvo pradėtas trečiosios šalies paslaugoje ir jo metu renkami duomenys.</span><span class="sxs-lookup"><span data-stu-id="22fdf-117">**Running** - The experiment was started in the third-party service and is collecting data.</span></span>
- <span data-ttu-id="22fdf-118">**Pristabdyta** – eksperimentas pristabdytas ir duomenys nerenkami.</span><span class="sxs-lookup"><span data-stu-id="22fdf-118">**Paused** - The experiment is paused and not collecting data.</span></span> <span data-ttu-id="22fdf-119">Norėdami, kad duomenys vėl būtų renkami, turite tęsti eksperimento vykdymą.</span><span class="sxs-lookup"><span data-stu-id="22fdf-119">You must resume the experiment for it to collect data again.</span></span>
- <span data-ttu-id="22fdf-120">**Suarchyvuota** – eksperimentas buvo įvykdytas ir įrašytas į trečiosios šalies paslaugos katalogą, kad jį būtų galima naudoti ateityje.</span><span class="sxs-lookup"><span data-stu-id="22fdf-120">**Archived** - The experiment has run its course and has been cataloged in the third-party service for future reference.</span></span>

<span data-ttu-id="22fdf-121">Toliau pateiktoje diagramoje parodyti abu būsenų rinkiniai ir kaip jie susiję tarpusavyje.</span><span class="sxs-lookup"><span data-stu-id="22fdf-121">The diagram below shows both sets of statuses and how they relate to each other.</span></span>

<span data-ttu-id="22fdf-122">[ ![Eksperimentų būsenos](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="22fdf-122">[ ![Experimentation statuses](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)</span></span>
