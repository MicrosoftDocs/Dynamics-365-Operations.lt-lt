---
title: Dvigubo rašymo sąranka iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį tarp naujos Finance and Operations aplinkos ir naujos Common Data Service aplinkos iš „Microsoft Dynamics Lifecycle Services“ (LCS).
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
ms.openlocfilehash: f49eba1748861af6ee3353a6c58005ee84ccae23
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998113"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="de09e-103">Dvigubo rašymo sąranka iš „Lifecycle Services“</span><span class="sxs-lookup"><span data-stu-id="de09e-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="de09e-104">Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį tarp naujos Finance and Operations aplinkos ir naujos Common Data Service aplinkos iš „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="de09e-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="de09e-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="de09e-105">Prerequisites</span></span>

<span data-ttu-id="de09e-106">Norėdami nustatyti dvigubo rašymo ryšį, turite turėti administratoriaus statusą.</span><span class="sxs-lookup"><span data-stu-id="de09e-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="de09e-107">Turite turėti prieigos prie nuomotojo teisę.</span><span class="sxs-lookup"><span data-stu-id="de09e-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="de09e-108">Turite būti administratorius tiek Finance and Operations, tiek Common Data Service aplinkose.</span><span class="sxs-lookup"><span data-stu-id="de09e-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="de09e-109">Dvigubo rašymo ryšio nustatymas</span><span class="sxs-lookup"><span data-stu-id="de09e-109">Set up a dual-write connection</span></span>

<span data-ttu-id="de09e-110">Norėdami nustatyti dvigubo rašymo ryšį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="de09e-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="de09e-111">Nueikite į savo projektą, esantį LCS.</span><span class="sxs-lookup"><span data-stu-id="de09e-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="de09e-112">Pasirinkite **Konfigūruoti** , kad įdiegtumėte naują aplinką.</span><span class="sxs-lookup"><span data-stu-id="de09e-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="de09e-113">Pasirinkite versiją.</span><span class="sxs-lookup"><span data-stu-id="de09e-113">Select the version.</span></span> 
4. <span data-ttu-id="de09e-114">Pasirinkite topologiją.</span><span class="sxs-lookup"><span data-stu-id="de09e-114">Select the topology.</span></span> <span data-ttu-id="de09e-115">Jei galima tik viena topologija, ji pasirenkama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="de09e-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="de09e-116">Atlikite pirmuosius veiksmus vedlyje **Diegimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="de09e-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="de09e-117">Skirtuke **Common Data Service** atlikite vieną iš toliau nurodytų veiksmų:</span><span class="sxs-lookup"><span data-stu-id="de09e-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="de09e-118">Jei Common Data Service aplinka jau parengta jūsų nuomininkui, ją galite pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="de09e-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="de09e-119">Parinktį **Konfigūruoti Common Data Service** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="de09e-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="de09e-120">Lauke **Galimos aplinkos** pasirinkite aplinką, į kurią norite integruoti savo Finance and Operations duomenis.</span><span class="sxs-lookup"><span data-stu-id="de09e-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="de09e-121">Į sąrašą įeina visos aplinkos, kuriose turite administratoriaus privilegijas.</span><span class="sxs-lookup"><span data-stu-id="de09e-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="de09e-122">Norėdami nurodyti, kad sutinkate su pateiktomis sąlygomis, pasirinkite žymės langelį **Sutinku**.</span><span class="sxs-lookup"><span data-stu-id="de09e-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Skirtukas Common Data Service, kai aplinka Common Data Service parengta jūsų nuomotojui](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="de09e-124">Jei jūsų nuomotojas dar neturi Common Data Service aplinkos, bus parengta nauja aplinka.</span><span class="sxs-lookup"><span data-stu-id="de09e-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="de09e-125">Parinktį **Konfigūruoti Common Data Service** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="de09e-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="de09e-126">Įveskite Common Data Service aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="de09e-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="de09e-127">Pasirinkite regioną, kuriame norite įdiegti aplinką.</span><span class="sxs-lookup"><span data-stu-id="de09e-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="de09e-128">Pasirinkite numatytąją aplinkos kalbą ir valiutą.</span><span class="sxs-lookup"><span data-stu-id="de09e-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="de09e-129">Vėliau pakeisti kalbos ir valiutos negalite.</span><span class="sxs-lookup"><span data-stu-id="de09e-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="de09e-130">Norėdami nurodyti, kad sutinkate su pateiktomis sąlygomis, pasirinkite žymės langelį **Sutinku**.</span><span class="sxs-lookup"><span data-stu-id="de09e-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Skirtukas Common Data Service, kai jūsų nuomotojas dar neturi Common Data Service aplinkos](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="de09e-132">Atlikite likusius veiksmus vedlyje **Diegimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="de09e-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="de09e-133">Kai aplinka įgyja statusą **Įdiegta** , atidarykite aplinkos išsamios informacijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="de09e-133">After the environment has a status of **Deployed** , open the environment details page.</span></span> <span data-ttu-id="de09e-134">Skyriuje **Common Data Service aplinkos informacija** pateikiami susietų Finance and Operations ir Common Data Service aplinkų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="de09e-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Common Data Service aplinkos informacijos skyrius](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="de09e-136">Finance and Operations aplinkos administratorius turi prisijungti prie LCS ir pasirinkti **Programėlių CDS saitas** , kad susiejimas būtų užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="de09e-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="de09e-137">Aplinkos informacijos puslapyje pateikiama administratoriaus kontaktinė informacija.</span><span class="sxs-lookup"><span data-stu-id="de09e-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="de09e-138">Susiejimą užbaigus, būsena atnaujinama į **Aplinkos siejimas sėkmingai užbaigtas**.</span><span class="sxs-lookup"><span data-stu-id="de09e-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="de09e-139">Norėdami atidaryti aplinkoje Finance and Operations esančią darbo sritį **Duomenų integravimas** ir valdyti pasiekiamus šablonus, pasirinkite **Programėlių CDS saitas**.</span><span class="sxs-lookup"><span data-stu-id="de09e-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Mygtukas „Programėlių CDS saitas“, esantis Common Data Service aplinkos informacijos sekcijoje](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="de09e-141">Negalite atsieti aplinkos naudodami LCS.</span><span class="sxs-lookup"><span data-stu-id="de09e-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="de09e-142">Norėdami atsieti aplinką, aplinkoje Finance and Operations atidarykite darbo sritį **Duomenų integravimas** ir pasirinkite **Atsieti**.</span><span class="sxs-lookup"><span data-stu-id="de09e-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
