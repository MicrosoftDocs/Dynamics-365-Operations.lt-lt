---
title: Kurti pagrindinę prognozę
description: Gamybos planuotojas gali sukurti pagrindinę prognozę naudodamas laiko serijos prognozės modelius arba nukopijuodamas praeities poreikį.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc43c852fc1eff8134251efd617fc4c80b9b5480
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835939"
---
# <a name="create-a-baseline-forecast"></a>Kurti pagrindinę prognozę

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gamybos planuotojas gali sukurti pagrindinę prognozę naudodamas laiko serijos prognozės modelius arba nukopijuodamas praeities poreikį. Šioje procedūroje parodoma, kaip sukurti pagrindinę visų produktų prognozę, naudojant vieną prekių paskirstymo raktą nukopijavus praeities poreikį. 


## <a name="set-up-an-item-allocation-key"></a>Prekių paskirstymo rakto nustatymas
1. Pasirinkite Bendrasis planavimas > Nustatymas > Bendros įmonių planavimo grupės.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką „Pavadinimas“ reikšme „10“.
    * Poreikio prognozė vykdoma per visus juridinius subjektus. Todėl jums reikės visas įmones, kurioms norite generuoti prognozes, įtraukti į vieną bendrą įmonių planavimo grupę.  
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Spustelėkite „Prekių paskirstymo raktai“.
    * Pasirinkite visus prekių paskirstymo raktus, kuriems norite kurti prognozes.  
5. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite D_Aloc prekių paskirstymo raktą.  
6. Spustelėti >.
7. Uždarykite puslapį.
8. Uždarykite puslapį.

## <a name="set-up-the-demand-forecasting-paramters"></a>Nustatyti poreikio prognozės parametrus
1. Pasirinkite Bendrasis planavimas > Nustatymas > Poreikio prognozė > Poreikio prognozės parametrai.
2. Išplėskite skirtuką Prognozės algoritmo parametrai.
3. Lauke „Prognozės generavimo strategija“ pasirinkite „Kopijuoti praeities poreikį".
4. Spustelėkite Įrašyti.

## <a name="create-a-baseline-forecast"></a>Kurti pagrindinę prognozę
1. Pasirinkite Bendrasis planavimas > Prognozė > Poreikio prognozė > Generuoti pagrindinę statistinę prognozę.
2. Lauke Pradžios data įveskite datą.
    * Jei turite pardavimo užsakymų, prasidedančių 2015 m. sausio 1 d., įveskite šią datą. Jei neturite, įveskite anksčiausią pardavimo užsakymų datą.  
3. Lauke Pabaigos data įveskite datą.
    * Įveskite paskutinę savo pardavimo užsakymų datą, pavyzdžiui, „2015-03-31‟.  
4. Lauke Pradžios data įveskite datą.
    * Įveskite „2015-04-01‟. Ši data bus automatiškai skaičiuojama kaip kito prognozės segmento pradžios data.  
5. Išplėskite dalį Įtrauktini įrašai.
6. Spustelėkite Filtras.
7. Sąraše pažymėkite pasirinktą eilutę.
    * Pažymėkite eilutę, kur laukas = bendra įmonių planavimo grupė.  
8. Lauke Kriterijai surinkite reikšmę.
    * Įveskite bendrą įmonių planavimo grupę, pvz., 10, kurią naudojote pirmojoje užduotyje.  
9. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite eilutę, kur laukas = prekių paskirstymo raktas.  
10. Lauke Kriterijai surinkite reikšmę.
11. Spustelėkite GERAI.
12. Išplėskite skyrių „Išplėstiniai parametrai“.
13. Lauke „Prognozės segmentas“ pasirinkite „Mėnesis“.
14. Lauke „Prognozės laikotarpis“ įveskite „3“.
15. Lauke „Blokavimo laiko ribos“ įveskite „1‟.
16. Spustelėkite GERAI.

## <a name="visualize-the-demand-forecast"></a>Vizualizuoti poreikio prognozę
1. Pasirinkite Bendrasis planavimas > Prognozė > Poreikio prognozė > Pakoreguota poreikio prognozė.
2. Bendrojo rodinio lentelėje pasirinkite 1 eilutėje 2 stulpelyje esantį langelį. Tai – antras mėnuo, kuriam sukūrėte prognozę.
3. Nustatykite „QtyCell“ reikšmę „400“.
    * Langelyje įveskite kitą numerį nei buvo prognozuotas, pvz., 400.  
4. Pakoregavote prognozę rankiniu būdu. Atlikdami kitą veiksmą atkreipkite dėmesį į grafinę indikaciją.
5. Spustelėkite „Prognozės eilutės informacija“.
    * Šiame puslapyje galite matyti tikslumo reikšmes, praeities poreikį ir prognozę. Taip pat galite keisti ir prognozę.  

