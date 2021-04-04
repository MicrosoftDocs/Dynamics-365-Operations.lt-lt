---
title: Sunaudojimo principai
description: Šioje temoje aprašomi keturi žaliavų sunaudojimo principai.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4336dcf5b17da8fd89f5f8246f2956a2ba15fe87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246242"
---
# <a name="flushing-principles"></a>Sunaudojimo principai

[!include [banner](../includes/banner.md)]

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]