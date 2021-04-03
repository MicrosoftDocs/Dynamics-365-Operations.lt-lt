---
title: Kurti „lean manufacturing“ perdavimo veiklas
description: Sukurkite „lean manufacturing“ perkėlimo veiklą.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e3c92c5fc9cdba7c77942fae5c32d625cc939f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237923"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Kurti „lean manufacturing“ perdavimo veiklas

[!include [banner](../../includes/banner.md)]

Sukurkite „lean manufacturing“ perkėlimo veiklą. 

Išankstiniai reikalavimai: 

1. Turi būti sukurta gamybos eiga ir neaktyvi versija.

2. Turi būti sukurti iš ir į sandėliai ir vietos. Pasirinktinai turėtų būti sukurtas papildantis arba papildytas darbo elementas.


## <a name="find-the-production-flow-version"></a>Kaip rasti gamybos eigos versiją
1. Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Nepamirškite, kad gamybos eiga turi turėti juodraščio būsenos versiją.  
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="create-a-new-activity"></a>Naujos veiklos kūrimas
1. Spustelėkite Veiklos.
    * Užtikrinkite, kad pasirinkta gamybos eiga turi juodraščio versiją ir pasirinkite tą versiją.  
2. Spustelėkite Kurti naują plano veiklą.
3. Spustelėkite Pirmyn.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Veiklos tipas pasirinkite „Perkėlimas“.
6. Lauke Proceso kiekis įveskite skaičių.
7. Spustelėkite Pirmyn.

## <a name="select-the-work-cells"></a>Darbo elementų pasirinkimas
1. Lauke Papildymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Norėdami darbo elemento išeigos vietą perkėlimo veikloje naudoti kaip vietą iš, pasirinkite darbo elementą. Tą patį galima atlikti naudojant papildytą darbo elementą, kuris nustato perkėlimo veiklos paskirties vietą.  
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="define-the-inventory-updates"></a>Atsargų atnaujinimų nurodymas
1. Lauke Produkto tipas pasirinkite pasirinktį.
    * Atkreipkite dėmesį, kad perkėlimas nepakeičia produkto tipo. Galite perkelti baigtus arba pusiau baigtus produktus (perkėlimas tarp dviejų gamybos eigos veiklų ir galbūt „kanban“ srauto).     Perkeldami baigtus produktus galite pasirinkti, ar paimant arba gaunant pradedama atsargų operacija.  

## <a name="define-the-transfer-locations"></a>Perkėlimo vietų nurodymas
1. Spustelėkite Pirmyn.
2. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Lauke Transportuoja pasirinkite „Siuntėjas“.
    * Galimos pasirinktys: Siuntėjas – siuntimo sandėlį valdanti organizacija, Gavėjas – gavimo sandėlį valdanti organizacija, Vežėjas – trečiosios šalies tiekėjas. Jei valdanti organizacija yra tiekėjas, norint atlikti perkėlimo veiklą reikalinga subrangos sutartis.  
8. Spustelėkite Pirmyn.

## <a name="define-the-activity-times"></a>Veiklos laikų nurodymas
1. Sąraše raskite ir pasirinkite norimą įrašą.
    * Būtinas dalies Apdorojimo laikas apibrėžimas. Apdorojimo laikas naudojamas skaičiuojant savikainą ir „kanban“ užduočių našumo laikus. Apdorojimo laikai nenaudojami skaičiuojant pajėgumą ir suvartojimą, kurie apskaičiuojami pagal iš gamybos eigos versijos užduoties gautą ciklo laiką.  
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]