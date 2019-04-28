---
title: Atsijungia „Talent“ klientas
description: Šioje temoje paaiškinama, ką daryti, jei klientas (-ė) atjungiamas (-a) nuo savo aplinkos ir nežino, kodėl.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 885e2d743cd2b01588546327840508f6f7e95958
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "859925"
---
# <a name="talent-client-disconnects"></a>Atsijungia „Talent“ klientas

[!include [banner](includes/banner.md)]

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

„Microsoft Dynamics 365 for Talent“ platforma atjungia vartotojus, kai vienu metu tam pačiam vartotojui ir tam pačiam naršyklės tipui atidaromi du skirtingi seansai. (Pavyzdžiui, vartotojas A peržiūri 1 ir 2 aplinkas naršyklėje „Chrome“.) Nesvarbu, ar vartotojai atidaro skirtingus naršyklės langus, ar skirtingus skirtukus. Naudojant to paties vartotojo kredencialus prisijungti prie 1 ir 2 aplinkų vienu metu ir tuo pačiu naršyklės tipu, „Talent“ atjungia vieną iš seansų.

**Sprendimas**

Įsitikinkite, kad naudojant nurodytą naršyklės tipą vienu metu atidaryta tik viena aplinka. Vartotojai gali atidaryti kelis seansus toje pačioje aplinkoje (t. y. kelis skirtukus toje pačioje naršyklėje).

Vartotojai, norintys vienu metu pereiti iš vienos aplinkos į kitą, kiekvieną aplinką turi atidaryti naudodami kitą naršyklės tipą. (Pavyzdžiui, vartotojas A gali peržiūrėti 1 aplinką naršyklėje „Chrome“, o 2 aplinką – naršyklėje „Microsoft Edge“.)
