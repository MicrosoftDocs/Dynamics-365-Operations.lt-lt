---
title: Nusidėvėjimo pasiūlymo kūrimas
description: Šioje temoje aprašoma, kaip veikia nusidėvėjimo paketo pasiūlymai, ir paaiškinama, kaip pasiūlyti ilgalaikio turto nusidėvėjimą.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90c24e9d89c055ea95ca5f25cd85ef4042476a90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187066"
---
# <a name="create-a-depreciation-proposal"></a>Nusidėvėjimo pasiūlymo kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje aprašoma, kaip veikia nusidėvėjimo paketo pasiūlymai, ir paaiškinama, kaip pasiūlyti ilgalaikio turto nusidėvėjimą. Ši užduotis naudoja USMF demonstracinių duomenų įmonę ir buhalterio vaidmenį.


## <a name="create-a-depreciation-proposal"></a>Nusidėvėjimo pasiūlymo kūrimas
1. Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Kurti nusidėvėjimo pasiūlymą**.
2. Lauke **Žurnalo pavadinimas** išplečiamajame meniu pažymėkite parinktį.
3. Lauke **Pabaigos data** įveskite datą.

    - Pažymėkite parinktį **Apibendrinti nusidėvėjimą**, kad vienoje žurnalo eilutėje apibendrintumėte mėnesinį nusidėvėjimą.  
    - Pavyzdžiui., jei reikšmė Pabaigos data yra 2015 m. kovo 31 d., sugeneruojamas toks aprašas: „Nusidėvėjimas nuo 2015 m. sausio 31 d.“. Tada lauke **Data** pasiūlytoje žurnalo eilutėje yra nustatyta 2015 m. kovo 31 d.  
    - Nusidėvėjimo pasiūlymą galima filtruoti pagal turtą, turto grupę arba kitus kriterijus naudojant parinktį **Filtras**.  
    - Kai naudojate formą **Kurti ilgalaikio turto įsigijimo arba nusidėvėjimo pasiūlymą**, nusidėvėjimą galite siūlyti paketais. Tai rekomenduojama didesniems projektams, kurie naudos daugiau sistemos išteklių. Jei pasirenkate paketo parinktį, vis tiek galite per tą laiką užbaigti kitas užduotis. Kai siūlote nusidėvėjimą tokiu būdu, nusidėvėjimas apskaičiuojamas ilgalaikio turto vertinimo modeliams.  

4. Pažymėkite **Kurti žurnalą**.

## <a name="review-depreciation-entries"></a>Peržiūrėti nusidėvėjimo įrašus
1. Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Pasirinkite **Eilutės**.
4. Pasirinkite **Registruoti**.
