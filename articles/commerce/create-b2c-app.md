---
title: B2C programos kūrimas
description: Šiame straipsnyje aprašoma, kaip portale sukurti programą "verslas vartotojui" Microsoft Azure (B2C).
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785825"
---
# <a name="create-a-b2c-application"></a>B2C programos kūrimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip portale sukurti programą "verslas vartotojui" Microsoft Azure (B2C).

Sukūrę savo B2C nuomininką, turėsite sukurti B2C Azure Active Directory programą savo naujame (Azure AD) nuomininke, kuris sąveikaus su Commerce.

Norėdami sukurti B2C programą, atlikite tolesnius veiksmus.

1. „Azure“ portale pasirinkite **Programų registracijos**, o tada pasirinkite **Nauja registracija**.
1. Dalyje **Pavadinimas** įveskite „Azure AD B2C” programai suteikiamą pavadinimą.
1. Dalyje **Palaikomi abonementų tipai** pasirinkite **Abonementai bet kuriame tapatybės teikėjo arba organizacijos kataloge (vartotojų su vartotojų srautais autentifikavimui)**.
1. Dalyje **Peradresavimo URI** įveskite jūsų paskirto atsakymo URL kaip **Žiniatinklio** tipą. Daugiau informacijos apie atsakymo URL ir kaip juos formatuoti, rasite [Atsakymo URL](#reply-urls) žemiau. Reikia įvesti nukreipimo URI / atsakymo URL Azure AD, kad įgalinant nukreipimus iš B2C atgal į jūsų svetainę, kai autentifikuoja vartotojas. Atsakymo URL gali būti pridėtas per registracijos procesą arba **jis gali būti pridėtas** vėliau pasirenkant saitą Įtraukti nukreipimo **URI** **iš meniu Apžvalga, B2C programos peržiūros skyriuje.**
1. Dalyje **Teisės** pasirinkite **Suteikti administratoriaus sutikimą „OpenID” ir prieigos neprisijungus teisėms**.
1. Pasirinkite **Registruotis**.
1. Pasirinkite naujai sukurtą programą ir pereikite į autentifikavimo **meniu**. 
1. Jei įvestas atsakymo URL, **dalyje Netiesiogiai subsidijos ir "pasirinktys" pasirinkite** **ir prieigos atpažinimo ženklų, ir ID atpažinimo ženklų pasirinktis** **·**, kad įgalintumėte juos programai, tada pasirinkite **Įrašyti.** Jei registruojant atsakymo URL nebuvo įvestas, **jį taip pat galima įtraukti į šį puslapį: pasirinkti Įtraukti platformą**, **pasirinkti** Internetą ir įvesti programos nukreipimo URI. Tada **skyrius Netiesiogiai subsidijos ir sekos** bus galimas ir prieigos atpažinimo **ženklų, ir ID atpažinimo** **ženklų pasirinktims** pasirinkti.
1. Eikite į „Azure” portalo **Apžvalgos** meniu ir nukopijuokite **Programos (kliento) ID**. Pasižymėkite šį ID, nes jis bus reikalingas kitiems nustatymo veiksmams (toliau nurodytą kaip **Kliento GUID**).

Papildomų nuorodų apie „Azure AD B2C” programos registracijas rasite [Nauja programų registracijų patirtis „Azure Active Directory B2C”](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Atsakymo URL

Atsakymo URL yra svarbūs, nes jie suteikia leidžiamų grąžinimo domenų sąrašą, kai jūsų svetainė reikalauja „Azure AD“ B2C, kad būtų autentifikuotas vartotojas. Tai leidžia autentifikuoti vartotoją grąžinti į domeną, iš kurio jis prisijungė (jūsų svetainės domenas). 

Lauke **Atsakymo URL** ekrane **„Azure AD“ B2c – programos \> Nauja programa** turite įtraukti atskiras eilutes tiek svetainės domenui, tiek (kai jūsų aplinka paruošta) „Commerce“ sugeneruotam URL. Šie URL turi visada naudoti tinkamą URL formatą ir jie turi būti tik pagrindiniai URL (nėra pasvirųjų brūkšnių ar maršrutų). Tada eilutę ``/_msdyn365/authresp`` reikia pridėti prie pagrindinių URL, kaip tolesniuose pavyzdžiuose.

- ``https://www.fabrikam.com/_msdyn365/authresp`` (Domenas turi visiškai sutapti su „E-commerce“ domenu. Jei turite kelis domenus, turite įtraukti šį URL į kiekvieną domeną.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti B2C nuomininkų nustatymo komercijos procesą, tęskite vartotojų srautų [strategijų kūrimo procesą](create-user-flow-policies.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” B2C nuomotojo sąranka](set-up-b2c-tenant.md)

[Kurti arba susieti su esamu Azure AD B2C nuomininku "Azure" portale](create-link-aad-b2c-tenant.md)

[Vartotojo srauto strategijų kūrimas](create-user-flow-policies.md)

[Socialinės tapatybės teikimo įrankio įtraukimas (pasirinktinai)](add-social-identity-providers.md)

[Naujinti "Commerce Headquarters" naudojant naują Azure AD B2C informaciją](update-hq-aad-b2c-info.md)

[Konfigūruokite B2C nuomotoją „Commerce“ svetainių daryklėje](config-b2c-tenant-site-builder.md)

[Papildoma B2C informacija](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
