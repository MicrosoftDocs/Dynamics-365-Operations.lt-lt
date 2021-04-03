---
title: Vartotojo registracijos pasirinktinių puslapių sąranka
description: Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477953"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="374e5-103">Vartotojo registracijos pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="374e5-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="374e5-104">Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.</span><span class="sxs-lookup"><span data-stu-id="374e5-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="374e5-105">Norėdami naudoti tinkintus puslapius, kurie sukurti „Dynamics 365 Commerce“ programoje valdyti vartotojo registravimosi srautus, turite nustatyti „Azure AD“ strategijas, kurios bus nurodytos „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="374e5-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="374e5-106">Galite konfigūruoti „Prisijungti ir įeiti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“ „Azure AD“ B2C strategijas naudodami „Azure AD“ B2C programą.</span><span class="sxs-lookup"><span data-stu-id="374e5-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="374e5-107">„Azure AD“ B2C nuomotojo ir strategijos pavadinimai gali būti nurodyti rengimo proceso metu, kuris vykdomas „Commerce“ aplinkai naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="374e5-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="374e5-108">Tinkintą „Commerce“ puslapį galima sukurti naudojant registravimosi, prisijungimo, paskyros profilio redagavimo arba slaptažodžio nustatymo iš naujo modulį.</span><span class="sxs-lookup"><span data-stu-id="374e5-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="374e5-109">Puslapio URL, kurie publikuojami šiems tinkintiems puslapiams, turėtų būti nurodyti „Azure AD“ B2C strategijų konfigūracijose, „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="374e5-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="374e5-110">B2C strategijų sąranka</span><span class="sxs-lookup"><span data-stu-id="374e5-110">Set up B2C policies</span></span>

<span data-ttu-id="374e5-111">Nustatę savo „Azure AD“ B2C nuomotoją ir susieję jį su savo „Commerce“ aplinka, eikite į **„Azure AD“ B2C** puslapį, esantį „Azure“ portale, ir meniu, dalyje **Strategijos**, pasirinkite **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="374e5-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Meniu komanda Vartotojo srautai (strategijos)](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="374e5-113">Dabar galite konfigūruoti vartotojų prisijungimo srautus „Registruotis ir prisijungti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“.</span><span class="sxs-lookup"><span data-stu-id="374e5-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="374e5-114">Konfigūruoti strategiją „Registruotis ir prisijungti“</span><span class="sxs-lookup"><span data-stu-id="374e5-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="374e5-115">Norėdami sukonfigūruoti strategiją „Registruotis ir prisijungti“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="374e5-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="374e5-116">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Registruotis ir prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="374e5-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="374e5-117">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="374e5-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="374e5-118">Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje.</span><span class="sxs-lookup"><span data-stu-id="374e5-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="374e5-119">Turi būti pažymėta bent **El. pašto registracija**.</span><span class="sxs-lookup"><span data-stu-id="374e5-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="374e5-120">Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas**, **Vardas** ir **Pavardė**.</span><span class="sxs-lookup"><span data-stu-id="374e5-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="374e5-121">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="374e5-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Pasirinkti atributai ir pareiškimai](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="374e5-123">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="374e5-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="374e5-124">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="374e5-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="374e5-125">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="374e5-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Naujos strategijos ypatybių puslapis](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="374e5-127">Strategijos pavadinimas bus išsamiai nurodytas „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="374e5-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="374e5-128">(**B2C\_1\_** priešvardis bus įtrauktas į nuorodą.) Sukūrus strategiją, strategijų pervardyti negalima.</span><span class="sxs-lookup"><span data-stu-id="374e5-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="374e5-129">Jei keičiate esamą „Commerce“ aplinkos strategiją, galite panaikinti pradinę strategiją ir sukurti naują strategiją, turinčią tokį patį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="374e5-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="374e5-130">Taip pat, jei aplinka jau parengta, galite pateikti naują strategijos pavadinimą naudodami paslaugos užklausą.</span><span class="sxs-lookup"><span data-stu-id="374e5-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="374e5-131">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="374e5-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="374e5-132">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="374e5-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="374e5-133">„Profilių redagavimo“ strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="374e5-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="374e5-134">Norėdami sukonfigūruoti „Profilio redagavimo“ strategiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="374e5-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="374e5-135">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Profilio redagavimas**.</span><span class="sxs-lookup"><span data-stu-id="374e5-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="374e5-136">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="374e5-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="374e5-137">Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje.</span><span class="sxs-lookup"><span data-stu-id="374e5-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="374e5-138">Turi būti pažymėta bent **Prisijungimas prie vietinės paskyros**.</span><span class="sxs-lookup"><span data-stu-id="374e5-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="374e5-139">Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas** ir **Pavardė**.</span><span class="sxs-lookup"><span data-stu-id="374e5-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="374e5-140">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="374e5-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="374e5-141">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="374e5-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="374e5-142">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="374e5-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="374e5-143">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="374e5-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="374e5-144">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="374e5-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="374e5-145">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="374e5-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="374e5-146">„Slaptažodžio nustatymo iš naujo“ strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="374e5-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="374e5-147">Norėdami sukonfigūruoti „Slaptažodžio nustatymo iš naujo“ strategiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="374e5-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="374e5-148">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Peržiūra** pasirinkite strategiją **Slaptažodžio nustatymas iš naujo v1.1**.</span><span class="sxs-lookup"><span data-stu-id="374e5-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Slaptažodžio nustatymo iš naujo v1.1 strategija, pasirinkta skirtuke Peržiūra](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="374e5-150">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="374e5-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="374e5-151">Skyriuje **Tapapybės teikimo įrankis** pasirinkite **Iš naujo nustatyti slaptažodį naudojant el. pašto adresą**.</span><span class="sxs-lookup"><span data-stu-id="374e5-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="374e5-152">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresas**, **Vardas**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="374e5-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Pasirinkti pareiškimai](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="374e5-154">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="374e5-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="374e5-155">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="374e5-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="374e5-156">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="374e5-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="374e5-157">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="374e5-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="374e5-158">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="374e5-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="374e5-159">Tinkintų puslapių kūrimas</span><span class="sxs-lookup"><span data-stu-id="374e5-159">Build the custom pages</span></span>

<span data-ttu-id="374e5-160">Norėdami sukurti tinkintus puslapius, skirtus valdyti vartotojų prisijungimus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="374e5-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="374e5-161">„Commerce“ kūrimo įrankiuose eikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="374e5-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="374e5-162">Sukurkite šiuos penkis šablonus ir penkis puslapius:</span><span class="sxs-lookup"><span data-stu-id="374e5-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="374e5-163">**Prisijungimo** šabloną ir puslapį, kuriuose naudojamas prisijungimo modulis.</span><span class="sxs-lookup"><span data-stu-id="374e5-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="374e5-164">**Registravimosi** šabloną ir puslapė, kuriuose naudojamas registravimosi modulis.</span><span class="sxs-lookup"><span data-stu-id="374e5-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="374e5-165">**Slaptažodžio nustatymo iš naujo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo modulis.</span><span class="sxs-lookup"><span data-stu-id="374e5-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="374e5-166">**Slaptažodžio nustatymo iš naujo tikrinimo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo tikrinimo modulis.</span><span class="sxs-lookup"><span data-stu-id="374e5-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="374e5-167">**Profilio redagavimo** šabloną ir puslapį, kuriuose naudojamas paskyros profilio redagavimo modulis</span><span class="sxs-lookup"><span data-stu-id="374e5-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="374e5-168">Kurdami puslapius vadovaukitės šiais nurodymais:</span><span class="sxs-lookup"><span data-stu-id="374e5-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="374e5-169">Kiekviename puslapyje ar modulyje naudokite maketą ir stilių, kurie geriausiai atitinka jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="374e5-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="374e5-170">Publikuokite visus puslapius ir URL, kurie turi būti naudojami „Azure AD“ B2C sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="374e5-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="374e5-171">Po to, kai puslapiai ir URL publikuojami, rinkite URL, kurie turi būti naudojami „Azure AD“ B2C"strategijos konfigūracijoms.</span><span class="sxs-lookup"><span data-stu-id="374e5-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="374e5-172">Povardis **?preloadscripts=true** bus įtrauktas į kiekvieną naudojamą URL.</span><span class="sxs-lookup"><span data-stu-id="374e5-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="374e5-173">Nenaudokite universalių antraščių ir poraščių, kuriose yra santykinių saitų.</span><span class="sxs-lookup"><span data-stu-id="374e5-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="374e5-174">Kadangi šie puslapiai bus nuomojami „Azure AD“ B2C domene, juos naudojant, visiems saitams reikia naudoti tik absoliučias URL.</span><span class="sxs-lookup"><span data-stu-id="374e5-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="374e5-175">„Azure AD“ B2C strategijų konfigūravimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="374e5-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="374e5-176">„Azure“ portale grįžkite į **„Azure AD“ B2C** puslapį ir meniu dalyje, srityje **Strategijos** pasirinkite **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="374e5-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="374e5-177">„Registruotis ir prisijungti“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="374e5-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="374e5-178">Atnaujinti strategiją „Registruotis ir prisijungti“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="374e5-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="374e5-179">Jūsų anksčiau sukonfigūruotoje strategijoje **Registruotis ir prisijungti**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="374e5-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="374e5-180">Pasirinkite maketą **Vieningasis registracijos ir prisijungimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="374e5-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="374e5-181">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="374e5-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="374e5-182">Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL.</span><span class="sxs-lookup"><span data-stu-id="374e5-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="374e5-183">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="374e5-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="374e5-184">Pavyzdžiui, įveskite ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="374e5-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="374e5-185">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="374e5-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="374e5-186">Pasirinkite maketą **Registravimosi į vietinę paskyrą puslapis**.</span><span class="sxs-lookup"><span data-stu-id="374e5-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="374e5-187">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="374e5-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="374e5-188">Lauke **Pasirinktinis puslapio URI** įveskite visą registracijos URL.</span><span class="sxs-lookup"><span data-stu-id="374e5-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="374e5-189">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="374e5-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="374e5-190">Pavyzdžiui, įveskite ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="374e5-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="374e5-191">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="374e5-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="374e5-192">Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="374e5-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="374e5-193">Atributams **El. pašto adresas**, **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Reikalingas patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="374e5-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="374e5-194">Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="374e5-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Registravimosi prie vietinės paskyros puslapio strategijos konfigūravimas](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="374e5-196">„Profilio redagavimas“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="374e5-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="374e5-197">Atnaujinti strategiją „Profilio redagavimas“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="374e5-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="374e5-198">Jūsų anksčiau sukonfigūruotoje strategijoje **Profilio redagavimas**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="374e5-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="374e5-199">Pasirinkite maketą **Profilio redagavimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="374e5-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="374e5-200">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="374e5-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="374e5-201">Lauke **Pasirinktinis puslapio URI** įveskite visą profilio redagavimo URL.</span><span class="sxs-lookup"><span data-stu-id="374e5-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="374e5-202">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="374e5-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="374e5-203">Pavyzdžiui, įveskite ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="374e5-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="374e5-204">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="374e5-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="374e5-205">Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="374e5-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="374e5-206">Atributams **El. pašto adresas**, **Vardas** pasirinkite **Ne** lauke **Reikalingas tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="374e5-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="374e5-207">Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="374e5-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="374e5-208">„Slaptažodžio nustatymo iš naujo“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="374e5-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="374e5-209">Atnaujinti strategiją „Slaptažodžio nustatymas iš naujo“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="374e5-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="374e5-210">Jūsų anksčiau sukonfigūruotoje strategijoje **Slaptažodžio nustatymas iš naujo**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="374e5-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="374e5-211">Pasirinkite maketą **Naujo slaptažodžio puslapis**.</span><span class="sxs-lookup"><span data-stu-id="374e5-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="374e5-212">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="374e5-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="374e5-213">Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo URL.</span><span class="sxs-lookup"><span data-stu-id="374e5-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="374e5-214">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="374e5-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="374e5-215">Pavyzdžiui, įveskite ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="374e5-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="374e5-216">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="374e5-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="374e5-217">Pasirinkite maketą **Paskyros patvirtinimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="374e5-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="374e5-218">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="374e5-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="374e5-219">Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo patikros URL.</span><span class="sxs-lookup"><span data-stu-id="374e5-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="374e5-220">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="374e5-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="374e5-221">Pavyzdžiui, įveskite ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="374e5-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="374e5-222">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="374e5-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="374e5-223">Etikečių ir aprašų numatytųjų teksto eilučių tinkinimas</span><span class="sxs-lookup"><span data-stu-id="374e5-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="374e5-224">Modulių bibliotekoje prisijungimo moduliai yra iš anksto užpildyti etikečių ir aprašų numatytomis teksto eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="374e5-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="374e5-225">Galite pritaikyti šias eilutes programinės įrangos kūrimo rinkinyje (SDK), atnaujindami reikšmes, esančias prisijungimo modulio global.json faile.</span><span class="sxs-lookup"><span data-stu-id="374e5-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="374e5-226">Pavyzdžiui, numatytasis pamiršto slaptažodžio saito tekstas **Pamiršote slaptažodį?**.</span><span class="sxs-lookup"><span data-stu-id="374e5-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="374e5-227">Šiame prisijungimo puslapyje pateikiamas šis numatytasis tekstas.</span><span class="sxs-lookup"><span data-stu-id="374e5-227">The following shows this default text on the sign-in page.</span></span>

![Numatytasis pamiršto slaptažodžio saito, esančio prisijungimo puslapyje, tekstas](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="374e5-229">Tačiau modulių bibliotekos, esančios prisijungimo modulyje, global.json faile galite redaguoti tekstą į **Pamiršote slaptažodį?**, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="374e5-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Atnaujintas saito tekstas prisijungimo modulio global.json faile](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="374e5-231">Atnaujinus global.json failą ir publikavus keitimus, naujas saito tekstas atsiranda ir „Commerce“ ir tiesioginio registravimosi puslapio prisijungimo modulyje.</span><span class="sxs-lookup"><span data-stu-id="374e5-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="374e5-232">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="374e5-232">Additional resources</span></span>

[<span data-ttu-id="374e5-233">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="374e5-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="374e5-234">Talpinkite naują e-komercijos nuomotoją</span><span class="sxs-lookup"><span data-stu-id="374e5-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="374e5-235">Sukurkite e-komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="374e5-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="374e5-236">Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu</span><span class="sxs-lookup"><span data-stu-id="374e5-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="374e5-237">„robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="374e5-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="374e5-238">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="374e5-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="374e5-239">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="374e5-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="374e5-240">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="374e5-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="374e5-241">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="374e5-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="374e5-242">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="374e5-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
