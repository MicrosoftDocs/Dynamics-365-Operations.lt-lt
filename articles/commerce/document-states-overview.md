---
title: Dokumentų būsenos ir vykdymo ciklas
description: Šiame straipsnyje nurodytos įvairios puslapio elementų dokumentų valstijos Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 04836ecf80fc86ab6abb96e4255779c8c03988d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909463"
---
# <a name="document-states-and-lifecycle"></a>Dokumentų būsenos ir vykdymo ciklas

[!include [banner](includes/banner.md)]

Šiame straipsnyje nurodytos įvairios puslapio elementų dokumentų valstijos Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Dokumento būsenos aprašas

Puslapio [elementų straipsnyje](page-elements-overview.md) pateikiami įvairūs dokumentų tipai turinio valdymo sistemoje (CMS). Šie dokumentų tipai gali turėti kelias būsenas kūrimo įrankyje. Dokumentų būsenos padeda apsaugoti nuo duomenų nesuderinamumo ir įgalinti versijų valdymą. Jomis galima nustatyti, kas gali keisti dokumentus, kada dokumentai gali būti keičiami ir kada keitimus gali peržiūrėti kiti asmenys.

Šioje lentelėje pateikiamos galimos „Commerce“ puslapio elementų dokumento būsenos.

| Dokumento būsena      | Svetainių daryklės veiksmai        | aprašymas                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Išregistruota         | Pasirinkite **Redaguoti**.           | Taikomas dokumentas paimamas ir užrakinamas. Kol dokumentas yra šioje būsenoje, jo negalima pakeisti kiti autentifikuoti sistemos vartotojai, o visi keitimai, kuriuos atliekate dokumente, matomi tik jums. |
| Įrašyta               | Pasirinkite **Įrašyti**.           | Keitimai, atlikti išregistruotame dokumente, įrašomi į duomenų bazę, tačiau dokumentas dar nėra įrašomas ir atrakinamas ar publikuojamas. Įrašyti keitimai nematomi kitiems autentifikuotiems sistemos vartotojams, kol autorius nepasirenka **Baigti redagavimą**. Jie nematomi išoriniams vartotojams, kol elementas nebus publikuotas. |
| Atmestas paėmimas ir užrakinimas | Pasirinkite **Atmesti pakeitimus**.  | Visi išregistruoto dokumento pakeitimai atmetami, o elementas grįžta į paskutinę įrašytą ir atrakintą versiją. |
| Įregistruota          | Pasirinkite **Baigti redagavimą**. | Redaguotas dokumentas yra įrašomas ir atrakinamas. Visi pakeitimai yra matomi kitiems autentifikuotiems sistemos vartotojams ir tie vartotojai gali redaguoti dokumentą. Kiekvienas įrašymas ir atrakinimas sukuria dokumento versijos įrašą elemento retrospektyvoje. |
| Publikuota           | Pasirinkite **Publikuoti**.        | Dokumentas publikuojamas, o pakeitimai yra paskelbiami jūsų paleistoje svetainėje ir tampa aptinkami išoriniams vartotojams. Elementai gali būti publikuojami tik tada, kai jie įrašyti ir atrakinti pasirinkus **Baigti redagavimą**. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Turinio įtraukimo būdai](add-manage-content.md)

[Puslapio modelio žodynas](page-elements-overview.md)

[Darbas su publikavimo grupėmis](publish-groups.md)

[Kelių kanalų bendrinimo funkcijos įjungimas ir naudojimas](cross-channel-sharing.md)

[Darbas su moduliais](work-with-modules.md)

[Darbas su fragmentais](work-with-fragments.md)

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Svetainės naršymo tinkinimas](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]