---
title: „Commerce“ peržiūros aplinkos parengimas
description: Šioje temoje paaiškinama, kaip parengti „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934753"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="21de4-103">„Commerce“ peržiūros aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="21de4-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="21de4-104">Šioje temoje paaiškinama, kaip parengti „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="21de4-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="21de4-105">Prieš pradedant rekomenduojame bent peržvelgti visą šią temą, kad suprastumėte, koks tai procesas ir kas aprašoma šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="21de4-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="21de4-106">Jei dar negavote prieigos prie „Dynamics 365 Commerce“ peržiūros, galite prašyti prieigos prie peržiūros [„Commerce“ svetainėje](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="21de4-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="21de4-107">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="21de4-107">Overview</span></span>

<span data-ttu-id="21de4-108">Norėdami sėkmingai parengti savo „Commerce“ peržiūros aplinką, turite sukurti projektą, kuriame būtų konkretaus produkto pavadinimas ir tipas.</span><span class="sxs-lookup"><span data-stu-id="21de4-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="21de4-109">Aplinka ir „Retail Cloud Scale Unit“ (RCSU) taip pat turi tam tikrų konkrečių parametrų, kuriuos turite naudoti, vėliau parengdami „e-Commerce“.</span><span class="sxs-lookup"><span data-stu-id="21de4-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="21de4-110">Šios temos instrukcijose aprašomi visi būtini veiksmai, kuriuos turite atlikti, ir parametrai, kuriuos turite naudoti.</span><span class="sxs-lookup"><span data-stu-id="21de4-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="21de4-111">Sėkmingai parengę „Commerce“ peržiūros aplinką, turite atlikti keletą veiksmų po parengimo, kad ją paruoštumėte.</span><span class="sxs-lookup"><span data-stu-id="21de4-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="21de4-112">Kai kurie veiksmai yra pasirinktiniai, atsižvelgiant į tai, kokius sistemos aspektus norite įvertinti.</span><span class="sxs-lookup"><span data-stu-id="21de4-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="21de4-113">Visada galite atlikti pasirinktinius veiksmus vėliau.</span><span class="sxs-lookup"><span data-stu-id="21de4-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="21de4-114">Informacijos apie tai, kaip sukonfigūruoti „Commerce“ peržiūros aplinką po to, kai ją parengsite, rasite skyriuje [„Commerce“ peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="21de4-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="21de4-115">Informacijos apie tai, kaip sukonfigūruoti „Commerce“ peržiūros aplinkos pasirinktines funkcijas, rasite skyriuje [„Commerce“ peržiūros aplinkos pasirinktinių funkcijų konfigūravimas](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="21de4-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="21de4-116">Jei turite klausimų dėl parengimo veiksmų arba kyla problemų, praneškite apie tai „Microsoft“ [„Microsoft Dynamics 365 Commerce“ peržiūros „Yammer“ grupėje](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="21de4-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="21de4-117">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="21de4-117">Prerequisites</span></span>

<span data-ttu-id="21de4-118">Toliau pateikiamos būtinosios sąlygos turi būti įvykdytos prieš parengiant „Commerce“ peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="21de4-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="21de4-119">Turite prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS) portalo.</span><span class="sxs-lookup"><span data-stu-id="21de4-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="21de4-120">Buvote priimti į „Dynamics 365 Commerce“ peržiūros programą.</span><span class="sxs-lookup"><span data-stu-id="21de4-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="21de4-121">Turite reikiamas teises kurti **Galimi išankstiniai pardavimai** arba **Perkelti, kurti sprendimus ir sužinoti** projektą.</span><span class="sxs-lookup"><span data-stu-id="21de4-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="21de4-122">Esate vaidmens **Aplinkos administratorius** arba **Projekto savininkas** narys projekte, kuriame parengsite aplinką.</span><span class="sxs-lookup"><span data-stu-id="21de4-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="21de4-123">Turite administratoriaus prieigą prie savo „Microsoft Azure“ prenumeratos arba galite susisiekti su prenumeratos administratoriumi, kuris gali atlikti du veiksmus, reikalaujančius administratoriaus teisių, jūsų vardu.</span><span class="sxs-lookup"><span data-stu-id="21de4-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="21de4-124">Turite savo „Azure Active Directory“ („Azure AD“) nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="21de4-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="21de4-125">Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip „e-Commerce“ sistemos administratoriaus grupė, ir turite jos ID.</span><span class="sxs-lookup"><span data-stu-id="21de4-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="21de4-126">Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip įvertinimų ir apžvalgų moderatoriaus grupė, ir turite jos ID.</span><span class="sxs-lookup"><span data-stu-id="21de4-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="21de4-127">(Ši saugos grupė gali sutapti su „e-Commerce“ sistemos administravimo grupe.)</span><span class="sxs-lookup"><span data-stu-id="21de4-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="21de4-128">„Azure AD“ nuomotojo ID radimas</span><span class="sxs-lookup"><span data-stu-id="21de4-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="21de4-129">Jūsų „Azure AD“ nuomotojo ID yra visuotinai unikalų identifikatorius (GUID), panašus į šį pavyzdį: **„72f988bf-86f1-41af-91ab-2d7cd011db47“**.</span><span class="sxs-lookup"><span data-stu-id="21de4-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="21de4-130">„Azure AD“ nuomotojo ID radimas „Azure“ portale</span><span class="sxs-lookup"><span data-stu-id="21de4-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="21de4-131">Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="21de4-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="21de4-132">Įsitikinkite, kad pasirinktas tinkamas katalogas.</span><span class="sxs-lookup"><span data-stu-id="21de4-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="21de4-133">Kairėje esančiame meniu pasirinkite **„Azure Active Directory“**.</span><span class="sxs-lookup"><span data-stu-id="21de4-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="21de4-134">Dalyje **Valdyti** pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="21de4-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="21de4-135">„Azure AD“ nuomotojo ID rodomas dalyje **Katalogo ID**.</span><span class="sxs-lookup"><span data-stu-id="21de4-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="21de4-136">„Azure AD“ nuomotojo ID radimas naudojant OpenID „Connect“ metaduomenis</span><span class="sxs-lookup"><span data-stu-id="21de4-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="21de4-137">Sukurkite OpenID URL, pakeitę **\{YOUR\_DOMAIN\}** savo domenu, pvz., `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="21de4-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="21de4-138">Pavyzdžiui, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` taps `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="21de4-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="21de4-139">Eikite į OpenID URL, kuriame nurodytas jūsų domenas.</span><span class="sxs-lookup"><span data-stu-id="21de4-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="21de4-140">Savo „Azure AD“ nuomotojo ID rasite keliose ypatybių vertėse.</span><span class="sxs-lookup"><span data-stu-id="21de4-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="21de4-141">Raskite **authorization\_endpoint** ir išskleiskite GUID, rodomą iškart po `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="21de4-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="21de4-142">„Azure AD“ saugos grupės ID radimas</span><span class="sxs-lookup"><span data-stu-id="21de4-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="21de4-143">„Azure AD“ saugos grupės ID yra GUID, panašus į šį pavyzdį: **„436ea7f5-ee6c-40c1-9f08-825c5811066a“**.</span><span class="sxs-lookup"><span data-stu-id="21de4-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="21de4-144">Atliekant šią procedūrą laikoma, kad esate grupės, kurios ID bandote rasti, narys.</span><span class="sxs-lookup"><span data-stu-id="21de4-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="21de4-145">Atidarykite [„Graph“ naršyklę](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="21de4-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="21de4-146">Pasirinkite **Prisijungti naudojant „Microsoft“** ir prisijunkite, naudodami savo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="21de4-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="21de4-147">Kairėje pasirinkite **rodyti daugiau pavyzdžių**.</span><span class="sxs-lookup"><span data-stu-id="21de4-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="21de4-148">Dešiniojoje srityje įjunkite **Grupės**.</span><span class="sxs-lookup"><span data-stu-id="21de4-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="21de4-149">Uždarykite dešiniąją sritį.</span><span class="sxs-lookup"><span data-stu-id="21de4-149">Close the right pane.</span></span>
1. <span data-ttu-id="21de4-150">Pasirinkite **visos grupės, kurioms priklausau**.</span><span class="sxs-lookup"><span data-stu-id="21de4-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="21de4-151">Lauke **Atsakymo peržiūra** raskite savo grupę.</span><span class="sxs-lookup"><span data-stu-id="21de4-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="21de4-152">Saugos grupės ID rodomas po ypatybės **„id“**.</span><span class="sxs-lookup"><span data-stu-id="21de4-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="21de4-153">Jūsų „Commerce“ peržiūros aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="21de4-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="21de4-154">Šiose procedūrose paaiškinama, kaip parengti „Commerce“ peržiūros aplinką.</span><span class="sxs-lookup"><span data-stu-id="21de4-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="21de4-155">Sėkmingai jas atlikus, „Commerce“ peržiūros aplinka bus paruošta konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="21de4-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="21de4-156">Visos čia aprašytos veiklos vyksta LCS portale.</span><span class="sxs-lookup"><span data-stu-id="21de4-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21de4-157">Peržiūros prieiga yra susieta su LCS paskyra ir organizacija, kurią nurodėte prašyme dėl peržiūros.</span><span class="sxs-lookup"><span data-stu-id="21de4-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="21de4-158">Norėdami parengti „Commerce“ peržiūros aplinką, turite naudoti tą pačią paskyrą.</span><span class="sxs-lookup"><span data-stu-id="21de4-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="21de4-159">Jei „Commerce“ peržiūros aplinkoje tenka naudoti kitą LCS paskyrą arba nuomotoją, turite pateikti šiuos duomenis įmonei „Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="21de4-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="21de4-160">Kontaktinės informacijos ieškokite toliau šioje temoje, skyriuje [„Commerce“ peržiūros aplinkos palaikymas](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="21de4-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="21de4-161">Prieigos prie el. prekybos programų suteikimas</span><span class="sxs-lookup"><span data-stu-id="21de4-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21de4-162">Prisijungiantis asmuo turi būti „Azure AD“ nuomotojo administratorius, kuris turi „Azure AD“ nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="21de4-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="21de4-163">Jei šis veiksmas nebus sėkmingai atliktas, nepavyks atlikti kitų parengimo veiksmų.</span><span class="sxs-lookup"><span data-stu-id="21de4-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="21de4-164">Norėdami įgalioti „e-Commerce“ programas pasiekti „Azure“ prenumeratą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21de4-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="21de4-165">Sudėliokite URL toliau pateikiamu formatu.</span><span class="sxs-lookup"><span data-stu-id="21de4-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="21de4-166">Nukopijuokite ir įklijuokite URL į naršyklę arba teksto rengyklę ir pakeiskite **\{AAD\_TENANT\_ID\}** į savo „Azure AD“ nuomotojo ID.</span><span class="sxs-lookup"><span data-stu-id="21de4-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="21de4-167">Tuomet atidarykite URL.</span><span class="sxs-lookup"><span data-stu-id="21de4-167">Then open the URL.</span></span>
1. <span data-ttu-id="21de4-168">Prisijungimo prie „Azure AD“ dialogo lange prisijunkite ir patvirtinkite, kad **Dynamics 365 Commerce (Peržiūra)** norite suteikti prieigą prie prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="21de4-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="21de4-169">Pamatysite puslapį, kuriame nurodoma, ar operacija buvo sėkminga.</span><span class="sxs-lookup"><span data-stu-id="21de4-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="21de4-170">Patvirtinimas, kad peržiūros funkcijos prieinamos ir įjungtos LCS</span><span class="sxs-lookup"><span data-stu-id="21de4-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="21de4-171">Norėdami patvirtinti, kad peržiūros funkcijos yra prieinamos ir įjungtos LCS, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21de4-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="21de4-172">Prisijunkite prie [LCS portalo](https://lcs.dynamics.com), naudodami LCS paskyrą, kurią naudojote prašydami suteikti prieigą prie peržiūros.</span><span class="sxs-lookup"><span data-stu-id="21de4-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="21de4-173">LCS pagrindiniame puslapyje slinkite į dešinę iki pat galo ir pasirinkite plytelę **Peržiūros versijos funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="21de4-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Peržiūros versijos valdymo plytelė](./media/preview1.png)

1. <span data-ttu-id="21de4-175">Slinkite žemyn iki **Asmeninės peržiūros funkcijos** ir patvirtinkite, kad toliau pateikiamos funkcijos yra galimos ir įjungtos.</span><span class="sxs-lookup"><span data-stu-id="21de4-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="21de4-176">El. prekybos vertinimas</span><span class="sxs-lookup"><span data-stu-id="21de4-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="21de4-177">„Commerce“ peržiūros programos aplinkos</span><span class="sxs-lookup"><span data-stu-id="21de4-177">Commerce Preview Program Environments</span></span>

    ![Privačiosios vertinimo versijos funkcijos](./media/preview2.png)

1. <span data-ttu-id="21de4-179">Jei šios funkcijos sąraše nerodomos, susisiekite su „Microsoft“ ir pateikite savo darbo el. pašto adresą, LCS paskyrą ir nuomotojo informaciją.</span><span class="sxs-lookup"><span data-stu-id="21de4-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="21de4-180">Kontaktinės informacijos ieškokite skyriuje [„Commerce“ peržiūros aplinkos palaikymas](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="21de4-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="21de4-181">Kurti naują projektą</span><span class="sxs-lookup"><span data-stu-id="21de4-181">Create a new project</span></span>

<span data-ttu-id="21de4-182">Norėdami sukurti naują projektą LCS, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21de4-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="21de4-183">LCS pagrindiniame puslapyje pasirinkite pliuso ženklą (**„+“**), kad sukurtumėte projektą.</span><span class="sxs-lookup"><span data-stu-id="21de4-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="21de4-184">Dešiniojoje srityje atlikite vieną iš toliau pateikiamų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="21de4-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="21de4-185">Jei esate partneris, pasirinkite **Perkelti, kurti sprendimus ir sužinoti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="21de4-186">Jei esate klientas, pasirinkite **Galimas išankstinis pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="21de4-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="21de4-187">Įveskite pavadinimą, aprašą ir pramonės šaką.</span><span class="sxs-lookup"><span data-stu-id="21de4-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="21de4-188">Lauke **Produkto pavadinimas** pasirinkite **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="21de4-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="21de4-189">Lauke **Produkto versija** pasirinkite **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="21de4-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="21de4-190">Lauke **Metodika** pasirinkite **„Dynamics Retail“ visuotinio diegimo metodika**.</span><span class="sxs-lookup"><span data-stu-id="21de4-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="21de4-191">Pasirinktinai: galite importuoti vaidmenis ir vartotojus iš esamo projekto.</span><span class="sxs-lookup"><span data-stu-id="21de4-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="21de4-192">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-192">Select **Create**.</span></span> <span data-ttu-id="21de4-193">Pateikiamas projekto rodinys.</span><span class="sxs-lookup"><span data-stu-id="21de4-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="21de4-194">„Azure“ jungties įtraukimas</span><span class="sxs-lookup"><span data-stu-id="21de4-194">Add the Azure Connector</span></span>

<span data-ttu-id="21de4-195">Norėdami įtraukti „Azure“ jungti į savo LCS projektą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21de4-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="21de4-196">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="21de4-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="21de4-197">Jei esate partneris, pasirinkite plytelę **Projekto parametrai** dešinės pusės gale.</span><span class="sxs-lookup"><span data-stu-id="21de4-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="21de4-198">Jei esate klientas, viršutiniame meniu pasirinkite **Projekto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="21de4-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="21de4-199">Pasirinkite **„Azure“ jungtys**.</span><span class="sxs-lookup"><span data-stu-id="21de4-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="21de4-200">Pasirinkite **Įtraukti**, norėdami įtraukti „Azure“ jungtį.</span><span class="sxs-lookup"><span data-stu-id="21de4-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="21de4-201">Įvesti vardą.</span><span class="sxs-lookup"><span data-stu-id="21de4-201">Enter a name.</span></span>
1. <span data-ttu-id="21de4-202">Įveskite savo „Azure“ prenumeratos ID.</span><span class="sxs-lookup"><span data-stu-id="21de4-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="21de4-203">Įjunkite parinktį **Konfigūruoti, kad būtų galima naudoti „Azure“ išteklių tvarkytuvą (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="21de4-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="21de4-204">Įsitikinkite, kad vertė **„Azure“ prenumeratos AAD nuomotojo domenas ( arba ID)** yra tinkama.</span><span class="sxs-lookup"><span data-stu-id="21de4-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="21de4-205">Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.</span><span class="sxs-lookup"><span data-stu-id="21de4-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="21de4-206">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="21de4-206">Select **Next**.</span></span>
1. <span data-ttu-id="21de4-207">Sekite puslapyje pateikiamas instrukcijas, kad suteiktumėte reikiamoms programoms prieigą prie jūsų prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="21de4-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="21de4-208">Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.</span><span class="sxs-lookup"><span data-stu-id="21de4-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="21de4-209">Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="21de4-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="21de4-210">Įsitikinkite, kad pasirinktas tinkamas katalogas, o tada kairėje esančiame meniu pasirinkite **Prenumeratos**.</span><span class="sxs-lookup"><span data-stu-id="21de4-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="21de4-211">Sąraše raskite tinkamą prenumeratą ir ją pasirinkite.</span><span class="sxs-lookup"><span data-stu-id="21de4-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="21de4-212">Pagal poreikį naudokite ieškos funkciją.</span><span class="sxs-lookup"><span data-stu-id="21de4-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="21de4-213">Meniu pasirinkite **Prieigos valdymas (IAM)**.</span><span class="sxs-lookup"><span data-stu-id="21de4-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="21de4-214">Dešinėje, dalyje **Įtraukti vaidmens priskyrimą** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="21de4-215">Rodoma sritis **Įtraukti vaidmens priskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="21de4-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="21de4-216">Lauke **Vaidmuo** pasirinkite **Bendraautorius**.</span><span class="sxs-lookup"><span data-stu-id="21de4-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="21de4-217">Lauke **Priskirti prieigą prie** palikite numatytąją reikšmę, **„Azure AD“ vartotojas, grupė arba paslaugos narys**.</span><span class="sxs-lookup"><span data-stu-id="21de4-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="21de4-218">Dalyje **Pasirinkti** įveskite **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="21de4-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="21de4-219">Sąraše pasirinkite **„Dynamics Deployment Services“ \[wsfed-enabled\]**.</span><span class="sxs-lookup"><span data-stu-id="21de4-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="21de4-220">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-220">Select **Save**.</span></span>

1. <span data-ttu-id="21de4-221">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="21de4-221">Select **Next**.</span></span>
1. <span data-ttu-id="21de4-222">Sekite puslapyje pateikiamas instrukcijas, kad suteiktumėte reikiamoms programoms prieigą prie jūsų prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="21de4-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="21de4-223">Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.</span><span class="sxs-lookup"><span data-stu-id="21de4-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="21de4-224">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="21de4-224">Select **Next**.</span></span>
1. <span data-ttu-id="21de4-225">Lauke **„Azure“ regionas** pasirinkite **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.</span><span class="sxs-lookup"><span data-stu-id="21de4-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="21de4-226">Pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-226">Select **Connect**.</span></span> <span data-ttu-id="21de4-227">Jūsų „Azure“ jungtis turi pasirodyti sąraše.</span><span class="sxs-lookup"><span data-stu-id="21de4-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="21de4-228">„Commerce“ peržiūros demonstracinio pagrindinio plėtinio importavimas</span><span class="sxs-lookup"><span data-stu-id="21de4-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="21de4-229">Norėdami importuoti „Commerce“ peržiūros demonstracinį pagrindinį plėtinį į savo projektą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21de4-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="21de4-230">Atidarykite projekto pagrindinį puslapį, pasirinkę projekto pavadinimą viršuje.</span><span class="sxs-lookup"><span data-stu-id="21de4-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="21de4-231">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="21de4-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="21de4-232">Jei esate partneris, pasirinkite plytelę **Turto biblioteka** dešinės pusės gale.</span><span class="sxs-lookup"><span data-stu-id="21de4-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="21de4-233">Jei esate klientas, viršutiniame meniu pasirinkite **Turto biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="21de4-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="21de4-234">Pasirinkite **Programinės įrangos diegimo paketas** iš sąrašo kairėje pusėje.</span><span class="sxs-lookup"><span data-stu-id="21de4-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="21de4-235">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-235">Select **Import**.</span></span>
1. <span data-ttu-id="21de4-236">Dalyje **Bendrai naudojamo turto biblioteka** turto sąraše pasirinkite **„Commerce“ peržiūros demonstracinis pagrindinis plėtinys**.</span><span class="sxs-lookup"><span data-stu-id="21de4-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="21de4-237">Pasirinkite **Paimti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-237">Select **Pick**.</span></span> <span data-ttu-id="21de4-238">Grįšite į turto biblioteką ir turėtumėte matyti plėtinį sąraše.</span><span class="sxs-lookup"><span data-stu-id="21de4-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="21de4-239">Toliau pateikiamoje iliustracijoje parodyti veiksmai, kurių reikia imtis LCS puslapyje **Turto biblioteka**.</span><span class="sxs-lookup"><span data-stu-id="21de4-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![„Commerce“ peržiūros demonstracinio pagrindinio plėtinio importavimas](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="21de4-241">Aplinkos diegimas</span><span class="sxs-lookup"><span data-stu-id="21de4-241">Deploy the environment</span></span>

<span data-ttu-id="21de4-242">Atlikite toliau pateikiamus veiksmus, norėdami įdiegti aplinką.</span><span class="sxs-lookup"><span data-stu-id="21de4-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="21de4-243">Gali būti, kad nereikės atlikti 6, 7 ir (arba) 8 veiksmų, nes puslapiai, kuriuose yra viena parinktis, praleidžiami.</span><span class="sxs-lookup"><span data-stu-id="21de4-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="21de4-244">Rodinyje **Aplinkos parametrai** patvirtinkite, kad tekstas **„Dynamics 365 Commerce“ (Peržiūra) – Demonstracinė versija (10.0.6 su 30 platformos naujinimu)** rodomas tiesiai virš lauko **Aplinkos pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="21de4-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="21de4-245">Žr. iliustraciją, pateikiamą po 8 veiksmo.</span><span class="sxs-lookup"><span data-stu-id="21de4-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="21de4-246">Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.</span><span class="sxs-lookup"><span data-stu-id="21de4-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="21de4-247">Pasirinkite **Įtraukti**, kad įtrauktumėte aplinką.</span><span class="sxs-lookup"><span data-stu-id="21de4-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="21de4-248">Lauke **Programos versija** pasirinkite **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="21de4-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="21de4-249">Lauke **Platformos versija** pasirinkite **30 platformos naujinimas**.</span><span class="sxs-lookup"><span data-stu-id="21de4-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Programos ir platformos versijų pasirinkimas](./media/project1.png)

1. <span data-ttu-id="21de4-251">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="21de4-251">Select **Next**.</span></span>
1. <span data-ttu-id="21de4-252">Pasirinkite aplinkos topologiją **Demonstracinė versija**.</span><span class="sxs-lookup"><span data-stu-id="21de4-252">Select **Demo** as the environment topology.</span></span>

    ![1 aplinkos topologijos pasirinkimas](./media/project2.png)

1. <span data-ttu-id="21de4-254">Pasirinkite aplinkos topologiją **„Dynamics 365 Commerce“ (Peržiūra) – Demonstracinė versija**.</span><span class="sxs-lookup"><span data-stu-id="21de4-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="21de4-255">Jei anksčiau sukonfigūruosite vieną „Azure“ jungtį, ji bus naudojama šioje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="21de4-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="21de4-256">Jei sukonfigūravote keletą „Azure“ jungčių, galite pasirinkti, kurią jungtį naudoti: **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.</span><span class="sxs-lookup"><span data-stu-id="21de4-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="21de4-257">(Geriausiam betarpiškam našumui užtikrinti rekomenduojame pasirinkti **Vakarų JAV 2**.)</span><span class="sxs-lookup"><span data-stu-id="21de4-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![2 aplinkos topologijos pasirinkimas](./media/project3.png)

1. <span data-ttu-id="21de4-259">Puslapyje **Diegti aplinką** įveskite aplinkos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="21de4-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="21de4-260">Nekeiskite išplėstinių parametrų.</span><span class="sxs-lookup"><span data-stu-id="21de4-260">Leave the advanced settings as they are.</span></span>

    ![Puslapis Diegti aplinką](./media/project4.png)

1. <span data-ttu-id="21de4-262">Pagal poreikį pakoreguokite VM dydį.</span><span class="sxs-lookup"><span data-stu-id="21de4-262">Adjust the VM size as required.</span></span> <span data-ttu-id="21de4-263">(Rekomenduojame VM sandėliavimo vienetą \[SKU\] **„D13 v2“**.)</span><span class="sxs-lookup"><span data-stu-id="21de4-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="21de4-264">Peržiūrėkite kainodaros ir licencijavimo sąlygas, tada pažymėkite žymės langelį, kad patvirtintumėte, jog su jomis sutinkate.</span><span class="sxs-lookup"><span data-stu-id="21de4-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="21de4-265">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="21de4-265">Select **Next**.</span></span>
1. <span data-ttu-id="21de4-266">Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="21de4-267">Grįšite į rodinį **Aplinkos diegimo debesyje įrankis**, o jūsų aplinka turėtų būti rodoma sąraše.</span><span class="sxs-lookup"><span data-stu-id="21de4-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="21de4-268">Jūsų pageidaujama aplinka bus rodoma eilėje ir paskui diegiama.</span><span class="sxs-lookup"><span data-stu-id="21de4-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="21de4-269">Aplinkos darbo eigoms užbaigti prireiks laiko.</span><span class="sxs-lookup"><span data-stu-id="21de4-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="21de4-270">Todėl patikrinkite vėl maždaug po šešių–devynių valandų.</span><span class="sxs-lookup"><span data-stu-id="21de4-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="21de4-271">Prieš tęsdami įsitikinkite, kad jūsų aplinkos būsena yra **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="21de4-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="21de4-272">Paleiskite RCSU.</span><span class="sxs-lookup"><span data-stu-id="21de4-272">Initialize RCSU</span></span>

<span data-ttu-id="21de4-273">Norėdami inicijuoti RCSU, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21de4-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="21de4-274">Rodinyje **Aplinkos diegimo debesyje įrankis** sąraše pasirinkite savo aplinką.</span><span class="sxs-lookup"><span data-stu-id="21de4-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="21de4-275">Aplinkos rodinyje dešinėje pasirinkite **Visa išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="21de4-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="21de4-276">Rodomas aplinkos išsamios informacijos rodinys.</span><span class="sxs-lookup"><span data-stu-id="21de4-276">The environment details view appears.</span></span>
1. <span data-ttu-id="21de4-277">Dalyje **Aplinkos funkcijos** pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="21de4-278">Skirtuke **„Retail“** pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="21de4-279">Rodomas RCSU inicijavimo parametrų rodinys.</span><span class="sxs-lookup"><span data-stu-id="21de4-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="21de4-280">Lauke **Regionas** pasirinkite **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.</span><span class="sxs-lookup"><span data-stu-id="21de4-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="21de4-281">Lauke **Versija** sąraše pasirinkite **Nurodykite versiją**, tada pasirodžiusiame lauke nurodykite **9.16.19262.5**.</span><span class="sxs-lookup"><span data-stu-id="21de4-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="21de4-282">Būtinai nurodykite būtent tą versiją, kuri nurodyta čia.</span><span class="sxs-lookup"><span data-stu-id="21de4-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="21de4-283">Priešingu atveju vėliau teks atnaujinti RCSU į tinkamą versiją.</span><span class="sxs-lookup"><span data-stu-id="21de4-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="21de4-284">Įjunkite parinktį **Taikyti plėtinį**.</span><span class="sxs-lookup"><span data-stu-id="21de4-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="21de4-285">Plėtinių sąraše pasirinkite **„Commerce“ peržiūros demonstracinis pagrindinis plėtinys**.</span><span class="sxs-lookup"><span data-stu-id="21de4-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="21de4-286">Pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="21de4-287">Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="21de4-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="21de4-288">Grįšite į rodinį **„Retail“ valdymas**, kuriame pasirinktas skirtukas **„Retail“**.</span><span class="sxs-lookup"><span data-stu-id="21de4-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="21de4-289">Jūsų RCSU jau buvo rengimo eilėje.</span><span class="sxs-lookup"><span data-stu-id="21de4-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="21de4-290">Prieš tęsdami įsitikinkite, kad jūsų RCSU būsena yra **Pavyko**.</span><span class="sxs-lookup"><span data-stu-id="21de4-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="21de4-291">Inicijavimas trunka maždaug dvi–penkias valandas.</span><span class="sxs-lookup"><span data-stu-id="21de4-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="21de4-292">El. prekybos inicijavimas</span><span class="sxs-lookup"><span data-stu-id="21de4-292">Initialize e-Commerce</span></span>

<span data-ttu-id="21de4-293">Norėdami inicijuoti „e-Commerce“, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21de4-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="21de4-294">Skirtuke **„e-Commerce“ (Peržiūra)** peržiūrėkite sutikimą dėl peržiūros, tada pasirinkite **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="21de4-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="21de4-295">Lauke **„e-Commerce“ nuomotojo pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="21de4-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="21de4-296">Tačiau įsidėmėkite, kad šis pavadinimas bus rodomas kai kuriuose URL, nukreiptuose į jūsų „e-Commerce“ egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="21de4-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="21de4-297">Lauke **„Retail Cloud Scale Unit“ pavadinimas** sąraše pasirinkite savo RCSU.</span><span class="sxs-lookup"><span data-stu-id="21de4-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="21de4-298">(Sąraše turėtų būti tik viena parinktis.)</span><span class="sxs-lookup"><span data-stu-id="21de4-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="21de4-299">Laukas **„e-Commerce“ geografija** nustatomas automatiškai ir vertės keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="21de4-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="21de4-300">Pasirinkite **Pirmyn**, kad tęstumėte.</span><span class="sxs-lookup"><span data-stu-id="21de4-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="21de4-301">Lauke **Palaikomi pagrindinių kompiuterių vardai** įveskite bet kurį tinkamą domeną, pvz., `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="21de4-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="21de4-302">Lauke **AAD saugos grupė sistemos administratoriui** įveskite keletą pirmų norimos naudoti saugos grupės pavadinimo raidžių.</span><span class="sxs-lookup"><span data-stu-id="21de4-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="21de4-303">Pasirinkite padidinamojo stiklo piktogramą, kad būtų rodomi ieškos rezultatai.</span><span class="sxs-lookup"><span data-stu-id="21de4-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="21de4-304">Pasirinkite saugos grupę sąraše.</span><span class="sxs-lookup"><span data-stu-id="21de4-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="21de4-305">Lauke **AAD saugos grupė įvertinimų ir apžvalgų moderatoriui** įveskite keletą pirmų norimos naudoti saugos grupės pavadinimo raidžių.</span><span class="sxs-lookup"><span data-stu-id="21de4-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="21de4-306">Pasirinkite padidinamojo stiklo piktogramą, kad būtų rodomi ieškos rezultatai.</span><span class="sxs-lookup"><span data-stu-id="21de4-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="21de4-307">Pasirinkite saugos grupę sąraše.</span><span class="sxs-lookup"><span data-stu-id="21de4-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="21de4-308">Parinktį **Įjungti įvertinimų ir apžvalgų paslauga** palikite įjungtą.</span><span class="sxs-lookup"><span data-stu-id="21de4-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="21de4-309">Jei jau atlikote „Microsoft Azure Active Directory“ („Azure AD“) sutikimo veiksmą, aprašytą skyriuje „Prieigos prie „e-Commerce“ programų suteikimas“, pažymėkite žymės langelį, kad patvirtintumėte savo sutikimą.</span><span class="sxs-lookup"><span data-stu-id="21de4-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="21de4-310">Jei šio veiksmo dar neatlikote, turite tai padaryti prieš tęsdami inicijavimą.</span><span class="sxs-lookup"><span data-stu-id="21de4-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="21de4-311">Norėdami atidaryti sutikimo dialogo langą ir atlikti veiksmą, pažymėkite šalia žymės langelio esančiame tekste esantį saitą.</span><span class="sxs-lookup"><span data-stu-id="21de4-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="21de4-312">Pasirinkite **Inicijuoti**.</span><span class="sxs-lookup"><span data-stu-id="21de4-312">Select **Initialize**.</span></span> <span data-ttu-id="21de4-313">Grįžtate į rodinį **„Retail“ valdymas**, kuriame pasirinktas skirtukas **„e-Commerce“ (Peržiūra)**.</span><span class="sxs-lookup"><span data-stu-id="21de4-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="21de4-314">„E-Commerce“ inicijavimas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="21de4-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="21de4-315">Prieš tęsdami, palaukite, kol „e-Commerce“ inicijavimo būsena bus **Inicijuota sėkmingai**.</span><span class="sxs-lookup"><span data-stu-id="21de4-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="21de4-316">Dalyje **Saitai** apatiniame dešiniajame kampe pasižymėkite toliau pateikiamų saitų URL.</span><span class="sxs-lookup"><span data-stu-id="21de4-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="21de4-317">**„e-Commerce“ svetainė** – saitas į jūsų „e-Commerce“ svetainės šaknį.</span><span class="sxs-lookup"><span data-stu-id="21de4-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="21de4-318">**„e-Commerce“ svetainės valdymo įrankis** – saitas į svetainės valdymo įrankį.</span><span class="sxs-lookup"><span data-stu-id="21de4-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="21de4-319">„Commerce“ peržiūros aplinkos palaikymas</span><span class="sxs-lookup"><span data-stu-id="21de4-319">Commerce preview environment support</span></span>

<span data-ttu-id="21de4-320">Jei atlikdami parengimo veiksmus patiriate problemų, apsilankykite [„Microsoft Dynamics 365 Commerce“ peržiūros versijos „Yammer“ grupėje](https://aka.ms/Dynamics365CommercePreviewYammer) dėl pagalbos.</span><span class="sxs-lookup"><span data-stu-id="21de4-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="21de4-321">Jei, bandant pasiekti „Yammer“ grupę, kyla problemų, su „Microsoft“ galite susisiekti el. pašto adresu <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="21de4-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="21de4-322">Šis el. pašto adresas nėra aktyviai stebimas.</span><span class="sxs-lookup"><span data-stu-id="21de4-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="21de4-323">Todėl atsakyti galime ne iš karto.</span><span class="sxs-lookup"><span data-stu-id="21de4-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="21de4-324">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="21de4-324">Next steps</span></span>

<span data-ttu-id="21de4-325">Norėdami tęsti „Commerce“ peržiūros aplinkos parengimo ir konfigūravimo procesą, žr. skyrių [„Commerce“ peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="21de4-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21de4-326">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="21de4-326">Additional resources</span></span>

[<span data-ttu-id="21de4-327">„Commerce” peržiūros aplinkos apžvalga</span><span class="sxs-lookup"><span data-stu-id="21de4-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="21de4-328">„Commerce” peržiūros aplinkos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="21de4-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="21de4-329">Pasirenkamų „Commerce” peržiūros aplinkos funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="21de4-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="21de4-330">DUK apie „Commerce” peržiūros aplinką</span><span class="sxs-lookup"><span data-stu-id="21de4-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="21de4-331">„Microsoft Lifecycle Services“ (LCS)</span><span class="sxs-lookup"><span data-stu-id="21de4-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="21de4-332">„Retail Cloud Scale Unit“ (RCSU)</span><span class="sxs-lookup"><span data-stu-id="21de4-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="21de4-333">„Microsoft Azure“ portalas</span><span class="sxs-lookup"><span data-stu-id="21de4-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="21de4-334">„Dynamics 365 Commerce“ svetainė</span><span class="sxs-lookup"><span data-stu-id="21de4-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="21de4-335">„Dynamics 365 Retail“ žinyno ištekliai</span><span class="sxs-lookup"><span data-stu-id="21de4-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
