---
title: Kas nauja ar pasikeitė „Warehouse Management Mobile App” programėlėje
description: Šioje temoje pateikiamos naujos ir pakeistos kiekvienos išleistos „Warehouse Management Mobile App”, skirtos „Microsoft Dynamics 365 Supply Chain Management”, versijos funkcijos.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261790"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="185ec-103">Kas nauja ar pasikeitė „Warehouse Management Mobile App” programėlėje</span><span class="sxs-lookup"><span data-stu-id="185ec-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="185ec-104">Šioje temoje pateikiamos naujos kiekvienos išleistos „Warehouse Management Mobile App”, skirtos „Microsoft Dynamics 365 Supply Chain Management”, versijos funkcijos, klaidų taisymai ir žinomos problemos.</span><span class="sxs-lookup"><span data-stu-id="185ec-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="185ec-105">2.0.6.0 versija</span><span class="sxs-lookup"><span data-stu-id="185ec-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="185ec-106">2.0.6.0 versijos naujos funkcijos, klaidų taisymai ir patobulinimai</span><span class="sxs-lookup"><span data-stu-id="185ec-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="185ec-107">Šioje versijoje pristatomos toliau pateiktos naujos funkcijos, klaidų taisymai ir patobulinimai:</span><span class="sxs-lookup"><span data-stu-id="185ec-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="185ec-108">Demonstracinis režimas dabar rodo visas žymas įrenginio kalba.</span><span class="sxs-lookup"><span data-stu-id="185ec-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="185ec-109">Mažiau tikėtina, kad gausite šį klaidos pranešimą: „Nepavyksta rasti tinkamo nurodyto dydžio rodinio.”</span><span class="sxs-lookup"><span data-stu-id="185ec-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="185ec-110">Padidintas minimalus darbo kortelių aukštis (atvejais, kai konfigūruojami trys ar mažiau laukų, kad jie būtų rodomi darbų sąraše).</span><span class="sxs-lookup"><span data-stu-id="185ec-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="185ec-111">Patobulintos paraštės (palaipsniui išnykstančios) informacijos kortelių apačioje.</span><span class="sxs-lookup"><span data-stu-id="185ec-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="185ec-112">Netinkami XML failų simboliai, kurie keičiasi serveryje, dabar yra apdorojami sėkmingai.</span><span class="sxs-lookup"><span data-stu-id="185ec-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="185ec-113">(Pavyzdžiui, nespausdinamieji simboliai dabar tvarkomi labai sėkmingai ir nesukelia programos nereagavimo.)</span><span class="sxs-lookup"><span data-stu-id="185ec-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="185ec-114">HTTP klaidos (pavyzdžiui, „klaida 503”), kai serverio užklausa pateikta, dabar tvarkomos labai sėkmingai.</span><span class="sxs-lookup"><span data-stu-id="185ec-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="185ec-115">Kai rodoma klaida, automatiškai neberodomas pasirinktinio įvedimo lauko valdiklių parinkčių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="185ec-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="185ec-116">Programa daugiau nenustoja reaguoti dėl vartotojo parametruose pasirinktos ekrano padėties.</span><span class="sxs-lookup"><span data-stu-id="185ec-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="185ec-117">Dabar produktų vaizdai yra rodomi savitarnos aplinkose.</span><span class="sxs-lookup"><span data-stu-id="185ec-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="185ec-118">Šis pakeitimas taikomas tik mažos skiriamosios gebos versijoms.</span><span class="sxs-lookup"><span data-stu-id="185ec-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="185ec-119">(Failų valdymo tarnyba nepalaiko viso dydžio vaizdų savitarnos aplinkose.)</span><span class="sxs-lookup"><span data-stu-id="185ec-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="185ec-120">Buvo išspręsta problema, susijusi su nulinio kiekio trumpais paėmimais.</span><span class="sxs-lookup"><span data-stu-id="185ec-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="185ec-121">Programa daugiau nenustoja reaguoti, kai informacijos kortelėje rodomi keli identiški laukai.</span><span class="sxs-lookup"><span data-stu-id="185ec-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="185ec-122">Žinomos problemos 2.0.6.0 versijoje</span><span class="sxs-lookup"><span data-stu-id="185ec-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="185ec-123">Šioje versijoje yra tokios žinomos problemos:</span><span class="sxs-lookup"><span data-stu-id="185ec-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="185ec-124">Programa (ypač darbų sąrašas) laikui bėgant tampa lėtesni.</span><span class="sxs-lookup"><span data-stu-id="185ec-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="185ec-125">**„Windows” versija:** Kai USB ginklas naudojamas nuskaitymui „Windows”, nenuoseklūs rezultatai sukelia nuskaitytų simbolių sumaišymą.</span><span class="sxs-lookup"><span data-stu-id="185ec-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="185ec-126">2.0.5.0 versija</span><span class="sxs-lookup"><span data-stu-id="185ec-126">Version 2.0.5.0</span></span>

<span data-ttu-id="185ec-127">Šioje versijoje pristatomos toliau pateiktos naujos funkcijos, klaidų taisymai ir patobulinimai:</span><span class="sxs-lookup"><span data-stu-id="185ec-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="185ec-128">Ryšio parametrų nustatyme nebeslepiamas kliento slaptasis raktas.</span><span class="sxs-lookup"><span data-stu-id="185ec-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="185ec-129">Dabar galite ilgai paspausti ant bet kokio teksto, kad jį pilnai pamatytumėte.</span><span class="sxs-lookup"><span data-stu-id="185ec-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="185ec-130">Patobulintas klaidos pranešimas, kai trūksta saugojimo teisių.</span><span class="sxs-lookup"><span data-stu-id="185ec-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="185ec-131">Kai kuriems srautams buvo įtrauktos naujos valdiklių sekos.</span><span class="sxs-lookup"><span data-stu-id="185ec-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="185ec-132">Pateikimo mygtukas daugiau neteisingai netampa tinkamas dėl lango dydžio.</span><span class="sxs-lookup"><span data-stu-id="185ec-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="185ec-133">Kai naudojami didesni mygtukų dydžiai, slankikliai gali toliau veikti mažesniuose ekranuose.</span><span class="sxs-lookup"><span data-stu-id="185ec-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="185ec-134">Keturių mygtukų perdanga nebėra nutraukiama.</span><span class="sxs-lookup"><span data-stu-id="185ec-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="185ec-135">Dabar klaviatūra palaiko naikinimo mygtuką.</span><span class="sxs-lookup"><span data-stu-id="185ec-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="185ec-136">Ryškumo problema, kuri galėjo įvykti paspaudus klaviatūrą, buvo išspręsta.</span><span class="sxs-lookup"><span data-stu-id="185ec-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="185ec-137">Buvo išspręstos įvairios demonstracinių duomenų problemos.</span><span class="sxs-lookup"><span data-stu-id="185ec-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="185ec-138">Problema, kuri veikdavo informacijos puslapio skaitinius laukus, buvo ištaisyta.</span><span class="sxs-lookup"><span data-stu-id="185ec-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="185ec-139">Ekrano klaviatūra daugiau nebepradingsta kai kuriuose įrenginiuose.</span><span class="sxs-lookup"><span data-stu-id="185ec-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="185ec-140">Įvairios vartotojo sąsajos (UI) klaidos buvo ištaisytos, pavyzdžiui, klaidos, veikusios fono spalvą ir padėtį.</span><span class="sxs-lookup"><span data-stu-id="185ec-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="185ec-141">Patobulinta rusų kalbos vartotojo sąsaja.</span><span class="sxs-lookup"><span data-stu-id="185ec-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="185ec-142">Buvo išspręstos įvairios problemos, dėl kurių sistema nebereaguodavo.</span><span class="sxs-lookup"><span data-stu-id="185ec-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="185ec-143">Buvo išspręsta problema, susijusi su skaičiuotuvo atidarymu iš naujo.</span><span class="sxs-lookup"><span data-stu-id="185ec-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="185ec-144">**„Android” versija:** Problema, dėl kurios „4.4 Android” nustojo reaguoti į paleistį, buvo ištaisyta.</span><span class="sxs-lookup"><span data-stu-id="185ec-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="185ec-145">**„Android” versija:** Minimalus mastelio keitimas sumažintas iki 50 procentų.</span><span class="sxs-lookup"><span data-stu-id="185ec-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="185ec-146">2.0.4.0 versija</span><span class="sxs-lookup"><span data-stu-id="185ec-146">Version 2.0.4.0</span></span>

<span data-ttu-id="185ec-147">2.0.4.0 versija buvo pirmasis bendrai pasiekiamas „Warehouse Management Mobile App” programėlės leidimas.</span><span class="sxs-lookup"><span data-stu-id="185ec-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="185ec-148">2.0.4.0 versijos naujos funkcijos, klaidų taisymai ir patobulinimai</span><span class="sxs-lookup"><span data-stu-id="185ec-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="185ec-149">Šioje versijoje pristatomos naujos funkcijos, klaidų taisymai ir patobulinimai, kurių nebuvo peržiūros versijoje:</span><span class="sxs-lookup"><span data-stu-id="185ec-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="185ec-150">Jei išsamios informacijos kortelėje yra dvi žymos, kurių duomenys vienodi, viena iš žymų yra paslėpta.</span><span class="sxs-lookup"><span data-stu-id="185ec-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="185ec-151">Specialieji simboliai dabar rodomi pagal numatytuosius nustatymus,o jų paslėpimo parinktis buvo pašalinta iš vartotojo parametrų.</span><span class="sxs-lookup"><span data-stu-id="185ec-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="185ec-152">Išjungti pateikimo mygtukai dabar rodomi kaip negalimi kompaktiniame rankiniame rodinyje.</span><span class="sxs-lookup"><span data-stu-id="185ec-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="185ec-153">Keitimas į sekos logiką valdikliams užtikrina sklandesnį mastelio keitimą įrenginiams.</span><span class="sxs-lookup"><span data-stu-id="185ec-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="185ec-154">Todėl yra mažesnis poreikis koreguoti šriftų arba mygtukų dydį.</span><span class="sxs-lookup"><span data-stu-id="185ec-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="185ec-155">Numatytoji spalvos tema buvo pakeista į *Tamsią*.</span><span class="sxs-lookup"><span data-stu-id="185ec-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="185ec-156">Trūkstama išjungto pateikimo mygtuko piktograma įtraukta į juostos rodinį.</span><span class="sxs-lookup"><span data-stu-id="185ec-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="185ec-157">Pasibaigusio skirtojo laiko išimtys dabar perkels jus į ryšio puslapį, o ne rodys eilutės klaidą.</span><span class="sxs-lookup"><span data-stu-id="185ec-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="185ec-158">Jei negalimas joks pateikimo veiksmas (pavyzdžiui, **GERAI**, **Taip**, **Priimti**, **Įvykdyta** arba **Baigta**), pateikimo mygtukas bus išjungtas.</span><span class="sxs-lookup"><span data-stu-id="185ec-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="185ec-159">Patobulintas programos stabilumas.</span><span class="sxs-lookup"><span data-stu-id="185ec-159">App stability has been improved.</span></span>
- <span data-ttu-id="185ec-160">Yra sprendimas saugumo pažeidžiamumui [„CVE-2021-26701”](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="185ec-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="185ec-161">**„Windows” versija:** „Windows” problema, kai meniu nereaguoja pakeitus lango dydį, buvo išspręsta.</span><span class="sxs-lookup"><span data-stu-id="185ec-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="185ec-162">Žinoma problema 2.0.4.0 versijoje</span><span class="sxs-lookup"><span data-stu-id="185ec-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="185ec-163">Šioje versijoje yra tokia žinoma problema:</span><span class="sxs-lookup"><span data-stu-id="185ec-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="185ec-164">Šioje versijoje yra problema su įrenginiais, kurie naudoja „Android 4.4”.</span><span class="sxs-lookup"><span data-stu-id="185ec-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="185ec-165">Naudojant programą su šia „Android” versija, gali kilti problemų.</span><span class="sxs-lookup"><span data-stu-id="185ec-165">You might experience issues when you use the app on this Android version.</span></span>
