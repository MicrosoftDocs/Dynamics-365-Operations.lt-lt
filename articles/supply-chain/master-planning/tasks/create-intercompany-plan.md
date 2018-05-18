--- 
title: "Kurti vidinės įmonės planą"
description: "Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-intercompany-plan"></a>Kurti vidinės įmonės planą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Vidinės įmonės planavimo grupės nustatymas 
1. Pasirinkite Vidinės įmonės planavimo grupės.
    * Bendrasis planavimas > Sąranka > Vidinės įmonės planavimo grupės  
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką „Pavadinimas“ reikšme „10“.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Spustelėkite Naikinti.
    * Šis veiksmas yra būtinas, norint sutrumpinti vidinės įmonės planavimą.   Vidinės įmonės planavimo procesas vykdys bendrąjį planavimą visose planavimo grupės įmonėse, pradedant nuo žemiausio planavimo sekos.  
5. Spustelėkite Taip.
6. Uždarykite puslapį.

## <a name="create-an-intercompany-plan"></a>Kurti vidinės įmonės planą
1. Spustelėkite Vidinės įmonės bendrasis planavimas.
    * Tai pateikiama darbo srityje Bendrasis planavimas.  
2. Lauke Vidinės įmonės planavimo grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite 10 vidinės įmonės planavimo grupę.  
4. Lauke Vidinės įmonės planavimo pakartojimų skaičius įveskite skaičių 2.
    * 10 vidinės įmonės planavimo grupėje yra du nariai. Norėdami atidėjimus perduoti iš šaltinio įmonės (USMF) į kliento įmonę (DEMF), turėsite vykdyti vidinės įmonę abiejose įmonėse du kartus. Vykdant pirmąjį kartojimą bus perduotas poreikis ir nustatyti atidėjimai šaltinio įmonėje (USMF). Vykdant antrąjį kartojimą atidėjimai bus perduoti iš USMF į DEMF.  
5. Lauke Pirmasis kartojimas pasirinkite parinktį.
6. Lauke Pirmasis kartojimas pasirinkite Regeneravimas.
7. Lauke Paskesni pakartojimai pasirinkite Regeneravimas.
8. Lauke Gijų skaičius įveskite skaičių.
    * Tai nurodo lygiagrečių gijų, naudojamų planuojant, skaičių.  
9. Spustelėkite GERAI.

## <a name="view-the-result-of-the-plan"></a>Plano rezultatų peržiūra
1. Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Spustelėkite StaticPlan saitą. Turite būti įmonėje USMF.  
3. Spustelėkite Suplanuoti užsakymai.


