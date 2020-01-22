---
title: Vartotojo registracijos pasirinktinių puslapių sąranka
description: Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.
author: brianshook
manager: annbe
ms.date: 12/05/2019
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
ms.openlocfilehash: 20bfacbc2374003814e12e7737644d118d404cc0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945564"
---
# <a name="set-up-custom-pages-for-user-logins"></a><span data-ttu-id="e6cc2-103">Vartotojo prisijungimo tinkintų puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="e6cc2-103">Set up custom pages for user logins</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e6cc2-104">Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="e6cc2-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="e6cc2-105">Overview</span></span>

<span data-ttu-id="e6cc2-106">Norėdami naudoti tinkintus puslapius, kurie sukurti „Dynamics 365 Commerce“ programoje valdyti vartotojo registravimosi srautus, turite nustatyti „Azure AD“ strategijas, kurios bus nurodytos „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="e6cc2-107">Galite konfigūruoti „Prisijungti ir įeiti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“ „Azure AD“ B2C strategijas naudodami „Azure AD“ B2C programą.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="e6cc2-108">„Azure AD“ B2C nuomotojo ir strategijos pavadinimai gali būti nurodyti rengimo proceso metu, kuris vykdomas „Commerce“ aplinkai naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="e6cc2-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="e6cc2-109">Tinkintą „Commerce“ puslapį galima sukurti naudojant registravimosi, prisijungimo, paskyros profilio redagavimo arba slaptažodžio nustatymo iš naujo modulį.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="e6cc2-110">Puslapio URL, kurie publikuojami šiems tinkintiems puslapiams, turėtų būti nurodyti „Azure AD“ B2C strategijų konfigūracijose, „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="e6cc2-111">B2C strategijų sąranka</span><span class="sxs-lookup"><span data-stu-id="e6cc2-111">Set up B2C policies</span></span>

<span data-ttu-id="e6cc2-112">Nustatę savo „Azure AD“ B2C nuomotoją ir susieję jį su savo „Commerce“ aplinka, eikite į **„Azure AD“ B2C** puslapį, esantį „Azure“ portale, ir meniu, dalyje **Strategijos**, pasirinkite **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Meniu komanda Vartotojo srautai (strategijos)](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="e6cc2-114">Dabar galite konfigūruoti vartotojų prisijungimo srautus „Registruotis ir prisijungti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="e6cc2-115">Konfigūruoti strategiją „Registruotis ir prisijungti“</span><span class="sxs-lookup"><span data-stu-id="e6cc2-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="e6cc2-116">Norėdami sukonfigūruoti strategiją „Registruotis ir prisijungti“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="e6cc2-117">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Registruotis ir prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="e6cc2-118">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="e6cc2-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="e6cc2-119">Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="e6cc2-120">Turi būti pažymėta bent **El. pašto registracija**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="e6cc2-121">Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas**, **Vardas**ir **Pavardė**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="e6cc2-122">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Pasirinkti atributai ir pareiškimai](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="e6cc2-124">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e6cc2-125">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e6cc2-126">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Naujos strategijos ypatybių puslapis](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="e6cc2-128">Strategijos pavadinimas bus išsamiai nurodytas „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="e6cc2-129">(**B2C\_1\_** priešvardis bus įtrauktas į nuorodą.) Sukūrus strategiją, strategijų pervardyti negalima.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="e6cc2-130">Jei keičiate esamą „Commerce“ aplinkos strategiją, galite panaikinti pradinę strategiją ir sukurti naują strategiją, turinčią tokį patį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="e6cc2-131">Taip pat, jei aplinka jau parengta, galite pateikti naują strategijos pavadinimą naudodami paslaugos užklausą.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="e6cc2-132">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e6cc2-133">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="e6cc2-134">„Profilių redagavimo“ strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="e6cc2-135">Norėdami sukonfigūruoti „Profilio redagavimo“ strategiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="e6cc2-136">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Profilio redagavimas**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="e6cc2-137">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="e6cc2-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="e6cc2-138">Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="e6cc2-139">Turi būti pažymėta bent **Prisijungimas prie vietinės paskyros**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="e6cc2-140">Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas** ir **Pavardė**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="e6cc2-141">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="e6cc2-142">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e6cc2-143">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e6cc2-144">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="e6cc2-145">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e6cc2-146">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="e6cc2-147">„Slaptažodžio nustatymo iš naujo“ strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="e6cc2-148">Norėdami sukonfigūruoti „Slaptažodžio nustatymo iš naujo“ strategiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="e6cc2-149">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Peržiūra** pasirinkite strategiją **Slaptažodžio nustatymas iš naujo v1.1**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Slaptažodžio nustatymo iš naujo v1.1 strategija, pasirinkta skirtuke Peržiūra](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="e6cc2-151">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="e6cc2-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="e6cc2-152">Skyriuje **Tapapybės teikimo įrankis** pasirinkite **Iš naujo nustatyti slaptažodį naudojant el. pašto adresą**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="e6cc2-153">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresas**, **Vardas**, **Pavardė**ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Pasirinkti pareiškimai](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="e6cc2-155">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="e6cc2-156">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="e6cc2-157">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="e6cc2-158">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="e6cc2-159">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="e6cc2-160">Tinkintų puslapių kūrimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-160">Build the custom pages</span></span>

<span data-ttu-id="e6cc2-161">Norėdami sukurti tinkintus puslapius, skirtus valdyti vartotojų prisijungimus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="e6cc2-162">„Commerce“ kūrimo įrankiuose eikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="e6cc2-163">Sukurkite šiuos penkis šablonus ir penkis puslapius:</span><span class="sxs-lookup"><span data-stu-id="e6cc2-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="e6cc2-164">**Prisijungimo**šabloną ir puslapį, kuriuose naudojamas prisijungimo modulis.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="e6cc2-165">**Registravimosi**šabloną ir puslapė, kuriuose naudojamas registravimosi modulis.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="e6cc2-166">**Slaptažodžio nustatymo iš naujo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo modulis.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="e6cc2-167">**Slaptažodžio nustatymo iš naujo tikrinimo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo tikrinimo modulis.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="e6cc2-168">**Profilio redagavimo** šabloną ir puslapį, kuriuose naudojamas paskyros profilio redagavimo modulis</span><span class="sxs-lookup"><span data-stu-id="e6cc2-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="e6cc2-169">Kurdami puslapius vadovaukitės šiais nurodymais:</span><span class="sxs-lookup"><span data-stu-id="e6cc2-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="e6cc2-170">Kiekviename puslapyje ar modulyje naudokite maketą ir stilių, kurie geriausiai atitinka jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="e6cc2-171">Publikuokite visus puslapius ir URL, kurie turi būti naudojami „Azure AD“ B2C sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="e6cc2-172">Po to, kai puslapiai ir URL publikuojami, rinkite URL, kurie turi būti naudojami „Azure AD“ B2C"strategijos konfigūracijoms.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="e6cc2-173">Povardis **?preloadscripts=true** bus įtrauktas į kiekvieną naudojamą URL.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e6cc2-174">Nenaudokite universalių antraščių ir poraščių, kuriose yra santykinių saitų.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="e6cc2-175">Kadangi šie puslapiai bus nuomojami „Azure AD“ B2C domene, juos naudojant, visiems saitams reikia naudoti tik absoliučias URL.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="e6cc2-176">„Azure AD“ B2C strategijų konfigūravimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="e6cc2-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="e6cc2-177">„Azure“ portale grįžkite į **„Azure AD“ B2C** puslapį ir meniu dalyje, srityje **Strategijos** pasirinkite **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="e6cc2-178">„Registruotis ir prisijungti“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="e6cc2-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="e6cc2-179">Atnaujinti strategiją „Registruotis ir prisijungti“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e6cc2-180">Jūsų anksčiau sukonfigūruotoje strategijoje **Registruotis ir prisijungti**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e6cc2-181">Pasirinkite maketą **Vieningasis registracijos ir prisijungimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="e6cc2-182">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e6cc2-183">Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="e6cc2-184">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e6cc2-185">Pavyzdžiui, įveskite ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e6cc2-186">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="e6cc2-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e6cc2-187">Pasirinkite maketą **Registravimosi į vietinę paskyrą puslapis**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="e6cc2-188">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e6cc2-189">Lauke **Pasirinktinis puslapio URI** įveskite visą registracijos URL.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="e6cc2-190">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e6cc2-191">Pavyzdžiui, įveskite ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e6cc2-192">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="e6cc2-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e6cc2-193">Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="e6cc2-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="e6cc2-194">Atributams **El. pašto adresas**, **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Reikalingas patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="e6cc2-195">Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Registravimosi prie vietinės paskyros puslapio strategijos konfigūravimas](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="e6cc2-197">„Profilio redagavimas“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="e6cc2-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="e6cc2-198">Atnaujinti strategiją „Profilio redagavimas“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e6cc2-199">Jūsų anksčiau sukonfigūruotoje strategijoje **Profilio redagavimas**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e6cc2-200">Pasirinkite maketą **Profilio redagavimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="e6cc2-201">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e6cc2-202">Lauke **Pasirinktinis puslapio URI** įveskite visą profilio redagavimo URL.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="e6cc2-203">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e6cc2-204">Pavyzdžiui, įveskite ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e6cc2-205">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="e6cc2-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e6cc2-206">Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="e6cc2-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="e6cc2-207">Atributams **El. pašto adresas**, **Vardas** pasirinkite **Ne** lauke **Reikalingas tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="e6cc2-208">Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="e6cc2-209">„Slaptažodžio nustatymo iš naujo“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="e6cc2-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="e6cc2-210">Atnaujinti strategiją „Slaptažodžio nustatymas iš naujo“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="e6cc2-211">Jūsų anksčiau sukonfigūruotoje strategijoje **Slaptažodžio nustatymas iš naujo**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="e6cc2-212">Pasirinkite maketą **Naujo slaptažodžio puslapis**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="e6cc2-213">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e6cc2-214">Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo URL.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="e6cc2-215">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e6cc2-216">Pavyzdžiui, įveskite ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e6cc2-217">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="e6cc2-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="e6cc2-218">Pasirinkite maketą **Paskyros patvirtinimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="e6cc2-219">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="e6cc2-220">Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo patikros URL.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="e6cc2-221">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="e6cc2-222">Pavyzdžiui, įveskite ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="e6cc2-223">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="e6cc2-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="e6cc2-224">Etikečių ir aprašų numatytųjų teksto eilučių tinkinimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="e6cc2-225">Darbo pradžios rinkinyje prisijungimo moduliai yra iš anksto užpildyti etikečių ir aprašų numatytomis teksto eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-225">In the starter kit, sign in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="e6cc2-226">Galite pritaikyti šias eilutes programinės įrangos kūrimo rinkinyje (SDK), atnaujindami reikšmes, esančias prisijungimo modulio global.json faile.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="e6cc2-227">Pavyzdžiui, numatytasis pamiršto slaptažodžio saito tekstas **Pamiršote slaptažodį?**.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="e6cc2-228">Šiame prisijungimo puslapyje pateikiamas šis numatytasis tekstas.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-228">The following shows this default text on the sign-in page.</span></span>

![Numatytasis pamiršto slaptažodžio saito, esančio prisijungimo puslapyje, tekstas](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="e6cc2-230">Tačiau darbo pradžios rinkinio, esančio prisijungimo modulyje, global.json faile galite redaguoti tekstą į **Pamiršai slaptažodį?**, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-230">However, in the global.json file for the starter kit sign in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Atnaujintas saito tekstas prisijungimo modulio global.json faile](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="e6cc2-232">Atnaujinus global.json failą ir publikavus keitimus, naujas saito tekstas atsiranda ir „Commerce“ ir tiesioginio registravimosi puslapio prisijungimo modulyje.</span><span class="sxs-lookup"><span data-stu-id="e6cc2-232">After you update the global.json file and publish your changes, the new link text appears in the sign in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6cc2-233">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e6cc2-233">Additional resources</span></span>

[<span data-ttu-id="e6cc2-234">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e6cc2-235">Naujos e. prekybos svetainės visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-235">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e6cc2-236">E. prekybos svetainės kūrimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-236">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e6cc2-237">Interneto svetainės susiejimas su kanalu</span><span class="sxs-lookup"><span data-stu-id="e6cc2-237">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e6cc2-238">„Robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e6cc2-239">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-239">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e6cc2-240">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="e6cc2-240">Enable location-based store detection</span></span>](enable-store-detection.md)
