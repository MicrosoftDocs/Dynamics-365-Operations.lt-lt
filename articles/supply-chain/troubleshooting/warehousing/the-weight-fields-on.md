---
title: Krovinio eilučių svorio laukai neatitinka krovinio svorio laukų
description: Krovinio eilučių svorio laukai neatitinka krovinio svorio laukų
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924356"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="0057d-103">Krovinio eilučių svorio laukai neatitinka krovinio svorio laukų</span><span class="sxs-lookup"><span data-stu-id="0057d-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="0057d-104">Klaidos kodai: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="0057d-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="0057d-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="0057d-105">Symptoms</span></span>

<span data-ttu-id="0057d-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="0057d-106">The system shows the following error message:</span></span>

> <span data-ttu-id="0057d-107">Krovinio eilučių svorio laukai neatitinka krovinio svorio laukų %1.</span><span class="sxs-lookup"><span data-stu-id="0057d-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="0057d-108">Paleiskite sandėlio krovinio svorio vientisumo tikrinkite, ar norite perskaičiuoti svorio laukus.</span><span class="sxs-lookup"><span data-stu-id="0057d-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="0057d-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="0057d-109">Cause</span></span>

<span data-ttu-id="0057d-110">**Grynasis svoris** ir **Taros svoris** laukeliai yra nustatyti į *0* (nulį) pakrovimo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0057d-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="0057d-111">Tačiau produkto svorio matavimo svorio laukai *nėra* nustatomi kaip 0.</span><span class="sxs-lookup"><span data-stu-id="0057d-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="0057d-112">Jei krovinio eilutėje nėra nustatyti svorio laukai, bet kokie kiekio koregavimai krovinio eilutėje gali svorio skaičiavimą atlikti neteisingai.</span><span class="sxs-lookup"><span data-stu-id="0057d-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="0057d-113">Ši problema gali kilti, jei sukūrus krovinio eilutę produkto svoris buvo pakeistas.</span><span class="sxs-lookup"><span data-stu-id="0057d-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="0057d-114">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="0057d-114">Resolution</span></span>

<span data-ttu-id="0057d-115">Pagal numatytuosius nustatymus, kai sukuriama krovinio eilutė, į ją įvedami produkto svorio laukai.</span><span class="sxs-lookup"><span data-stu-id="0057d-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="0057d-116">Jei svoris lygus nuliui, galite jį perskaičiuoti naudodami sandėlio *krovinio svorio vientisumo* tikrinimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="0057d-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="0057d-117">Eikite į **Sistemos administravimas \> Periodinės užduotys \> Duomenš bazę \> Periodinis tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="0057d-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="0057d-118">Žymės **langelyje** Vientisumas nustatykite **modulio** lauką kaip *Sandėlio* valdymas.</span><span class="sxs-lookup"><span data-stu-id="0057d-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="0057d-119">Nustatykite **Tikrinti/Taisyti** laukelį į *Taisyti klaidą*.</span><span class="sxs-lookup"><span data-stu-id="0057d-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="0057d-120">Žymės langelyje pažymėkite žymės langelį Sandėlio krovinio svorio nuoseklumas ir įsitikinkite, kad pažymėtas **tik** šio žymės langelio eilutė.</span><span class="sxs-lookup"><span data-stu-id="0057d-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="0057d-121">Žymės langelio sąrašo viršuje pasirinkite elipsės mygtuką (... ), tada **meniu** pasirinkite **Tekstas**.</span><span class="sxs-lookup"><span data-stu-id="0057d-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="0057d-122">Sandėlio **krovinio svorio vientisumo žymės lange nustatykite šiuos laukus, norėdami nurodyti kriterijus, pagal** kuriuos turėtų būti vykdomas vientisumo tikrinimas:</span><span class="sxs-lookup"><span data-stu-id="0057d-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="0057d-123">**Krovinio ID:** nurodykite krovinio ID.</span><span class="sxs-lookup"><span data-stu-id="0057d-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="0057d-124">Palikite šį tuščią, jei norite patikrinti visus krovinio ID.</span><span class="sxs-lookup"><span data-stu-id="0057d-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="0057d-125">**Prekės numeris:** nurodykite prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="0057d-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="0057d-126">Palikite šį tuščią, jei norite patikrinti visas prekes.</span><span class="sxs-lookup"><span data-stu-id="0057d-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="0057d-127">**Visada perskaičiuoti krovinio svorį:** nustatykite šią parinktį *kaip* Taip.</span><span class="sxs-lookup"><span data-stu-id="0057d-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="0057d-128">**Leisti perrašyti svorį krovinio eilutėse:** nustatykite šią parinktį *kaip* Taip.</span><span class="sxs-lookup"><span data-stu-id="0057d-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="0057d-129">Pasirinkite **Gerai,** kad uždarytumėte žymės langelį **Sandėlio krovinio svorio** vientisumas.</span><span class="sxs-lookup"><span data-stu-id="0057d-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="0057d-130">Pasirinkite elipsės mygtuką, tada **meniu** pasirinkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="0057d-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="0057d-131">Svoris perskaičiuojamas pagal jūsų nurodytus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="0057d-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="0057d-132">Pasirinkti saitą **Pranešimo** informacija, kad būtų galima peržiūrėti vientisumo tikrinimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="0057d-132">Select the **Message details** link to view the result of the consistency check.</span></span>
