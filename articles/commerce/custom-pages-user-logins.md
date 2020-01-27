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
# <a name="set-up-custom-pages-for-user-logins"></a>Vartotojo prisijungimo tinkintų puslapių sąranka

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.

## <a name="overview"></a>Peržiūrėti

Norėdami naudoti tinkintus puslapius, kurie sukurti „Dynamics 365 Commerce“ programoje valdyti vartotojo registravimosi srautus, turite nustatyti „Azure AD“ strategijas, kurios bus nurodytos „Commerce“ aplinkoje. Galite konfigūruoti „Prisijungti ir įeiti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“ „Azure AD“ B2C strategijas naudodami „Azure AD“ B2C programą. „Azure AD“ B2C nuomotojo ir strategijos pavadinimai gali būti nurodyti rengimo proceso metu, kuris vykdomas „Commerce“ aplinkai naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).

Tinkintą „Commerce“ puslapį galima sukurti naudojant registravimosi, prisijungimo, paskyros profilio redagavimo arba slaptažodžio nustatymo iš naujo modulį. Puslapio URL, kurie publikuojami šiems tinkintiems puslapiams, turėtų būti nurodyti „Azure AD“ B2C strategijų konfigūracijose, „Azure“ portale.

## <a name="set-up-b2c-policies"></a>B2C strategijų sąranka

Nustatę savo „Azure AD“ B2C nuomotoją ir susieję jį su savo „Commerce“ aplinka, eikite į **„Azure AD“ B2C** puslapį, esantį „Azure“ portale, ir meniu, dalyje **Strategijos**, pasirinkite **Vartotojų srautai (strategijos)**.

![Meniu komanda Vartotojo srautai (strategijos)](./media/B2C_CustomPage_PoliciesMenu.png)

Dabar galite konfigūruoti vartotojų prisijungimo srautus „Registruotis ir prisijungti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigūruoti strategiją „Registruotis ir prisijungti“

Norėdami sukonfigūruoti strategiją „Registruotis ir prisijungti“, atlikite šiuos veiksmus.

1. Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Registruotis ir prisijungti**.
1. Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_SignInSignUp**).
1. Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje. Turi būti pažymėta bent **El. pašto registracija**.
1. Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas**, **Vardas**ir **Pavardė**.
1. Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.

    ![Pasirinkti atributai ir pareiškimai](./media/B2C_SignInSignUp_Attributes.png)

1. Pasirinkite **Gerai**, kad sukurtumėte strategiją.
1. Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.
1. Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.

    ![Naujos strategijos ypatybių puslapis](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Strategijos pavadinimas bus išsamiai nurodytas „Commerce“ aplinkoje. (**B2C\_1\_** priešvardis bus įtrauktas į nuorodą.) Sukūrus strategiją, strategijų pervardyti negalima. Jei keičiate esamą „Commerce“ aplinkos strategiją, galite panaikinti pradinę strategiją ir sukurti naują strategiją, turinčią tokį patį pavadinimą. Taip pat, jei aplinka jau parengta, galite pateikti naują strategijos pavadinimą naudodami paslaugos užklausą.

Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius. Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.

### <a name="configure-the-profile-editing-policy"></a>„Profilių redagavimo“ strategijos konfigūravimas

Norėdami sukonfigūruoti „Profilio redagavimo“ strategiją, atlikite tolesnius veiksmus.

1. Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Rekomenduojama** pasirinkite strategiją **Profilio redagavimas**.
1. Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_EditProfile**).
1. Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje. Turi būti pažymėta bent **Prisijungimas prie vietinės paskyros**.
1. Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas** ir **Pavardė**.
1. Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.
1. Pasirinkite **Gerai**, kad sukurtumėte strategiją.
1. Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.
1. Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.

Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius. Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.

### <a name="configure-the-password-reset-policy"></a>„Slaptažodžio nustatymo iš naujo“ strategijos konfigūravimas

Norėdami sukonfigūruoti „Slaptažodžio nustatymo iš naujo“ strategiją, atlikite tolesnius veiksmus.

1. Pasirinkite **Naujas vartotojo srautas**, tada skirtuke **Peržiūra** pasirinkite strategiją **Slaptažodžio nustatymas iš naujo v1.1**.

    ![Slaptažodžio nustatymo iš naujo v1.1 strategija, pasirinkta skirtuke Peržiūra](./media/B2C_ForgetPassword_Menu.png)

1. Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_ForgetPassword**).
1. Skyriuje **Tapapybės teikimo įrankis** pasirinkite **Iš naujo nustatyti slaptažodį naudojant el. pašto adresą**.
1. Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresas**, **Vardas**, **Pavardė**ir **Vartotojo objekto ID**.

    ![Pasirinkti pareiškimai](./media/B2C_ForgetPassword_Attributes.png)

1. Pasirinkite **Gerai**, kad sukurtumėte strategiją.
1. Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.
1. Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.

Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius. Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.

## <a name="build-the-custom-pages"></a>Tinkintų puslapių kūrimas

Norėdami sukurti tinkintus puslapius, skirtus valdyti vartotojų prisijungimus, atlikite šiuos veiksmus.

1. „Commerce“ kūrimo įrankiuose eikite į savo svetainę.
1. Sukurkite šiuos penkis šablonus ir penkis puslapius:

    - **Prisijungimo**šabloną ir puslapį, kuriuose naudojamas prisijungimo modulis.
    - **Registravimosi**šabloną ir puslapė, kuriuose naudojamas registravimosi modulis.
    - **Slaptažodžio nustatymo iš naujo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo modulis.
    - **Slaptažodžio nustatymo iš naujo tikrinimo** šabloną ir puslapį, kuriuose naudojamas slaptažodžio nustatymo iš naujo tikrinimo modulis.
    - **Profilio redagavimo** šabloną ir puslapį, kuriuose naudojamas paskyros profilio redagavimo modulis

Kurdami puslapius vadovaukitės šiais nurodymais:

- Kiekviename puslapyje ar modulyje naudokite maketą ir stilių, kurie geriausiai atitinka jūsų verslo poreikius.
- Publikuokite visus puslapius ir URL, kurie turi būti naudojami „Azure AD“ B2C sąrankoje.
- Po to, kai puslapiai ir URL publikuojami, rinkite URL, kurie turi būti naudojami „Azure AD“ B2C"strategijos konfigūracijoms. Povardis **?preloadscripts=true** bus įtrauktas į kiekvieną naudojamą URL.

> [!IMPORTANT]
> Nenaudokite universalių antraščių ir poraščių, kuriose yra santykinių saitų. Kadangi šie puslapiai bus nuomojami „Azure AD“ B2C domene, juos naudojant, visiems saitams reikia naudoti tik absoliučias URL.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>„Azure AD“ B2C strategijų konfigūravimas naudojant pasirinktinę puslapio informaciją 

„Azure“ portale grįžkite į **„Azure AD“ B2C** puslapį ir meniu dalyje, srityje **Strategijos** pasirinkite **Vartotojų srautai (strategijos)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>„Registruotis ir prisijungti“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją

Atnaujinti strategiją „Registruotis ir prisijungti“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.

1. Jūsų anksčiau sukonfigūruotoje strategijoje **Registruotis ir prisijungti**, naršymo srityje, pasirinkite **Puslapio maketai**.
1. Pasirinkite maketą **Vieningasis registracijos ir prisijungimo puslapis**.
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**
1. Pasirinkite maketą **Registravimosi į vietinę paskyrą puslapis**.
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Pasirinktinis puslapio URI** įveskite visą registracijos URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**
1. Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:

    1. Atributams **El. pašto adresas**, **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Reikalingas patvirtinimas**.
    1. Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.

    ![Registravimosi prie vietinės paskyros puslapio strategijos konfigūravimas](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>„Profilio redagavimas“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją

Atnaujinti strategiją „Profilio redagavimas“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.

1. Jūsų anksčiau sukonfigūruotoje strategijoje **Profilio redagavimas**, naršymo srityje, pasirinkite **Puslapio maketai**.
1. Pasirinkite maketą **Profilio redagavimo puslapis**.
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Pasirinktinis puslapio URI** įveskite visą profilio redagavimo URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**
1. Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:

    1. Atributams **El. pašto adresas**, **Vardas** pasirinkite **Ne** lauke **Reikalingas tikrinimas**.
    1. Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** lauke **Nebūtina**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>„Slaptažodžio nustatymo iš naujo“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją

Atnaujinti strategiją „Slaptažodžio nustatymas iš naujo“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.

1. Jūsų anksčiau sukonfigūruotoje strategijoje **Slaptažodžio nustatymas iš naujo**, naršymo srityje, pasirinkite **Puslapio maketai**.
1. Pasirinkite maketą **Naujo slaptažodžio puslapis**.
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/passwordreset?preloadscripts=true``.
1. Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**
1. Pasirinkite maketą **Paskyros patvirtinimo puslapis**.
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo patikros URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.
1. Lauke **Puslapio maketo versija (peržiūra)** pasirinkite **1.2.0.**



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Etikečių ir aprašų numatytųjų teksto eilučių tinkinimas

Darbo pradžios rinkinyje prisijungimo moduliai yra iš anksto užpildyti etikečių ir aprašų numatytomis teksto eilutėmis. Galite pritaikyti šias eilutes programinės įrangos kūrimo rinkinyje (SDK), atnaujindami reikšmes, esančias prisijungimo modulio global.json faile.

Pavyzdžiui, numatytasis pamiršto slaptažodžio saito tekstas **Pamiršote slaptažodį?**. Šiame prisijungimo puslapyje pateikiamas šis numatytasis tekstas.

![Numatytasis pamiršto slaptažodžio saito, esančio prisijungimo puslapyje, tekstas](./media/B2C_SignUp_ModuleFace.png)

Tačiau darbo pradžios rinkinio, esančio prisijungimo modulyje, global.json faile galite redaguoti tekstą į **Pamiršai slaptažodį?**, kaip parodyta šioje iliustracijoje.

![Atnaujintas saito tekstas prisijungimo modulio global.json faile](./media/B2C_CustomizingStringsForModule.png)

Atnaujinus global.json failą ir publikavus keitimus, naujas saito tekstas atsiranda ir „Commerce“ ir tiesioginio registravimosi puslapio prisijungimo modulyje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Naujos e. prekybos svetainės visuotinis diegimas](deploy-ecommerce-site.md)

[E. prekybos svetainės kūrimas](create-ecommerce-site.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[„Robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)
