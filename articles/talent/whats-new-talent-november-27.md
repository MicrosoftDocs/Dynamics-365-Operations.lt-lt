---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent – Core HR“ (2018 m. lapkričio 27 d.)
description: Šioje temoje aprašomos „Microsoft“ sistemos „Dynamics 365 Talent – Core HR“ naujos ir pakeistos funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9ff375ca97444d060c701e27c8fdcfecab4df186
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010181"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-november-27-2018"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent: Core HR“ (2018 m. lapkričio 27 d.)

[!include [banner](includes/banner.md)]

**8.1.2064 versija**

Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.


## <a name="changes"></a>Pakeitimai

### <a name="unable-to-create-a-note-in-case-management"></a>Nepavyksta sukurti pastabos sprendime Atvejų valdymas

Atliktas pakeitimas, susijęs su problema, kildavusia bandant redaguoti ar sukurti pastabą sprendimo Atvejų valdymas atvejo žurnale.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Klaidingai parašytas žodis kompensacijos darbo srityje pateikiamame kompensavimo skirtuke 

Žodžių „Etninė kilmė“, esančių kompensacijos darbo srities kompensacijos analizės diagramoje rašyba pakeista į teisingą.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Kai vartotojas nepriskirtas darbininkui, darbuotojų savitarnos darbo sritis nerodoma. 

Atliktas pakeitimas, susijęs su tuo, kai pirmame paleisties puslapyje vartotojas, kuris nėra priskirtas darbininkui, pasirinkdavo darbo sritį **Darbuotojų savitarna**. Tokiu atveju bus rodoma numatytoji ataskaitų sritis.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Su atostogomis ir neatvykimu susijusi klaida: objekto egzemplioriui nenustatyta objekto nuoroda.

Atlikta su atostogomis ir neatvykimu susijusių pakeitimų, siekiant ištaisyti šią klaidą, kai sąraše **Man priskirti darbo elementai** patvirtinami su atostogomis ir neatvykimu susiję įrašai.

### <a name="unable-to-recall-an-image-workflow"></a>Nepavyksta atšaukti vaizdo darbo eigos

Atšaukus vaizdo darbo eigą, ši eiga bus nustatyta kaip „Atšaukta“, o esamą užklausą bus galima panaikinti darbuotojų savitarnos darbo srityje.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Po atleidimo keletą kartų rodomi pakartotinai pasamdyti darbuotojai arba rangovai. 

Po šio atnaujinimo atleisti ir pakartotinai pasamdyti darbuotojai esamame sąraše bus rodomi tik kartą. 

## <a name="known-issue"></a>Žinoma problema

- **Problema**: įtraukiant naują priedą į darbininko puslapį mygtukai **Naujas** ir **Redaguoti** yra papilkinti. 
- **Problemos sprendimas:** prieš atidarydami priedų puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti. Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti. (Ši problema bus pašalinta kitame platformos naujinime.)
