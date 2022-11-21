---
title: Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje
description: Šiame straipsnyje aprašoma, kaip konfigūruoti savo verslo įmonių (B2C) nuomininkus svetainės Microsoft Dynamics 365 Commerce generatoriuje.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785832"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti savo verslo įmonių (B2C) nuomininkus svetainės Microsoft Dynamics 365 Commerce generatoriuje.

Kai jūsų „Azure AD B2C“ nuomotojo sąranka baigta, turite sukonfigūruoti B2C nuomininką „Commerce“ svetainių rengyklėje. Konfigūracijos veiksmai apima B2C programos informacijos iš „Azure“ portalo surinkimą, tos į B2C programos informacijos įvedimą į svetainių daryklę, ir B2C programos susiejimą su jūsų svetaine ir kanalu.

### <a name="collect-the-required-application-information"></a>Reikiamos programos informacijos surinkimas

Norėdami surinkti reikiamą programos informaciją, atlikite tolesnius veiksmus.

1. "Azure" portale eikite į **B2C \>Azure AD pagrindinis puslapis – programos registracijos**.
1. Norėdami gauti programos informaciją, pasirinkite savo programą, o tada kairiojoje **naršymo** srityje pasirinkite Peržiūra.
1. Iš programos **(kliento) ID nuorodos surinkkite B2C programos, sukurtos jūsų B2C nuomininke, programos ID**. Tai vėliau bus įvesta kaip **Kliento GUID** svetainių rengyklėje.
1. Pasirinkite **nukreipimo URL** ir surinkkite atsakymo URL, rodomą jūsų svetainei (atsakymo URL, įvestą nustatymo metu).
1. Eikite **į Pagrindinį \>Azure AD B2C – Vartotojo** srautai, tada surinkkite visus kiekvienos vartotojo eigos strategijos pavadinimus.

Toliau pateiktame paveikslėlyje pateikiamas **Azure AD B2C – programos registracijų apžvalgos** puslapio pavyzdys.

![Azure AD B2C – programos registracijų peržiūros puslapis su išryškintu programos (kliento) ID](./media/ClientGUID_Application_AzurePortal.png)

Toliau pateiktame paveikslėlyje parodytas vartotojo srauto strategijų puslapyje **„Azure AD“ B2C – vartotojo srautai (strategijos)** pavyzdys.

![Visų B2C strategijos srautų pavadinimų rinkimas.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Įveskite savo Azure AD B2C nuomininkų programos informaciją į "Commerce"

Prieš susiedami B2C nuomotoją su savo svetaine (-ėmis), įveskite „Azure AD“ B2C nuomotojo informaciją į „Commerce“ svetainių daryklę.

Norėdami įtraukti savo Azure AD B2C nuomininkų programos informaciją į "Commerce", atlikite šiuos veiksmus.

1. Prisijunkite kaip administratorius prie savo aplinkos „Commerce“ svetainių daryklėje.
1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Nuomotojo parametrai**.
1. Dalyje **Nuomininkų parametrai pasirinkite** Svetainės **autentifikavimo nustatymas**. 
1. Pagrindiniame lange, šalia svetainės autentifikavimo **šablonų**, pasirinkite **Valdyti**. (Jei jūsų nuomininkas pasirodys svetainės autentifikavimo profilių sąraše, jį jau pridėjo administratorius. Patikrinkite, ar toliau atlikdami 6 veiksmą prekės atitinka jūsų numatytas B2C nustatymo prekes. Naujas profilis taip pat gali būti sukurtas Azure AD naudojant panašius B2C nuomininkus arba programas, kad būtų galima atsižvelgti į neesminius skirtumus, pvz., skirtingas vartotojo strategijos ID).
1. Pasirinkite Įtraukti **svetainės autentifikavimo šabloną**.
1. Į rodomą formą įveskite toliau nurodytus privalomus elementus naudodami reikšmes iš B2C nuomotojo ir programos. Neprivalomus laukus (be žvaigždutės) galima palikti tuščius.

    - **Programos pavadinimas**: jūsų B2C programos pavadinimas, pavyzdžiui, „Fabrikam B2C“.
    - **Nuomotojo pavadinimas:** B2C nuomotojo pavadinimas (pvz.: naudokite „fabrikam”, jei B2C nuomotojo domenas rodomas kaip „fabrikam.onmicrosoft.com”). 
    - **Pamiršto slaptažodžio strategijos ID**: pamiršto slaptažodžio vartotojo srauto strategijos ID, pavyzdžiui, „B2C_1_PasswordReset“.
    - **Registracijos pasirašant strategijos ID**: prisiregistrėjimo ir prisijungimo vartotojo srauto strategijos ID, pvz., "B2C_1_signup_signin".
    - **Kliento GUID**: B2C programos ID, pavyzdžiui, „22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6“.
    - **Redaguoti profilio strategijos ID**: profilį redaguojančio vartojo srauto strategijos ID, pavyzdžiui, „B2C_1A_ProfileEdit“.

1. Pasirinkite **Gerai**. Dabar sąraše turėtumėte matyti savo B2C programos pavadinimą.
1. Pasirinkite **Įrašyti**, kad įrašytumėte pakeitimus.

Pasirinktinis **pasirinktinio prisijungimo** domeno laukas turi Azure AD būti naudojamas, tik jei nustatote B2C nuomininko pasirinktinį domeną. Papildomos informacijos ir aplinkybės, susijusios su pasirinktinio domeno **registravimosi lauko** naudojimu, ieškokite [papildoma B2C informacija](additional-b2c-info.md).

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C programos susiejimas su svetaine ir kanalu

> [!WARNING]
> - Jei jūsų svetainė jau yra susieta su B2C programa, keičiant į kitą B2C programą, bus pašalintos esamos rekomendacijos, nustatytos vartotojams, kurie jau yra prisiregistravę prie šios aplinkos. Pakeitus, bet kokie kredencialai, susieti su šiuo metu priskirta B2C programa, nebus prieinami vartotojams. 
> - Atnaujinkite B2C programą tik tada, jei kanalo B2C programą nustatote pirmą kartą arba jei ketinate, kad vartotojai vėl prisiregistruotų naudodami naujus šio kanalo kredencialus naudodami naują B2C programą. Būkite atsargūs susiedami kanalus su B2C programomis ir duokite aiškius pavadinimus programoms. Jei kanalas nėra susiejamas su B2C programa atliekant tolesnius veiksmus, vartotojai, prisijungiantys prie tokio kanalo, kad patektų į jūsų svetainę, bus įvesti į B2C programą, rodomą kaip **numatytoji** B2C programų sąraše **Nuomotojo parametrai \> B2C parametrai**.

Norėdami susieti B2C programą su svetainę ir kanalu, atlikite tolesnius veiksmus.

1. Eikite į savo svetainę „Commerce“ svetainių daryklėje.
1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.
1. Po **Svetainės parametrai** pasirinkite **Kanalai**.
1. Pagrindiniame lange, dalyje **Kanalai** pasirinkite savo kanalą.
1. Kanalo ypatybės srityje dešinėje, išplečiamajame meniu Pasirinkti B2C **programą pasirinkite savo B2C** programos pavadinimą.
1. Pasirinkite **Uždaryti**, tada pasirinkite **Įrašyti ir publikuoti**.

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti B2C nuomininkų nustatymo komercijoje procesą, pereikite prie [papildomos B2C informacijos](additional-b2c-info.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” B2C nuomotojo sąranka](set-up-b2c-tenant.md)

[Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale](create-link-aad-b2c-tenant.md)

[B2C programos kūrimas](create-b2c-app.md)

[Vartotojo srauto strategijų kūrimas](create-user-flow-policies.md)

[Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)](add-social-identity-providers.md)

[Naujinti "Commerce Headquarters" naudojant naują Azure AD B2C informaciją](update-hq-aad-b2c-info.md)

[Papildoma B2C informacija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
