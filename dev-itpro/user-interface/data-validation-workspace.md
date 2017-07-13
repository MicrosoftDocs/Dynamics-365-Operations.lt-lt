---
title: "Duomenų tikrinimo darbo sritis"
description: "Naudodami duomenų tikrinimo kontrolinio sąrašo darbo sritį galite sekti visų įmonių, sričių ir žmonių duomenų tikrinimo procesus. Kontrolinį sąrašą galima naudoti atliekant naują diegimą, po atnaujinimo arba perkėlus."
author: bking
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: 
ms.assetid: 
ms.search.region: Global
ms.author: bking
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: e105c4b171979a03c20718c1fa9d558c921cd704
ms.contentlocale: lt-lt
ms.lasthandoff: 06/20/2017


---

# <a name="data-validation-workspace"></a>Duomenų tikrinimo darbo sritis

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama **Duomenų tikrinimo kontrolinio sąrašo darbo srities** ir susijusios konfigūracijos apžvalga.

## <a name="data-validation-checklist-workspace"></a>Duomenų tikrinimo kontrolinio sąrašo darbo sritis

Naudodami darbo sritį **Duomenų tikrinimo kontrolinis sąrašas** galite sekti visų įmonių, sričių ir žmonių duomenų tikrinimo procesus. Kontrolinį sąrašą galima naudoti atliekant naują diegimą, po atnaujinimo arba perkėlus. Priklausomai nuo darbo srities **Duomenų tikrinimo kontrolinis sąrašas** rodinio, matote arba visas duomenų tikrinimo projekto užduotis ir būsenas, arba tik jums priskirtas užduotis.

Pirmiausia darbo srities viršuje turite pasirinkti duomenų tikrinimo projektą. Tada visi darbo srityje rodomi duomenys filtruojami pagal pasirinktą duomenų tikrinimo projektą.

### <a name="summary-tiles"></a>Suvestinės išklotinės

Išklotinėse **Suvestinė** pateikiama proceso apžvalga ir indikatoriai, padedantys sekti duomenų tikrinimo procesą. Galite matyti visas likusias, atliktas, atliekamas ir nepradėtas proceso užduotis. Ši informacija skirta visoms įmonėms, kurios įtrauktos į pasirinktą duomenų tikrinimo projektą.

### <a name="tasks-and-status-section"></a>Užduotys ir būsenos dalis

Skyriuje **Užduotys ir būsena** bendra duomenų tikrinimo projekto būsena rodoma įvairiais būdais: būsena pagal juridinį subjektą, pagal sritį ir pagal užduočių sąrašą. Norėdami peržiūrėti konkrečios įmonės būseną, galite pasirinkti filtrą. Kiekviename būsenos skirtuke pateikiamas suskaidymas pagal baigimo procentinę dalį ir likusių užduočių skaičių.

Paskutinis skirtukas skirtas išsamiam užduočių sąrašui. Šiame sąraše išvardijamos visos užduotys.
Užduočių sąrašą galite filtruoti keliais būdais. Norėdami pakeisti užduoties būseną arba priskirti užduotį, spustelėkite **Redaguoti užduotį**. Norėdami peržiūrėti užduoties priedus, spustelėkite **Priedai**.

Užduoties pavadinimas yra nuorodą į „Microsoft Dynamics 365 for Finance and Operations“ (leidimas „Enterprise‟) puslapį arba kitą tinklalapį, kuriame turi apsilankyti vartotojas, norėdamas užbaigti darbą. Šį hipersaitą galite nustatyti naudodami lauką **Meniu elemento pavadinimas**, kai redaguojate arba kuriate užduotį naudodami formą **Konfigūruoti duomenų tikrinimo projektą**.

Naudodami veiksmą **Priedai** prie užduoties galite pridėti failus, pastabas, vaizdus ir URL. Pavyzdžiui, galite pridėti išspausdintą užduoties ataskaitos failą. Jei esama priedo, užduoties stulpelyje **Priedas** atsiranda piktograma.

Atlikus užduotį parinktis **Baigė** bus užpildoma automatiškai ir joje bus nurodomas užduotį atlikusio darbuotojo vardas. Kai užduotis pažymėta kaip baigta, laukas **Baigimo data** atnaujinamas automatiškai, nurodant dabartinę datą ir laiką.

### <a name="configure-data-validation-project-page"></a>Konfigūruoti duomenų tikrinimo projekto puslapį

Prieš naudodami darbo sritį **Duomenų tikrinimo kontrolinis sąrašas** turite sukonfigūruoti procesą naudodami puslapį **Konfigūruoti duomenų tikrinimo projektą**. (Spustelėkite **Darbo sritys** \> **Duomenų tikrinimo kontrolinis sąrašas** \> **Konfigūruoti duomenų tikrinimo projektą**.)

### <a name="task-areas"></a>Užduočių sritys

Norėdami grupuoti savo organizacijos duomenų tikrinimo užduotis į logines nuosavybės sritis, naudokite užduočių sritis. Pavyzdžiui, kaip užduočių sritis galima naudoti Mokėtinos sumos, Gautinos sumos arba Didžioji knyga.

**Meniu elemento pavadinimas** susietas su užduoties darbo pastanga ir gali būti naudojamas norint pereiti iš darbo srities užduoties saito tiesiogiai į susietą puslapį. Pvz., duomenų tikrinimo užduotį, kuri skirta parengti mokėtinų sumų ataskaitą **Mokėtinų sumų skirstymas pagal terminus**, galima susieti su puslapiu **Mokėtinų sumų skirstymo pagal terminus ataskaita**.

