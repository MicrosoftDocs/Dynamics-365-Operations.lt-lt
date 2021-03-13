---
title: Dvigubo rašymo sąranka iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį iš „Microsoft Dynamics Lifecycle Services” (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: df67e498b963af3ded7464f46f37bb4b2ca7d852
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127598"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="1adb9-103">Dvigubo rašymo sąranka iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="1adb9-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="1adb9-104">Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį tarp naujos Finance and Operations aplinkos ir naujos Dataverse aplinkos iš „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="1adb9-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1adb9-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="1adb9-105">Prerequisites</span></span>

<span data-ttu-id="1adb9-106">Norėdami nustatyti dvigubo rašymo ryšį, turite turėti administratoriaus statusą.</span><span class="sxs-lookup"><span data-stu-id="1adb9-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="1adb9-107">Turite turėti prieigos prie nuomotojo teisę.</span><span class="sxs-lookup"><span data-stu-id="1adb9-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="1adb9-108">Turite būti administratorius tiek Finance and Operations, tiek Dataverse aplinkose.</span><span class="sxs-lookup"><span data-stu-id="1adb9-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="1adb9-109">Dvigubo rašymo ryšio nustatymas</span><span class="sxs-lookup"><span data-stu-id="1adb9-109">Set up a dual-write connection</span></span>

<span data-ttu-id="1adb9-110">Norėdami nustatyti dvigubo rašymo ryšį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1adb9-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="1adb9-111">Nueikite į savo projektą, esantį LCS.</span><span class="sxs-lookup"><span data-stu-id="1adb9-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="1adb9-112">Pasirinkite **Konfigūruoti**, kad įdiegtumėte naują aplinką.</span><span class="sxs-lookup"><span data-stu-id="1adb9-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="1adb9-113">Pasirinkite versiją.</span><span class="sxs-lookup"><span data-stu-id="1adb9-113">Select the version.</span></span> 
4. <span data-ttu-id="1adb9-114">Pasirinkite topologiją.</span><span class="sxs-lookup"><span data-stu-id="1adb9-114">Select the topology.</span></span> <span data-ttu-id="1adb9-115">Jei galima tik viena topologija, ji pasirenkama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="1adb9-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="1adb9-116">Atlikite pirmuosius veiksmus vedlyje **Diegimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="1adb9-117">Skirtuke **Dataverse** atlikite vieną iš toliau nurodytų veiksmų:</span><span class="sxs-lookup"><span data-stu-id="1adb9-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="1adb9-118">Jei Dataverse aplinka jau parengta jūsų nuomininkui, ją galite pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="1adb9-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="1adb9-119">Parinktį **Konfigūruoti Dataverse** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="1adb9-120">Stulpelyje **Galimos aplinkos** pasirinkite aplinką, į kurią norite integruoti savo Finance and Operations duomenis.</span><span class="sxs-lookup"><span data-stu-id="1adb9-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="1adb9-121">Į sąrašą įeina visos aplinkos, kuriose turite administratoriaus privilegijas.</span><span class="sxs-lookup"><span data-stu-id="1adb9-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="1adb9-122">Norėdami nurodyti, kad sutinkate su pateiktomis sąlygomis, pasirinkite žymės langelį **Sutinku**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Skirtukas Dataverse, kai aplinka Dataverse parengta jūsų nuomotojui](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="1adb9-124">Jei jūsų nuomotojas dar neturi Dataverse aplinkos, bus parengta nauja aplinka.</span><span class="sxs-lookup"><span data-stu-id="1adb9-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="1adb9-125">Parinktį **Konfigūruoti Dataverse** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="1adb9-126">Įveskite Dataverse aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="1adb9-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="1adb9-127">Pasirinkite regioną, kuriame norite įdiegti aplinką.</span><span class="sxs-lookup"><span data-stu-id="1adb9-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="1adb9-128">Pasirinkite numatytąją aplinkos kalbą ir valiutą.</span><span class="sxs-lookup"><span data-stu-id="1adb9-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="1adb9-129">Vėliau pakeisti kalbos ir valiutos negalite.</span><span class="sxs-lookup"><span data-stu-id="1adb9-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="1adb9-130">Norėdami nurodyti, kad sutinkate su pateiktomis sąlygomis, pasirinkite žymės langelį **Sutinku**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Skirtukas Dataverse, kai jūsų nuomotojas dar neturi Dataverse aplinkos](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="1adb9-132">Atlikite likusius veiksmus vedlyje **Diegimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="1adb9-133">Kai aplinka įgyja statusą **Įdiegta**, atidarykite aplinkos išsamios informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="1adb9-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="1adb9-134">Skyriuje **Power Platform integravimas** pateikiami susietų Finance and Operations ir Dataverse aplinkų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="1adb9-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![„Power Platform” integravimo skyrius](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="1adb9-136">Finance and Operations aplinkos administratorius turi prisijungti prie LCS ir pasirinkti **Programėlių CDS saitas**, kad susiejimas būtų užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="1adb9-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="1adb9-137">Aplinkos informacijos puslapyje pateikiama administratoriaus kontaktinė informacija.</span><span class="sxs-lookup"><span data-stu-id="1adb9-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="1adb9-138">Susiejimą užbaigus, būsena atnaujinama į **Aplinkos siejimas sėkmingai užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="1adb9-139">Norėdami atidaryti aplinkoje Finance and Operations esančią darbo sritį **Duomenų integravimas** ir valdyti pasiekiamus šablonus, pasirinkite **Programėlių CDS saitas**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Mygtukas CDS programoms, esantis Power Platform integravimo skyriuje](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="1adb9-141">Negalite atsieti aplinkos naudodami LCS.</span><span class="sxs-lookup"><span data-stu-id="1adb9-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="1adb9-142">Norėdami atsieti aplinką, aplinkoje Finance and Operations atidarykite darbo sritį **Duomenų integravimas** ir pasirinkite **Atsieti**.</span><span class="sxs-lookup"><span data-stu-id="1adb9-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

