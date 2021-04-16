---
title: „Regulatory Configuration Services (RCS)” – globalizacijos funkcijos
description: Šioje temoje aiškinama, kaip pasinaudoti „Microsoft Regulatory Configuration Services (RCS)” ir Visuotine saugykla, kad sukurtumėte ir pasinaudotumėte globalizacijos funkcijomis.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: cbb1d9a53a7a09ab525532f08553898c4e40223a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822786"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="2266c-103">„Regulatory Configuration Services (RCS)” – globalizacijos funkcijos</span><span class="sxs-lookup"><span data-stu-id="2266c-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2266c-104">Galite naudoti „Microsoft Regulatory Configuration Services (RCS)“, norėdami sukurti globalizacijos funkciją, naudojamą globalizacijos paslaugose, pavyzdžiui, el. sąskaitų faktūrų išrašymo paslaugai.</span><span class="sxs-lookup"><span data-stu-id="2266c-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="2266c-105">RCS leidžia atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="2266c-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="2266c-106">Nurodyti susijusius funkcijos komponentus.</span><span class="sxs-lookup"><span data-stu-id="2266c-106">Define related components of a feature.</span></span>
- <span data-ttu-id="2266c-107">Valdyti funkcijos ciklą naudojant funkcijos būseną.</span><span class="sxs-lookup"><span data-stu-id="2266c-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="2266c-108">Sukurti funkciją, kurią galima naudoti apibrėžtose aplinkose.</span><span class="sxs-lookup"><span data-stu-id="2266c-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="2266c-109">Bendrinti funkciją su kitomis organizacijomis.</span><span class="sxs-lookup"><span data-stu-id="2266c-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="2266c-110">Šios procedūros paaiškina, kaip vartotojas RCS gali pridėti globalizacijos funkciją ir susijusius komponentus, atnaujinti funkcijos būseną ir padaryti šią funkciją prieinamą, kad ji galėtų būti naudojama globalizacijos paslaugose.</span><span class="sxs-lookup"><span data-stu-id="2266c-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="2266c-111">Prieš atlikdami procedūras, turite atlikti veiksmus, susijusius su šiomis užduotimis:</span><span class="sxs-lookup"><span data-stu-id="2266c-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="2266c-112">Prisijungti prie savo RCS.</span><span class="sxs-lookup"><span data-stu-id="2266c-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="2266c-113">Sukurti ir aktyvuoti konfigūracijos teikėją.</span><span class="sxs-lookup"><span data-stu-id="2266c-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="2266c-114">Daugiau informacijos žr. [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2266c-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="2266c-115">Savo „Finance and Operations” programoje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2266c-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="2266c-116">Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="2266c-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="2266c-117">Jei jūsų įmonei RCS aplinka neparengta, pasirinkite **Regulatory services – Konfigūracija** ir vykdykite instrukcijas, kad ją parengtumėte.</span><span class="sxs-lookup"><span data-stu-id="2266c-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="2266c-118">Jei RCS aplinka jūsų įmonei jau parengta, pasiekite ją naudodami puslapio URL ir pasirinkdami prisijungimo parinktį.</span><span class="sxs-lookup"><span data-stu-id="2266c-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="2266c-119">Įjunkite Globalizacijos funkcijas</span><span class="sxs-lookup"><span data-stu-id="2266c-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="2266c-120">Savo RCS egzemplioriuje pasirinkite **Funkcijos valdymo** plytelę.</span><span class="sxs-lookup"><span data-stu-id="2266c-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="2266c-121">**Funkcijų valdymo** darbo srityje sąraše pasirinkite **Globalizacijos funkcijos** ir pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="2266c-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Globalizacijos funkcijos Funkcijų valdyme](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="2266c-123">Globalizacijos funkcijos</span><span class="sxs-lookup"><span data-stu-id="2266c-123">Globalization features</span></span>

<span data-ttu-id="2266c-124">Norėdami naudoti Globalizacijos funkciją, pirmiausia turite ją importuoti iš Visuotinės saugyklos ir sukurti savo versiją.</span><span class="sxs-lookup"><span data-stu-id="2266c-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="2266c-125">Yra du būdai, kaip pridėti Globalizacijos funkcijas:</span><span class="sxs-lookup"><span data-stu-id="2266c-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="2266c-126">Pridėkite išvestinę funkciją, pagrįstą esama funkcija, kuri buvo publikuota ar bendrai naudojama.</span><span class="sxs-lookup"><span data-stu-id="2266c-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="2266c-127">Pridėkite naują funkciją, kurią sukūrėte nuo pradžių.</span><span class="sxs-lookup"><span data-stu-id="2266c-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="2266c-128">Prieiga prie Globalizacijos funkcijų</span><span class="sxs-lookup"><span data-stu-id="2266c-128">Access Globalization features</span></span>

1. <span data-ttu-id="2266c-129">Įsitikinkite, kad **Globalizacijos funkcijos** funkcija yra įjungta Funkcijų valdyme, kaip aprašyta anksčiau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="2266c-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="2266c-130">Atverkite naują **Globalizacijos funkcijos** darbo sritį, o tada dalyje po **Funkcijos** pasirinkite **El. SF išrašymas** plytelę.</span><span class="sxs-lookup"><span data-stu-id="2266c-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Visuotinių funkcijų darbo sritis](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="2266c-132">**El. SF išrašymo funkcijos** puslapis atvertas.</span><span class="sxs-lookup"><span data-stu-id="2266c-132">The **e-Invoicing Features** page is opened.</span></span>

    ![El. sąskaitų faktūrų išrašymo funkcijų puslapis](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="2266c-134">Įtraukite išvestinę Globalizacijos funkciją</span><span class="sxs-lookup"><span data-stu-id="2266c-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="2266c-135">Galite pridėti naują Globalizacijos funkciją išvesdami ją iš esamos, kuri buvo publikuota ar bendrai naudojama.</span><span class="sxs-lookup"><span data-stu-id="2266c-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="2266c-136">Pasirinkite **Importuoti**, kad atvertumėte **Importuoti funkciją iš Visuotinės saugyklos** puslapio.</span><span class="sxs-lookup"><span data-stu-id="2266c-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Importuokite funkciją š Visuotinės saugyklos puslapio](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="2266c-138">Pasirinkite **Sinchronizuoti**, kad gautumėte naujausias funkcijas.</span><span class="sxs-lookup"><span data-stu-id="2266c-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="2266c-139">Sinchronizuotame sąraše yra funkcijų, kurias galite naudoti, nes jas publikavo „Microsoft ” arba dėl to, kad kitas konfigūracijos teikėjas bendrino jas su jumis.</span><span class="sxs-lookup"><span data-stu-id="2266c-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Sinchronizuotas funkcijų sąrašas](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="2266c-141">Sąraše pasirinkite importuotinas funkcijas ir pasirinkite **importuoti**.</span><span class="sxs-lookup"><span data-stu-id="2266c-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="2266c-142">Gausite pranešimą, kai atrinktos funkcijos bus sėkmingai importuotos.</span><span class="sxs-lookup"><span data-stu-id="2266c-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Sėkmingo importavimo pranešimas](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="2266c-144">Pasirinkite **Įtrauki**, tada išplečiamojo dialogo lango lauke pasirinkite **Pagrįstas esama versija** parinktį.</span><span class="sxs-lookup"><span data-stu-id="2266c-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="2266c-145">Įveskite funkcijos pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="2266c-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="2266c-146">Galimų funkcijų sąraše pasirinkite pagrindinę funkcijos versiją ir pasirinkite **Kurti priemonę**.</span><span class="sxs-lookup"><span data-stu-id="2266c-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Išvestos funkcijos pridėjimas](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="2266c-148">Jūsų pridėta funkcija sukuriama ir jos būsena yra **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="2266c-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Išvestinė funkcija, turinti Juodraščio būseną](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="2266c-150">Peržiūrėkite funkcijų komponentus, kad nustatytumėte, kurie naujiniai yra reikalingi:</span><span class="sxs-lookup"><span data-stu-id="2266c-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="2266c-151">Peržiūrėkite konfigūracijas, jei jums reikia tinkinti Elektroninių ataskaitų (ER) formatus ir jų susiejimą su formato priskyrimais, skirtais funkcijos versijai.</span><span class="sxs-lookup"><span data-stu-id="2266c-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="2266c-152">Peržiūrėkite sąranką, jei jums reikia tinkinti **Veiksmai** skirtuką, **Taikymo taisyklės** skirtuką arba **Kintamieji** skirtuką funkcijos versijai.</span><span class="sxs-lookup"><span data-stu-id="2266c-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="2266c-153">**Versijos** skirtuke pasirinkite **Įsigalioja nuo** datą ir įveskite aprašą, jei **Aprašas** laukas yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="2266c-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="2266c-154">Pasirinkite **Pakeisti būseną**, kad užbaigtumėte funkciją.</span><span class="sxs-lookup"><span data-stu-id="2266c-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="2266c-155">Baigtos funkcijos gali būti prieinamos tam tikrai aplinkai, kad jos galėtų būti naudojamos Globalizacijos paslaugose arba jos gali būti paskelbtos Visuotinėje saugykloje.</span><span class="sxs-lookup"><span data-stu-id="2266c-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="2266c-156">Funkcijos, turinčios **Funkcijos versijos būsena** vertę **Paskelbta**, gali būti bendrinamos su išorinėmis organizacijomis.</span><span class="sxs-lookup"><span data-stu-id="2266c-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="2266c-157">Įtraukite naują Globalizacijos funkciją</span><span class="sxs-lookup"><span data-stu-id="2266c-157">Add a new Globalization feature</span></span>

<span data-ttu-id="2266c-158">Galite pridėti naują Globalizacijos funkciją sukurdami ją nuo pradžių.</span><span class="sxs-lookup"><span data-stu-id="2266c-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="2266c-159">**Importuoti funkciją iš Visuotinės saugyklos** puslapyje pasirinkite **Pridėti**, tada išplečiamojo dialogo lango lauke pasirinkite **Nauja funkcija** parinktį.</span><span class="sxs-lookup"><span data-stu-id="2266c-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="2266c-160">Įveskite funkcijos pavadinimą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="2266c-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="2266c-161">Pasirinkite **Sukurti funkciją**.</span><span class="sxs-lookup"><span data-stu-id="2266c-161">Select **Create feature**.</span></span>

    ![Naujos funkcijos įtraukimas](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="2266c-163">**Versijos** skirtuke pasirinkite **Įsigalioja nuo** datą ir pasirinkite **Keisti būseną**, kad baigtumėte funkciją.</span><span class="sxs-lookup"><span data-stu-id="2266c-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="2266c-164">Baigtos funkcijos gali būti prieinamos tam tikrai aplinkai, kad jos galėtų būti naudojamos Globalizacijos paslaugose arba jos gali būti paskelbtos Visuotinėje saugykloje.</span><span class="sxs-lookup"><span data-stu-id="2266c-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="2266c-165">Funkcijos, turinčios **Funkcijos versijos būsena** vertę **Paskelbta**, gali būti bendrinamos su išorinėmis organizacijomis.</span><span class="sxs-lookup"><span data-stu-id="2266c-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="2266c-166">Funkcijos komponento apžvalga</span><span class="sxs-lookup"><span data-stu-id="2266c-166">Feature component overview</span></span>

<span data-ttu-id="2266c-167">Globalizacijos funkcijos susideda iš kelių komponentų:</span><span class="sxs-lookup"><span data-stu-id="2266c-167">Globalization features have several components:</span></span>

- <span data-ttu-id="2266c-168">**Versija** – šis komponentas palaiko funkcijų ciklo valdymą ir leidžia vartotojams valdyti skirtingas funkcijos versijas.</span><span class="sxs-lookup"><span data-stu-id="2266c-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="2266c-169">**Konfigūracijos** – šis komponentas leidžia vartotojams valdyti, peržiūrėti ir redaguoti ER formatus ir formatų susiejimus.</span><span class="sxs-lookup"><span data-stu-id="2266c-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="2266c-170">**Sąrankos** – šis komponentas leidžia globalizacijos paslaugų vartotojams, pavyzdžiui, el. SF paslaugos, tvarkyti susijusios funkcijos versijos sąranką.</span><span class="sxs-lookup"><span data-stu-id="2266c-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="2266c-171">Todėl jis palaiko lanksčią bendravimo ir atsakymų taisyklių konstrukciją.</span><span class="sxs-lookup"><span data-stu-id="2266c-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="2266c-172">**Aplinka** – šis komponentas leidžia globalizacijos paslaugų vartotojams, pvz., elektroninių SF paslaugos, valdyti aplinką, kurioje naudojama funkcijos versijos sąranka, ir suteikti autorizavimą vartotojams, kurie turės prieigą prie jos.</span><span class="sxs-lookup"><span data-stu-id="2266c-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="2266c-173">**Organizacijos** – šis komponentas leidžia vartotojams bendrinti funkciją su išorinėmis organizacijomis.</span><span class="sxs-lookup"><span data-stu-id="2266c-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="2266c-174">Funkcijos komponentų konfigūracija</span><span class="sxs-lookup"><span data-stu-id="2266c-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="2266c-175">Versija ir būsena</span><span class="sxs-lookup"><span data-stu-id="2266c-175">Version and status</span></span>

<span data-ttu-id="2266c-176">Versija naudojama Globalizacijos funkcijos ciklo valdymui valdyti.</span><span class="sxs-lookup"><span data-stu-id="2266c-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="2266c-177">Būsena gali būti keičiama **Būsena** lauke **Versija** skirtuke. Galimos šios būsenos:</span><span class="sxs-lookup"><span data-stu-id="2266c-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="2266c-178">**Juodraštis** – funkcija gali būti redaguojama tik tada, kai ji yra šios būsenos.</span><span class="sxs-lookup"><span data-stu-id="2266c-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="2266c-179">**Baigta** – funkcija ir visi susiję komponentai buvo užbaigti (baigti) ir jų negalima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="2266c-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="2266c-180">**Publikuota** – funkcija ir visi susiję komponentai publikuoti Visuotinėje saugykloje.</span><span class="sxs-lookup"><span data-stu-id="2266c-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="2266c-181">**Bendrinta** – funkcija ir visi susiję komponentai buvo bendrinti su išorinėmis organizacijomis.</span><span class="sxs-lookup"><span data-stu-id="2266c-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="2266c-182">**Įjungta** – funkcija ir visi susiję komponentai buvo įjungti Globalizacijos paslaugai, pvz., el. sąskaitų faktūrų išrašymo paslauga, naudoti.</span><span class="sxs-lookup"><span data-stu-id="2266c-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="2266c-183">Funkcijos turi būti nuosekliai perkeltos per kai kurias būsenas.</span><span class="sxs-lookup"><span data-stu-id="2266c-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="2266c-184">Todėl ne kiekviena būsena gali būti pasiekiama kiekviename ciklo etape.</span><span class="sxs-lookup"><span data-stu-id="2266c-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="2266c-185">Konfigūracijos</span><span class="sxs-lookup"><span data-stu-id="2266c-185">Configurations</span></span>

<span data-ttu-id="2266c-186">Toliau nurodyti veiksmai galimi šioms konfigūracijoms:</span><span class="sxs-lookup"><span data-stu-id="2266c-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="2266c-187">**Peržiūrėti** – peržiūrėkite paryškintas funkcijų konfigūracijas, kurias nereikia atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="2266c-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="2266c-188">**Redaguoti** – sukurkite pasirinktos konfigūracijos juodraštinę versiją, kad galėtumėte redaguoti formatą arba formatuoti susiejimą Formato dizaino įrankyje.</span><span class="sxs-lookup"><span data-stu-id="2266c-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="2266c-189">**Naikinti** – sunaikinkite pasirinktą funkcijos konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="2266c-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="2266c-190">**Pritaikyti kitoje vietoje** – pritaikykite funkciją kitam.</span><span class="sxs-lookup"><span data-stu-id="2266c-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="2266c-191">Daugiau informacijos rasite [Pritaikykite Globalizacijos funkcijas kitoje vietoje](#rebase) skyriuje, aptartame vėliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="2266c-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="2266c-192">Nustatymai</span><span class="sxs-lookup"><span data-stu-id="2266c-192">Setups</span></span>

<span data-ttu-id="2266c-193">Toliau nurodyti veiksmai galimi funkcijos sąrankai:</span><span class="sxs-lookup"><span data-stu-id="2266c-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="2266c-194">**Pridėti** – sukurkite naują funkcijos sąranką.</span><span class="sxs-lookup"><span data-stu-id="2266c-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="2266c-195">Ši funkcijos sąranka gali būti išvesta iš esamos funkcijos sąrankos arba sukurta nuo pradžių.</span><span class="sxs-lookup"><span data-stu-id="2266c-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="2266c-196">**Naikinti** – sunaikinkite pasirinktą funkcijos sąranką.</span><span class="sxs-lookup"><span data-stu-id="2266c-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="2266c-197">**Peržiūrėti** – peržiūrėkite paryškintą funkcijos sąranką, kurią nereikia keisti.</span><span class="sxs-lookup"><span data-stu-id="2266c-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="2266c-198">**Redaguoti** – kurkite, sunaikinkite arba modifikuokite trijų pagrindinių funkcijos sąrankos komponentų atributus:</span><span class="sxs-lookup"><span data-stu-id="2266c-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="2266c-199">Veiksmai ir jų parametrai</span><span class="sxs-lookup"><span data-stu-id="2266c-199">Actions and their parameters</span></span>
    - <span data-ttu-id="2266c-200">Taikymo taisyklės</span><span class="sxs-lookup"><span data-stu-id="2266c-200">Applicability rules</span></span>
    - <span data-ttu-id="2266c-201">Kintamieji</span><span class="sxs-lookup"><span data-stu-id="2266c-201">Variables</span></span>

![Funkcijos versijos sąrankos puslapis](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="2266c-203">Aplinkos</span><span class="sxs-lookup"><span data-stu-id="2266c-203">Environments</span></span>

<span data-ttu-id="2266c-204">Toliau nurodyti veiksmai galimi aplinkoms:</span><span class="sxs-lookup"><span data-stu-id="2266c-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="2266c-205">**Įjungti** – pasirinktai funkcijos versijai pasirinkite publikuotą aplinką ir pasirinkite **Įsigalioja nuo** datą, kada ji turėtų būti prieinama.</span><span class="sxs-lookup"><span data-stu-id="2266c-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="2266c-206">Daugiau informacijos rasite [Konfigūruokite aplinkas aktyvavimui](#configureenvironment) skyriuje, aptartame vėliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="2266c-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="2266c-207">**Atšaukti** – pašalinkite aplinką funkcijos sąrankai.</span><span class="sxs-lookup"><span data-stu-id="2266c-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="2266c-208">Organizacijos</span><span class="sxs-lookup"><span data-stu-id="2266c-208">Organizations</span></span>

<span data-ttu-id="2266c-209">Atlikite šiuos veiksmus, kad bendrintumėte Globalizacijos funkciją su išorine organizacija.</span><span class="sxs-lookup"><span data-stu-id="2266c-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="2266c-210">**El. sąskaitų faktūrų išrašymo funkcijos** puslapyje pasirinkite funkciją ir funkcijos versiją, kurią norite bendrinti.</span><span class="sxs-lookup"><span data-stu-id="2266c-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="2266c-211">**Organizacijos** skirtuke pasirinkite **Bendrinti su**, tada išplečiamajame dialogo lange įveskite organizacijos domeno pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2266c-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="2266c-212">Pasirinkite **Bendrinti**.</span><span class="sxs-lookup"><span data-stu-id="2266c-212">Select **Share**.</span></span>

    ![Funkcijos bendrinimas su organizacija](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="2266c-214">Funkcija bendrinama su pasirinkta organizacija ir ji prieinama tai organizacijai Visuotinėje saugykloje.</span><span class="sxs-lookup"><span data-stu-id="2266c-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="2266c-215">Iš ten funkcija gali būti importuojama į organizacijos egzempliorių RCS arba „Dynamics 365 Finance”, kad ja galima būtų naudotis.</span><span class="sxs-lookup"><span data-stu-id="2266c-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="2266c-216">Pritaikykite išvestines Globalizacijos funkcijas kitoje vietoje</span><span class="sxs-lookup"><span data-stu-id="2266c-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="2266c-217">Galite pritaikyti išvestinę Globalizacijos funkciją kitoje vietoje naujai arba atnaujintai pagrindinei funkcijos versijai.</span><span class="sxs-lookup"><span data-stu-id="2266c-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="2266c-218">Tokiu būdu pakeitimai, atlikti pagrindinėje versijoje, gali būti automatiškai atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="2266c-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="2266c-219">Atnaujintą pagrindinę funkcijos versiją sukuria pirminės konfigūracijos teikėjas, ji publikuojama arba bendrinama.</span><span class="sxs-lookup"><span data-stu-id="2266c-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Atnaujinta pagrindinės funkcijos versija](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="2266c-221">Pavyzdžiui, jei norite pritaikyti jūsų sukurtą išvestinę funkcijos versiją kitoje vietoje, pirmiausia turite gauti naujausią šios funkcijos versiją importuodami ją iš Visuotinės saugyklos.</span><span class="sxs-lookup"><span data-stu-id="2266c-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="2266c-222">**El. sąskaitų faktūrų išrašymo funkcijos** puslapyje pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="2266c-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="2266c-223">Pasirinkite **Sinchronizuoti**, kad gautumėte naujausias funkcijas.</span><span class="sxs-lookup"><span data-stu-id="2266c-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="2266c-224">Funkcijų sąraše pasirinkite funkcijas, kurias norite importuoti, ir tada pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="2266c-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Naujausios funkcijos versijos importavimas](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="2266c-226">Funkcijų sąraše pasirinkite funkciją, kurią norite pritaikyti kitoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="2266c-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="2266c-227">**Versija** skirtuke pasirinkite **Nauja**, kad sukurtumėte juodraštinę versiją.</span><span class="sxs-lookup"><span data-stu-id="2266c-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Nauja juodraštinė versija sukurta](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="2266c-229">Pasirinkite **Pritaikyti kitoje vietoje**.</span><span class="sxs-lookup"><span data-stu-id="2266c-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="2266c-230">Dialogo lange **Pritaikyti kitoje vietoje** pasirinkite naujausią funkcijos versiją, kurią norite pritaikyti kitoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="2266c-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Pritaikymo kitoje vietoje dialogo langas](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="2266c-232">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2266c-232">Select **OK**.</span></span>
9. <span data-ttu-id="2266c-233">Peržiūrėkite funkcijos komponentus ir atlikite būtinus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="2266c-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="2266c-234">Pasirinkite **Pakeisti būseną**, kad užbaigtumėte pritaikytą kitoje vietoje funkciją.</span><span class="sxs-lookup"><span data-stu-id="2266c-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="2266c-235">Kai pritaikymas kitoje vietoje baigiamas, galite atlikti papildomus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2266c-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="2266c-236">Pavyzdžiui, galite publikuoti funkciją ir ją padaryti prieinamą naudojimui Globalizacijos paslaugose.</span><span class="sxs-lookup"><span data-stu-id="2266c-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Funkcijos būsena atnaujinta į Baigta](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="2266c-238">Konfigūruoti aplinkas, skirtas Globalizacijos funkcijoms</span><span class="sxs-lookup"><span data-stu-id="2266c-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="2266c-239">Globalizacijos paslaugų vartotojai gali valdyti aplinką, kad nustatytų Globalizacijos funkciją ir suteiktų autorizavimą kitiems vartotojams, kurie turės prieigą prie jos.</span><span class="sxs-lookup"><span data-stu-id="2266c-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="2266c-240">**Globalizacijos funkcijos** darbo srityje, o tada dalyje po **Aplinkos** pasirinkite **El. SF išrašymas** plytelę.</span><span class="sxs-lookup"><span data-stu-id="2266c-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Globalizacijos funkcijų darbo sritis](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="2266c-242">Pasirinkite **Pagrindiniai saugyklos parametrai** ir pasirinkite **Nauja**, kad sukurtumėte „Azure Key Vault” slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="2266c-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="2266c-243">Įveskite pagrindinės saugyklos aprašą ir tada **Pagrindinės saugyklos URl** lauke įveskite URL, identifikuojantį Pagrindinės saugyklos šaltinį, esantį „Azure”.</span><span class="sxs-lookup"><span data-stu-id="2266c-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="2266c-244">**Sertifikatai** „FastTab” pasirinkite **Pridėti**, kad pridėtumėte sertifikatą, ir įveskite kiekvieno sertifikato pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="2266c-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Pridėtas sertifikatas](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="2266c-246">Pasirinkite **Nauja**, kad sukurtumėte naują aplinką.</span><span class="sxs-lookup"><span data-stu-id="2266c-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="2266c-247">Įveskite pavadinimą, aprašą ir bendrintos prieigos parašo atpažinimo ženklo slaptažodį, reikalingą saugojimui.</span><span class="sxs-lookup"><span data-stu-id="2266c-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="2266c-248">**Vartotojai**„FastTab” pasirinkite **Nauja**, kad pridėtumėte vartotoją, kuriam bus suteikta teisė pasiekti šią aplinką.</span><span class="sxs-lookup"><span data-stu-id="2266c-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="2266c-249">Įveskite vartotojo ID ir el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="2266c-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="2266c-250">Pakartokite 7 ir 8 žingsnius, jei norite pridėti daugiau vartotojų.</span><span class="sxs-lookup"><span data-stu-id="2266c-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="2266c-251">Pasirinkite **Publikuoti**, kad publikuotumėte aplinką.</span><span class="sxs-lookup"><span data-stu-id="2266c-251">Select **Publish** to publish the environment.</span></span>

    ![Publikuota aplinka](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]