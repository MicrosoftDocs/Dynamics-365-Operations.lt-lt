---
title: Keisti apdorojimo užduoties „kanban“ taisykles
description: Ši procedūra padės pakeisti naudojamą „kanban“ taisyklę į nurodytą „kanban“.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e0e1989bcc4ca02d097f9ebff40f21158f26546
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981361"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Keisti apdorojimo užduoties „kanban“ taisykles

[!include [banner](../../includes/banner.md)]

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

