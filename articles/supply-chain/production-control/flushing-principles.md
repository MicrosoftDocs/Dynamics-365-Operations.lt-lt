---
title: Sunaudojimo principai
description: "Šioje temoje aprašomi keturi žaliavų sunaudojimo principai."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 54d438de096b0ff317d94a03d8ae572e6350a865
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="controlling-raw-material-consumption-by-using-flushing-principles"></a>Žaliavų suvartojimo kontrolė taikant sunaudojimo principus

[!include[banner](../includes/banner.md)]

Sunaudojimo principai atspindi skirtingas gamybos procesuose naudojamų žaliavų suvartojimo strategijas. Gamyba yra procesas, kurio metu medžiagos paimamos iš turimų atsargų ir gamybos užsakymuose bei paketiniuose užsakymuose nustatoma vartojamų medžiagų būsenos reikšmė **Nebaigta gamyba** (NG). Vartojamos žaliavos paprastai paimamos iš sukonfigūruotos proceso, naudojančio medžiagas, vietos. Ši vieta vadinama gamybos įvesties vieta.

Prieš medžiagas vartojant jos yra perkeliamos į įvesties vietą. Procesas parodytas tolesniame paveikslėlyje.

[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)

1. Medžiagų sandėlis
2. Žaliavų paėmimas
3. Gamybos įvesties vieta
4. Žaliavų suvartojimas
5. Gamybos procesas

Medžiagų suvartojimas valdomas naudojant keturis toliau pateiktus sunaudojimo principus.

- Neautomatinis
- Pradžios
- Baigti
- Yra vietoje

Sunaudojimo principai konfigūruojami pagal numatytųjų reikšmių hierarchiją. Hierarchija prasideda patvirtintu produktu, kur sunaudojimo principo reikšmė yra **Pradžia**. Komplektavimo specifikacijos (KS) arba formulės eilutėje produkto sunaudojimo principą galima perrašyti. Numatytasis sunaudojimo principas, pateiktas gamybos KS eilutėse arba paketinio užsakymo formulės eilutėse, paimamas iš produkto ar perrašytos reikšmės KS arba formulėse.

## <a name="description-of-the-flushing-principles"></a>Sunaudojimo principų aprašymas

### <a name="manual"></a>Neautomatinis
Sunaudojimo principas Neautomatinis nurodo, kad medžiagų suvartojimo registravimas yra neautomatinė operacija. Šis principas yra aktualus, jei, pavyzdžiui, norite, kad būtų galima sekti laiką, o vartojamų paketų numerių arba serijos numerių kiekį reikia registruoti sekimo tikslais. Neautomatinis suvartojimas registruojamas gamybos išrinkimo dokumentų žurnale. Jei įjungta prekių patobulintų sandėlio procesų funkcija, galima taikyti rankinį srautą.

### <a name="start"></a>Pradžios
Sunaudojimo principas Pradžia nurodo, kad medžiagos bus automatiškai suvartojamos pradėjus gamybos užsakymą. Suvartojamų medžiagų kiekis yra proporcingas pradžios kiekiui. Jei sunaudojimo principas Pradžia yra naudojamas kartu su gamybos vykdymo sistema, jį taip pat galima naudoti norint sunaudoti medžiagas, kai pradedama operacija arba vykdymo užduotis. Šis principas yra aktualus, jei, pavyzdžiui, suvartojimo nuokrypis yra žemas, medžiagos yra žemos vertės medžiagos, sekimo reikalavimų nėra arba operacijų apdorojimo laikas yra trumpas. 

### <a name="finish"></a>Baigti
Sunaudojimo principas Pabaiga nurodo, kad medžiagos bus automatiškai suvartojamos, kai gamybos užsakymas paskelbiamas baigtu arba kai operacija, nustatyta vartoti medžiagas, užregistruojama kaip baigta. Suvartojamų medžiagų kiekis yra proporcingas kiekiui, kuris paskelbtas baigtu. Jei sunaudojimo principas Pabaiga yra naudojamas kartu su gamybos vykdymo sistema, jį taip pat galima naudoti norint sunaudoti medžiagas, kai baigiama operacija arba vykdymo užduotis. Šis principas yra aktualus tokiomis pačiomis sąlygomis kaip principas Pradžia. Tačiau principas Pabaiga skirtas operacijoms, kurių apdorojimo laikas yra ilgesnis, kai medžiagos neturėtų būti nustatytos į parinktį NG, kol operacija nebaigta. 

### <a name="available-at-location"></a>Yra vietoje
Sunaudojimo principas Yra vietoje nurodo, kad medžiagos bus automatiškai suvartojamos, kai jos užregistruojamos kaip paimtos gamybai vykdyti. Medžiagos užregistruojamos kaip paimtos iš vietos, kai žaliavų paėmimo užduotis baigta arba kai medžiagų yra gamybos įvesties vietoje ir medžiagų eilutė išleidžiama į sandėlį. Proceso metu sugeneruojamas išrinkimo dokumentas užregistruojamas paketinėje užduotyje. Šis principas yra aktualus, jei, pavyzdžiui, vienam gamybos užsakymui priskirta daug išrinkimo veiklų. Tokiu atveju išrinkimo dokumento neautomatiškai naujinti nereikia ir galima matyti dabartinį NG balanso rodinį.

