---
title: Ilgalaikio turto skaidymas
description: Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai.
author: moaamer
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1073f262d29e19fbbdc2257f5cdc18c4fa629196
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725855"
---
# <a name="split-a-fixed-asset"></a>Ilgalaikio turto skaidymas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai. 

## <a name="create-a-new-fixed-asset"></a>Kurti naują ilgalaikį turtą

1. Naršymo srityje eikite į **Moduliai \> Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.
2. Pasirinkite **Naujas**.
3. Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę. Pasižymėkite ilgalaikio turto numerį, kuris bus vėliau naudojamas skaidymo procese.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Uždarykite formą.

## <a name="split-a-fixed-asset"></a>Ilgalaikio turto skaidymas

Prieš suskaidant visiškai nusidėvusį turtą, turto knygos būseną reikia rankiniu būdu pakeisti iš **Uždaryta** į **Atidaryta**. Šis veiksmas būtinas, nes knygos būsena turi būti **Atidaryta**, jei turite užregistruoti turto operacijas (pvz., likvidavimo pardavimo). Taip pat turite įjungti parametrą **Leisti kelias operacijas viename kvite**, kuris yra puslapio **DK parametrai** skirtuke **Bendra**. Kai pasikeičia turto knygos būsena ir viename kvite leidžiamos kelios operacijos, atlikite šiuos veiksmus, kad padalytumėte turtą.

1. Sąraše raskite ir pasirinkite ilgalaikio turto, kurį norite skaidyti, nuorodą.
2. Pasirinkite **Knygos**. Pasirinkite, kurią knygą padalinti naujajam turtui.
3. Pasirinkite **Funkcijos**.
4. Pasirinkite **Skaidyti ilgalaikį turtą**.
5. Lauke **Į ilgalaikį turtą** įveskite arba pasirinkite reikšmę.
6. Lauke **Į knygą** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Lauke **Operacijos data** įveskite datą.
8. Lauke **Procentas** įveskite skaičių.
9. Lauke **Žurnalo pavadinimas** įveskite arba pasirinkite reikšmę.
10. Pasirinkite **Gerai**.

## <a name="post-the-journal-transaction"></a>Registruoti žurnalo operaciją

1. Naršymo srityje eikite į **Moduliai \> Ilgalaikis turtas \> Žurnalo įrašai \> Ilgalaikio turto žurnalas**.
2. Sąraše pasirinkite žurnalą, sukurtą skaidymo procesu.
3. Pasirinkite **Eilutės**.

    - Patikrinkite sukurtas žurnalo eilutes.
    - Sukuriama pradinio turto įsigijimo koregavimo operacija, kad būtų galima sumažinti reikšmę procentine dalimi, nurodyta skaidymo proceso metu.
    - Sukuriama tos pačios sumos naujojo turto įsigijimo operacija.

4. Pasirinkite **Registruoti**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
