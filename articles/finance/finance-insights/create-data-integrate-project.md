---
title: Duomenų integratoriaus projekto kūrimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip sukurti duomenų integratoriaus projektą.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 59f85c64ea7b1f539a245e08b76bd6a34797b0ca
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186473"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="883ec-103">Duomenų integratoriaus projekto kūrimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="883ec-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="883ec-104">Šioje temoje paaiškinama, kaip sukurti duomenų integratoriaus projektą.</span><span class="sxs-lookup"><span data-stu-id="883ec-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="883ec-105">Prisijunkite prie „Microsoft Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="883ec-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="883ec-106">Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite **Duomenų objektai**.</span><span class="sxs-lookup"><span data-stu-id="883ec-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="883ec-107">Palaukite, kol visi duomenų objektai bus atnaujinti, prieš pereidami prie tolesnio veiksmo.</span><span class="sxs-lookup"><span data-stu-id="883ec-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="883ec-108">Atidarykite [„Power Apps“ portalą](https://make.powerapps.com/) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="883ec-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="883ec-109">Pasirinkite tinkamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="883ec-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="883ec-110">Kairiojoje naršymo srityje pasirinkite **Duomenys \> Ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="883ec-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="883ec-111">Prisijunkite prie atitinkamų tolesnių elementų egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="883ec-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="883ec-112">„Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="883ec-112">Dynamics 365</span></span>
        - <span data-ttu-id="883ec-113">„Dynamics 365 for Fin & Ops“</span><span class="sxs-lookup"><span data-stu-id="883ec-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="883ec-114">Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="883ec-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="883ec-115">Pasirinkite **Duomenų integratorius**.</span><span class="sxs-lookup"><span data-stu-id="883ec-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="883ec-116">Pasirinkite **Ryšio rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="883ec-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="883ec-117">Pasirinkite **Naujas ryšio rinkinys**.</span><span class="sxs-lookup"><span data-stu-id="883ec-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="883ec-118">Įveskite ryšio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="883ec-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="883ec-119">Pasirinkite atitinkamus tolesnių elementų ryšius.</span><span class="sxs-lookup"><span data-stu-id="883ec-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="883ec-120">„Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="883ec-120">Dynamics 365</span></span>
        - <span data-ttu-id="883ec-121">„Dynamics 365 for Fin & Ops“</span><span class="sxs-lookup"><span data-stu-id="883ec-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="883ec-122">Pasirinkite tinkamą organizacijos susiejimą.</span><span class="sxs-lookup"><span data-stu-id="883ec-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="883ec-123">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="883ec-123">Select **Create**.</span></span>

5. <span data-ttu-id="883ec-124">Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="883ec-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="883ec-125">Kurkite tolesnių šablonų duomenų integravimo projektus, naudodami ką tik sukurtą ryšio rinkinį.</span><span class="sxs-lookup"><span data-stu-id="883ec-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="883ec-126">Kliento mokėjimo įžvalgų rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="883ec-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
            - <span data-ttu-id="883ec-127">Jei naudojate 10.0.17 ar vėlesnę versiją, turite naudoti šabloną, pavadinimu Kliento mokėjimo įžvalgų rezultatai (CDS į Fin ir Ops 10.0.17+).</span><span class="sxs-lookup"><span data-stu-id="883ec-127">If you are using version 10.0.17 or later, you need to use the template named, Customer payment insights result (CDS to Fin and Ops 10.0.17+).</span></span>
        - <span data-ttu-id="883ec-128">Grynųjų pinigų srautų laiko serijos rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="883ec-128">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="883ec-129">Biudžeto laiko serijos rezultatai (CDS į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="883ec-129">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="883ec-130">Nustatykite tinkamą kiekvieno projekto planavimą.</span><span class="sxs-lookup"><span data-stu-id="883ec-130">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="883ec-131">Jei nematote reikiamų objektų CDS, eikite į **Kreditas ir surinkimas > Sąranka > „Finance Insights” > „Finance Insights” parametrai**, įjunkite funkciją Kliento mokėjimo prognozės ir spustelėkite mygtuką **Sukurti prognozavimo modelį**.</span><span class="sxs-lookup"><span data-stu-id="883ec-131">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="883ec-132">Kai DI modelio diegimas baigtas (sėkmingas arba jo nepavyko atlikti), CDS objektai, kurių reikia kuriant integraciją, bus įdiegti į CDS.</span><span class="sxs-lookup"><span data-stu-id="883ec-132">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
