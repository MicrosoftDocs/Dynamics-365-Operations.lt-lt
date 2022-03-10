---
title: Vartotojo registracijos pasirinktinių puslapių sąranka
description: Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f4a3c7c3410a903ae7bc0bac27e861a0dbfa19fdd65761628549c403c4e5db16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723268"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Vartotojo registracijos pasirinktinių puslapių sąranka

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti tinkintus „Microsoft Dynamics 365 Commerce“ puslapius, kuriuose galima valdyti pritaikytus „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojų vartotojų prisijungimus.

Norėdami naudoti tinkintus puslapius, kurie sukurti „Dynamics 365 Commerce“ programoje valdyti vartotojo registravimosi srautus, turite nustatyti „Azure AD“ strategijas, kurios bus nurodytos „Commerce“ aplinkoje. Galite konfigūruoti „Prisijungti ir įeiti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“ „Azure AD“ B2C strategijas naudodami „Azure AD“ B2C programą. „Azure AD“ B2C nuomotojo ir strategijos pavadinimai gali būti nurodyti rengimo proceso metu, kuris vykdomas „Commerce“ aplinkai naudojant „Microsoft Dynamics“ „Lifecycle Services“ (LCS).

Tinkintą „Commerce“ puslapį galima sukurti naudojant registravimosi, prisijungimo, paskyros profilio redagavimo, slaptažodžio nustatymo arba bendrąjį AAD modulius. Puslapio URL, kurie publikuojami šiems tinkintiems puslapiams, turėtų būti nurodyti „Azure AD“ B2C strategijų konfigūracijose, „Azure“ portale.

> [!WARNING] 
> „Azure AD B2C” panaikins senus (senstelėjusius) vartotojų srautus 2021 m. rugpjūčio mėnesio 1 d. Todėl turėtumėte planuoti perkelti savo vartotojų srautus į naują rekomenduojamą versiją. Nauja versija suteikia lygiavertiškas bei naujas funkcijas. Daugiau informacijos rasite [„Azure Active Directory B2C” vartotojų srautai](/azure/active-directory-b2c/user-flow-overview).

>„Commerce” 10.0.15 arba naujesnės versijos modulių biblioteka turi būti naudojama su rekomenduojamais B2C vartotojų srautais. Taip pat galima naudoti „Azure AD B2C” pasiūlytus numatytuosius vartotojo strategijos puslapius ir leisti įtraukti fono vaizdą, logotipą ir fono spalvų keitimus, susijusius su įmonės prekės ženklo integravimu. Nors numatytų vartotojo strategijos puslapių dizaino galimybės yra ribotesnės, juose suteikiamos „Azure AD B2C” strategijos funkcijos nekuriant ir nekonfigūruojant paskirtų pasirinktinių puslapių. 

## <a name="set-up-b2c-policies"></a>B2C strategijų sąranka

Nustatę savo „Azure AD“ B2C nuomotoją ir susieję jį su savo „Commerce“ aplinka, eikite į **„Azure AD“ B2C** puslapį, esantį „Azure“ portale, ir meniu, dalyje **Strategijos**, pasirinkite **Vartotojų srautai (strategijos)**.

![Meniu komanda Vartotojo srautai (strategijos).](./media/B2C_CustomPage_PoliciesMenu.png)

Dabar galite konfigūruoti vartotojų prisijungimo srautus „Registruotis ir prisijungti“, „Profilio redagavimas“ ir „Slaptažodžio nustatymas iš naujo“.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>Konfigūruoti strategiją „Registruotis ir prisijungti“

Norėdami sukonfigūruoti strategiją „Registruotis ir prisijungti“, atlikite šiuos veiksmus.

1. Pasirinkite **Naujas vartotojo srautas**, **Registruotis ir prisijungti**, tada – skirtuką **Rekomenduojama** ir **Kurti**.
1. Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_SignInSignUp**).
1. Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje. Turi būti pažymėta bent **El. pašto registracija**.
1. Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **El. pašto adresas**, **Vardas** ir **Pavardė**.
1. Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.

    ![Pasirinkti atributai ir pareiškimai.](./media/B2C_SignInSignUp_Attributes.png)

1. Pasirinkite **Gerai**, kad sukurtumėte strategiją.
1. Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.
1. Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.

    ![Naujos strategijos ypatybių puslapis.](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> Strategijos pavadinimas bus išsamiai nurodytas „Commerce“ aplinkoje. (**B2C\_1\_** priešvardis bus įtrauktas į nuorodą.) Sukūrus strategiją, strategijų pervardyti negalima. Jei keičiate esamą „Commerce“ aplinkos strategiją, galite panaikinti pradinę strategiją ir sukurti naują strategiją, turinčią tokį patį pavadinimą. Taip pat, jei aplinka jau parengta, galite pateikti naują strategijos pavadinimą naudodami paslaugos užklausą.

Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius. Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.

### <a name="configure-the-profile-editing-policy"></a>„Profilių redagavimo“ strategijos konfigūravimas

Norėdami sukonfigūruoti „Profilio redagavimo“ strategiją, atlikite tolesnius veiksmus.

1. Pasirinkite **Naujas vartotojo srautas**, **Profilio redagavimas**, tada – skirtuką **Rekomenduojama** ir **Kurti**.
1. Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_EditProfile**).
1. Skyriuje **Tapatybės teikimo įrankiai** pasirinkite, kokius tapatybės teikimo įrankius naudoti strategijoje. Turi būti pažymėta bent **Prisijungimas prie vietinės paskyros**.
1. Stulpelyje **Rinkti atributą** pasirinkite žymės laukelius **Duotas vardas** ir **Pavardė**.
1. Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresai**, **Vardas**, **Tapatybės teikimo įrankis**, **Pavardė** ir **Vartotojo objekto ID**.
1. Pasirinkite **Gerai**, kad sukurtumėte strategiją.
1. Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.
1. Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.

Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius. Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.

### <a name="configure-the-password-reset-policy"></a>„Slaptažodžio nustatymo iš naujo“ strategijos konfigūravimas

Norėdami sukonfigūruoti „Slaptažodžio nustatymo iš naujo“ strategiją, atlikite tolesnius veiksmus.

1. Pasirinkite **Naujas vartotojo srautas**, tada – **Slaptažodžio nustatymo iš naujo** parinkties skirtuką **Rekomenduojama** bei spustelėkite **Kurti**.
1. Įveskite strategijos pavadinimą (pavyzdžiui **B2C\_1\_ForgetPassword**).
1. Skyriuje **Tapapybės teikimo įrankis** pasirinkite **Iš naujo nustatyti slaptažodį naudojant el. pašto adresą**.
1. Stulpelyje **Grįžties pareiškimas** pažymėkite žymės langelius **El. pašto adresas**, **Vardas**, **Pavardė** ir **Vartotojo objekto ID**.
1. Pasirinkite **Gerai**, kad sukurtumėte strategiją.
1. Du kartus spustelėkite naują strategijos pavadinimą, o tada naršymo srityje pasirinkite **Ypatybės**.
1. Nustatykite parinktį **Įjungti „JavaScript“ vykdymo puslapio maketas (peržiūra)** į **Įjungta**.

Jūs grįšite į šią strategiją, kad užbaigtumėte sąranką sukūrę tinkintus puslapius. Dabar uždarykite strategiją, kad sugrįžtumėte į „Azure“ portalo puslapį **Vartotojų srautai (strategijos)**.

## <a name="build-the-custom-pages"></a>Tinkintų puslapių kūrimas

Paskirtieji „Azure AD” moduliai yra įtraukti į „Commerce” norint sukurti pasirinktinius „Azure AD B2C” vartotojo strategijų puslapius. Puslapius galima kurti specialiai kiekvienam vartotojo strategijos puslapio maketui naudojant pagrindinius „Azure AD B2C” modulius, aprašytus žemiau. Taip pat **bendrasis AAD** modulis gali būti naudojamas visiems „Azure AD B2C” puslapių maketams ir strategijoms (net ir žemiau nenurodytoms puslapio maketo parinktiems strategijose). 

- Puslapiui konkretūs„ Azure AD” moduliai yra susieti su duomenų įvesties elementais, atvaizduotais „Azure AD B2C”. Šie moduliai suteikia jums daugiau kontrolės nustatyti elementų vietą jūsų puslapiuose. Tačiau gali reikėti sukurti daugiau puslapių ir modulių plėtinių, kad būtų galima atsakyti už nuokrypius, kurie viršija žemiau aprašytus numatytuosius parametrus.
- Modulis **bendrasis AAD** sukuria „div” elementą, skirtą „Azure AD B2C” atvaizduoti visus elementus vartotojo strategijos puslapio makete, taip suteikiant daugiau lankstumo puslapio B2C funkcijos, tačiau mažiau kontrolės vietos padėties nustatymui ir stiliui (nors „CSS” gali būti naudojamas jūsų svetainės išvaizdos ir funkcijų derinimui).

Galite sukurti vieną puslapį naudodami **bendrąjį AAD** modulį ir naudoti jį visuose jūsų vartotojo strategijos puslapiuose arba sukurti konkrečius puslapius, naudodami atskirus „Azure AD” prisijungimo, registracijos, profilio redagavimo, slaptažodžio nustatymo iš naujo ir slaptažodžio nustatymo iš naujo patvirtinimo modulius. Taip pat galbūt norėsite naudoti abejų modulį derinį, naudojant konkrečius „Azure AD” puslapius žemiau pateiktiems puslapio maketams ir bendrąjį AAD modulį kitiems puslapio maketams šiose ar kitose vartotojo strategijų puslapiuose.

Norėdami sužinoti daugiau apie „Azure AD” modulius, kurie siunčia kartu su modulių biblioteka, skaitykite [Tapatybės valdymo puslapiai ir moduliai](identity-mgmt-modules.md).

Norėdami sukurti tinkintus puslapius su konkrečiais tapatybės moduliais, skirtus valdyti vartotojų prisijungimus, atlikite šiuos veiksmus.

1. Eikite į savo svetainę „Commerce“ svetainių daryklėje.
1. Sukurkite šiuos penkis šablonus ir puslapius (jei jų dar nėra jūsų svetainėje):
    - **Prisijungimo** šabloną ir puslapį, naudojantį prisijungimo modulį.
    - **Registravimosi** šabloną ir puslapį, kuriuose naudojantį registravimosi modulį.
    - **Slaptažodžio nustatymo iš naujo** šabloną ir puslapį, naudojantį slaptažodžio nustatymo iš naujo modulį.
    - **Slaptažodžio nustatymo iš naujo patvirtinimo** šabloną ir puslapį, naudojantį slaptažodžio nustatymo iš naujo patvirtinimo modulį.
    - **Profilio redagavimo** šabloną ir puslapį, naudojantį paskyros profilio redagavimo modulį.

Kurdami puslapius vadovaukitės šiais nurodymais:

- Kiekviename puslapyje ar modulyje naudokite maketą ir stilių, kurie geriausiai atitinka jūsų verslo poreikius.
- Publikuokite visus puslapius ir URL, kurie turi būti naudojami „Azure AD“ B2C sąrankoje.
- Po to, kai puslapiai ir URL publikuojami, rinkite URL, kurie turi būti naudojami „Azure AD“ B2C"strategijos konfigūracijoms. Povardis **?preloadscripts=true** bus įtrauktas į kiekvieną naudojamą URL.

> [!IMPORTANT]
> Puslapiai, sukurti „Azure AD B2C” nuorodai, pristatomi tiesiai iš „Azure AD B2C” nuomotojo domeno. Pakartotinai nenaudokite universalių antraščių ir poraščių, kuriose yra santykinių saitų. Kadangi šie puslapiai bus nuomojami „Azure AD“ B2C domene, juos naudojant, visiems saitams reikia naudoti tik absoliučias URL. Rekomenduojama sukurti konkrečią antraštę ir poraštę su absoliučiais URL, skirtiems jūsų su „Azure AD” susijusiais pasirinktiniais puslapiais, naudojant bet kurį „Commerce” būdingą modulį, kuriam reikia panaikinti ryšį su „Retail Server”. Pavyzdžiui, parankinių, ieškos juostos, prisijungimo saito ir krepšelio modulių negalima įtraukti į jokius puslapius, kurie bus naudojami „Azure AD B2C” vartotojų srautuose.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>„Azure AD“ B2C strategijų konfigūravimas naudojant pasirinktinę puslapio informaciją 

„Azure“ portale grįžkite į **„Azure AD“ B2C** puslapį ir meniu dalyje, srityje **Strategijos** pasirinkite **Vartotojų srautai (strategijos)**.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>„Registruotis ir prisijungti“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją

Atnaujinti strategiją „Registruotis ir prisijungti“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.

1. Jūsų anksčiau sukonfigūruotoje strategijoje **Registruotis ir prisijungti**, naršymo srityje, pasirinkite **Puslapio maketai**.
1. Pasirinkite maketą **Vieningasis registracijos ir prisijungimo puslapis**.
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Vartotojo puslapio URL** įveskite visą prisijungimo URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/sign-in?preloadscripts=true``.
1. Lauke **Puslapio maketo versija** pasirinkite **2.1.0 arba** naujesnę versiją (reikia „Commerce” 10.0.15 arba naujesnės versijos modulių bibliotekos).
1. Pasirinkite **Įrašyti**.
1. Pasirinkite maketą **Registravimosi į vietinę paskyrą puslapis**.
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Pasirinktinis puslapio URI** įveskite visą registracijos URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/sign-up?preloadscripts=true``.
1. Lauke **Puslapio maketo versija** pasirinkite **2.1.0 arba** naujesnę versiją (reikia „Commerce” 10.0.15 arba naujesnės versijos modulių bibliotekos).
1. Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:
    1. Atributams **Pateiktas vardas** ir **Pavardė** pasirinkite **Ne** stulpelyje **Reikia patvirtinimo**.
    1. Atributui **El. pašto adresas** rekomenduojama palikti pasirinktą numatytąją reikšmę **Taip** stulpelyje **Reikia patvirtinimo**. Ši parinktis užtikrina, kad vartotojai registruodamiesi su pateiktu el. pašto adresu, patvirtina, kad šis el. pašto adresas priklauso jiems.
    1. Atributams **El. pašto adresas**, **Vardas** ir **Pavardė** pasirinkite **Ne** stulpelyje **Pasirinktinis**.
1. Pasirinkite **Įrašyti**.

    ![Vietinės paskyros registravimo puslapio strategijos konfigūravimas.](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>„Profilio redagavimas“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją

Atnaujinti strategiją „Profilio redagavimas“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.

1. Jūsų anksčiau sukonfigūruotoje strategijoje **Profilio redagavimas**, naršymo srityje, pasirinkite **Puslapio maketai**.
1. Pasirinkite **Profilio redagavimo puslapio** maketą (gali reikėti slinkti žemyn per kitas maketo parinktis, atsižvelgiant į jūsų ekraną).
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Pasirinktinis puslapio URI** įveskite visą profilio redagavimo URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/profile-edit?preloadscripts=true``.
1. **Puslapio maketo versijai** pasirinkite **2.1.0 arba** aukštesnę versiją (reikia „Commerce” 10.0.15 arba naujesnės versijos modulių bibliotekos).
1. Skyriuje **Vartotojo atributai** atlikite šiuos veiksmus:
    1. Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** stulpelyje **Pasirinktinis**.
    1. Atributams **Vardas** ir **Pavardė** pasirinkite **Ne** stulpelyje **Reikia patvirtinimo**.
1. Pasirinkite **Įrašyti**.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>„Slaptažodžio nustatymo iš naujo“ strategijos naujinimas naudojant pasirinktinę puslapio informaciją

Atnaujinti strategiją „Slaptažodžio nustatymas iš naujo“ naudokite pasirinktinę puslapio informaciją bei atlikite toliaus nurodytus veiksmus.

1. Jūsų anksčiau sukonfigūruotoje strategijoje **Slaptažodžio nustatymas iš naujo**, naršymo srityje, pasirinkite **Puslapio maketai**.
1. Pasirinkite maketą **Pamiršto slaptažodžio puslapis**.
1. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
1. Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo patikros URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/password-reset-verification?preloadscripts=true``.
1. Lauke **Puslapio maketo versija** pasirinkite **2.1.0 arba** vėlesnę versiją (reikia „Commerce” 10.0.15 arba naujesnės versijos modulių bibliotekos).
2. Pasirinkite **Įrašyti**.
3. Pasirinkite maketą **Slaptažodžio keitimo puslapis**.
4. Nustatykite parinktį **Naudoti pasirinktinį puslapio turinį** į **Taip**.
5. Lauke **Pasirinktinis puslapio URI** įveskite visą slaptažodžio nustatymo iš naujo URL. Įtraukite povardį **?preloadscripts=true**. Pavyzdžiui, įveskite ``www.<my domain>.com/password-reset?preloadscripts=true``.
6. Lauke **Puslapio maketo versija** pasirinkite **2.1.0 arba** vėlesnę versiją (reikia „Commerce” 10.0.15 arba naujesnės versijos modulių bibliotekos).
7. Pasirinkite **Įrašyti**.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Etikečių ir aprašų numatytųjų teksto eilučių tinkinimas

Modulių bibliotekoje prisijungimo moduliai yra iš anksto užpildyti etikečių ir aprašų numatytomis teksto eilutėmis. Galite tinkinti eilutes modulio, su kuriuo dirbate, ypatybių srityje. Papildomoms eilutėms puslapyje (pavyzdžiui, **Pamiršote slaptažodį?** saito tekstas arba **Sukurti paskyrą** tekstas, raginantis imtis veiksmų) reikės naudoti „Commerce” programinės įrangos kūrimo rinkinį (SDK) ir atnaujinti global.json failo reikšmes prisijungimo moduliui.

Pavyzdžiui, numatytasis pamiršto slaptažodžio saito tekstas **Pamiršote slaptažodį?**. Šiame prisijungimo puslapyje pateikiamas šis numatytasis tekstas.

![Numatytasis pamiršto slaptažodžio saito, esančio prisijungimo puslapyje, tekstas.](./media/B2C_SignUp_ModuleFace.png)

Tačiau modulių bibliotekos, esančios prisijungimo modulyje, global.json faile galite redaguoti tekstą į **Pamiršote slaptažodį?**, kaip parodyta šioje iliustracijoje.

![Atnaujintas saito tekstas prisijungimo modulio global.json faile.](./media/B2C_CustomizingStringsForModule.png)

Atnaujinus global.json failą ir publikavus keitimus, naujas saito tekstas atsiranda ir „Commerce“ ir tiesioginio registravimosi puslapio prisijungimo modulyje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Talpinkite naują e-komercijos nuomotoją](deploy-ecommerce-site.md)

[Sukurkite e-komercijos saitą](create-ecommerce-site.md)

[Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu](associate-site-online-store.md)

[„robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]