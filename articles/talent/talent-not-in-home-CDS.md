---
title: „Talent“ nerodoma tarp „Microsoft Dynamics 365“ programų („Common Data Service 1.0“)
description: Šioje temoje aiškinama, ką daryti, jei klientas nemato programos „Dynamics 365 for Talent“ tarp „Microsoft Dynamics 365“ programų.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518695"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="8d389-103">„Talent“ nerodoma tarp „Microsoft Dynamics 365“ programų („Common Data Service 1.0“)</span><span class="sxs-lookup"><span data-stu-id="8d389-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d389-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="8d389-104">**Issue**</span></span>

<span data-ttu-id="8d389-105">Klientas nemato programos „Microsoft Dynamics 365 for Talent“ tarp „Microsoft Dynamics 365“ programų.</span><span class="sxs-lookup"><span data-stu-id="8d389-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="8d389-106">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="8d389-106">**Resolution**</span></span>

<span data-ttu-id="8d389-107">Vartotojas turi būti įtrauktas į „Microsoft PowerApps“ aplinkai skirtą vaidmenį Aplinkos kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="8d389-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="8d389-108">Administratoriaus vartotojas, turintis „PowerApps“ 2 plano licenciją, turi atidaryti [„PowerApps“ administravimo portalą](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="8d389-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="8d389-109">Pasirinkite **Aplinkos**, tada pasirinkite „Talent“ tinkamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="8d389-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="8d389-110">Skirtuke **Sauga**, pateikiamame skirtuke **Aplinkos vaidmenys**, pasirinkite **Aplinkos kūrėjas**.</span><span class="sxs-lookup"><span data-stu-id="8d389-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Skirtukas Aplinkos vaidmenys](media/environment-roles.png)

4. <span data-ttu-id="8d389-112">Skirtuke **Vartotojai** įtraukite vartotoją arba savo organizaciją.</span><span class="sxs-lookup"><span data-stu-id="8d389-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Skirtukas Vartotojai](media/environment-maker.png)

5. <span data-ttu-id="8d389-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="8d389-114">Select **Save**.</span></span>
6. <span data-ttu-id="8d389-115">Dabar vartotojas turi prisijungti prie [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="8d389-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="8d389-116">Pasirinkite **Sinchronizuoti**, kad atnaujintumėte vartotojo programas.</span><span class="sxs-lookup"><span data-stu-id="8d389-116">Select **Sync** to update the user apps.</span></span>

    ![Sinchronizavimo mygtukas](media/get-more.png)

    <span data-ttu-id="8d389-118">Baigus sinchronizuoti, „Talent“ bus rodoma pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="8d389-118">After synchronization is completed, Talent will appear on the home page.</span></span>
