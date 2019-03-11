---
title: Keisti apdorojimo užduoties „kanban“ taisykles
description: Ši procedūra padės pakeisti naudojamą „kanban“ taisyklę į nurodytą „kanban“.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38d9ff0a7d6aeb0a589fd6b9ab34b818c46644cc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "314951"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Keisti apdorojimo užduoties „kanban“ taisykles

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padės pakeisti naudojamą „kanban“ taisyklę į nurodytą „kanban“. Tai naudinga norint išlyginti arba paskirstyti krovinio išteklius. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta planuotojui, dirbančiam „lean“ gamybos įmonėje, kuri yra atsakinga už vertės srautą.


## <a name="copy-kanban-rule"></a>Kopijuokite „kanban“ taisyklę
1. Eikite į „Kanban“ taisyklės.
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite L0001 įvykio „Kanban“ taisyklę 000022.  
3. Spustelėkite „Kanban“ taisyklės kopijavimas.
4. Spustelėkite GERAI.

## <a name="change-kanban-rule"></a>Keisti „kanban“ taisyklę
1. Uždarykite puslapį.
2. Pasirinkite „Kanban“ užduoties planavimas.
3. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite eilutę su „Kanban“ 000177.  
4. Spustelėkite Naudoti alternatyvią „kanban“ taisyklę.
5. Spustelėkite Pirmyn.
6. Lauke „Kanban“ taisyklė įveskite arba pasirinkite reikšmę.
    * Pasirinkite anksčiau sukurtą „kanban“ taisyklę. Tai yra „kanban“ taisyklė, kurios numeris didžiausias.  
7. Spustelėkite Baigti.
    * Dabar „kanban“ užduotis naudoja kitą „kanban“ taisyklę. Tai gali būti naudinga norint išlyginti krovinio darbo elementus.  

