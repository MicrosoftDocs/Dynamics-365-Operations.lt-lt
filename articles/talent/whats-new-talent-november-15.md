---
title: "Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. lapkričio 15 d.)"
description: "Šioje temoje aprašomos naujos ir pakeistos šio „Microsoft Dynamics 365 for Talent“ „Core HR“ funkcijos."
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 3cc19a8e5f726495e698a3a2f4ccce7460a61657
ms.openlocfilehash: 0e9de5e36e67941ab09c773a63b0e7045105a07e
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-15-2018"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. lapkričio 15 d.)

[!include [banner](includes/banner.md)]

**8.1.2045 versija**

Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.

## <a name="other-changesfixes"></a>Kiti pakeitimai / pataisos

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Nepavyksta dabartinių darbuotojo pareigų pakeisti būsimas atviras pareigas

Atliktas pakeitimas, kad būtų galima perkelti pareigas, kai jos pasiekiamos tik ateityje. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Kuriant naują darbuotoją nerodomos pareigos

Atliktas pakeitimas, kad programoje „Talent“ samdant naujus darbuotojus būtų rodomos visos pasiekiamos pareigos, kurias galima priskirti. Tai taikoma retrospektyvinėms pareigoms arba tuo atveju, jei pareigų data yra būsima. Dabar pareigos, priklausomai nuo įdarbinimo pradžios datos, bus rodomos teisingai. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Dabar atleidimo data rodoma remiantis vartotojo parametrais

Atliktas buvusių darbuotojų sąrašo pakeitimas, kad peržiūrint atleidimo datą darbuotojai sąrašą galėtų pritaikyti pagal pageidaujamus laiko juostos poslinkius.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Man priskirti darbo elementai siejasi su neteisingai rodoma informacija

Atlikus šį pakeitimą, naršant po išsamią atskirų darbo elementų, esančių sąraše, informaciją, bus rodoma teisinga pasirinkto elemento informacija. Ši problema iškildavo tik taikant išplėstines saugos parinktis.


## <a name="known-issue"></a>Žinoma problema

- **Problema**: įtraukiant naują priedą į darbininko puslapį mygtukai **Naujas** ir **Redaguoti** yra papilkinti. 
- **Problemos sprendimas:** prieš atidarydami priedų puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti. Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti. (Ši problema bus pašalinta kitame platformos naujinime.)

