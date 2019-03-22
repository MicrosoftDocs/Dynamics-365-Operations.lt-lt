---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. sausio 31 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ab43bab53afd979d64099425f0582f6c1bb5a8b0
ms.sourcegitcommit: 383a344deb5abf48584ea2ee7774b8dbbbec49b3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/08/2019
ms.locfileid: "377855"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. sausio 31 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 for Talent“ funkcijos

**8.1.2128 versija**

## <a name="core-hr-changes"></a>„Core HR“ pakeitimai

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Nurodant atostogų laiką atostogaujančių žmonių kortelėje neatsižvelgiama į atostogų plano datas
Tiems, kurių atostogų planai nesudaromi pagal kalendorinius metus, kortelė **Užimta** dabar rodo užimtą laiką planu apibrėžtuose atostogų metuose. Pavyzdžiui, jei organizacijos atostogų metai yra nuo birželio 1 d. iki gegužės 30 d. ir darbuotojas atostogavo 3 dienas gruodžio mėn., kortelė **Užimta** sausio 15 d. rodys 3 dienas. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Kaupimo sumos nesutampa su pakopos datos pagrindu
Naujos parinktys įtrauktos į atostogų ir neatvykimo nustatymus (**personalo** parametrus), kad klientai galėtų nustatyti, kada darbuotojų aptarnavimo datų mėnesiai yra aktyvūs. Kai kuriose organizacijose data yra mėnesio pabaiga, tačiau kitose tai gali būti kito mėnesio pradžia. Pvz., viena organizacija gali skirti atostogų laiką gruodžio 31 d., o kita gali skirti atostogų laiką sausio 1 d. Ši parinktis suteiks galimybę pasirinkti, kada skyrimas turėtų įvykti. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Darbuotojo samdos veiksmų būsena Darbo eiga baigta nesikeičia
Atlikti keitimai siekiant ištaisyti problemą, dėl kurios kelios darbo eigos baigdavosi nustatant būseną Darbo eiga baigta. Naujos darbo eigos dabar turėtų būti perkeltos į būseną Užbaigta, kai darbo eiga baigiama. Visos darbo eigos, kurių darbo eigos būsena baigta, bus perkeltos į klaidos būseną, kad pagal poreikį būtų galima atnaujinti arba pašalinti. 
