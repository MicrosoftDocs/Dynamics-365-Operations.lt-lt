---
title: Sukurti gamybos aukšto vykdymo sąsają
description: Šioje temoje aprašoma, kaip sukurti vartotojo sąsajos turinį kiekvienam konfigūravimui.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664277"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="aaa00-103">Sukurti gamybos aukšto vykdymo sąsają</span><span class="sxs-lookup"><span data-stu-id="aaa00-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="aaa00-104">Galite sukurti vartotojo sąsajos turinį kiekvienam konfigūravimui naudojamui gamybos aukšto vykdymo sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="aaa00-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="aaa00-105">Pavyzdžiui, darbuotojams viename darbo laukelyje gali reikėti atverti darbo instrukcijas gamybos aukšte, o kitame darbo laukelyje, instrukcijų nereikia.</span><span class="sxs-lookup"><span data-stu-id="aaa00-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="aaa00-106">Tokiu atveju, reikia sukurti du konfigūravimus, vieną su mygtuku dokumentų priedų atvėrimui ir vieną be šio mygtuko.</span><span class="sxs-lookup"><span data-stu-id="aaa00-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="aaa00-107">Sukurkite skirtuką</span><span class="sxs-lookup"><span data-stu-id="aaa00-107">Design a tab</span></span>

<span data-ttu-id="aaa00-108">Puslapyje **Konfigūruoti gamybos aukšto vykdymą** galite sukurti ir konfigūruoti skirtukus pasirinkdami **Kurti skirtukus** veiksmų juostoje.</span><span class="sxs-lookup"><span data-stu-id="aaa00-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="aaa00-109">Visi skirtukai padalyti į keturis skyrius kaip parodyti tolesniame paveisklėlyje.</span><span class="sxs-lookup"><span data-stu-id="aaa00-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="aaa00-110">![Skirtuko išdėstymas](media/pfe-tab-layout.png "Skirtuko išdėstymas")</span><span class="sxs-lookup"><span data-stu-id="aaa00-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="aaa00-111">Tolesni elementai rodomi paveikslėlyje:</span><span class="sxs-lookup"><span data-stu-id="aaa00-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="aaa00-112">Pagrindinė įrankių juosta</span><span class="sxs-lookup"><span data-stu-id="aaa00-112">Primary toolbar</span></span>
1. <span data-ttu-id="aaa00-113">Antrinė įrankių juosta</span><span class="sxs-lookup"><span data-stu-id="aaa00-113">Secondary toolbar</span></span>
1. <span data-ttu-id="aaa00-114">Pagrindinis rodinys</span><span class="sxs-lookup"><span data-stu-id="aaa00-114">Main view</span></span>
1. <span data-ttu-id="aaa00-115">Išsamus rodinys</span><span class="sxs-lookup"><span data-stu-id="aaa00-115">Detailed view</span></span>

<span data-ttu-id="aaa00-116">Norėdami sukurti ir konfigūruoti naują skirtuką, atlikite šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="aaa00-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="aaa00-117">Eikite į **Gamybos valdymą &gt; Nusttymai &gt; Gamybos vykdymas**.</span><span class="sxs-lookup"><span data-stu-id="aaa00-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="aaa00-118">Rinkitės **Sukurti skirtukus** veiksmų juostoje, tam, kad atvertumėte **Kūrimo skirtukų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="aaa00-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="aaa00-119">![Kūrimo skirtukų puslapis](media/pfe-design-tabs.png "Kūrimo skirtukų puslapis")</span><span class="sxs-lookup"><span data-stu-id="aaa00-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="aaa00-120">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="aaa00-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="aaa00-121">Nustatykite tolesnius nustatymus antraštės puslapyje:</span><span class="sxs-lookup"><span data-stu-id="aaa00-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="aaa00-122">**Skirtuko pavadinimas** - Nurodykite skirtuko pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="aaa00-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="aaa00-123">**Pagrindinis rodinys** - Pasirinkite tarp dviejų iš anksto nustatytų darbo sąrašų (*Įjungti darbai* ar *Visi darbai*).</span><span class="sxs-lookup"><span data-stu-id="aaa00-123">**Main view** - Select between the two pre-defined job lists (*Active jobs* or *All jobs*).</span></span>
    - <span data-ttu-id="aaa00-124">**Išsamios informacijos rodinys** - Pasirinkite tarp tuščios vertės ar **Išsamios darbo informacijos**.</span><span class="sxs-lookup"><span data-stu-id="aaa00-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="aaa00-125">Jei pasirinkote tuščią vertę, nebus jokio išsamios informacijos rodinio skirtuke. Jei pasirinkote **Išsami darbo informacija**, išsamiame rodinyje bus išsamus darbo aprašas iš pasirinkto darbo aprašo pagrindiniame rodinyje.</span><span class="sxs-lookup"><span data-stu-id="aaa00-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="aaa00-126">Skyriuje **Pirminė įrankių juosta** pasirinkite, kurie mygtukai turi būti prieinami pirminėje įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="aaa00-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="aaa00-127">Stulpelis **Prieinami veiksmai** rodo visų mygtukų sąrašą, kurie gali būti įtraukti.</span><span class="sxs-lookup"><span data-stu-id="aaa00-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="aaa00-128">Stulpelis **Pasirinkti veiksmai** rodo visų mygtukų, įtrauktų į esamą organizaciją, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="aaa00-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="aaa00-129">Naudokite mygtukus tarp stulpelių, kad judintumėte pasirinktas prekes tarp stuleplių, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="aaa00-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="aaa00-130">Naudokite mygtukus į viršų ir į apačią šalia **Pasirinkti veiksmai** stulpelius, kad valdytumėte užsakymą, kuriame mygtukai yra rodomi vartotojo sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="aaa00-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="aaa00-131">Skyriuje **Antroji** **įrankių juosta** pasirinkite, kurie mygtukai turi būti prieinami antrojoje įrankių juostoje.</span><span class="sxs-lookup"><span data-stu-id="aaa00-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="aaa00-132">Stulpelis **Prieinami veiksmai** rodo visų mygtukų sąrašą, kurie gali būti įtraukti.</span><span class="sxs-lookup"><span data-stu-id="aaa00-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="aaa00-133">Stulpelis **Pasirinkti veiksmai** rodo visų mygtukų, įtrauktų į esamą organizaciją, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="aaa00-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="aaa00-134">Naudokite mygtukus tarp stulpelių, kad judintumėte pasirinktas prekes tarp stuleplių, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="aaa00-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="aaa00-135">Naudokite mygtukus į viršų ir į apačią šalia **Pasirinkti veiksmai** stulpelius, kad valdytumėte užsakymą, kuriame mygtukai yra rodomi vartotojo sąsajoje.</span><span class="sxs-lookup"><span data-stu-id="aaa00-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="aaa00-136">Susiekite skirtuką su konfigūravimu</span><span class="sxs-lookup"><span data-stu-id="aaa00-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="aaa00-137">Jums sukūrųs visus būtinus skirtukus, galite susieti juos su konfigūravimu.</span><span class="sxs-lookup"><span data-stu-id="aaa00-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="aaa00-138">Eikite į **Gamybos valdymą &gt; Nusttymai &gt; Konfigūravimo gamybos aukšto vykdymas**.</span><span class="sxs-lookup"><span data-stu-id="aaa00-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="aaa00-139">![Konfigūruoti gamybos vietos vykdymą](media/pfe-config-prod-floor-execution.png "Konfigūruoti gamybos vietos vykdymą")</span><span class="sxs-lookup"><span data-stu-id="aaa00-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="aaa00-140">„FastTab“ **Skirtuko pasirinkimas** rinkitės **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="aaa00-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="aaa00-141">Nauja eilutė yra įtraukta į tinklelį.</span><span class="sxs-lookup"><span data-stu-id="aaa00-141">A new row is added to the grid.</span></span> <span data-ttu-id="aaa00-142">Šiai naujai eilutei, pasirinkite skirtuko pavadinimą, kurį norite įtraukti į konfigūravimą.</span><span class="sxs-lookup"><span data-stu-id="aaa00-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="aaa00-143">Tęskite įtraukdami papildomus skirtukus, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="aaa00-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="aaa00-144">Naudokite mygtukus **Judėti aukštyn** ir **Judėti žemyn** įrankių juostoje, kad sudėliotumėte skirtukus kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="aaa00-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="aaa00-145">Skirtukai bus rodomi iš kairės į dešinę tvarka rodoma virš momentinės ekrano nuotraukos (skirtukos viršuje rodomas kairėje).</span><span class="sxs-lookup"><span data-stu-id="aaa00-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>
