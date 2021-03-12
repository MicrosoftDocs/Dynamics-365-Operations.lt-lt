---
title: Darbo su Meksikos elektroninių SF išrašymo priedu pradžia
description: Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis Meksikos elektroninių SF išrašymo priedu „Microsoft Dynamics 365 Finance” ir „Dynamics 365 Supply Chain Management”.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d91f377af2514af932ea585adb75a56bdee13871
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988488"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a><span data-ttu-id="dd77b-103">Darbo su Meksikos elektroninių SF išrašymo priedu pradžia</span><span class="sxs-lookup"><span data-stu-id="dd77b-103">Get started with the Electronic invoicing add-on for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="dd77b-104">Meksikos elektroninių SF išrašymo priedas šiuo metu gali nepalaikyti visų funkcijų, pasiekiamų „Comprobante Fiscal Digital por Internet” (CFDI) dokumente ir susijusiame integravime, įtaisytame „Microsoft Dynamics 365 Finance” arba „Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="dd77b-104">The Electronic invoicing add-on for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="dd77b-105">Šioje temoje pateikiama informacija, kuri padės jums pradėti naudotis Meksikos elektroninių SF išrašymo priedu.</span><span class="sxs-lookup"><span data-stu-id="dd77b-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Mexico.</span></span> <span data-ttu-id="dd77b-106">Ji padės atlikti konfigūracijos veiksmus, priklausančius nuo šalies, „Regulatory Configuration Services” (RCS) ir „Finance”.</span><span class="sxs-lookup"><span data-stu-id="dd77b-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="dd77b-107">Ji taip pat padeda jums atlikti veiksmus „Finance”, kurių reikia, kad CFDI SF būtų teikiamos naudojant paslaugą, ir paaiškina, kaip peržiūrėti apdorojimo rezultatus ir CFDI SF būsenas.</span><span class="sxs-lookup"><span data-stu-id="dd77b-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dd77b-108">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="dd77b-108">Prerequisites</span></span>

<span data-ttu-id="dd77b-109">Prieš atlikdami šioje temoje nurodytus veiksmus, turite atlikti veiksmus, esančius [Darbo su elektroninių SF išrašymo priedu pradžia](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="dd77b-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="dd77b-110">RCS sąranka</span><span class="sxs-lookup"><span data-stu-id="dd77b-110">RCS setup</span></span>

<span data-ttu-id="dd77b-111">RCS nustatymo metu galėsite atlikti toliau pateiktas užduotis.</span><span class="sxs-lookup"><span data-stu-id="dd77b-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="dd77b-112">Importuoti el. SF išrašymo funkciją, skirtą CFDI SF apdorojimui.</span><span class="sxs-lookup"><span data-stu-id="dd77b-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="dd77b-113">Peržiūrėti formato konfigūracijas, kurių reikia norint generuoti, pateikti ir gauti atsakymus apie CFDI SF ir pateikti bei gauti atsakymus apie atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="dd77b-114">Konfigūruoti įvykius, palaikančius CFDI SF pateikimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="dd77b-115">Publikuoti el. SF išrašymo funkciją, skirtą CFDI SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="dd77b-116">„El. SF išrašymo funkcija” yra bendras išteklių, sukonfigūruotų ir publikuotų siekiant naudoti elektroninių SF išrašymo priedo serverį, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="dd77b-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="dd77b-117">Šiuo atveju CFDI SF (MX) yra el. SF išrašymo funkcija, kurią nustatysite.</span><span class="sxs-lookup"><span data-stu-id="dd77b-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="dd77b-118">El. SF išrašymo funkcijos importavimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="dd77b-119">Prisijunkite prie jūsų RCS abonemento.</span><span class="sxs-lookup"><span data-stu-id="dd77b-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="dd77b-120">Darbo srities **Globalizacijos funkcijos** dalyje **Funkcijos** pasirinkite plytelę **El. SF išrašymas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="dd77b-121">Puslapyje **El. SF išrašymo funkcijos** pasirinkite **Importuoti**, norėdami importuoti funkciją **CFDI SF (MX)** iš visuotinės saugyklos.</span><span class="sxs-lookup"><span data-stu-id="dd77b-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dd77b-122">Jei sąraše nematote funkcijos, pasirinkite **Sinchronizuoti** ir pakartokite 3 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![CFDI SF (MX) funkcijos importavimas](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="dd77b-124">Kai importuojate funkciją **CFDI SF (MX)** iš visuotinės saugyklos, taip pat importuojami visi funkcijų parametrai, įskaitant konfigūracijas ir veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="dd77b-125">Naujos CFDI SF (MX) funkcijos versijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="dd77b-126">Galite sukurti naują versiją, jei, pavyzdžiui, reikia atnaujinti URL.</span><span class="sxs-lookup"><span data-stu-id="dd77b-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="dd77b-127">Daugiau informacijos žr. [El. CFDI SF išrašymas](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="dd77b-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="dd77b-128">Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![Naujos el. SF išrašymo funkcijos versijos įtraukimas](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="dd77b-130">Konfigūracijos versijos naujinimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-130">Update the configuration version</span></span>

1. <span data-ttu-id="dd77b-131">Puslapio **El. SF išrašymo funkcijos** skirtuke **Konfigūracijos** pasirinkite **Įtraukti** arba **Naikinti**, norėdami valdyti konfigūracijos versijas (ER failo formato konfigūracijas).</span><span class="sxs-lookup"><span data-stu-id="dd77b-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![El. SF išrašymo funkcijos konfigūracijų valdymas](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="dd77b-133">Kai kuriate naują versiją, visos konfigūracijos perduodamos iš paskutinės publikuotos versijos.</span><span class="sxs-lookup"><span data-stu-id="dd77b-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="dd77b-134">Norint apdoroti CFDI SF, būtinos toliau pateiktos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="dd77b-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="dd77b-135">CFDI SF (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="dd77b-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="dd77b-136">CFDI atsakymo pranešimo importavimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-136">CFDI response message import</span></span>
    - <span data-ttu-id="dd77b-137">CFDI klaidų žurnalo importavimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-137">CFDI error log import</span></span>
    - <span data-ttu-id="dd77b-138">CFDI atšaukimo užklausa (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="dd77b-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="dd77b-139">CFDI SF (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="dd77b-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="dd77b-140">Sąraše pasirinkite konfigūracijos versiją, tada pasirinkite **Redaguoti** arba **Peržiūrėti**, kad būtų atidarytas puslapis **Formato dizaino įrankis**, kuriame galite redaguoti arba peržiūrėti konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="dd77b-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Puslapio Formato dizaino įrankis atidarymas](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="dd77b-142">Norėdami redaguoti ir peržiūrėti ER formato failo konfigūracijas, naudokite puslapį **Formato dizaino įrankis**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="dd77b-143">Daugiau informacijos žr. [Elektroninių dokumentų konfigūracijų kūrimas](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="dd77b-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Formato dizaino įrankio puslapis](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="dd77b-145">El. SF išrašymo funkcijos nustatymų valdymas</span><span class="sxs-lookup"><span data-stu-id="dd77b-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="dd77b-146">Puslapio **El. SF išrašymo funkcijos** skirtuke **Nustatymai** pasirinkite **Įtraukti**, **Naikinti** arba **Redaguoti**, norėdami valdyti el. SF išrašymo funkcijos nustatymus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![El. SF išrašymo funkcijos nustatymų valdymas](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="dd77b-148">Norint pateikti CFDI SF autorizuoti (generuoti XML failą, pateikti XML failą ir apdoroti atsakymą), reikalingas **Pardavimo SF** funkcijos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="dd77b-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="dd77b-149">Norint pateikti CFDI SF atšaukimą, reikalingi funkcijų **Atšaukimas** ir **Atšaukti** nustatymai.</span><span class="sxs-lookup"><span data-stu-id="dd77b-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="dd77b-150">Pardavimo SF funkcijos nustatymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="dd77b-151">Puslapio **El. SF išrašymo funkcijos** skirtuko **Nustatymai** stulpelyje **Funkcijos nustatymas** pasirinkite **Pardavimo SF**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="dd77b-152">Pasirinkite **Redaguoti**, norėdami konfigūruoti veiksmus, taikymo taisykles ir kintamuosius.</span><span class="sxs-lookup"><span data-stu-id="dd77b-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![El. SF išrašymo funkcijos nustatymo redagavimas](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="dd77b-154">Puslapyje **Funkcijos versijos nustatymas** pasirinkite skirtuką **Veiksmai**, norėdami valdyti veiksmų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="dd77b-155">Skirtukas Veiksmai nurodo operacijų, kurios turi būti vykdomos eilės tvarka siekiant visiškai įvykdyti įvykį, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Skirtukas Veiksmai](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="dd77b-157">Veiksmo ID</span><span class="sxs-lookup"><span data-stu-id="dd77b-157">Action ID</span></span> | <span data-ttu-id="dd77b-158">Veiksmas</span><span class="sxs-lookup"><span data-stu-id="dd77b-158">Action</span></span>                   | <span data-ttu-id="dd77b-159">Veiksmo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-159">Action name</span></span>                                  | <span data-ttu-id="dd77b-160">Veiksmo aprašas</span><span class="sxs-lookup"><span data-stu-id="dd77b-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="dd77b-161">1</span><span class="sxs-lookup"><span data-stu-id="dd77b-161">1</span></span>         | <span data-ttu-id="dd77b-162">Pakeisti dokumentą</span><span class="sxs-lookup"><span data-stu-id="dd77b-162">Transform document</span></span>       | <span data-ttu-id="dd77b-163">Generuoti CFDI el. SF be skaitmeninio parašo</span><span class="sxs-lookup"><span data-stu-id="dd77b-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="dd77b-164">Generuojama CFDI el. SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="dd77b-165">2</span><span class="sxs-lookup"><span data-stu-id="dd77b-165">2</span></span>         | <span data-ttu-id="dd77b-166">Pasirašyti dokumentą</span><span class="sxs-lookup"><span data-stu-id="dd77b-166">Sign document</span></span>            | <span data-ttu-id="dd77b-167">Skaitmeninis parašas</span><span class="sxs-lookup"><span data-stu-id="dd77b-167">Digital sign</span></span>                                 | <span data-ttu-id="dd77b-168">Pateikimo el. SF pasirašoma skaitmeniniu būdu.</span><span class="sxs-lookup"><span data-stu-id="dd77b-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="dd77b-169">3</span><span class="sxs-lookup"><span data-stu-id="dd77b-169">3</span></span>         | <span data-ttu-id="dd77b-170">Iškviesti Meksikos PAC tarnybą</span><span class="sxs-lookup"><span data-stu-id="dd77b-170">Call Mexican PAC service</span></span> | <span data-ttu-id="dd77b-171">Pateikti CFDI el. SF</span><span class="sxs-lookup"><span data-stu-id="dd77b-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="dd77b-172">„Windows” ryšio platformos (WCF) klientas pateikia CFDI el. SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="dd77b-173">4</span><span class="sxs-lookup"><span data-stu-id="dd77b-173">4</span></span>         | <span data-ttu-id="dd77b-174">Apdoroti atsakymą</span><span class="sxs-lookup"><span data-stu-id="dd77b-174">Process response</span></span>         | <span data-ttu-id="dd77b-175">Analizuoti žiniatinklio tarnybos atsakymą</span><span class="sxs-lookup"><span data-stu-id="dd77b-175">Analyze web service response</span></span>                 | <span data-ttu-id="dd77b-176">Analizuojamas žiniatinklio tarnybos atsakymas ir grąžinamas klaidų žurnalas.</span><span class="sxs-lookup"><span data-stu-id="dd77b-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="dd77b-177">Meksikos PAC žiniatinklio tarnybų URL nustatymas</span><span class="sxs-lookup"><span data-stu-id="dd77b-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="dd77b-178">Puslapio **Funkcijos versijos nustatymas** skirtuko **Veiksmai** „FastTab” **Veiksmai** pasirinkite **Iškviesti Meksikos PAC tarnybą**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="dd77b-179">„FastTab” **Parametrai** lauke **URL adresas** įveskite CFDI SF pateikimo žiniatinklio tarnybos URL.</span><span class="sxs-lookup"><span data-stu-id="dd77b-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="dd77b-180">Atlikite tuos pačius veiksmus, norėdami atnaujinti URL, skirtą funkcijų **Atšaukti** ir **Atšaukimo užklausa** nustatymų veiksmui **Iškviesti Meksikos PAC tarnybą**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="dd77b-181">Juodraščio versijos priskyrimas el. SF išrašymo aplinkai</span><span class="sxs-lookup"><span data-stu-id="dd77b-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="dd77b-182">Puslapio **El. SF išrašymo funkcijos** skirtuke **Aplinkos** pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="dd77b-183">Lauke **Aplinka** pasirinkite aplinką.</span><span class="sxs-lookup"><span data-stu-id="dd77b-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="dd77b-184">Lauke **Galioja nuo** pasirinkite datą, kada aplinka turėtų įsigalioti.</span><span class="sxs-lookup"><span data-stu-id="dd77b-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="dd77b-185">Pasirinkite **Įjungti**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-185">Select **Enable**.</span></span>

![El. SF išrašymo aplinkos įgalinimas](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="dd77b-187">Versijos būsenos keitimas į Baigta</span><span class="sxs-lookup"><span data-stu-id="dd77b-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="dd77b-188">Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite el. SF išrašymo funkcijos versiją, kurios būsena yra **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="dd77b-189">Pasirinkite **Keisti būseną \> Baigta**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="dd77b-190">Versijos būsenos keitimas į Publikuota</span><span class="sxs-lookup"><span data-stu-id="dd77b-190">Change the version status to Published</span></span>

- <span data-ttu-id="dd77b-191">Puslapio **El. SF išrašymo funkcijos** skirtuke **Versijos** pasirinkite **Keisti būseną \> Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="dd77b-192">El. SF išrašymo funkcijos publikavimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="dd77b-193">Puslapyje **El. SF išrašymo funkcijos** pasirinkite skirtuką **Versijos**, norėdami valdyti funkcijos **CFDI SF (MX)** būseną.</span><span class="sxs-lookup"><span data-stu-id="dd77b-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="dd77b-194">Pasirinkite **Keisti būseną**, norėdami pakeisti funkcijos būseną.</span><span class="sxs-lookup"><span data-stu-id="dd77b-194">Select **Change status** to change the status of the feature.</span></span>

![El. SF išrašymo funkcijos būsenos keitimas](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="dd77b-196">Elektroninių SF išrašymo priedo integravimo nustatymas „Finance”</span><span class="sxs-lookup"><span data-stu-id="dd77b-196">Set up Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="dd77b-197">Norėdami nustatyti elektroninių SF išrašymo priedą „Finance”, atlikite toliau pateiktas užduotis.</span><span class="sxs-lookup"><span data-stu-id="dd77b-197">To set up the Electronic invoicing add-on in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="dd77b-198">Importuokite ER duomenų modelį, ER duomenų modelio susiejimą ir formatus, reikalingus CFDI SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="dd77b-199">Konfigūruokite atsakymų tipus CFDI SF atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="dd77b-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="dd77b-200">Šie atsakymų tipai naudojami įgaliotojo sertifikavimo teikėjo (PAC) serverio atsakymui.</span><span class="sxs-lookup"><span data-stu-id="dd77b-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="dd77b-201">ER duomenų modelio, ER duomenų modelio susiejimo ir konteksto konfigūracijų, reikalingų CFDI SF, importavimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="dd77b-202">Prisijunkite prie „Finance“.</span><span class="sxs-lookup"><span data-stu-id="dd77b-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="dd77b-203">Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="dd77b-204">Įsitikinkite, kad šis konfigūracijos teikėjas nustatytas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="dd77b-205">Daugiau informacijos apie tai, kaip nustatyti teikėją į **Aktyvus**, žr. [Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="dd77b-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="dd77b-206">Pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="dd77b-207">Pasirinkite **Visuotiniai ištekliai \> Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="dd77b-208">Importuokite **SF modelis**, **SF modelio susiejimas**, **CFDI SF formatas (MX)**, **CFDI SF atšaukimo užklausos formatas (MX)** ir **CFDI SF atšaukimo formatas (MX)**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="dd77b-209">CFDI SF apdorojimo funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="dd77b-210">Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="dd77b-211">Skirtuke **Funkcijos** pažymėkite žymės langelį **Įjungti** eilutėse, skirtose funkcijos nuorodoms **MX-00010** ir **MX-00016**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![CFDI SF apdorojimo funkcijų įjungimas](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="dd77b-213">ER konfigūracijų importavimas ir CFDI SF naujinimo atsakymų tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="dd77b-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="dd77b-214">Importuokite ER konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="dd77b-214">Import ER configurations</span></span>

1. <span data-ttu-id="dd77b-215">Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **„Microsoft”**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="dd77b-216">Pasirinkite **Saugyklos**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="dd77b-217">Pasirinkite **Visuotiniai ištekliai \> Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="dd77b-218">Importuokite **Atsakymo pranešimo modelis**, **CFDI klaidų žurnalo importavimas (MX)** ir **CFDI atsakymo pranešimo importavimas (MX)**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="dd77b-219">Atsakymų tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="dd77b-219">Set up the response types</span></span>

1. <span data-ttu-id="dd77b-220">Eikite į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="dd77b-221">Skirtuke **Elektroninis dokumentas** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="dd77b-222">Įveskite kliento SF žurnalą, tada lauke **Lentelės pavadinimas** pasirinkite projekto SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="dd77b-223">Nurodykite kiekvienos lentelės susijusį dokumento kontekstą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="dd77b-224">Dalyje **Kliento SF žurnalas** įveskite **Kliento SF kontekstas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="dd77b-225">Dalyje **Projekto SF** įveskite **Projekto SF kontekstas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="dd77b-226">Pasirinkite **Atsakymų tipai**, norėdami sukonfigūruoti atsakymų tipus, kuriuos galima grąžinti iš elektroninių SF išrašymo priedo ir įtraukti į kliento SF žurnalą ar projekto SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-226">Select **Response types** to configure the response types that can be returned from the Electronic invoicing add-on and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="dd77b-227">Pasirinkite **Naujas**, tada lauke **Atsakymo tipas** pasirinkite **Atsakymas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="dd77b-228">Lauke **Pateikimo būsena** pasirinkite **Laukiama**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="dd77b-229">Lauke **Modelio susiejimas** pasirinkite **Atsakymo pranešimo importavimo formatas – modelio susiejimas iš atsakymo pranešimo**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="dd77b-230">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-230">Select **Save**.</span></span>
9. <span data-ttu-id="dd77b-231">Pasirinkite **Naujas**, tada lauke **Atsakymo tipas** pasirinkite **Atsakymo duomenys**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="dd77b-232">Lauke **Pateikimo būsena** pasirinkite **Laukiama**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="dd77b-233">Lauke **Modelio susiejimas** pasirinkite **CFDI atsakymo duomenų importavimo formatas (informacija) – atsakymo duomenų importavimas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="dd77b-234">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="dd77b-235">Elektroninių SF apdorojimas „Finance”</span><span class="sxs-lookup"><span data-stu-id="dd77b-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="dd77b-236">CFDI SF apdorojimo metu „Finance” naudodami elektroninių SF išrašymo priedą galite atlikti toliau pateiktas užduotis.</span><span class="sxs-lookup"><span data-stu-id="dd77b-236">During the processing of CFDI invoices in Finance through the Electronic invoicing add-on, you can perform the following tasks:</span></span>

- <span data-ttu-id="dd77b-237">Pateikti CFDI SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="dd77b-238">Peržiūrėti pateikimo vykdymo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-238">View the submission execution logs.</span></span>
- <span data-ttu-id="dd77b-239">Pateikti CFDI SF atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="dd77b-240">CFDI SF pateikimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-240">Submit CFDI invoices</span></span>

<span data-ttu-id="dd77b-241">Po to, kai įjungiate funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**, proceso **Elektroninės SF eksportavimas / importavimas** (**Gautinos sumos \> SF \> El. SF**), skirto CFDI SF pateikti, nebegalima naudoti.</span><span class="sxs-lookup"><span data-stu-id="dd77b-241">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="dd77b-242">Jis pakeičiamas nauju procesu pavadinimu **Pateikti elektroninius dokumentus**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="dd77b-243">Prieš pradėdami naudoti naują procesą **Pateikti elektroninius dokumentus**, įsitikinkite, kad atliktas reikiamas Meksikos el. SF nustatymas.</span><span class="sxs-lookup"><span data-stu-id="dd77b-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="dd77b-244">Daugiau informacijos žr. [CFDI 3.3 maketo versija](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="dd77b-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="dd77b-245">Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Pateikti elektroninius dokumentus**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="dd77b-246">Pirmą kartą pateikę bet kokį dokumentą, visada nustatykite parinktį **Iš naujo pateikti dokumentus** į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="dd77b-247">Jei turite iš naujo pateikti dokumentą naudodami paslaugą, nustatykite šią parinktį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="dd77b-248">„FastTab” **Įtrauktini įrašai** pasirinkite **Filtruoti**, kad būtų atidarytas dialogo langas **Užklausa**, kuriame galite kurti užklausą, norėdami pasirinkti dokumentus pateikimui.</span><span class="sxs-lookup"><span data-stu-id="dd77b-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![CFDI dokumento pateikimas](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="dd77b-250">Pirmą kartą bandant pateikti dokumentą naudojant paslaugą, būsite paraginti patvirtinti ryšį su elektroninių SF išrašymo priedu.</span><span class="sxs-lookup"><span data-stu-id="dd77b-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="dd77b-251">Pasirinkite **Spustelėkite čia, kad prisijungtumėte prie elektroninių dokumentų pateikimo paslaugos**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="dd77b-252">Pateikimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="dd77b-252">View submission logs</span></span>

<span data-ttu-id="dd77b-253">Galite peržiūrėti visų pateiktų dokumentų arba tik vieno pateikto dokumento pateikimo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="dd77b-254">Visų pateikimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="dd77b-254">View all submission logs</span></span>

<span data-ttu-id="dd77b-255">Įjungus funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**, galima naudoti naują puslapį, leidžiantį sekti dokumento pateikimo procesą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-255">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="dd77b-256">Galite naudoti šį puslapį norėdami peržiūrėti visų pateiktų dokumentų pateikimo žurnalus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="dd77b-257">Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="dd77b-258">Lauke **Dokumento tipas** pasirinkite **Kliento SF žurnalas**, norėdami filtruoti pagal reikiamus elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Dokumento tipo pasirinkimas norint peržiūrėti pateikimo žurnalus](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="dd77b-260">Norėdami peržiūrėti išsamią pateikimo vykdymo žurnalų informaciją, veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Pateikimo žurnalo informacijos peržiūra](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="dd77b-262">Pateikimo žurnalų informacija suskirstyta į tris toliau pateiktus „FastTab”.</span><span class="sxs-lookup"><span data-stu-id="dd77b-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="dd77b-263">**Apdorojimo veiksmai** – šis „FastTab” nurodo veiksmų, sukonfigūruotų funkcijos versijoje, nustatytoje RCS, vykdymo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="dd77b-264">Stulpelyje **Būsena** nurodoma, ar veiksmas sėkmingai įvykdytas.</span><span class="sxs-lookup"><span data-stu-id="dd77b-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="dd77b-265">**Veiksmų failai** – šis „FastTab” nurodo tarpinius failus, sugeneruotus veiksmų vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="dd77b-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="dd77b-266">Galite pasirinkti **Peržiūrėti**, norėdami atsisiųsti failą ir jį peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="dd77b-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="dd77b-267">**Apdorojimo veiksmų žurnalas** – šis „FastTab” nurodo ryšio tarp elektroninių SF išrašymo priedo ir tikslinės žiniatinklio tarnybos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-267">**Processing action log** – This FastTab shows the results of the communication between the Electronic invoicing add-on and the target web service.</span></span> <span data-ttu-id="dd77b-268">Taip pat rodoma, ką pateikė žiniatinklio tarnybos apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="dd77b-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="dd77b-269">Stulpelyje **Klaidos kodas** rodomas grąžinimo kodas, kurį pateikė autorizavimo žiniatinklio tarnyba.</span><span class="sxs-lookup"><span data-stu-id="dd77b-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="dd77b-270">Kai pateikta CFDI SF patvirtinama, jos būsena atnaujinama į **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="dd77b-271">Pateikimo žurnalų peržiūra iš CFDI SF</span><span class="sxs-lookup"><span data-stu-id="dd77b-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="dd77b-272">Įjungę funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**, taip pat galite peržiūrėti pateikimo žurnalus iš CFDI SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-272">After you turn on the **ConfigurableElectronic invoicing add-on integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="dd77b-273">Eikite į **Gautinos sumos \> Užklausos ir ataskaitos \> CFDI (elektroninės SF)**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="dd77b-274">Pasirinkite CFDI SF, kuri buvo pateikta po to, kai buvo įjungta funkcija **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>
3. <span data-ttu-id="dd77b-275">Veiksmų srities skirtuke **Retrospektyva** pasirinkite **Elektroninio dokumento žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Pateikimo žurnalų peržiūra iš CFDI SF](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="dd77b-277">Mygtukas **Retrospektyva** pasiekiamas CFDI SF, kurios buvo pateiktos prieš funkcijos **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** įjungimą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing add-on integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="dd77b-278">Mygtukas **Retrospektyva** nėra pasiekiamas CFDI SF, pateiktoms po funkcijos **Konfigūruojamas elektroninių SF išrašymo priedo integravimas** įjungimo.</span><span class="sxs-lookup"><span data-stu-id="dd77b-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="dd77b-279">CFDI SF atšaukimo pateikimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="dd77b-280">Įjungus funkciją **Konfigūruojamas elektroninių SF išrašymo priedo integravimas**, nebegalima naudoti senojo CFDI SF atšaukimo proceso.</span><span class="sxs-lookup"><span data-stu-id="dd77b-280">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="dd77b-281">Jis pakeičiamas nauju atšaukimo procesu, kuris įdėtas puslapyje **Elektroninių dokumentų pateikimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="dd77b-282">Eikite į **Gautinos sumos \> Užklausos ir ataskaitos \> CFDI (elektroninės SF)**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="dd77b-283">Jei CFDI SF būsena yra **Patvirtinta**, pasirinkite **Funkcijos \> Atšaukti CFDI**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="dd77b-284">Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="dd77b-285">Pasirinkite CFDI SF, tada pasirinkite **Funkcijos \> Siųsti susijusius pateikimus**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="dd77b-286">Įveskite susijusio pateikimo aprašą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="dd77b-287">Atšaukimo pateikimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="dd77b-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="dd77b-288">Eikite į **Organizacijos administravimas \> Laikotarpio \> Elektroniniai dokumentai \> Elektroninio dokumento pateikimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="dd77b-289">Lauke **Dokumento tipas** pasirinkite **Kliento SF žurnalas**, norėdami filtruoti tik pagal kliento SF žurnalo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="dd77b-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="dd77b-290">Pasirinkite CFDI SF, tada veiksmų srityje pasirinkite **Užklausos \> Susijęs pateikimas**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="dd77b-291">Puslapyje **Susiję pateikimai** rodomi visi susiję pateikimai ir konkrečių CFDI SF pateikimo būsenos.</span><span class="sxs-lookup"><span data-stu-id="dd77b-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="dd77b-292">Toliau pateiktoje iliustracijoje pirmoji eilutė nurodo pateikimą, kuris pateikė CFDI SF patvirtinimo užklausą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="dd77b-293">Antroji eilutė nurodo pateikimą, atšaukusį CFDI SF.</span><span class="sxs-lookup"><span data-stu-id="dd77b-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Atšaukimo pateikimo žurnalų peržiūra](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="dd77b-295">Norėdami peržiūrėti išsamią pateikimo vykdymo žurnalų informaciją, veiksmų srityje pasirinkite **Užklausos \> Pateikimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Atšaukimo pateikimo žurnalų informacijos peržiūra](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="dd77b-297">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="dd77b-297">Privacy notice</span></span>
<span data-ttu-id="dd77b-298">Įgalinant funkcijas MX-00010 ir MX-00016 (CFDI SF ir CFDI atšaukimas) gali reikėti siųsti ribotus duomenis, įskaitant organizacijos mokesčių registracijos ID.</span><span class="sxs-lookup"><span data-stu-id="dd77b-298">Enabling the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="dd77b-299">Jie bus persiųsti mokesčių inspekcijos patvirtintoms trečiųjų šalių agentūroms, kad būtų galima siųsti elektronines SF šiai mokesčių inspekcijai iš anksto nustatytu formatu, reikalingu integravimui su vyriausybės žiniatinklio tarnyba.</span><span class="sxs-lookup"><span data-stu-id="dd77b-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="dd77b-300">Administratorius gali įjungti ir išjungti funkcijas MX-00010 ir MX-00016 (CFDI SF ir CFDI atšaukimas), nuėjęs į **Organizacijos administravimas \> Nustatymas \> Elektroninių dokumentų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dd77b-300">An administrator can enable and disable the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="dd77b-301">Pasirinkite skirtuką **Funkcijos**, pasirinkite eilutes, kuriose yra funkcijos MX-00010 ir MX-00016, tada atlikite reikiamą žymėjimą.</span><span class="sxs-lookup"><span data-stu-id="dd77b-301">Select the **Features** tab, select the rows containing the MX-00010 and MX-00016 features, and then make the appropriate selection.</span></span> <span data-ttu-id="dd77b-302">Duomenims, importuotiems iš šių išorinių sistemų į šią „Dynamics 365” internetinę paslaugą, taikomos [privatumo nuostatos](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="dd77b-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="dd77b-303">Daugiau informacijos ieškokite skyriuose Privatumo pranešimas, esančiuose konkrečios šalies funkcijos dokumentacijoje.</span><span class="sxs-lookup"><span data-stu-id="dd77b-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd77b-304">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dd77b-304">Additional resources</span></span>

- [<span data-ttu-id="dd77b-305">Elektroninių SF išrašymo priedo apžvalga</span><span class="sxs-lookup"><span data-stu-id="dd77b-305">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="dd77b-306">Darbo su elektroninių SF išrašymo priedu pradžia</span><span class="sxs-lookup"><span data-stu-id="dd77b-306">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="dd77b-307">Elektroninių SF išrašymo priedo nustatymas</span><span class="sxs-lookup"><span data-stu-id="dd77b-307">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
