---
title: Parengti „kanban“ užduoties apdorojimą, kai nėra darbo elemento medžiagų
description: Šios procedūros tikslas yra parengti proceso „kanban“ užduotį, kai darbo elementui trūksta kai kurių medžiagų, todėl būtina paimti medžiagas iš sandėlio.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bba9e5cb7dfddd2a80a37e7a57fdf94a91341e8f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843630"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Parengti „kanban“ užduoties apdorojimą, kai nėra darbo elemento medžiagų

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šios procedūros tikslas yra parengti proceso „kanban“ užduotį, kai darbo elementui trūksta kai kurių medžiagų, todėl būtina paimti medžiagas iš sandėlio. Būtina šios procedūros sukūrimo sąlyga yra procedūra „Parengti proceso „kanban“ užduotį, kai yra reikiamų medžiagų“. Ši procedūra skirta mašinos operatoriui. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.

1. Pasirinkite Gamybos kontrolė > „Kanban“ > „Kanban“ sritis proceso užduotims.
2. Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite 1250 darbo elementą.  
4. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite „Kanban“ 000356.  
5. Sąraše raskite ir pasirinkite norimą įrašą.
    * Sąraše panaikinkite 4 eilutės žymėjimą. arba pažymėkite 4 eilutę, jei nebaigėte užduoties „Parengti proceso „kanban“ užduotį, kai yra reikiamų medžiagų“.  
6. Perjunkite skyriaus „Išrinkimo dokumentas“ išplėtimą.
    * Įrašo „Ne“ piktograma tiekimo būsenoje nurodo, kad darbo elementui trūksta 48 ae prekės P0002.  

## <a name="transfer-materials-to-work-cell"></a>Perkelti medžiagas į darbo elementą
1. Perjunkite skyriaus „Perkėlimo užduotys“ išplėtimą.
2. Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Prekės numeris pagal reikšmę P0002.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Spustelėkite Pradėti.
    * Vyksta perdavimas.  
5. Spustelėkite Baigti.
    * Prekė P0002 dabar yra „kanban“ užduoties išrinkimo dokumente. Tai reiškia, kad galime paruošti „kanban“ su visomis reikiamomis medžiagomis.  
6. Spustelėkite „Parengti“.
    * Atkreipkite dėmesį – užduoties būsenos piktograma nurodo, kad užduotis jau parengta.  

