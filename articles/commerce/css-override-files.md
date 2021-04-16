---
title: Darbas su CSS perrašymo failais
description: Šioje temoje aprašoma, kodėl, kada ir kaip programoje „Microsoft Dynamics 365 Commerce“ naudoti pakopinių stilių sąrašo (CSS) perrašymo failus.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ef96070fe77b46622667301c7c7c402909ee7dfc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799498"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="6c884-103">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="6c884-103">Work with CSS override files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c884-104">Šioje temoje aprašoma, kodėl, kada ir kaip programoje „Microsoft Dynamics 365 Commerce“ naudoti pakopinių stilių sąrašo (CSS) perrašymo failus.</span><span class="sxs-lookup"><span data-stu-id="6c884-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6c884-105">Nuolatiniai svetainės stiliai paprastai turėtų būti tvarkomi naudojant svetainės temą.</span><span class="sxs-lookup"><span data-stu-id="6c884-105">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="6c884-106">Naudojant temas pasiekiami pagrindiniai bet kurio svetainės puslapio CSS ir stilių parametrai.</span><span class="sxs-lookup"><span data-stu-id="6c884-106">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="6c884-107">Temos kuriamos naudojant „Dynamics 365 Commerce“ internetinį programinės įrangos kūrimo rinkinį (SDK), o į svetaines įdiegiamos naudojant „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="6c884-107">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6c884-108">Naudodami temų derinimo galimybes ir modulių sąsajos konfigūracijas SDK žinyno svetainėje, svetainių programuotojai gali lengviau kurti tinkinamus ir darnius svetainių dizaino paketus.</span><span class="sxs-lookup"><span data-stu-id="6c884-108">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="6c884-109">Kai šie dizaino paketai įdiegiami į svetainę, jos autoriai gali sutelkti dėmesį į turinio kūrimą, redagavimą ir publikavimą, o ne į svetainės programavimą.</span><span class="sxs-lookup"><span data-stu-id="6c884-109">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="6c884-110">Atsižvelgiant į įprastą temos ciklą, priklausomybė nuo programuotojų, keičiančių stilius per SDK ir LCS diegimo srautą, kai kuriose situacijose gali būti pernelyg didelė.</span><span class="sxs-lookup"><span data-stu-id="6c884-110">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="6c884-111">Jei SDK nesukonfigūruotas arba jei neturite laiko laukti įdiegties per LCS, svetainės prototipai ar karštosios pataisos gali atrodyti sudėtingi.</span><span class="sxs-lookup"><span data-stu-id="6c884-111">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="6c884-112">Tokiose situacijose gali padėti CSS perrašymo failai.</span><span class="sxs-lookup"><span data-stu-id="6c884-112">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="6c884-113">Naudodami „Commerce“ kūrimo įrankius, autentifikuoti vartotojai gali nusiųsti CSS failą, jį peržiūrėti ir aktyvinti, kad perrašytų svetainės temą.</span><span class="sxs-lookup"><span data-stu-id="6c884-113">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="6c884-114">Nereikalinga papildoma SDK ar LCS įdiegtis.</span><span class="sxs-lookup"><span data-stu-id="6c884-114">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="6c884-115">CSS perrašymo faile gali būti nurodytas toks mažas perrašymas, kaip vieno teksto stiliaus pakeitimas, arba toks platus, kaip visiškas prekės ženklo perkūrimas.</span><span class="sxs-lookup"><span data-stu-id="6c884-115">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="6c884-116">Prieš naudodami CSS perrašymo failus, turėkite omenyje tolesnius apribojimus.</span><span class="sxs-lookup"><span data-stu-id="6c884-116">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="6c884-117">Vienu metu svetainėje gali būti aktyvus tik vienas CSS perrašymo failas.</span><span class="sxs-lookup"><span data-stu-id="6c884-117">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="6c884-118">Todėl visi aktyvūs perrašymo veiksmai turi būti viename perrašymo faile.</span><span class="sxs-lookup"><span data-stu-id="6c884-118">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="6c884-119">Nors perrašymo veiksmus galite peržiūrėti „Commerce“ kūrimo įrankiuose, juose nėra specialių derinimo funkcijų, padedančių nustatyti perrašymo veiksmų sukeliamas klaidas.</span><span class="sxs-lookup"><span data-stu-id="6c884-119">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="6c884-120">Kitaip tariant, kai naudojate CSS perrašymo failus, neturite tokio paties įrankių rinkinio, kurį SDK suteikia moduliams ir kūrimui tikrinti.</span><span class="sxs-lookup"><span data-stu-id="6c884-120">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="6c884-121">Nepaisant to, CSS perrašymo failai yra greitas būdas dizaino prototipui sukurti ar karštajai pataisai įdiegti prieš sukuriant ir įdiegiant visapusį temos naujinimą.</span><span class="sxs-lookup"><span data-stu-id="6c884-121">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="6c884-122">CSS perrašymo failo sukūrimas</span><span class="sxs-lookup"><span data-stu-id="6c884-122">Create a CSS override file</span></span>

<span data-ttu-id="6c884-123">Norėdami sukurti CSS perrašymo failą, galite naudoti integruotąją programavimo aplinką (IDE), teksto rengyklę arba šaltinio kodo rengyklę.</span><span class="sxs-lookup"><span data-stu-id="6c884-123">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="6c884-124">Įprasta naršyklėje naudojant standartines žiniatinklio derintuves nustatyti esamos svetainės stilių išrinkiklius, ypatybes ir reikšmes.</span><span class="sxs-lookup"><span data-stu-id="6c884-124">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="6c884-125">Daugelyje naršyklių galima keisti reikšmes ir jas peržiūrėti derintuvėje.</span><span class="sxs-lookup"><span data-stu-id="6c884-125">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="6c884-126">Identifikavę norimus atlikti keitimus, galite juos įrašyti į savo CSS failą.</span><span class="sxs-lookup"><span data-stu-id="6c884-126">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="6c884-127">CSS perrašymo failo nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="6c884-127">Upload a CSS override file</span></span>

<span data-ttu-id="6c884-128">Norėdami programoje „Commerce“ į svetainę nusiųsti CSS failą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6c884-128">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6c884-129">Naudodami kūrimo įrankius, nueikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="6c884-129">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="6c884-130">Kairėje esančioje naršymo srityje pasirinkite **Dizainas**.</span><span class="sxs-lookup"><span data-stu-id="6c884-130">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c884-131">Kad galėtumėte pasirinkti **Dizainas**, naršymo srityje gali reikėti išplėsti elementą **Parametrai** – tai priklauso nuo naudojamos „Commerce“ kūrimo įrankių versijos.</span><span class="sxs-lookup"><span data-stu-id="6c884-131">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="6c884-132">Jei jis dar nepasirinktas, pagrindinės dizaino srities viršuje pasirinkite skirtuką **CSS perrašymas**.</span><span class="sxs-lookup"><span data-stu-id="6c884-132">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="6c884-133">Dalyje **Galimi CSS perrašymo veiksmai** pasirinkite **Nusiųsti CSS failą**.</span><span class="sxs-lookup"><span data-stu-id="6c884-133">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="6c884-134">Atsiranda failų naršyklės langas.</span><span class="sxs-lookup"><span data-stu-id="6c884-134">A File Explorer window appears.</span></span>
1. <span data-ttu-id="6c884-135">Naršydami failų naršyklėje pasirinkite CSS failą, tada – **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="6c884-135">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="6c884-136">Nusiųstas CSS failas dabar rodomas dalyje **Galimi CSS perrašymo veiksmai**.</span><span class="sxs-lookup"><span data-stu-id="6c884-136">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="6c884-137">CSS perrašymo failo peržiūra</span><span class="sxs-lookup"><span data-stu-id="6c884-137">Preview a CSS override file</span></span>

<span data-ttu-id="6c884-138">Jei CSS perrašymo failą norite peržiūrėti prieš jį suaktyvindami savo paleistoje svetainėje, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6c884-138">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="6c884-139">Kairėje esančioje naršymo srityje pasirinkite **Dizainas**, tada skirtuko **CSS perrašymas** dalyje **Galimi CSS perrašymo veiksmai** suraskite CSS failą, kurį norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="6c884-139">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="6c884-140">Prie CSS failo pavadinimo pasirinkite **Peržiūrėti svetainę**.</span><span class="sxs-lookup"><span data-stu-id="6c884-140">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="6c884-141">Dialogo lange **Pasirinkite URL** pasirinkite svetainės, kuriai norite taikyti perrašymo veiksmą, URL, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6c884-141">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="6c884-142">Jei yra keli pasirinkto URL variantai, pasirodžiusiame dialogo lange **Peržiūros variantai** pasirinkite norimą variantą.</span><span class="sxs-lookup"><span data-stu-id="6c884-142">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="6c884-143">Atidaromas naujas naršyklės skirtukas arba langas, kuriame galite patikrinti svetainės stilių perrašymo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6c884-143">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="6c884-144">URL tada galite bendrinti su kitais autentifikuotais „Commerce“ vartotojais, kad jie galėtų svetainę įvertinti ir pateikti atsiliepimų.</span><span class="sxs-lookup"><span data-stu-id="6c884-144">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="6c884-145">CSS perrašymo failo suaktyvinimas paleistoje svetainėje</span><span class="sxs-lookup"><span data-stu-id="6c884-145">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="6c884-146">Peržiūrėję ir patvirtinę CSS perrašymo failą, jį galite suaktyvinti paleistoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="6c884-146">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="6c884-147">Vienu metu svetainėje gali būti aktyvus tik vienas CSS perrašymo failas.</span><span class="sxs-lookup"><span data-stu-id="6c884-147">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="6c884-148">Jei suaktyvinate naują perrašymo failą, ankstesnis perrašymo failas supasyvinamas.</span><span class="sxs-lookup"><span data-stu-id="6c884-148">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="6c884-149">Todėl įsitikinkite, kad visi reikiami perrašymo veiksmai yra viename CSS perrašymo faile.</span><span class="sxs-lookup"><span data-stu-id="6c884-149">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="6c884-150">Norėdami suaktyvinti CSS perrašymo failą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6c884-150">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="6c884-151">Kairėje esančioje naršymo srityje pasirinkite **Dizainas**, tada skirtuko **CSS perrašymas** dalyje **Galimi CSS perrašymo veiksmai** suraskite CSS failą, kurį norite suaktyvinti.</span><span class="sxs-lookup"><span data-stu-id="6c884-151">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="6c884-152">Po CSS failo pavadinimu pasirinkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="6c884-152">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="6c884-153">Perrašymo failas iš karto tampa aktyvus jūsų paleistoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="6c884-153">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="6c884-154">CSS perrašymo failo išjungimas paleistoje svetainėje</span><span class="sxs-lookup"><span data-stu-id="6c884-154">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="6c884-155">Norėdami savo svetainėje CSS perrašymo failą išjungti, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6c884-155">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="6c884-156">Kairėje esančioje naršymo srityje pasirinkite **Dizainas**, tada skirtuko **CSS perrašymas** dalyje **Galimi CSS perrašymo veiksmai** suraskite CSS failą, kurį norite išjungti.</span><span class="sxs-lookup"><span data-stu-id="6c884-156">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="6c884-157">Po CSS failo pavadinimu pasirinkite **Išjungti**.</span><span class="sxs-lookup"><span data-stu-id="6c884-157">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="6c884-158">Perrašymo failas iš karto tampa neaktyvus jūsų paleistoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="6c884-158">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="6c884-159">Norėdami pasiekti papildomas CSS perrašymo failų parinktis, pasirinkite prie CSS failo pavadinimo esantį daugtaškį (**...**).</span><span class="sxs-lookup"><span data-stu-id="6c884-159">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="6c884-160">Parinktys **Atsisiųsti**, **Pervardyti** ir **Pakeisti** yra naudingos norint greitai pakeisti esamą CSS perrašymo failą.</span><span class="sxs-lookup"><span data-stu-id="6c884-160">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c884-161">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6c884-161">Additional resources</span></span>

[<span data-ttu-id="6c884-162">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="6c884-162">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="6c884-163">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="6c884-163">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="6c884-164">Darbas su stilių išankstinėmis parinktimis</span><span class="sxs-lookup"><span data-stu-id="6c884-164">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="6c884-165">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="6c884-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="6c884-166">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="6c884-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="6c884-167">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="6c884-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="6c884-168">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="6c884-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="6c884-169">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="6c884-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
