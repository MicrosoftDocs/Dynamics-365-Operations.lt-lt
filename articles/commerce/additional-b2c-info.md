---
title: Papildoma B2C informacija
description: Šiame straipsnyje pateikiama papildoma informacija, kaip nustatyti savo įmonę vartotojui (B2C) nuomininką Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785823"
---
# <a name="additional-b2c-information"></a>Papildoma B2C informacija

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama papildoma informacija, kaip nustatyti savo įmonę vartotojui (B2C) nuomininką Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>Kliento perkėlimas

Jei ketinate perkelti kliento įrašus iš ankstesnės tapatybės teikimo įrankio platformos, dirbkite su „Dynamics 365 Commerce“ komanda, kad peržiūrėtumėte savo klientų perkėlimo poreikius.

Norėdami gauti daugiau „Azure AD“ B2C dokumentų apie klientų perkėlimą, žr. [Vartotojų perkėlimas į „Azure Active Directory“ B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Pasirinktinės strategijos

Norėdami gauti daugiau informacijos apie „Azure AD“ B2C sąveikas ir strategijos srautus be to, kas siūloma standartinėse B2C strategijose, žr. [Pasirinktinės strategijos „Azure Active Directory“ B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Antrinis administratorius

Pasirinktinio antrinio administratoriaus sąskaita gali būti įtraukta į jūsų B2C nuomotojo skyrių **Vartotojai**. Tai gali būti tiesioginė sąskaita arba bendroji sąskaita. Jei reikia bendrinti sąskaitą su komandos ištekliais, galima sukurti bendrąją sąskaitą. Atsižvelgiant į tai, kad „Azure AD“ B2C saugomi duomenys yra jautrūs, bendroji sąskaita turi būti atidžiai stebima pagal jūsų įmonės saugumo praktiką.

### <a name="set-up-a-custom-sign-in-domain"></a>Pasirinktinio prisijungimo domeno nustatymas

Azure AD B2C leidžia nustatyti B2C nuomininkui pritaikytą Azure AD prisijungimo domeną. Instrukcijų ieškokite B2C [pasirinktinių domenų Azure Active Directory įgalintas](/azure/active-directory-b2c/custom-domain). 

Jei naudojate pasirinktinį prisijungimo domeną, domenas turi būti įvestas į "Commerce" svetainės generatorių.

Norėdami įvesti pasirinktinį prisijungimo domeną svetainės generatoriuje, atlikite šiuos veiksmus.

1. Viršutiniame dešiniajame svetainės generatoriaus kampe pasirinkite svetainės perjungimo priemonę ir pasirinkite Tvarkyti **svetaines**.
1. Kairiajame naršymo lange pasirinkite nuomininkų **parametrų svetainės \> autentifikavimo nustatymą**.
1. Skyriuje Svetainės **autentifikavimo profiliai** pasirinkite **Tvarkyti**.
1. Iškmesdami meniu dešinėje pasirinkite mygtuką Redaguoti (simbolių blokavimas), esantį šalia svetainės autentifikavimo profilio, **kurio** pasirinktinį domeną norite įvesti.
1. Svetainės autentifikavimo **profilio** **redagavimo** dialogo lange dalyje Registruoti pasirinktinį domeną įveskite pasirinktinį prisijungimo domeną (pvz., "login.fabrikam.com").

> [!WARNING]
> Kai atnaujinate B2C Azure AD nuomininko pasirinktinį domeną, pakeitimas pakeičia sugeneruoto atpažinimo ženklo nuomininko informaciją. Tada išdavėjo informacija apims pasirinktinį domeną, o ne numatytąjį domeną, pateiktą Azure AD B2C. Kita "**Commerce** Headquarters" išdavėjo konfigūracija ("Retail" ir "**Commerce Headquarters \>\>" nustatymo parametrai "Commerce \>\> Shared Parameters Identity Providers**") pakeičia sistemos sąveiką su svetainės vartotojais, gali sukurti naują kliento įrašą, jei vartotojas autentifikuoja naują išdavėją. Prieš pereinant prie pasirinktinio domeno tiesioginėje B2C aplinkoje, būtina atidžiai patikrinti bet kokius pasirinktinio Azure AD domeno pakeitimus.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” B2C nuomotojo sąranka](set-up-b2c-tenant.md)

[Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale](create-link-aad-b2c-tenant.md)

[B2C programos kūrimas](create-b2c-app.md)

[Vartotojo srauto strategijų kūrimas](create-user-flow-policies.md)

[Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)](add-social-identity-providers.md)

[Naujinti "Commerce Headquarters" naudojant naują Azure AD B2C informaciją](update-hq-aad-b2c-info.md)

[Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
