---
title: "Atidėjimai"
description: "Šiame straipsnyje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9113c7728c5d23b70e3809bab31136aff63c6acf
ms.lasthandoff: 03/31/2017


---

# <a name="delays"></a>Atidėjimai

Šiame straipsnyje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.

Bendrasis planavimas pagal vykdymo laiką, turimas medžiagas, turimus pajėgumus ir įvairius planavimo parametrus gali apskaičiuoti anksčiausią operacijos įvykdymo datą. 

Jei bendrojo planavimo apskaičiuota užsakymo data yra ankstesnė negu dabartinė data, užsakymas negali būti įvykdytas laiku. Todėl užsakymas atidedamas. Tokiu atveju bendrasis planavimas suplanuoja užsakymą į ateitį nuo dabartinės datos ir įtraukia vykdymo laikus. Šie vykdymo laikai prasideda nuo žemesnio lygio komponento elementų. Tada užsakymui suteikiama atidėjimo data. Atidėjimo data yra realus terminas, sugeneruotas remiantis esamais duomenimis. Bendrasis planavimas taip pat apskaičiuoja atidėjimo dienų skaičių. 

Kai kuriais atvejais jūs galite pasirinkti neapskaičiuoti atidėjimų, pvz., kai vartotojai žino, kad jie gali pagreitinti vykdymo laikus, pasirinkdami alternatyvius pristatymo būdus. 

Galite konfigūruoti, kaip skaičiuojami padengimo grupės atidėjimai. Vėliau prie prekės galite pridėti padengimo grupę. 

Puslapyje **Bendrojo planavimo parametrai** galite nustatyti atidėjimų skaičiavimo pradžios laiką. Jei užsakymas įvykdomas po šio laiko, prie užsakymo atidėjimo datos pridedamas vienos dienos atidėjimas. 

**Pastaba:** ankstesnėse versijose, apskaičiuotas vėlavimą vadinosi *ateities pranešimai*, uždelstos dienos buvo žinomas kaip į *ateities data*, ir uždelstas sandoris buvo nurodyta kaip *operacija, kuri buvo ateityje rinkinys*.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Padengimo parametrai](coverage-settings.md)


