---
title: "Sulaikymo užsakymai"
description: "Šiame straipsnyje aprašoma, kaip, naudojant sulaikymo užsakymus, galima blokuoti atsargas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 394276e6908f2c1f6bc72eea061facc3afe701e9
ms.lasthandoff: 03/31/2017


---

# <a name="quarantine-orders"></a>Sulaikymo užsakymai

Šiame straipsnyje aprašoma, kaip, naudojant sulaikymo užsakymus, galima blokuoti atsargas. 

Naudojant sulaikymo užsakymus galima blokuoti atsargas. Pavyzdžiui, galbūt norėsite sulaikytų prekių kokybės kontrolės sumetimais. Atsargų, kad sulaikytas perkeliamas į sulaikymo sandėlį. **Pastaba.** Jei naudojate patobulinto sandėlio valdymo procesus (modulyje Sandėlio valdymas), sulaikymo užsakymų apdorojimo funkcija naudojama tik su grąžinimo pardavimo užsakymais.

## <a name="quarantine-onhand-inventory-items"></a>Karantino turimų atsargų inventorių
Kai sulaikote prekes, galite sulaikymo užsakymus kurti patys arba nustatyti sistemą, kad ji automatiškai kurtų sulaikymo užsakymus vykdant gavimo apdorojimą. Norėdami sulaikymo užsakymus kurti automatiškai, puslapio **Prekių modelių grupės** skirtuke **Atsargų strategijos** pasirinkite parinktį **Sulaikymo valdymas**. Taip pat gavimo sandėlių lauke **Sulaikymo sandėlis** reikia nurodyti numatytąjį sulaikymo sandėlį. Kai faktiškai turimos atsargos įrašomos pirkimo užsakyme arba gamybos užsakyme, programoje „Microsoft Dynamics 365 for Operations‟ sulaikytos prekės automatiškai perkeliamos į sulaikymo sandėlį. Perkeliama, nes sulaikymo užsakymo būsena pakeičiama į **Pradėtas**. Kai patys kuriate sulaikymo užsakymus, nėra būtina nustatyti dabartinės prekės sulaikymo valdymo susietoje prekių modelių grupėje. Norėdami vykdyti šį procesą, turite nurodyti sulaikytinas turimas atsargas ir naudotiną sulaikymo sandėlį. Planuoti šį procesą jums padės sulaikymo užsakymų būsenos.

## <a name="quarantine-order-statuses"></a>Sulaikymo užsakymų būsenos
Sulaikymo užsakymų būsenos gali būti tokios:

-   Sukurta
-   Pradėta
-   Paskelbta baigtu
-   Baigta

### <a name="created"></a>Sukurta

Kai sulaikymo užsakymas sukurtas neautomatiniu būdu, bet prekė dar neperkelta į sulaikymo sandėlį, sulaikymo užsakymo būsena yra **Sukurtas**. Sugeneruojamos dvi atsargų operacijos. Viena operacija – tai išdavimo operacija, kurios būsena gali būti **Užsakyta**, **Rezervuota faktiškai** arba **Paimta**. Kita operacija – tai gavimo operacija, kurios būsena sulaikymo sandėlyje gali būti **Užsakyta** arba **Užregistruota**. Galite rezervuoti, pasirinkti ir registruoti atsargų naujinimus naudodami įprastus procesus.

### <a name="started"></a>Pradėta

Kai sulaikymo užsakymo būsena yra **Pradėtas**, atsargos perkeliamos iš įprasto sandėlio į sulaikymo sandėlį ir sugeneruojamos dvi atsargų operacijos. Vienos operacijos būsena yra **Išskaičiuota**, o kitos operacijos būsena yra **Gauta**. Tuo pat metu sukuriamos dvi atsargų operacijos, tvarkančios grįžtamąjį perkėlimą. Šių operacijų datos nenurodytos. Vienos operacijos būsena yra **Rezervuota faktiškai**, o kitos operacijos būsena yra **Užsakyta**.

### <a name="reported-as-finished"></a>Paskelbta baigtu

Spustelėdami **Paskelbti baigtu**, galite paskelbti, kad pradėtas sulaikymo užsakymas baigtas. Prekė nebėra sulaikoma, tačiau dar nėra perkeliama atgal į įprastą sandėlį. Perkėlimą atgal į įprastą sandėlį galima apdoroti naudojant žurnalą Prekių gavimas, kurį galima inicijuoti proceso Skelbti baigtu metu.

### <a name="ended"></a>Baigta

Pasibaigus sulaikymo užsakymui, prekė iš sulaikymo sandėlio perkeliama atgal į įprastą sandėlį. Prekės operacijos būsena sulaikymo sandėlyje nustatoma kaip **Parduota**, o įprastame sandėlyje – kaip **Nupirkta**.

## <a name="quarantine-order-scrap"></a>Sulaikymo užsakymo nurašytas kiekis
Sulaikymo užsakymo proceso metu galite nurašyti atsargas. Apdorojant nurašymą atsargų būsena bus nustatyta į **Parduotos** iš sulaikymo sandėlio naudojant išdavimo operaciją.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Inventory blocking](inventory-blocking.md)


