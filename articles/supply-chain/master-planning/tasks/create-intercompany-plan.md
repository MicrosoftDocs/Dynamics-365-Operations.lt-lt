---
title: Kurti vidinės įmonės planą
description: Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą.
author: t-benebo
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2486ce6f03d03982a7ae9c43af447923aabfed2
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469567"
---
# <a name="create-an-intercompany-plan"></a>Kurti vidinės įmonės planą

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti vidinės įmonės planą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.

## <a name="set-up-an-intercompany-planning-group"></a>Vidinės įmonės planavimo grupės nustatymas

1. **Naršymo sritis** eikite į **Moduliai > Pagrindinis planavimas > Sąranka > Vidinės įmonės planavimo grupės**.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką „Pavadinimas“ reikšme „10“.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Pasirinkite **Naikinti**. Šis veiksmas yra būtinas, norint sutrumpinti vidinės įmonės planavimą.   Vidinės įmonės planavimo procesas vykdys bendrąjį planavimą visose planavimo grupės įmonėse, pradedant nuo žemiausio planavimo sekos.  
5. Pasirinkite **Taip**.
6. Uždarykite puslapį.

## <a name="create-an-intercompany-master-plan"></a>Vidinės įmonės bendrojo plano kūrimas

1. **Naršymo sritis** eikite į **Moduliai > Pagrindinis planavimas > Darbo sritys > Pagrindinis planavimas**.
2. Pasirinkite **Vidinės įmonės bendrasis planavimas**.  
3. Lauke **Vidinės įmonės planavimo grupė** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje. Pasirinkite 10 vidinės įmonės planavimo grupę.  
5. Lauke **Vidinės įmonės planavimo derinių skaičius** įveskite „2“. 10 vidinės įmonės planavimo grupėje yra du nariai. Norėdami atidėjimus perduoti iš šaltinio įmonės (USMF) į kliento įmonę (DEMF), turėsite vykdyti vidinės įmonę abiejose įmonėse du kartus. Vykdant pirmąjį kartojimą bus perduotas poreikis ir nustatyti atidėjimai šaltinio įmonėje (USMF). Vykdant antrąjį kartojimą atidėjimai bus perduoti iš USMF į DEMF.  
6. Lauke **Pirmas derinys** pažymėkite Regeneravimas.
7. Lauke **Kiti deriniai** pažymėkite Regeneravimas.
8. Lauke **Gijų skaičius** įveskite skaičių. Tai nurodo lygiagrečių gijų, naudojamų planuojant, skaičių.  
9. Pasirinkite **Gerai**.

## <a name="view-the-result-of-the-plan"></a>Plano rezultatų peržiūra

1. Lauke **Planas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
2. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje. Pasirinkite saitą Statiniam planui. Turite būti įmonėje USMF.  
3. Pažymėkite **Suplanuoti užsakymai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]