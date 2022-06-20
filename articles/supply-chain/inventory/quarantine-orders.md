---
title: Sulaikymo užsakymai
description: Šiame straipsnyje aprašoma, kaip naudoti sulaikymo užsakymus atsargai blokuoti.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ee1ba338d90c6ee9cdc37948061f518040ae1a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869668"
---
# <a name="quarantine-orders"></a>Sulaikymo užsakymai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti sulaikymo užsakymus atsargai blokuoti.

Sulaikymo užsakymai leidžia užblokuoti atsargas. Pavyzdžiui, galbūt sulaikyti prekes norėsite kokybės kontrolės tikslais. Sulaikytos atsargos perkeliamos į sulaikymo sandėlį.

> [!NOTE]
> Pastaba. Jei naudojate patobulinto sandėlio valdymo procesus (modulyje Sandėlio valdymas), sulaikymo užsakymų apdorojimo funkcija naudojama tik su grąžinimo pardavimo užsakymais.

## <a name="quarantine-on-hand-inventory-items"></a>Turimų atsargų prekių sulaikymas

Kai sulaikote prekes, galite sulaikymo užsakymus kurti rankiniu būdu arba nustatyti sistemą, kad ji automatiškai kurtų sulaikymo užsakymus vykdant gavimo apdorojimą.

Norėdami nustatyti sistemą automatiškai generuoti sulaikymo užsakymus, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargos \> Prekių modelių grupės**.
1. Pasirinkite atitinkamą modelio grupę iš juostos arba sukurkite naują modelio grupę.
1. „FastTab” **Atsargų strategijos** pasirinkite **Karantino valdymo** žymės langelį.
1. Uždarykite puslapį.
1. Taip pat gavimo sandėlių lauke **Sulaikymo sandėlis** reikia nurodyti numatytą karantino sandėlį.

Kai prekė, užregistruota kaip gauta sandėlyje, priklauso modelių grupei, kurioje pažymėtas sulaikymo valdymo žymės langelis, sistema sugeneruoja jai **sulaikymo** užsakymą. Sulaikymo užsakymas nurodo darbuotojams perkelti prekę į sulaikymo sandėlį.

Kai rankiniu būdu kuriate karantino užsakymus **Karantino užsakymai** puslapyje, nėra būtina nustatyti dabartinės prekės sulaikymo valdymo susietoje prekių modelių grupėje. Norėdami vykdyti šį procesą, turite nurodyti sulaikytinas turimas atsargas ir naudotiną sulaikymo sandėlį. Planuoti šį procesą jums padės sulaikymo užsakymų būsenos.

## <a name="quarantine-order-statuses"></a>Sulaikymo užsakymų būsenos

Sulaikymo užsakymų būsenos gali būti tokios:

- Sukurta
- Pradėta
- Paskelbta baigtu
- Baigta

### <a name="created"></a>Sukurta

Kai sulaikymo užsakymas sukurtas neautomatiniu būdu, bet prekė dar neperkelta į sulaikymo sandėlį, sulaikymo užsakymo būsena yra **Sukurtas**. Sugeneruojamos dvi atsargų operacijos. Viena operacija – tai išdavimo operacija, kurios būsena gali būti **Užsakyta**, **Rezervuota faktiškai** arba **Paimta**. Kita operacija – tai gavimo operacija, kurios būsena sulaikymo sandėlyje gali būti **Užsakyta** arba **Užregistruota**. Galite rezervuoti, pasirinkti ir registruoti atsargų naujinimus naudodami įprastus procesus.

### <a name="started"></a>Pradėta

Kai sulaikymo užsakymo būsena yra **Pradėtas**, atsargos perkeliamos iš įprasto sandėlio į sulaikymo sandėlį ir sugeneruojamos dvi atsargų operacijos. Vienos operacijos būsena yra **Išskaičiuota**, o kitos operacijos būsena yra **Gauta**. Tuo pat metu sukuriamos dvi atsargų operacijos, tvarkančios grįžtamąjį perkėlimą. Šių operacijų datos nenurodytos. Vienos operacijos būsena yra **Rezervuota faktiškai**, o kitos operacijos būsena yra **Užsakyta**.

### <a name="reported-as-finished"></a>Paskelbta baigtu

Norėdami pradėti sulaikymo užsakymą pranešti baigtu, atidarykite užsakymą ir veiksmų srityje **pasirinkite** Pranešti apie baigtą. Prekė nebėra sulaikoma, tačiau dar nėra perkeliama atgal į įprastą sandėlį. Perkėlimą atgal į įprastą sandėlį galima apdoroti naudojant žurnalą Prekių gavimas, kurį galima inicijuoti proceso Skelbti baigtu metu.

### <a name="ended"></a>Baigta

Pasibaigus sulaikymo užsakymui, prekė iš sulaikymo sandėlio perkeliama atgal į įprastą sandėlį. Prekės operacijos būsena sulaikymo sandėlyje nustatoma kaip *Parduota*, o įprastame sandėlyje – kaip *Nupirkta*.

## <a name="quarantine-order-scrap"></a>Sulaikymo užsakymo nurašytas kiekis

Sulaikymo užsakymo proceso metu galite nurašyti atsargas. Apdorojant nurašymą atsargų būsena bus nustatyta į *Parduotos* iš sulaikymo sandėlio naudojant išdavimo operaciją.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Atsargų blokavimas](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
