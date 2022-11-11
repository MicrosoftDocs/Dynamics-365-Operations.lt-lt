---
title: Plano retrospektyvos ir planavimo žurnalų peržiūra
description: Šiame straipsnyje paaiškinama, kaip peržiūrėti planavimo užduočių retrospektyvą.
author: t-benebo
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740937"
---
# <a name="view-plan-history-and-planning-logs"></a>Plano retrospektyvos ir planavimo žurnalų peržiūra

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip peržiūrėti "Microsoft" planavimo užduočių retrospektyvą Dynamics 365 Supply Chain Management.

Norėdami peržiūrėti plano istoriją, atidarykite planą eidami į **Pagrindinis planavimas** \> **Sąranka** \> **Planai** \> **Bendrieji planai** ir pasirinkite **Istorija**. Istorijoje išvardintos visos pasirinkto plano užduotys. Į sąrašą įtrauktos baigtos ir aktyvios užduotys.

Sistema išlaiko daugiausia 60 retrospektyvos įrašų vienam planui ir panaikina senesnius nei 30 dienų įrašus. Kaskart jums paleidus naują bendrojo planavimo skaičiavimą, sistema prideda naują retrospektyvos įrašą ir, jei reikia, išvalo seniausius įrašus.

Be užduočių pradžios laiko ir būsenos, taip pat galite peržiūrėti konkrečios užduoties žurnalą. Žurnale pateikiama papildoma informacija ir įspėjimai. Ne visos užduotys turi žurnalą. Norėdami peržiūrėti užduoties žurnalą, pasirinkite **Žurnalas.** Žurnalo įrašai saugomi tik 30 dienų po užduoties pabaigos datos, po to, kai jie automatiškai panaikinami.

Jei „FastTab” **Vykdyti fone** parinktis **Paketinis apdorojimas** buvo įgalinta nustačius bendrojo planavimo apdorojimą, paketinių užduočių žurnale rodoma daugiau informacijos apie įspėjimus ir klaidas, sugeneruotus bendrojo planavimo vykdymo metu. Pavyzdžiui, automatinio užbaigimo klaidos yra fiksuojamos tik paketinių užduočių žurnale. Jos nėra rodomos **Retrospektyvos** puslapio žurnaluose.

Norėdami peržiūrėti automatinio užbaigimo klaidas ir kitus įspėjimus ar klaidas, įvykusius bendrojo planavimo metu, atlikite šiuos veiksmus.

1. Pasirinkite **Sistemos administravimas \> Užklausos \> Paketinės užduotys**.
1. Raskite ir pasirinkite įrašą, atspindintį jus dominantį bendrojo planavimo vykdymą. (Pavyzdžiui, lauko **Užduoties aprašas** reikšmė gali prasidėti *Bendrasis planavimas*.)
1. Atlikite vieną iš šių veiksmų, priklausomai nuo to, ar naudojate *patobulintą formą* ar *senstelėjusią (nepatobulintą) formą* puslapiui **Paketinės užduotys**:

    - Jei naudojate patobulintą formą: veiksmų srityje pasirinkite **Paketinių užduočių retrospektyvą**. Tada veiksmų srities puslapyje **Paketinių užduočių retrospektyva** pasirinkite **Žurnalas**.
    - Jei naudojate senstelėjusią formą: veiksmų srities skirtuke **Paketinė užduotis** pasirinkite **Žurnalas**.

1. Pasirinkite **Pranešimo informacija**, kad atidarytumėte **Pranešimo informacijos** sritį, kurioje galite peržiūrėti visus įspėjimus ir klaidas, užfiksuotus apdorojimo metu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
