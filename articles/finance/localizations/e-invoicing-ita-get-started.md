---
title: Darbo su elektroninių SF priedu Italijai pradžia
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu Italijai.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 140977a6eac145f35870d3516a4b0d0c794afe4b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894782"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a><span data-ttu-id="1b30a-103">Darbo su elektroninių SF priedu Italijai pradžia</span><span class="sxs-lookup"><span data-stu-id="1b30a-103">Get started with Electronic invoicing for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="1b30a-104">Italijos elektroninių SF išrašymo priedas šiuo metu gali nepalaikyti visų funkcijų, pasiekiamų elektroninėms SF „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="1b30a-104">Electronic invoicing for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="1b30a-105">Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis elektroninių SF išrašymo priedu Italijai.</span><span class="sxs-lookup"><span data-stu-id="1b30a-105">This topic provides information that will help you get started with Electronic invoicing for Italy.</span></span> <span data-ttu-id="1b30a-106">Ji padės atlikti konfigūracijos veiksmus, priklausančius nuo šalies, „Regulatory Configuration Services” (RCS) ir „Finance”.</span><span class="sxs-lookup"><span data-stu-id="1b30a-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="1b30a-107">Ji taip pat paaiškina, kaip pateikti elektronines SF, sugeneruotas Italijai būdingu formatu **„FatturaPA”**, naudojant paslaugą, ir kaip peržiūrėti apdorojimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="1b30a-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1b30a-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="1b30a-108">Prerequisites</span></span>

<span data-ttu-id="1b30a-109">Prieš atlikdami šioje temoje nurodytus veiksmus, turite atlikti veiksmus, esančius [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="1b30a-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="1b30a-110">RCS sąranka</span><span class="sxs-lookup"><span data-stu-id="1b30a-110">RCS setup</span></span>

<span data-ttu-id="1b30a-111">RCS nustatymo metu galėsite atlikti toliau pateiktas užduotis.</span><span class="sxs-lookup"><span data-stu-id="1b30a-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="1b30a-112">Importuoti el. SF išrašymo funkciją, skirtą kliento SF, kurių formatas **„FatturaPA”**, eksportavimui.</span><span class="sxs-lookup"><span data-stu-id="1b30a-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="1b30a-113">Peržiūrėti formato konfigūracijas, kurių reikia norint generuoti, pateikti ir gauti atsakymus apie elektronines SF.</span><span class="sxs-lookup"><span data-stu-id="1b30a-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="1b30a-114">Konfigūruoti įvykius, palaikančius elektroninių SF pateikimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="1b30a-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="1b30a-115">Publikuoti el. SF išrašymo funkciją.</span><span class="sxs-lookup"><span data-stu-id="1b30a-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="1b30a-116">„El. SF išrašymo funkcija” yra bendras išteklių, sukonfigūruotų ir publikuotų siekiant naudoti elektroninių SF išrašymo priedo serverį, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="1b30a-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="1b30a-117">Šiuo atveju kliento elektroninių SF eksportavimas yra el. SF išrašymo funkcija, kurią nustatysite.</span><span class="sxs-lookup"><span data-stu-id="1b30a-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="1b30a-118">El. SF išrašymo funkcijos importavimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="1b30a-119">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="1b30a-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="1b30a-120">Darbo srities **Globalizacijos funkcijos** dalyje **Funkcijos** pasirinkite plytelę **El. SF išrašymas**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="1b30a-121">Puslapyje **El. SF išrašymo funkcijos** pasirinkite **Importuoti**, norėdami importuoti el. SF išrašymo funkciją iš visuotinės saugyklos.</span><span class="sxs-lookup"><span data-stu-id="1b30a-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1b30a-122">Jei nematote pasiekiamų funkcijų sąrašo, pasirinkite **Sinchronizuoti**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="1b30a-123">Pasirinkite funkciją **El. SF eksportavimas (IT)** ir pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![Funkcijos El. SF eksportavimas (IT) importavimas](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="1b30a-125">Kai importuojate funkciją **El. SF eksportavimas (IT)** iš visuotinės saugyklos, taip pat importuojami visi kituose skyriuose aprašyti parametrai.</span><span class="sxs-lookup"><span data-stu-id="1b30a-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="1b30a-126">Naujos funkcijos El. SF eksportavimas (IT) versijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="1b30a-127">Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Naujos el. SF išrašymo funkcijos versijos įtraukimas](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="1b30a-129">Taip pat sukonfigūruosite elektroninių ataskaitų (ER) formatus, susietus su el. SF išrašymo funkcija.</span><span class="sxs-lookup"><span data-stu-id="1b30a-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="1b30a-130">Skirtuke **Konfigūracijos** pasirinkite **Įtraukti**, norėdami valdyti konfigūracijos versijas.</span><span class="sxs-lookup"><span data-stu-id="1b30a-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![El. SF išrašymo funkcijos konfigūracijos versijų valdymas](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="1b30a-132">Šio etapo metu galite įtraukti ir konfigūruoti įvairių failų, kurie naudojami Italijos el. SF eksportuoti, ER formatus.</span><span class="sxs-lookup"><span data-stu-id="1b30a-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="1b30a-133">Jei naudojate Italijos „FatturaPA” el. SF, naudokite toliau pateiktas standartines konfigūracijas arba faktines tinkintas konfigūracijas, kurias naudojate el. SF išrašymui.</span><span class="sxs-lookup"><span data-stu-id="1b30a-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="1b30a-134">Pardavimo SF (IT)</span><span class="sxs-lookup"><span data-stu-id="1b30a-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="1b30a-135">Projekto SF (IT)</span><span class="sxs-lookup"><span data-stu-id="1b30a-135">Project invoice (IT)</span></span>

    <span data-ttu-id="1b30a-136">Kai kuriate el. SF išrašymo funkciją, išvestą iš kitos el. SF išrašymo funkcijos, visi ER formatai perduodami iš pradinės funkcijos.</span><span class="sxs-lookup"><span data-stu-id="1b30a-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="1b30a-137">Pasirinkite konkrečią ER formato failo konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="1b30a-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="1b30a-138">Norėdami atidaryti puslapį **Formato dizaino įrankis**, pasirinkite **Redaguoti** arba **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Puslapio Formato dizaino įrankis atidarymas](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="1b30a-140">Norėdami redaguoti ir peržiūrėti ER formato failo konfigūracijas, naudokite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Formato dizaino įrankio puslapis](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="1b30a-142">El. SF išrašymo funkcijos nustatymų valdymas</span><span class="sxs-lookup"><span data-stu-id="1b30a-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="1b30a-143">Puslapio **El. SF išrašymo funkcijos** skirtuke **Nustatymai** pasirinkite **Įtraukti**, **Naikinti** arba **Redaguoti**, norėdami valdyti el. SF išrašymo funkcijos nustatymus.</span><span class="sxs-lookup"><span data-stu-id="1b30a-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![El. SF išrašymo funkcijos nustatymų valdymas](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="1b30a-145">Atlikdami šį veiksmą galite konfigūruoti įvykius, taikomus elektroninėms SF, įskaitant XML išvesties failų generavimą **„FatturaPA”** formatu ir pasirašymą skaitmeniniu būdu (jei reikia).</span><span class="sxs-lookup"><span data-stu-id="1b30a-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="1b30a-146">Pardavimo SF funkcijos nustatymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="1b30a-147">Puslapio **El. SF išrašymo funkcijos** skirtuko **Nustatymai** stulpelyje **Funkcijos nustatymas** pasirinkite **Pardavimo SF**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="1b30a-148">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-148">Select **Edit**.</span></span>
3. <span data-ttu-id="1b30a-149">Puslapyje **Funkcijos versijos nustatymas** pasirinkite skirtuką **Veiksmai**, norėdami valdyti veiksmų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1b30a-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="1b30a-150">Skirtukas Veiksmai nurodo operacijų, kurios turi būti vykdomos eilės tvarka siekiant visiškai įvykdyti įvykį, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1b30a-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Skirtukas Veiksmai](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="1b30a-152">Veiksmo ID</span><span class="sxs-lookup"><span data-stu-id="1b30a-152">Action ID</span></span> | <span data-ttu-id="1b30a-153">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-153">Action name</span></span>        | <span data-ttu-id="1b30a-154">Veiksmo aprašas</span><span class="sxs-lookup"><span data-stu-id="1b30a-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="1b30a-155">1</span><span class="sxs-lookup"><span data-stu-id="1b30a-155">1</span></span>         | <span data-ttu-id="1b30a-156">Pakeisti dokumentą</span><span class="sxs-lookup"><span data-stu-id="1b30a-156">Transform document</span></span> | <span data-ttu-id="1b30a-157">Kurkite el. SF XML failą **„FatturaPA”** formatu.</span><span class="sxs-lookup"><span data-stu-id="1b30a-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="1b30a-158">2</span><span class="sxs-lookup"><span data-stu-id="1b30a-158">2</span></span>         | <span data-ttu-id="1b30a-159">Pasirašyti dokumentą</span><span class="sxs-lookup"><span data-stu-id="1b30a-159">Sign document</span></span>      | <span data-ttu-id="1b30a-160">Pritaikykite skaitmeninį parašą XML failui.</span><span class="sxs-lookup"><span data-stu-id="1b30a-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="1b30a-161">Norėdami peržiūrėti ir tvarkyti taikymo taisykles, pasirinkite skirtuką **Taikymo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="1b30a-162">Pritaikymo taisyklės nurodo kontekstą, kuriame bus vykdomas veiksmas.</span><span class="sxs-lookup"><span data-stu-id="1b30a-162">Applicability rules define the context where the action will be run.</span></span>

    ![Skirtukas Taikymo taisyklės](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="1b30a-164">Pasirinkite skirtuką **Kintamieji**, norėdami peržiūrėti ir tvarkyti kintamuosius.</span><span class="sxs-lookup"><span data-stu-id="1b30a-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Skirtukas Kintamieji](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="1b30a-166">Nustatykite viešuosius kintamuosius, reikalingus veiksmams vykdyti.</span><span class="sxs-lookup"><span data-stu-id="1b30a-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="1b30a-167">Projekto SF funkcijos nustatymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="1b30a-168">Veiksmai ir parametrai, reikalingi **Projekto SF** funkcijos nustatymui konfigūruoti, yra labai panašūs į **Pardavimo SF** funkcijos nustatymo veiksmus ir parametrus.</span><span class="sxs-lookup"><span data-stu-id="1b30a-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="1b30a-169">Kai dirbate su projekto SF, peržiūrėkite pardavimo SF procedūras.</span><span class="sxs-lookup"><span data-stu-id="1b30a-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="1b30a-170">El. SF išrašymo funkcijos priskyrimas aplinkai</span><span class="sxs-lookup"><span data-stu-id="1b30a-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="1b30a-171">Puslapio **El. SF išrašymo funkcijos** skirtuke **Aplinkos** pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="1b30a-172">Lauke **Aplinka** pasirinkite aplinką.</span><span class="sxs-lookup"><span data-stu-id="1b30a-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="1b30a-173">Lauke **Galioja nuo** pasirinkite datą, kada aplinka turėtų įsigalioti.</span><span class="sxs-lookup"><span data-stu-id="1b30a-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="1b30a-174">Pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-174">Select **Enable**.</span></span> 

![El. SF išrašymo aplinkos įgalinimas](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="1b30a-176">El. SF išrašymo funkcijos publikavimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="1b30a-177">Galite publikuoti el. SF išrašymo funkciją pakeisdami versijos būseną į **Baigta** arba **Publikuota**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="1b30a-178">Versijos būsenos keitimas į Baigta</span><span class="sxs-lookup"><span data-stu-id="1b30a-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="1b30a-179">Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite el. SF išrašymo funkcijos versiją, kurios būsena yra **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="1b30a-180">Pasirinkite **Keisti būseną \> Baigta**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="1b30a-181">Versijos būsenos keitimas į Publikuota</span><span class="sxs-lookup"><span data-stu-id="1b30a-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="1b30a-182">Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite el. SF išrašymo funkcijos versiją, kurios būsena yra **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="1b30a-183">Pasirinkite **Keisti būseną \> Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-183">Select **Change status \> Publish**.</span></span>

![El. SF išrašymo funkcijos būsenos keitimas](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a><span data-ttu-id="1b30a-185">Elektroninių SF išrašymo priedo integravimo nustatymas „Finance”</span><span class="sxs-lookup"><span data-stu-id="1b30a-185">Set up Electronic invoicing integration in Finance</span></span>

<span data-ttu-id="1b30a-186">„Finance” nustatymo metu galėsite atlikti toliau pateiktas užduotis.</span><span class="sxs-lookup"><span data-stu-id="1b30a-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="1b30a-187">Importuokite ER duomenų modelį, ER duomenų modelio susiejimą ir konteksto konfigūracijas, skirtas „FatturaPA” el. SF.</span><span class="sxs-lookup"><span data-stu-id="1b30a-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="1b30a-188">Sukonfigūruokite sertifikatą, kurio reikia norint skaitmeniniu būdu pasirašyti Italijos el. SF.</span><span class="sxs-lookup"><span data-stu-id="1b30a-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="1b30a-189">ER duomenų modelio, duomenų modelio susiejimo ir formatų importavimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="1b30a-190">Darbo srityje **Elektroninės ataskaitos** įsitikinkite, kad **verslo dokumentų paslaugos** konfigūracijos teikėjas nustatytas į **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="1b30a-191">Pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="1b30a-192">Pasirinkite **Visuotiniai ištekliai \> Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="1b30a-193">Importuokite **SF modelis**, **SF modelio susiejimas** ir **Kliento SF konteksto modelis**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="1b30a-194">Italijos kliento elektroninių SF eksportavimo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="1b30a-195">Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="1b30a-196">Skirtuke **Funkcijos** pažymėkite žymės langelį **Įjungta** eilutėje, skirtoje funkcijos nuorodai **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![Funkcijos „FatturaPA” įjungimas](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="1b30a-198">Elektroninių dokumentų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-198">Configure electronic documents</span></span>

1. <span data-ttu-id="1b30a-199">Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="1b30a-200">Skirtuke **Elektroninis dokumentas** pasirinkite **Įtraukti** ir įveskite lenteles, kurių reikia norint generuoti Italijos el. SF:</span><span class="sxs-lookup"><span data-stu-id="1b30a-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="1b30a-201">**Lentelės pavadinimas:** Kliento SF žurnalas</span><span class="sxs-lookup"><span data-stu-id="1b30a-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="1b30a-202">**Lentelės pavadinimas:** Projekto SF</span><span class="sxs-lookup"><span data-stu-id="1b30a-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="1b30a-203">Nurodykite kiekvienos lentelės susijusį dokumento kontekstą.</span><span class="sxs-lookup"><span data-stu-id="1b30a-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="1b30a-204">Dalyje **Kliento SF žurnalas** pasirinkite **Kliento SF kontekstas**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="1b30a-205">Dalyje **Projekto SF** pasirinkite **Projekto SF kontekstas**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Atsakymų tipų nustatymas](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="1b30a-207">El. SF apdorojimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-207">Electronic invoice processing</span></span>

<span data-ttu-id="1b30a-208">Apdorojimo „Finance” metu atliksite toliau pateiktas užduotis.</span><span class="sxs-lookup"><span data-stu-id="1b30a-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="1b30a-209">Italijos el. SF generavimas naudojant elektroninių SF išrašymo priedą</span><span class="sxs-lookup"><span data-stu-id="1b30a-209">Generate Italian e-invoices through Electronic invoicing</span></span>
2. <span data-ttu-id="1b30a-210">Vykdymo žurnalų ir apdorojimo rezultatų peržiūra</span><span class="sxs-lookup"><span data-stu-id="1b30a-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="1b30a-211">Elektroninių SF generavimas</span><span class="sxs-lookup"><span data-stu-id="1b30a-211">Generate electronic invoices</span></span>

<span data-ttu-id="1b30a-212">Įjungus funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** ir suaktyvinus funkciją **IT00036**, nebegalima naudoti senojo „Finance” proceso, skirto Italijos el. SF generuoti.</span><span class="sxs-lookup"><span data-stu-id="1b30a-212">After you turn on the **Configurable Electronic invoicing integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="1b30a-213">Jis pakeičiamas nauju procesu pavadinimu **Pateikti elektroninius dokumentus**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="1b30a-214">Dokumentus galite pateikti neautomatiniu būdu, atsižvelgdami į el. SF dokumentų poreikį.</span><span class="sxs-lookup"><span data-stu-id="1b30a-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="1b30a-215">Prieš tęsdami įsitikinkite, kad nustatymas, reikalingas Italijos el. SF, buvo užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="1b30a-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="1b30a-216">Daugiau informacijos žr. [Kliento elektroninės SF](./emea-ita-e-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="1b30a-216">For more information, see [Customer electronic invoices](./emea-ita-e-invoices.md).</span></span> <span data-ttu-id="1b30a-217">Turėkite omenyje, kad kai kurie toje temoje aprašyti nustatymo veiksmai gali būti nepasiekiami dėl elektroninių SF išrašymo priedo aktyvinimo.</span><span class="sxs-lookup"><span data-stu-id="1b30a-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing activation.</span></span>

1. <span data-ttu-id="1b30a-218">Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Pateikti elektroninius dokumentus**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="1b30a-219">Pirmą kartą pateikę bet kokį dokumentą, nustatykite parinktį **Iš naujo pateikti dokumentus** į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="1b30a-220">Jei turite iš naujo pateikti dokumentą naudodami paslaugą, nustatykite šią parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="1b30a-221">„FastTab” **Įtrauktini įrašai** pasirinkite **Filtruoti**, kad būtų atidarytas dialogo langas **Užklausa**, kuriame galite kurti užklausą, norėdami pasirinkti dokumentus pateikimui.</span><span class="sxs-lookup"><span data-stu-id="1b30a-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Dialogo langas Pateikti elektroninius dokumentus](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="1b30a-223">Filtro užklausa</span><span class="sxs-lookup"><span data-stu-id="1b30a-223">Filter query</span></span>

1. <span data-ttu-id="1b30a-224">Dialogo lange **Užklausa** konfigūruokite pardavimo SF ir projekto SF filtravimo sąlygas arba palikite sąlygas tuščias, kad būtų įtrauktos visos nepateiktos SF.</span><span class="sxs-lookup"><span data-stu-id="1b30a-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Pateikimo filtro kriterijų nustatymas](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="1b30a-226">Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Užklausa**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="1b30a-227">Pasirinkti **Gerai**, norėdami pateikti pasirinktus dokumentus.</span><span class="sxs-lookup"><span data-stu-id="1b30a-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="1b30a-228">![PASTABA] Pirmą kartą bandant pateikti dokumentą naudojant paslaugą, būsite paraginti patvirtinti ryšį su elektroninių SF išrašymo priedu.</span><span class="sxs-lookup"><span data-stu-id="1b30a-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="1b30a-229">Pasirinkite **Spustelėkite čia, kad prisijungtumėte prie elektroninių dokumentų pateikimo paslaugos**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="1b30a-230">Pateikimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="1b30a-230">View submission logs</span></span>

<span data-ttu-id="1b30a-231">Galite peržiūrėti visų pateiktų dokumentų pateikimo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="1b30a-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="1b30a-232">Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="1b30a-233">Lauke **Dokumento tipas** pasirinkite **Kliento SF žurnalas** arba **Projekto SF**, norėdami filtruoti pagal reikiamus elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="1b30a-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Dokumento tipo pasirinkimas norint peržiūrėti pateikimo žurnalus](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="1b30a-235">Stulpelyje **Pateikimo būsena** rodoma reikšmė nurodo pateikimo proceso būseną.</span><span class="sxs-lookup"><span data-stu-id="1b30a-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="1b30a-236">Ji nurodo, ar procesas buvo vykdomas kaip sukonfigūruotas ir ar reikia papildomų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="1b30a-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="1b30a-237">Norėdami peržiūrėti išsamią pateikimo vykdymo žurnalų informaciją, veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="1b30a-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Pateikimo žurnalo informacijos peržiūra](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="1b30a-239">„FastTab” **Apdorojimo veiksmai** galite peržiūrėti veiksmų, sukonfigūruotų funkcijos versijoje, nustatytoje RCS, vykdymo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="1b30a-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="1b30a-240">Stulpelyje **Būsena** nurodoma, ar veiksmas sėkmingai įvykdytas.</span><span class="sxs-lookup"><span data-stu-id="1b30a-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="1b30a-241">„FastTab” **Veiksmų failai** galite peržiūrėti tarpinius failus, sugeneruotus veiksmų vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="1b30a-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="1b30a-242">Galite pasirinkti **Peržiūrėti**, norėdami atsisiųsti išvesties XML failą **FatturaPA** formatu ir peržiūrėti jo turinį.</span><span class="sxs-lookup"><span data-stu-id="1b30a-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b30a-243">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="1b30a-243">Related topics</span></span>

- [<span data-ttu-id="1b30a-244">Elektroninių SF išrašymo priedo apžvalga</span><span class="sxs-lookup"><span data-stu-id="1b30a-244">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="1b30a-245">Darbo su elektroninių SF priedu pradžia</span><span class="sxs-lookup"><span data-stu-id="1b30a-245">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="1b30a-246">Elektroninių SF nustatymas</span><span class="sxs-lookup"><span data-stu-id="1b30a-246">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]