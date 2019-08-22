---
title: Skaidyti ilgalaikį turtą
description: Šis užduočių vadovas išskaidys vienos turto knygos procentinę dalį naujai turto knygai.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: d8e5fdc8a7b326daca1fc0f0962c69bb8fb1ff64
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839718"
---
# <a name="split-a-fixed-asset"></a>Skaidyti ilgalaikį turtą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas išskaidys vienos turto knygos procentinę dalį naujai turto knygai.  Jis naudoja vaidmenį Buhalteris ir USMF demonstracinius duomenis.


## <a name="create-a-new-fixed-asset"></a>Kurti naują ilgalaikį turtą
1. Eikite į dalį Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas.
2. Spustelėkite Naujas.
3. Lauke Ilgalaikio turto grupė įveskite arba pasirinkite reikšmę.
4. Pasižymėkite ilgalaikio turto numerį, kuris bus vėliau naudojamas skaidymo procese.
5. Lauke Pavadinimas surinkite reikšmę.
6. Uždarykite formą.

## <a name="split-a-fixed-asset"></a>Skaidyti ilgalaikį turtą
1. Sąraše raskite ir pasirinkite skaidytiną ilgalaikį turtą.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Spustelėkite Knygos.
    * Pasirinkite, kurią knygą padalinti naujajam turtui.  
4. Spustelėkite Funkcijos.
5. Spustelėkite Skaidyti ilgalaikį turtą.
6. Lauke Į ilgalaikį turtą įveskite arba pasirinkite reikšmę.
7. Lauke Į knygą spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Lauke Operacijos data įveskite datą.
9. Lauke Procentas įveskite skaičių.
10. Lauke Žurnalo pavadinimas įveskite arba pasirinkite reikšmę.
11. Spustelėkite GERAI.

## <a name="post-the-journal-transaction"></a>Registruoti žurnalo operaciją
1. Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.
2. Sąraše pasirinkite žurnalą, sukurtą skaidymo procesu.
3. Spustelėkite Eilutės.
    * Patikrinkite sukurtas žurnalo eilutes.  Sukuriama pradinio turto įsigijimo koregavimo operacija, kad būtų galima sumažinti reikšmę procentine dalimi, nurodyta skaidymo proceso metu.  Sukuriama tos pačios sumos naujojo turto įsigijimo operacija.  
4. Spustelėkite Registruoti.

