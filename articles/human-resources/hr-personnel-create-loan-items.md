---
title: Kurti panaudos objektus
description: Skolinamos prekės yra įrašai, kurie padeda sekti fizines prekes, pvz., telefonus arba kompiuterius, kurias jūsų įmonė skolina darbuotojams.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26bf5a83a6d25e99996ec4219c5fbbeed806e22d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693730"
---
# <a name="create-loan-items"></a>Kurti panaudos objektus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Skolinamos prekės yra įrašai, kurie padeda sekti fizines prekes, pvz., telefonus arba kompiuterius, kurias jūsų įmonė skolina darbuotojams. Kiekviena fizinė prekė turi turėti atitinkamą skolinamą prekę. Kiekviename skolinamos prekės įraše turi būti aprašyta, kas skolinama, kas atsakingas už paskolą ir kiek dienų prekę galima skolinti. Vienu kartu galite sukurti keletą skolinamų prekių, pvz., raktų, įėjimo kortelių ar uniformų. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-loan-types"></a>Kurti paskolų tipus
1. Eiti į **Human resourcesWorkersLoan** > **·** > **itemsLoan** > **tipus**.
2. Spustelėkite **Naujas**.
3. Lauke Panaudos **tipas** įveskite vertę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Įveskite dienų, kurias šiam paskolos tipui priskirtų prekių grąžinimas gali vėluoti, skaičių. 
6. Spustelėkite **Įrašyti**.
7. Uždarykite puslapį.
8. Atnaujinkite puslapį.

## <a name="create-loan-items"></a>Kurti panaudos objektus
1. Eiti į **Human resourcesWorkersLoan** > **·** > **itemsLoan** > **elementus**.
2. Spustelėkite Kurti **panaudos objektus**.
3. **Lauke Kiekis** įveskite skaičių.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke Panaudos **tipas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Įveskite skaičių dienų, kurias prekė gali būti paskolinta.
    * Puslapyje „Paskolinta įranga“ esančio lauko „Planuojamas grąžinimas“ numatytoji vertė apskaičiuojama prie dabartinės datos pridedant šį skaičių.  
9. Lauke Atsakingas **asmuo spustelėkite** išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
10. Spustelėkite **Pažymėti**.
11. **Lauke Pradžios vertė** įveskite skaičių.
12. Lauke **Intervalas** įveskite skaičių.
13. **Lauke Formatas** įveskite vertę.
    * Pavyzdžiui, jei panaudos prekės pradžios numeris yra 10, lauke Formatas įveskite du numerio **simbolius**.  
14. Spustelėkite **Gerai**.
15. Atnaujinkite puslapį.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
