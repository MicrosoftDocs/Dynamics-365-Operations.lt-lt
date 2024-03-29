---
title: 'Vadovas: Pagrindinės prognozės kūrimas'
description: Gamybos planuotojas gali sukurti pagrindinę prognozę naudodamas laiko serijos prognozės modelius arba nukopijuodamas praeities poreikį.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eb2450f0e86eb4aa9a69c9c651ab1648ca0172b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469595"
---
# <a name="guide-create-a-baseline-forecast"></a>Vadovas: Pagrindinės prognozės kūrimas

[!include [banner](../../includes/banner.md)]

Gamybos planuotojas gali sukurti pagrindinę prognozę naudodamas laiko serijos prognozės modelius arba nukopijuodamas praeities poreikį. Šioje procedūroje parodoma, kaip sukurti pagrindinę visų produktų prognozę, naudojant vieną prekių paskirstymo raktą nukopijavus praeities poreikį.

## <a name="set-up-an-item-allocation-key"></a>Prekių paskirstymo rakto nustatymas

1. Pasirinkite **Bendrasis planavimas > Nustatymas > Bendros įmonių planavimo grupės**.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką *Pavadinimas* reikšme *10*.
    * Poreikio prognozė vykdoma per visus juridinius subjektus. Todėl jums reikės visas įmones, kurioms norite generuoti prognozes, įtraukti į vieną bendrą įmonių planavimo grupę.  
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Rinkitės **Prekių paskyrimo raktai**.
    * Pasirinkite visus prekių paskirstymo raktus, kuriems norite kurti prognozes.  
5. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite D_Aloc prekių paskirstymo raktą.  
6. Pasirinkti  **>**.
7. Uždarykite puslapį.
8. Uždarykite puslapį.

## <a name="set-up-the-demand-forecasting-parameters"></a>Nustatykite paklausos prognozės parametrus

1. Pasirinkite **Bendrasis planavimas > Nustatymas > Poreikio prognozė > Poreikio prognozės parametrai**.
2. Plėskite **Prognozės algoritmo parametrai** skirtuką.
3. Lauke **Prognozės generavimo strategija** pasirinkite **Kopijuoti praeities poreikį**.
4. Pasirinkite **Įrašyti**.

## <a name="create-a-baseline-forecast"></a>Pagrindinės prognozės kūrimas

1. Pasirinkite **Bendrasis planavimas > Prognozė > Poreikio prognozė > Generuoti pagrindinę statistinę prognozę**.
2. Lauke **Pradžios data** įveskite datą.
    * Jei turite pardavimo užsakymų, prasidedančių 2015 m. sausio 1 d., įveskite šią datą. Jei neturite, įveskite anksčiausią pardavimo užsakymų datą.  
3. Lauke **Pabaigos data** įveskite datą.
    * Įveskite paskutinę savo pardavimo užsakymų datą, pavyzdžiui *2015-03-31*.  
4. Lauke **Pradžios data** įveskite datą.
    * Įveskite *2015-04-01*. Ši data bus automatiškai skaičiuojama kaip kito prognozės segmento pradžios data.  
5. Išplėskite dalį **Įtrauktini įrašai**.
6. Pasirinkite **Filtras**.
7. Sąraše pažymėkite pasirinktą eilutę.
    * Pažymėkite eilutę, kur **Laukas** = *bendra įmonių planavimo grupė*.  
8. Lauke **Kriterijai** įveskite reikšmę.
    * Įveskite bendrą įmonių planavimo grupę, (pvz.,, *10*), kurią naudojote pirmojoje užduotyje.  
9. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite eilutę, kur **laukas** = *Prekių paskirstymo raktas*.  
10. Lauke **Kriterijai** įveskite reikšmę.
11. Pasirinkite **Gerai**.
12. Išplėskite skyrių **Išplėstiniai parametrai**.
13. Lauke **Prognozės segmentas** pasirinkite *Mėnesis*.
14. Lauke **Prognozės laikotarpis** įveskite *3*.
15. Lauke **Blokavimo laiko ribos** įveskite *1*.
16. Pasirinkite **Gerai**.

## <a name="visualize-the-demand-forecast"></a>Vizualizuoti poreikio prognozę

1. Pasirinkite **Bendrasis planavimas > Prognozė > Poreikio prognozė > Pakoreguota poreikio prognozė**.
2. Bendrojo rodinio lentelėje pasirinkite 1 eilutėje 2 stulpelyje esantį langelį. Tai – antras mėnuo, kuriam sukūrėte prognozę.
3. Nustatykite **QtyCell** į *400*.
    * Langelyje įveskite kitą numerį nei buvo prognozuotas, pvz., 400.  
4. Pakoregavote prognozę rankiniu būdu. Atlikdami kitą veiksmą atkreipkite dėmesį į grafinę indikaciją.
5. Spustelėkite **Prognozės eilutės informacija**.
    * Šiame puslapyje galite matyti tikslumo reikšmes, praeities poreikį ir prognozę. Taip pat galite keisti ir prognozę.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]