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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5d9f2febc912b35897b063019146d219cadea1fa
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517237"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="8a4ab-103">Vartotojo registracijos pasirinktinių puslapių sąranka</span><span class="sxs-lookup"><span data-stu-id="8a4ab-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8a4ab-104">Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="8a4ab-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="8a4ab-105">Overview</span></span>

<span data-ttu-id="8a4ab-106">Norėdami naudoti tinkintus puslapius, kurie sukurti „Dynamics 365 Commerce“ programoje valdyti vartotojo registravimosi srautus, turite nustatyti „Azure AD“ strategijas, kurios bus nurodytos „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="8a4ab-107">Galite konfigūruoti „Prisijungti ir įeiti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“ „Azure AD“ B2C strategijas naudodami „Azure AD“ B2C programą.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="8a4ab-108">„Azure AD“ B2C nuomotojo ir strategijos pavadinimai gali būti nurodyti rengimo proceso metu, kuris vykdomas „Commerce“ aplinkai naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="8a4ab-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="8a4ab-109">Tinkintą „Commerce“ puslapį galima sukurti naudojant registravimosi, prisijungimo, paskyros profilio redagavimo arba slaptažodžio nustatymo iš naujo modulį.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="8a4ab-110">Puslapio URL, kurie publikuojami šiems tinkintiems puslapiams, turėtų būti nurodyti „Azure AD“ B2C strategijų konfigūracijose, „Azure“ portale.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="8a4ab-111">B2C strategijų sąranka</span><span class="sxs-lookup"><span data-stu-id="8a4ab-111">Set up B2C policies</span></span>

<span data-ttu-id="8a4ab-112">Nustatę savo „Azure AD“ B2C nuomotoją ir susieję jį su savo „Commerce“ aplinka, eikite į **„Azure AD“ B2C** puslapį, esantį „Azure“ portale, ir meniu, dalyje **Strategijos**, pasirinkite **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Meniu komanda Vartotojo srautai (strategijos)](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="8a4ab-114">Dabar galite konfigūruoti vartotojų prisijungimo srautus „Registruotis ir prisijungti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="8a4ab-115">Konfigūruoti strategiją „Registruotis ir prisijungti“</span><span class="sxs-lookup"><span data-stu-id="8a4ab-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="8a4ab-116">Norėdami sukonfigūruoti strategiją „Registruotis ir prisijungti“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="8a4ab-117">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Registruotis ir prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="8a4ab-118">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_SignInSignUp**).</span><span class="sxs-lookup"><span data-stu-id="8a4ab-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="8a4ab-119">Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="8a4ab-120">Turi būti pažymėta bent **El. pašto registracija**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="8a4ab-121">Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas**, **Vardas** ir **Pavardė**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="8a4ab-122">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Pasirinkti atributai ir pareiškimai](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="8a4ab-124">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="8a4ab-125">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="8a4ab-126">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Naujos strategijos ypatybių puslapis](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="8a4ab-128">Strategijos pavadinimas bus išsamiai nurodytas „Commerce“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="8a4ab-129">(**B2C\_1\_** priešvardis bus įtrauktas į nuorodą.) Sukūrus strategiją, strategijų pervardyti negalima.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="8a4ab-130">Jei keičiate esamą „Commerce“ aplinkos strategiją, galite panaikinti pradinę strategiją ir sukurti naują strategiją, turinčią tokį patį pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="8a4ab-131">Taip pat, jei aplinka jau parengta, galite pateikti naują strategijos pavadinimą naudodami paslaugos užklausą.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="8a4ab-132">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="8a4ab-133">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="8a4ab-134">„Profilių redagavimo“ strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="8a4ab-135">Norėdami sukonfigūruoti „Profilio redagavimo“ strategiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="8a4ab-136">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Profilio redagavimas**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="8a4ab-137">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_EditProfile**).</span><span class="sxs-lookup"><span data-stu-id="8a4ab-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="8a4ab-138">Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="8a4ab-139">Turi būti pažymėta bent **Prisijungimas prie vietinės paskyros**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="8a4ab-140">Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas** ir **Pavardė**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="8a4ab-141">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="8a4ab-142">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="8a4ab-143">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="8a4ab-144">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="8a4ab-145">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="8a4ab-146">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="8a4ab-147">„Slaptažodžio nustatymo iš naujo“ strategijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="8a4ab-148">Norėdami sukonfigūruoti „Slaptažodžio nustatymo iš naujo“ strategiją, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="8a4ab-149">Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Peržiūra** pasirinkite strategiją **Slaptažodžio nustatymas iš naujo v1.1**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Slaptažodžio nustatymo iš naujo v1.1 strategija, pasirinkta skirtuke Peržiūra](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="8a4ab-151">Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_ForgetPassword**).</span><span class="sxs-lookup"><span data-stu-id="8a4ab-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="8a4ab-152">Skyriuje **Tapapybės teikimo įrankis** pasirinkite **Iš naujo nustatyti slaptažodį naudojant el. pašto adresą**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="8a4ab-153">Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresas**, **Vardas**, **Pavardė** ir **Vartotojo objekto ID**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Pasirinkti pareiškimai](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="8a4ab-155">Pasirinkite **Gerai**, kad sukurtumėte strategiją.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="8a4ab-156">Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="8a4ab-157">Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="8a4ab-158">Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="8a4ab-159">Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="8a4ab-160">Tinkintų puslapių kūrimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-160">Build the custom pages</span></span>

<span data-ttu-id="8a4ab-161">Norėdami sukurti tinkintus puslapius, skirtus valdyti vartotojų prisijungimus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="8a4ab-162">„Commerce“ kūrimo įrankiuose eikite į savo svetainę.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="8a4ab-163">Sukurkite šiuos penkis šablonus ir penkis puslapius:</span><span class="sxs-lookup"><span data-stu-id="8a4ab-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="8a4ab-164">**Prisijungimo** šabloną ir puslapį, kuriuose naudojamas prisijungimo modulis.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="8a4ab-165">**Registravimosi** šabloną ir puslapė, kuriuose naudojamas registravimosi modulis.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="8a4ab-166">**Slaptažodžio nustatymo iš naujo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo modulis.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="8a4ab-167">**Slaptažodžio nustatymo iš naujo tikrinimo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo tikrinimo modulis.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="8a4ab-168">**Profilio redagavimo** šabloną ir puslapį, kuriuose naudojamas paskyros profilio redagavimo modulis</span><span class="sxs-lookup"><span data-stu-id="8a4ab-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="8a4ab-169">Kurdami puslapius vadovaukitės šiais nurodymais:</span><span class="sxs-lookup"><span data-stu-id="8a4ab-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="8a4ab-170">Kiekviename puslapyje ar modulyje naudokite maketą ir stilių, kurie geriausiai atitinka jūsų verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="8a4ab-171">Publikuokite visus puslapius ir URL, kurie turi būti naudojami „Azure AD“ B2C sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="8a4ab-172">Po to, kai puslapiai ir URL publikuojami, rinkite URL, kurie turi būti naudojami „Azure AD“ B2C"strategijos konfigūracijoms.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="8a4ab-173">Povardis **?preloadscripts=true** bus įtrauktas į kiekvieną naudojamą URL.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a4ab-174">Nenaudokite universalių antraščių ir poraščių, kuriose yra santykinių saitų.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="8a4ab-175">Kadangi šie puslapiai bus nuomojami „Azure AD“ B2C domene, juos naudojant, visiems saitams reikia naudoti tik absoliučias URL.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="8a4ab-176">„Azure AD“ B2C strategijų konfigūravimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="8a4ab-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="8a4ab-177">„Azure“ portale grįžkite į **„Azure AD“ B2C** puslapį ir meniu dalyje, srityje **Strategijos** pasirinkite **Vartotojų srautai (strategijos)**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="8a4ab-178">„Registruotis ir prisijungti“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="8a4ab-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="8a4ab-179">Atnaujinti strategiją „Registruotis ir prisijungti“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="8a4ab-180">Jūsų anksčiau sukonfigūruotoje strategijoje **Registruotis ir prisijungti**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="8a4ab-181">Pasirinkite maketą **Vieningasis registracijos ir prisijungimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="8a4ab-182">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="8a4ab-183">Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="8a4ab-184">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="8a4ab-185">Pavyzdžiui, įveskite ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="8a4ab-186">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="8a4ab-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="8a4ab-187">Pasirinkite maketą **Registravimosi į vietinę paskyrą puslapis**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="8a4ab-188">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="8a4ab-189">Lauke **Pasirinktinis puslapio URI** įveskite visą registracijos URL.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="8a4ab-190">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="8a4ab-191">Pavyzdžiui, įveskite ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="8a4ab-192">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="8a4ab-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="8a4ab-193">Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8a4ab-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="8a4ab-194">Atributams **El. pašto adresas**, **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Reikalingas patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="8a4ab-195">Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Registravimosi prie vietinės paskyros puslapio strategijos konfigūravimas](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="8a4ab-197">„Profilio redagavimas“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="8a4ab-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="8a4ab-198">Atnaujinti strategiją „Profilio redagavimas“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="8a4ab-199">Jūsų anksčiau sukonfigūruotoje strategijoje **Profilio redagavimas**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="8a4ab-200">Pasirinkite maketą **Profilio redagavimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="8a4ab-201">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="8a4ab-202">Lauke **Pasirinktinis puslapio URI** įveskite visą profilio redagavimo URL.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="8a4ab-203">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="8a4ab-204">Pavyzdžiui, įveskite ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="8a4ab-205">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="8a4ab-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="8a4ab-206">Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="8a4ab-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="8a4ab-207">Atributams **El. pašto adresas**, **Vardas** pasirinkite **Ne** lauke **Reikalingas tikrinimas**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="8a4ab-208">Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="8a4ab-209">„Slaptažodžio nustatymo iš naujo“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją</span><span class="sxs-lookup"><span data-stu-id="8a4ab-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="8a4ab-210">Atnaujinti strategiją „Slaptažodžio nustatymas iš naujo“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="8a4ab-211">Jūsų anksčiau sukonfigūruotoje strategijoje **Slaptažodžio nustatymas iš naujo**, naršymo srityje, pasirinkite **Puslapio maketai**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="8a4ab-212">Pasirinkite maketą **Naujo slaptažodžio puslapis**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="8a4ab-213">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="8a4ab-214">Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo URL.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="8a4ab-215">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="8a4ab-216">Pavyzdžiui, įveskite ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="8a4ab-217">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="8a4ab-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="8a4ab-218">Pasirinkite maketą **Paskyros patvirtinimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="8a4ab-219">Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="8a4ab-220">Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo patikros URL.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="8a4ab-221">Įtraukite povardį **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="8a4ab-222">Pavyzdžiui, įveskite ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="8a4ab-223">Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**</span><span class="sxs-lookup"><span data-stu-id="8a4ab-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="8a4ab-224">Etikečių ir aprašų numatytųjų teksto eilučių tinkinimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="8a4ab-225">Modulių bibliotekoje prisijungimo moduliai yra iš anksto užpildyti etikečių ir aprašų numatytomis teksto eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-225">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="8a4ab-226">Galite pritaikyti šias eilutes programinės įrangos kūrimo rinkinyje (SDK), atnaujindami reikšmes, esančias prisijungimo modulio global.json faile.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="8a4ab-227">Pavyzdžiui, numatytasis pamiršto slaptažodžio saito tekstas **Pamiršote slaptažodį?**.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="8a4ab-228">Šiame prisijungimo puslapyje pateikiamas šis numatytasis tekstas.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-228">The following shows this default text on the sign-in page.</span></span>

![Numatytasis pamiršto slaptažodžio saito, esančio prisijungimo puslapyje, tekstas](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="8a4ab-230">Tačiau modulių bibliotekos, esančios prisijungimo modulyje, global.json faile galite redaguoti tekstą į **Pamiršote slaptažodį?**, kaip parodyta šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-230">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Atnaujintas saito tekstas prisijungimo modulio global.json faile](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="8a4ab-232">Atnaujinus global.json failą ir publikavus keitimus, naujas saito tekstas atsiranda ir „Commerce“ ir tiesioginio registravimosi puslapio prisijungimo modulyje.</span><span class="sxs-lookup"><span data-stu-id="8a4ab-232">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a4ab-233">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8a4ab-233">Additional resources</span></span>

[<span data-ttu-id="8a4ab-234">Jūsų domeno vardo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="8a4ab-235">Talpinkite naują e-komercijos nuomotoją</span><span class="sxs-lookup"><span data-stu-id="8a4ab-235">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="8a4ab-236">Sukurkite e-komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="8a4ab-236">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="8a4ab-237">Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu</span><span class="sxs-lookup"><span data-stu-id="8a4ab-237">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="8a4ab-238">„robots.txt” failų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-238">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="8a4ab-239">Masinis URL peradresavimų nusiuntimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-239">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="8a4ab-240">B2C nuomotojo nustatymas „Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="8a4ab-240">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="8a4ab-241">„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-241">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="8a4ab-242">Turinio pristatymo tinklo (CDN) palaikymo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-242">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="8a4ab-243">Parduotuvės nustatymo pagal vietą įgalinimas</span><span class="sxs-lookup"><span data-stu-id="8a4ab-243">Enable location-based store detection</span></span>](enable-store-detection.md)
