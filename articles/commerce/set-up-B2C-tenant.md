---
title: „Commerce” B2C nuomotojo sąranka
description: Šioje temoje aprašoma, kaip nustatyti „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojus, skirtus vartotojo svetainės autentifikavimui „Dynamics 365 Commerce“.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
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
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: af2ec75328b6377c5d92656d011d21576417a63f
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517385"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>„Commerce” B2C nuomotojo sąranka

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti „Azure Active Directory“ („Azure AD“) verslo ir vartotojų (B2C) nuomotojus, skirtus vartotojo svetainės autentifikavimui „Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

„Dynamics 365 Commerce“ naudoja „Azure AD“ B2C, kad palaikytų vartotojo kredencialus ir autentifikavimo srautus. Vartotojas gali prisiregistruoti, prisijungti ir iš naujo nustatyti savo slaptažodį naudodamas šiuos srautus. „Azure AD“ B2C saugoma vartotojo slapto autentifikavimo informacija, pvz., vartotojo vardas ir slaptažodis. Vartotoje įraše B2C nuomotojuje bus saugomas arba B2C vietos sąskaitos įrašas arba B2C socialinės tapatybės teikimo įrankio įrašas. Šie B2C įrašai bus susieti su kliento įrašu „Commerce“ aplinkoje.

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a>Kūrimas arba susiejimas su esamu AAD B2C nuomotoju „Azure“ portale

1. Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).
1. „Azure“ portalo meniu pasirinkite **Kurti išteklius**. Įsitikinkite, kad naudojate prenumeratą ir katalogą, kurie bus susieti su jūsų „Commerce“ aplinka.

    ![Išteklių „Azure“ portale kūrimas](./media/B2CImage_1.png)

1. Eikite į **Tapatybė \> „Azure Active Directory“ B2C**.
1. Kai būsite puslapyje **Kurti naują B2C nuomotoją arba susieti su esamu nuomotoju**, pasirinkite vieną iš toliau apteiktų parinkčių, kuri geriausiai atitinka jūsų įmonės poreikius.

    - **Kurti naują „Azure AD“ B2C nuomotoją**: naudokite šią parinktį, kad sukurtumėte naują AAD B2C nuomotoją.
        1. Pasirinkite **Kurti naują „Azure AD“ B2C nuomotoją**.
        1. Dalyje **Organizacijos pavadinimas** įveskite organizacijos pavadinimą.
        1. Dalyje **Pradinis domeno pavadinimas** įveskite pradinį domeno pavadinimą.
        1. Dalyje **Šalis arba regionas** pasirinkite šalį arba regioną.
        1. Pasirinkite **Kurti**, kad sukurtumėte nuomotoją.

     ![Naujo „Azure AD“ nuomotojo kūrimas](./media/B2CImage_2.png)

     - **Susieti esamą „Azure AD“ B2C nuomotoją su mano „Azure“ prenumerata**: naudokite šią parinktį, jei jau turite „Azure AD“ B2C nuomininką, su kuriuo norite susieti.
        1. Pasirinkite **Susieti esamą „Azure AD“ B2C nuomotoją su mano Azure prenumerata**.
        1. Jei **„Azure AD“ B2C nuomotojas**, pasirinkite atitinkamą B2C nuomotoją. Jei pasirinkimo lauke rodomas pranešimas „Nerasta tinkamų B2C nuomotojų“, neturite tinkamo B2C nuomotojo ir turite sukurti naują.
        1. Jei **Išteklių grupė**, pasirinkite **Kurti naują**. Įveskite išteklių grupės, kurioje bus nuomotojas, **Pavadinimas**, pasirinkite **Išteklių grupės vieta**, tada pasirinkite **Kurti**.

    ![Esamo „Azure AD“ B2C nuomotojo susiejimas su „Azure“ prenumerata](./media/B2CImage_3.png)

1. Kai sukuriamas naujas „Azure AD“ B2C katalogas (tai gali užtrukti kelias akimirkas), ataskaitų srityje bus pradėtas rodyti saitas į ataskaitų sritį. Šis saitas nukreips jus į puslapį „Sveiki atvykę į „Azure Active Directory“ B2C“.

    ![Susiejimas su nauju AAD katalogu](./media/B2CImage_4.png)

> [!NOTE]
> Jei turite kelias savo „Azure“ sąskaitos prenumeratas arba nustatėte B2C nuomotoją nesusiedami su aktyvia prenumerata, nesusiejant su aktyvia prenumerata, juosta **Trikčių diagnostika** jus nukreips, kad susietumėte nuomotoją su prenumerata. Pasirinkite trikčių diagnostikos pranešimą ir sekite instrukcijas, kad išspręstumėte prenumeratos problemą.

Šiame vaizde parodytas „Azure AD“ B2C **Trikčių diagnostika** juosta.

![Įspėjimas, rodantis, kad kataloge nėra aktyvios prenumeratos](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>B2C programos kūrimas

Sukūrus B2C nuomotoją, bus sukurta B2C programa, skirta dirbti su „Commerce“ veiksmais.

Norėdami sukurti B2C programą, atlikite tolesnius veiksmus.

1. „Azure“ portale pasirinkite **Programos(ankstesnės)** ir tuomet pasirinkite **Įtraukti**.
1. Dalyje **Pavadinimas** įveskite pageidaujamos AAD B2C programos pavadinimą.
1. Dalyje **Web App/Web API** **Įtraukti žiniatinklio programa / žiniatinklio API** pasirinkite **Taip**.
1. Norėdami **Leisti numanomą srautą** pasirinkite **Taip** (numatytoji reikšmė).
1. Dalyje **Atsakymo URL** įveskite skirtuosius atsakymo URL. Žr. [Atsakymo URL](#reply-urls) toliau, kur pateikta informacijos apie atsakymo URL ir kaip juos formatuoti.
1. Norėdami **Įtraukti vietinį klientą**, pasirinkite **Ne** (numatytoji reikšmė).
1. Pasirinkite **Kurti**.

### <a name="reply-urls"></a>Atsakymo URL

Atsakymo URL yra svarbūs, nes jie suteikia leidžiamų grąžinimo domenų sąrašą, kai jūsų svetainė reikalauja „Azure AD“ B2C, kad būtų autentifikuotas vartotojas. Tai leidžia autentifikuoti vartotoją grąžinti į domeną, iš kurio jis prisijungė (jūsų svetainės domenas). 

Lauke **Atsakymo URL** ekrane **„Azure AD“ B2c – programos \> Nauja programa** turite įtraukti atskiras eilutes tiek svetainės domenui, tiek (kai jūsų aplinka paruošta) „Commerce“ sugeneruotam URL. Šie URL turi visada naudoti tinkamą URL formatą ir jie turi būti tik pagrindiniai URL (nėra pasvirųjų brūkšnių ar maršrutų). Tada eilutę ``/_msdyn365/authresp`` reikia pridėti prie pagrindinių URL, kaip tolesniuose pavyzdžiuose.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domenas turi visiškai sutapti su „E-commerce“ domenu. Jei turite kelis domenus, turite įtraukti šį URL į kiekvieną domeną.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Vartotojo srauto strategijų kūrimas

Vartotojų srautai yra strategijos, kurias „Azure AD“ B2C naudoja, kad suteiktų saugą prisiregistravimą, prisijungimą, profilio redagavimą ir pamiršto slaptažodžio keitimą. „Dynamics 365 Commerce“ naudoja šiuos srautus, kad galėtų atlikti strategijos veiksmus, skirtus sąveikauti „Azure AD“ B2C nuomotoju. Kai vartotojas sąveikauja su šiomis strategijomis, jis nukreipiami į „Azure AD“ B2C nuomotoją, kad atliktų veiksmus.

„Azure AD“ B2C pateikiami trys pagrindiniai vartotojo srautų tipai:
- Prisiregistravimas ir prisijungimas
- Profilio redagavimas
- Slaptažodžio nustatymas iš naujo

Galite pasirinkti naudoti numatytuosius vartotojo srautus, kuriuos siūlo „Azure AD“ ir kurie bus rodomi AAD B2C puslapyje. Arba galite sukurti HTML puslapį, kad galėtumėte valdyti šios vartotojo srauto patirties apipavidalinimą. 

Norėdami tinkinti vartotojo strategijos puslapius „Dynamics 365 Commerce“ žr. [Pasirinktinių puslapių nustatymas vartotojų prisijungimui](custom-pages-user-logins.md). Daugiau informacijos žr. [Vartotojų patirties sąsajos tinkinimas „Azure Active Directory“ B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Prisiregistravimo ir prisijungimo vartotojo srauto strategijos kūrimas

Norėdami sukurti prisiregistravimo ir prisijungimo vartotojo srauto strategiją, atlikite šiuos veiksmus.

1. „Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.
1. Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.
1. Skirtuke **Rekomenduojama** pasirinkite **Registruotis ir prisijungti**.
1. Dalyje **Pavadinimas** įveskite strategijos pavadinimą. Šis pavadinimas bus rodomas su prievardžiu, kurį priskyrė portalas (pavyzdžiui, „B2C_1_“).
1. Dalyje **Tapatybės teikimo įrankiai** pažymėkite atitinkamą žymės langelį.
1. Dalyje **Kelių faktorių autentifikavimas** atlikite pasirinkimą pagal savo įmonę. 
1. Dalyje **Vartotojo atributai ir pretenzijos** pasirinkite pasirinktis, kad būtų galima rinkti atributus arba grąžinti pretenzijas, kaip tinkama. „Commerce“ reikia nustatyti tolesnes numatytąsias parinktis:

    | **Rinkti atributą** | **Grąžinti pretenziją** |
    | ---------------------- | ----------------- |
    | El. pašto adresas          | El. pašto adresai   |
    | Vardas             | Vardas        |
    |                        | Tapatybės teikėjas |
    | Pavardė                | Pavardė           |
    |                        | Vartotojo objekto ID  |

1. Pasirinkite **Kurti**.

Tolesniame vaizde pateikiamas „Azure AD“ B2C prisiregistravimo ir prisijungimo vartotojo srauto pavyzdys.

![Prisiregistravimo ir prisijungimo strategijos parametrai](./media/B2CImage_11.png)

Tolesniame paveiksle rodoma parinktis **Vykdyti vartotojo srautą** „Azure AD“ B2C prisiregistravimo ir prisijungimo vartotojo sraute.

![Vartotojo srauto vykdymo parinktis strategijos sraute](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a>Profilio redagavimo vartotojo srauto strategijos kūrimas

Norėdami sukurti profilio redagavimo vartotojo srauto strategiją, atlikite šiuos veiksmus.

1. „Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.
1. Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.
1. Skirtuke **Rekomenduojama** pasirinkite **Profilio redagavimas**.
1. Dalyje **Pavadinimas** įveskite profilio redagavimo vartotojo srautą. Šis pavadinimas bus rodomas su prievardžiu, kurį priskyrė portalas (pavyzdžiui, „B2C_1_“).
1. Dalyje **Tapatybės teikimo įrankis** pasirinkite **Prisijungimas prie vietinės sąskaitos**.
1. Dalyje **Vartotojo atributai** pažymėkite bet kurį iš šių žymės langelių:
    - **El. pašto adresai** (tik **Grąžinti pretenziją**)
    - **Vardas** (**Rinkti atributą** ir **Grąžinti pretenziją**)
    - **Tapatybės teikimo įrankis** (tik **Grąžinti pretenziją** )
    - **Pavardę** (**Rinkti atributą** ir **Grąžinti pretenziją**)
    - **Vartotojo objekto ID** (tik **Grąžinti pretenziją**)
1. Pasirinkite **Kurti**.

Tolesniame paveiksle pateiktas „Azure AD“ B2C profilio redagavimo vartotojo srauto pavyzdys.

![Profilio redagavimo vartotojo srauto kūrimas](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Slaptažodžio nustatymo iš naujo vartotojo srauto strategijos kūrimas

Norėdami sukurti slaptažodžio nustatymo iš naujo vartotojo srauto strategiją, atlikite šiuos veiksmus.

1. „Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.
1. Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.
1. Skirtuke **Rekomenduojama** pasirinkite **Slaptažodžio nustatymas iš naujo**.
1. Dalyje **Pavadinimas** įveskite slaptažodžio nustatymo iš naujo vartotojo srauto pavadinimą.
1. Dalyje **Tapatybės teikimo įrankiai** pasirinkite **Iš naujo nustatyti slaptažodį naudojant el. pašto adresą**.
1. Pasirinkite **Kurti**.
1. Dalyje **Programos teiginiai** pažymėkite bet kurį iš šių žymės langelių:
    - **El. pašto adresai**
    - **Vardas**
    - **Pavardė**
    - **Vartotojo objekto ID**
1. Pasirinkite **Kurti**.

Toliau pateiktame paveiksle parodyta, kur nustatyti **Nustatyti iš naujo slaptažodį naudojant el. pašto adresą** „Azure AD“ B2C vartotojo slaptažodžio nustatymo iš naujo sraute.

![„Nustatyti iš naujo slaptažodį naudojant el. pašto adresą“ nustatymas slaptažodžio nustatymo iš naujo strategijoje](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a>Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)

Socialinės tapatybės teikimo įrankis leidžia vartotojams naudotis savo socialinėmis sąskaitomis autentifikavimo tikslais. Socialinės tapatybės teikimo įrankio autentifikavimo įtraukimas yra pasirinktinis „Dynamics 365 Commerce“. 

Jei nėra įtrauktas socialinės tapatybės teikimo įrankio autentifikavimas, numatytieji „Azure AD“ B2C profiliai bus pagrindiniai vartotojų bazės profiliai. Vartotojai pasirinks savo vartotojo vardą (pageidaujamą el. pašto adresą) ir nustatys slaptažodį. „Azure AD“ B2C autentifikuos vartotojus tiesiogiai. 

Jei įtrauktas socialinės tapatybės teikimo įrankio autentifikavimas ir vartotojas pasirenka vieną iš siūlomų socialinės tapatybės teikimo įrankių, šis objektas vis dar yra sukurtas „Azure AD“ B2C nuomotojuje. „Azure AD“ B2C autentifikuos vartotojo kredencialus naudodama socialinės tapatybė teikimo įrankį,

> [!NOTE]
> Tapatybės teikimo įrankio prisijungimas sukuria įrašą B2C nuomotojuje, tačiau kitu formatu, nei vietos sąskaitos, nes jis iškviečia išorinę socialinės tapatybės teikimo įrankio nuorodą autentifikavimui. Vartotojas gali naudoti tą patį el. pašto adresą visiems socialinės tapatybės teikimo įrankiams, t. y. el. pašto vartotojo vardas, naudojamas autentifikavimui, negali būti unikalus nuomotojui. „Azure AD“ B2C užtikrins tik tai, kad vartotojas turi unikalų el. pašto adresą vietos B2C sąskaitose.

Prieš pridėdami socialinės tapatybės teikimo įrankį autentifikavimo tikslu, turite eiti į tapatybės teikimo įrankio portalą ir nustatyti tapatybės teikimo įrankio programą, kaip nurodyta „Azure AD B2C“ dokumentuose. Saitų į dokumentus sąrašas pateiktas toliau.

- [„Amazon“](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD(Vienas nuomotojas)](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [„Microsoft“ abonementas](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [„LinkedIn“](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [„Twitter“](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Socialinės tapatybės teikimo įrankio įtraukimas ir nustatymas

Norėdami įtraukti ir nustatyti socialinės tapatybės teikimo įrankį, atlikite tolesnius veiksmus.  

1. „Azure“ portale eikite į **Tapatybės teikimo įrankiai**.
1. Pasirinkite **Įtraukti**. Rodomas langas **Įtraukti tapatybės teikimo įrankį**.
1. Dalyje **Pavadinimas** įveskite pavadinimą, kuris bus rodomas vartotojams prisijungimo ekrane.
1. Dalyje **Tapatybės teikimo įrankio tipas** iš sąrašo pasirinkite tapatybės teikimo įrankį.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Nustatyti šį tapatybės teikimo įrankį**, kad būtų atidarytas ekranas **Nustatyti socialinės tapatybės teikimo įrankį**.
1. Dalyje **Kliento ID** įveskite kliento ID, gautą iš tapatybės teikimo įrankio programos sąrankos.
1. Dalyje **Kliento paslaptis** įveskite kliento paslaptį, gautą iš tapatybės teikimo įrankio programos sąrankos.
1. Vartotojo prisiregistravimo ir prisijungimo srauto strategijų pridėjimas:
1. Eikite į **„Azure AD“ B2C – vartotojo srautai (strategijos) \> {jūsų prisiregistravimo ir prisijungimo strategija} \> Tapatybės teikimo įrankiai**.
1. Norėdami pridėti prisiregistravimo / prisijungimo vartotojo srauto strategiją, pasirinkit kiekvieną tapatybės teikimo įrankį, kurį nustatėte savo sąskaitoje. Norėdami tai atlikti, pasirinkite **Vykdyti vartotoją srautą** kiekvienam tapatybės teikimo įrankiui. Naujame skirtuke bus rodomas registravimosi puslapis, kuriame rodomas naujo tapatybės teikimo įrankio langelis.

Tolesniame paveiksle pateikiami ekranų **Įtraukti tapatybės teikimo įrankį** ir **Nustatyti socialinės tapatybės teikimo įrankį** „Azure AD“ B2C.

![Socialinės tapatybės teikimo įrankio įtraukimas į programą](./media/B2CImage_14.png)

Tolesniame paveiksle pateiktas pavyzdys, kaip pasirinkti tapatybės teikimo įrankius „Azure AD“ B2C puslapyje **Tapatybės teikimo įrankiai**.

![Kiekvieno socialinės tapatybės teikimo įrankio pasirinkimas siekiant įjungti strategiją](./media/B2CImage_16.png)

Toliau pateiktame paveikslėlyje parodytas numatytojo prisijungimo ekrano, kuriame rodomas socialinės tapatybės teikimo įrankio prisijungimo mygtukas, pavyzdys.

![Numatytojo prisijungimo ekrano su rodomu socialinės tapatybės teikimo įrankio mygtuku pavyzdys](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>„Commerce“ būstinės naujinimas su nauja „Azure AD B2C“ informacija

Kai užbaigiami pirmiau nurodyti „Azure AD“ B2C paruošimo veiksmai, „Azure AD“ B2C programą reikia užregistruoti jūsų „Dynamics 365 Commerce“ aplinkoje.

Norėdami atnaujinti būstinę su naują „Azure AD“ B2C informaciją, atlikite tolesnius veiksmus.

1. „Commerce“ eikite į **„Commerce“ bendrinti parametrai** ir kairiajame meniu pasirinkite **Tapatybės teikimo įrankiai**.
1. Dalyje **Tapatybės teikimo įrankiai** atlikite tolesnius veiksmus.
    1. Lauke **Leidėjas** įveskite tapatybės teikimo įrankio leidėjo URL. Norėdami rasti savo leidėjo URL, žr. [Leidėjo URL gavimas](#obtain-issuer-url) toliau.
    1. Lauke **Pavadinimas** įveskite savo leidėjo įrašo pavadinimą.
    1. Lauke **Tipas** įveskite **„Azure AD“ B2C (id_token)**.
1. Dalyje **Pasikliaujančios šalys** su anksčiau pasirinktu B2C tapatybės teikimo įrankiu atlikite tolesnius veiksmus.
    1. Lauke **KlientoID** įveskite B2C programos ID. Tai galite rasti savo B2C programos ypatybių puslapio lauke **Programos ID**.
    1. Lauke **Tipas** įveskite **Viešas**.
    1. Lauke **Vartotojo tipas** įveskite **Klientas**.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „Commerce“ ieškos lauke ieškokite **Paskirstymo grafikas**
1. Puslapio **Paskirstymo grafikai** kairiajame naršymo meniu pasirinkite užduotį **1110 visuotinė konfigūracija**.
1. Veiksmų srityje pasirinkite **Vykdyti dabar**.

### <a name="obtain-issuer-url"></a>Leidėjo URL gavimas

Norėdami gauti savo tapatybės teikimo įrankio leidėjo URL, atlikite tolesnius veiksmus.

1. Sukurkite metaduomenų adreso URL toliau nurodytu formatu, naudodami savo B2C nuomotoją ir strategiją:``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Pavyzdys: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Į naršyklės adresų juostą įveskite metaduomenų adreso URL.
1. Metaduomenyse kopijuokite tapatybės teikimo įrankio leidėjo URL (**„leidėjo“** reikšmę).
    - Pavyzdys: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje

Kai jūsų „Azure AD B2C“ nuomotojo sąranka baigta, turite sukonfigūruoti B2C nuomininką „Commerce“ svetainių rengyklėje. Konfigūracijos veiksmai apima B2C programos informacijos iš „Azure“ portalo surinkimą, tos į B2C programos informacijos įvedimą į svetainių daryklę, ir B2C programos susiejimą su jūsų svetaine ir kanalu.

### <a name="collect-the-required-application-information"></a>Reikiamos programos informacijos surinkimas

Norėdami surinkti reikiamą programos informaciją, atlikite tolesnius veiksmus.

1. „Azure“ portale eikite į **Pagrindinis \> „Azure AD“ B2C – programos**.
1. Pasirinkite programą, tada kairiojoje naršymo srityje pasirinkite **Ypatybes**, kad gautumėte programos informaciją.
1. Laukelyje **Programos ID** patikrinkite B2C programos, sukurtos jūsų B2C nuomotojuje, programos ID. Tai vėliau bus įvesta kaip **Kliento GUID** svetainių rengyklėje.
1. Dalyje **Atsakymo URL** surinkite atsakymo URL.
1. Eikite į **Pagrindinis \> „Azure AD“ B2C – vartotojo srautus (strategijos)**, tada surinkite kiekvieno vartotojo srauto strategijos pavadinimus.

Toliau pateiktame paveikslėlyje parodytas puslapio **„Azure AD“ B2C – programos** pavyzdys.

![Perėjimas į B2C programą nuomotojuje](./media/B2CImage_19.png)

Toliau pateiktame paveikslėlyje parodytas programos puslapio **Ypatybės**, esančio „Azure AD“ B2C, pavyzdys. 

![Programos ID kopijavimas iš B2C programos ypatybių](./media/B2CImage_21.png)

Toliau pateiktame paveikslėlyje parodytas vartotojo srauto strategijų puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pavyzdys.

![Visų B2C strategijos srautų pavadinimų rinkimas](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a>AAD B2C nuomotojo programos informacijos įvedimas „Commerce“

Prieš susiedami B2C nuomotoją su savo svetaine (-ėmis), įveskite „Azure AD“ B2C nuomotojo informaciją į „Commerce“ svetainių daryklę.

Norėdami įtraukti AAD B2C nuomotojo programos informaciją į „Commerce“, atlikite toliau nurodytus veiksmus.

1. Prisijunkite kaip administratorius prie savo aplinkos „Commerce“ svetainių daryklėje.
1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Nuomotojo parametrai**.
1. Dalyje **Nuomotojo parametrai** pasirinkite **B2C parametrai**. 
1. Pagrindiniame lange šalia **B2C programos** pasirinkite **Valdyti**. (Jei jūsų nuomotojas yra įtrauktas į B2C programų sąrašą, jį jau įtraukė ir administratorius. Patikrinkite, ar tolesnio 6 veiksmo elementai sutampa su jūsų B2C programa.)
1. Pasirinkite **Įtraukti B2C programą**.
1. Į rodomą formą įveskite toliau nurodytus privalomus elementus naudodami reikšmes iš B2C nuomotojo ir programos. Neprivalomus laukus (be žvaigždutės) galima palikti tuščius.

    - **Programos pavadinimas**: jūsų B2C programos pavadinimas, pavyzdžiui, „Fabrikam B2C“.
    - **Nuomotojo pavadinimas:** B2C nuomotojo pavadinimas (pvz.: naudokite „fabrikam”, jei B2C nuomotojo domenas rodomas kaip „fabrikam.onmicrosoft.com”). 
    - **Pamiršto slaptažodžio strategijos ID**: pamiršto slaptažodžio vartotojo srauto strategijos ID, pavyzdžiui, „B2C_1_PasswordReset“.
    - **Registracijos / prisijungimo strategijos ID**: registracija ir prisijungimas vartotojo srauto strategijos ID, pavyzdžiui, „B2C_1_signup_signin“.
    - **Kliento GUID**: B2C programos ID, pavyzdžiui, „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6“.
    - **Redaguoti profilio strategijos ID**: profilį redaguojančio vartojo srauto strategijos ID, pavyzdžiui, „B2C_1A_ProfileEdit“.

1. Pasirinkite **Gerai**. Dabar sąraše turėtumėte matyti savo B2C programos pavadinimą.
1. Pasirinkite **Įrašyti**, kad įrašytumėte pakeitimus.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C programos susiejimas su svetaine ir kanalu

> [!WARNING]
> Jei jūsų svetainė jau yra susieta su B2C programa, keičiant į kitą B2C programą, bus pašalintos esamos rekomendacijos, nustatytos vartotojams, kurie jau yra prisiregistravę prie šios aplinkos. Pakeitus, bet kokie kredencialai, susieti su šiuo metu priskirta B2C programa, nebus prieinami vartotojams. 
> 
> Atnaujinkite B2C programą, tik jei kanalo B2C programą nustatote pirmą kartą arba jei ketinate turėti vartotojų su naujais prisijungimo prie šio kanalo kredencialais naudojant naują B2C programą. Būkite atsargūs susiedami kanalus su B2C programomis ir duokite aiškius pavadinimus programoms. Jei kanalas nėra susiejamas su B2C programa atliekant tolesnius veiksmus, vartotojai, prisijungiantys prie tokio kanalo, kad patektų į jūsų svetainę, bus įvesti į B2C programą, rodomą kaip **numatytoji** B2C programų sąraše **Nuomotojo parametrai \> B2C parametrai**.

Norėdami susieti B2C programą su svetainę ir kanalu, atlikite tolesnius veiksmus.

1. Eikite į savo svetainę „Commerce“ svetainių daryklėje.
1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.
1. Po **Svetainės parametrai** pasirinkite **Kanalai**.
1. Pagrindiniame lange, dalyje **Kanalai** pasirinkite savo kanalą.
1. Kanalo ypatybių srityje dešinėje pusėje pasirinkite savo B2C programos pavadinimą iš išskleidžiamojo meniu **Pasirinkti B2C programą**.
1. Pasirinkite **Uždaryti**, tada pasirinkite **Įrašyti ir publikuoti**.

## <a name="additional-b2c-information"></a>Papildoma B2C informacija

### <a name="customer-migration"></a>Kliento perkėlimas

Jei ketinate perkelti kliento įrašus iš ankstesnės tapatybės teikimo įrankio platformos, dirbkite su „Dynamics 365 Commerce“ komanda, kad peržiūrėtumėte savo klientų perkėlimo poreikius.

Norėdami gauti daugiau „Azure AD“ B2C dokumentų apie klientų perkėlimą, žr. [Vartotojų perkėlimas į „Azure Active Directory“ B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Pasirinktinės strategijos

Norėdami gauti daugiau informacijos apie „Azure AD“ B2C sąveikas ir strategijos srautus be to, kas siūloma standartinėse B2C strategijose, žr. [Pasirinktinės strategijos „Azure Active Directory“ B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Antrinis administratorius

Pasirinktinio antrinio administratoriaus sąskaita gali būti įtraukta į jūsų B2C nuomotojo skyrių **Vartotojai**. Tai gali būti tiesioginė sąskaita arba bendroji sąskaita. Jei reikia bendrinti sąskaitą su komandos ištekliais, galima sukurti bendrąją sąskaitą. Atsižvelgiant į tai, kad „Azure AD“ B2C saugomi duomenys yra jautrūs, bendroji sąskaita turi būti atidžiai stebima pagal jūsų įmonės saugumo praktiką.

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Talpinkite naują e-komercijos nuomotoją](deploy-ecommerce-site.md)

[Sukurkite e-komercijos saitą](create-ecommerce-site.md)

[Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu](associate-site-online-store.md)

[„robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Įkelkite URL nukreipimus bendrai](upload-bulk-redirects.md) Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2C nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]