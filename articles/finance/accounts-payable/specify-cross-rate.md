---
title: Kryžminio tarifo nurodymas
description: Šiame straipsnyje pateikta informacija apie kryžmines normas " Microsoft Dynamics 365 Finance".
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb01948af2bcba9ca740e8bd0e12584cf021fce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889967"
---
# <a name="specify-the-cross-rate"></a>Kryžminio tarifo nurodymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinamas kryžminio kurso tikslas ir, kaip nurodyti kryžminį kursą, kai sudengiate mokėjimą SF. Naudokite kryžminį tarifą, kai taikomi šie kriterijai: 
-   Sudengiate mokėjimą su SF. 
-   Skirtingos valiutos naudojamos mokėjimo eilutėje ir SF eilutėje. 
-   Nei viena valiuta nėra apskaitos valiuta. 

Kryžminis tarifas nenaudojamas siekiant apskaičiuoti mokėjimo operacijos valiutos konvertavimo į mokėjimo apskaitos valiutą vertę. Vietoj to, iš valiutos kursų lentelės nuskaitomi valiutos kursai, siekiant apskaičiuoti mokėjimo operacijos valiutos sumos vertę ir mokėjimo apskaitos valiutos sumos vertę. 

Pavyzdžiui, apskaitos valiuta yra USD, SF valiuta – CAD, o mokėjimo valiuta – EUR. Naudodami kryžminį kursą galite įvesti valiutos kursą – tuomet bus tiesiogiai konvertuojama iš CAD į EUR ir atvirkščiai, ir nebereikės konvertuoti naudojant USD. Pasirinkdami SF ir pirminį mokėjimą, galite įvesti kryžminį kursą SF eilutei. Kryžminis kursas yra valiutos kursas tarp dviejų valiutų, taikomas toms operacijoms sudengimo datą.

1.  Eikite į vieną iš šių puslapių:
- **Gautinos sumos > Bendra > Klientai > Visi klientai** 
- **Mokėtinos sumos > Bendra > Tiekėjai > Visi tiekėjai** 
- **Paraiškos > Bendra > Tiekėjai > Visi tiekėjai**
2.  Pasirinkite klientą arba tiekėją, kurio atviras operacijas sudengiate. 
3.  Pasirinkę klientą, sąrašo **Visi klientai** puslapyje eikite į **Surinkimas > Sudengti atidarytas operacijas**. Pasirinkę tiekėją, sąrašo **Visi tiekėjai** puslapyje eikite į **Sąskaita faktūra > Sudengti atidarytas operacijas**. 
4.  Pasirinkite operaciją, kuri yra pirminis mokėjimas, ir spustelėkite **Pažymėti mokėjimą**. Pažymimas žymės langelis stulpelyje **Pažymėti**, o stulpelyje **Pirminis mokėjimas** rodoma informacijos piktograma. 
5.  Lauke **Kryžminis tarifas** įveskite valiutos kursą, kuris sudengimo datą taikomas tarp SF valiutos ir mokėjimo valiutos. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
