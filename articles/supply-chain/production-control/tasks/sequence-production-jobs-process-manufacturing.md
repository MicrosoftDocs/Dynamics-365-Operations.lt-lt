---
title: Gamybos užduočių sekos nustatymas gamybai
description: Šioje procedūroje kaip pavyzdys naudojami dažų produktai, kad būtų galima parodyti, kaip suplanuotų užsakymų seką nustatyti pagal spalvos ir pakuotės dydžio prioritetą.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e7cf6adc5c72494d6a9a72765a3d165424c72b2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835837"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Gamybos užduočių sekos nustatymas gamybai

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje kaip pavyzdys naudojami dažų produktai, kad būtų galima parodyti, kaip suplanuotų užsakymų seką nustatyti pagal spalvos ir pakuotės dydžio prioritetą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USPI. Ši procedūra yra skirta gamybos planuotojui.


## <a name="run-master-planning-for-uspi"></a>USPI bendrojo planavimo vykdymas
1. Pasirinkite Bendrasis planavimas > Bendrasis planavimas > Vykdyti > Bendrasis planavimas.
2. Lauke „Bendrasis planas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite MasterPlan.  
4. Spustelėkite GERAI.
    * Taip pradedamas bendrasis planavimas, įskaitant sekos procesą. Šis procesas gali užtrukti kelias minutes.  

## <a name="view-planned-orders-for-the-paint-products"></a>Suplanuotų dažų produktų užsakymų peržiūra
1. Pasirinkite Bendrasis planavimas > Bendrasis planavimas > Suplanuoti užsakymai.
2. Išplėskite „FactBox‟ dalį Prekės informacija.
3. Išplėskite „FactBox‟ dalį Grafiko informacija.
4. Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite MasterPlan.  
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Prekės numeris pagal reikšmę P300.
    * Atrakinkite, norėdami slinkti į dešinę, kad matytumėte užsakymo datą ir pristatymo datą. Atkreipkite dėmesį, kad šių elementų užsakymo data yra Šiandien ir suplanuotų užsakymų pristatymo datų seka nenustatyta pagal spalvos ir pakuotės dydžio prioritetą, kaip parodyta produkto pavadinime. Galite pelės žymeklį palaikyti virš prekės numerio ir matyti produkto pavadinimą bei prioritetą.  

## <a name="sequence-planned-orders-for-paint"></a>Suplanuotų dažų užsakymų sekos nustatymas
1. Uždarykite puslapį.
2. Pasirinkite Bendrasis planavimas > Bendrasis planavimas > Sekos suplanuoti užsakymai.
3. Išplėskite „FactBox‟ dalį Prekės informacija.
4. Išplėskite „FactBox‟ dalį Grafiko informacija.
    * Pastaba. Čia matote, kad suplanuotų užsakymų Pradžios datos / laikos seka nustatyta pagal spalvą ir pakuotės dydį 28 dienų įkainojimo laikotarpiu. Šiuos laikotarpius apibrėžia lauko Kampanija skaičius. Sekos suplanuoto užsakymo forma veikia kaip įprasta suplanuoto užsakymo forma, ir joje gamybos planuotojas gali tvirtinti suplanuotus užsakymus.  
5. Pažymėkite visas eilutes.
6. Spustelėkite Priimti.
    * Taip suplanuoti užsakymai bus atnaujinti pasirinktu sekos veiksmu – Atidėti arba Perkelti į priekį.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Suplanuotų užsakymų sekos tikrinimas
1. Uždarykite puslapį.
2. Pasirinkite Bendrasis planavimas > Bendrasis planavimas > Suplanuoti užsakymai.
3. Išplėskite „FactBox‟ dalį Prekės informacija.
4. Išplėskite „FactBox‟ dalį Grafiko informacija.
5. Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite MasterPlan.  
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Prekės numeris pagal reikšmę P300.
    * Atkreipkite dėmesį, kad užsakymų seka dabar nustatoma pagal spalvos ir dydžio prioritetą, o suplanuoti užsakymai pradedami anksčiausią užsakymo datą ir pristatymo datą. Stulpelį Užsakymo data arba pradžios datą galite patikrinti „FactBox‟ dalyje Grafiko informacija.  

