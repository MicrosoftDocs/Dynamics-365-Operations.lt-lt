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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: fb17d5e82709a34ff088774d9e9034adb714b58c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646258"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="07203-103">Duomenų integratoriaus projekto kūrimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="07203-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="07203-104">Šioje temoje paaiškinama, kaip sukurti duomenų integratoriaus projektą.</span><span class="sxs-lookup"><span data-stu-id="07203-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="07203-105">Prisijunkite prie „Microsoft Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="07203-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="07203-106">Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite **Duomenų objektai**.</span><span class="sxs-lookup"><span data-stu-id="07203-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="07203-107">Palaukite, kol visi duomenų objektai bus atnaujinti, prieš pereidami prie tolesnio veiksmo.</span><span class="sxs-lookup"><span data-stu-id="07203-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="07203-108">Atidarykite [„Power Apps“ portalą](https://make.powerapps.com/) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="07203-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="07203-109">Pasirinkite tinkamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="07203-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="07203-110">Kairiojoje naršymo srityje pasirinkite **Duomenys \> Ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="07203-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="07203-111">Prisijunkite prie atitinkamų tolesnių elementų egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="07203-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="07203-112">„Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="07203-112">Dynamics 365</span></span>
        - <span data-ttu-id="07203-113">„Dynamics 365 for Fin & Ops“</span><span class="sxs-lookup"><span data-stu-id="07203-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="07203-114">Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="07203-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="07203-115">Pasirinkite **Duomenų integratorius**.</span><span class="sxs-lookup"><span data-stu-id="07203-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="07203-116">Pasirinkite **Ryšio rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="07203-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="07203-117">Pasirinkite **Naujas ryšio rinkinys**.</span><span class="sxs-lookup"><span data-stu-id="07203-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="07203-118">Įveskite ryšio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="07203-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="07203-119">Pasirinkite atitinkamus tolesnių elementų ryšius.</span><span class="sxs-lookup"><span data-stu-id="07203-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="07203-120">„Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="07203-120">Dynamics 365</span></span>
        - <span data-ttu-id="07203-121">„Dynamics 365 for Fin & Ops“</span><span class="sxs-lookup"><span data-stu-id="07203-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="07203-122">Pasirinkite tinkamą organizacijos susiejimą.</span><span class="sxs-lookup"><span data-stu-id="07203-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="07203-123">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="07203-123">Select **Create**.</span></span>

5. <span data-ttu-id="07203-124">Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="07203-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="07203-125">Kurkite tolesnių šablonų duomenų integravimo projektus, naudodami ką tik sukurtą ryšio rinkinį.</span><span class="sxs-lookup"><span data-stu-id="07203-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="07203-126">Kliento mokėjimo įžvalgų rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="07203-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="07203-127">Grynųjų pinigų srautų laiko serijos rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="07203-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="07203-128">Biudžeto laiko serijos rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="07203-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="07203-129">Nustatykite tinkamą kiekvieno projekto planavimą.</span><span class="sxs-lookup"><span data-stu-id="07203-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="07203-130">Jei nematote reikiamų objektų CDS, eikite į **Kreditas ir surinkimas > Sąranka > Finansinės įžvalgos > Finansinių įžvalgų parametrai**, įjunkite funkciją Kliento mokėjimo prognozės ir spustelėkite mygtuką **Sukurti prognozavimo modelį**.</span><span class="sxs-lookup"><span data-stu-id="07203-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="07203-131">Kai DI modelio diegimas baigtas (sėkmingas arba jo nepavyko atlikti), CDS objektai, kurių reikia kuriant integraciją, bus įdiegti į CDS.</span><span class="sxs-lookup"><span data-stu-id="07203-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="07203-132">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="07203-132">Privacy notice</span></span>

<span data-ttu-id="07203-133">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="07203-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
