---
title: „Regulatory Configuration Service” (RCS) – RCS aplinkos naikinimas
description: Šioje temoje paaiškinta, kaip „Regulatory Configuration Service” (RCS) sistemos administratorius gali panaikinti RCS aplinką ir susijusius duomenis.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295823"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="24dd7-103">„Regulatory Configuration Service” (RCS) – RCS aplinkos naikinimas</span><span class="sxs-lookup"><span data-stu-id="24dd7-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24dd7-104">Šioje temoje paaiškinta, kaip „Regulatory Configuration Service” (RCS) sistemos administratorius gali panaikinti RCS aplinką ir susijusius duomenis.</span><span class="sxs-lookup"><span data-stu-id="24dd7-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="24dd7-105">Tam, kad užbaigtumėte šios temos, privalote atitikti šias būtinąsias sąlygas:</span><span class="sxs-lookup"><span data-stu-id="24dd7-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="24dd7-106">Privalote turėti jums priskirtą **Sistemos administratoriaus** vaidmenį RCS aplinkai.</span><span class="sxs-lookup"><span data-stu-id="24dd7-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="24dd7-107">**Sistemos administratoriaus** vaidmuo privalo turėti jam priskirtą **„RCSDeleteEnvironmentDuty”** vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="24dd7-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="24dd7-108">RCS aplinkos naikinimas</span><span class="sxs-lookup"><span data-stu-id="24dd7-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="24dd7-109">Atidarykite RCS ir pasirinkite **Elektroninių ataskaitų** darbo srities plytelę.</span><span class="sxs-lookup"><span data-stu-id="24dd7-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="24dd7-110">Skyriuje **Susiję saitai** pasirinkite **Naikinti RCS aplinką**.</span><span class="sxs-lookup"><span data-stu-id="24dd7-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![RCS aplinkos saito naikinimas Susijusių nuorodų skyriuje](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="24dd7-112">Pasirodžiusiame dialogo lange peržiūrėkite pranešimus apie aplinkos naikinimo aprėptį.</span><span class="sxs-lookup"><span data-stu-id="24dd7-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Pranešimai RCS aplinkos naikinimo dialogo lange](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="24dd7-114">RCS aplinkos panaikinimo negalima atšaukti.</span><span class="sxs-lookup"><span data-stu-id="24dd7-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="24dd7-115">Operacija panaikina pasirinktą RCS aplinką ir visus susijusius duomenis, įskaitant funkcijas ir konfigūracijas, saugomas visuotinėje saugykloje.</span><span class="sxs-lookup"><span data-stu-id="24dd7-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="24dd7-116">Funkcijos ir konfigūracijos, bendrai naudojamos su kitomis organizacijomis, nebebus bendrinamos, jei neturi priklausomybių.</span><span class="sxs-lookup"><span data-stu-id="24dd7-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="24dd7-117">Funkcijos ir konfigūracijos, kurios turi priklausomybių, bus pažymėtos kaip nutrauktos.</span><span class="sxs-lookup"><span data-stu-id="24dd7-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="24dd7-118">Pateiktame lauke įveskite RCS aplinkos globaliai unikalų identifikatorių (GUID), kad patvirtintumėte, jog norite ją panaikinti.</span><span class="sxs-lookup"><span data-stu-id="24dd7-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="24dd7-119">Aplinkos GUID yra įtrauktas į naikinimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="24dd7-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="24dd7-120">Pasirinkite **Naikinti aplinką**.</span><span class="sxs-lookup"><span data-stu-id="24dd7-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="24dd7-121">Dabar jūsų RCS aplinka ir visi susiję duomenys yra panaikinti.</span><span class="sxs-lookup"><span data-stu-id="24dd7-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24dd7-122">Panaikinus RCS aplinką, nėra jokio būdo atkurti duomenis.</span><span class="sxs-lookup"><span data-stu-id="24dd7-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="24dd7-123">Naują RCS aplinką galima sukurti bet kuriame galimame RCS regione.</span><span class="sxs-lookup"><span data-stu-id="24dd7-123">A new RCS environment can be created in any available RCS region.</span></span>
