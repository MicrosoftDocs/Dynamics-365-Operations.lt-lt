---
title: Įtraukti socialinio identifikavimo teikėjus
description: Šiame straipsnyje aprašoma, kaip į portalą įtraukti socialinio identifikavimo teikėjus Microsoft Azure.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785824"
---
# <a name="add-social-identity-providers"></a>Įtraukti socialinio identifikavimo teikėjus

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip į portalą įtraukti socialinio identifikavimo teikėjus Microsoft Azure.

Socialinės tapatybės teikimo įrankis leidžia vartotojams naudotis savo socialinėmis sąskaitomis autentifikavimo tikslais. Socialinės tapatybės teikimo įrankio autentifikavimo įtraukimas yra pasirinktinis „Dynamics 365 Commerce“. 

Jei socialinio tapatybės teikėjo autentifikavimas nepridėtas, Azure Active Directory numatytieji (Azure AD) B2C profiliai bus pagrindiniai jūsų vartotojo pagrindo profiliai. Vartotojai pasirinks savo vartotojo vardą (pageidaujamą el. pašto adresą) ir nustatys slaptažodį. „Azure AD“ B2C autentifikuos vartotojus tiesiogiai. 

Jei įtrauktas socialinės tapatybės teikimo įrankio autentifikavimas ir vartotojas pasirenka vieną iš siūlomų socialinės tapatybės teikimo įrankių, šis objektas vis dar yra sukurtas „Azure AD“ B2C nuomotojuje. „Azure AD“ B2C autentifikuos vartotojo kredencialus naudodama socialinės tapatybė teikimo įrankį,

> [!NOTE]
> Tapatybės teikimo įrankio prisijungimas sukuria įrašą B2C nuomotojuje, tačiau kitu formatu, nei vietos sąskaitos, nes jis iškviečia išorinę socialinės tapatybės teikimo įrankio nuorodą autentifikavimui. Vartotojas gali naudoti tą patį el. pašto adresą visiems socialinės tapatybės teikimo įrankiams, t. y. el. pašto vartotojo vardas, naudojamas autentifikavimui, negali būti unikalus nuomotojui. „Azure AD“ B2C užtikrins tik tai, kad vartotojas turi unikalų el. pašto adresą vietos B2C sąskaitose.

Prieš pridėdami socialinės tapatybės teikimo įrankį autentifikavimo tikslu, turite eiti į tapatybės teikimo įrankio portalą ir nustatyti tapatybės teikimo įrankio programą, kaip nurodyta „Azure AD B2C“ dokumentuose. Saitų į dokumentus sąrašas pateiktas toliau.

- [„Amazon“](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD(Vienas nuomotojas)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [„Microsoft“ abonementas](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [„Facebook“](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [„LinkedIn“](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [„Twitter“](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Socialinės tapatybės teikimo įrankio įtraukimas ir nustatymas

> [!NOTE]
> Įtraukti socialinio tapatybės teikėjus yra pasirinktinis žingsnis, kai nustatomas vartotojas (B2C) nuomininkas Microsoft Dynamics 365 Commerce.

Norėdami įtraukti ir nustatyti socialinės tapatybės teikimo įrankį, atlikite tolesnius veiksmus.  

1. „Azure“ portale eikite į **Tapatybės teikimo įrankiai**.
1. Pasirinkite **Įtraukti**. Rodomas langas **Įtraukti tapatybės teikimo įrankį**.
1. Dalyje **Pavadinimas** įveskite pavadinimą, kuris bus rodomas vartotojams prisijungimo ekrane.
1. Dalyje **Tapatybės teikimo įrankio tipas** iš sąrašo pasirinkite tapatybės teikimo įrankį.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Nustatyti šį tapatybės teikimo įrankį**, kad būtų atidarytas ekranas **Nustatyti socialinės tapatybės teikimo įrankį**.
1. Dalyje **Kliento ID** įveskite kliento ID, gautą iš tapatybės teikimo įrankio programos sąrankos.
1. Dalyje **Kliento paslaptis** įveskite kliento paslaptį, gautą iš tapatybės teikimo įrankio programos sąrankos.
1. Pridėkite vartotojų srautą prisijungimo / prisiregistrimo strategijų:
1. Eikite į **„Azure AD“ B2C – vartotojo srautai (strategijos) \> {jūsų prisiregistravimo ir prisijungimo strategija} \> Tapatybės teikimo įrankiai**.
1. Norėdami pridėti prisijungimo / prisiregistrėjimo vartotojo eigos strategiją, pasirinkite kiekvieną nustatytą sąskaitos tapatybės teikėją. Norėdami patikrinti srautus, pasirinkite **Kiekvienos tapatybės tiekėjo paleisti** vartotojų eigą. Naujas skirtukas rodo prisijungimo puslapį, kuriame rodomas naujos tapatybės tiekėjo pasirinkimo laukas.

Tolesniame paveiksle pateikiami ekranų **Įtraukti tapatybės teikimo įrankį** ir **Nustatyti socialinės tapatybės teikimo įrankį** „Azure AD“ B2C.

![Socialinės tapatybės teikimo įrankio įtraukimas į programą.](./media/B2CImage_14.png)

Tolesniame paveiksle pateiktas pavyzdys, kaip pasirinkti tapatybės teikimo įrankius „Azure AD“ B2C puslapyje **Tapatybės teikimo įrankiai**.

![Kiekvieno socialinės tapatybės teikimo įrankio pasirinkimas siekiant įjungti strategiją.](./media/B2CImage_16.png)

Toliau pateiktame paveikslėlyje parodytas numatytojo prisijungimo ekrano, kuriame rodomas socialinės tapatybės teikimo įrankio prisijungimo mygtukas, pavyzdys.

> [!NOTE]
> Jeigu savo vartotojo srautams naudojate pasirinktinius puslapius, įtaisytus „Commerce”, naudojant „Commerce” modulių bibliotekos išplėtimo funkcijas reikės įtraukti socialinės tapatybės teikėjams skirtus mygtukus. Be to, kai nustatote savo programas su konkrečiu socialinės tapatybės teikėju, kai kuriais atvejais URL ar konfigūracijos eilutės gali skirti didžiąsias ir mažąsias raides. Norėdami gauti daugiau informacijos, vadovaukitės savo socialinės tapatybės teikėjo ryšio instrukcijomis.
 
![Numatytojo prisijungimo ekrano su rodomu socialinės tapatybės teikimo įrankio mygtuku pavyzdys.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti B2C nuomininkų nustatymo "Commerce" procesą, [tęskite "Commerce Headquarters Azure AD " su nauja B2C informacija](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” B2C nuomotojo sąranka](set-up-b2c-tenant.md)

[Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale](create-link-aad-b2c-tenant.md)

[B2C programos kūrimas](create-b2c-app.md)

[Vartotojo srauto strategijų kūrimas](create-user-flow-policies.md)

[Naujinti "Commerce Headquarters" naudojant naują Azure AD B2C informaciją](update-hq-aad-b2c-info.md)

[Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje](config-b2c-tenant-site-builder.md)

[Papildoma B2C informacija](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
