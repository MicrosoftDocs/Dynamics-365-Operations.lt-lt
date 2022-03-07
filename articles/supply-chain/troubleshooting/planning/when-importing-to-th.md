---
title: Jūs esate paraginamas įrašyti prekės padengimo parametrus, net jei neatlikote jokių pakeitimų
description: Jūs esate paraginamas įrašyti prekės padengimo parametrus, net jei neatlikote jokių pakeitimų.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 29ee23164430f219ff3d0c94216a8be43f480ce309f6cdac3dac6ed5b6d030af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730087"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a>Jūs esate paraginamas įrašyti prekės padengimo parametrus, net jei neatlikote jokių pakeitimų

KB numeris: 4615588

## <a name="symptoms"></a>Požymiai

Kai kuriais scenarijais galite gauti toliau pateiktą pranešimą, kai atidarote **Prekės padengimo** puslapį po prekių importavimo per *Prekės padengimo V2* objektą:

> Ar prieš uždarant įrašyti konfigūracijos keitimus?

Jūs gaunate šį pranešimą, nors neatlikote jokių pakeitimų.

## <a name="resolution"></a>Sprendimas

**Prekių padengimo** puslapyje įtraukta sudėtinga numatytoji logika, kuri gali sąlygoti pranešimo rodymą po to, kai atliksite tiesioginius pakeitimus duomenų bazėje, pavyzdžiui, importuodami objektą. Pavyzdžiui, objekto „`AREGENERALSETTINGSOVERRIDDEN`” laukas nustatytas į *Ne*, tačiau importuojate failą, pateikiantį naujas arba modifikuotas laukų reikšmes, tokias kaip „`PRODUCTCOVERAGEGROUPID`” ir (arba) „`VENDORACCOUNTNUMBER`”. Šiuo atveju, kadangi laukas „`AREGENERALSETTINGSOVERRIDDEN`” nustatytas į *Ne*, reikšmės yra automatiškai išvalomos iš laukų, kai pirmą kartą atidarote **Prekių padengimo** puslapį po importavimo. Jeigu įrašote pakeitimus kaip pranešimų langelio raginimus, jie yra saugomi duomenų bazėje. Kitu atveju, gausite tą patį pranešimą, kai atidarysite puslapį kitą kartą.

Norėdami išvengti tokio veikimo būdo, bet įtraukti ir tokių laukų, kaip „`PRODUCTCOVERAGEGROUPID`” reikšmes per objekto importavimą, nustatykite „`AREGENERALSETTINGSOVERRIDDEN`” į *Taip*, kai importuojate.
