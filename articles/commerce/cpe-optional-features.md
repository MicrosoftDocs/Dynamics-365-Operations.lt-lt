---
title: Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinimo aplinkoje
description: Šiame skyriuje paaiškinama, kaip sukonfigūruoti pasirenkamas funkcija „Microsoft Dynamics 365 Commerce“ vertinimo aplinkoje.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a93429e836d818458f11f6f6821fda237edc291
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936985"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="e49df-103">Pasirinktinių „Dynamics 365 Commerce” vertinimo aplinkos funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e49df-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e49df-104">Šiame skyriuje paaiškinama, kaip sukonfigūruoti pasirenkamas funkcija „Microsoft Dynamics 365 Commerce“ vertinimo aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="e49df-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e49df-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="e49df-105">Prerequisites</span></span>

<span data-ttu-id="e49df-106">Jei norite įvertinti operacines el. pašto funkcijas, turi būti įvykdytos šios būtinosios sąlygos:</span><span class="sxs-lookup"><span data-stu-id="e49df-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="e49df-107">Turite prieinamą elektroninio pašto serverį („Simple Mail Transfer Protocol“ \[SMTP\] serverį), kuris gali būti naudojamas „Microsoft Azure“ prenumeratai, kuria aprūpinote savo vertinimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="e49df-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="e49df-108">Turite pasiekiamus serverio visiškai apibrėžtą domeno vardą (FQDN) / IP adresą, SMTP prievado numerį ir autentifikavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="e49df-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="e49df-109">Vaizdų posistemio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e49df-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="e49df-110">Pagrindinio medijos URL radimas</span><span class="sxs-lookup"><span data-stu-id="e49df-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="e49df-111">Kad galėtumėte atlikti šią procedūrą, turite atlikti dalyje [Svetainės nustatymas programoje „Commerce“](cpe-post-provisioning.md#set-up-your-site-in-commerce) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e49df-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="e49df-112">Prisijunkite prie komercijos svetainės kūrėjo naudodami URL, kurį užsirašėte pradėdami „e-Commerce“ parengimo metu (žr. [Pradėti „e-Commerce“](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="e49df-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="e49df-113">Atidarykite **„Fabrikam“** svetainę.</span><span class="sxs-lookup"><span data-stu-id="e49df-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="e49df-114">Meniu kairėje pasirinkite **Medijos biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="e49df-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="e49df-115">Pasirinkite bet kurį vieną vaizdo išteklių.</span><span class="sxs-lookup"><span data-stu-id="e49df-115">Select any single image asset.</span></span>
1. <span data-ttu-id="e49df-116">Dešinėje esančiame ypatybių inspektoriuje suraskite ypatybę **Viešasis URL**.</span><span class="sxs-lookup"><span data-stu-id="e49df-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="e49df-117">Jos reikšmė yra URL.</span><span class="sxs-lookup"><span data-stu-id="e49df-117">The value is a URL.</span></span> <span data-ttu-id="e49df-118">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e49df-118">Here is an example:</span></span>

    <span data-ttu-id="e49df-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="e49df-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="e49df-120">Paskutinį URL identifikatorių (pirmiau pateiktame pavyzdyje – **MA1nQC**) pakeiskite eilute **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="e49df-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="e49df-121">Toliau parodyta, kaip atrodo taip pakeistas URL pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e49df-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="e49df-122">Šis URL yra jūsų pagrindinis medijos URL.</span><span class="sxs-lookup"><span data-stu-id="e49df-122">This URL is your media base URL.</span></span> <span data-ttu-id="e49df-123">Jį pasižymėkite.</span><span class="sxs-lookup"><span data-stu-id="e49df-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="e49df-124">Pagrindinio medijos URL naujinimas</span><span class="sxs-lookup"><span data-stu-id="e49df-124">Update the media base URL</span></span>

1. <span data-ttu-id="e49df-125">Prisijunkite prie komercijos būstinės.</span><span class="sxs-lookup"><span data-stu-id="e49df-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e49df-126">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="e49df-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="e49df-127">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-127">Select **Edit**.</span></span>
1. <span data-ttu-id="e49df-128">Dalyje **Profilio ypatybės** ypatybės **Pagrindinis medijos serverio URL** reikšmę pakeiskite savo anksčiau sukurtu pagrindiniu medijos URL.</span><span class="sxs-lookup"><span data-stu-id="e49df-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="e49df-129">Pasirinkite kanalą pavadinimu **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="e49df-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="e49df-130">Dalyje **Profilio ypatybės** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="e49df-131">Kaip įtrauktos ypatybės raktą pasirinkite **Pagrindinis medijos serverio URL**.</span><span class="sxs-lookup"><span data-stu-id="e49df-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="e49df-132">Kaip ypatybės reikšmę įveskite savo anksčiau sukurtą pagrindinį medijos URL.</span><span class="sxs-lookup"><span data-stu-id="e49df-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="e49df-133">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="e49df-134">Konfigūruokite ir testuokite elektroninio pašto serverį</span><span class="sxs-lookup"><span data-stu-id="e49df-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="e49df-135">SMTP serveris arba el. pašto paslauga, kuriuos čia įvedate, turi būti pasiekiami „Azure“ prenumeratoje, kurią naudojate aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="e49df-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="e49df-136">Prisijunkite prie komercijos būstinės.</span><span class="sxs-lookup"><span data-stu-id="e49df-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e49df-137">Naudokite meniu kairėje ir eikite į **Moduliai \> Mažmena ir komercija \> Būstinės sąranka \> Parametrai \> Elektroninio pašto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e49df-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="e49df-138">Skirtuko **SMTP parametrai** lauke **Siunčiamo pašto serveris** įveskite savo SMTP serverio ar el. pašto tarnybos FQDN arba IP adresą.</span><span class="sxs-lookup"><span data-stu-id="e49df-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="e49df-139">Lauke **SMTP prievado numeris** įveskite prievado numerį.</span><span class="sxs-lookup"><span data-stu-id="e49df-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="e49df-140">(Jei nenaudojate saugiųjų jungčių lygmens \[SSL\], numatytasis prievado numeris yra **25**.)</span><span class="sxs-lookup"><span data-stu-id="e49df-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="e49df-141">Jei reikalingas autentifikavimas, įveskite reikšmes laukuose **Vartotojo vardas** ir **Slaptažodis**.</span><span class="sxs-lookup"><span data-stu-id="e49df-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="e49df-142">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-142">Select **Save**.</span></span>
1. <span data-ttu-id="e49df-143">Pasirinkite **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="e49df-144">Skirtuko **Bandomasis el. laiškas** lauke **El. pašto teikėjas** pasirinkite **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="e49df-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="e49df-145">Lauke **Gavėjas** įveskite el. pašto adresą, kuriuo bandomasis el. laiškas turi būti pristatytas.</span><span class="sxs-lookup"><span data-stu-id="e49df-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="e49df-146">Pasirinkite **Išsiųsti bandomąjį el. laišką**.</span><span class="sxs-lookup"><span data-stu-id="e49df-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="e49df-147">El. laiškų šablonų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e49df-147">Configure email templates</span></span>

<span data-ttu-id="e49df-148">Kiekvieno operacinio įvykio, dėl kurio norite siųsti el. laiškus, el. laiškų šabloną turite atnaujinti galiojančiu siuntėjo el. pašto adresu.</span><span class="sxs-lookup"><span data-stu-id="e49df-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="e49df-149">Prisijunkite prie komercijos būstinės.</span><span class="sxs-lookup"><span data-stu-id="e49df-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e49df-150">Naudokite meniu kairėje ir eikite į **Moduliai \> Mažmena ir komercija \> Būstinės sąranka \> Parametrai \> Organizaciniai elektroninio pašto šablonai**.</span><span class="sxs-lookup"><span data-stu-id="e49df-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="e49df-151">Pasirinkite **Rodyti sąrašą**.</span><span class="sxs-lookup"><span data-stu-id="e49df-151">Select **Show list**.</span></span>
1. <span data-ttu-id="e49df-152">Su kiekvienu sąraše esančiu šablonu atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e49df-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="e49df-153">Lauke **Siuntėjo el. paštas** įveskite siuntėjo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="e49df-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="e49df-154">Nebūtina: lauke **Siuntėjo vardas** įveskite vardą, kuris turi būti naudojamas kaip siuntėjo vardas.</span><span class="sxs-lookup"><span data-stu-id="e49df-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="e49df-155">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="e49df-156">El. laiškų šablonų tinkinimas</span><span class="sxs-lookup"><span data-stu-id="e49df-156">Customize email templates</span></span>

<span data-ttu-id="e49df-157">Galbūt norėsite el. laiškų šablonus tinkinti, kad juose būtų naudojami skirtingi vaizdai.</span><span class="sxs-lookup"><span data-stu-id="e49df-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="e49df-158">Arba jums reikėtų atnaujinti nuorodas į šablonus tam, kad jie galėtų patekti į jūsų vertinimo aplinką.</span><span class="sxs-lookup"><span data-stu-id="e49df-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="e49df-159">Šia procedūra paaiškinama, kaip atsisiųsti numatytuosius šablonus, juos tinkinti ir atnaujinti sistemos šablonus.</span><span class="sxs-lookup"><span data-stu-id="e49df-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="e49df-160">Tinklo naršyklėje atsisiųskite [„Microsoft Dynamics 365 Commerce“ vertinimo numatytųjų el. pašto šablonų archyvuotą failą](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) į savo vietos kompiuterį.</span><span class="sxs-lookup"><span data-stu-id="e49df-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="e49df-161">Šiame faile yra tolesni HTML dokumentai.</span><span class="sxs-lookup"><span data-stu-id="e49df-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="e49df-162">Užsakymo patvirtinimo šablonas</span><span class="sxs-lookup"><span data-stu-id="e49df-162">Order confirmation template</span></span>
    - <span data-ttu-id="e49df-163">Dovanų kortelės išdavimo šablonas</span><span class="sxs-lookup"><span data-stu-id="e49df-163">Issue gift card template</span></span>
    - <span data-ttu-id="e49df-164">Naujo užsakymo šablonas</span><span class="sxs-lookup"><span data-stu-id="e49df-164">New order template</span></span>
    - <span data-ttu-id="e49df-165">Paketo užsakymo šablonas</span><span class="sxs-lookup"><span data-stu-id="e49df-165">Pack order template</span></span>
    - <span data-ttu-id="e49df-166">Paėmimo užsakymo šablonas</span><span class="sxs-lookup"><span data-stu-id="e49df-166">Pick order template</span></span>

1. <span data-ttu-id="e49df-167">Tinkinkite šablonus naudodami teksto arba HTML rengyklę.</span><span class="sxs-lookup"><span data-stu-id="e49df-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="e49df-168">[Palaikomų atpažinimo ženklų](#supported-tokens-in-the-email-template) sąrašą rasite tolesnėje šios temos dalyje.</span><span class="sxs-lookup"><span data-stu-id="e49df-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="e49df-169">Prisijunkite prie „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e49df-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="e49df-170">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Organizacijos administravimas \> Sąranka \> Organizacijos el. laiškų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="e49df-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="e49df-171">Išskleiskite sąrašą kairėje, kad pamatytumėte visus šablonus.</span><span class="sxs-lookup"><span data-stu-id="e49df-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="e49df-172">Su kiekvienu norimu tinkinti šablonu atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e49df-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="e49df-173">Pasirinkite šabloną sąraše.</span><span class="sxs-lookup"><span data-stu-id="e49df-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="e49df-174">Dalyje **El. laiško turinys** iš sąrašo pasirinkite tinkamą kalbos versiją.</span><span class="sxs-lookup"><span data-stu-id="e49df-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="e49df-175">(Numatytoji kalba yra **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="e49df-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="e49df-176">Dalyje **El. laiško turinys** pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="e49df-177">Atsiranda sritis **Nusiųsti el. laiškų šabloną**.</span><span class="sxs-lookup"><span data-stu-id="e49df-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="e49df-178">Pasirinkite **Naršyti** ir suraskite HTML failą, kuriame yra tinkintas turinys.</span><span class="sxs-lookup"><span data-stu-id="e49df-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="e49df-179">Pasirinkite **Nusiųsti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-179">Select **Upload**.</span></span> <span data-ttu-id="e49df-180">Šablonas nusiunčiamas į sistemą ir rodoma peržiūra.</span><span class="sxs-lookup"><span data-stu-id="e49df-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="e49df-181">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e49df-181">Select **OK**.</span></span>
    1. <span data-ttu-id="e49df-182">Nebūtina: tinkinkite šablono ypatybę **Tema**.</span><span class="sxs-lookup"><span data-stu-id="e49df-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="e49df-183">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e49df-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="e49df-184">Palaikomi el. laiškų šablono atpažinimo ženklai</span><span class="sxs-lookup"><span data-stu-id="e49df-184">Supported tokens in the email template</span></span>

<span data-ttu-id="e49df-185">Generuojant el. laišką šie atpažinimo ženklai pakeičiami faktinėmis reikšmėmis, kurios taikomos klientui ir jo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="e49df-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="e49df-186">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="e49df-186">Sales order</span></span>

<span data-ttu-id="e49df-187">Toliau nurodyti atpažinimo ženklai taikomi bendram pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="e49df-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="e49df-188">Atpažinimo ženklo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="e49df-188">Name of the token</span></span> | <span data-ttu-id="e49df-189">Atpažinimo ženklas</span><span class="sxs-lookup"><span data-stu-id="e49df-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="e49df-190">Užsakymo numeris</span><span class="sxs-lookup"><span data-stu-id="e49df-190">Order number</span></span>      | <span data-ttu-id="e49df-191">„%salesid%“</span><span class="sxs-lookup"><span data-stu-id="e49df-191">%salesid%</span></span> |
| <span data-ttu-id="e49df-192">Kliento pavadinimas</span><span class="sxs-lookup"><span data-stu-id="e49df-192">Customer's name</span></span>   | <span data-ttu-id="e49df-193">„%customername%“</span><span class="sxs-lookup"><span data-stu-id="e49df-193">%customername%</span></span> |
| <span data-ttu-id="e49df-194">Pristatymo adresas</span><span class="sxs-lookup"><span data-stu-id="e49df-194">Delivery address</span></span>  | <span data-ttu-id="e49df-195">„%deliveryaddress%“</span><span class="sxs-lookup"><span data-stu-id="e49df-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="e49df-196">Sąskaitų siuntimo adresas</span><span class="sxs-lookup"><span data-stu-id="e49df-196">Billing address</span></span>   | <span data-ttu-id="e49df-197">„%customeraddress%“</span><span class="sxs-lookup"><span data-stu-id="e49df-197">%customeraddress%</span></span> |
| <span data-ttu-id="e49df-198">Užsakymo data</span><span class="sxs-lookup"><span data-stu-id="e49df-198">Order date</span></span>        | <span data-ttu-id="e49df-199">„%shipdate%“</span><span class="sxs-lookup"><span data-stu-id="e49df-199">%shipdate%</span></span> |
| <span data-ttu-id="e49df-200">Pristatymo režimas</span><span class="sxs-lookup"><span data-stu-id="e49df-200">Delivery mode</span></span>     | <span data-ttu-id="e49df-201">„%modeofdelivery%“</span><span class="sxs-lookup"><span data-stu-id="e49df-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="e49df-202">Nuolaida</span><span class="sxs-lookup"><span data-stu-id="e49df-202">Discount</span></span>          | <span data-ttu-id="e49df-203">„%discount%“</span><span class="sxs-lookup"><span data-stu-id="e49df-203">%discount%</span></span> |
| <span data-ttu-id="e49df-204">PVM</span><span class="sxs-lookup"><span data-stu-id="e49df-204">Sales tax</span></span>         | <span data-ttu-id="e49df-205">„%tax%“</span><span class="sxs-lookup"><span data-stu-id="e49df-205">%tax%</span></span> |
| <span data-ttu-id="e49df-206">Užsakymo suma</span><span class="sxs-lookup"><span data-stu-id="e49df-206">Order total</span></span>       | <span data-ttu-id="e49df-207">„%total%“</span><span class="sxs-lookup"><span data-stu-id="e49df-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="e49df-208">Pardavimo eilutė</span><span class="sxs-lookup"><span data-stu-id="e49df-208">Sales line</span></span>

<span data-ttu-id="e49df-209">Tolesni atpažinimo ženklai pakeičiami kiekvieno užsakymo produkto reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="e49df-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="e49df-210">Atpažinimo ženklą **Produktų sąrašas – pradžia** įdėkite HTML bloko, kuris kartojamas su kiekvienu produktu, pradžioje, o atpažinimo ženklą **Produktų sąrašas – pabaiga** įdėkite bloko pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="e49df-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="e49df-211">Atpažinimo ženklo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="e49df-211">Name of the token</span></span>      | <span data-ttu-id="e49df-212">Atpažinimo ženklas</span><span class="sxs-lookup"><span data-stu-id="e49df-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="e49df-213">Produktų sąrašas – pradžia</span><span class="sxs-lookup"><span data-stu-id="e49df-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="e49df-214">Produktų sąrašas – pabaiga</span><span class="sxs-lookup"><span data-stu-id="e49df-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="e49df-215">Produkto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="e49df-215">Product name</span></span>           | <span data-ttu-id="e49df-216">„%lineproductname%“</span><span class="sxs-lookup"><span data-stu-id="e49df-216">%lineproductname%</span></span> |
| <span data-ttu-id="e49df-217">aprašymas</span><span class="sxs-lookup"><span data-stu-id="e49df-217">Description</span></span>            | <span data-ttu-id="e49df-218">„%lineproductdescription%“</span><span class="sxs-lookup"><span data-stu-id="e49df-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="e49df-219">Kiekis</span><span class="sxs-lookup"><span data-stu-id="e49df-219">Quantity</span></span>               | <span data-ttu-id="e49df-220">„%linequantity%“</span><span class="sxs-lookup"><span data-stu-id="e49df-220">%linequantity%</span></span> |
| <span data-ttu-id="e49df-221">Eilutės vieneto kaina</span><span class="sxs-lookup"><span data-stu-id="e49df-221">Line unit price</span></span>        | <span data-ttu-id="e49df-222">%lineprice% (patikrinti)</span><span class="sxs-lookup"><span data-stu-id="e49df-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="e49df-223">Iš viso eilutės elementų</span><span class="sxs-lookup"><span data-stu-id="e49df-223">line item total</span></span>        | <span data-ttu-id="e49df-224">„%linenetamount%“</span><span class="sxs-lookup"><span data-stu-id="e49df-224">%linenetamount%</span></span> |
| <span data-ttu-id="e49df-225">eilutės nuolaida</span><span class="sxs-lookup"><span data-stu-id="e49df-225">line discount</span></span>          | <span data-ttu-id="e49df-226">„%linediscount%“</span><span class="sxs-lookup"><span data-stu-id="e49df-226">%linediscount%</span></span> |
| <span data-ttu-id="e49df-227">Siuntimo data</span><span class="sxs-lookup"><span data-stu-id="e49df-227">Ship date</span></span>              | <span data-ttu-id="e49df-228">„%lineshipdate%“</span><span class="sxs-lookup"><span data-stu-id="e49df-228">%lineshipdate%</span></span> |
| <span data-ttu-id="e49df-229">Įsigijimo metodas</span><span class="sxs-lookup"><span data-stu-id="e49df-229">Procurement method</span></span>     | <span data-ttu-id="e49df-230">„%linedeliverymode%“</span><span class="sxs-lookup"><span data-stu-id="e49df-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="e49df-231">pristatymo adresas</span><span class="sxs-lookup"><span data-stu-id="e49df-231">delivery address</span></span>       | <span data-ttu-id="e49df-232">„%linedeliveryaddress%“</span><span class="sxs-lookup"><span data-stu-id="e49df-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="e49df-233">Eilutės pardavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="e49df-233">Sales unit of the line</span></span> | <span data-ttu-id="e49df-234">„%lineunit%“</span><span class="sxs-lookup"><span data-stu-id="e49df-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="e49df-235">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e49df-235">Additional resources</span></span>

[<span data-ttu-id="e49df-236">„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra</span><span class="sxs-lookup"><span data-stu-id="e49df-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="e49df-237">Parenkite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="e49df-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="e49df-238">Sukonfigūruokite „Dynamics 365 Commerce“ vertinimo aplinką</span><span class="sxs-lookup"><span data-stu-id="e49df-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e49df-239">Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje</span><span class="sxs-lookup"><span data-stu-id="e49df-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="e49df-240">„Dynamics 365 Commerce“ vertinimo aplinkos DUK</span><span class="sxs-lookup"><span data-stu-id="e49df-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="e49df-241">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="e49df-241">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="e49df-242">„Retail Cloud Scale Unit“ (RCSU)</span><span class="sxs-lookup"><span data-stu-id="e49df-242">Retail Cloud Scale Unit (RCSU)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="e49df-243">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="e49df-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="e49df-244">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="e49df-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]