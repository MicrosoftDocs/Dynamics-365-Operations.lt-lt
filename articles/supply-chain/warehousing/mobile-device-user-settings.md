---
title: Mobiliojo įrenginio vartotojo parametrai
description: Šioje temoje paaiškinama, kaip valdyti sandėlio darbuotojų mobiliojo įrenginio vartotojo parametrus.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mafoge
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8090305c1b296d8a8a64df444abb1d1f2235aeee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501203"
---
# <a name="mobile-device-user-settings"></a><span data-ttu-id="b270d-103">Mobiliojo įrenginio vartotojo parametrai</span><span class="sxs-lookup"><span data-stu-id="b270d-103">Mobile device user settings</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="b270d-104">Naujoje Sandėlio valdymo mobiliųjų įrenginių programėlėje yra programai skirtų parametrų rinkinys, padedantis pritaikyti vartotojų patirtį.</span><span class="sxs-lookup"><span data-stu-id="b270d-104">The new Warehouse Management mobile app has a set of app-specific settings that help tailor the user experience.</span></span> <span data-ttu-id="b270d-105">Programą galima naudoti įvairių ekranų dydžių ir konfigūracijų (pvz., planšetinis kompiuteris, telefonas ar išmanusis laikrodis) įrenginiuose, todėl gali būti naudinga centralizuotai valdyti šiuos parametrus „Microsoft Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="b270d-105">Because the app can be used on devices of different screen sizes and configurations (such as tablet, phone, or arm-held), it can be useful to centrally manage these settings from Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="b270d-106">*Mobiliojo įrenginio vartotojo parametrų* funkcija leidžia nustatyti visuotinius vartotojo parametrus, kurie bus naudojami visuose įrenginiuose.</span><span class="sxs-lookup"><span data-stu-id="b270d-106">The *mobile device user settings* feature lets you define global user settings that will be used on all devices.</span></span> <span data-ttu-id="b270d-107">Taip pat galite nustatyti išsamesnius vartotojo parametrus, skirtus individualiems įrenginių prekių ženklams, įrenginių modeliams ir (arba) darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="b270d-107">You can also define more granular user settings for individual device brands, device models, and/or workers.</span></span> <span data-ttu-id="b270d-108">Kai darbuotojas prisijungia prie Sandėlio valdymo mobiliųjų įrenginių programėlės, programa išrenką ir pritaiko konkrečių parametrų profilį, kuris saugomas „Supply Chain Management” ir yra atitinkamo prekės ženklo, įrenginio ir (arba) vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="b270d-108">When a worker signs in to the Warehouse Management mobile app, the app fetches and applies the most specific settings profile that is stored in Supply Chain Management for the matching brand, device, and/or user ID.</span></span>

<span data-ttu-id="b270d-109">Ši funkcija gali padėti darbuotojams greitai pradėti dirbti, kai tik jie pradeda naudoti naują įrenginį.</span><span class="sxs-lookup"><span data-stu-id="b270d-109">This feature can help workers get started more quickly whenever they begin to use a new device.</span></span> <span data-ttu-id="b270d-110">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="b270d-110">Here are some examples:</span></span>

- <span data-ttu-id="b270d-111">Administratoriai gali nustatyti standartinį nuostatų rinkinį, kuris geriausiai veikia konkretaus gamintojo ir (arba) konkrečių įrenginių modelių įrenginiuose.</span><span class="sxs-lookup"><span data-stu-id="b270d-111">Admins can establish a standard set of preferences that work best for devices from a specific manufacturer and/or for specific device models.</span></span> <span data-ttu-id="b270d-112">Todėl darbuotojai gali pradėti naudoti naują įrenginį nekeisdami parametrų.</span><span class="sxs-lookup"><span data-stu-id="b270d-112">Therefore, workers can get started with a new device without necessarily having to change the settings.</span></span>
- <span data-ttu-id="b270d-113">Jei jūsų įmonėje yra identiškų įrenginių telkinys, kurį bendrai naudoja darbuotojai, darbuotojai matys norimą sąranką kiekvieną kartą prisijungdami, net jei jie niekada nenaudojo konkretaus fizinio įrenginio, kurį pasirinko nurodytą dieną.</span><span class="sxs-lookup"><span data-stu-id="b270d-113">If your company has a pool of identical devices that are shared among workers, workers will see their preferred setup every time that they sign in, even if they have never used the specific physical device that they selected on a given day.</span></span>
- <span data-ttu-id="b270d-114">„Supply Chain Management” administratoriai gali peržiūrėti ir redaguoti visus išsaugotus parametrus, net ir atskirų darbuotojų.</span><span class="sxs-lookup"><span data-stu-id="b270d-114">In Supply Chain Management, admins can view and edit all stored settings, even for individual workers.</span></span> <span data-ttu-id="b270d-115">Ši galimybė gali padėti jiems pašalinti triktis arba tiksliai suderinti naujas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b270d-115">This capability can help them troubleshoot or fine-tune new features.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b270d-116">*Mobiliojo įrenginio vartotojo parametrų* funkcija taikoma tik naujai Sandėlio valdymo mobiliųjų įrenginių programėlei.</span><span class="sxs-lookup"><span data-stu-id="b270d-116">The *mobile device user settings* feature applies only to the new Warehouse Management mobile app.</span></span> <span data-ttu-id="b270d-117">Jis neveikia senoje sandėlio programoje.</span><span class="sxs-lookup"><span data-stu-id="b270d-117">It doesn't work with the old warehouse app.</span></span>

## <a name="turn-on-the-mobile-device-user-settings-feature"></a><span data-ttu-id="b270d-118">Mobiliojo įrenginio vartotojo parametrų funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="b270d-118">Turn on the mobile device user settings feature</span></span>

<span data-ttu-id="b270d-119">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="b270d-119">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="b270d-120">Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją.</span><span class="sxs-lookup"><span data-stu-id="b270d-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="b270d-121">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="b270d-121">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b270d-122">**Modulis:** *Sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="b270d-122">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b270d-123">**Funkcijos pavadinimas:** *Naujos sandėlio programos vartotojo parametrai, piktogramos ir veiksmų pavadinimai*</span><span class="sxs-lookup"><span data-stu-id="b270d-123">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="create-and-manage-user-settings"></a><span data-ttu-id="b270d-124">Vartotojo parametrų kūrimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="b270d-124">Create and manage user settings</span></span>

<span data-ttu-id="b270d-125">Norėdami kurti, peržiūrėti ir valdyti parametrų profilius visuose detalumo lygiuose, naudokite puslapį **Mobiliojo įrenginio vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b270d-125">Use the **Mobile device user settings** page to create, view, and manage settings profiles at all levels of granularity.</span></span> <span data-ttu-id="b270d-126">Pirmą kartą, kai darbuotojas redaguoja vartotojo parametrus naujame įrenginyje, naujas profilis automatiškai įtraukiamas į šį puslapį, jei jo dar nėra.</span><span class="sxs-lookup"><span data-stu-id="b270d-126">The first time that a worker edits their user settings on a new device, a new profile is automatically added on this page, if it doesn't already exist.</span></span> <span data-ttu-id="b270d-127">Tada šis profilis atnaujinamas kiekvieną kartą, kai darbuotojas atlieka keitimą.</span><span class="sxs-lookup"><span data-stu-id="b270d-127">That profile is then updated every time that the worker makes a change.</span></span>

<span data-ttu-id="b270d-128">Taip pat galite nustatyti parametrų profilį, taikomą visiems įrenginių prekių ženklams, įrenginių modeliams ir (arba) darbuotojams.</span><span class="sxs-lookup"><span data-stu-id="b270d-128">You can also define a settings profile that applies to all device brands, device models, and/or workers.</span></span> <span data-ttu-id="b270d-129">Tada galite padidinti detalumą pritaikydami daugiau konkrečių prekių ženklų, modelių ir (arba) darbuotojų parametrų.</span><span class="sxs-lookup"><span data-stu-id="b270d-129">You can then increase the granularity by applying more specific settings for individual brands, models, and/or workers.</span></span>

<span data-ttu-id="b270d-130">Norėdami sukurti ir valdyti jūsų mobiliųjų įrenginių vartotojo nustatymus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b270d-130">Follow these steps to create and manage user settings for your mobile devices.</span></span>

1. <span data-ttu-id="b270d-131">Eikite į **Sandėlio valdymas \> Mobilusis įrenginys \> Mobiliojo įrenginio vartotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="b270d-131">Go to **Warehouse management \> Mobile device \> Mobile device user settings**.</span></span>
1. <span data-ttu-id="b270d-132">Sąrašo srityje pasirinkite esamą vartotojo parametrų profilį, kad atidarytumėte jo įrašą.</span><span class="sxs-lookup"><span data-stu-id="b270d-132">Select an existing user settings profile in the list pane to open its record.</span></span> <span data-ttu-id="b270d-133">Arba, norėdami sukurti naują profilį, veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b270d-133">Alternatively, select **New** on the Action Pane to create a new profile.</span></span>

    <span data-ttu-id="b270d-134">Kiekvienas sąrašo srities profilis yra pažymėtas, kad nurodytų prekės ženklą, modelį ir (arba) vartotojo ID, kuriems taikomas profilis.</span><span class="sxs-lookup"><span data-stu-id="b270d-134">Each profile in the list pane is labeled to indicate the brand, model, and/or user ID that the profile applies to.</span></span> <span data-ttu-id="b270d-135">Bendresnių profilių kai kurių arba visų šių charakteristikų reikšmė nustatyta į *Visi*.</span><span class="sxs-lookup"><span data-stu-id="b270d-135">More general profiles have a value of *All* for some or all of these characteristics.</span></span>

1. <span data-ttu-id="b270d-136">Naujo ar pasirinkto parametrų profilio įrašo antraštės skyriuje nustatykite toliau pateiktus laukus.</span><span class="sxs-lookup"><span data-stu-id="b270d-136">In the header section of the record for the new or selected settings profile, set the following fields:</span></span>

    - <span data-ttu-id="b270d-137">**Įrenginio prekės ženklo pavadinimas** – pasirinkite įrenginio prekės ženklo pavadinimą, kuriam turi būti taikomas profilis.</span><span class="sxs-lookup"><span data-stu-id="b270d-137">**Device brand name** – Select the device brand name that the profile should apply to.</span></span> <span data-ttu-id="b270d-138">Jei profilis turi būti taikomas visiems prekių ženklams, palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="b270d-138">If the profile should apply to all brands, leave this field blank.</span></span> <span data-ttu-id="b270d-139">Reikšmių sąrašas apima visus jūsų sistemoje nustatytus prekės ženklus.</span><span class="sxs-lookup"><span data-stu-id="b270d-139">The list of values includes all the brands that have been defined in your system.</span></span> <span data-ttu-id="b270d-140">Norėdami gauti informacijos apie tai, kaip apibrėžti prekių ženklų sąrašą, žr. kitą skyrių.</span><span class="sxs-lookup"><span data-stu-id="b270d-140">For information about how to define the list of brands, see the next section.</span></span>
    - <span data-ttu-id="b270d-141">**Įrenginio modelio ID** – pasirinkite įrenginio modelį, kuriam turi būti taikomas profilis.</span><span class="sxs-lookup"><span data-stu-id="b270d-141">**Device model ID** – Select the device model that the profile should apply to.</span></span> <span data-ttu-id="b270d-142">Jei profilis turi būti taikomas visiems pasirinkto prekės ženklo modeliams, palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="b270d-142">If the profile should apply to all models of the selected brand, leave this field blank.</span></span> <span data-ttu-id="b270d-143">Reikšmių sąraše pateikiami visi apibrėžti prekės ženklo, pasirinkto lauke **Įrenginio prekės ženklo pavadinimas**, modeliai.</span><span class="sxs-lookup"><span data-stu-id="b270d-143">The list of values includes all the models that have been defined for the brand that is selected in the **Device brand name** field.</span></span> <span data-ttu-id="b270d-144">Norėdami gauti informacijos apie tai, kaip apibrėžti kiekvieno prekės ženklo modelių sąrašą, žr. kitą skyrių.</span><span class="sxs-lookup"><span data-stu-id="b270d-144">For information about how to define the list of models for each brand, see the next section.</span></span>
    - <span data-ttu-id="b270d-145">**Vartotojo ID** – pasirinkite sandėlio darbuotojo, kuriam turėtų būti taikomas parametrų profilis, vartotojo ID.</span><span class="sxs-lookup"><span data-stu-id="b270d-145">**User ID** – Select the user ID of the warehouse worker that the setting profile should apply to.</span></span> <span data-ttu-id="b270d-146">Jei profilis turi būti taikomas visiems darbuotojams, palikite šį lauką tuščią.</span><span class="sxs-lookup"><span data-stu-id="b270d-146">If the profile should apply to all workers, leave this field blank.</span></span>

1. <span data-ttu-id="b270d-147">„FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.</span><span class="sxs-lookup"><span data-stu-id="b270d-147">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="b270d-148">**Mygtukų padėtis** – pasirinkite, kaip mygtukus reikia išdėstyti įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="b270d-148">**Button position** – Select how buttons should be positioned on the device.</span></span> <span data-ttu-id="b270d-149">Programos elementai bus perkelti, kad geriau atitiktų darbuotojo nuostatas arba naudojimą.</span><span class="sxs-lookup"><span data-stu-id="b270d-149">Elements in the app will be moved to better fit the preference or handedness of the worker.</span></span> <span data-ttu-id="b270d-150">Galimos parinktys yra *Apačioje dešinėje (numatytoji)*, *Apačioje kairėje*, *Viršuje dešinėje* ir *Viršuje kairėje*.</span><span class="sxs-lookup"><span data-stu-id="b270d-150">The available options are *Bottom right (default)*, *Bottom left*, *Top right*, and *Top left*.</span></span>
    - <span data-ttu-id="b270d-151">**Ekrano padėtis** – pasirinkite ekrano padėtį, kuri programoje turi būti taikoma pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="b270d-151">**Display orientation** – Select the display orientation that should be applied by default in the app.</span></span>
    - <span data-ttu-id="b270d-152">**Nuskaityti naudojant kamerą** – nustatykite šią parinktį į *Taip*, kad įvesties laukams nuskaityti būtų naudojama įrenginio kamera, kai pageidaujamas įvesties režimas nustatytas į *Nuskaitymas*.</span><span class="sxs-lookup"><span data-stu-id="b270d-152">**Scan with camera** – Set this option to *Yes* to use the device camera to scan input fields where the preferred input mode is set to *Scanning*.</span></span> <span data-ttu-id="b270d-153">Jei jūsų įrenginyje yra įdiegtas skaitytuvas, nustatykite šią parinktį į *Ne*, kad naudotumėte skaitytuvą.</span><span class="sxs-lookup"><span data-stu-id="b270d-153">If your device has a built-in scanner, set this option to *No* to use the scanner instead.</span></span>
    - <span data-ttu-id="b270d-154">**Rodyti produkto nuotrauką** – pasirinkite, ar turi būti rodomos išleisto produkto nuotraukos, jei jų yra.</span><span class="sxs-lookup"><span data-stu-id="b270d-154">**Show product photo** – Select whether product photos should be shown if they are available for the released product.</span></span> <span data-ttu-id="b270d-155">Daugiau informacijos apie tai, kaip pridėti produkto vaizdus, žr. [Vaizdo pridėjimas prie produkto](../pim/tasks/add-image-product.md).</span><span class="sxs-lookup"><span data-stu-id="b270d-155">For more information about how to add product images, see [Add an image to a product](../pim/tasks/add-image-product.md).</span></span>
    - <span data-ttu-id="b270d-156">**Rodyti spalvų temą** – pasirinkite įrenginio spalvų temą.</span><span class="sxs-lookup"><span data-stu-id="b270d-156">**Display color theme** – Select a color theme for the device.</span></span>
    - <span data-ttu-id="b270d-157">**Garsumo lygis** – pasirinkite įrenginio garsumo lygį.</span><span class="sxs-lookup"><span data-stu-id="b270d-157">**Sound level** – Select the sound level for the device.</span></span> <span data-ttu-id="b270d-158">Pasirinkite vertę nuo 0 (nulio) iki 10.</span><span class="sxs-lookup"><span data-stu-id="b270d-158">Select a value between 0 (zero) and 10.</span></span> <span data-ttu-id="b270d-159">Vertė *0* reiškia, kad nėra jokio garsumo, o vertė *10* reiškia didžiausią garsumą.</span><span class="sxs-lookup"><span data-stu-id="b270d-159">A value of *0* represents no sound, and a value of *10* represents maximum volume.</span></span> <span data-ttu-id="b270d-160">Numatytoji vertė yra *4*.</span><span class="sxs-lookup"><span data-stu-id="b270d-160">The default value is *4*.</span></span>
    - <span data-ttu-id="b270d-161">**Vibracijos lygis** – pasirinkite įrenginio vibracijos lygį.</span><span class="sxs-lookup"><span data-stu-id="b270d-161">**Vibration level** – Select the vibration level for the device.</span></span> <span data-ttu-id="b270d-162">Pasirinkite vertę nuo 0 (nulio) iki 5.</span><span class="sxs-lookup"><span data-stu-id="b270d-162">Select a value between 0 (zero) and 5.</span></span> <span data-ttu-id="b270d-163">Vertė *0* reiškia, kad nėra jokios vibracijos, o vertė *5* reiškia didžiausią vibraciją.</span><span class="sxs-lookup"><span data-stu-id="b270d-163">A value of *0* represents no vibration, and a value of *5* represents maximum vibration.</span></span> <span data-ttu-id="b270d-164">Numatytoji vertė yra *1*.</span><span class="sxs-lookup"><span data-stu-id="b270d-164">The default value is *1*.</span></span>
    - <span data-ttu-id="b270d-165">**Teksto dydis procentais** – nurodykite teksto dydį standartinio dydžio procentais.</span><span class="sxs-lookup"><span data-stu-id="b270d-165">**Text scale percentage** – Specify the text size as a percentage of the standard size.</span></span> <span data-ttu-id="b270d-166">Įveskite vertę nuo 70 iki 400.</span><span class="sxs-lookup"><span data-stu-id="b270d-166">Enter a value between 70 and 400.</span></span> <span data-ttu-id="b270d-167">Vertė *70* reiškia mažiausią teksto dydį, o vertė *400* reiškia didžiausią teksto dydį.</span><span class="sxs-lookup"><span data-stu-id="b270d-167">A value of *70* represents the smallest text scale, and a value of *400* represents the largest text scale.</span></span> <span data-ttu-id="b270d-168">Numatytoji vertė yra *100*.</span><span class="sxs-lookup"><span data-stu-id="b270d-168">The default value is *100*.</span></span>
    - <span data-ttu-id="b270d-169">**Mygtukų dydis procentais** – nurodykite mygtukų dydį standartinio dydžio procentais.</span><span class="sxs-lookup"><span data-stu-id="b270d-169">**Button scale percentage** – Specify the button size as a percentage of the standard size.</span></span> <span data-ttu-id="b270d-170">Įveskite vertę nuo 50 iki 200.</span><span class="sxs-lookup"><span data-stu-id="b270d-170">Enter a value between 50 and 200.</span></span> <span data-ttu-id="b270d-171">Vertė *50* reiškia mažiausią mygtukų dydį, o vertė *200* reiškia didžiausią mygtukų dydį.</span><span class="sxs-lookup"><span data-stu-id="b270d-171">A value of *50* represents the smallest button scale, and a value of *200* represents the largest button scale.</span></span> <span data-ttu-id="b270d-172">Numatytoji vertė yra *100*.</span><span class="sxs-lookup"><span data-stu-id="b270d-172">The default value is *100*.</span></span>

## <a name="create-and-manage-mobile-device-brands"></a><span data-ttu-id="b270d-173">Mobiliojo įrenginio prekių ženklų kūrimas ir valdymas</span><span class="sxs-lookup"><span data-stu-id="b270d-173">Create and manage mobile device brands</span></span>

<span data-ttu-id="b270d-174">Norėdami peržiūrėti, kurti ir valdyti įrenginio prekių ženklus ir modelius, kuriuos galima naudoti su jūsų parametrų profiliais, naudokite puslapį **Mobiliojo įrenginio prekių ženklai**.</span><span class="sxs-lookup"><span data-stu-id="b270d-174">Use the **Mobile device brands** page to view, create, and manage the device brands and models that can be used with your settings profiles.</span></span> <span data-ttu-id="b270d-175">Mobiliųjų įrenginių programėlė automatiškai nuskaito ir pateikia vietinio prekės ženklo pavadinimą ir modelio ID pirmą kartą, kai darbuotojas redaguoja parametrus konkrečiame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="b270d-175">The mobile app automatically fetches and submits the local brand name and model ID the first time that a worker edits their settings on a given device.</span></span> <span data-ttu-id="b270d-176">Todėl dauguma šių įrašų paprastai bus sugeneruoti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="b270d-176">Therefore, most of these records will usually be automatically generated.</span></span> <span data-ttu-id="b270d-177">Tačiau taip pat galite valdyti visus įrašus šiame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="b270d-177">However, you can also manage all the records on this page.</span></span> <span data-ttu-id="b270d-178">Pavyzdžiui, galite suteikti naudingesnius kiekvieno prekės ženklo ir modelio aprašymus, kad būtų lengviau atskirti panašius ar užšifruotus modelių ID.</span><span class="sxs-lookup"><span data-stu-id="b270d-178">For example, you can give more useful descriptions to each brand and model to help distinguish similar or cryptic model IDs.</span></span>

<span data-ttu-id="b270d-179">Norėdami kurti ir valdyti jūsų mobiliųjų įrenginių prekių ženklus ir modelius, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b270d-179">Follow these steps to create and manage your mobile device brands and models.</span></span>

1. <span data-ttu-id="b270d-180">Eikite į **Sandėlio valdymas \> Mobilusis įrenginys \> Mobiliojo įrenginio prekių ženklai**.</span><span class="sxs-lookup"><span data-stu-id="b270d-180">Go to **Warehouse management \> Mobile device \> Mobile device brands**.</span></span>
1. <span data-ttu-id="b270d-181">Sąrašo srityje pasirinkite mobiliojo įrenginio prekės ženklą, kad atidarytumėte jo įrašą.</span><span class="sxs-lookup"><span data-stu-id="b270d-181">In the list pane, select a mobile device brand to open its record.</span></span> <span data-ttu-id="b270d-182">Arba, norėdami sukurti naują prekės ženklą, veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b270d-182">Alternatively, select **New** on the Action Pane to create a new brand.</span></span>
1. <span data-ttu-id="b270d-183">Naujo ar pasirinkto įrenginio prekės ženklo įrašo antraštės skyriuje nustatykite toliau pateiktus laukus.</span><span class="sxs-lookup"><span data-stu-id="b270d-183">In the header section of the record for the new or selected device brand, set the following fields:</span></span>

    - <span data-ttu-id="b270d-184">**Įrenginio prekės ženklo pavadinimas** – įrenginio prekės ženklo pavadinimas, pvz., *„Microsoft Corporation”*.</span><span class="sxs-lookup"><span data-stu-id="b270d-184">**Device brand name** – The brand name of the device, such as *Microsoft Corporation*.</span></span>
    - <span data-ttu-id="b270d-185">**Aprašas** – aprašą galima įvesti norint padėti atskirti prekių ženklų pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="b270d-185">**Description** – You can enter a description to help distinguish brand names.</span></span>

1. <span data-ttu-id="b270d-186">„FastTab” **Mobiliojo įrenginio modeliai** rodomi visi pasirinkto įrenginio prekės ženklo modeliai.</span><span class="sxs-lookup"><span data-stu-id="b270d-186">The **Mobile device models** FastTab shows all the models for the selected device brand.</span></span> <span data-ttu-id="b270d-187">Naudokite mygtukus įrankių juostoje, norėdami įtraukti eilučių į tinklelį arba pašalinti jas.</span><span class="sxs-lookup"><span data-stu-id="b270d-187">Use the buttons on the toolbar to add rows to the grid or remove rows.</span></span> <span data-ttu-id="b270d-188">Kiekvienai eilutei nustatykite toliau pateiktus laukus.</span><span class="sxs-lookup"><span data-stu-id="b270d-188">For each row, you can set the following fields:</span></span>

    - <span data-ttu-id="b270d-189">**Įrenginio modelio ID** – įrenginio modelio ID, pvz., *„Surface Book 2”*.</span><span class="sxs-lookup"><span data-stu-id="b270d-189">**Device model ID** – The device model ID, such as *Surface Book 2*.</span></span>
    - <span data-ttu-id="b270d-190">**Aprašas** – aprašą galima įvesti norint padėti atskirti modelių ID.</span><span class="sxs-lookup"><span data-stu-id="b270d-190">**Description** – You can enter a description to help distinguish model IDs.</span></span>