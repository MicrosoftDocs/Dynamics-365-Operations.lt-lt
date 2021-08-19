---
title: Sudėtinių produktų medžiagų plano kūrimas
description: Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d829687521c002a84de8f88caff22a8f0362c75e91ac355fd0b5002d0bd981c2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768076"
---
# <a name="create-a-material-plan-for-co-products"></a>Sudėtinių produktų medžiagų plano kūrimas

[!include [banner](../../includes/banner.md)]

Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USP2.

## <a name="create-requirement-for-a-co-product"></a>Kurti sudėtinio produkto poreikį

1. Eikite **į pardavimo ir rinkodaros darbo sričių pardavimo užsakymo \> \> apdorojimą ir užklausą**.
1. Pasirinkite **Naujas**.
1. Pasirinkite **Pardavimo užsakymas**.
1. Lauke **Kliento sąskaita** surinkite reikšmę.
    * Pavyzdys: US-001  
1. Pasirinkite **Gerai**.
1. Lauke **Prekės numeris** įveskite vertę.
    * Pavyzdys: P6003  
1. Lauke **Kiekis** įveskite skaičių.
    * Pavyzdys: 50000  
1. Pasirinkite **Įrašyti**.

## <a name="create-a-material-plan-for-co-products"></a>Sudėtinių produktų medžiagų plano kūrimas

1. Uždarykite puslapį.
1. Uždarykite puslapį.
1. Pasirinkite **Bendrasis planavimas**.
1. Lauke **Planas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
    * Pavyzdys: MasterPlan  
1. Pasirinkite **Vykdyti**.
1. Išplėskite arba sutraukite dalį **įtrauktini įrašai**.
1. Pasirinkite **Filtras**.
1. Sąraše pasirinkite lauko eilutę **Laukelis** = *Elemento numeris*.
1. Lauke **Kriterijai** įveskite reikšmę.
    * Pavyzdys: P6003  
1. Pasirinkite **Gerai**.
1. Pasirinkite **Gerai**.
1. Pažymėkite **Suplanuoti užsakymai**.
1. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką **Prekės numeris** reikšme 'P6000'.
    * Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.  
1. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite vieną iš filtro pateiktų eilučių.  
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Išplėskite skyrių **Susiejimas**.
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
    * Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.  
1. Uždarykite puslapį.

## <a name="create-a-second-requirement-for-a-co-product"></a>Kurti antrą sudėtinio produkto poreikį

1. Eikite **į pardavimo ir rinkodaros darbo sričių pardavimo užsakymo \> \> apdorojimą ir užklausą**.
1. Pasirinkite **Naujas**.
1. Pasirinkite **Pardavimo užsakymas**.
1. Lauke **Kliento sąskaita** surinkite reikšmę.
    * Pavyzdys: US-001  
1. Pasirinkite **Gerai**.
1. Lauke **Prekės numeris** įveskite vertę.
    * Pavyzdys: P6003  
1. Lauke **Kiekis** įveskite skaičių.
    * Pavyzdys: 50000  
1. Pasirinkite **Įrašyti**.

## <a name="create-a-second-material-plan-for-co-products"></a>Sudėtinių antrų produktų medžiagų plano kūrimas

1. Lauke **Planas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
2. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
    * Pavyzdys: MasterPlan  
3. Pasirinkite **Vykdyti**.
4. Išplėskite arba sutraukite dalį **įtrauktini įrašai**.
5. Pasirinkite **Filtras**.
6. Sąraše pasirinkite lauko eilutę **Laukelis** = *Elemento numeris*.
7. Lauke *Kriterijai* įveskite reikšmę.
    * Pavyzdys: P6003  
8. Pasirinkite **Gerai**.
9. Pasirinkite **Gerai**.
10. Pažymėkite **Suplanuoti užsakymai**.
11. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką **Prekės numeris** reikšme 'P6000'.
    * Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.  
12. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite vieną iš filtro pateiktų eilučių.  
13. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
14. Išplėskite arba sutraukite skyrių **Susiejimas**.
15. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
    * Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.  
16. Uždarykite puslapį.
17. Pasirinkite **Bendrasis planavimas**.
18. Eikite į **Bendrasis planavimas \> Sąranka \> Bendrojo planavimo parametrai**.
19. Rinkitės *Ne* lauke **Išjungti visus planavimo procesus**.
20. Uždarykite puslapį.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]