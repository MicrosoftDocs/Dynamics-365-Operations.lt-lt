---
title: "Tarp „Microsoft Dynamics 365“ programų nėra „Talent“ (CDS1.0)"
description: "Šioje temoje aiškinama, ką daryti, jei klientas nemato programos „Microsoft Dynamics 365 for Talent“ tarp „Microsoft Dynamics 365“ programų."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="06e3c-103">Tarp „Microsoft Dynamics 365“ programų nėra „Talent“ (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="06e3c-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06e3c-104">**Problema**</span><span class="sxs-lookup"><span data-stu-id="06e3c-104">**Issue**</span></span>

<span data-ttu-id="06e3c-105">Klientas nemato programos „Microsoft Dynamics 365 for Talent“ tarp „Microsoft Dynamics 365“ programų.</span><span class="sxs-lookup"><span data-stu-id="06e3c-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="06e3c-106">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="06e3c-106">**Resolution**</span></span>

<span data-ttu-id="06e3c-107">Vartotojas turi būti įtrauktas į „Microsoft PowerApps“ aplinkai skirtą vaidmenį Aplinkos kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="06e3c-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="06e3c-108">Administratoriaus vartotojas, turintis „PowerApps“ 2 plano licenciją, turi atidaryti [„PowerApps“ administravimo portalą](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="06e3c-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="06e3c-109">Pasirinkite **Aplinkos**, tada pasirinkite „Talent“ tinkamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="06e3c-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="06e3c-110">Skirtuke **Sauga**, pateikiamame skirtuke **Aplinkos vaidmenys**, pasirinkite **Aplinkos kūrėjas**.</span><span class="sxs-lookup"><span data-stu-id="06e3c-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Skirtukas Aplinkos vaidmenys](media/environment-roles.png)

4. <span data-ttu-id="06e3c-112">Skirtuke **Vartotojai** įtraukite vartotoją arba savo organizaciją.</span><span class="sxs-lookup"><span data-stu-id="06e3c-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Skirtukas Vartotojai](media/environment-maker.png)

5. <span data-ttu-id="06e3c-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="06e3c-114">Select **Save**.</span></span>
6. <span data-ttu-id="06e3c-115">Dabar vartotojas turi prisijungti prie [„Microsoft Dynamics 365“](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="06e3c-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="06e3c-116">Pasirinkite **Sinchronizuoti**, kad atnaujintumėte vartotojo programas.</span><span class="sxs-lookup"><span data-stu-id="06e3c-116">Select **Sync** to update the user apps.</span></span>

    ![Sinchronizavimo mygtukas](media/get-more.png)

    <span data-ttu-id="06e3c-118">Baigus sinchronizuoti, „Talent“ bus rodoma pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="06e3c-118">After synchronization is completed, Talent will appear on the home page.</span></span>

