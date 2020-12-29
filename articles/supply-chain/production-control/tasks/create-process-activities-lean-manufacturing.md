---
title: Kurti „lean manufacturing“ proceso veiklas
description: Sukurkite „lean manufacturing“ proceso veiklą.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cb096eb25fa449b521c370bcb1677e38e399658
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433310"
---
# <a name="create-process-activities-for-lean-manufacturing"></a>Kurti „lean manufacturing“ proceso veiklas

[!include [banner](../../includes/banner.md)]

Sukurkite „lean manufacturing“ proceso veiklą. 

Išankstiniai reikalavimai: 

1. Turi būti sukurta gamybos eiga ir neaktyvi versija.

2. Turi būti sukurtas darbo elementas.


## <a name="find-the-production-flow-version"></a>Kaip rasti gamybos eigos versiją
1. Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="create-a-new-activity"></a>Naujos veiklos kūrimas
1. Spustelėkite Veiklos.
    * Užtikrinkite, kad pasirinkta gamybos eiga turi juodraščio versiją ir pasirinkite tą versiją.  
2. Spustelėkite Kurti naują plano veiklą.
3. Spustelėkite Pirmyn.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Pavadinimas surinkite reikšmę.
    * Atkreipkite dėmesį, kad pavadinimas turi būti unikalus visų versijų duotai gamybos eigai.  
6. Lauke Proceso kiekis įveskite skaičių.
    * Nepamirškite, kad nepriklausomai nuo to, koks užduoties kiekis bus apdorojamas, tai mažiausias darbo kiekis darbo išlaidoms apskaičiuoti. Jei darbo kiekis skiriasi nuo šio kiekio, bus sukurtas darbo išlaidų nuokrypis.  
7. Spustelėkite Pirmyn.

## <a name="select-the-work-cell"></a>Kaip pasirinkti darbo elementą
1. Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="define-the-inventory-updates"></a>Atsargų atnaujinimų nurodymas
1. Pažymėkite arba išvalykite žymės langelį Atnaujinti gautas turimas atsargas.
    * Jei atliekamas veiksmas Atnaujinti turimas atsargas = Ne, galite nurodyti veiklą ir gauti pusiau baigtą produktą (veikla nepatenka į kitą KS lygį).    Taip pat galite pasirinkti naudoti pusiau baigtus produktus.  

## <a name="define-the-picking-activities"></a>Išrinkimo veiklų nurodymas
1. Spustelėkite Pirmyn.
2. Sąraše pažymėkite pasirinktą eilutę.
    * Sukuriama pasirinkto darbo elemento įvesties vietos numatytoji išrinkimo veikla.  
3. Spustelėkite Pridėti.
    * Galite sukurti papildomų išrinkimo veiklų, skirtų konkretiems darbo elemento įvesties veikloje nesuskirstytiems produktams.  
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Lauke Prekės numeris surinkite reikšmę.
6. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Šiuo apibrėžimu visos veikloje suvartotos medžiagos, išskyrus antrojoje išrinkimo veikloje nurodytą prekę, paimamos iš numatytojo įvesties sandėlio ir vietos. Ši prekė bus paimta iš kito sandėlio ir kitos vietos.  
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Pažymėkite arba išvalykite žymės langelį Registruoti nurašymus.
10. Spustelėkite Pirmyn.

## <a name="define-the-activity-times"></a>Veiklos laikų nurodymas
1. Sąraše raskite ir pasirinkite norimą įrašą.
    * Būtinas dalies Apdorojimo laikas apibrėžimas. Apdorojimo laikas naudojamas skaičiuojant išlaidas ir „kanban“ užduočių našumo laikus. Apdorojimo laikai nenaudojami skaičiuojant pajėgumą ir suvartojimą, nes tai apskaičiuojama pagal iš gamybos eigos versijos užduoties gautą ciklo laiką.  
2. Lauke Laikas įveskite skaičių.
3. Lauke „Vienetas“ įveskite reikšmę.
4. Pasirinkite Laiko vienetas.
5. Lauke Už kiekį įveskite skaičių.
6. Sąraše raskite ir pasirinkite norimą įrašą.
    * Laukimo eilėje laikai nebūtini.  
7. Lauke Laikas įveskite skaičių.
8. Lauke „Vienetas“ įveskite reikšmę.
9. Pasirinkite Laiko vienetas.
10. Lauke Už kiekį įveskite skaičių.
11. Spustelėkite Pirmyn.
12. Spustelėkite Baigti.
13. Uždarykite puslapį.

