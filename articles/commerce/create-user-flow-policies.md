---
title: Vartotojo srauto strategijų kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti vartotojų srauto strategijas portale Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785829"
---
# <a name="create-user-flow-policies"></a>Vartotojo srauto strategijų kūrimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti vartotojų srauto strategijas portale Microsoft Azure.

Vartotojų srautai – tai Azure Active Directory strategijos (Azure AD) "verslas vartotojui" (B2C), naudojamos siekiant pateikti saugią prisijungimo informaciją, registruotis, redaguoti profilį ir pamiršti slaptažodžio naudojimo patirtį. „Dynamics 365 Commerce“ naudoja šiuos srautus, kad galėtų atlikti strategijos veiksmus, skirtus sąveikauti „Azure AD“ B2C nuomotoju. Kai vartotojas bendrauja su šiomis strategijas, jis peradresuoja į Azure AD B2C nuomininką, kad galėtų atlikti veiksmus.

„Azure AD“ B2C pateikiami trys pagrindiniai vartotojo srautų tipai:
- Prisiregistravimas ir prisijungimas
- Profilio redagavimas
- Slaptažodžio nustatymas iš naujo

Galite pasirinkti naudoti numatytuosius vartotojų srautus, kuriuos teikia Azure AD, o taip bus rodomas Azure AD B2C nuomojamas puslapis. Arba galite sukurti HTML puslapį, kad galėtumėte valdyti šios vartotojo srauto patirties apipavidalinimą. 

Norėdami tinkinti vartotojo strategijos puslapius su „Dynamics 365 Commerce“ platformoje sukurtais puslapiais, skaitykite [Pasirinktinių puslapių nustatymas vartotojų prisijungimui](custom-pages-user-logins.md). Norėdami gauti daugiau informacijos, žr [. Tinkinti vartotojo patirties Azure Active Directory B2C sąsają](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Sukurti prisiregistrėjimo ir prisijungimo vartotojų eigos strategiją

Norėdami sukurti prisijungimo ir prisijungimo vartotojų srautų strategiją, atlikite šiuos veiksmus.

1. „Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.
1. Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.
1. Pasirinkite **Registravimosi ir prisijungimo** strategiją, o tada pasirinkite **Rekomenduojamą** versiją.
1. Dalyje **Pavadinimas** įveskite strategijos pavadinimą. Šis pavadinimas bus rodomas su prievardžiu, kurį priskyrė portalas (pavyzdžiui, „B2C_1_“).
1. **Skyriaus Vietinės** sąskaitos dalyje Tapatybės **teikėjai pasirinkite** Registruotis el **. paštu**. El. laiškų autentifikavimas naudojamas dažniausiais "Commerce" scenarijais. Jei naudojate ir socialinio tapatybės tiekėjo autentifikavimą, šiuo metu galite pasirinkti juos.
1. Dalyje **Kelių faktorių autentifikavimas** atlikite pasirinkimą pagal savo įmonę. 
1. Dalyje **Vartotojo atributai ir pretenzijos** pasirinkite pasirinktis, kad būtų galima rinkti atributus arba grąžinti pretenzijas, kaip tinkama. Pasirinkite **Rodyti daugiau... Norėdami** gauti visą atributų ir paraiškos pasirinkčių sąrašą. „Commerce“ reikia nustatyti tolesnes numatytąsias parinktis:

    | **Rinkti atributą** | **Grąžinti pretenziją** |
    | ---------------------- | ----------------- |
    | El. pašto adresas          | El. pašto adresai   |
    | Vardas             | Vardas        |
    |                        | Tapatybės teikėjas |
    | Pavardė                | Pavardė           |
    |                        | Vartotojo objekto ID  |

1. Pasirinkite **Kurti**.

Toliau pateiktas vaizdas yra Azure AD B2C prisijungimo ir vartotojų prisijungimo srauto pavyzdys.

![Prisiregistravimo ir prisijungimo strategijos parametrai.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Profilio redagavimo vartotojo srauto strategijos kūrimas

Norėdami sukurti profilio redagavimo vartotojo srauto strategiją, atlikite šiuos veiksmus.

1. „Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.
1. Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.
1. Pasirinkite **Profilio redagavimas**, o tada pasirinkite **Rekomenduojamą** versiją.
1. Dalyje **Pavadinimas** įveskite profilio redagavimo vartotojo srautą. Šis pavadinimas bus rodomas su prievardžiu, kurį priskyrė portalas (pavyzdžiui, „B2C_1_“).
1. Dalies Tapatybės **teikėjai skyriuje** Vietinės sąskaitos **pasirinkite** El. pašto **prisijungimas**.
1. Dalyje **Vartotojo atributai** pažymėkite bet kurį iš šių žymės langelių:
    
    | **Rinkti atributą** | **Grąžinti pretenziją** |
    | ---------------------- | ----------------- |
    |                        | El. pašto adresai   |
    | Vardas             | Vardas        |
    |                        | Tapatybės teikėjas |
    | Pavardė                | Pavardė           |
    |                        | Vartotojo objekto ID  |
    
1. Pasirinkite **Kurti**.

Tolesniame paveiksle pateiktas „Azure AD“ B2C profilio redagavimo vartotojo srauto pavyzdys.

![Azure AD B2C šablono vartotojų srauto redagavimo pavyzdys](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Slaptažodžio nustatymo iš naujo vartotojo srauto strategijos kūrimas

Norėdami sukurti slaptažodžio nustatymo iš naujo vartotojo srauto strategiją, atlikite šiuos veiksmus.

1. „Azure“ portale kairiojoje naršymo srityje pasirinkite **Vartotojo srautai (strategijos)**.
1. Puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pasirinkite **Naujas vartotojo srautas**.
1. Pasirinkite **Slaptažodžio nustatymas iš naujo**, o tada pasirinkite **Rekomenduojamą** versiją.
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

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti B2C nuomininkų nustatymo "Commerce" procesą, tęskite socialinio tapatybės [teikėjų pridėjimą](add-social-identity-providers.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” B2C nuomotojo sąranka](set-up-b2c-tenant.md)

[Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale](create-link-aad-b2c-tenant.md)

[B2C programos kūrimas](create-b2c-app.md)

[Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)](add-social-identity-providers.md)

[Naujinti "Commerce Headquarters" naudojant naują Azure AD B2C informaciją](update-hq-aad-b2c-info.md)

[Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje](config-b2c-tenant-site-builder.md)

[Papildoma B2C informacija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
