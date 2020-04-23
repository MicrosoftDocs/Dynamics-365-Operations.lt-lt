---
title: Kurti kelių veiklos rūšių „kanban“ taisykles
description: Šioje procedūroje parodoma, kaip kurti „kanban“ taisyklę, kuri apima kelias gamybos eigos veiklas.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68cac0f581e786cdb3801e03fb60db7bc05ffb2f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212229"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Kurti kelių veiklos rūšių „kanban“ taisykles

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti „kanban“ taisyklę, kuri apima kelias gamybos eigos veiklas. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši užduotis skirta proceso inžinieriui arba vertės srauto vadovui, nes jie parengia naujos arba pakeistos prekės gamybą „lean“ aplinkoje.


## <a name="create-a-new-kanban-rule"></a>Kurti naują „kanban“ taisyklę
1. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
2. Spustelėkite Naujas.
3. Lauke Papildymo strategija pasirinkite Suplanuota.
4. Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.
    * Pasirinkite SpeakerAssemblyAndPolish.  
5. Pasirinkite žymės langelį Kelios veiklos.
    * Tikslas yra į „kanban“ taisyklę įtraukti daugiau nei vieną veiklą. Gamybos eigos kelias pasirenkamas, kai pasirenkama paskutiniojo plano veikla.  
6. Lauke Paskutinioji plano veikla įveskite arba pasirinkite reikšmę.
    * Pasirinkite SpeakerTestAndPackaging. Pasirinkus reikšmę automatiškai atidaromas puslapis. Pasirinkite „kanban“ srauto SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Spustelėkite GERAI.  
7. Išplėskite skyrių Išsami informacija.
8. Lauke Produktas įveskite arba pasirinkite reikšmę.
    * Pasirinkite prekę L0006.  

## <a name="create-kanban-and-view-jobs"></a>Kurti „kanban“ ir peržiūrėti užduotis
1. Išplėskite skyrių „Kanbans“.
2. Spustelėkite Pridėti.
3. Lauke Naujų „kanban“ skaičius įveskite 1.
    * Taip sukursite vieną „kanban“.  
4. Nustatykite produkto kiekio reikšmę „3“.
    * „Kanban“ apdoros 3 produktus.  
5. Lauke Termino data / laikas įveskite datą ir laiką.
    * Galite įvesti Šiandien.  
6. Spustelėkite Kurti.
7. Spustelėkite Informacija.
    * Atkreipkite dėmesį, kad „kanban“ priskirtos dvi gamybos eigos proceso užduotys. Pirmoji yra SpeakerAssemblyAndPolish, o antroji – SpeakerTestAndPackaging.  
    * Tai paskutinis veiksmas!  

