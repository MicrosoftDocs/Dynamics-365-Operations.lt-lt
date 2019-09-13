---
title: Ilgalaikio turto skaidymas
description: Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867588"
---
# <a name="split-a-fixed-asset"></a>Ilgalaikio turto skaidymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje paaiškinta, kaip vienos turto knygos procentinę dalį padalinti naujai turto knygai. Jis naudoja vaidmenį Buhalteris ir USMF demonstracinius duomenis.


## <a name="create-a-new-fixed-asset"></a>Kurti naują ilgalaikį turtą
1. Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas**.
2. Pasirinkite **Naujas**.
3. Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę. Pasižymėkite ilgalaikio turto numerį, kuris bus vėliau naudojamas skaidymo procese.  
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Uždarykite formą.

## <a name="split-a-fixed-asset"></a>Ilgalaikio turto skaidymas
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
1. Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.
2. Sąraše pasirinkite žurnalą, sukurtą skaidymo procesu.
3. Pasirinkite **Eilutės**.

    - Patikrinkite sukurtas žurnalo eilutes.  
    - Sukuriama pradinio turto įsigijimo koregavimo operacija, kad būtų galima sumažinti reikšmę procentine dalimi, nurodyta skaidymo proceso metu.  
    - Sukuriama tos pačios sumos naujojo turto įsigijimo operacija.  

4. Pasirinkite **Registruoti**.

