---
title: Padengimo laiko riba
description: Šiame straipsnyje aprašoma, kaip nustatyti padengimo laiko ribas. Padengimo laiko riba nurodo jūsų planavimo perspektyvą ir limitą.
author: t-benebo
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 987dea4c1b693fc1bb687f97d51288d5e51e7d4c
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740119"
---
# <a name="coverage-time-fences"></a>Padengimo laiko riba

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti padengimo *laiko ribas*. „Planners“ gali apibrėžti planavimo perspektyvą (padengimo laiko ribą dienomis) ir neįtraukti tiekimo ir poreikio, nepatenkančio į tą laikotarpį. Todėl padengimo laiko ribos padeda išvengti „triukšmo”, kurį sukelia tiekimo pasiūlymai, į kuriuos jums nereikia reaguoti mėnesiais. Pavyzdžiai apima kitų metų prognozę ir klientų užsakymus, pateikiamus daug toliau nei įprastas gamybos laikas.

Padengimo laiko riba yra dienų skaičius po šiandienos datos (arba tiksliau, planavimo vykdymo datos), neįtraukiant tiekimo ir poreikio. Norėdami išvengti vėlavimo, turite užtikrinti, kad padengimo laiko riba yra ilgesnė už bendrą gamybos laiką. Numatytoji sistemos reikšmė yra 100 dienų.

Galite nurodyti padengimo laiko ribas kiekvienam iš šių lygių:

- **Padengimo grupė** – galite nustatyti numatytąją padengimo laiko ribą kiekvienai padengimo grupei.
- **Prekės padengimas** – galite keisti padengimo laiko ribą, perimtą iš prekei priskirtos padengimo grupės.
- **Bendrasis planas** – galite keisti padengimo laiko ribas, perimtas iš padengimo grupės ir prekės padengimo parametrų.

Šiuose skyriuose paaiškinama, kaip nurodyti padengimo grupę kiekvienu lygiu.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Padengimo laiko ribos nustatymas padengimo grupei

Kai nurodote padengimo laiko ribas padengimo grupei, nustatymas taikomas visoms tai grupei priklausančioms prekėms (produktams). Tačiau galite keisti konkrečių prekių ar konkrečių bendrųjų planų parametrus.

Norėdami nurodyti padengimo grupės padengimo laiko ribą, atlikite šiuos veiksmus.

1. Pasirinkite **Bendrasis planavimas \> Sąranka \> Padengimas \> Padengimo grupės**.
1. Pasirinkite esamą padengimo grupę iš sąrašo arba sukurkite naują padengimo grupę.
1. „FastTab” **Bendra** nustatykite lauką **Padengimo laiko riba (dienomis)** į tokį dienų skaičių, kurį norite naudoti kaip padengimo laiko ribą padengimo grupei.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Padengimo laiko ribos nustatymas konkrečiai prekei

Kiekviena prekė (produktas) priklauso padengimo grupei. Jeigu prekei tiesiogiai nepriskirta jokia padengimo grupė, taikoma numatytoji padengimo grupė. Kiekviena prekė perima padengimo laiko ribą iš jos padengimo grupės. Tačiau, jei norite, galite keisti šią laiko ribą konkrečioms prekėms.

Norėdami nurodyti konkrečios prekės padengimo laiko ribą, atlikite šiuos veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Pasirinkite produktą iš tinklelio.
1. Veiksmų srities skirtuko **Planas** grupėje **Padengimas** pasirinkite **Prekės padengimas**.
1. Puslapio **Prekės padengimas** skirtuke **Apžvalga** pasirinkite arba sukurkite eilutę vietai, kurioje norite nustatyti padengimo laiko ribą.
1. Pasirinkite **Bendra** skirtuką pasirinktos svetainės parametrams atidaryti.
1. Pasirinkite **Keisti padengimo grupės parametrus** žymės langelį.
1. Nustatykite lauką **Padengimo laiko riba (dienomis)** į tokį dienų skaičių, kurį norite naudoti kaip padengimo laiko ribą prekei.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Padengimo laiko ribos nustatymas bendrajam planui

Galite nurodyti padengimo laiko ribas bendrojo plano lygiu. Tokiu būdu apibrėžiate dienų skaičių, kurį apima bendrojo planavimo skaičiavimas bendrajam planui. Šis parametras pakeičia bet kuriuos padengimo laiko parametrus, kuriuos apibrėžėte kiekvienai atitinkamai prekei ir padengimo grupei.

Norėdami nurodyti konkretaus bendrojo plano padengimo laiko ribą, atlikite šiuos veiksmus.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Iš sąrašo pasirinkite esamą bendrąjį planą arba sukurkite naują bendrąjį planą.
1. „FastTab” **Laiko ribos dienomis** nustatykite **Padengimo** parinktį į *Taip*. Tada lauke, esančiame po parinktimi, įveskite tokį dienų skaičių, kurį norite naudoti kaip padengimo laiko ribą bendrajam planui.

## <a name="considerations-for-coverage-time-fences"></a>Padengimo laiko ribų svarstymai

Nustatydami padengimo laiko ribas, atsižvelkite į šiuos aspektus:

- Padengimo laiko ribos paveikia tik bendrojo planavimo įvesties duomenis. Jei atsiranda vėlavimas, gautų suplanuotų užsakymų data gali būti gaunama prie šios dienos datos pridėjus padengimo laiko ribą.
- Padengimo laiko ribos apibrėžiamos kalendorinėmis dienomis. Kalendoriai, naudojantys darbo dienas, nepaveikia laiko ribos skaičiavimo. Pavyzdžiui, savaitė visada laikoma septyniomis dienomis, net jei savaitgaliai nustatomi kaip uždarytos dienos darbo laiko kalendoriuje.
- Poreikio operacijos nebus generuojamos jokiam tiekimui ir poreikiui, kuris nepatenka į padengimo laiko ribas.
- Jei bet koks patvirtintas tiekimas ir poreikis nepatenka į padengimo laiko ribas, jis nebus įkeltas į mechanizmą. Todėl tai nesuaktyvins jokių papildymų ir vėlavimas nebus skaičiuojamas. Nepaisant to, šis tiekimas ir poreikis neturi būti pašalintas iš sistemos.
- Pakankamų atsargų kiekio (iš minimalių raktų) nuokrypių nebus paisoma, jeigu jie nėra padengimo laiko ribose.
- Vidinės įmonės poreikio bus nepaisoma, jei apskaičiuota pageidaujama siuntimo data nėra padengimo laiko ribose. Atkreipkite dėmesį, kad pasenusiam bendrojo planavimo moduliui vidinės įmonės poreikis nėra ribojamas pagal padengimo laiko ribas.
- Poreikio prognozių bus nepaisoma, jeigu biudžeto data nėra padengimo laiko ribose. Atsikreipkite dėmesį, kad pasenusiam bendrojo planavimo moduliui poreikio prognozės ribojamos pagal padengimo laiko ribas.
- Planavimo optimizavimas palaiko laiko juostas. Jis atsižvelgia į tiekimo ir poreikio tinklaviečių laiko juostas ir planavimo vykdymo laiką. Pavyzdžiui, bendrasis planavimas suaktyvinamas spalio 15 d. 11 val. iš tinklavietės Danijoje (GMT+1 laiko juosta) ir panaudojama dešimt dienų padengimo laiko riba. Šiuo atveju, tiekimas ir poreikis iš tinklavietės Sietle (GMT-8 laiko juostos) įtraukiamas iki spalio 25 d. 2 val. (= dešimt dienų po 24 valandas po bendrojo planavimo suaktyvinimo, atėmus devynių valandų laiko juostos skirtumą). Atsikreipkite dėmesį, kad pasenusiu bendrojo planavimo moduliu atsižvelgiama tik į laiko ribos datą. Todėl rezultatas gali skirtis.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]