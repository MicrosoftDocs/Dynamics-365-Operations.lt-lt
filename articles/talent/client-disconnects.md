---
title: "Atsijungia „Talent“ klientas"
description: "Šioje temoje paaiškinama, ką daryti, jei klientas (-ė) atjungiamas (-a) nuo savo aplinkos ir nežino, kodėl."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 4f96b986059c179268f8a96ea7e7725831a93524
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

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

**Problema** 

**Naršyklės tipai:** „Google Chrome“, „Internet Explorer“ ir „Microsoft Edge“

„Microsoft Dynamics 365 for Talent“ platforma atjungia vartotojus, kai vienu metu tam pačiam vartotojui ir tam pačiam naršyklės tipui atidaromi du skirtingi seansai. (Pavyzdžiui, vartotojas A peržiūri 1 ir 2 aplinkas naršyklėje „Chrome“.) Nesvarbu, ar vartotojai atidaro skirtingus naršyklės langus, ar skirtingus skirtukus. Naudojant to paties vartotojo kredencialus prisijungti prie 1 ir 2 aplinkų vienu metu ir tuo pačiu naršyklės tipu, „Talent“ atjungia vieną iš seansų.

**Sprendimas**

Įsitikinkite, kad naudojant nurodytą naršyklės tipą vienu metu atidaryta tik viena aplinka. Vartotojai gali atidaryti kelis seansus toje pačioje aplinkoje (t. y. kelis skirtukus toje pačioje naršyklėje).

Vartotojai, norintys vienu metu pereiti iš vienos aplinkos į kitą, kiekvieną aplinką turi atidaryti naudodami kitą naršyklės tipą. (Pavyzdžiui, vartotojas A gali peržiūrėti 1 aplinką naršyklėje „Chrome“, o 2 aplinką – naršyklėje „Microsoft Edge“.)

