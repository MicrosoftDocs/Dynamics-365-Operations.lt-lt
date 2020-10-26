---
title: Eksperimento nustatymas
description: Šioje temoje aprašoma, kaip nustatyti eksperimentą trečiosios šalies paslaugoje.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930252"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="ee621-103">Eksperimento nustatymas</span><span class="sxs-lookup"><span data-stu-id="ee621-103">Set up an experiment</span></span>

<span data-ttu-id="ee621-104">[Nustatę hipotezę ir sėkmės metriką, kurią norite naudoti](experimentation-identify.md), turite nustatyti jūsų eksperimentą trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="ee621-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="ee621-105">Toliau pateiktoje diagramoje rodomi visi veiksmai, susiję su eksperimento nustatymu ir vykdymu „e-Commerce“ svetainėje „Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="ee621-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ee621-106">Papildomi veiksmai aprašomi kitose temose.</span><span class="sxs-lookup"><span data-stu-id="ee621-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="ee621-107">[ ![Vartotojo eksperimentavimo kelionė – nustatymas](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="ee621-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="ee621-108">Eksperimento nustatymas trečiosios šalies paslaugoje</span><span class="sxs-lookup"><span data-stu-id="ee621-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="ee621-109">Jau turėjote pasirinkti trečiosios šalies paslaugą, kuri vykdys ir stebės jūsų eksperimentą, ir nustatyti eksperimento jungtį.</span><span class="sxs-lookup"><span data-stu-id="ee621-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="ee621-110">Šios būtinosios sąlygos išvardytos [Eksperimentavimas „Dynamics 365 Commerce”](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ee621-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="ee621-111">Atlikite veiksmus, reikalingus eksperimentui sukurti trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="ee621-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="ee621-112">Jei jungtis tinkamai sukonfigūruota, visas eksperimentų, kuriuos nustatysite trečiosios šalies paslaugoje, sąrašas atsiras svetainių daryklėje per maždaug 5 minutes.</span><span class="sxs-lookup"><span data-stu-id="ee621-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will surface in site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="ee621-113">Jūsų sėkmės metrikos nustatymas</span><span class="sxs-lookup"><span data-stu-id="ee621-113">Set up your success metrics</span></span>
<span data-ttu-id="ee621-114">Kiekvienam eksperimentui reikia metrikos, kad būtų galima įvertinti variacijų poveikį ir patvirtinti hipotezę.</span><span class="sxs-lookup"><span data-stu-id="ee621-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="ee621-115">Atlikite toliau nurodytus veiksmus, norėdami įgalinti metrikos skaičiavimą trečiosios šalies paslaugoje naudojant aktyvius „Dynamics 365 Commerce” telemetrijos įvykius.</span><span class="sxs-lookup"><span data-stu-id="ee621-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

1. <span data-ttu-id="ee621-116">Svetainių daryklės kairiojoje naršymo srityje pasirinkite skirtuką **Puslapiai** ir pasirinkite puslapį, kurio metriką norite rinkti.</span><span class="sxs-lookup"><span data-stu-id="ee621-116">In site builder, select the **Pages** tab in the left navigation pane and then select the page that you want to collect metrics on.</span></span> 
1. <span data-ttu-id="ee621-117">Eikite į puslapio ar modulio, kurį norite sekti, dešinėje esančios ypatybių srities sekciją **Įvykių ID, kurie bus sekami**.</span><span class="sxs-lookup"><span data-stu-id="ee621-117">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="ee621-118">Pasirinkite **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="ee621-118">Select **View**.</span></span> <span data-ttu-id="ee621-119">Rodomas visų įvykių ID sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ee621-119">A list of all event IDs is displayed.</span></span> <span data-ttu-id="ee621-120">Kopijuokite įvykį, kurį norite sekti, ir įklijuokite įvykio raktą į nurodytą vietą trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="ee621-120">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="ee621-121">Jei reikia daugiau nei vieno įvykio, vienu metu kopijuokite po vieną raktą.</span><span class="sxs-lookup"><span data-stu-id="ee621-121">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="ee621-122">Norėdami sužinoti, kaip peržiūrėti visus galimus įvykius ir atributus, įskaitant puslapių rodinius ir įplaukų sekimą, žr. [„Commerce“ komponentų įvykiai triktims diagnozuoti ir šalinti](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="ee621-122">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="ee621-123">Atlikite kitus reikalingus metrikos sekimo veiksmus trečiosios šalies paslaugoje.</span><span class="sxs-lookup"><span data-stu-id="ee621-123">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="ee621-124">Ankstesnis veiksmas</span><span class="sxs-lookup"><span data-stu-id="ee621-124">Previous step</span></span>
[<span data-ttu-id="ee621-125">Eksperimento hipotezės ir metrikos nustatymas</span><span class="sxs-lookup"><span data-stu-id="ee621-125">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="ee621-126">Kitas veiksmas</span><span class="sxs-lookup"><span data-stu-id="ee621-126">Next step</span></span>
[<span data-ttu-id="ee621-127">Eksperimento prijungimas ir redagavimas</span><span class="sxs-lookup"><span data-stu-id="ee621-127">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
