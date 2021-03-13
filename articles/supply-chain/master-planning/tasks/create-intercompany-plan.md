---
title: Kurti vidinės įmonės planą
description: Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c368e461860a41d0110f5aed79c2aac49c437d68
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011418"
---
# <a name="create-an-intercompany-plan"></a>Kurti vidinės įmonės planą

[!include [banner](../../includes/banner.md)]

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

