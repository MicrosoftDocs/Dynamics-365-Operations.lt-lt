---
title: „PowerApps“ programų įdėjimas „Core HR“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai „PowerApps“ meniu elementas neberodomas sistemos administravimo modulyje.
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
ms.openlocfilehash: e3b20e1d0a873c32b8f6f5e28f786febf62db355
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "859556"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="fd6ca-103">„PowerApps“ programų įdėjimas „Core HR“</span><span class="sxs-lookup"><span data-stu-id="fd6ca-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fd6ca-104">**Problema**</span><span class="sxs-lookup"><span data-stu-id="fd6ca-104">**Issue**</span></span>

<span data-ttu-id="fd6ca-105">**PowerApps** meniu elementas neberodomas modulyje **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="fd6ca-106">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="fd6ca-106">**Cause**</span></span>

<span data-ttu-id="fd6ca-107">Pakeistas vartotojo sąsajos (UI) dizainas, todėl dabar „Microsoft PowerApps“ įtrauktas į standartinį personalizavimo modelį.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="fd6ca-108">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="fd6ca-108">**Resolution**</span></span>

<span data-ttu-id="fd6ca-109">Pakeistas „PowerApps“ programų įdėjimo būdas.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="fd6ca-110">Dabar „PowerApps“ programos įtraukiamos per personalizavimo modelį.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="fd6ca-111">„PowerApps“ programų galite įtraukti beveik į visus „Microsoft Dynamics 365 for Talent“ puslapius.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="fd6ca-112">Norėdami gauti informacijos apie tai, kaip „PowerApps“ programas įdėti į „Talent“, žr. [„PowerApps“ programų įdėjimas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="fd6ca-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="fd6ca-113">Tie „PowerApps“ klientai, kurie programas įdėjo iki keitimo, turi atnaujinti programą į naują modelį.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="fd6ca-114">Mygtukas **PowerApps** pateiktas beveik kiekvieno „Talent“ puslapio viršutiniame dešiniajame kampe.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="fd6ca-115">Šį mygtuką galite naudoti norėdami įterpti „PowerApps“ programą.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="fd6ca-116">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-116">Here is an example.</span></span>

1. <span data-ttu-id="fd6ca-117">Eikite į **Personalo valdymas \> Nuorodos \> Darbininkai \> Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="fd6ca-118">Pasirinkite mygtuką **PowerApps**, tada pasirinkite **Įterpti „PowerApp“**.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![Mygtukas „PowerApps“](media/png.png)

3. <span data-ttu-id="fd6ca-120">Užpildykite laukus, pateiktus dialogo lange **Įterpti „PowerApp“**.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialogo langas Įterpti „PowerApp“](media/insert-powerapp.png)

<span data-ttu-id="fd6ca-122">Arba atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="fd6ca-123">Puslapio srityje Veiksmas, pateiktoje grupės **Personalizavimas** skirtuke **Parinktys**, pasirinkite **Personalizuoti šią formą**.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Grupės personalizavimas skirtuke Parinktys](media/options.png)

    <span data-ttu-id="fd6ca-125">Parodoma personalizavimo įrankių juosta.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="fd6ca-126">Įrankių juostoje pasirinkite **Įterpti \> „PowerApp“**.</span><span class="sxs-lookup"><span data-stu-id="fd6ca-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![„PowerApps“ programos įterpimas naudojant personalizavimo įrankių juostą](media/powerapp-bar.png)
