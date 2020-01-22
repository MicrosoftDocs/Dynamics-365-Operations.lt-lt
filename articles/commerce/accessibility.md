---
title: Pritaikymo neįgaliesiems funkcijos ir galimybės
description: Šioje temoje pateikiama informacijos apie „Microsoft Dynamics 365 Commerce“ pritaikymo neįgaliesiems funkcijas ir galimybes.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
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
ms.openlocfilehash: 3e667f89ffbc5496cc93f83fd3e7b29ba6ffa979
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946053"
---
# <a name="accessibility-features-and-capabilities"></a>Pritaikymo neįgaliesiems funkcijos ir galimybės

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje pateikiama informacijos apie „Microsoft Dynamics 365 Commerce“ pritaikymo neįgaliesiems funkcijas ir galimybes.

## <a name="overview"></a>Peržiūrėti

Pritaikymo neįgaliesiems funkcijos ir galimybės – tai funkcinės priemonės visiems vartotojams, kad jie galėtų pasiekti ir atlikti veiksmus bei įgyvendinti tikslus. Šiam plačiam vartotojų ratui gali reikėti pagalbinių klausos, regos, mobilumo ir neurologinės įvairovės įrankių.

Naudojant įvairias „Dynamics 365 Commerce“ funkcijas, galima sukurti svetainę su pagalbinėmis funkcijomis. Projektuojant svetainę reikėtų apsvarstyti pritaikymo neįgaliesiems funkcijų sritis, minimas [„Microsoft“ pritaikymo neįgaliesiems centre](https://www.microsoft.com/accessibility). 

Šioje temoje aprašomos kelios papildomos pritaikymo neįgaliesiems funkcijų sritys, kurias turėtumėte apsvarstyti naudodami „Dynamics 365 Commerce“.

## <a name="image-alt-text"></a>Alternatyvusis vaizdo tekstas

Sprendime „Dynamics 365 Commerce“ integruota skaitmeninių išteklių valdymo sistema, skirta jūsų svetainėje naudojamiems vaizdų ir vaizdo įrašų ištekliams stebėti. Renkantis ar nusiunčiant vaizdą, jo ypatybių srityje galima įtraukti vaizdo antraštę, aprašą ir alternatyvųjį tekstą.

## <a name="video-accessibility"></a>Vaizdo įrašų pritaikymas neįgaliesiems

„Dynamics 365 Commerce“ skaitmeninių išteklių valdymo sistema palaiko kelias vaizdo įrašų turinio pritaikymo neįgaliesiems funkcijas. Tolesnėje lentelėje pateikiama keletas pavyzdžių.

| Vaizdo įrašų funkcija               | Aprašymas |
|-----------------------------|-------------|
| Paslėptieji titrai      | Gali būti rodomas vaizdo įrašo garso ir garsinių apibūdinamųjų elementų tekstas, kuris gali padėti vartotojams, turintiems klausos negalią. |
| Subtitrai                   | Titrų failai, kuriuos naudojant rodomas kontekstinių priemonių ar ekrane vykstančio dialogo tekstas |
| Garso nuorašai           | Tekstinis ištartų žodžių nuorašas, generuojamas iš vaizdo ištekliaus garso |
| Apibūdinamasis garsas           | Nepagrindinis garso kanalas, apibūdinantis ekrane vykstantį turinį ar kontekstą |
| Amžiaus patikros sistema            | Atributas, kuriame gali būti saugomas minimalus amžius, kurio turi būti sulaukęs žiūrovas, kad galėtų žiūrėti vaizdo įrašą (tik metaduomenys) |

### <a name="configure-video-accessibility-elements"></a>Vaizdo įrašų pritaikymo neįgaliesiems elementų konfigūravimas

Naudodami „Dynamics 365 Commerce“, savo svetainės dalyje **Ištekliai** galite nusiųsti vaizdo įrašų išteklius, kuriuose yra atskiri paslėptųjų titrų, įprasto garso ir apibūdinamojo garso failai. Paslėptieji titrai taip pat gali būti generuojami automatiškai, kai vaizdo įrašo išteklius yra nusiunčiamas.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Paslėptųjų titrų generavimas ar nusiuntimas nusiunčiant vaizdo įrašo išteklių

Norėdami paslėptųjų titrų failą generuoti automatiškai, kai nusiunčiate vaizdo įrašą, atlikite tolesnį veiksmą.

- Dialogo lange **Išteklių nusiuntimas** pasirinkite **Automatiškai generuoti paslėptuosius titrus**. Jei generuojate paslėptųjų titrų failą, dialogo lange paslėptųjų failų išrinkiklis nebus pasiekiamas.

Jei, nusiųsdami vaizdo įrašą, paslėptųjų titrų failą norite generuoti patys, atlikite tolesnį veiksmą.

- Dialogo lange **Išteklių nusiuntimas** išvalykite elementą **Automatiškai generuoti paslėptuosius titrus**.

Norėdami nusiųsti vaizdo įrašo įprasto garso arba apibūdinamojo garso failus, naudokite dialogo lango **Išteklių nusiuntimas** failų išrinkiklį.

> [!NOTE]
> Paslėptųjų titrų, įprasto garso ir apibūdinamojo garso išteklius taip pat galima įtraukti vaizdo įrašo išteklių nusiuntus. Nueikite į **Ištekliai**, pasirinkite vaizdo įrašo išteklių ir jį paimkite bei užrakinkite. Tada jo ypatybių srityje nusiųskite papildomus išteklius.

#### <a name="edit-cc-and-audio-transcript-files"></a>Paslėpųjų titrų ir garso nuorašų failų redagavimas

Paslėptųjų titrų ir garso nuorašų failus galima redaguoti tiesiogiai kūrimo įrankyje. Redaguojant galima vaizdo įrašo atkūrimo funkcija.

Norėdami redaguoti paslėptųjų titrų ir nuorašų failus, atlikite tolesnius veiksmus.

1. Nueikite į **Ištekliai**, pasirinkite vaizdo įrašo išteklių, tada – **Redaguoti paslėptuosius titrus / nuorašą**. Rodoma paslėptųjų titrų ir nuorašų turinio rengyklė.
1. Pasirinkite **Paimti**.
1. Redaguokite paslėptųjų titrų ar nuorašo tekstą.
1. Baigę pasirinkite **Įrašyti**, tada – **Įrašyti ir atrakinti**.
1. Kai būsite pasirengę publikuoti, pasirinkite **Publikuoti**.

#### <a name="set-the-minimum-age-attribute"></a>Atributo Minimalus amžius nustatymas

Su vaizdo įrašų ištekliais galima susieti metaduomenų atributą **Minimalus amžius**.

Norėdami nustatyti vaizdo įrašo ištekliaus atributą **Minimalus amžius**, atlikite tolesnius veiksmus.

1. Nueikite į **Ištekliai** ir pasirinkite vaizdo įrašo išteklių.
1. Pasirinkite **Paimti**.
1. Vaizdo įrašo ištekliaus ypatybių srityje nustatykite atributą **Minimalus amžius**.

> [!NOTE]
> Ypatybių sritis naudojama tik metaduomenų atributo reikšmei nustatyti ir saugoti. Norint šį atributą naudoti kaip amžiaus patikros sistemą atkuriant turinį, turi būti sukurti tinkinti moduliai.

## <a name="additional-resources"></a>Papildomi ištekliai

[Formų, produktų ir valdiklių pritaikymas neįgaliesiems](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[„Microsoft“ pritaikymo neįgaliesiems centras](https://www.microsoft.com/accessibility)

[„Dynamics 365“ pritaikymo neįgaliesiems centras](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Atitikties apžvalga](compliance-overview.md)

[Slapukų atitiktis](cookie-compliance.md)

[Privatumo strategijos puslapio įtraukimas](add-privacy-page.md)
