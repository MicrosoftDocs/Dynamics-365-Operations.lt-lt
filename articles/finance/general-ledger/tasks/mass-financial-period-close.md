---
title: Masinis finansinio laikotarpio uždarymas
description: Šioje temoje aptariama, kaip nustatyti laikotarpį vykdyti fone arba vienu metu visiškai panaikinti laikotarpį arba daugiau nei vieną juridinį asmenį.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a149b35c6964166207effc799a02cd4c59bbb843
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445920"
---
# <a name="mass-financial-period-close"></a>Masinis finansinio laikotarpio uždarymas

[!include [banner](../../includes/banner.md)]

Šioje temoje aptariama, kaip nustatyti laikotarpį vykdyti fone arba vienu metu visiškai panaikinti laikotarpį arba daugiau nei vieną juridinį asmenį. Be to, užduotyje parodoma, kaip apriboti vartotojų grupę registruoti naudojant konkrečius modulius.

1. Naršymo srityje eikite į **Moduliai > Didžioji knyga > Laikotarpio naikinimas > DK kalendoriai**. Atminkite, kad rodomų juridinių subjektų sąrašas priklauso nuo puslapyje pasirinkto finansinio kalendoriaus. Bus rodomi tik tie juridiniai subjektai, kurie naudoja pasirinktą finansinį kalendorių.
2. Pasirinkite **Redaguoti**.
3. Pasirinkite laikotarpį, kurio būseną norite keisti.
4. Pasirinkite juridinius subjektus, kurių būseną norite naujinti. Galite greitai pasirinkti visus juridinius asmenis užžymėję varnelę tinklelio viršutinėje kairėje pusėje.  
5. Pažymėkite **Naujinti modulio prieigą**, kad nurodytumėte registravimo prieigą pasirinktam moduliui. Kiekviena modulio būsena taip pat gali būti atnaujinta, redaguojant įrašus tinklelyje. Mygtukas yra naudingas, kai norite greitai atnaujinti kelis juridinio subjekto įrašus.  
6. Modulyje **Taikymas** pasirinkite modulį, kuriam norite naujinti būseną. Spustelėkite **Pažymėti**.
7. Lygyje **Prieiga** pasirinkite **Visa**, **Nė vienas** arba konkrečią vartotojų grupę. Spustelėkite **Pažymėti**. Visi reiškia, kad visi vartotojai, turintys prieigą redaguoti modulį, gali užregistruoti, jei laikotarpis atidarytas. Niekas reiškia, kad nė vienas vartotojas negali registruoti į modulį, jei laikotarpis atidarytas. Konkreti vartotojų grupė reiškia, kad į modulį registruoti gali tik grupės vartotojai, jei laikotarpis atidarytas.  
8. Pasirinkite **Naujinti**.
9. Pasirinkite kitą laikotarpį, kurio būseną naujinsite.
10. Pasirinkite juridinius subjektus, kurių laikotarpio būseną norite naujinti.
11. Pasirinkite **Naujinti laikotarpio būseną** ir nustatykite būseną į **Atidėtas**, **Atviras** arba **Panaikintas visam laikui**. **Atviras** nurodo, kad laikotarpį galima registruoti, jei naudotojas turi prie jo prieigą. **Atidėtas** reiškia, jog laikotarpį negalima registruoti, tačiau laikotarpį galima vėl atverti. **Panaikintas visam laikui** reiškia, jog laikotarpis yra panaikintas ir negali būti atvertas. Koregavimų registruoti negalima. Nėra rekomenduotina nustatyti laikotarpį į **Panaikintas visam laikui**, kol visos korekcijos ir patikrinimai nėra baigti.  
12. Pasirinkite **Naujinti**.

