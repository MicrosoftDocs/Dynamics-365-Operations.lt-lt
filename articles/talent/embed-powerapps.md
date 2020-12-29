---
title: „Power Apps“ programų įdėjimas „Dynamics 365 Human Resources“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai „Microsoft Power Apps“ meniu elementas neberodomas sistemos administravimo modulyje.
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461954"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="97f7e-103">„Power Apps“ programų įdėjimas „Dynamics 365 Human Resources“</span><span class="sxs-lookup"><span data-stu-id="97f7e-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="97f7e-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="97f7e-104">**Issue**</span></span>

<span data-ttu-id="97f7e-105">**„Power Apps”** meniu elementas neberodomas modulyje **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="97f7e-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="97f7e-106">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="97f7e-106">**Cause**</span></span>

<span data-ttu-id="97f7e-107">Pakeistas vartotojo sąsajos (UI) dizainas, todėl dabar „Microsoft Power Apps“ įtrauktas į standartinį personalizavimo modelį.</span><span class="sxs-lookup"><span data-stu-id="97f7e-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="97f7e-108">**Nutarimas**</span><span class="sxs-lookup"><span data-stu-id="97f7e-108">**Resolution**</span></span>

<span data-ttu-id="97f7e-109">Pakeistas „Power Apps“ įdėjimo būdas.</span><span class="sxs-lookup"><span data-stu-id="97f7e-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="97f7e-110">Dabar „Power Apps“ įtraukiamos per personalizavimo modelį.</span><span class="sxs-lookup"><span data-stu-id="97f7e-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="97f7e-111">„Power Apps“ galite įtraukti beveik į visus „Microsoft Dynamics 365 Talent“ puslapius.</span><span class="sxs-lookup"><span data-stu-id="97f7e-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="97f7e-112">Norėdami gauti informacijos apie tai, kaip „Power Apps“ įdėti į „Talent“, žr. [„Power Apps“ įdėjimas](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="97f7e-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="97f7e-113">Tie „Power Apps“ klientai, kurie programas įdėjo iki keitimo, turi atnaujinti programą į naują modelį.</span><span class="sxs-lookup"><span data-stu-id="97f7e-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="97f7e-114">Mygtukas **„Power Apps”** pateiktas beveik kiekvieno „Talent“ puslapio viršutiniame dešiniajame kampe.</span><span class="sxs-lookup"><span data-stu-id="97f7e-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="97f7e-115">Šį mygtuką galite naudoti norėdami įterpti programas.</span><span class="sxs-lookup"><span data-stu-id="97f7e-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="97f7e-116">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="97f7e-116">Here is an example.</span></span>

1. <span data-ttu-id="97f7e-117">Eikite į **Personalo valdymas \> Nuorodos \> Darbininkai \> Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="97f7e-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="97f7e-118">Pasirinkite mygtuką **„Power Apps“**, tada pasirinkite **Įtraukti programą iš „Power Apps“**.</span><span class="sxs-lookup"><span data-stu-id="97f7e-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Mygtukas „Power Apps”](media/png.png)

3. <span data-ttu-id="97f7e-120">Užpildykite laukus, esančius dialogo lange **Įtraukti programą iš „Power Apps“**.</span><span class="sxs-lookup"><span data-stu-id="97f7e-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Dialogo langas Įtraukti programą iš „Power Apps“](media/insert-powerapp.png)

<span data-ttu-id="97f7e-122">Arba atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="97f7e-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="97f7e-123">Puslapio veiksmų srityje skirtuke **Parinktys** grupėje **Pritaikyti asmeniniams poreikiams** pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**.</span><span class="sxs-lookup"><span data-stu-id="97f7e-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Grupės personalizavimas skirtuke Parinktys](media/options.png)

    <span data-ttu-id="97f7e-125">Parodoma personalizavimo įrankių juosta.</span><span class="sxs-lookup"><span data-stu-id="97f7e-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="97f7e-126">Įrankių juostoje pasirinkite **Įtraukti programą iš „Power Apps“**.</span><span class="sxs-lookup"><span data-stu-id="97f7e-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Įtraukti programą iš „Power Apps“ naudojant personalizavimo įrankių juostą](media/powerapp-bar.png)
