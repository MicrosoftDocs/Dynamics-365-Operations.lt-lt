---
title: Klientas atsijungia
description: Šiame straipsnyje paaiškinama, ką daryti, jei klientas (-ė) atjungiamas (-a) nuo savo aplinkos ir nežino, kodėl.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2088706baf8735fa371960955a2ffc3240ccac76
ms.sourcegitcommit: a26e4963d40796da21ce6581cfb2f4d9db4f6776
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/27/2020
ms.locfileid: "4419805"
---
# <a name="client-disconnects"></a>Klientas atsijungia

**Aplinkos informacija** 

Ši problema gali kilti visose aplinkose.
 
**Požymis** 

Klientas (-ė) atjungiamas (-a) nuo savo aplinkos ir nežino, kodėl. Klientui rodomas vienas iš toliau pateiktų klaidos pranešimų.

- Nutrūko ryšys su jumis. Spustelėkite Uždaryti, kad galėtumėte tęsti darbą.
- Atrodo, kad nutrūko tinklo ryšys. Spustelėkite Kartoti, jei norite bandyti dar kartą.

**Raudona vėliavėlė**

Taip dažnai nutinka, kai vartotojai, vykdydami įdiegimo etapą, lygina informaciją gamybos bei bandomojoje aplinkose ir pamiršta, kad tarp seansų jos persijungia. Jei vartotojai vykdo šį etapą, jie greičiausiai susidurs su šia problema.

**Išduoti** 

**Naršyklės tipai**: „Google Chrome“, „Internet Explorer“ ir „Microsoft Edge“

„Microsoft Dynamics 365 Human Resources“ atjungia vartotojus, kai vienu metu tam pačiam vartotojui ir tam pačiam naršyklės tipui atidaromi du skirtingi seansai. (Pavyzdžiui, vartotojas A peržiūri 1 ir 2 aplinkas naršyklėje „Chrome“.) Nesvarbu, ar vartotojai atidaro skirtingus naršyklės langus, ar skirtingus skirtukus. Naudojant to paties vartotojo kredencialus prisijungti prie 1 ir 2 aplinkų vienu metu ir tuo pačiu naršyklės tipu, „Human Resources“ atjungia vieną iš seansų.

**Sprendimas**

Įsitikinkite, kad naudojant nurodytą naršyklės tipą vienu metu atidaryta tik viena aplinka. Vartotojai gali atidaryti kelis seansus toje pačioje aplinkoje (t. y. kelis skirtukus toje pačioje naršyklėje).

Vartotojai, norintys vienu metu pereiti iš vienos aplinkos į kitą, kiekvieną aplinką turi atidaryti naudodami kitą naršyklės tipą. (Pavyzdžiui, vartotojas A gali peržiūrėti 1 aplinką naršyklėje „Chrome“, o 2 aplinką – naršyklėje „Microsoft Edge“.)
