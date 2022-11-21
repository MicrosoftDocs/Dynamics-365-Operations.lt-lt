---
title: Masinis finansinio laikotarpio uždarymas
description: Šiame straipsnyje rodoma, kaip sulaikyti laikotarpį arba visam laikui uždaryti laikotarpį ar daugiau nei vieną juridinį subjektą.
author: aprilolson
ms.date: 11/16/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a85d512842b27f2d74507be16a8f2819f483e0d
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779832"
---
# <a name="mass-financial-period-close"></a>Masinis finansinio laikotarpio uždarymas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje rodoma, kaip sulaikyti laikotarpį arba visam laikui uždaryti laikotarpį ar daugiau nei vieną juridinį subjektą. Be to, užduotyje parodoma, kaip apriboti vartotojų grupę registruoti naudojant konkrečius modulius.

1. Naršymo srityje eikite į DK **, kai > laikotarpio uždarymą > DK kalendorius**. 

>[!NOTE]
> Rodomas juridinių subjektų sąrašas priklauso nuo puslapyje pasirinkto finansinio kalendoriaus. Bus rodomi tik tie juridiniai subjektai, kurie naudoja pasirinktą finansinį kalendorių.

2. Pasirinkite **Redaguoti**.
3. Pasirinkite laikotarpį, kurio būseną norite keisti.
4. Pasirinkite juridinius subjektus, kurių būseną norite naujinti. Galite greitai pasirinkti visus juridinius asmenis užžymėję varnelę tinklelio viršutinėje kairėje pusėje.  
5. Pažymėkite **Naujinti modulio prieigą**, kad nurodytumėte registravimo prieigą pasirinktam moduliui. Kiekviena modulio būsena taip pat gali būti atnaujinta, redaguojant įrašus tinklelyje. Mygtukas yra naudingas, kai norite greitai atnaujinti kelis juridinio subjekto įrašus.  
6. Modulyje **Taikymas** pasirinkite modulį, kuriam norite naujinti būseną. Spustelėkite **Pažymėti**.
7. Lygyje **Prieiga** pasirinkite **Visa**, **Nė vienas** arba konkrečią vartotojų grupę. Spustelėkite **Pažymėti**.  
- **Visi** – visi vartotojai, kurie turi redagavimo prieigą prie modulio, gali registruotis, jei laikotarpis atviras. 
- **Nėra** – vartotojai negali registruoti modulyje, jei laikotarpis atviras. Konkreti vartotojų grupė reiškia, kad į modulį registruoti gali tik grupės vartotojai, jei laikotarpis atidarytas.  
8. Pasirinkite **Atnaujinti**, 
9. Pasirinkite kitą laikotarpį, kurio būseną naujinsite.
10. Pasirinkite juridinius subjektus, kurių laikotarpio būseną norite naujinti.
11. Pasirinkite **Naujinti laikotarpio būseną** ir nustatykite būseną į **Atidėtas**, **Atviras** arba **Panaikintas visam laikui**. **Atviras** nurodo, kad laikotarpį galima registruoti, jei naudotojas turi prie jo prieigą. **Atidėtas** reiškia, jog laikotarpį negalima registruoti, tačiau laikotarpį galima vėl atverti. **Panaikintas visam laikui** reiškia, jog laikotarpis yra panaikintas ir negali būti atvertas. Koregavimų registruoti negalima. Mes nerekomenduojame nustatyti laikotarpio kaip Uždaryta visam **laikui,** kol nebus atlikti visi koregavimai ir auditai.  
12. Pasirinkite **Naujinti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
