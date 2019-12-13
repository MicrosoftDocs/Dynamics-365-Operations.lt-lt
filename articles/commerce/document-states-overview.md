---
title: Dokumentų būsenos ir vykdymo ciklas
description: Šioje temoje aptariamos įvairios „Microsoft Dynamics 365 Commerce“ puslapių elementų būsenos.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a34d10edbf84ac1814afdc7107727aea68a303e0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770440"
---
# <a name="document-states-and-lifecycle"></a>Dokumentų būsenos ir vykdymo ciklas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aptariamos įvairios „Microsoft Dynamics 365 Commerce“ puslapių elementų būsenos.

## <a name="document-state-descriptions"></a>Dokumento būsenos aprašas

Temoje [Puslapio elementai](page-elements-overview.md) pateikiama įvairių dokumentų tipų turinio valdymo sistemoje (TVS). Šie dokumentų tipai gali turėti kelias būsenas kūrimo įrankyje. Dokumentų būsenos padeda apsaugoti nuo duomenų nesuderinamumo ir įgalinti versijų valdymą. Jomis galima nustatyti, kas gali keisti dokumentus, kada dokumentai gali būti keičiami ir kada keitimus gali peržiūrėti kiti asmenys.

Šioje lentelėje pateikiamos galimos „Commerce“ puslapio elementų dokumento būsenos.

| Dokumento būsena | Aprašymas |
|---|---|
| Paimta ir užrakinta | Jums paėmus ir užrakinus TVS elementą, jo negali redaguoti jokie kiti autentifikuoti sistemos vartotojai. Visi keitimai, kuriuos atliekate elementui, matomi tik jums. |
| Įrašyta ir atrakinta | Kai TVS elementas įrašytas ir atrakintas, visi keitimai yra matomi kitiems autentifikuotiems sistemos vartotojams, ir tie vartotojai gali tik tada paimti ir užrakinti elementą bei jį redaguoti. Kiekvienas įrašymas ir atrakinimas sukuria dokumento versijos įrašą elemento retrospektyvoje. |
| Publikuota | Kai TVS elementas yra publikuotas, jis yra priverstinai teikiamas į jūsų tiesioginę svetainę ir tampa aptinkamas internete neautentifikuotų Išorinių vartotojų. Elementai gali būti publikuojami tik tada, kai jie įrašyti ir atrakinti. |
| Įrašyta | Keitimai, kurie buvo atlikti su paimtu ir užrakintu TVS elementu, gali būti įrašyti į TVS, prieš elementą įrašant ir atrakinant ar publikuojant. Šie įrašyti keitimai nematomi kitiems autentifikuotiems sistemos vartotojams, kol elementas nebus įrašytas ir atrakintas. Jie nematomi išoriniams vartotojams, kol elementas nebus publikuotas. |
| Atmestas paėmimas ir užrakinimas | Kai paimtas ir užrakintas TVS elementas atmetamas, visi įrašyti keitimai panaikinami, o elementas grįžta į vėliausiai įrašytą ir atrakintą versiją. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Turinio įtraukimo būdai](add-manage-content.md)

[Puslapio modelio žodynas](page-elements-overview.md)

[Darbas su moduliais](work-with-modules.md)

[Darbas su fragmentais](work-with-fragments.md)

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Svetainės naršymo tinkinimas](customize-site-navigation.md)
