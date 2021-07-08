---
title: Kai veikia įtaisytasis bendrojo planavimo mechanizmas, rodomas klaidos pranešimas
description: Kai vykdote nerekomenduojamą įtaisytąjį bendrojo planavimo mechanizmą, rodomas klaidos pranešimas.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294138"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Kai veikia įtaisytasis bendrojo planavimo mechanizmas, rodomas klaidos pranešimas

Klaidos kodas: „ReqCalcScheduleItemTablePlanningOptimizationFitError”

## <a name="symptoms"></a>Požymiai

Kai vykdote bendrąjį planavimą naudodami nerekomenduojamą įtaisytąjį bendrojo planavimo mechanizmą, rodomas toliau pateiktas klaidos pranešimas:

> Gaunate tolesnį klaidos pranešimą, nes sukurtas pagrindinis planavimo variklis buvo naudojamas scenarijų metu, kuriuos palaikė „Planning Optimization“. Turite perkelti į „Planning Optimization“ dabar, nes esamas sukurtas pagrindinis planavimas nebegalios. Atminkite, kad šis pagrindinio planavimo vykdymas sėkmingai baigtas. Jei perkėlimas turi stiprius priklausinius nuo esamų funkcijų, išlyga, kuria bus tęsiamas sukurtų pagrindinio planavimo variklio naudojimas gali būti prašomas. Prašome užbaigti tolesnį klausimyną, kad pradėtumėte darbą ir, jei būtina, pateikti išimties užklausą dėl persikėlimo į Planavimo optimizavimą. [Planavimo optimizavimo perkėlimo ir išimčių klausimynas](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Priežastis

Jei vykdote planavimą ir nenaudojate gamybos kontrolės priemonių, turėtumėte apsvarstyti galimybę persikelti į Planavimo optimizavimą. Įtaisytasis bendrojo planavimo mechanizmas yra nerekomenduojamas. Todėl jei norite toliau jį naudoti negaudami klaidos pranešimo, turite pateikti užklausą dėl „Microsoft” išimties.

## <a name="resolution"></a>Sprendimas

Daugiau informacijos apie tai, kaip persikelti į Planavimo optimizavimą, arba kaip pateikti išimties užklausą, kad būtų galima ir toliau naudoti nerekomenduojamą įtaisytąjį planavimo mechanizmą, rasite [Persikėlimas į Planavimo optimizavimą bendrajam planavimui](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
