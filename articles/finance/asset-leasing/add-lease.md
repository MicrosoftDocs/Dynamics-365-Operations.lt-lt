---
title: Nuomos įtraukimas arba kopijavimas (peržiūros versija)
description: Šioje temoje aprašoma, kaip sukurti naują nuomą, įvedant jos informaciją modulyje Turto nuoma arba kopijuojant informaciją iš esamos nuomos.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: abbf04d009a4b347792cd8b317e334da2a4cbbee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969608"
---
# <a name="add-or-copy-leases-preview"></a>Nuomos įtraukimas arba kopijavimas (peržiūros versija)

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nuo nulio sukurti nuomą modulyje Turto nuoma ir kaip sukurti nuomą nukopijuojant esamą nuomą. Nuomos kūrimo nuo nulio procesas apima naujos nuomos informacijos įvedimą ir nuomos grafiko sukūrimą. Nustačius bent vieną nuomą, gali būti lengviau nukopijuoti informaciją iš esamos nuomos ir pagal poreikį redaguoti šią informaciją, kad būtų sukurta nauja nuoma.

## <a name="create-a-lease"></a>Nuomos kūrimas

Atlikite tolesnius veiksmus, norėdami sukurti nuomą modulyje Turto nuoma.

1. Puslapio **Nuomos suvestinė** veiksmų srityje pasirinkite **Nauja**.
2. Įveskite nuomos informaciją. Laukų, kuriuos būtina užpildyti, kraštinės yra raudonos.

## <a name="create-a-lease-schedule"></a>Nuomos grafiko kūrimas

Baigę įvesti nuomos informaciją, atlikite šiuos veiksmus, kad sukurtumėte nuomos grafiką.

> [!NOTE]
> Finansinės dimensijos gali keistis atsižvelgiant į bet kokias pasirinktines finansines dimensijas.

1. Pasirinkite **Kurti grafikus** nuomos knygoms generuoti. Nuomos knygos apima mokėjimo, amortizacijos, nusidėvėjimo ir išlaidų grafikus.
2. Norėdami pasiekti nuomos knygas ir peržiūrėti naujai sukurtus grafikus, pasirinkite skirtuką **Knygos**.

    Puslapyje **Knygų informacija** rodoma, kaip nuoma apskaitoma knygose, kurios jai priskirtos. Čia galite peržiūrėti nuomos grafikus.

    Į mokėjimo grafiką įtraukiami įvesti duomenys iš puslapio **Nuomos įtraukimas** skirtuko **Mokėjimo grafiko eilutės**. Vis tiek galite pakeisti kiekvieną mokėjimo sumą ir kintamąjį mokėjimą. Nuomos įsipareigojimas apskaičiuojamas pagal pakeistą mokėjimo grafiką.

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
