---
title: Nustatyti vežėjo degalų indeksus
description: Šis vadovas parodo, kaip sukurti degalų indekso regioną, degalų indeksą ir vežėjo degalų indeksą.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09dc948e673bb8be49ac81e5ad2b20bc6c62b286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233660"
---
# <a name="set-up-a-carrier-fuel-index"></a>Nustatyti vežėjo degalų indeksus

[!include [banner](../../includes/banner.md)]

Šis vadovas parodo, kaip sukurti degalų indekso regioną, degalų indeksą ir vežėjo degalų indeksą. Degalų indekso regionas nurodo, kuriam regionui turėtų būti taikomas degalų indeksas, o degalų indeksas tam tikro laikotarpio degalų kainą. Norėdami įvertinti degalų kainų pokyčius per tam tikrą laiką, galite susieti vežėją su keliais degalų indeksais.  Šias užduotis paprastai atlieka transportavimo koordinatorius. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba naudodami savo duomenis.


## <a name="create-a-fuel-index-region"></a>Kurti degalų indekso regioną
1. Pasirinkite Transportavimo valdymas > Nustatymas > Degalų indeksai > Degalų indekso regionai.
    * Pirmiausia turite sukurti skirtingus savo veiklos regionus ir apskaičiuoti skirtingus papildomus degalų mokesčius.  
2. Spustelėkite Naujas.
3. Lauke „Regionas“ įveskite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Spustelėkite Įrašyti.

## <a name="create-a-fuel-index"></a>Degalų indekso kūrimas
1. Pasirinkite Transportavimo valdymas > Nustatymas > Degalų indeksai > Degalų indeksai.
    * Savo nustatytiems regionams turite įvesti dabartines degalų kainas.  
2. Spustelėkite Naujas.
3. Lauke „Regionas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke „Kaina už galoną“ įveskite skaičių.
6. Lauke „Įsigaliojimo pradžios data ir laikas“ įveskite datą ir laiką.
7. Spustelėkite Įrašyti.

## <a name="create-a-carrier-fuel-index"></a>Kurti vežėjo degalų indeksą
1. Pasirinkite Transportavimo valdymas > Nustatymas > Degalų indeksai > Vežėjo degalų indeksai.
2. Spustelėkite Naujas.
3. Lauke „Vežėjo degalų indeksas“ įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Naujas.
6. Lauke „Įsigaliojimo pradžios data ir laikas“ įveskite datą ir laiką.
7. Lauke „PPG nuo“ įveskite skaičių.
    * Šiame pavyzdyje laukui „PPG nuo“ galite nustatyti reikšmę 1.95.  
8. Lauke „PPG iki“ įveskite skaičių.
    * Šiame pavyzdyje laukui „PPG iki“ galite nustatyti reikšmę 2.  
9. Lauke Procentas įveskite skaičių.
    * Šiame pavyzdyje galite nustatyti procentinę reikšmę 3.  
10. Lauke Valiuta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite ir pasirinkite norimą įrašą.
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13. Spustelėkite Įrašyti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]