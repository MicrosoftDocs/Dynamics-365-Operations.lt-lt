---
title: „Power Apps“ programų įdėjimas „Dynamics 365 - Core HR“
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
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830214"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="423d7-103">„Power Apps“ programų įdėjimas „Dynamics 365 - Core HR“</span><span class="sxs-lookup"><span data-stu-id="423d7-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="423d7-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="423d7-104">**Issue**</span></span>

<span data-ttu-id="423d7-105">**„Power Apps”** meniu elementas neberodomas modulyje **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="423d7-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="423d7-106">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="423d7-106">**Cause**</span></span>

<span data-ttu-id="423d7-107">Pakeistas vartotojo sąsajos (UI) dizainas, todėl dabar „Microsoft Power Apps“ įtrauktas į standartinį personalizavimo modelį.</span><span class="sxs-lookup"><span data-stu-id="423d7-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="423d7-108">**Nutarimas**</span><span class="sxs-lookup"><span data-stu-id="423d7-108">**Resolution**</span></span>

<span data-ttu-id="423d7-109">Pakeistas „Power Apps“ įdėjimo būdas.</span><span class="sxs-lookup"><span data-stu-id="423d7-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="423d7-110">Dabar „Power Apps“ įtraukiamos per personalizavimo modelį.</span><span class="sxs-lookup"><span data-stu-id="423d7-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="423d7-111">„Power Apps“ galite įtraukti beveik į visus „Microsoft Dynamics 365 Talent“ puslapius.</span><span class="sxs-lookup"><span data-stu-id="423d7-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="423d7-112">Norėdami gauti informacijos apie tai, kaip „Power Apps“ įdėti į „Talent“, žr. [„Microsoft Power Apps“ įdėjimas](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="423d7-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="423d7-113">Tie „Power Apps“ klientai, kurie programas įdėjo iki keitimo, turi atnaujinti programą į naują modelį.</span><span class="sxs-lookup"><span data-stu-id="423d7-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="423d7-114">Mygtukas **„Power Apps”** pateiktas beveik kiekvieno „Talent“ puslapio viršutiniame dešiniajame kampe.</span><span class="sxs-lookup"><span data-stu-id="423d7-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="423d7-115">Šį mygtuką galite naudoti norėdami įterpti „Power Apps“.</span><span class="sxs-lookup"><span data-stu-id="423d7-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="423d7-116">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="423d7-116">Here is an example.</span></span>

1. <span data-ttu-id="423d7-117">Eikite į **Personalo valdymas \> Nuorodos \> Darbininkai \> Darbuotojai**.</span><span class="sxs-lookup"><span data-stu-id="423d7-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="423d7-118">Pasirinkite mygtuką **„Power Apps”**, tada pasirinkite **Įterpti „PowerApp“**.</span><span class="sxs-lookup"><span data-stu-id="423d7-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Mygtukas „Power Apps”](media/png.png)

3. <span data-ttu-id="423d7-120">Užpildykite laukus, pateiktus dialogo lange **Įterpti „PowerApp“**.</span><span class="sxs-lookup"><span data-stu-id="423d7-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Dialogo langas Įterpti „PowerApp“](media/insert-powerapp.png)

<span data-ttu-id="423d7-122">Arba atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="423d7-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="423d7-123">Puslapio srityje Veiksmas, pateiktoje grupės **Personalizavimas** skirtuke **Parinktys**, pasirinkite **Personalizuoti šią formą**.</span><span class="sxs-lookup"><span data-stu-id="423d7-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Grupės personalizavimas skirtuke Parinktys](media/options.png)

    <span data-ttu-id="423d7-125">Parodoma personalizavimo įrankių juosta.</span><span class="sxs-lookup"><span data-stu-id="423d7-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="423d7-126">Įrankių juostoje pasirinkite **Įterpti \> „PowerApp“**.</span><span class="sxs-lookup"><span data-stu-id="423d7-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![„Power Apps“ programos įterpimas naudojant personalizavimo įrankių juostą](media/powerapp-bar.png)
