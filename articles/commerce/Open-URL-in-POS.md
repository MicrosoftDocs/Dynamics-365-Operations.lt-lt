---
title: URL atidarymas EKA
description: Šioje temoje apžvelgiama, kaip patobulinta „Dynamics 365 Commerce“ produktų ir klientų ieškos funkcija.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 252b24919e4c22233ee8fe7e94c9bc6bbf60dacd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796467"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="d9b30-103">URL atidarymas elektroniniame kasos aparate</span><span class="sxs-lookup"><span data-stu-id="d9b30-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9b30-104">Šioje temoje aprašoma, kaip galite sukonfigūruoti mygtuką „Retail“ elektroniniame kasos aparate (POS), kad būtų galima atidaryti URL.</span><span class="sxs-lookup"><span data-stu-id="d9b30-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="d9b30-105">Šiai funkcija įjungti nereikia tinkinti kodo, taip pat ją sukonfigūruoti gali bet kuris vartotojas, turintis ne kūrėjo vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="d9b30-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="d9b30-106">Ši funkcija leidžia sukonfigūruoti EKA mygtuką naudojant mygtukyno dizaino įrankį, kad būtų galima atidaryti URL.</span><span class="sxs-lookup"><span data-stu-id="d9b30-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="d9b30-107">Šiuo metu atidaryti URL galima toliau nurodytomis konfigūracijomis.</span><span class="sxs-lookup"><span data-stu-id="d9b30-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="d9b30-108">Atidaryti naujame lange.</span><span class="sxs-lookup"><span data-stu-id="d9b30-108">Open in new window.</span></span>
- <span data-ttu-id="d9b30-109">Atidaryti pačiame EKA.</span><span class="sxs-lookup"><span data-stu-id="d9b30-109">Open within POS.</span></span>
- <span data-ttu-id="d9b30-110">Atidaryti vietinėje programoje.</span><span class="sxs-lookup"><span data-stu-id="d9b30-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="d9b30-111">Atidaryti naujame lange</span><span class="sxs-lookup"><span data-stu-id="d9b30-111">Open in new window</span></span>

<span data-ttu-id="d9b30-112">Šia konfigūracija apibrėžiama, ar URL atidaryti naujame lange, ar pačioje programoje.</span><span class="sxs-lookup"><span data-stu-id="d9b30-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="d9b30-113">Sukonfigūravus atidaryti interneto URL pačioje programoje, matoma šoninė naršymo sritis ir EKA viršutinė juosta, su kuriomis vartotojas gali sąveikauti.</span><span class="sxs-lookup"><span data-stu-id="d9b30-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="d9b30-114">Sukonfigūravus atidaryti naujame lange, URL bus atidarytas naujame „Modern POS“, skirto „Windows“, programos lange, o visų kitų EKA klientų atveju – naujame naršyklės skirtuke.</span><span class="sxs-lookup"><span data-stu-id="d9b30-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="d9b30-115">Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti pasirinkę parinktį **Atidaryti naujame lange**.</span><span class="sxs-lookup"><span data-stu-id="d9b30-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="d9b30-116">Atidaryti pačiame EKA</span><span class="sxs-lookup"><span data-stu-id="d9b30-116">Open within POS</span></span>

<span data-ttu-id="d9b30-117">Šiuo metu galimybė atidaryti interneto URL pačiame EKA palaikoma tik „Modern POS“, skirtame „Windows“.</span><span class="sxs-lookup"><span data-stu-id="d9b30-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="d9b30-118">Kitiems klientams ši funkcija dar kuriama ir ją planuojama išleisti kartu su būsimais naujinimais.</span><span class="sxs-lookup"><span data-stu-id="d9b30-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="d9b30-119">Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti nepasirinkę parinkties **Atidaryti naujame lange**.</span><span class="sxs-lookup"><span data-stu-id="d9b30-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="d9b30-120">Atidaryti vietinėje programoje</span><span class="sxs-lookup"><span data-stu-id="d9b30-120">Open a native app</span></span>

<span data-ttu-id="d9b30-121">Ši funkcija leidžia jums nurodyti ne interneto URL, kad būtų galima atidaryti vietinėje programoje.</span><span class="sxs-lookup"><span data-stu-id="d9b30-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="d9b30-122">Pavyzdžiui, galite nurodyti URL protokolus, pvz., „MailTo“, SIP, IM arba MSTEAMS, kuriuos vėliau galima sutvarkyti naudojant atitinkamas prieglobos įrenginio vietines programas.</span><span class="sxs-lookup"><span data-stu-id="d9b30-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="d9b30-123">Norėdami įgalinti šią funkciją, URL turite sukonfigūruoti pasirinkę parinktį **Atidaryti naujame lange**.</span><span class="sxs-lookup"><span data-stu-id="d9b30-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="d9b30-124">Jei naudojate kompiuterius, kuriuose įdiegti „Windows“, žr. [Numatytųjų programos susiejimų eksportavimas arba importavimas](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations), kad nustatytumėte numatytąsias protokolo asociacijas, kai kompiuterį nustatote naudodamiesi vaizdų aptarnavimo ir tvarkymo visuotinio diegimo (DISM) sprendimu.</span><span class="sxs-lookup"><span data-stu-id="d9b30-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="d9b30-125">Jei „Windows“ kompiuteriams valdyti naudojate MDM, pvz., „Intune“, žr. [Strategijos CSP – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="d9b30-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="d9b30-126">Jei esate kūrėjas, kuriant pasirinktinę žiniatinklio svetainę, žr. [Numatytosios programos URI paleidimas](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="d9b30-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="d9b30-127">Sklandus atidarymas vietinėje programoje</span><span class="sxs-lookup"><span data-stu-id="d9b30-127">Open a native app seamlessly</span></span>

<span data-ttu-id="d9b30-128">„Windows“, „iOS“ ir „Android“ taip pat leidžiama sklandžiau atidaryti daugiau programų, priklausomai nuo programos protokolo susiejimo.</span><span class="sxs-lookup"><span data-stu-id="d9b30-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="d9b30-129">Jei jūsų programa dar nesukonfigūruota taip, kad atidarymą galėtų tvarkyti interneto naršyklėje, šiai funkcijai sukonfigūruoti gali prireikti kūrėjo paslaugų.</span><span class="sxs-lookup"><span data-stu-id="d9b30-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="d9b30-130">Jei naudojate „Windows“, žr. [Programų žiniatinklio svetainėms įgalinimas naudojant URI apdorojimo programas](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="d9b30-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="d9b30-131">Jei naudojate „iOS“, žr. [Kūrėjams skirtos universalios nuorodos](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="d9b30-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="d9b30-132">Jei naudojate „Android“, žr. [„Android“ programos nuorodų tvarkymas](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="d9b30-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="d9b30-133">Klientas</span><span class="sxs-lookup"><span data-stu-id="d9b30-133">Client</span></span>                | <span data-ttu-id="d9b30-134">Atidaryti naujame lange</span><span class="sxs-lookup"><span data-stu-id="d9b30-134">Open in new window</span></span> | <span data-ttu-id="d9b30-135">Atidaryti vietinėje programoje</span><span class="sxs-lookup"><span data-stu-id="d9b30-135">Open native app</span></span> | <span data-ttu-id="d9b30-136">Atidaryti pačiame EKA</span><span class="sxs-lookup"><span data-stu-id="d9b30-136">Open within POS</span></span> | <span data-ttu-id="d9b30-137">Informacija</span><span class="sxs-lookup"><span data-stu-id="d9b30-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="d9b30-138">„Windows“ skirtas „Modern POS“</span><span class="sxs-lookup"><span data-stu-id="d9b30-138">Modern POS on Windows</span></span> | <span data-ttu-id="d9b30-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="d9b30-139">✓\*</span></span>                | <span data-ttu-id="d9b30-140">✓</span><span class="sxs-lookup"><span data-stu-id="d9b30-140">✓</span></span>               | <span data-ttu-id="d9b30-141">✓</span><span class="sxs-lookup"><span data-stu-id="d9b30-141">✓</span></span>              | <span data-ttu-id="d9b30-142">\* Atidaroma naujame „Modern POS“ lange</span><span class="sxs-lookup"><span data-stu-id="d9b30-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="d9b30-143">„Cloud POS“</span><span class="sxs-lookup"><span data-stu-id="d9b30-143">Cloud POS</span></span>             | <span data-ttu-id="d9b30-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="d9b30-144">✓\*</span></span>                | <span data-ttu-id="d9b30-145">✓</span><span class="sxs-lookup"><span data-stu-id="d9b30-145">✓</span></span>               | <span data-ttu-id="d9b30-146">X</span><span class="sxs-lookup"><span data-stu-id="d9b30-146">X</span></span>              | <span data-ttu-id="d9b30-147">\* Atidaroma naujame naršyklės skirtuke</span><span class="sxs-lookup"><span data-stu-id="d9b30-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="d9b30-148">„iOS“ skirtas „Modern POS“</span><span class="sxs-lookup"><span data-stu-id="d9b30-148">Modern POS on iOS</span></span>     | <span data-ttu-id="d9b30-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="d9b30-149">✓\*</span></span>                | <span data-ttu-id="d9b30-150">✓</span><span class="sxs-lookup"><span data-stu-id="d9b30-150">✓</span></span>               | <span data-ttu-id="d9b30-151">X</span><span class="sxs-lookup"><span data-stu-id="d9b30-151">X</span></span>              | <span data-ttu-id="d9b30-152">\* Atidaroma naujame naršyklės skirtuke</span><span class="sxs-lookup"><span data-stu-id="d9b30-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="d9b30-153">„Modern POS“, skirtas „Android“</span><span class="sxs-lookup"><span data-stu-id="d9b30-153">Modern POS on Android</span></span> | <span data-ttu-id="d9b30-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="d9b30-154">✓\*</span></span>                | <span data-ttu-id="d9b30-155">✓</span><span class="sxs-lookup"><span data-stu-id="d9b30-155">✓</span></span>               | <span data-ttu-id="d9b30-156">X</span><span class="sxs-lookup"><span data-stu-id="d9b30-156">X</span></span>              | <span data-ttu-id="d9b30-157">\* Atidaroma naujame naršyklės skirtuke</span><span class="sxs-lookup"><span data-stu-id="d9b30-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="d9b30-158">Prieš pradedant</span><span class="sxs-lookup"><span data-stu-id="d9b30-158">Before you begin</span></span>

<span data-ttu-id="d9b30-159">Prieš pradėdami, peržiūrėkite, kaip konfigūruoti [elektroninio kasos aparato (EKA) ekrano maketus](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="d9b30-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="d9b30-160">URL atidarymas EKA</span><span class="sxs-lookup"><span data-stu-id="d9b30-160">Open URL in POS</span></span>

<span data-ttu-id="d9b30-161">Norėdami sukonfigūruoti URL taip, kad jį būtų galima atidaryti EKA, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d9b30-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="d9b30-162">Pagrindiniame biure eikite į **„Retail and Commerce“ \> Kanalo sąranka \> EKA sąranka \> EKA \> Ekrano maketai**.</span><span class="sxs-lookup"><span data-stu-id="d9b30-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="d9b30-163">Pasirinkite **Mygtukynai \> Kūrimo įrankis**.</span><span class="sxs-lookup"><span data-stu-id="d9b30-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="d9b30-164">Sukurkite naują mygtuką.</span><span class="sxs-lookup"><span data-stu-id="d9b30-164">Create a new button.</span></span>
4. <span data-ttu-id="d9b30-165">Pasirinkite **mygtuko** ypatybes.</span><span class="sxs-lookup"><span data-stu-id="d9b30-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="d9b30-166">Kaip veiksmą pasirinkite **Atidaryti URL**.</span><span class="sxs-lookup"><span data-stu-id="d9b30-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="d9b30-167">Įveskite norimą naudoti URL.</span><span class="sxs-lookup"><span data-stu-id="d9b30-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="d9b30-168">Sukonfigūruokite, ar norite, kad URL būtų atidaromas naujame lange.</span><span class="sxs-lookup"><span data-stu-id="d9b30-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]