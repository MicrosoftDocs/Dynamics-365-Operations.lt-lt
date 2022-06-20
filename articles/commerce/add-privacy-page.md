---
title: Privatumo strategijos puslapio įtraukimas
description: Šiame straipsnyje aprašoma, kaip į savo svetainę įtraukti privatumo strategijos puslapį Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
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
ms.openlocfilehash: f220ee5502f269299d2af253d7790e503668c0ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871707"
---
# <a name="add-a-privacy-policy-page"></a>Privatumo strategijos puslapio įtraukimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip į savo svetainę įtraukti privatumo strategijos puslapį Microsoft Dynamics 365 Commerce.

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

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte puslapio šabloną.
1. Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Reklaminės juostos šablonas** ir pasirinkite **Gerai**.
1. Šablone į reikiamas puslapio dalis įtraukite reikiamus modulius. Norėdami gauti nurodymų, užveskite pelės žymiklį virš raudonų šauktukų. (Pavyzdžiui, dalyje **HTML antraštė** gali reikėti modulio **Numatytasis išorinis scenarijus**.)
1. Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis puslapis**.
1. Modulio **Numatytasis puslapis** dalyje **Pagrindinis** įtraukite modulį **Raiškiojo turinio blokas**.
1. Modulyje **Raiškiojo turinio blokas** įtraukite modulį **Raiškiojo turinio bloko elementas**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

### <a name="build-a-privacy-policy-page"></a>Privatumo strategijos puslapio kūrimas

Norėdami sukurti privatumo strategijos puslapį, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite privatumo strategijos puslapio šabloną.
1. Įveskite puslapio pavadinimą ir URL, tada pasirinkite **Gerai**. 
1. Puslapio vietoje **Pagrindinis** įtraukite modulį **Raiškiojo turinio blokas**.
1. Modulyje **Raiškiojo turinio blokas** įtraukite modulį **Raiškiojo turinio bloko elementas**.
1. Modulio **Raiškiojo turinio blokas** ypatybių srityje pasirinkite **Įtraukti duomenų šaltinį**, tada – **Raiškiojo teksto turinys**.
1. Raiškiojo teksto rengyklėje įveskite privatumo strategijos puslapio turinį. Jei reikia, raiškiojo teksto rengyklę išplėskite į viso ekrano režimą.
1. Baigę įvesti turinį, pasirinkite **Peržiūra**, kad puslapį galėtumėte peržiūrėti žiniatinklio naršyklėje.
1. Įtraukite likusius puslapio elementus ir modulių ypatybes.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Norėdami publikuoti privatumo strategijos puslapio URL, atlikite tolesnius veiksmus.

1. Nueikite į **URL adresai** ir pasirinkite privatumo strategijos puslapio URL.
1. Pasirinkite **Publikuoti**, kad publikuotumėte pasirinktą URL.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Saito su privatumo strategijos puslapiu sukūrimas poraštėje

Saitą su privatumo strategijos puslapiu galite įtraukti į fragmentą. Tokiu būdu saitą galite bendrinti ir atnaujinti keliuose svetainės puslapiuose, nurodydami fragmentą. Šiame pavyzdyje parodoma, kaip saitą su privatumo strategijos puslapiu įtraukti į poraštės fragmentą.

Norėdami į poraštės fragmentą įtraukti saitą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte puslapio fragmentą.
1. Dialogo lange **Naujas fragmentas** pasirinkite **Poraštės** modulį.
1. Dalyje **Fragmento pavadinimas** įveskite fragmento pavadinimą ir tuomet pasirinkite **Gerai**.
1. Dalyje **Poraštės kategorija** įtraukite modulį **Poraštės elementas**.
1. Dešinėje esančioje ypatybių srityje pasirinkite **Saito tekstas**.
1. Dialogo lange **Saito tekstas** įveskite privatumo strategijos puslapio saito tekstą ir paskirtį, tada spustelėkite **Gerai**.
1. Norėdami gauti privatumo strategijos puslapio URL, nueikite į **Puslapiai**, tada – į privatumo strategijos puslapį ir nukopijuokite URL iš ypatybių srities.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Peržiūrėkite fragmentą ir išbandykite saitą su privatumo strategijos puslapiu.

Dabar fragmentą galima nurodyti šablone kitiems svetainės puslapiams. Kai šis fragmentas nurodomas šablono modulyje **Poraštė**, saito nuoroda bus rodoma visuose puslapiuose, kurie yra sukurti naudojant tą šabloną.

## <a name="additional-resources"></a>Papildomi ištekliai

[Atitikties apžvalga](compliance-overview.md)

[Pritaikymo neįgaliesiems funkcijos ir galimybės](accessibility.md)

[Slapukų atitiktis](cookie-compliance.md)

[Su sekamais turinio pakeitimais susietų vartotojo ID keitimas](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
