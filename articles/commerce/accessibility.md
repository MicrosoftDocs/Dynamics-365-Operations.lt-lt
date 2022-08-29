---
title: Pritaikymo neįgaliesiems funkcijos ir galimybės
description: Šiame straipsnyje pateikiama informacija apie pasiekiamumo priemones ir galimybes Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a797b94d8101100574169cdcecfe8df2b5954c15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278157"
---
# <a name="accessibility-features-and-capabilities"></a>Pritaikymo neįgaliesiems funkcijos ir galimybės

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie pasiekiamumo priemones ir galimybes Microsoft Dynamics 365 Commerce.

Pritaikymo neįgaliesiems funkcijos ir galimybės – tai funkcinės priemonės visiems vartotojams, kad jie galėtų pasiekti ir atlikti veiksmus bei įgyvendinti tikslus. Šiam plačiam vartotojų ratui gali reikėti pagalbinių klausos, regos, mobilumo ir neurologinės įvairovės įrankių.

Naudojant įvairias „Dynamics 365 Commerce“ funkcijas, galima sukurti svetainę su pagalbinėmis funkcijomis. Projektuojant svetainę reikėtų apsvarstyti pritaikymo neįgaliesiems funkcijų sritis, minimas [„Microsoft“ pritaikymo neįgaliesiems centre](https://www.microsoft.com/accessibility). 

Šiame straipsnyje aprašomos kai kurios papildomos pasiekiamumo funkcijos, į kurias turėtumėte atsižvelgti naudodami Dynamics 365 Commerce.

## <a name="image-alt-text"></a>Alternatyvusis vaizdo tekstas

Sprendime „Dynamics 365 Commerce“ integruota skaitmeninių išteklių valdymo sistema, skirta jūsų svetainėje naudojamiems vaizdų ir vaizdo įrašų ištekliams stebėti. Renkantis ar nusiunčiant vaizdą, jo ypatybių srityje galima įtraukti vaizdo antraštę, aprašą ir alternatyvųjį tekstą.

## <a name="video-accessibility"></a>Vaizdo įrašų pritaikymas neįgaliesiems

„Dynamics 365 Commerce“ skaitmeninių išteklių valdymo sistema palaiko kelias vaizdo įrašų turinio pritaikymo neįgaliesiems funkcijas. Tolesnėje lentelėje pateikiama keletas pavyzdžių.

| Vaizdo įrašų funkcija               | Aprašymas |
|-----------------------------|-------------|
| Paslėptieji titrai      | Gali būti rodomas vaizdo įrašo garso ir garsinių apibūdinamųjų elementų tekstas, kuris gali padėti kurtiesiems ar neprigirdintiesiems vartotojams |
| Subtitrai                   | Titrų failai, kuriuos naudojant rodomas kontekstinių priemonių ar ekrane vykstančio dialogo tekstas |
| Garso nuorašai           | Tekstinis ištartų žodžių nuorašas, generuojamas iš vaizdo ištekliaus garso |
| Apibūdinamasis garsas           | Nepagrindinis garso kanalas, apibūdinantis ekrane vykstantį turinį ar kontekstą |
| Amžiaus patikros sistema            | Atributas, kuriame gali būti saugomas minimalus amžius, kurio turi būti sulaukęs žiūrovas, kad galėtų žiūrėti vaizdo įrašą (tik metaduomenys) |

### <a name="configure-video-accessibility-elements"></a>Vaizdo įrašų pritaikymo neįgaliesiems elementų konfigūravimas

„Commerce“ dalyje **Medijos biblioteka** galite nusiųsti vaizdo įrašų išteklius, kuriuose yra atskiri paslėptųjų titrų, įprasto garso ir apibūdinamojo garso failai. Paslėptieji titrai taip pat gali būti generuojami automatiškai, kai vaizdo įrašo išteklius yra nusiunčiamas.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Paslėptųjų titrų generavimas ar nusiuntimas nusiunčiant vaizdo įrašo išteklių

Norėdami paslėptųjų titrų failą generuoti automatiškai, kai nusiunčiate vaizdo įrašą, atlikite tolesnį veiksmą.

- Dialogo lange **Išteklių nusiuntimas** pasirinkite **Automatiškai generuoti paslėptuosius titrus**. Jei generuojate paslėptųjų titrų failą, dialogo lange paslėptųjų failų išrinkiklis nebus pasiekiamas.

Jei, nusiųsdami vaizdo įrašą, paslėptųjų titrų failą norite generuoti patys, atlikite tolesnį veiksmą.

- Dialogo lange **Išteklių nusiuntimas** išvalykite elementą **Automatiškai generuoti paslėptuosius titrus**.

Norėdami nusiųsti vaizdo įrašo įprasto garso arba apibūdinamojo garso failus, naudokite dialogo lango **Išteklių nusiuntimas** failų išrinkiklį.

> [!NOTE]
> Paslėptųjų titrų, įprasto garso ir apibūdinamojo garso išteklius taip pat galima įtraukti vaizdo įrašo išteklių nusiuntus. Eikite į **Medijos biblioteka**, pasirinkite vaizdo įrašo išteklių, tada – **Redaguoti**, kad paimtumėte bei užrakintumėte jį. Tada jo ypatybių srityje nusiųskite papildomus išteklius.

#### <a name="edit-cc-and-audio-transcript-files"></a>Titrų ir garso nuorašų failų redagavimas

Paslėptųjų titrų ir garso nuorašų failus galima redaguoti tiesiogiai kūrimo įrankyje. Redaguojant galima vaizdo įrašo atkūrimo funkcija.

Norėdami redaguoti paslėptųjų titrų ir nuorašų failus, atlikite tolesnius veiksmus.

1. Eikite į **Medijos biblioteka** ir pasirinkite vaizdo įrašo ištekliaus failo pavadinimą. Rodoma paslėptųjų titrų ir nuorašų turinio rengyklė.
1. Pasirinkite **Redaguoti**.
1. Redaguokite paslėptųjų titrų ar nuorašo tekstą.
1. Baigę pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Kai būsite pasirengę publikuoti, pasirinkite **Publikuoti**.

#### <a name="set-the-minimum-age-attribute"></a>Atributo Minimalus amžius nustatymas

Su vaizdo įrašų ištekliais galima susieti metaduomenų atributą **Minimalus amžius**.

Norėdami nustatyti vaizdo įrašo ištekliaus atributą **Minimalus amžius**, atlikite tolesnius veiksmus.

1. Nueikite į **Medijos biblioteka** ir pasirinkite vaizdo įrašo išteklių.
1. Pasirinkite **Redaguoti**.
1. Vaizdo įrašo ištekliaus ypatybių srityje nustatykite atributą **Minimalus amžius**.

> [!NOTE]
> Ypatybių sritis naudojama tik metaduomenų atributo reikšmei nustatyti ir saugoti. Norint šį atributą naudoti kaip amžiaus patikros sistemą atkuriant turinį, turi būti sukurti tinkinti moduliai.

## <a name="additional-resources"></a>Papildomi ištekliai

[Formų, produktų ir valdiklių pritaikymas neįgaliesiems](/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[„Microsoft“ pritaikymo neįgaliesiems centras](https://www.microsoft.com/accessibility)

[„Dynamics 365“ pritaikymo neįgaliesiems centras](/dynamics365/get-started/accessibility/index)

[Atitikties peržiūra](compliance-overview.md)

[Slapukų atitiktis](cookie-compliance.md)

[Įtraukti privatumo strategijos puslapį](add-privacy-page.md)

[Su sekamais turinio pakeitimais susietų vartotojo ID keitimas](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
