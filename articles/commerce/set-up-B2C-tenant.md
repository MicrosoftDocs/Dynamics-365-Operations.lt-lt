---
title: „Commerce” B2C nuomotojo sąranka
description: Šioje temoje aprašoma, kaip nustatyti „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojus, skirtus vartotojo svetainės autentifikavimui „Dynamics 365 Commerce“.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: a5fca37fb89c723273ef753b102092e2cfb26563
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096517"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="e7e71-103">„Commerce” B2C nuomotojo sąranka</span><span class="sxs-lookup"><span data-stu-id="e7e71-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7e71-104">Šioje temoje aprašoma, kaip nustatyti „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojus, skirtus vartotojo svetainės autentifikavimui „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7e71-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="e7e71-105">Overview</span></span>

<span data-ttu-id="e7e71-106">„Dynamics 365 Commerce“ naudoja „Azure AD“ B2C, kad palaikytų vartotojo kredencialus ir autentifikavimo srautus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="e7e71-107">Vartotojas gali prisiregistruoti, prisijungti ir iš naujo nustatyti savo slaptažodį naudodamas šiuos srautus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="e7e71-108">„Azure AD“ B2C saugoma vartotojo slapto autentifikavimo informacija, pvz., vartotojo vardas ir slaptažodis.</span><span class="sxs-lookup"><span data-stu-id="e7e71-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="e7e71-109">Vartotoje įraše B2C nuomotojuje bus saugomas arba B2C vietos sąskaitos įrašas arba B2C socialinės tapatybės teikimo įrankio įrašas.</span><span class="sxs-lookup"><span data-stu-id="e7e71-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="e7e71-110">Šie B2C įrašai bus susieti su kliento įrašu „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="e7e71-111">Kūrimas arba susiejimas su esamu AAD B2C nuomotoju „Azure“ portale</span><span class="sxs-lookup"><span data-stu-id="e7e71-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="e7e71-112">Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="e7e71-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="e7e71-113">„Azure“ portalo meniu pasirinkite **Kurti išteklius**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="e7e71-114">Įsitikinkite, kad naudojate prenumeratą ir katalogą, kurie bus susieti su jūsų „Commerce“ aplinka.</span><span class="sxs-lookup"><span data-stu-id="e7e71-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Išteklių „Azure“ portale kūrimas](./media/B2CImage_1.png)

1. <span data-ttu-id="e7e71-116">Eikite į **Tapatybė \> „Azure Active Directory“ B2C**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="e7e71-117">Kai būsite puslapyje **Kurti naują B2C nuomotoją arba susieti su esamu nuomotoju**, pasirinkite vieną iš toliau apteiktų parinkčių, kuri geriausiai atitinka jūsų įmonės poreikius.</span><span class="sxs-lookup"><span data-stu-id="e7e71-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="e7e71-118">**Kurti naują „Azure AD“ B2C nuomotoją**: naudokite šią parinktį, kad sukurtumėte naują AAD B2C nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="e7e71-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="e7e71-119">Pasirinkite **Kurti naują „Azure AD“ B2C nuomotoją**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="e7e71-120">Dalyje **Organizacijos pavadinimas** įveskite organizacijos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="e7e71-121">Dalyje **Pradinis domeno pavadinimas** įveskite pradinį domeno pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="e7e71-122">Dalyje **Šalis arba regionas** pasirinkite šalį arba regioną.</span><span class="sxs-lookup"><span data-stu-id="e7e71-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="e7e71-123">Pasirinkite **Kurti**, kad sukurtumėte nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="e7e71-123">Select **Create** to create the tenant.</span></span>

     ![Naujo „Azure AD“ nuomotojo kūrimas](./media/B2CImage_2.png)

     - <span data-ttu-id="e7e71-125">**Susieti esamą „Azure AD“ B2C nuomotoją su mano „Azure“ prenumerata**: naudokite šią parinktį, jei jau turite „Azure AD“ B2C nuomininką, su kuriuo norite susieti.</span><span class="sxs-lookup"><span data-stu-id="e7e71-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="e7e71-126">Pasirinkite **Susieti esamą „Azure AD“ B2C nuomotoją su mano Azure prenumerata**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="e7e71-127">Jei **„Azure AD“ B2C nuomotojas**, pasirinkite atitinkamą B2C nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="e7e71-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="e7e71-128">Jei pasirinkimo lauke rodomas pranešimas „Nerasta tinkamų B2C nuomotojų“, neturite tinkamo B2C nuomotojo ir turite sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="e7e71-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="e7e71-129">Jei **Išteklių grupė**, pasirinkite **Kurti naują**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="e7e71-130">Įveskite išteklių grupės, kurioje bus nuomotojas, **Pavadinimas**, pasirinkite **Išteklių grupės vieta**, tada pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Esamo „Azure AD“ B2C nuomotojo susiejimas su „Azure“ prenumerata](./media/B2CImage_3.png)

1. <span data-ttu-id="e7e71-132">Kai sukuriamas naujas „Azure AD“ B2C katalogas (tai gali užtrukti kelias akimirkas), ataskaitų srityje bus pradėtas rodyti saitas į ataskaitų sritį.</span><span class="sxs-lookup"><span data-stu-id="e7e71-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="e7e71-133">Šis saitas nukreips jus į puslapį „Sveiki atvykę į „Azure Active Directory“ B2C“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Susiejimas su nauju AAD katalogu](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="e7e71-135">Jei turite kelias savo „Azure“ sąskaitos prenumeratas arba nustatėte B2C nuomotoją nesusiedami su aktyvia prenumerata, nesusiejant su aktyvia prenumerata, juosta **Trikčių diagnostika** jus nukreips, kad susietumėte nuomotoją su prenumerata.</span><span class="sxs-lookup"><span data-stu-id="e7e71-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="e7e71-136">Pasirinkite trikčių diagnostikos pranešimą ir sekite instrukcijas, kad išspręstumėte prenumeratos problemą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="e7e71-137">Šiame vaizde parodytas „Azure AD“ B2C **Trikčių diagnostika** juosta.</span><span class="sxs-lookup"><span data-stu-id="e7e71-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Įspėjimas, rodantis, kad kataloge nėra aktyvios prenumeratos](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="e7e71-139">B2C programos kūrimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-139">Create the B2C application</span></span>

<span data-ttu-id="e7e71-140">Sukūrus B2C nuomotoją, bus sukurta B2C programa, skirta dirbti su „Commerce“ veiksmais.</span><span class="sxs-lookup"><span data-stu-id="e7e71-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="e7e71-141">Norėdami sukurti B2C programą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-142">„Azure“ portale pasirinkite **Programos**, tada pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-142">In the Azure portal, select **Applications** and then select **Add**.</span></span>
1. <span data-ttu-id="e7e71-143">Dalyje **Pavadinimas** įveskite pageidaujamos AAD B2C programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="e7e71-144">Dalyje **Web App/Web API** **Įtraukti žiniatinklio programa / žiniatinklio API** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="e7e71-145">Norėdami **Leisti numanomą srautą** pasirinkite **Taip** (numatytoji reikšmė).</span><span class="sxs-lookup"><span data-stu-id="e7e71-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="e7e71-146">Dalyje **Atsakymo URL** įveskite skirtuosius atsakymo URL.</span><span class="sxs-lookup"><span data-stu-id="e7e71-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="e7e71-147">Žr. [Atsakymo URL](#reply-urls) toliau, kur pateikta informacijos apie atsakymo URL ir kaip juos formatuoti.</span><span class="sxs-lookup"><span data-stu-id="e7e71-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="e7e71-148">Norėdami **Įtraukti vietinį klientą**, pasirinkite **Ne** (numatytoji reikšmė).</span><span class="sxs-lookup"><span data-stu-id="e7e71-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="e7e71-149">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="e7e71-150">Atsakymo URL</span><span class="sxs-lookup"><span data-stu-id="e7e71-150">Reply URLs</span></span>

<span data-ttu-id="e7e71-151">Atsakymo URL yra svarbūs, nes jie leidžia grąžinimo domenų baltąjį sąrašą, kai jūsų svetainė reikalauja „Azure AD“ B2C, kad būtų autentifikuotas vartotojas.</span><span class="sxs-lookup"><span data-stu-id="e7e71-151">Reply URLs are important as they allow a whitelist of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="e7e71-152">Tai leidžia autentifikuoti vartotoją grąžinti į domeną, iš kurio jis prisijungė (jūsų svetainės domenas).</span><span class="sxs-lookup"><span data-stu-id="e7e71-152">This allows the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="e7e71-153">Lauke **Atsakymo URL** ekrane **„Azure AD“ B2c – programos \> Nauja programa** turite įtraukti atskiras eilutes tiek svetainės domenui, tiek (kai jūsų aplinka paruošta) „Commerce“ sugeneruotam URL.</span><span class="sxs-lookup"><span data-stu-id="e7e71-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="e7e71-154">Šie URL turi visada naudoti tinkamą URL formatą ir jie turi būti tik pagrindiniai URL (nėra pasvirųjų brūkšnių ar maršrutų).</span><span class="sxs-lookup"><span data-stu-id="e7e71-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="e7e71-155">Tada eilutę ``/_msdyn365/authresp`` reikia pridėti prie pagrindinių URL, kaip tolesniuose pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="e7e71-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- ``https://fabrikam.com/_msdyn365/authresp``
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="e7e71-156">Vartotojo srauto strategijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-156">Create user flow policies</span></span>

<span data-ttu-id="e7e71-157">Vartotojų srautai yra strategijos, kurias „Azure AD“ B2C naudoja, kad suteiktų saugą prisiregistravimą, prisijungimą, profilio redagavimą ir pamiršto slaptažodžio keitimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-157">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="e7e71-158">„Dynamics 365 Commerce“ naudoja šiuos srautus, kad galėtų atlikti strategijos veiksmus, skirtus sąveikauti „Azure AD“ B2C nuomotoju.</span><span class="sxs-lookup"><span data-stu-id="e7e71-158">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="e7e71-159">Kai vartotojas sąveikauja su šiomis strategijomis, jis nukreipiami į „Azure AD“ B2C nuomotoją, kad atliktų veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-159">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="e7e71-160">„Azure AD“ B2C pateikiami trys pagrindiniai vartotojo srautų tipai:</span><span class="sxs-lookup"><span data-stu-id="e7e71-160">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="e7e71-161">Prisiregistravimas ir prisijungimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-161">Sign up and sign in</span></span>
- <span data-ttu-id="e7e71-162">Profilio redagavimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-162">Profile editing</span></span>
- <span data-ttu-id="e7e71-163">Slaptažodžio nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="e7e71-163">Password reset</span></span>

<span data-ttu-id="e7e71-164">Galite pasirinkti naudoti numatytuosius vartotojo srautus, kuriuos siūlo „Azure AD“ ir kurie bus rodomi AAD B2C puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-164">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="e7e71-165">Arba galite sukurti HTML puslapį, kad galėtumėte valdyti šios vartotojo srauto patirties apipavidalinimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-165">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="e7e71-166">Norėdami tinkinti vartotojo strategijos puslapius „Dynamics 365 Commerce“ žr. [Pasirinktinių puslapių nustatymas vartotojų prisijungimui](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="e7e71-166">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="e7e71-167">Daugiau informacijos žr. [Vartotojų patirties sąsajos tinkinimas „Azure Active Directory“ B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="e7e71-167">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="e7e71-168">Prisiregistravimo ir prisijungimo vartotojo srauto strategijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-168">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="e7e71-169">Norėdami sukurti prisiregistravimo ir prisijungimo vartotojo srauto strategiją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-169">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-170">„Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-170">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="e7e71-171">Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-171">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="e7e71-172">Skirtuke **Rekomenduojama** pasirinkite **Registruotis ir prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-172">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="e7e71-173">Dalyje **Pavadinimas** įveskite strategijos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-173">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="e7e71-174">Šis pavadinimas bus rodomas su prievardžiu, kurį priskyrė portalas (pavyzdžiui, „B2C_1_“).</span><span class="sxs-lookup"><span data-stu-id="e7e71-174">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="e7e71-175">Dalyje **Tapatybės teikimo įrankiai** pažymėkite atitinkamą žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="e7e71-175">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="e7e71-176">Dalyje **Kelių faktorių autentifikavimas** atlikite pasirinkimą pagal savo įmonę.</span><span class="sxs-lookup"><span data-stu-id="e7e71-176">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="e7e71-177">Dalyje **Vartotojo atributai ir pretenzijos**pasirinkite pasirinktis, kad būtų galima rinkti atributus arba grąžinti pretenzijas, kaip tinkama.</span><span class="sxs-lookup"><span data-stu-id="e7e71-177">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="e7e71-178">„Commerce“ reikia nustatyti tolesnes numatytąsias parinktis:</span><span class="sxs-lookup"><span data-stu-id="e7e71-178">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="e7e71-179">**Rinkti atributą**</span><span class="sxs-lookup"><span data-stu-id="e7e71-179">**Collect  attribute**</span></span> | <span data-ttu-id="e7e71-180">**Grąžinti pretenziją**</span><span class="sxs-lookup"><span data-stu-id="e7e71-180">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    |                        | <span data-ttu-id="e7e71-181">El. pašto adresai</span><span class="sxs-lookup"><span data-stu-id="e7e71-181">Email Addresses</span></span>   |
    | <span data-ttu-id="e7e71-182">Vardas</span><span class="sxs-lookup"><span data-stu-id="e7e71-182">Given Name</span></span>             | <span data-ttu-id="e7e71-183">Vardas</span><span class="sxs-lookup"><span data-stu-id="e7e71-183">Given Name</span></span>        |
    |                        | <span data-ttu-id="e7e71-184">Tapatybės teikimo įrankis</span><span class="sxs-lookup"><span data-stu-id="e7e71-184">Identity Provider</span></span> |
    | <span data-ttu-id="e7e71-185">Pavardė</span><span class="sxs-lookup"><span data-stu-id="e7e71-185">Surname</span></span>                | <span data-ttu-id="e7e71-186">Pavardė</span><span class="sxs-lookup"><span data-stu-id="e7e71-186">Surname</span></span>           |
    |                        | <span data-ttu-id="e7e71-187">Vartotojo objekto ID</span><span class="sxs-lookup"><span data-stu-id="e7e71-187">User’s Object ID</span></span>  |

1. <span data-ttu-id="e7e71-188">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-188">Select **Create**.</span></span>

<span data-ttu-id="e7e71-189">Tolesniame vaizde pateikiamas „Azure AD“ B2C prisiregistravimo ir prisijungimo vartotojo srauto pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e7e71-189">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Prisiregistravimo ir prisijungimo strategijos parametrai](./media/B2CImage_11.png)

<span data-ttu-id="e7e71-191">Tolesniame paveiksle rodoma parinktis **Vykdyti vartotojo srautą** „Azure AD“ B2C prisiregistravimo ir prisijungimo vartotojo sraute.</span><span class="sxs-lookup"><span data-stu-id="e7e71-191">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Vartotojo srauto vykdymo parinktis strategijos sraute](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="e7e71-193">Profilio redagavimo vartotojo srauto strategijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-193">Create a profile editing user flow policy</span></span>

<span data-ttu-id="e7e71-194">Norėdami sukurti profilio redagavimo vartotojo srauto strategiją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-194">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-195">„Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-195">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="e7e71-196">Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-196">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="e7e71-197">Skirtuke **Rekomenduojama** pasirinkite **Profilio redagavimas**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-197">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="e7e71-198">Dalyje **Pavadinimas** įveskite profilio redagavimo vartotojo srautą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-198">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="e7e71-199">Šis pavadinimas bus rodomas su prievardžiu, kurį priskyrė portalas (pavyzdžiui, „B2C_1_“).</span><span class="sxs-lookup"><span data-stu-id="e7e71-199">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="e7e71-200">Dalyje **Tapatybės teikimo įrankis** pasirinkite **Prisijungimas prie vietinės sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-200">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="e7e71-201">Dalyje **Vartotojo atributai** pažymėkite bet kurį iš šių žymės langelių:</span><span class="sxs-lookup"><span data-stu-id="e7e71-201">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="e7e71-202">**El. pašto adresai** (tik **Grąžinti pretenziją**)</span><span class="sxs-lookup"><span data-stu-id="e7e71-202">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="e7e71-203">**Vardas** (**Rinkti atributą** ir **Grąžinti pretenziją**)</span><span class="sxs-lookup"><span data-stu-id="e7e71-203">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="e7e71-204">**Tapatybės teikimo įrankis** (tik **Grąžinti pretenziją** )</span><span class="sxs-lookup"><span data-stu-id="e7e71-204">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="e7e71-205">**Pavardę** (**Rinkti atributą** ir **Grąžinti pretenziją**)</span><span class="sxs-lookup"><span data-stu-id="e7e71-205">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="e7e71-206">**Vartotojo objekto ID** (tik **Grąžinti pretenziją**)</span><span class="sxs-lookup"><span data-stu-id="e7e71-206">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="e7e71-207">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-207">Select **Create**.</span></span>

<span data-ttu-id="e7e71-208">Tolesniame paveiksle pateiktas „Azure AD“ B2C profilio redagavimo vartotojo srauto pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e7e71-208">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Profilio redagavimo vartotojo srauto kūrimas](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="e7e71-210">Slaptažodžio nustatymo iš naujo vartotojo srauto strategijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-210">Create a password reset user flow policy</span></span>

<span data-ttu-id="e7e71-211">Norėdami sukurti slaptažodžio nustatymo iš naujo vartotojo srauto strategiją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-211">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-212">„Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-212">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="e7e71-213">Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-213">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="e7e71-214">Skirtuke **Rekomenduojama** pasirinkite **Slaptažodžio nustatymas iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-214">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="e7e71-215">Dalyje **Pavadinimas** įveskite slaptažodžio nustatymo iš naujo vartotojo srauto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-215">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="e7e71-216">Dalyje **Tapatybės teikimo įrankiai** pasirinkite **Iš naujo nustatyti slaptažodį naudojant el. pašto adresą**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-216">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="e7e71-217">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-217">Select **Create**.</span></span>
1. <span data-ttu-id="e7e71-218">Dalyje **Programos teiginiai** pažymėkite bet kurį iš šių žymės langelių:</span><span class="sxs-lookup"><span data-stu-id="e7e71-218">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="e7e71-219">**El. pašto adresas**</span><span class="sxs-lookup"><span data-stu-id="e7e71-219">**Email**</span></span>
    - <span data-ttu-id="e7e71-220">**Adresai**</span><span class="sxs-lookup"><span data-stu-id="e7e71-220">**Addresses**</span></span>
    - <span data-ttu-id="e7e71-221">**Vardas**</span><span class="sxs-lookup"><span data-stu-id="e7e71-221">**Given Name**</span></span>
    - <span data-ttu-id="e7e71-222">**Pavardė**</span><span class="sxs-lookup"><span data-stu-id="e7e71-222">**Surname**</span></span>
    - <span data-ttu-id="e7e71-223">**Vartotojo objekto ID**</span><span class="sxs-lookup"><span data-stu-id="e7e71-223">**User's Object ID**</span></span>
1. <span data-ttu-id="e7e71-224">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-224">Select **Create**.</span></span>

<span data-ttu-id="e7e71-225">Toliau pateiktame paveiksle parodyta, kur nustatyti **Nustatyti iš naujo slaptažodį naudojant el. pašto adresą** „Azure AD“ B2C vartotojo slaptažodžio nustatymo iš naujo sraute.</span><span class="sxs-lookup"><span data-stu-id="e7e71-225">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![„Nustatyti iš naujo slaptažodį naudojant el. pašto adresą“ nustatymas slaptažodžio nustatymo iš naujo strategijoje](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="e7e71-227">Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="e7e71-227">Add social identity providers (Optional)</span></span>

<span data-ttu-id="e7e71-228">Socialinės tapatybės teikimo įrankis leidžia vartotojams naudotis savo socialinėmis sąskaitomis autentifikavimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="e7e71-228">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="e7e71-229">Socialinės tapatybės teikimo įrankio autentifikavimo įtraukimas yra pasirinktinis „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-229">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="e7e71-230">Jei nėra įtrauktas socialinės tapatybės teikimo įrankio autentifikavimas, numatytieji „Azure AD“ B2C profiliai bus pagrindiniai vartotojų bazės profiliai.</span><span class="sxs-lookup"><span data-stu-id="e7e71-230">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="e7e71-231">Vartotojai pasirinks savo vartotojo vardą (pageidaujamą el. pašto adresą) ir nustatys slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="e7e71-231">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="e7e71-232">„Azure AD“ B2C autentifikuos vartotojus tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="e7e71-232">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="e7e71-233">Jei įtrauktas socialinės tapatybės teikimo įrankio autentifikavimas ir vartotojas pasirenka vieną iš siūlomų socialinės tapatybės teikimo įrankių, šis objektas vis dar yra sukurtas „Azure AD“ B2C nuomotojuje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-233">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="e7e71-234">„Azure AD“ B2C autentifikuos vartotojo kredencialus naudodama socialinės tapatybė teikimo įrankį,</span><span class="sxs-lookup"><span data-stu-id="e7e71-234">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="e7e71-235">Tapatybės teikimo įrankio prisijungimas sukuria įrašą B2C nuomotojuje, tačiau kitu formatu, nei vietos sąskaitos, nes jis iškviečia išorinę socialinės tapatybės teikimo įrankio nuorodą autentifikavimui.</span><span class="sxs-lookup"><span data-stu-id="e7e71-235">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="e7e71-236">Vartotojas gali naudoti tą patį el. pašto adresą visiems socialinės tapatybės teikimo įrankiams, t. y. el. pašto vartotojo vardas, naudojamas autentifikavimui, negali būti unikalus nuomotojui.</span><span class="sxs-lookup"><span data-stu-id="e7e71-236">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="e7e71-237">„Azure AD“ B2C užtikrins tik tai, kad vartotojas turi unikalų el. pašto adresą vietos B2C sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="e7e71-237">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="e7e71-238">Prieš pridėdami socialinės tapatybės teikimo įrankį autentifikavimo tikslu, turite eiti į tapatybės teikimo įrankio portalą ir nustatyti tapatybės teikimo įrankio programą, kaip nurodyta „Azure AD B2C“ dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="e7e71-238">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="e7e71-239">Saitų į dokumentus sąrašas pateiktas toliau.</span><span class="sxs-lookup"><span data-stu-id="e7e71-239">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="e7e71-240">„Amazon“</span><span class="sxs-lookup"><span data-stu-id="e7e71-240">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="e7e71-241">Azure AD(Vienas nuomotojas)</span><span class="sxs-lookup"><span data-stu-id="e7e71-241">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="e7e71-242">„Microsoft“ abonementas</span><span class="sxs-lookup"><span data-stu-id="e7e71-242">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="e7e71-243">Facebook</span><span class="sxs-lookup"><span data-stu-id="e7e71-243">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="e7e71-244">GitHub</span><span class="sxs-lookup"><span data-stu-id="e7e71-244">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="e7e71-245">Google</span><span class="sxs-lookup"><span data-stu-id="e7e71-245">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="e7e71-246">„LinkedIn“</span><span class="sxs-lookup"><span data-stu-id="e7e71-246">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="e7e71-247">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="e7e71-247">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="e7e71-248">„Twitter“</span><span class="sxs-lookup"><span data-stu-id="e7e71-248">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="e7e71-249">Socialinės tapatybės teikimo įrankio įtraukimas ir nustatymas</span><span class="sxs-lookup"><span data-stu-id="e7e71-249">Add and set up a social identity provider</span></span>

<span data-ttu-id="e7e71-250">Norėdami įtraukti ir nustatyti socialinės tapatybės teikimo įrankį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-250">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="e7e71-251">„Azure“ portale eikite į **Tapatybės teikimo įrankiai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-251">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="e7e71-252">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-252">Select **Add**.</span></span> <span data-ttu-id="e7e71-253">Rodomas langas **Įtraukti tapatybės teikimo įrankį**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-253">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="e7e71-254">Dalyje **Pavadinimas**įveskite pavadinimą, kuris bus rodomas vartotojams prisijungimo ekrane.</span><span class="sxs-lookup"><span data-stu-id="e7e71-254">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="e7e71-255">Dalyje **Tapatybės teikimo įrankio tipas** iš sąrašo pasirinkite tapatybės teikimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="e7e71-255">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="e7e71-256">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-256">Select **OK**.</span></span>
1. <span data-ttu-id="e7e71-257">Pasirinkite **Nustatyti šį tapatybės teikimo įrankį**, kad būtų atidarytas ekranas **Nustatyti socialinės tapatybės teikimo įrankį**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-257">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="e7e71-258">Dalyje **Kliento ID** įveskite kliento ID, gautą iš tapatybės teikimo įrankio programos sąrankos.</span><span class="sxs-lookup"><span data-stu-id="e7e71-258">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="e7e71-259">Dalyje **Kliento paslaptis** įveskite kliento paslaptį, gautą iš tapatybės teikimo įrankio programos sąrankos.</span><span class="sxs-lookup"><span data-stu-id="e7e71-259">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="e7e71-260">Vartotojo prisiregistravimo ir prisijungimo srauto strategijų pridėjimas:</span><span class="sxs-lookup"><span data-stu-id="e7e71-260">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="e7e71-261">Eikite į **„Azure AD“ B2C – vartotojo srautai (strategijos) \> {jūsų prisiregistravimo ir prisijungimo strategija} \> Tapatybės teikimo įrankiai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-261">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="e7e71-262">Norėdami pridėti prisiregistravimo / prisijungimo vartotojo srauto strategiją, pasirinkit kiekvieną tapatybės teikimo įrankį, kurį nustatėte savo sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-262">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="e7e71-263">Norėdami tai atlikti, pasirinkite **Vykdyti vartotoją srautą** kiekvienam tapatybės teikimo įrankiui.</span><span class="sxs-lookup"><span data-stu-id="e7e71-263">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="e7e71-264">Naujame skirtuke bus rodomas registravimosi puslapis, kuriame rodomas naujo tapatybės teikimo įrankio langelis.</span><span class="sxs-lookup"><span data-stu-id="e7e71-264">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="e7e71-265">Tolesniame paveiksle pateikiami ekranų **Įtraukti tapatybės teikimo įrankį** ir **Nustatyti socialinės tapatybės teikimo įrankį** „Azure AD“ B2C.</span><span class="sxs-lookup"><span data-stu-id="e7e71-265">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Socialinės tapatybės teikimo įrankio įtraukimas į programą](./media/B2CImage_14.png)

<span data-ttu-id="e7e71-267">Tolesniame paveiksle pateiktas pavyzdys, kaip pasirinkti tapatybės teikimo įrankius „Azure AD“ B2C puslapyje **Tapatybės teikimo įrankiai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-267">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Kiekvieno socialinės tapatybės teikimo įrankio pasirinkimas siekiant įjungti strategiją](./media/B2CImage_16.png)

<span data-ttu-id="e7e71-269">Toliau pateiktame paveikslėlyje parodytas numatytojo prisijungimo ekrano, kuriame rodomas socialinės tapatybės teikimo įrankio prisijungimo mygtukas, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e7e71-269">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Numatytojo prisijungimo ekrano su rodomu socialinės tapatybės teikimo įrankio mygtuku pavyzdys](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="e7e71-271">„Commerce“ būstinės naujinimas su nauja „Azure AD B2C“ informacija</span><span class="sxs-lookup"><span data-stu-id="e7e71-271">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="e7e71-272">Kai užbaigiami pirmiau nurodyti „Azure AD“ B2C paruošimo veiksmai, „Azure AD“ B2C programą reikia užregistruoti jūsų „Dynamics 365 Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-272">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="e7e71-273">Norėdami atnaujinti būstinę su naują „Azure AD“ B2C informaciją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-273">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-274">„Commerce“ eikite į **„Commerce“ bendrinti parametrai** ir kairiajame meniu pasirinkite **Tapatybės teikimo įrankiai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-274">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="e7e71-275">Dalyje **Tapatybės teikimo įrankiai** atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-275">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="e7e71-276">Lauke **Leidėjas** įveskite tapatybės teikimo įrankio leidėjo URL.</span><span class="sxs-lookup"><span data-stu-id="e7e71-276">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="e7e71-277">Norėdami rasti savo leidėjo URL, žr. [Leidėjo URL gavimas](#obtain-issuer-url) toliau.</span><span class="sxs-lookup"><span data-stu-id="e7e71-277">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="e7e71-278">Lauke **Pavadinimas** įveskite savo leidėjo įrašo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-278">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="e7e71-279">Lauke **Tipas** įveskite **„Azure AD“ B2C (id_token)**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-279">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="e7e71-280">Dalyje **Pasikliaujančios šalys** su anksčiau pasirinktu B2C tapatybės teikimo įrankiu atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-280">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="e7e71-281">Lauke **KlientoID** įveskite B2C programos ID.</span><span class="sxs-lookup"><span data-stu-id="e7e71-281">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="e7e71-282">Tai galite rasti savo B2C programos ypatybių puslapio lauke **Programos ID**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-282">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="e7e71-283">Lauke **Tipas** įveskite **Viešas**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-283">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="e7e71-284">Lauke **Vartotojo tipas** įveskite **Klientas**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-284">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="e7e71-285">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-285">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="e7e71-286">„Commerce“ ieškos lauke ieškokite **Numeracijos** (organizacijos administravimas > Numeracijos).</span><span class="sxs-lookup"><span data-stu-id="e7e71-286">In the Commerce search box, search for **Number sequences** (Organization administration > Number sequences).</span></span>
1. <span data-ttu-id="e7e71-287">Veiksmų srityje pasirinkite **Redaguoti** dalyje **Tvarkyti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-287">Under the action pane, select **Edit** under **Maintain**.</span></span>
1. <span data-ttu-id="e7e71-288">„Fast tab“ **Bendra** pasirinkite **Ne** ties **Rankiniu būdu**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-288">On the **General** fast tab, select **No** for **Manual**.</span></span>
1. <span data-ttu-id="e7e71-289">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-289">On the action pane, select **Save**.</span></span> 
1. <span data-ttu-id="e7e71-290">„Commerce“ ieškos lauke ieškokite **Paskirstymo grafikas**</span><span class="sxs-lookup"><span data-stu-id="e7e71-290">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="e7e71-291">Puslapio **Paskirstymo grafikai** kairiajame naršymo meniu pasirinkite užduotį **1110 visuotinė konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-291">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="e7e71-292">Veiksmų srityje pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-292">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="e7e71-293">Leidėjo URL gavimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-293">Obtain issuer URL</span></span>

<span data-ttu-id="e7e71-294">Norėdami gauti savo tapatybės teikimo įrankio leidėjo URL, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-294">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-295">Sukurkite metaduomenų adreso URL toliau nurodytu formatu, naudodami savo B2C nuomotoją ir strategiją:``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="e7e71-295">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="e7e71-296">Pavyzdys: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="e7e71-296">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="e7e71-297">Į naršyklės adresų juostą įveskite metaduomenų adreso URL.</span><span class="sxs-lookup"><span data-stu-id="e7e71-297">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="e7e71-298">Metaduomenyse kopijuokite tapatybės teikimo įrankio leidėjo URL (**„leidėjo“** reikšmę).</span><span class="sxs-lookup"><span data-stu-id="e7e71-298">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="e7e71-299">Pavyzdys: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="e7e71-299">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="e7e71-300">Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje</span><span class="sxs-lookup"><span data-stu-id="e7e71-300">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="e7e71-301">Kai jūsų „Azure AD B2C“ nuomotojo sąranka baigta, turite sukonfigūruoti B2C nuomininką „Commerce“ svetainių rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-301">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="e7e71-302">Konfigūracijos veiksmai apima B2C programos informacijos iš „Azure“ portalo surinkimą, tos į B2C programos informacijos įvedimą į svetainių daryklę, ir B2C programos susiejimą su jūsų svetaine ir kanalu.</span><span class="sxs-lookup"><span data-stu-id="e7e71-302">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="e7e71-303">Reikiamos programos informacijos surinkimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-303">Collect the required application information</span></span>

<span data-ttu-id="e7e71-304">Norėdami surinkti reikiamą programos informaciją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-304">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-305">„Azure“ portale eikite į **Pagrindinis \> „Azure AD“ B2C – programos**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-305">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="e7e71-306">Pasirinkite programą, tada kairiojoje naršymo srityje pasirinkite **Ypatybes**, kad gautumėte programos informaciją.</span><span class="sxs-lookup"><span data-stu-id="e7e71-306">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="e7e71-307">Laukelyje **Programos ID** patikrinkite B2C programos, sukurtos jūsų B2C nuomotojuje, programos ID.</span><span class="sxs-lookup"><span data-stu-id="e7e71-307">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="e7e71-308">Tai vėliau bus įvesta kaip **Kliento GUID** svetainių rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-308">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="e7e71-309">Dalyje **Atsakymo URL** surinkite atsakymo URL.</span><span class="sxs-lookup"><span data-stu-id="e7e71-309">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="e7e71-310">Eikite į **Pagrindinis \> „Azure AD“ B2C – vartotojo srautus (strategijos)**, tada surinkite kiekvieno vartotojo srauto strategijos pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-310">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="e7e71-311">Toliau pateiktame paveikslėlyje parodytas puslapio **„Azure AD“ B2C – programos** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e7e71-311">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Perėjimas į B2C programą nuomotojuje](./media/B2CImage_19.png)

<span data-ttu-id="e7e71-313">Toliau pateiktame paveikslėlyje parodytas programos puslapio **Ypatybės**, esančio „Azure AD“ B2C, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e7e71-313">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Programos ID kopijavimas iš B2C programos ypatybių](./media/B2CImage_21.png)

<span data-ttu-id="e7e71-315">Toliau pateiktame paveikslėlyje parodytas vartotojo srauto strategijų puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e7e71-315">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Visų B2C strategijos srautų pavadinimų rinkimas](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="e7e71-317">AAD B2C nuomotojo programos informacijos įvedimas „Commerce“</span><span class="sxs-lookup"><span data-stu-id="e7e71-317">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="e7e71-318">Prieš susiedami B2C nuomotoją su savo svetaine (-ėmis), įveskite „Azure AD“ B2C nuomotojo informaciją į „Commerce“ svetainių daryklę.</span><span class="sxs-lookup"><span data-stu-id="e7e71-318">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="e7e71-319">Norėdami įtraukti AAD B2C nuomotojo programos informaciją į „Commerce“, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-319">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-320">Prisijunkite kaip administratorius prie savo aplinkos „Commerce“ svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-320">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="e7e71-321">Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Nuomotojo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-321">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="e7e71-322">Dalyje **Nuomotojo parametrai** pasirinkite **B2C parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-322">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="e7e71-323">Pagrindiniame lange šalia **B2C programos** pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-323">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="e7e71-324">(Jei jūsų nuomotojas yra įtrauktas į B2C programų sąrašą, jį jau įtraukė ir administratorius.</span><span class="sxs-lookup"><span data-stu-id="e7e71-324">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="e7e71-325">Patikrinkite, ar tolesnio 6 veiksmo elementai sutampa su jūsų B2C programa.)</span><span class="sxs-lookup"><span data-stu-id="e7e71-325">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="e7e71-326">Pasirinkite **Įtraukti B2C programą**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-326">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="e7e71-327">Į rodomą formą įveskite toliau nurodytus privalomus elementus naudodami reikšmes iš B2C nuomotojo ir programos.</span><span class="sxs-lookup"><span data-stu-id="e7e71-327">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="e7e71-328">Neprivalomus laukus (be žvaigždutės) galima palikti tuščius.</span><span class="sxs-lookup"><span data-stu-id="e7e71-328">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="e7e71-329">**Programos pavadinimas**: jūsų B2C programos pavadinimas, pavyzdžiui, „Fabrikam B2C“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-329">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="e7e71-330">**Nuomotojo pavadinimas**: jūsų B2C nuomotojo pavadinimas, pavyzdžiui, „Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-330">**Tenant Name**: The name of your B2C Tenant, for example "Fabrikam".</span></span>
    - <span data-ttu-id="e7e71-331">**Pamiršto slaptažodžio strategijos ID**: pamiršto slaptažodžio vartotojo srauto strategijos ID, pavyzdžiui, „B2C_1_PasswordReset“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-331">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="e7e71-332">**Registracijos / prisijungimo strategijos ID**: registracija ir prisijungimas vartotojo srauto strategijos ID, pavyzdžiui, „B2C_1_signup_signin“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-332">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="e7e71-333">**Kliento GUID**: B2C programos ID, pavyzdžiui, „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-333">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="e7e71-334">**Redaguoti profilio strategijos ID**: profilį redaguojančio vartojo srauto strategijos ID, pavyzdžiui, „B2C_1A_ProfileEdit“.</span><span class="sxs-lookup"><span data-stu-id="e7e71-334">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="e7e71-335">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-335">Select **OK**.</span></span> <span data-ttu-id="e7e71-336">Dabar sąraše turėtumėte matyti savo B2C programos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-336">You should now see the name of your B2C application appear in the list.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="e7e71-337">B2C programos susiejimas su svetaine ir kanalu</span><span class="sxs-lookup"><span data-stu-id="e7e71-337">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="e7e71-338">Jei jūsų svetainė jau yra susieta su B2C programa, keičiant į kitą B2C programą, bus pašalintos esamos rekomendacijos, nustatytos vartotojams, kurie jau yra prisiregistravę prie šios aplinkos.</span><span class="sxs-lookup"><span data-stu-id="e7e71-338">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="e7e71-339">Pakeitus, bet kokie kredencialai, susieti su šiuo metu priskirta B2C programa, nebus prieinami vartotojams.</span><span class="sxs-lookup"><span data-stu-id="e7e71-339">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="e7e71-340">Atnaujinkite B2C programą, tik jei kanalo B2C programą nustatote pirmą kartą arba jei ketinate turėti vartotojų su naujais prisijungimo prie šio kanalo kredencialais naudojant naują B2C programą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-340">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="e7e71-341">Būkite atsargūs susiedami kanalus su B2C programomis ir duokite aiškius pavadinimus programoms.</span><span class="sxs-lookup"><span data-stu-id="e7e71-341">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="e7e71-342">Jei kanalas nėra susiejamas su B2C programa atliekant tolesnius veiksmus, vartotojai, prisijungiantys prie tokio kanalo, kad patektų į jūsų svetainę, bus įvesti į B2C programą, rodomą kaip **numatytoji** B2C programų sąraše **Nuomotojo parametrai \> B2C parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-342">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="e7e71-343">Norėdami susieti B2C programą su svetainę ir kanalu, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e7e71-343">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="e7e71-344">Eikite į savo svetainę „Commerce“ svetainių daryklėje.</span><span class="sxs-lookup"><span data-stu-id="e7e71-344">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="e7e71-345">Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-345">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="e7e71-346">Po **Svetainės parametrai** pasirinkite **Kanalai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-346">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="e7e71-347">Pagrindiniame lange, dalyje **Kanalai** pasirinkite savo kanalą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-347">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="e7e71-348">Kanalo ypatybių srityje dešinėje pusėje pasirinkite savo B2C programos pavadinimą iš išskleidžiamojo meniu **Pasirinkti B2C programą**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-348">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="e7e71-349">Pasirinkite **Uždaryti**, tada pasirinkite **Įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-349">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="e7e71-350">Papildoma B2C informacija</span><span class="sxs-lookup"><span data-stu-id="e7e71-350">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="e7e71-351">Kliento perkėlimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-351">Customer migration</span></span>

<span data-ttu-id="e7e71-352">Jei ketinate perkelti kliento įrašus iš ankstesnės tapatybės teikimo įrankio platformos, dirbkite su „Dynamics 365 Commerce“ komanda, kad peržiūrėtumėte savo klientų perkėlimo poreikius.</span><span class="sxs-lookup"><span data-stu-id="e7e71-352">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="e7e71-353">Norėdami gauti daugiau „Azure AD“ B2C dokumentų apie klientų perkėlimą, žr. [Vartotojų perkėlimas į „Azure Active Directory“ B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="e7e71-353">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="e7e71-354">Pasirinktinės strategijos</span><span class="sxs-lookup"><span data-stu-id="e7e71-354">Custom policies</span></span>

<span data-ttu-id="e7e71-355">Norėdami gauti daugiau informacijos apie „Azure AD“ B2C sąveikas ir strategijos srautus be to, kas siūloma standartinėse B2C strategijose, žr. [Pasirinktinės strategijos „Azure Active Directory“ B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="e7e71-355">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="e7e71-356">Antrinis administratorius</span><span class="sxs-lookup"><span data-stu-id="e7e71-356">Secondary admin</span></span>

<span data-ttu-id="e7e71-357">Pasirinktinio antrinio administratoriaus sąskaita gali būti įtraukta į jūsų B2C nuomotojo skyrių **Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="e7e71-357">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="e7e71-358">Tai gali būti tiesioginė sąskaita arba bendroji sąskaita.</span><span class="sxs-lookup"><span data-stu-id="e7e71-358">This can be a direct account or a general account.</span></span> <span data-ttu-id="e7e71-359">Jei reikia bendrinti sąskaitą su komandos ištekliais, galima sukurti bendrąją sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="e7e71-359">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="e7e71-360">Atsižvelgiant į tai, kad „Azure AD“ B2C saugomi duomenys yra jautrūs, bendroji sąskaita turi būti atidžiai stebima pagal jūsų įmonės saugumo praktiką.</span><span class="sxs-lookup"><span data-stu-id="e7e71-360">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7e71-361">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e7e71-361">Additional resources</span></span>

[<span data-ttu-id="e7e71-362">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-362">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e7e71-363">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-363">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e7e71-364">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-364">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e7e71-365">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="e7e71-365">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e7e71-366">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="e7e71-366">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e7e71-367">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-367">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e7e71-368">Vartotojo prisijungimo pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="e7e71-368">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e7e71-369">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-369">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e7e71-370">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-370">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e7e71-371">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="e7e71-371">Enable location-based store detection</span></span>](enable-store-detection.md)