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
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21127c46615015c30e06465b390f67b835e746cb
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068139"
---
# <a name="create-loan-items"></a>Kurti panaudos objektus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Skolinamos prekės yra įrašai, kurie padeda sekti fizines prekes, pvz., telefonus arba kompiuterius, kurias jūsų įmonė skolina darbuotojams. Kiekviena fizinė prekė turi turėti atitinkamą skolinamą prekę. Kiekviename skolinamos prekės įraše turi būti aprašyta, kas skolinama, kas atsakingas už paskolą ir kiek dienų prekę galima skolinti. Vienu kartu galite sukurti keletą skolinamų prekių, pvz., raktų, įėjimo kortelių ar uniformų. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-loan-types"></a>Kurti paskolų tipus
1. Eiti į **Žmogiškieji ištekliai** > **Darbininkai** > **Paskolos daiktai** > **Paskolų rūšys**.
2. Spustelėkite **Naujas**.
3. Viduje konors **Paskolos tipas** lauke įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Įveskite dienų, kurias šiam paskolos tipui priskirtų prekių grąžinimas gali vėluoti, skaičių. 
6. Spustelėkite **Įrašyti**.
7. Uždarykite puslapį.
8. Atnaujinkite puslapį.

## <a name="create-loan-items"></a>Kurti panaudos objektus
1. Eiti į **Žmogiškieji ištekliai** > **Darbininkai** > **Paskolos daiktai** > **Paskolos daiktai**.
2. Spustelėkite **Sukurkite paskolos elementus**.
3. Viduje konors **Kiekis.** lauke įveskite skaičių.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Viduje konors **Paskolos tipas** lauke spustelėkite išskleidžiamąjį mygtuką, kad atidarytumėte paiešką.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Įveskite skaičių dienų, kurias prekė gali būti paskolinta.
    * Puslapyje „Paskolinta įranga“ esančio lauko „Planuojamas grąžinimas“ numatytoji vertė apskaičiuojama prie dabartinės datos pridedant šį skaičių.  
9. Viduje konors **Atsakingas asmuo** lauke spustelėkite išskleidžiamąjį mygtuką, kad atidarytumėte paiešką.
10. Spustelėkite **Pažymėti**.
11. Viduje konors **Pradinė vertė** lauke įveskite skaičių.
12. Lauke **Intervalas** įveskite skaičių.
13. Viduje konors **Formatas** lauke įveskite reikšmę.
    * Pavyzdžiui, jei paskolos prekės pradinis skaičius yra 10, įveskite du skaičių simbolių simbolius **Formatas** lauke.  
14. Spustelėkite **Gerai**.
15. Atnaujinkite puslapį.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
