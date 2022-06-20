---
title: Nuomos įtraukimas arba kopijavimas (peržiūros versija)
description: Šiame straipsnyje aprašoma, kaip sukurti naują nuomą įvedant informaciją apie ją turto operacijai arba kopijuojant informaciją iš esamos nuomos.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 798ab3ece45ee6f21694a364cfb7a4ff14a9c8aa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880938"
---
# <a name="add-or-copy-leases-preview"></a>Nuomos įtraukimas arba kopijavimas (peržiūros versija)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip kurti nuomą nuo pradžių turto perskyroje, ir kaip kurti nuomą kopijuojant esamą nuomą. Nuomos kūrimo nuo nulio procesas apima naujos nuomos informacijos įvedimą ir nuomos grafiko sukūrimą. Nustačius bent vieną nuomą, gali būti lengviau nukopijuoti informaciją iš esamos nuomos ir pagal poreikį redaguoti šią informaciją, kad būtų sukurta nauja nuoma.

## <a name="create-a-lease"></a>Nuomos kūrimas

Atlikite tolesnius veiksmus, norėdami sukurti nuomą modulyje Turto nuoma.

1. Puslapio **Nuomos suvestinė** veiksmų srityje pasirinkite **Nauja**.
2. Įveskite nuomos informaciją. Laukų, kuriuos būtina užpildyti, kraštinės yra raudonos.

Nuomos mokėjimo pradžios data negali būti ankstesnė už nuomos pradžios datą. Jei įvesite nuomos mokėjimo pradžios datą, kuri būtų ankstesnė nei nuomos pradžios data, gausite klaidos pranešimą.

Pagal numatytuosius **nustatymus** **paskirstymo** mokėjimo sumos parinktis, esanti puslapio Nuomos informacija bendrajame **FastTab** **, yra nustatyta kaip Ne** **·** **·**, jei turto parametrų puslapyje leisti mokėjimo paskirstymą nustatyta **kaip Taip.** 

Jei paskirstymo **mokėjimo sumos parinktis** nustatyta kaip **Taip**, mokėjimo **grafiko** eilučių **"** FastTab" mokėjimo sumos laukas yra užrakintas. Jis bus nustatytas kaip bendroji mokėjimo sumų suma, kuri vėliau įvedama mokėjimo sumos **paskirstymo kataloge**.

Pasirinkite **mokėjimo sumos paskirstymą**, kad atidarytumėte puslapį, kuriame galite įtraukti elemento mokėjimo tipus. Mygtukas **Įtraukti sumas į mokėjimo sumą** perkels sumas į lauką **Mokėjimo** suma.

> [!NOTE]
> Jei pridedate prekę mokėjimo **sumą ir tada pasirenkate klavišą Esc**, **·** **įvestos sumos nebus pridėtos prie mokėjimo sumos lauko mokėjimo grafiko eilutėse** "FastTab". Todėl jie bus saugomi mokėjimo sumos **paskirstymo** dialogo lange. Jei norite, kad dialogo lange būtų rodoma bendroji suma, pasirinkite stulpelį Suma, **pasirinkite** ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku), **tada pasirinkite Šio stulpelio suma**. 

Mygtukas **Kopijuoti eilutę** kopijuos visų elementų mokėjimo paskirstymą.

## <a name="create-a-lease-schedule"></a>Nuomos grafiko kūrimas

Baigę įvesti nuomos informaciją, atlikite šiuos veiksmus, kad sukurtumėte nuomos grafiką.

> [!NOTE]
> Finansinės dimensijos gali keistis atsižvelgiant į bet kokias pasirinktines finansines dimensijas.

1. Pasirinkite **Kurti grafikus** nuomos knygoms generuoti. Nuomos knygos apima mokėjimo, amortizacijos, nusidėvėjimo ir išlaidų grafikus.
2. Norėdami pasiekti nuomos knygas ir peržiūrėti naujai sukurtus grafikus, pasirinkite skirtuką **Knygos**.

    Puslapyje **Knygų informacija** rodoma, kaip nuoma apskaitoma knygose, kurios jai priskirtos. Čia galite peržiūrėti nuomos grafikus.

    Į mokėjimo grafiką įtraukiami įvesti duomenys iš puslapio **Nuomos įtraukimas** skirtuko **Mokėjimo grafiko eilutės**. Vis tiek galite pakeisti kiekvieną mokėjimo sumą ir kintamąjį mokėjimą. Nuomos įsipareigojimas apskaičiuojamas pagal pakeistą mokėjimo grafiką.

    > [!NOTE]
    > Nuomos mokėjimo pradžios data turi būti tokia pati arba vėlesnė už nuomos pradžios datą. Jei mokėjimo pradžios data yra ankstesnė nei nuomos pradžios data, gausite klaidos pranešimą. 

4. Peržiūrėję mokėjimo grafiką, pasirinkite **Patvirtinti grafiką**. Patvirtinus grafiką, nuomos nebegalima redaguoti.

    > [!NOTE]
    > Sistema automatiškai apskaičiuoja nuomos terminą pagal mokėjimo grafiko eilutes, esančias puslapyje **Nuomos įtraukimas**.
    >
    > Kad apskaičiuotų nuomos terminą mėnesiais, sistema suranda skirtumą tarp konkrečios mokėjimo grafiko eilutės pradžios datos ir pabaigos datos. Tada ji pereina į kitą mokėjimo grafiko eilutę ir vėl suranda skirtumą. Galiausiai sistema susumuoja visas sumas, kad nustatytų nuomos terminą mėnesiais.

5. Norėdami peržiūrėti apskaičiuotas laikotarpio palūkanų sąnaudas, atidarykite puslapį **Įsipareigojimų amortizacijos grafikas**. Norėdami peržiūrėti apskaičiuotą tiesiogiai proporcingą nusidėvėjimą, atidarykite puslapį **Turto nusidėvėjimo grafikas**.
6. Baigę peržiūrėti apskaičiuotą sumą, puslapyje **Pradinis pripažinimas** galite sukurti pradinio pripažinimo žurnalo įrašą. Gausite pranešimą, kuriame bus teigiama, kad sukurtas žurnalas.

    > [!NOTE]
    > Žurnalo įrašas neregistruojamas didžiojoje knygoje tol, kol neužregistruojate įrašo neautomatiniu būdu.

7. Norėdami peržiūrėti siūlomą pradinio pripažinimo įrašą prieš jį registruodami, pasirinkite **Turto nuomos žurnalas**.

    > [!NOTE]
    > Turto nuomos žurnalo negalima sukurti neautomatiniu būdu. Jis sukuriamas automatiškai, kai kuriami nuomos grafikai.

8. Kai baigiate peržiūrėti pradinio pripažinimo žurnalo įrašą ir esate pasiruošę jį užregistruoti, pasirinkite **Registruoti**, kad būtų pripažįstamas naudojimo teise valdomas turtas ir nuomos įsipareigojimas didžiojoje knygoje.

## <a name="copy-a-lease"></a>Nuomos kopijavimas

Modulis Turto nuoma leidžia kopijuoti nuomos informaciją, kad būtų sukurta nauja nuoma su ta pačia informacija. Tada galite pakeisti nuomos laukus prieš kurdami nukopijuotos nuomos grafikus.

1. Puslapyje **Nuomos suvestinė** pasirinkite kopijuotiną nuomą, tada veiksmų srityje pasirinkite **Kopijuoti nuomą**.

    > [!NOTE]
    > Jei nuomos ID numeracijos parametras **Neautomatinis** išjungtas, kitas numeracijos skaičius automatiškai generuojamas kaip nukopijuotos nuomos ID. Jei parametras **Neautomatinis** įjungtas, gaunate pranešimą, raginantį įvesti nuomos ID prieš toliau kopijuojant nuomą.

2. Pasirinkite **Kopijuoti**. Nuomos informacija iš pasirinktos nuomos nukopijuojama į naują nuomą. Tada galite redaguoti naujos nuomos informaciją, prieš ją įrašydami ir kurdami nuomos grafikus.

## <a name="asset-leasing-journal"></a>Turto nuomos žurnalas

Visi žurnalo įrašai, sukurti modulyje Turto nuoma, pateikiami Turto nuomos žurnale. Puslapyje **Turto nuomos žurnalas** (**Turto nuoma \> Žurnalo įrašai \> Turto nuomos žurnalas**) galite filtruoti pagal registravimo būseną, peržiūrėti konkrečius žurnalo įrašus ir kvitus bei registruoti neregistruotus žurnalo įrašus.

> [!NOTE]
> Turto nuomos žurnalo negalima sukurti neautomatiniu būdu. Jis sukuriamas automatiškai, kai kuriami nuomos grafikai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
