---
title: Slapukų atitiktis
description: Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.
author: BrianShook
ms.date: 03/10/2022
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
ms.openlocfilehash: 2efb866d513ba90630b0397c1ca144c92d40719c
ms.sourcegitcommit: 4645278a4b4a38dcb18fdfb49ce2e276eabb59de
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/11/2022
ms.locfileid: "8403152"
---
# <a name="cookie-compliance"></a>Slapukų atitiktis

[!include [banner](includes/banner.md)]

Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.

Kai sekamos technologijos, veikiančios el. prekybos klientus, privatumas yra svarbus veiksnys. Dėl privatumo atitikties standartų, pvz., Europos Sąjungos (ES) bendrojo duomenų apsaugos reglamento (BDAR), administruojant bet kurią šiuo metu aktyvią svetainę reikia apsvarstyti elektroninio privatumo rekomendacijas. Kadangi daugelis el. prekybos svetainių pagal numatytuosius parametrus yra pasiekiamos visame pasaulyje, svarbu peržiūrėti el. prekybos svetainės atitikties standartus.

Norėdami daugiau sužinoti apie pagrindinius „Microsoft“ naudojamus slapukų atitikties principus, apsilankykite [„Microsoft“ patikimumo centre](https://www.microsoft.com/trust-center). Šioje svetainėje taip pat galite gauti daugiau informacijos apie atitikties sritis ir privatumą.

Toliau pateikiamoje lentelėje rodomas dabartinis slapukų nuorodų sąrašas, kuriuos patalpino „Dynamics 365 Commerce” svetainės.

| Slapuko pavadinimas                               | Naudojimas                                                        | Gyvavimo laikotarpis |
| ------------------------------------------- | ------------------------------------------------------------ |  ------- |
| .AspNet.Slapukai                             | Parduotuvės „Microsoft Azure Active Directory” („Azure AD”) autentifikavimo slapukai vienkartiniam prisijungimui (SSO). Parduotuvės užšifravo vartotojo pagrindinę informaciją (vardą, pavardę, el. paštą). | Seansas |
| „\_msdyn365___cart_”                           | Parduotuvės krepšelio ID naudojamas produktų, pridėtų į krepšelio egzempliorių, sąrašui gauti. | Seansas |
| „\_msdyn365___checkout_cart_”                           | Parduotuvės pirkimo užbaigimo krepšelio ID naudojamas produktų, pridėtų į pirkimo užbaigimo krepšelio egzempliorių, sąrašui gauti. | Seansas |
| „\_msdyn365___ucc_”                            | Slapuko atitikties sutikimo sekimas.                          | 1 metai |
| ai_seansas                                  | Aptinka, keliuose vartotojo veiklos seansuose buvo tam tikrų programėlės puslapių ir funkcijų. | 30 min. |
| ai_vartotojas                                     | Aptinka, kaip daug žmonių naudojo programėlę ir jos funkcijas. Vartotojai skaičiuojami naudojant anoniminius ID. | 1 metai |
| b2cru                                       | Saugomas dinamiškai peradresavimo URL.                              | Seansas |
| JSESSIONID                                  | Mokėjimo jungtis naudoja „Adyen”, kad išsaugotų vartotojo seansą.       | Seansas |
| AtvertiIdPrijungti.nonce.&#42;                       | Autentifikavimas                                               | 11 minučių |
| x-ms-cpim-cache:.&#42;                          | Naudojama užklausos būsenai tvarkyti.                      | Seansas |
| x-ms-cpim-csrf                              | Kelių svetainių užklausų klastočių (CRSF) atpažinimo ženklas, naudojamas apsaugoti nuo CRSF.     | Seansas |
| x-ms-cpim-dc                                | Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių. | Seansas |
| x-ms-cpim-rc.&#42;                              | Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių. | Seansas |
| x-ms-cpim-slice                             | Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių. | Seansas |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | Naudojama SSO seansui tvarkyti.                        | Seansas |
| x-ms-cpim-trans                             | Naudojama operacijoms stebėti (atidarytų skirtukų skaičius, kuriais autentifikuojama lyginant su įmonė–vartotojui (B2C) svetaine), įskaitant dabartinę operaciją. | Seansas |
| „\_msdyn365___muid_”                            | Naudojama, jei aplinkai yra suaktyvintas eksperimentavimas; kuris naudojamas kaip vartotojo ID eksperimentavimo tikslais. | 1 metai |
| „\_msdyn365___exp_”                             | Naudojama, jei aplinkai yra suaktyvintas eksperimentavimas; naudojamas matuoti efektyvumo įkelties balansavimui.         | 1 valanda |
| „d365mkt”                                       | Naudojama, jei aptikimas pagal vietą, skirtas vartotojo IP adresui sekti dėl parduotuvių vietų pasiūlymų, yra įjungtas „Commerce” svetainių daryklėje: **Svetainės parametrai \> Bendra \> Įgalinti vieta pagrįstą parduotuvės aptikimą**.      | 1 valanda |
| \_msdyn365___tuid_                           | Naudojamas tik tada, jei suaktyvintas aplinkos suaktyvinimas; sugeneruoja GUID, kad jis būtų naudojamas kaip vartotojo identifikatorius. Reikšmė bus rodoma, jei pasikeičia vartotojo prisijungimo būsena.      | 1 metai |
| \_msdyn365___aud_0                          | Saugoma segmentų vertė, naudojama pagal taikymą ir naudojama tik tada, jei tikslinis taikymas konfigūruojamas puslapyje ar fragmentas, reikalaujamas svetainės vartotojo. Sausainis pateikiamas tik tada, kai segmento vertės atiteks trečiosios šalies segmentavimo tiekėjui.      | 7 dienos |
| \_msdyn365___aud_1                           | Saugoma segmentų vertė, naudojama pagal taikymą ir naudojama tik tada, jei tikslinis taikymas konfigūruojamas puslapyje ar fragmentas, reikalaujamas svetainės vartotojo. Sausainis pateikiamas tik tada, kai segmento vertės atiteks trečiosios šalies segmentavimo tiekėjui.      | 7 dienos |
| \_msdyn365___aud_2                           | Saugoma segmentų vertė, naudojama pagal taikymą ir naudojama tik tada, jei tikslinis taikymas konfigūruojamas puslapyje ar fragmentas, reikalaujamas svetainės vartotojo. Sausainis pateikiamas tik tada, kai segmento vertės atiteks trečiosios šalies segmentavimo tiekėjui.      | 7 dienos |
| "d365gi"                                       | Šiame slapukais saugomi geografinės vietos duomenys, kai naudojama trečiosios šalies geografinio paskirstymo tarnyba.      | 1 diena |

Jeigu svetainės vartotojas pasirenka bet kuriuos socialinės medijos saitus svetainėje, šioje lentelėje pateikti slapukai taip pat bus sekami jų naršyklėje.


| Domenas                      | Slapukas               | Aprašas                                                  | Šaltinis                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| „.linkedin.com”                | Vartotojo atitikties istorija         | „LinkedIn” skelbimų ID sinchronizavimas                                      | „LinkedIn” Sklaidos kanalas ir Įžvalgų žymė                                |
| „.linkedin.com”               | „li_sugr”                  | Naršyklės identifikatorius                                           | LinkedIn Insight žymė, jei IP adresas nėra paskirtoje šalyje |
| „.linkedin.com”               | Bizografikos atsisakymas       | Nustato atsisakymo būseną trečiosios šalies sekimui.              | „LinkedIn” svečių valdikliai ir industrijos atsisakymo puslapiai           |
| „.linkedin.com”               | „\_guid”                    | Naršyklės identifikatorius, skirtas „Google Ads”.                            | „LinkedIn” Sklaidos kanalas                                                |
| „.linkedin.com”               | „li_oatml”                 | Nario netiesioginis identifikatorius, skirtas konvertavimo sekimui, tiksliniam nukreipimui ir analizei. | „LinkedIn” Skelbimų ir Įžvalgų žymės                                |
| Įvairūs pirmosios šalies domenai | „li_fat_id”                | Nario netiesioginis identifikatorius, skirtas konvertavimo sekimui, tiksliniam nukreipimui ir analizei. | „LinkedIn” Skelbimų ir Įžvalgų žymės                                |
| „.adsymptotic.com”            | U                        | Naršyklės identifikatorius                                           | LinkedIn Insight žymė, jei IP adresas nėra paskirtoje šalyje |
| „.linkedin.com”                | „bcookie”                  | Naršyklės ID slapukas                                            | Užklausos į „LinkedIn”                                         |
| „.linkedin.com”                | „bscookie”                 | Saugios naršyklės slapukas                                        | Užklausos į „LinkedIn”                                         |
| „.linkedin.com”               | „lang”                     | Nustato numatytąją lokalę ir kalbą.                                 | Užklausos į „LinkedIn”                                         |
| „.linkedin.com”                | „lidc”                     | Naudojama nukreipimui.                                             | Užklausos į „LinkedIn”                                         |
| „.linkedin.com”               | „aam_uuid”                 | Adobe auditorijos vadybininko slapukai                                                     | ID sinchronizavimo nustatymas                                              |
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
| „.pinterest.com”              | Tarnybos darbuotojai          |                                                              |  Palūkanos                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>Svetainės vartotojo vartotojo sutikimas dėl el. komercijos svetainės 

Jei el. komercijos svetainės funkcija ar modulis naudoja neesminį slaptažodį, prieš sekant svetainėje reikia gauti svetainės vartotojo sutikimą. Kad svetainės vartotojai galėtų suteikti sutikimo sutikimą el. komercijos svetainėje, svetainės autorius turi puslapio antraštės modulyje pridėti ir konfigūruoti sutikimo internetu modulį, kad užtikrinti, kad sutikimas būtų raginamas ir gaunamas. Svetainės vartotojo sutikimas turi būti suteiktas prieš funkcijos arba modulio, naudojančio nepagrindinius slapukus, atvaizdavimą svetainės puslapyje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pritaikymo neįgaliesiems funkcijos ir galimybės](accessibility.md)

[Atitikties peržiūra](compliance-overview.md)

[Privatumo strategijos puslapio įtraukimas](add-privacy-page.md)

[Su sekamais turinio pakeitimais susietų vartotojo ID keitimas](replace-IDs-tracked-changes.md)

[Sutikimo dėl slapukų modulis](cookie-consent-module.md) 
 
[Antraštės modulis](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
