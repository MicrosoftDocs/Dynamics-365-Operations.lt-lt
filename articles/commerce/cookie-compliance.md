---
title: Slapukų atitiktis
description: Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 95c5801e69396b21a36c4ae12ce17801e6f7fd88
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993505"
---
# <a name="cookie-compliance"></a>Slapukų atitiktis

[!include [banner](includes/banner.md)]

Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

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