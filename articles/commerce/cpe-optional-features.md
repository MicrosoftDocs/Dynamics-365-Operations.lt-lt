---
title: Pasirinktinių „Dynamics 365 Commerce” peržiūros aplinkos funkcijų konfigūravimas
description: Šioje temoje paaiškinama, kaip sukonfigūruoti pasirenkamas „Microsoft Dynamics 365 Commerce“ peržiūros aplinkos funkcijas.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024734"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="7cc97-103">Pasirinktinių „Dynamics 365 Commerce” peržiūros aplinkos funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7cc97-104">Šioje temoje paaiškinama, kaip sukonfigūruoti pasirenkamas „Microsoft Dynamics 365 Commerce“ peržiūros aplinkos funkcijas.</span><span class="sxs-lookup"><span data-stu-id="7cc97-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7cc97-105">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="7cc97-105">Prerequisites</span></span>

<span data-ttu-id="7cc97-106">Jei norite įvertinti operacines el. pašto funkcijas, turi būti įvykdytos šios būtinosios sąlygos:</span><span class="sxs-lookup"><span data-stu-id="7cc97-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="7cc97-107">Turite pasiekiamą el. pašto serverį (paprastųjų pašto siuntų protokolo \[SMTP\] serverį), kuris gali būti naudojamas iš „Microsoft Azure“ prenumeratos, kurioje sukonfigūravote peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="7cc97-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="7cc97-108">Turite pasiekiamus serverio visiškai apibrėžtą domeno vardą (FQDN) / IP adresą, SMTP prievado numerį ir autentifikavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="7cc97-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="7cc97-109">Jei norite įvertinti skaitmeninių išteklių valdymo funkcijas tiesiogiai naudodami daugiakanalės platformos vaizdus, turite turėti savo turinio valdymo sistemos (TVS) nuomotojo vardą.</span><span class="sxs-lookup"><span data-stu-id="7cc97-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="7cc97-110">Nurodymai, kaip rasti šį vardą, pateikiami toliau šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="7cc97-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="7cc97-111">>>>(K: kur yra nurodymai?)</span><span class="sxs-lookup"><span data-stu-id="7cc97-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="7cc97-112">Vaizdų posistemio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="7cc97-113">Pagrindinio medijos URL radimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="7cc97-114">Kad galėtumėte atlikti šią procedūrą, turite atlikti dalyje [Svetainės nustatymas programoje „Commerce“](cpe-post-provisioning.md#set-up-your-site-in-commerce) nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7cc97-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="7cc97-115">Prisijunkite prie „Commerce“ svetainių valdymo įrankio naudodami URL, kurį pasižymėjote inicijuodami el. prekybą jos konfigūravimo metu (žr. [El. prekybos inicijavimas](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="7cc97-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="7cc97-116">Atidarykite **„Fabrikam“** svetainę.</span><span class="sxs-lookup"><span data-stu-id="7cc97-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="7cc97-117">Kairėje esančiame meniu pasirinkite **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="7cc97-118">Pasirinkite bet kurį vieną vaizdo išteklių.</span><span class="sxs-lookup"><span data-stu-id="7cc97-118">Select any single image asset.</span></span>
1. <span data-ttu-id="7cc97-119">Dešinėje esančiame ypatybių inspektoriuje suraskite ypatybę **Viešasis URL**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="7cc97-120">Jos reikšmė yra URL.</span><span class="sxs-lookup"><span data-stu-id="7cc97-120">The value is a URL.</span></span> <span data-ttu-id="7cc97-121">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7cc97-121">Here is an example:</span></span>

    <span data-ttu-id="7cc97-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="7cc97-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="7cc97-123">Paskutinį URL identifikatorių (pirmiau pateiktame pavyzdyje – **MA1nQC**) pakeiskite eilute **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="7cc97-124">Toliau parodyta, kaip atrodo taip pakeistas URL pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7cc97-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="7cc97-125">Šis URL yra jūsų pagrindinis medijos URL.</span><span class="sxs-lookup"><span data-stu-id="7cc97-125">This URL is your media base URL.</span></span> <span data-ttu-id="7cc97-126">Jį pasižymėkite.</span><span class="sxs-lookup"><span data-stu-id="7cc97-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="7cc97-127">Pagrindinio medijos URL naujinimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-127">Update the media base URL</span></span>

1. <span data-ttu-id="7cc97-128">Prisijunkite prie „Dynamics 365 Retail“.</span><span class="sxs-lookup"><span data-stu-id="7cc97-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="7cc97-129">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> „Retail“ \> Kanalo sąranka \> Kanalo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="7cc97-130">Pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-130">Select **Edit**.</span></span>
1. <span data-ttu-id="7cc97-131">Dalyje **Profilio ypatybės** ypatybės **Pagrindinis medijos serverio URL** reikšmę pakeiskite savo anksčiau sukurtu pagrindiniu medijos URL.</span><span class="sxs-lookup"><span data-stu-id="7cc97-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="7cc97-132">Kairėje esančiame sąraše prie kanalo **Numatytasis** pasirinkite kitą kanalą.</span><span class="sxs-lookup"><span data-stu-id="7cc97-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="7cc97-133">Dalyje **Profilio ypatybės** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="7cc97-134">Kaip įtrauktos ypatybės raktą pasirinkite **Pagrindinis medijos serverio URL**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="7cc97-135">Kaip ypatybės reikšmę įveskite savo anksčiau sukurtą pagrindinį medijos URL.</span><span class="sxs-lookup"><span data-stu-id="7cc97-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="7cc97-136">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="7cc97-137">El. pašto serverio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="7cc97-138">SMTP serveris arba el. pašto paslauga, kuriuos čia įvedate, turi būti pasiekiami „Azure“ prenumeratoje, kurią naudojate aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="7cc97-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="7cc97-139">Prisijunkite prie „Retail“.</span><span class="sxs-lookup"><span data-stu-id="7cc97-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="7cc97-140">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Sistemos administravimas \> Sąranka \> El. paštas \> El. pašto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="7cc97-141">Skirtuko **SMTP parametrai** lauke **Siunčiamo pašto serveris** įveskite savo SMTP serverio ar el. pašto tarnybos FQDN arba IP adresą.</span><span class="sxs-lookup"><span data-stu-id="7cc97-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="7cc97-142">Lauke **SMTP prievado numeris** įveskite prievado numerį.</span><span class="sxs-lookup"><span data-stu-id="7cc97-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="7cc97-143">(Jei nenaudojate saugiųjų jungčių lygmens \[SSL\], numatytasis prievado numeris yra **25**.)</span><span class="sxs-lookup"><span data-stu-id="7cc97-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="7cc97-144">Jei reikalinga autentifikacija, įveskite reikšmes laukuose **Vartotojo vardas** ir **Slaptažodis**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="7cc97-145">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-145">Select **Save**.</span></span>
1. <span data-ttu-id="7cc97-146">Pasirinkite **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="7cc97-147">Skirtuko **Bandomasis el. laiškas** lauke **El. pašto teikėjas** pasirinkite **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="7cc97-148">Lauke **Gavėjas** įveskite el. pašto adresą, kuriuo bandomasis el. laiškas turi būti pristatytas.</span><span class="sxs-lookup"><span data-stu-id="7cc97-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="7cc97-149">Pasirinkite **Išsiųsti bandomąjį el. laišką**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="7cc97-150">El. laiškų šablonų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-150">Configure email templates</span></span>

<span data-ttu-id="7cc97-151">Kiekvieno operacinio įvykio, dėl kurio norite siųsti el. laiškus, el. laiškų šabloną turite atnaujinti galiojančiu siuntėjo el. pašto adresu.</span><span class="sxs-lookup"><span data-stu-id="7cc97-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="7cc97-152">Prisijunkite prie „Retail“.</span><span class="sxs-lookup"><span data-stu-id="7cc97-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="7cc97-153">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Organizacijos administravimas \> Sąranka \> Organizacijos el. laiškų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7cc97-154">Pasirinkite **Rodyti sąrašą**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-154">Select **Show list**.</span></span>
1. <span data-ttu-id="7cc97-155">Su kiekvienu sąraše esančiu šablonu atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7cc97-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="7cc97-156">Lauke **Siuntėjo el. paštas** įveskite siuntėjo el. pašto adresą.</span><span class="sxs-lookup"><span data-stu-id="7cc97-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="7cc97-157">Nebūtina: lauke **Siuntėjo vardas** įveskite vardą, kuris turi būti naudojamas kaip siuntėjo vardas.</span><span class="sxs-lookup"><span data-stu-id="7cc97-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="7cc97-158">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="7cc97-159">El. laiškų šablonų tinkinimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-159">Customize email templates</span></span>

<span data-ttu-id="7cc97-160">Galbūt norėsite el. laiškų šablonus tinkinti, kad juose būtų naudojami skirtingi vaizdai.</span><span class="sxs-lookup"><span data-stu-id="7cc97-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="7cc97-161">Arba galbūt norėsite atnaujinti šablonų saitus, kad jų paskirties vieta būtų jūsų peržiūros aplinka.</span><span class="sxs-lookup"><span data-stu-id="7cc97-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="7cc97-162">Šia procedūra paaiškinama, kaip atsisiųsti numatytuosius šablonus, juos tinkinti ir atnaujinti sistemos šablonus.</span><span class="sxs-lookup"><span data-stu-id="7cc97-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="7cc97-163">Naudodami žiniatinklio naršyklę, į vietinį kompiuterį atsisiųskite [„Microsoft Dynamics 365 Commerce“ peržiūros numatytųjų el. laiškų šablonų ZIP failą](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip).</span><span class="sxs-lookup"><span data-stu-id="7cc97-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="7cc97-164">Šiame faile yra tolesni HTML dokumentai.</span><span class="sxs-lookup"><span data-stu-id="7cc97-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="7cc97-165">Užsakymo patvirtinimo šablonas</span><span class="sxs-lookup"><span data-stu-id="7cc97-165">Order confirmation template</span></span>
    - <span data-ttu-id="7cc97-166">Dovanų kortelės išdavimo šablonas</span><span class="sxs-lookup"><span data-stu-id="7cc97-166">Issue gift card template</span></span>
    - <span data-ttu-id="7cc97-167">Naujo užsakymo šablonas</span><span class="sxs-lookup"><span data-stu-id="7cc97-167">New order template</span></span>
    - <span data-ttu-id="7cc97-168">Paketo užsakymo šablonas</span><span class="sxs-lookup"><span data-stu-id="7cc97-168">Pack order template</span></span>
    - <span data-ttu-id="7cc97-169">Paėmimo užsakymo šablonas</span><span class="sxs-lookup"><span data-stu-id="7cc97-169">Pick order template</span></span>

1. <span data-ttu-id="7cc97-170">Tinkinkite šablonus naudodami teksto arba HTML rengyklę.</span><span class="sxs-lookup"><span data-stu-id="7cc97-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="7cc97-171">[Palaikomų atpažinimo ženklų](#supported-tokens-in-the-email-template) sąrašą rasite tolesnėje šios temos dalyje.</span><span class="sxs-lookup"><span data-stu-id="7cc97-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="7cc97-172">Prisijunkite prie „Retail“.</span><span class="sxs-lookup"><span data-stu-id="7cc97-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="7cc97-173">Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Organizacijos administravimas \> Sąranka \> Organizacijos el. laiškų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7cc97-174">Išskleiskite sąrašą kairėje, kad pamatytumėte visus šablonus.</span><span class="sxs-lookup"><span data-stu-id="7cc97-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="7cc97-175">Su kiekvienu norimu tinkinti šablonu atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7cc97-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="7cc97-176">Pasirinkite šabloną sąraše.</span><span class="sxs-lookup"><span data-stu-id="7cc97-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="7cc97-177">Dalyje **El. laiško turinys** iš sąrašo pasirinkite tinkamą kalbos versiją.</span><span class="sxs-lookup"><span data-stu-id="7cc97-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="7cc97-178">(Numatytoji kalba yra **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="7cc97-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="7cc97-179">Dalyje **El. laiško turinys** pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="7cc97-180">Atsiranda sritis **Nusiųsti el. laiškų šabloną**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="7cc97-181">Pasirinkite **Naršyti** ir suraskite HTML failą, kuriame yra tinkintas turinys.</span><span class="sxs-lookup"><span data-stu-id="7cc97-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="7cc97-182">Pasirinkite **Nusiųsti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-182">Select **Upload**.</span></span> <span data-ttu-id="7cc97-183">Šablonas nusiunčiamas į sistemą ir rodoma peržiūra.</span><span class="sxs-lookup"><span data-stu-id="7cc97-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="7cc97-184">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-184">Select **OK**.</span></span>
    1. <span data-ttu-id="7cc97-185">Nebūtina: tinkinkite šablono ypatybę **Tema**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="7cc97-186">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7cc97-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="7cc97-187">Palaikomi el. laiškų šablono atpažinimo ženklai</span><span class="sxs-lookup"><span data-stu-id="7cc97-187">Supported tokens in the email template</span></span>

<span data-ttu-id="7cc97-188">Generuojant el. laišką šie atpažinimo ženklai pakeičiami faktinėmis reikšmėmis, kurios taikomos klientui ir jo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="7cc97-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="7cc97-189">Pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="7cc97-189">Sales order</span></span>

<span data-ttu-id="7cc97-190">Toliau nurodyti atpažinimo ženklai taikomi bendram pardavimo užsakymui.</span><span class="sxs-lookup"><span data-stu-id="7cc97-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="7cc97-191">Atpažinimo ženklo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-191">Name of the token</span></span> | <span data-ttu-id="7cc97-192">Atpažinimo ženklas</span><span class="sxs-lookup"><span data-stu-id="7cc97-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="7cc97-193">Užsakymo numeris</span><span class="sxs-lookup"><span data-stu-id="7cc97-193">Order number</span></span>      | <span data-ttu-id="7cc97-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="7cc97-194">%salesid%</span></span> |
| <span data-ttu-id="7cc97-195">Kliento pavadinimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-195">Customer's name</span></span>   | <span data-ttu-id="7cc97-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="7cc97-196">%customername%</span></span> |
| <span data-ttu-id="7cc97-197">Pristatymo adresas</span><span class="sxs-lookup"><span data-stu-id="7cc97-197">Delivery address</span></span>  | <span data-ttu-id="7cc97-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="7cc97-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="7cc97-199">Sąskaitų siuntimo adresas</span><span class="sxs-lookup"><span data-stu-id="7cc97-199">Billing address</span></span>   | <span data-ttu-id="7cc97-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="7cc97-200">%customeraddress%</span></span> |
| <span data-ttu-id="7cc97-201">Užsakymo data</span><span class="sxs-lookup"><span data-stu-id="7cc97-201">Order date</span></span>        | <span data-ttu-id="7cc97-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="7cc97-202">%shipdate%</span></span> |
| <span data-ttu-id="7cc97-203">Pristatymo režimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-203">Delivery mode</span></span>     | <span data-ttu-id="7cc97-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="7cc97-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="7cc97-205">Nuolaida</span><span class="sxs-lookup"><span data-stu-id="7cc97-205">Discount</span></span>          | <span data-ttu-id="7cc97-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="7cc97-206">%discount%</span></span> |
| <span data-ttu-id="7cc97-207">PVM</span><span class="sxs-lookup"><span data-stu-id="7cc97-207">Sales tax</span></span>         | <span data-ttu-id="7cc97-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="7cc97-208">%tax%</span></span> |
| <span data-ttu-id="7cc97-209">Užsakymo suma</span><span class="sxs-lookup"><span data-stu-id="7cc97-209">Order total</span></span>       | <span data-ttu-id="7cc97-210">%total%</span><span class="sxs-lookup"><span data-stu-id="7cc97-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="7cc97-211">Pardavimo eilutė</span><span class="sxs-lookup"><span data-stu-id="7cc97-211">Sales line</span></span>

<span data-ttu-id="7cc97-212">Tolesni atpažinimo ženklai pakeičiami kiekvieno užsakymo produkto reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="7cc97-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="7cc97-213">Atpažinimo ženklą **Produktų sąrašas – pradžia** įdėkite HTML bloko, kuris kartojamas su kiekvienu produktu, pradžioje, o atpažinimo ženklą **Produktų sąrašas – pabaiga** įdėkite bloko pabaigoje.</span><span class="sxs-lookup"><span data-stu-id="7cc97-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="7cc97-214">Atpažinimo ženklo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-214">Name of the token</span></span>      | <span data-ttu-id="7cc97-215">Atpažinimo ženklas</span><span class="sxs-lookup"><span data-stu-id="7cc97-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="7cc97-216">Produktų sąrašas – pradžia</span><span class="sxs-lookup"><span data-stu-id="7cc97-216">Product list - start</span></span>   | <span data-ttu-id="7cc97-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="7cc97-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="7cc97-218">Produktų sąrašas – pabaiga</span><span class="sxs-lookup"><span data-stu-id="7cc97-218">Product list - end</span></span>     | <span data-ttu-id="7cc97-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="7cc97-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="7cc97-220">Produkto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-220">Product name</span></span>           | <span data-ttu-id="7cc97-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="7cc97-221">%lineproductname%</span></span> |
| <span data-ttu-id="7cc97-222">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="7cc97-222">Description</span></span>            | <span data-ttu-id="7cc97-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="7cc97-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="7cc97-224">Kiekis</span><span class="sxs-lookup"><span data-stu-id="7cc97-224">Quantity</span></span>               | <span data-ttu-id="7cc97-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="7cc97-225">%linequantity%</span></span> |
| <span data-ttu-id="7cc97-226">Eilutės vieneto kaina</span><span class="sxs-lookup"><span data-stu-id="7cc97-226">Line unit price</span></span>        | <span data-ttu-id="7cc97-227">%lineprice% (tikrinti)</span><span class="sxs-lookup"><span data-stu-id="7cc97-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="7cc97-228">Iš viso eilutės elementų</span><span class="sxs-lookup"><span data-stu-id="7cc97-228">line item total</span></span>        | <span data-ttu-id="7cc97-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="7cc97-229">%linenetamount%</span></span> |
| <span data-ttu-id="7cc97-230">eilutės nuolaida</span><span class="sxs-lookup"><span data-stu-id="7cc97-230">line discount</span></span>          | <span data-ttu-id="7cc97-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="7cc97-231">%linediscount%</span></span> |
| <span data-ttu-id="7cc97-232">Siuntimo data</span><span class="sxs-lookup"><span data-stu-id="7cc97-232">Ship date</span></span>              | <span data-ttu-id="7cc97-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="7cc97-233">%lineshipdate%</span></span> |
| <span data-ttu-id="7cc97-234">Įsigijimo metodas</span><span class="sxs-lookup"><span data-stu-id="7cc97-234">Procurement method</span></span>     | <span data-ttu-id="7cc97-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="7cc97-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="7cc97-236">pristatymo adresas</span><span class="sxs-lookup"><span data-stu-id="7cc97-236">delivery address</span></span>       | <span data-ttu-id="7cc97-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="7cc97-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="7cc97-238">Eilutės pardavimo vienetas</span><span class="sxs-lookup"><span data-stu-id="7cc97-238">Sales unit of the line</span></span> | <span data-ttu-id="7cc97-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="7cc97-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7cc97-240">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7cc97-240">Additional resources</span></span>

[<span data-ttu-id="7cc97-241">„Dynamics 365 Commerce“ peržiūros aplinkos apžvalga</span><span class="sxs-lookup"><span data-stu-id="7cc97-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="7cc97-242">„Dynamics 365 Commerce“ peržiūros aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="7cc97-243">„Dynamics 365 Commerce“ peržiūros aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7cc97-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="7cc97-244">DUK apie „Dynamics 365 Commerce“ peržiūros aplinką</span><span class="sxs-lookup"><span data-stu-id="7cc97-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="7cc97-245">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="7cc97-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="7cc97-246">„Retail Cloud Scale Unit“ (RCSU)</span><span class="sxs-lookup"><span data-stu-id="7cc97-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="7cc97-247">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="7cc97-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="7cc97-248">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="7cc97-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
