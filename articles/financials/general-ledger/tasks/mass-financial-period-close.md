---
title: Masinis finansinio laikotarpio uždarymas
description: Šioje procedūroje parodoma, kaip sulaikyti laikotarpį arba visam laikui uždaryti laikotarpį ar daugiau nei vieną juridinį subjektą tuo pat metu.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564486"
---
# <a name="mass-financial-period-close"></a>Masinis finansinio laikotarpio uždarymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip sulaikyti laikotarpį arba visam laikui uždaryti laikotarpį ar daugiau nei vieną juridinį subjektą tuo pat metu. Be to, užduotyje parodoma, kaip apriboti vartotojų grupę registruoti naudojant konkrečius modulius.

1. Pasirinkite DK > Laikotarpio uždarymas > DK kalendoriai.
    * Atminkite, kad rodomų juridinių subjektų sąrašas priklauso nuo puslapyje pasirinkto finansinio kalendoriaus. Bus rodomi tik tie juridiniai subjektai, kurie naudoja pasirinktą finansinį kalendorių.  
2. Spustelėkite Redaguoti.
3. Pasirinkite laikotarpį, kurio būseną norite keisti.
4. Pasirinkite juridinius subjektus, kurių būseną norite naujinti.
    * Galite greitai pasirinkti visus juridinius subjektus, pažymėdami žymės langelį, esantį tinklelio viršuje, kairėje pusėje.  
5. Pasirinkite Naujinti modulio prieigą, norėdami nustatyti registravimo prieigą prie pasirinkto modulio.
    * Kiekviena modulio būsena taip pat gali būti atnaujinta, redaguojant įrašus tinklelyje. Mygtukas yra naudingas, kai norite greitai atnaujinti kelis juridinio subjekto įrašus.  
6. Lauke Programos modulis pasirinkite modulį, kurio būseną norite naujinti. Spustelėkite Pažymėti.
7. Lauke Prieigos lygis pasirinkite Visi, Nė vienas arba konkrečią vartotojų grupę. Spustelėkite Pažymėti.
    * Visi reiškia, kad visi vartotojai, turintys prieigą redaguoti modulį, gali užregistruoti, jei laikotarpis atidarytas. Niekas reiškia, kad nė vienas vartotojas negali registruoti į modulį, jei laikotarpis atidarytas. Konkreti vartotojų grupė reiškia, kad į modulį registruoti gali tik grupės vartotojai, jei laikotarpis atidarytas.  
8. Spustelėkite Naujinti.
9. Pasirinkite kitą laikotarpį, kurio būseną naujinsite.
10. Pasirinkite juridinius subjektus, kurių laikotarpio būseną norite naujinti.
11. Pasirinkite Naujinti laikotarpio būseną ir nustatykite būseną Sulaikyta, Atidaryta arba Uždaryta visam laikui.
    * Atidaryta reiškia, kad į laikotarpį galima registruoti, jei vartotojas turi prieigą. Būsena Sulaikyta nurodo, kad laikotarpyje negalima registruoti, bet jį galima iš naujo atidaryti. Būsena Uždaryta visam laikui nurodo, kad laikotarpis yra uždarytas ir nebebus galima jo atidaryti. Koregavimų registruoti negalima. Nerekomenduojama nustatyti laikotarpio būsenos Uždaryta visam laikui, kol nėra pabaigti visi koregavimai ir auditai.  
12. Spustelėkite Naujinti.

