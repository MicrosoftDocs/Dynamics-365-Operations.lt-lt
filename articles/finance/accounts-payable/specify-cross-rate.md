---
title: Kryžminio tarifo nurodymas
description: Šioje temoje pateikiama informacija apie kryžminius tarifus programoje „Microsoft“ „Dynamics 365 Finance“.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46ac3324a985810ede61072190014538d0b7ed36f7eedfc387468619cc88cb2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737022"
---
# <a name="specify-the-cross-rate"></a>Kryžminio tarifo nurodymas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama kryžminio kurso paskirtis, ir kaip nurodyti kryžminį kursą sudengiant mokėjimą su SF. Naudokite kryžminį kursą, kai taikomi visi šie kriterijai. 
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