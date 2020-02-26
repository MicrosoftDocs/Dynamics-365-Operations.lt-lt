---
title: Privatumo strategijos puslapio įtraukimas
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti privatumo strategijos puslapį.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001328"
---
# <a name="add-a-privacy-policy-page"></a>Privatumo strategijos puslapio įtraukimas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti privatumo strategijos puslapį.

## <a name="overview"></a>Peržiūrėti

Laikantis privatumo apsaugos taisyklių, taikomos organizacinės priemonės, kuriomis svetainių vartotojai informuojami apie tai, kaip renkami ir tvarkomi jų duomenys. Tada vartotojai gali nuspręsti, kaip jų asmens duomenys turi būti tvarkomi, ir imtis atitinkamų veiksmų.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>„Microsoft“ privatumo nuostatų peržiūra programoje „Dynamics 365 Commerce“

Norėdami peržiūrėti „Microsoft“ privatumo nuostatas, kai esate prisijungę prie „Dynamics 365 Commerce“ kūrimo įrankių, pasirinkite viršutiniame dešiniajame kampe esantį mygtuką **Žinynas** (**?**), tada – **Privatumas ir slapukai**. Atidaromas naujas skirtukas, kuriame yra saitas su [„Microsoft“ privatumo nuostatomis](https://privacy.microsoft.com/privacystatement).

## <a name="build-a-privacy-policy-page-for-your-site"></a>Svetainės privatumo strategijos puslapio sukūrimas

Programoje „Dynamics 365 Commerce“ savo svetainės vartotojams prieigą prie privatumo strategijos galima suteikti keliais būdais. Šiame skyriuje parodoma, kaip sukurti privatumo strategijos puslapį, o tada į jį nurodyti naudojant poraštės fragmentą.

Toliau pateikiamos gairės yra pavyzdys, kuriuo parodoma, kaip sukurti bendrinį „Commerce“ svetainės privatumo strategijos puslapį. Jūsų pareiga yra sukurti ir įdiegti privatumo strategijos puslapio sprendimą, kuris geriausiai atitinka jūsų įmonės teisinius reikalavimus.

Norėdami pradėti, kūrimo įrankiuose nueikite į svetainę, kuriai norite sukurti privatumo strategijos puslapį.

### <a name="create-a-template"></a>Kurti šabloną

> [!NOTE]
> Jei šablonas, kurį galima naudoti privatumo strategijos puslapyje, jau sukurtas, pereikite į skyrių [Privatumo strategijos puslapio kūrimas](#build-a-privacy-policy-page).

Norėdami sukurti šabloną, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Šablonai \> Naujas šablonas**.
1. Įveskite šablono pavadinimą ir pasirinkite **Gerai**.
1. Šablone į reikiamas puslapio dalis įtraukite reikiamus modulius. Norėdami gauti nurodymų, užveskite pelės žymiklį virš raudonų šauktukų.

    Pavyzdžiui, dalyje **HTML antraštė** gali reikėti modulio **Numatytasis išorinis scenarijus**.

1. Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis puslapis**.
1. Modulio **Numatytasis puslapis** dalyje **Pagrindinis** įtraukite modulį **Raiškiojo turinio blokas**.
1. Modulyje **Raiškiojo turinio blokas** įtraukite modulį **Raiškiojo turinio bloko elementas**.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.

### <a name="build-a-privacy-policy-page"></a>Privatumo strategijos puslapio kūrimas

Norėdami sukurti privatumo strategijos puslapį, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Puslapiai \> Naujas puslapis**.
1. Pasirinkite privatumo strategijos puslapio šabloną.
1. Įveskite puslapio pavadinimą ir URL, tada pasirinkite **Gerai**. 
1. Puslapio vietoje **Pagrindinis** įtraukite modulį **Raiškiojo turinio blokas**.
1. Modulyje **Raiškiojo turinio blokas** įtraukite modulį **Raiškiojo turinio bloko elementas**.
1. Modulio **Raiškiojo turinio blokas** ypatybių srityje pasirinkite **Įtraukti duomenų šaltinį**, tada – **Raiškiojo teksto turinys**.
1. Raiškiojo teksto rengyklėje įveskite privatumo strategijos puslapio turinį. Jei reikia, raiškiojo teksto rengyklę išplėskite į viso ekrano režimą.
1. Baigę įvesti turinį, pasirinkite **Peržiūra**, kad puslapį galėtumėte peržiūrėti žiniatinklio naršyklėje.
1. Įtraukite likusius puslapio elementus ir modulių ypatybes.
1. Privatumo strategijos puslapį įrašykite ir atrakinkite bei publikuokite.

Norėdami publikuoti privatumo strategijos puslapio URL, atlikite tolesnius veiksmus.

1. Nueikite į **URL adresai** ir pasirinkite privatumo strategijos puslapio URL.
1. Pasirinktą URL publikuokite.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Saito su privatumo strategijos puslapiu sukūrimas poraštėje

Saitą su privatumo strategijos puslapiu galite įtraukti į fragmentą. Tokiu būdu saitą galite bendrinti ir atnaujinti keliuose svetainės puslapiuose, nurodydami fragmentą. Šiame pavyzdyje parodoma, kaip saitą su privatumo strategijos puslapiu įtraukti į poraštės fragmentą.

Norėdami į poraštės fragmentą įtraukti saitą, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Puslapio fragmentai \> Naujas puslapio fragmentas**.
1. Pasirinkite modulį **Poraštė**, tada lauke **Puslapio fragmento pavadinimas** įveskite pavadinimą.
1. Dalyje **Poraštės kategorija** įtraukite modulį **Poraštės elementas**.
1. Dešinėje esančioje ypatybių srityje pasirinkite **Saito tekstas**.
1. Dialogo lange **Saito tekstas** įveskite privatumo strategijos puslapio saito tekstą ir paskirtį, tada spustelėkite **Gerai**.

    Norėdami gauti privatumo strategijos puslapio URL, nueikite į **Puslapiai**, tada – į privatumo strategijos puslapį ir nukopijuokite URL iš ypatybių srities.

1. Fragmentą įrašykite, atrakinkite ir publikuokite.
1. Peržiūrėkite fragmentą ir išbandykite saitą su privatumo strategijos puslapiu.

Dabar fragmentą galima nurodyti šablone kitiems svetainės puslapiams. Kai šis fragmentas nurodomas šablono modulyje **Poraštė**, saito nuoroda bus rodoma visuose puslapiuose, kurie yra sukurti naudojant tą šabloną.

## <a name="additional-resources"></a>Papildomi ištekliai

[Atitikties apžvalga](compliance-overview.md)

[Pritaikymo neįgaliesiems funkcijos ir galimybės](accessibility.md)

[Slapukų atitiktis](cookie-compliance.md)
