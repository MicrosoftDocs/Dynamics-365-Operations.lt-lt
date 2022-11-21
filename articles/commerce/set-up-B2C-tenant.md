---
title: „Commerce” B2C nuomotojo sąranka
description: Šiame straipsnyje aprašoma, kaip nustatyti savo Azure Active Directory (Azure AD) nuo verslo įmonių (B2C) nuomininkus, kad būtų galima autentifikuoti vartotojų svetainę Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785147"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>„Commerce” B2C nuomotojo sąranka

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti savo Azure Active Directory (Azure AD) nuo verslo įmonių (B2C) nuomininkus, kad būtų galima autentifikuoti vartotojų svetainę Dynamics 365 Commerce.

„Dynamics 365 Commerce“ naudoja „Azure AD“ B2C, kad palaikytų vartotojo kredencialus ir autentifikavimo srautus. Vartotojas gali prisiregistruoti, prisijungti ir iš naujo nustatyti savo slaptažodį naudodamas šiuos srautus. „Azure AD“ B2C saugoma vartotojo slapto autentifikavimo informacija, pvz., vartotojo vardas ir slaptažodis. Vartotoje įraše B2C nuomotojuje bus saugomas arba B2C vietos sąskaitos įrašas arba B2C socialinės tapatybės teikimo įrankio įrašas. Šie B2C įrašai bus susieti su kliento įrašu „Commerce“ aplinkoje.

> [!WARNING] 
> „Azure AD B2C” panaikins senus (senstelėjusius) vartotojų srautus 2021 m. rugpjūčio mėnesio 1 d. Todėl turėtumėte planuoti perkelti savo vartotojų srautus į naują rekomenduojamą versiją. Nauja versija suteikia lygiavertiškas bei naujas funkcijas. „Commerce” 10.0.15 arba naujesnės versijos modulių biblioteka turi būti naudojama su rekomenduojamais B2C vartotojų srautais. Daugiau informacijos rasite [„Azure Active Directory B2C” vartotojų srautai](/azure/active-directory-b2c/user-flow-overview).
 
 > [!NOTE]
 > Į „Commerce” vertinimo aplinkas yra iš anksto įkeltas „Azure AD B2C” nuomotojas demonstraciniais tikslais. Vertinimo aplinkose nėra būtina įkelti savo „Azure AD B2C” nuomotojo atliekant žemiau nurodytus veiksmus.

> [!TIP]
> Galite toliau apsaugoti savo svetainės vartotojus ir padidinti savo B2C nuomininkų saugą „Azure AD“ naudodami tapatybės „Azure AD“ apsaugą ir sąlyginę prieigą. Norėdami peržiūrėti B2C priedų P1 ir P2 priedų nuomininkų pajėgumus, žr. B2C „Azure AD“ [tapatybės apsaugą ir „Azure AD“ sąlyginę prieigą](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>„Dynamics" aplinkos būtinosios sąlygos

Prieš pradėdami įsitikinkite, kad jūsų aplinka ir el. komercijos kanalas sukonfigūruoti „Dynamics 365 Commerce“ tinkamai, vykdydami nurodytas būtinąsias sąlygas.

- Nustatykite POS operacijas **AllowAnonymousAccess** vertę į „1" „Commerce headquarters“:
    1. Eiti į **EKA operacijas**.
    1. Operacijų tinklelyje, paspauskite dešinį klavišą ir rinkitės **Pritaikyti**.
    1. Pasirinkite **Įtraukti lauką**.
    1. Galimų stulpelių sąraše pasirinkite stulpelį **AllowAnonymousAccess,** kad jį įtraukdami.
    1. Pasirinkite **Naujinti**.
    1. Dėl **612** operacijos „Kliento įtraukimas" pakeiskite **AllowAnonymousAccess** į „1."
    1. Paleisti **1090 (registrai)** darbą.
- Nustatykite skaičių seką kliento sąskaitai **Rankinis** savybę į **Ne** „Commerce headquarters“:
    1. Eikite į **„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> Sąskaitos gaunami parametrai**.
    1. Pasirinkite **Skaičių sekos**.
    1. Kliento **sąskaitos eilutėje** du kartus spustelėkite **numeracijos kodo vertę**.
    1. Numeracijos **bendrajame** „FastTab“ nustatykite **Rankinis** kaip **Ne**.

Įdiegus „Dynamics 365 Commerce“ aplinką, taip pat rekomenduojama inicijuoti [pradinius duomenis aplinkoje](enable-configure-retail-functionality.md).

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti B2C nuomininko nustatymo "Commerce" procesą, tęskite veiksmus, [Azure AD kad sukurtumėte arba susietumėte su esamu B2C nuomininku "Azure" portale](create-link-aad-b2c-tenant.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale](create-link-aad-b2c-tenant.md)

[B2C programos kūrimas](create-b2c-app.md)

[Vartotojo srauto strategijų kūrimas](create-user-flow-policies.md)

[Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)](add-social-identity-providers.md)

[Naujinti "Commerce Headquarters" naudojant naują Azure AD B2C informaciją](update-hq-aad-b2c-info.md)

[Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje](config-b2c-tenant-site-builder.md)

[Papildoma B2C informacija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
