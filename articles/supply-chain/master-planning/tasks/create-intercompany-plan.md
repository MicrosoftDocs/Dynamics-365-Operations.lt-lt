---
title: Kurti vidinės įmonės planą
description: Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 194bb78eed5a673030f7cead031cf286cddbe77c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845214"
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

