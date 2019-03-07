---
title: URL atidarymas EKA
description: Šioje temoje apžvelgiama, kaip patobulinta „Microsoft Dynamics 365 for Retail“ produktų ir klientų ieškos funkcija.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b07406b4e218b45bdde87c4a579814fe0edbc286
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "327095"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="76ad9-103">URL atidarymas elektroniniame kasos aparate</span><span class="sxs-lookup"><span data-stu-id="76ad9-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="76ad9-104">Šioje temoje aprašoma, kaip galite sukonfigūruoti mygtuką „Retail“ elektroniniame kasos aparate (POS), kad būtų galima atidaryti URL.</span><span class="sxs-lookup"><span data-stu-id="76ad9-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="76ad9-105">Šiai funkcija įjungti nereikia tinkinti kodo, taip pat ją sukonfigūruoti gali bet kuris vartotojas, turintis ne kūrėjo vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="76ad9-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="76ad9-106">Ši funkcija veikia „Dynamics 365 for Finance and Operations“ 8.1.3 versijos (komponavimo versija: 8.1.227.10014) ir naujesniuose leidimuose.</span><span class="sxs-lookup"><span data-stu-id="76ad9-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="76ad9-107">Ši funkcija leidžia sukonfigūruoti EKA mygtuką naudojant mygtukyno dizaino įrankį, kad būtų galima atidaryti URL.</span><span class="sxs-lookup"><span data-stu-id="76ad9-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="76ad9-108">Šiuo metu atidaryti URL galima toliau nurodytomis konfigūracijomis.</span><span class="sxs-lookup"><span data-stu-id="76ad9-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="76ad9-109">Atidaryti naujame lange.</span><span class="sxs-lookup"><span data-stu-id="76ad9-109">Open in new window.</span></span>
- <span data-ttu-id="76ad9-110">Atidaryti pačiame EKA.</span><span class="sxs-lookup"><span data-stu-id="76ad9-110">Open within POS.</span></span>
- <span data-ttu-id="76ad9-111">Atidaryti vietinėje programoje.</span><span class="sxs-lookup"><span data-stu-id="76ad9-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="76ad9-112">Atidaryti naujame lange</span><span class="sxs-lookup"><span data-stu-id="76ad9-112">Open in new window</span></span>

<span data-ttu-id="76ad9-113">Šia konfigūracija apibrėžiama, ar URL atidaryti naujame lange, ar pačioje programoje.</span><span class="sxs-lookup"><span data-stu-id="76ad9-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="76ad9-114">Sukonfigūravus atidaryti interneto URL pačioje programoje, matoma šoninė naršymo sritis ir EKA viršutinė juosta, su kuriomis vartotojas gali sąveikauti.</span><span class="sxs-lookup"><span data-stu-id="76ad9-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="76ad9-115">Sukonfigūravus atidaryti naujame lange, URL bus atidarytas naujame „Modern POS“, skirto „Windows“, programos lange, o visų kitų EKA klientų atveju – naujame naršyklės skirtuke.</span><span class="sxs-lookup"><span data-stu-id="76ad9-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="76ad9-116">Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti pasirinkę parinktį **Atidaryti naujame lange**.</span><span class="sxs-lookup"><span data-stu-id="76ad9-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="76ad9-117">Atidaryti pačiame EKA</span><span class="sxs-lookup"><span data-stu-id="76ad9-117">Open within POS</span></span>

<span data-ttu-id="76ad9-118">Šiuo metu galimybė atidaryti interneto URL pačiame EKA palaikoma tik „Modern POS“, skirtame „Windows“.</span><span class="sxs-lookup"><span data-stu-id="76ad9-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="76ad9-119">Kitiems klientams ši funkcija dar kuriama ir ją planuojama išleisti kartu su būsimais naujinimais.</span><span class="sxs-lookup"><span data-stu-id="76ad9-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="76ad9-120">Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti nepasirinkę parinkties **Atidaryti naujame lange**.</span><span class="sxs-lookup"><span data-stu-id="76ad9-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="76ad9-121">Atidaryti vietinėje programoje</span><span class="sxs-lookup"><span data-stu-id="76ad9-121">Open a native app</span></span>

<span data-ttu-id="76ad9-122">Ši funkcija leidžia jums nurodyti ne interneto URL, kad būtų galima atidaryti vietinėje programoje.</span><span class="sxs-lookup"><span data-stu-id="76ad9-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="76ad9-123">Pavyzdžiui, galite nurodyti URL protokolus, pvz., „MailTo“, SIP, IM arba MSTEAMS, kuriuos vėliau galima sutvarkyti naudojant atitinkamas prieglobos įrenginio vietines programas.</span><span class="sxs-lookup"><span data-stu-id="76ad9-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="76ad9-124">Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti pasirinkę parinktį **Atidaryti naujame lange**.</span><span class="sxs-lookup"><span data-stu-id="76ad9-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="76ad9-125">Jei naudojate kompiuterius, kuriuose įdiegti „Windows“, žr. [Numatytųjų programos susiejimų eksportavimas arba importavimas](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), kad nustatytumėte numatytąsias protokolo asociacijas, kai kompiuterį nustatote naudodamiesi vaizdų aptarnavimo ir tvarkymo visuotinio diegimo (DISM) sprendimu.</span><span class="sxs-lookup"><span data-stu-id="76ad9-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="76ad9-126">Jei „Windows“ kompiuteriams valdyti naudojate MDM, pvz., „Intune“, žr. [Strategijos CSP – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="76ad9-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="76ad9-127">Jei esate kūrėjas, kuriant pasirinktinę žiniatinklio svetainę, žr. [Numatytosios programos URI paleidimas](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="76ad9-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="76ad9-128">Sklandus atidarymas vietinėje programoje</span><span class="sxs-lookup"><span data-stu-id="76ad9-128">Open a native app seamlessly</span></span>

<span data-ttu-id="76ad9-129">„Windows“, „iOS“ ir „Android“ taip pat leidžiama sklandžiau atidaryti daugiau programų, priklausomai nuo programos protokolo susiejimo.</span><span class="sxs-lookup"><span data-stu-id="76ad9-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="76ad9-130">Jei jūsų programa dar nesukonfigūruota taip, kad atidarymą galėtų tvarkyti interneto naršyklėje, šiai funkcijai sukonfigūruoti gali prireikti kūrėjo paslaugų.</span><span class="sxs-lookup"><span data-stu-id="76ad9-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="76ad9-131">Jei naudojate „Windows“, žr. [Programų žiniatinklio svetainėms įgalinimas naudojant URI apdorojimo programas](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="76ad9-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="76ad9-132">Jei naudojate „iOS“, žr. [Kūrėjams skirtos universalios nuorodos](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="76ad9-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="76ad9-133">Jei naudojate „Android“, žr. [„Android“ programos nuorodų tvarkymas](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="76ad9-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="76ad9-134">Klientas</span><span class="sxs-lookup"><span data-stu-id="76ad9-134">Client</span></span>                | <span data-ttu-id="76ad9-135">Atidaryti naujame lange</span><span class="sxs-lookup"><span data-stu-id="76ad9-135">Open in new window</span></span> | <span data-ttu-id="76ad9-136">Atidaryti vietinėje programoje</span><span class="sxs-lookup"><span data-stu-id="76ad9-136">Open native app</span></span> | <span data-ttu-id="76ad9-137">Atidaryti pačiame EKA</span><span class="sxs-lookup"><span data-stu-id="76ad9-137">Open within POS</span></span> | <span data-ttu-id="76ad9-138">Informacija</span><span class="sxs-lookup"><span data-stu-id="76ad9-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="76ad9-139">„Windows“ skirtas „Modern POS“</span><span class="sxs-lookup"><span data-stu-id="76ad9-139">Modern POS on Windows</span></span> | <span data-ttu-id="76ad9-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="76ad9-140">✓\*</span></span>                | <span data-ttu-id="76ad9-141">✓</span><span class="sxs-lookup"><span data-stu-id="76ad9-141">✓</span></span>               | <span data-ttu-id="76ad9-142">✓</span><span class="sxs-lookup"><span data-stu-id="76ad9-142">✓</span></span>              | <span data-ttu-id="76ad9-143">\* Atidaroma naujame „Modern POS“ lange</span><span class="sxs-lookup"><span data-stu-id="76ad9-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="76ad9-144">„Cloud POS“</span><span class="sxs-lookup"><span data-stu-id="76ad9-144">Cloud POS</span></span>             | <span data-ttu-id="76ad9-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="76ad9-145">✓\*</span></span>                | <span data-ttu-id="76ad9-146">✓</span><span class="sxs-lookup"><span data-stu-id="76ad9-146">✓</span></span>               | <span data-ttu-id="76ad9-147">X</span><span class="sxs-lookup"><span data-stu-id="76ad9-147">X</span></span>              | <span data-ttu-id="76ad9-148">\* Atidaroma naujame naršyklės skirtuke</span><span class="sxs-lookup"><span data-stu-id="76ad9-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="76ad9-149">„iOS“ skirtas „Modern POS“</span><span class="sxs-lookup"><span data-stu-id="76ad9-149">Modern POS on iOS</span></span>     | <span data-ttu-id="76ad9-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="76ad9-150">✓\*</span></span>                | <span data-ttu-id="76ad9-151">✓</span><span class="sxs-lookup"><span data-stu-id="76ad9-151">✓</span></span>               | <span data-ttu-id="76ad9-152">X</span><span class="sxs-lookup"><span data-stu-id="76ad9-152">X</span></span>              | <span data-ttu-id="76ad9-153">\* Atidaroma naujame naršyklės skirtuke</span><span class="sxs-lookup"><span data-stu-id="76ad9-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="76ad9-154">„Modern POS“ sistemovairuotoje „Android“</span><span class="sxs-lookup"><span data-stu-id="76ad9-154">Modern POS on Android</span></span> | <span data-ttu-id="76ad9-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="76ad9-155">✓\*</span></span>                | <span data-ttu-id="76ad9-156">✓</span><span class="sxs-lookup"><span data-stu-id="76ad9-156">✓</span></span>               | <span data-ttu-id="76ad9-157">X</span><span class="sxs-lookup"><span data-stu-id="76ad9-157">X</span></span>              | <span data-ttu-id="76ad9-158">\* Atidaroma naujame naršyklės skirtuke</span><span class="sxs-lookup"><span data-stu-id="76ad9-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="76ad9-159">Prieš pradedant</span><span class="sxs-lookup"><span data-stu-id="76ad9-159">Before you begin</span></span>

<span data-ttu-id="76ad9-160">Prieš pradėdami, peržiūrėkite, kaip konfigūruoti [elektroninio kasos aparato (EKA) ekrano maketus](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="76ad9-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="76ad9-161">URL atidarymas EKA</span><span class="sxs-lookup"><span data-stu-id="76ad9-161">Open URL in POS</span></span>

<span data-ttu-id="76ad9-162">Norėdami sukonfigūruoti URL taip, kad jį būtų galima atidaryti EKA, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="76ad9-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="76ad9-163">Pagrindinio biuro srityje eikite į **Mažmeninė prekyba \> Kanalo sąranka \> EKA sąranka \> EKA \> Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="76ad9-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="76ad9-164">Pasirinkite **Mygtukynai \> Kūrimo įrankis**.</span><span class="sxs-lookup"><span data-stu-id="76ad9-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="76ad9-165">Sukurkite naują mygtuką.</span><span class="sxs-lookup"><span data-stu-id="76ad9-165">Create a new button.</span></span>
4. <span data-ttu-id="76ad9-166">Pasirinkite **mygtuko** ypatybes.</span><span class="sxs-lookup"><span data-stu-id="76ad9-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="76ad9-167">Kaip veiksmą pasirinkite **Atidaryti URL**.</span><span class="sxs-lookup"><span data-stu-id="76ad9-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="76ad9-168">Įveskite norimą naudoti URL.</span><span class="sxs-lookup"><span data-stu-id="76ad9-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="76ad9-169">Sukonfigūruokite, ar norite, kad URL būtų atidaromas naujame lange.</span><span class="sxs-lookup"><span data-stu-id="76ad9-169">Configure whether to open the URL in a new window.</span></span>
