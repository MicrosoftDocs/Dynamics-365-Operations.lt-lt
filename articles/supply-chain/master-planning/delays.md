---
title: "Atidėjimai"
description: "Šiame straipsnyje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8db5c507fbc68e637dbbc4ef3311d1fbd298f24f
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="delays"></a>Atidėjimai

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.

Bendrasis planavimas pagal vykdymo laiką, turimas medžiagas, turimus pajėgumus ir įvairius planavimo parametrus gali apskaičiuoti anksčiausią operacijos įvykdymo datą. 

Jei bendrojo planavimo apskaičiuota užsakymo data yra ankstesnė negu dabartinė data, užsakymas negali būti įvykdytas laiku. Todėl užsakymas atidedamas. Tokiu atveju bendrasis planavimas suplanuoja užsakymą į ateitį nuo dabartinės datos ir įtraukia vykdymo laikus. Šie vykdymo laikai prasideda nuo žemesnio lygio komponento elementų. Tada užsakymui suteikiama atidėjimo data. Atidėjimo data yra realus terminas, sugeneruotas remiantis esamais duomenimis. Bendrasis planavimas taip pat apskaičiuoja atidėjimo dienų skaičių. 

Kai kuriais atvejais jūs galite pasirinkti neapskaičiuoti atidėjimų, pvz., kai vartotojai žino, kad jie gali pagreitinti vykdymo laikus, pasirinkdami alternatyvius pristatymo būdus. 

Galite konfigūruoti, kaip skaičiuojami padengimo grupės atidėjimai. Vėliau prie prekės galite pridėti padengimo grupę. 

Puslapyje **Bendrojo planavimo parametrai** galite nustatyti atidėjimų skaičiavimo pradžios laiką. Jei užsakymas įvykdomas po šio laiko, prie užsakymo atidėjimo datos pridedamas vienos dienos atidėjimas. 

**Pastaba:** ankstesnėse versijose apskaičiuoti atidėjimai buvo žinomi kaip *ateities pranešimai*, atidėjimo data buvo žinoma kaip *ateities data*, o atidėta operacija buvo vadinama *į ateitį nustatyta operacija*.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Padengimo parametrai](coverage-settings.md)




