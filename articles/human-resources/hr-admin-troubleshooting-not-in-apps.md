---
title: „Human Resources“ nėra „Microsoft Dynamics 365“ programose
description: Šiame straipsnyje aiškinama, ką daryti, jei klientas nemato programos „Dynamics 365 Human Resources“ tarp „Microsoft Dynamics 365“ programų.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803974"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="4be1b-103">„Human Resources“ nėra „Microsoft Dynamics 365“ programose</span><span class="sxs-lookup"><span data-stu-id="4be1b-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4be1b-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="4be1b-104">**Issue**</span></span>

<span data-ttu-id="4be1b-105">Klientas nematys „Dynamics 365 Human Resources“ tarp „Microsoft Dynamics 365“ programų.</span><span class="sxs-lookup"><span data-stu-id="4be1b-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="4be1b-106">**Nutarimas**</span><span class="sxs-lookup"><span data-stu-id="4be1b-106">**Resolution**</span></span>

<span data-ttu-id="4be1b-107">Vartotojas turi būti įtrauktas į „Microsoft Power Apps“ aplinkai skirtą vaidmenį Aplinkos kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="4be1b-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="4be1b-108">Vartotojas administratorius, turintis „Power Apps“ 2 plano licenciją, turi atidaryti [„Power Apps“ administravimo portalą](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="4be1b-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="4be1b-109">Pasirinkite **Aplinkos**, tada pasirinkite „Human Resources“ tinkamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="4be1b-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="4be1b-110">Skirtuke **Sauga**, pateikiamame skirtuke **Aplinkos vaidmenys**, pasirinkite **Aplinkos kūrėjas**.</span><span class="sxs-lookup"><span data-stu-id="4be1b-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Skirtukas Aplinkos vaidmenys](media/environment-roles.png)

4. <span data-ttu-id="4be1b-112">Skirtuke **Vartotojai** įtraukite vartotoją arba savo organizaciją.</span><span class="sxs-lookup"><span data-stu-id="4be1b-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Skirtukas Vartotojai](media/environment-maker.png)

5. <span data-ttu-id="4be1b-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4be1b-114">Select **Save**.</span></span>

6. <span data-ttu-id="4be1b-115">Dabar vartotojas turi prisijungti prie [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="4be1b-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="4be1b-116">Pasirinkite **Sinchronizuoti**, kad atnaujintumėte vartotojo programas.</span><span class="sxs-lookup"><span data-stu-id="4be1b-116">Select **Sync** to update the user apps.</span></span>

    ![Sinchronizavimo mygtukas](media/get-more.png)

    <span data-ttu-id="4be1b-118">Baigus sinchronizuoti, „Human Resources“ bus rodoma pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="4be1b-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]