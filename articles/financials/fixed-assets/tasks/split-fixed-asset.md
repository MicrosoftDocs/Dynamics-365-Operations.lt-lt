--- 
title: "Skaidyti ilgalaikį turtą"
description: "Šis užduočių vadovas išskaidys vienos turto knygos procentinę dalį naujai turto knygai."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="split-a-fixed-asset"></a>Skaidyti ilgalaikį turtą

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


