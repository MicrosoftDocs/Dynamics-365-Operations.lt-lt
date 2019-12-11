---
title: Vartotojo registracijos pasirinktinių puslapių sąranka
description: Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 644d937ddd3c219ae869f22d977d2846dffc20e1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697571"
---
# <a name="set-up-custom-pages-for-user-logins"></a><span data-ttu-id="acdd5-103">Vartotojo prisijungimo tinkintų puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="acdd5-103">Set up custom pages for user logins</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="acdd5-104">Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.</span><span class="sxs-lookup"><span data-stu-id="acdd5-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="acdd5-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="acdd5-105">Overview</span></span>

<span data-ttu-id="acdd5-106">Norėdami naudoti tinkintus puslapius, kurie sukurti „Dynamics 365 Commerce“ programoje valdyti vartotojo registravimosi srautus, turite nustatyti „Azure AD“ strategijas, kurios bus nurodytos „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="acdd5-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="acdd5-107">Galite konfigūruoti „Prisijungti ir įeiti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“ „Azure AD“ B2C strategijas naudodami „Azure AD“ B2C programą.</span><span class="sxs-lookup"><span data-stu-id="acdd5-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="acdd5-108">„Azure AD“ B2C nuomotojo ir strategijos pavadinimai gali būti nurodyti rengimo proceso metu, kuris vykdomas „Commerce“ aplinkai naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="acdd5-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="acdd5-109">Tinkintą „Commerce“ puslapį galima sukurti naudojant registravimosi, prisijungimo, paskyros profilio redagavimo arba slaptažodžio nustatymo iš naujo modulį.</span><span class="sxs-lookup"><span data-stu-id="acdd5-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="acdd5-110">Puslapio URL, kurie publikuojami šiems tinkintiems puslapiams, turėtų būti nurodyti „Azure AD“ B2C strategijų konfigūracijose, „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="acdd5-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="acdd5-111">B2C strategijų sąranka</span><span class="sxs-lookup"><span data-stu-id="acdd5-111">Set up B2C policies</span></span>

<span data-ttu-id="acdd5-112">Nustatę savo „Azure AD“ B2C nuomotoją ir susieję jį su savo „Commerce“ aplinka, eikite į **„Azure AD“ B2C** puslapį, esantį „Azure“ portale, ir meniu, dalyje **Strategijos**, pasirinkite **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Meniu komanda Vartotojo srautai (strategijos)](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="acdd5-114">Dabar galite konfigūruoti vartotojų prisijungimo srautus „Registruotis ir prisijungti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“.</span><span class="sxs-lookup"><span data-stu-id="acdd5-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="acdd5-115">Konfigūruoti strategiją „Registruotis ir prisijungti“</span><span class="sxs-lookup"><span data-stu-id="acdd5-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="acdd5-116">Norėdami sukonfigūruoti strategiją „Registruotis ir prisijungti“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acdd5-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="acdd5-117">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Registruotis ir prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="acdd5-118">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="acdd5-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="acdd5-119">Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje.</span><span class="sxs-lookup"><span data-stu-id="acdd5-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="acdd5-120">Turi būti pažymėta bent **El. pašto registracija**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="acdd5-121">Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas**, **Vardas**ir **Pavardė**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="acdd5-122">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Pasirinkti atributai ir pareiškimai](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="acdd5-124">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="acdd5-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="acdd5-125">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="acdd5-126">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Naujos strategijos ypatybių puslapis](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="acdd5-128">Strategijos pavadinimas bus išsamiai nurodytas „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="acdd5-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="acdd5-129">(**B2C\_1\_** priešvardis bus įtrauktas į nuorodą.) Sukūrus strategiją, strategijų pervardyti negalima.</span><span class="sxs-lookup"><span data-stu-id="acdd5-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="acdd5-130">Jei keičiate esamą „Commerce“ aplinkos strategiją, galite panaikinti pradinę strategiją ir sukurti naują strategiją, turinčią tokį patį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="acdd5-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="acdd5-131">Taip pat, jei aplinka jau parengta, galite pateikti naują strategijos pavadinimą naudodami paslaugos užklausą.</span><span class="sxs-lookup"><span data-stu-id="acdd5-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="acdd5-132">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="acdd5-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="acdd5-133">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="acdd5-134">„Profilių redagavimo“ strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="acdd5-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="acdd5-135">Norėdami sukonfigūruoti „Profilio redagavimo“ strategiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acdd5-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="acdd5-136">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Profilio redagavimas**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="acdd5-137">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="acdd5-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="acdd5-138">Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje.</span><span class="sxs-lookup"><span data-stu-id="acdd5-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="acdd5-139">Turi būti pažymėta bent **Prisijungimas prie vietinės paskyros**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="acdd5-140">Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas** ir **Pavardė**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="acdd5-141">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="acdd5-142">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="acdd5-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="acdd5-143">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="acdd5-144">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="acdd5-145">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="acdd5-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="acdd5-146">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="acdd5-147">„Slaptažodžio nustatymo iš naujo“ strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="acdd5-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="acdd5-148">Norėdami sukonfigūruoti „Slaptažodžio nustatymo iš naujo“ strategiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acdd5-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="acdd5-149">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Peržiūra** pasirinkite strategiją **Slaptažodžio nustatymas iš naujo v1.1**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Slaptažodžio nustatymo iš naujo v1.1 strategija, pasirinkta skirtuke Peržiūra](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="acdd5-151">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="acdd5-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="acdd5-152">Skyriuje **Tapapybės teikimo įrankis** pasirinkite **Iš naujo nustatyti slaptažodį naudojant el. pašto adresą**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="acdd5-153">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresas**, **Vardas**, **Pavardė**ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Pasirinkti pareiškimai](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="acdd5-155">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="acdd5-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="acdd5-156">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="acdd5-157">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="acdd5-158">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="acdd5-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="acdd5-159">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="acdd5-160">Tinkintų puslapių kūrimas</span><span class="sxs-lookup"><span data-stu-id="acdd5-160">Build the custom pages</span></span>

<span data-ttu-id="acdd5-161">Norėdami sukurti tinkintus puslapius, skirtus valdyti vartotojų prisijungimus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acdd5-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="acdd5-162">„Commerce“ kūrimo įrankiuose eikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="acdd5-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="acdd5-163">Sukurkite šiuos penkis šablonus ir penkis puslapius:</span><span class="sxs-lookup"><span data-stu-id="acdd5-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="acdd5-164">**Prisijungimo**šabloną ir puslapį, kuriuose naudojamas prisijungimo modulis.</span><span class="sxs-lookup"><span data-stu-id="acdd5-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="acdd5-165">**Registravimosi**šabloną ir puslapė, kuriuose naudojamas registravimosi modulis.</span><span class="sxs-lookup"><span data-stu-id="acdd5-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="acdd5-166">**Slaptažodžio nustatymo iš naujo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo modulis.</span><span class="sxs-lookup"><span data-stu-id="acdd5-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="acdd5-167">**Slaptažodžio nustatymo iš naujo tikrinimo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo tikrinimo modulis.</span><span class="sxs-lookup"><span data-stu-id="acdd5-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="acdd5-168">**Profilio redagavimo** šabloną ir puslapį, kuriuose naudojamas paskyros profilio redagavimo modulis</span><span class="sxs-lookup"><span data-stu-id="acdd5-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="acdd5-169">Kurdami puslapius vadovaukitės šiais nurodymais:</span><span class="sxs-lookup"><span data-stu-id="acdd5-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="acdd5-170">Kiekviename puslapyje ar modulyje naudokite maketą ir stilių, kurie geriausiai atitinka jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="acdd5-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="acdd5-171">Publikuokite visus puslapius ir URL, kurie turi būti naudojami „Azure AD“ B2C sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="acdd5-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="acdd5-172">Po to, kai puslapiai ir URL publikuojami, rinkite URL, kurie turi būti naudojami „Azure AD“ B2C"strategijos konfigūracijoms.</span><span class="sxs-lookup"><span data-stu-id="acdd5-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="acdd5-173">Povardis **?preloadscripts=true** bus įtrauktas į kiekvieną naudojamą URL.</span><span class="sxs-lookup"><span data-stu-id="acdd5-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="acdd5-174">Nenaudokite universalių antraščių ir poraščių, kuriose yra santykinių saitų.</span><span class="sxs-lookup"><span data-stu-id="acdd5-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="acdd5-175">Kadangi šie puslapiai bus nuomojami „Azure AD“ B2C domene, juos naudojant, visiems saitams reikia naudoti tik absoliučias URL.</span><span class="sxs-lookup"><span data-stu-id="acdd5-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="acdd5-176">„Azure AD“ B2C strategijų konfigūravimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="acdd5-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="acdd5-177">„Azure“ portale grįžkite į **„Azure AD“ B2C** puslapį ir meniu dalyje, srityje **Strategijos** pasirinkite **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="acdd5-178">„Registruotis ir prisijungti“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="acdd5-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="acdd5-179">Atnaujinti strategiją „Registruotis ir prisijungti“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acdd5-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="acdd5-180">Jūsų anksčiau sukonfigūruotoje strategijoje **Registruotis ir prisijungti**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="acdd5-181">Pasirinkite maketą **Vieningasis registracijos ir prisijungimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="acdd5-182">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="acdd5-183">Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL.</span><span class="sxs-lookup"><span data-stu-id="acdd5-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="acdd5-184">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="acdd5-185">Pavyzdžiui, įveskite **www.\<mano domenas\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-185">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="acdd5-186">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="acdd5-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="acdd5-187">Pasirinkite maketą **Registravimosi į vietinę paskyrą puslapis**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="acdd5-188">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="acdd5-189">Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL.</span><span class="sxs-lookup"><span data-stu-id="acdd5-189">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="acdd5-190">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="acdd5-191">Pavyzdžiui, įveskite **www.\<mano domenas\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-191">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="acdd5-192">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="acdd5-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="acdd5-193">Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="acdd5-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="acdd5-194">Atributams **El. pašto adresas**, **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Reikalingas patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="acdd5-195">Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Registravimosi prie vietinės paskyros puslapio strategijos konfigūravimas](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="acdd5-197">„Profilio redagavimas“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="acdd5-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="acdd5-198">Atnaujinti strategiją „Profilio redagavimas“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acdd5-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="acdd5-199">Jūsų anksčiau sukonfigūruotoje strategijoje **Profilio redagavimas**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="acdd5-200">Pasirinkite maketą **Profilio redagavimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="acdd5-201">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="acdd5-202">Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL.</span><span class="sxs-lookup"><span data-stu-id="acdd5-202">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="acdd5-203">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="acdd5-204">Pavyzdžiui, įveskite **www.\<mano domenas\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-204">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="acdd5-205">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="acdd5-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="acdd5-206">Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="acdd5-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="acdd5-207">Atributams **El. pašto adresas**, **Vardas** pasirinkite **Ne** lauke **Reikalingas tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="acdd5-208">Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="acdd5-209">„Slaptažodžio nustatymo iš naujo“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="acdd5-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="acdd5-210">Atnaujinti strategiją „Slaptažodžio nustatymas iš naujo“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acdd5-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="acdd5-211">Jūsų anksčiau sukonfigūruotoje strategijoje **Slaptažodžio nustatymas iš naujo**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="acdd5-212">Pasirinkite maketą **Naujo slaptažodžio puslapis**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="acdd5-213">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="acdd5-214">Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL.</span><span class="sxs-lookup"><span data-stu-id="acdd5-214">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="acdd5-215">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="acdd5-216">Pavyzdžiui, įveskite **www.\<mano domenas\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-216">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="acdd5-217">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="acdd5-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="acdd5-218">Pasirinkite maketą **Paskyros patvirtinimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="acdd5-219">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="acdd5-220">Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL.</span><span class="sxs-lookup"><span data-stu-id="acdd5-220">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="acdd5-221">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="acdd5-222">Pavyzdžiui, įveskite **www.\<mano domenas\>.com/sign-in?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-222">For example, enter **www.\<my domain\>.com/sign-in?preloadscripts=true**.</span></span>
1. <span data-ttu-id="acdd5-223">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="acdd5-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="acdd5-224">Etikečių ir aprašų numatytųjų teksto eilučių tinkinimas</span><span class="sxs-lookup"><span data-stu-id="acdd5-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="acdd5-225">Darbo pradžios rinkinyje prisijungimo moduliai yra iš anksto užpildyti etikečių ir aprašų numatytomis teksto eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="acdd5-225">In the starter kit, sign in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="acdd5-226">Galite pritaikyti šias eilutes programinės įrangos kūrimo rinkinyje (SDK), atnaujindami reikšmes, esančias prisijungimo modulio global.json faile.</span><span class="sxs-lookup"><span data-stu-id="acdd5-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="acdd5-227">Pavyzdžiui, numatytasis pamiršto slaptažodžio saito tekstas **Pamiršote slaptažodį?**.</span><span class="sxs-lookup"><span data-stu-id="acdd5-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="acdd5-228">Šiame prisijungimo puslapyje pateikiamas šis numatytasis tekstas.</span><span class="sxs-lookup"><span data-stu-id="acdd5-228">The following shows this default text on the sign-in page.</span></span>

![Numatytasis pamiršto slaptažodžio saito, esančio prisijungimo puslapyje, tekstas](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="acdd5-230">Tačiau darbo pradžios rinkinio, esančio prisijungimo modulyje, global.json faile galite redaguoti tekstą į **Pamiršai slaptažodį?**, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="acdd5-230">However, in the global.json file for the starter kit sign in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Atnaujintas saito tekstas prisijungimo modulio global.json faile](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="acdd5-232">Atnaujinus global.json failą ir publikavus keitimus, naujas saito tekstas atsiranda ir „Commerce“ ir tiesioginio registravimosi puslapio prisijungimo modulyje.</span><span class="sxs-lookup"><span data-stu-id="acdd5-232">After you update the global.json file and publish your changes, the new link text appears in the sign in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="acdd5-233">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="acdd5-233">Additional resources</span></span>

[<span data-ttu-id="acdd5-234">Interneto parduotuvės peržiūra</span><span class="sxs-lookup"><span data-stu-id="acdd5-234">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="acdd5-235">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="acdd5-235">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="acdd5-236">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="acdd5-236">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="acdd5-237">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="acdd5-237">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="acdd5-238">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="acdd5-238">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="acdd5-239">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="acdd5-239">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="acdd5-240">Įgalinti parduotuvės nustatymą pagal vietą</span><span class="sxs-lookup"><span data-stu-id="acdd5-240">Enable location-based store detection</span></span>](enable-store-detection.md)
