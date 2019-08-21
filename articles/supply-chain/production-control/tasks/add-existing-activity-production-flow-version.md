---
title: Esamos veiklos įtraukimas į gamybos eigos versiją
description: Kurdami naujas gamybos eigų versijas, į naują versiją galite įtraukti senesnių versijų sukurtas veiklas.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 315a82ce3502164fcf7813e866fb3dc1806d03d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843966"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a>Esamos veiklos įtraukimas į gamybos eigos versiją

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kurdami naujas gamybos eigų versijas, į naują versiją galite įtraukti senesnių versijų sukurtas veiklas. Šioje procedūroje parodoma, kaip kurti naują esamos gamybos eigos versiją nekopijuojant veiklų. Atliekant kitą veiksmą, esama veikla yra įtraukiama į naują versiją. 

Jei norite atlikti šią užduotį, turite sukurti gamybos eigos versiją ir veiklas.


## <a name="create-a-new-production-flow-version"></a>Kurti naują gamybos eigos versiją
1. Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Spustelėkite Redaguoti.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Lauke Galiojimo data įveskite datą ir laiką.
    * Atkreipkite dėmesį, kad prieš kurdami naują gamybos eigos versiją, turite patikrinti aktyvios versijos galiojimo pabaigos datą ir laiką. Nauja versija bus sukurta su įsigaliojimo pradžios data, kuri sutampa su pasirinktos versijos galiojimo pabaigos data.  
7. Spustelėkite Pridėti.
8. Lauke Kopijuoti iš versijos pasirinkite Ne.
    * Pasirinkite Ne, kai norite pradėti naudodami tuščią versiją, t. y., jei dauguma nukopijuotos versijos veiklos turi būti pakeistos naujomis veiklomis.. Neautomatiniu būdu įtraukite nepakitusias veiklas į veiklos formos funkciją Įtraukti esamą.  
9. Lauke Dubliuoti „kanban“ taisykles pasirinkite Ne.
    * Kai veiklos į naują versiją nekopijuojamos, naujos versijos kūrimo metu neįmanoma kopijuoti „kanban“ taisyklių.   Todėl vėliau reikia naudoti pakeitimo „kanban“ kūrimo funkciją „kanban“ taisyklės formoje, kad senos gamybos eigos versijos „kanban“ taisyklės būtų pakeistos naujos versijos veiklų „kanban“ taisyklėmis.  
10. Spustelėkite GERAI.
11. Sąraše raskite ir pasirinkite norimą įrašą.

## <a name="add-an-existing-activity"></a>Esamos veiklos įtraukimas
1. Spustelėkite Veiklos.
2. Spustelėdami Įtraukti esamą atidarykite išplečiamąjį dialogo langą.
    * Raskite ir pasirinkite esamą veiklą, kurią norite įtraukti į naują gamybos eigos versiją.  Atkreipkite dėmesį, kad sąraše rodomos šios gamybos eigos visų ankstesnių versijų sukurtos veiklos.  
3. Lauke Veikla įveskite arba pasirinkite reikšmę.
4. Spustelėkite GERAI.

