---
title: Slapukų atitiktis
description: Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446918"
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

## <a name="additional-resources"></a>Papildomi ištekliai

[Pritaikymo neįgaliesiems funkcijos ir galimybės](accessibility.md)

[Atitikties peržiūra](compliance-overview.md)

[Įtraukti privatumo strategijos puslapį](add-privacy-page.md)

[Su sekamais turinio pakeitimais susietų vartotojo ID keitimas](replace-IDs-tracked-changes.md)
