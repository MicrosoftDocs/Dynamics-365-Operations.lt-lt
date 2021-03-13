---
title: Duomenų integratoriaus projekto kūrimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip sukurti duomenų integratoriaus projektą.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0029e093f524c61ff17a480ee3b881b3994ba95a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009455"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="fc867-103">Duomenų integratoriaus projekto kūrimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="fc867-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="fc867-104">Šioje temoje paaiškinama, kaip sukurti duomenų integratoriaus projektą.</span><span class="sxs-lookup"><span data-stu-id="fc867-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="fc867-105">Prisijunkite prie „Microsoft Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="fc867-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="fc867-106">Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite **Duomenų objektai**.</span><span class="sxs-lookup"><span data-stu-id="fc867-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="fc867-107">Palaukite, kol visi duomenų objektai bus atnaujinti, prieš pereidami prie tolesnio veiksmo.</span><span class="sxs-lookup"><span data-stu-id="fc867-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="fc867-108">Atidarykite [„Power Apps“ portalą](https://make.powerapps.com/) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fc867-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="fc867-109">Pasirinkite tinkamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="fc867-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="fc867-110">Kairiojoje naršymo srityje pasirinkite **Duomenys \> Ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="fc867-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="fc867-111">Prisijunkite prie atitinkamų tolesnių elementų egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="fc867-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="fc867-112">„Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="fc867-112">Dynamics 365</span></span>
        - <span data-ttu-id="fc867-113">„Dynamics 365 for Fin & Ops“</span><span class="sxs-lookup"><span data-stu-id="fc867-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="fc867-114">Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fc867-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="fc867-115">Pasirinkite **Duomenų integratorius**.</span><span class="sxs-lookup"><span data-stu-id="fc867-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="fc867-116">Pasirinkite **Ryšio rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="fc867-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="fc867-117">Pasirinkite **Naujas ryšio rinkinys**.</span><span class="sxs-lookup"><span data-stu-id="fc867-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="fc867-118">Įveskite ryšio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="fc867-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="fc867-119">Pasirinkite atitinkamus tolesnių elementų ryšius.</span><span class="sxs-lookup"><span data-stu-id="fc867-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="fc867-120">„Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="fc867-120">Dynamics 365</span></span>
        - <span data-ttu-id="fc867-121">„Dynamics 365 for Fin & Ops“</span><span class="sxs-lookup"><span data-stu-id="fc867-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="fc867-122">Pasirinkite tinkamą organizacijos susiejimą.</span><span class="sxs-lookup"><span data-stu-id="fc867-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="fc867-123">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="fc867-123">Select **Create**.</span></span>

5. <span data-ttu-id="fc867-124">Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fc867-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="fc867-125">Kurkite tolesnių šablonų duomenų integravimo projektus, naudodami ką tik sukurtą ryšio rinkinį.</span><span class="sxs-lookup"><span data-stu-id="fc867-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="fc867-126">Kliento mokėjimo įžvalgų rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="fc867-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="fc867-127">Grynųjų pinigų srautų laiko serijos rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="fc867-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="fc867-128">Biudžeto laiko serijos rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="fc867-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="fc867-129">Nustatykite tinkamą kiekvieno projekto planavimą.</span><span class="sxs-lookup"><span data-stu-id="fc867-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="fc867-130">Jei nematote reikiamų objektų CDS, eikite į **Kreditas ir surinkimas > Sąranka > Finansinės įžvalgos > Finansinių įžvalgų parametrai**, įjunkite funkciją Kliento mokėjimo prognozės ir spustelėkite mygtuką **Sukurti prognozavimo modelį**.</span><span class="sxs-lookup"><span data-stu-id="fc867-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="fc867-131">Kai DI modelio diegimas baigtas (sėkmingas arba jo nepavyko atlikti), CDS objektai, kurių reikia kuriant integraciją, bus įdiegti į CDS.</span><span class="sxs-lookup"><span data-stu-id="fc867-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="fc867-132">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="fc867-132">Privacy notice</span></span>

<span data-ttu-id="fc867-133">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="fc867-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
