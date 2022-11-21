---
title: „Commerce“ būstinės naujinimas su nauja „Azure AD B2C“ informacija
description: Šiame straipsnyje aprašoma, kaip atnaujinti Microsoft Dynamics 365 Commerce būstinę nauja Azure Active Directory (Azure AD) informacija apie verslą (B2C).
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785833"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>„Commerce“ būstinės naujinimas su nauja „Azure AD B2C“ informacija

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip atnaujinti Microsoft Dynamics 365 Commerce būstinę nauja Azure Active Directory (Azure AD) informacija apie verslą (B2C).

Kai užbaigiami pirmiau nurodyti „Azure AD“ B2C paruošimo veiksmai, „Azure AD“ B2C programą reikia užregistruoti jūsų „Dynamics 365 Commerce“ aplinkoje.

Norėdami atnaujinti būstinę su naują „Azure AD“ B2C informaciją, atlikite tolesnius veiksmus.

1. „Commerce“ eikite į **„Commerce“ bendrinti parametrai** ir kairiajame meniu pasirinkite **Tapatybės teikimo įrankiai**.
1. Dalyje **Tapatybės teikimo įrankiai** atlikite tolesnius veiksmus.
    1. Išdavėjo **lauke** įveskite tapatybės teikėjo išdavėjo eilutę. Norėdami rasti savo išdavėjo eilutę, toliau [žr. "Gauti išdavėjo eilutę, kur bus galima nustatyti būstinę](#obtain-issuer-string-for-headquarters-setup) ".
    1. Lauke **Pavadinimas** įveskite savo leidėjo įrašo pavadinimą.
    1. Lauke **Tipas** įveskite **„Azure AD“ B2C (id_token)**.
1. Dalyje **Pasikliaujančios šalys** su anksčiau pasirinktu B2C tapatybės teikimo įrankiu atlikite tolesnius veiksmus.
    1. **ClientID lauke** įveskite savo B2C programos ID, **kurį galite rasti savo B2C programos ypatybės puslapio lauke Programos ID**.
    1. Lauke **Tipas** įveskite **Viešas**.
    1. Lauke **Vartotojo tipas** įveskite **Klientas**.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „Commerce“ ieškos lauke ieškokite **Paskirstymo grafikas**
1. Puslapio **Paskirstymo grafikai** kairiajame naršymo meniu pasirinkite užduotį **1110 visuotinė konfigūracija**.
1. Veiksmų srityje pasirinkite **Vykdyti dabar**.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Gauti būstinės sąrankos išdavėjo eilutę

Norėdami gauti savo tapatybės teikėjo išdavėjo eilutę, atlikite šiuos veiksmus.

1. „Azure” portalo puslapyje „Azure AD B2C” pereikite prie savo **Registravimosi ir prisijungimo** vartotojo srauto.
1. Kairiajame naršymo meniu pasirinkite **Puslapio maketai**, o tada dalyje **Maketo pavadinimas** pasirinkite **Bendras registravimosi arba prisijungimo puslapis** ir **Vykdyti vartotojo srautą**.
1. Įsitikinkite, kad jūsų programa nustatyta Azure AD į anksčiau sukurtą numatomą B2C programą, tada pasirinkite vartotojų srauto saitą, **kuris rodomas dalyje Vykdyti vartotojų** srauto antraštę, kuri apima ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``. (Nesrinkite **Paleisti vartotojų srautą**.) Atidaromas naujas skirtukas, rodomi strategijos metaduomenys, skirti rinkti išdavėjo eilutę.
1. Jūsų naršyklės skirtuke rodome metaduomenų puslapyje nukopijuokite tapatybės teikėjo išdavėjo eilutę (**išdavėjo** vertę, prasidedanti "https://" ir baigiant "/v2.0/"), kuri atrodo panašiai kaip šiame pavyzdyje.
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**ARBA**: Norėdami sukurti tą patį metaduomenų URL rankiniu būdu, atlikite šiuos veiksmus.

1. Sukurkite metaduomenų adreso URL toliau nurodytu formatu, naudodami savo B2C nuomotoją ir strategiją:``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Pavyzdys: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Į naršyklės adresų juostą įveskite metaduomenų adreso URL.
1. Metaduomenyse kopijuokite tapatybės teikimo įrankio leidėjo URL (**„leidėjo“** reikšmę).
    - Pavyzdys: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti B2C nuomininkų nustatymo "Commerce" procesą, [tęskite B2C nuomininkų konfigūravimą "Commerce Site Builder"](config-b2c-tenant-site-builder.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” B2C nuomotojo sąranka](set-up-b2c-tenant.md)

[Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale](create-link-aad-b2c-tenant.md)

[B2C programos kūrimas](create-b2c-app.md)

[Vartotojo srauto strategijų kūrimas](create-user-flow-policies.md)

[Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)](add-social-identity-providers.md)

[Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje](config-b2c-tenant-site-builder.md)

[Papildoma B2C informacija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
