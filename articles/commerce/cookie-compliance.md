---
title: Slapukų atitiktis
description: Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.
author: BrianShook
ms.date: 05/21/2021
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
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088392"
---
# <a name="cookie-compliance"></a>Slapukų atitiktis

[!include [banner](includes/banner.md)]

Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.

Kai sekamos technologijos, veikiančios el. prekybos klientus, privatumas yra svarbus veiksnys. Dėl privatumo atitikties standartų, pvz., Europos Sąjungos (ES) bendrojo duomenų apsaugos reglamento (BDAR), administruojant bet kurią šiuo metu aktyvią svetainę reikia apsvarstyti elektroninio privatumo rekomendacijas. Kadangi daugelis el. prekybos svetainių pagal numatytuosius parametrus yra pasiekiamos visame pasaulyje, svarbu peržiūrėti el. prekybos svetainės atitikties standartus.

Norėdami daugiau sužinoti apie pagrindinius „Microsoft“ naudojamus slapukų atitikties principus, apsilankykite [„Microsoft“ patikimumo centre](https://www.microsoft.com/trust-center). Šioje svetainėje taip pat galite gauti daugiau informacijos apie atitikties sritis ir privatumą.

Toliau pateikiamoje lentelėje rodomas dabartinis slapukų nuorodų sąrašas, kuriuos patalpino „Dynamics 365 Commerce” svetainės.

| Slapuko pavadinimas                               | Naudojimas                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Slapukai                             | Parduotuvės „Microsoft Azure Active Directory” („Azure AD”) autentifikavimo slapukai vienkartiniam prisijungimui (SSO). Parduotuvės užšifravo vartotojo pagrindinę informaciją (vardą, pavardę, el. paštą). |
| &#95;msdyn365___krepšelis&#95;                           | Parduotuvės krepšelio ID naudojamas produktų, pridėtų į krepšelio egzempliorių, sąrašui gauti. |
| &#95;msdyn365___ucc&#95;                            | Slapuko atitikties sutikimo sekimas.                          |
| ai_seansas                                  | Aptinka, keliuose vartotojo veiklos seansuose buvo tam tikrų programėlės puslapių ir funkcijų. |
| ai_vartotojas                                     | Aptinka, kaip daug žmonių naudojo programėlę ir jos funkcijas. Vartotojai skaičiuojami naudojant anoniminius ID. |
| b2cru                                       | Saugomas dinamiškai peradresavimo URL.                              |
| JSESSIONID                                  | Mokėjimo jungtis naudoja „Adyen”, kad išsaugotų vartotojo seansą.       |
| AtvertiIdPrijungti.nonce.&#42;                       | Autentifikavimas                                               |
| x-ms-cpim-cache:.&#42;                          | Naudojama užklausos būsenai tvarkyti.                      |
| x-ms-cpim-csrf                              | Kelių svetainių užklausų klastočių (CRSF) atpažinimo ženklas, naudojamas apsaugoti nuo CRSF.     |
| x-ms-cpim-dc                                | Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių. |
| x-ms-cpim-rc.&#42;                              | Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių. |
| x-ms-cpim-slice                             | Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių. |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Naudojama SSO seansui tvarkyti.                        |
| x-ms-cpim-trans                             | Naudojama operacijoms stebėti (atidarytų skirtukų skaičius, kuriais autentifikuojama lyginant su įmonė–vartotojui (B2C) svetaine), įskaitant dabartinę operaciją. |
| „\_msdyn365___muid_”                            | Naudojama, jei aplinkai yra suaktyvintas Eksperimentavimas; naudojamas kaip vartotojo ID eksperimentavimo tikslais. |
| „\_msdyn365___exp_”                             | Naudojama, jei aplinkai yra suaktyvintas Eksperimentavimas; naudojamas matuoti efektyvumo įkelties balansavimui.         |
| „d365mkt”                                       | Naudojama, jei aptikimas pagal vietą, skirtas vartotojo IP adresui sekti dėl parduotuvių vietų pasiūlymų, yra įjungtas „Commerce” svetainių daryklėje: **Svetainės parametrai > Bendra > Įgalinti vieta pagrįstą parduotuvės aptikimą**.      |

Jeigu svetainės vartotojas pasirenka bet kuriuos socialinės medijos saitus svetainėje, šioje lentelėje pateikti slapukai taip pat bus sekami jų naršyklėje.


| Domenas                      | Slapukas               | Aprašas                                                  | Šaltinis                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| „.linkedin.com”                | Vartotojo atitikties istorija         | „LinkedIn” skelbimų ID sinchronizavimas                                      | „LinkedIn” Sklaidos kanalas ir Įžvalgų žymė                                |
| „.linkedin.com”               | „li_sugr”                  | Naršyklės identifikatorius                                           | „LinkedIn” Įžvalgų žymė, jeigu IP adresas nėra priskirtoje šalyje |
| „.linkedin.com”               | Bizografikos atsisakymas       | Nustato atsisakymo būseną trečiosios šalies sekimui.              | „LinkedIn” svečių valdikliai ir industrijos atsisakymo puslapiai           |
| „.linkedin.com”               | „\_guid”                    | Naršyklės identifikatorius, skirtas „Google Ads”.                            | „LinkedIn” Sklaidos kanalas                                                |
| „.linkedin.com”               | „li_oatml”                 | Nario netiesioginis identifikatorius, skirtas konvertavimo sekimui, tiksliniam nukreipimui ir analizei. | „LinkedIn” Skelbimų ir Įžvalgų žymės                                |
| Įvairūs pirmosios šalies domenai | „li_fat_id”                | Nario netiesioginis identifikatorius, skirtas konvertavimo sekimui, tiksliniam nukreipimui ir analizei. | „LinkedIn” Skelbimų ir Įžvalgų žymės                                |
| „.adsymptotic.com”            | U                        | Naršyklės identifikatorius                                           | „LinkedIn” Įžvalgų žymė, jei IP adresas yra nepriskirtoje šalyje |
| „.linkedin.com”                | „bcookie”                  | Naršyklės ID slapukas                                            | Užklausos į „LinkedIn”                                         |
| „.linkedin.com”                | „bscookie”                 | Saugios naršyklės slapukas                                        | Užklausos į „LinkedIn”                                         |
| „.linkedin.com”               | „lang”                     | Nustato numatytąją lokalę ir kalbą.                                 | Užklausos į „LinkedIn”                                         |
| „.linkedin.com”                | „lidc”                     | Naudojama nukreipimui.                                             | Užklausos į „LinkedIn”                                         |
| „.linkedin.com”               | „aam_uuid”                 | „Adobe” auditorijos vadovo slapukas                                                     | ID sinchronizavimo nustatymas                                              |
| „.linkedin.com”               | „\_ga”                      | „Google Analytics“ slapukas                                            | „Google Analytics“                                             |
| „.linkedin.com”               | „\_gat”                     | „Google Analytics“ slapukas                                             | „Google Analytics“                                             |
| „.linkedin.com”               | „liap”                     | „Google Analytics“ slapukas                                             | „Google Analytics“                                             |
| „.linkedin.com”               | „lissc”                    |                                                              |                                                              |
| „.facebook.com”               | „c_user”                   | Slapuke yra šiuo metu prisijungusio vartotojo ID.  |   „Facebook“                                                           |
| „.facebook.com”               | „datr”                     | Naudojama nustatyti žiniatinklio naršyklę, kuri yra naudojama prisijungimui prie „Facebook”, nepriklausomai nuo prisijungusio vartotojo. | „Facebook“                                                             |
| „.facebook.com”               | „wd”                       | Saugo naršyklės lango dimensijas ir yra naudojama „Facebook” puslapio generavimui optimizuoti. | „Facebook“                                                             |
| „.facebook.com”               | „xs”                       | Dviženklis skaičius, nurodantis seanso numerį. Antroji reikšmes dalis yra seanso slaptasis raktas. |  „Facebook“                                                            |
| „.facebook.com”               | fr                       | Apima unikaliuosius naršyklės ir vartotojo ID, naudojamus tikslinei reklamai. |  „Facebook“                                                            |
| „.facebook.com”               | „sb”                       | Naudojama patobulinti „Facebook” draugų pasiūlymus.                                |  „Facebook“                                                            |
| „.facebook.com”               | „spin”                     |                                                              |  „Facebook“                                                            |
| „.twitter.com”                | „guest_id”                 |                                                              |  Twitter                                                            |
| „.twitter.com”                | „kdt”                      |                                                              |  Twitter                                                             |
| „.twitter.com”                | „personalization_id”       | Slapukas apima šiuo metu prisijungusio vartotojo ID.  |  Twitter                                                             |
| „.twitter.com”                | „remember_checked_on”      |                                                              | Twitter                                                              |
| „.twitter.com”                | „twid”                     |                                                              |  Twitter                                                             |
| „.pinterest.com”              | „\_auth”                    | Slapuke yra šiuo metu prisijungusio vartotojo ID.  |   „Pinterest”                                                           |
| „.pinterest.com”              | „\_ b”                       |                                                              |   „Pinterest”                                                           |
| „.pinterest.com”              | „\_pinterest_pfob”          |                                                              |  „Pinterest”                                                            |
| „.pinterest.com”              | „\_pinterest_referrer”      | Slapukai apima puslapius, kai vartotojas pasirenka „Pinterest” mygtuką.      |  „Pinterest”                                                            |
| „.pinterest.com”              | „\_pinterest_sess”          | Slapukai apima puslapius, kai vartotojas pasirenka „Pinterest” mygtuką.      |  „Pinterest”                                                            |
| „.pinterest.com”              | „\_routing_id”              |                                                              |  „Pinterest”                                                            |
| „.pinterest.com”              | „bei”                      |                                                              |  „Pinterest”                                                            |
| „.pinterest.com”              | „cm_sub”                   | Apima vartotojo ID ir slapuko sukūrimo laiko žymą. |  „Pinterest”                                                            |
| „.pinterest.com”              | „csrftoken”                | Slapukai apima puslapius, kai vartotojas pasirenka „Pinterest” mygtuką.      | „Pinterest”                                                             |
| „.pinterest.com”              | „sessionFunnelEventLogged” | Slapukai apima puslapius, kai vartotojas pasirenka „Pinterest” mygtuką.      | „Pinterest”                                                             |
| „.pinterest.com”              | Vietinė saugykla            |                                                              |  „Pinterest”                                                            |
| „.pinterest.com”              | Tarnybos darbuotojai          |                                                              |  „Pinterest”                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Svetainės vartotojo sutikimas dėl slapukų „e-Commerce” svetainėje 

Jei „e-Commerce” svetainės funkcija ar modulis naudoja nepagrindinius slapukus, prieš naudojant juos reikia gauti svetainės vartotojo sutikimą. Norint leisti svetainės vartotojams pateikti sutikimą dėl slapukų „e-Commerce” svetainėje, svetainės autorius turi įtraukti ir konfigūruoti sutikimo dėl slapukų modulį puslapio antraštės modulyje, kad būtų užtikrinta, jog sutikimo reikalaujama ir jis gaunamas. Svetainės vartotojo sutikimas turi būti suteiktas prieš funkcijos arba modulio, naudojančio nepagrindinius slapukus, atvaizdavimą svetainės puslapyje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pritaikymo neįgaliesiems funkcijos ir galimybės](accessibility.md)

[Atitikties peržiūra](compliance-overview.md)

[Privatumo strategijos puslapio įtraukimas](add-privacy-page.md)

[Su sekamais turinio pakeitimais susietų vartotojo ID keitimas](replace-IDs-tracked-changes.md)

[Sutikimo dėl slapukų modulis](cookie-consent-module.md) 
 
[Antraštės modulis](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
