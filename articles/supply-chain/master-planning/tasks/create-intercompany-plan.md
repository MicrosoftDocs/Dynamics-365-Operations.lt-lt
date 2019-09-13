---
title: Kurti vidinės įmonės planą
description: Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.
author: ShylaThompson
manager: AnnBe
ms.date: 08/13/2019
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
ms.openlocfilehash: f7fe8d155b39190f6c0ee1ee310a5edd2400623c
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916719"
---
# <a name="create-an-intercompany-plan"></a>Kurti vidinės įmonės planą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="set-up-an-intercompany-planning-group"></a>Vidinės įmonės planavimo grupės nustatymas 
1. **Naršymo sritis** eikite į **Moduliai > Pagrindinis planavimas > Sąranka > Vidinės įmonės planavimo grupės**. 
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką „Pavadinimas“ reikšme „10“.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Spustelėkite **Naikinti**. Šis veiksmas yra būtinas, norint sutrumpinti vidinės įmonės planavimą.   Vidinės įmonės planavimo procesas vykdys bendrąjį planavimą visose planavimo grupės įmonėse, pradedant nuo žemiausio planavimo sekos.  
5. Spustelėkite **Taip**.
6. Uždarykite puslapį.

## <a name="create-an-intercompany-plan"></a>Vidinės įmonės plano kūrimas
1. **Naršymo sritis** eikite į **Moduliai > Pagrindinis planavimas > Darbo sritys > Pagrindinis planavimas**.
2. Spustelėkite **Vidinės įmonės pagrindinis planavimas**.  
3. Lauke **Vidinės įmonės planavimo grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje. Pasirinkite 10 vidinės įmonės planavimo grupę.  
5. Lauke **Vidinės įmonės planavimo derinių skaičius** įveskite „2“. 10 vidinės įmonės planavimo grupėje yra du nariai. Norėdami atidėjimus perduoti iš šaltinio įmonės (USMF) į kliento įmonę (DEMF), turėsite vykdyti vidinės įmonę abiejose įmonėse du kartus. Vykdant pirmąjį kartojimą bus perduotas poreikis ir nustatyti atidėjimai šaltinio įmonėje (USMF). Vykdant antrąjį kartojimą atidėjimai bus perduoti iš USMF į DEMF.  
6. Lauke **Pirmas derinys** pažymėkite Regeneravimas.
7. Lauke **Kiti deriniai** pažymėkite Regeneravimas.
8. Lauke **Gijų skaičius** įveskite skaičių. Tai nurodo lygiagrečių gijų, naudojamų planuojant, skaičių.  
9. Spustelėkite **Gerai**.

## <a name="view-the-result-of-the-plan"></a>Plano rezultatų peržiūra
1. Lauke **Planas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje. Spustelėkite StaticPlan saitą. Turite būti įmonėje USMF.  
3. Spustelėkite **Suplanuoti užsakymai**.

