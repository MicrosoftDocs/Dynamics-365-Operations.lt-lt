---
title: Būklės vertinimas
description: Šioje temoje paaiškinama, kaip modulyje Turto valdymas sukurti turto būklės vertinimo šabloną ir registraciją.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 774c788959c5ebea69b4d22c886ac673f50b97f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433702"
---
# <a name="condition-assessment"></a>Būklės vertinimas

[!include [banner](../../includes/banner.md)]

 

Šioje temoje aiškinama, kaip modulyje Turto valdymas sukurti turto būklės vertinimo šabloną ir registraciją. Būklės vertinimas atliekamas reguliariais intervalais, o pagrindinis tikslas – sukurti ir išlaikyti būklės duomenis apie turtą. Žvelgiant iš prevencinės priežiūros perspektyvos, svarbu stebėti svarbiausią informaciją, pvz., dabartinę būklę ir likusį eksploatavimo laikotarpį. Be to, jei būklės vertinimą atliksite reguliariais intervalais, galėsite stebėti ir lyginti savo gamyklos mašinų būklę.

Būklės vertinimas gali būti naudojamas daugumai įrangos būklių matuoti ir stebėti. Pavyzdys: galite matuoti mašinų vibracijas. Užregistravę įvairių tipų įrangos vibracijos matavimus modulyje Turto valdymas, galite ieškoti naujausio užregistruoto vertinimo ir peržiūrėti vibracijos matavimus.

Sukuriamas turto būklės vertinimas. Prieš atlikdami būklės vertinimo procedūrą turite nustatyti turto tipo būklės vertinimo šabloną. Būklės vertinimo šablonų naudojimo priežastis – išvengti būklės duomenų apie panašų turtą kitimo. Būklės vertinimo nustatymo ir naudojimo seka modulyje Turto valdymas: pirmiausia nustatykite reikiamus būklės vertinimo šablonus. Tada susiekite šablonus su turto tipais formoje **Turto tipai**. Galiausiai, formoje **Turtas** galite kurti turto būklės vertinimo registracijas.

## <a name="create-a-condition-assessment-template"></a>Būklės vertinimo šablono kūrimas

1. Pasirinkite **Turto valdymas** > **Sąranka** > **Turto tipai** > **Būklės vertinimas**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
3. Lauke **Šablonas** įveskite ir šablono ID.
4. Lauke **Pavadinimas** įveskite šablono pavadinimą.
5. „FastTab“ skirtuke **Būklės vertinimo eilutės** pridėkite eilutes, reikalingas būklės vertinimui, įskaitant tinkamo būklės tipo ir matavimo vieneto pasirinkimą.
6. „FastTab“ skirtuke **Turto tipai** pridėkite turto tipus, kurie turėtų naudoti būklės vertinimo šabloną.
7. Grupės **Išsami informacija**, esančios ekrano viršuje, laukuose **Eilutės** ir **Turto tipai** pamatysite vertinimo eilučių ir turto tipų, susijusių su pasirinktu būklės vertinimo šablonu, skaičių.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Turto būklės vertinimo registracijos kūrimas

1. Pasirinkite **Turto valdymas** > **Bendra** > **Turtas** > **Visas turtas**.
2. Sąraše pasirinkite turtą, kurio būklės vertinimo registraciją norite sukurti.
3. Skirtuke **Bendra** spustelėkite **Būklės vertinimas**.
4. Spustelėję **Nauja** sukurkite naują registraciją.
5. Lauke **Data** pasirinkite būklės vertinimo datą.
6. Lauke **Darbuotojas** pasirinkite darbuotojo, kuris atliko vertinimo registraciją, vardą ir pavardę.
7. Lauke **Eilutės** pamatysite vertinimo eilučių, nustatytų atliekant būklės vertinimą, skaičių.
8. Lauke **Šablonas** pasirinkite būklės vertinimo šabloną. Šablono pavadinimas automatiškai įterpiamas į lauką **Pavadinimas**, o susijusios registracijos eilutės – į „FastTab“ skirtuką **Būklės vertinimo eilutės**.
9. „FastTab“ skirtuke **Pastabos** galite įterpti pastabų, susijusių su pasirinktu būklės vertinimu.
10. Lauke **Reikšmė** prie kiekvienos būklės vertinimo eilutės įterpkite matavimo duomenis.
11. Lauke **Būklės vertinimo eilutės** „FastTab“ > **Komentarai** prie pasirinktos registracijos eilutės galite įterpti komentarą. Jei prie eilutės pridedate komentarą, automatiškai parenkamas žymės langelis **Komentaras**.

Atlikę turto būklės vertinimo registraciją, galite atsispausdinti būklės vertinimo ataskaitą.

>[!NOTE]
>Taip pat galite užregistruoti darbo užsakymo būklės vertinimą (mygtukas **Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai** > **Būklės vertinimas**).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]