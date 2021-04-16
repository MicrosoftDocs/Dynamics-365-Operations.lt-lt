---
title: Planuoti priežiūros planus
description: Šioje temoje paaiškinta, kaip planuoti priežiūros planus modulyje Turto valdymas.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c19f999a94e6ad8451c208cf204d0b59306b77d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837806"
---
# <a name="schedule-maintenance-plans"></a>Planuoti priežiūros planus

[!include [banner](../../includes/banner.md)]

 

Planuojant prevencinę priežiūrą pagal nustatytus turto priežiūros planus generuojami turto kalendoriaus įrašai. Galite planuoti kalendoriaus įrašus pagal pasirinktus priežiūros planus, turto tipus ir turtą.

1. Spustelėkite **Turto valdymas** > **Laikotarpio** > **Prevencinė priežiūra** > **Planuoti priežiūros planus**.

2. Laukuose **Laikotarpis** ir **Laikotarpio dažnumas** galite pasirinkti laiko intervalą.

>[!NOTE]
>Laukuose **Laikotarpis** ir **Laikotarpio dažnumas** nurodoma, kiek laiko į priekį norite sukurti priežiūros grafiko eilučių, remiantis sukurtais priežiūros planais (pagal laiką arba pagal skaitiklį). Toliau pateiktame paveikslėlyje priežiūros grafiko eilutės (= darbo užsakymų pasiūlymai) kuriamos nuo dabartinės datos tris mėnesius į priekį.

3. Perjungimo mygtuke **Kurti automatiškai, jei nurodyta eilutėje**, pasirinkite „Taip“, jei darbo užsakymai turėtų būti automatiškai kuriami pagal priežiūros plano eilutę.

>[!NOTE]
>Jei nustatyta šio perjungimo mygtuko nuostata „Taip“, *o* formoje **Priežiūros planai** priežiūros planų eilutėse pažymėtas žymės langelis **Kurti automatiškai**, pagal priežiūros plano eilutes kuriami darbo užsakymai, taip pat sukuriamos priežiūros grafiko eilutės, kurių būsena yra „Sukurtas darbo užsakymas“. Jei pažymėta tik viena parinktis (šio dialogo lango perjungimo mygtukas **Kurti automatiškai, jei nurodyta eilutėje** arba žymės langelis **Kurti automatiškai** formoje **Priežiūros planai**) sukuriamos tik priežiūros grafiko eilutės, kurių būsena yra „Sukurta“. Tokiu atveju nesukuriama jokių darbo užsakymų.

4. Galima generuoti kalendoriaus įrašus pagal priežiūros planus (laiko ar skaitiklio), turtą, turto tipus, funkcines vietas ir funkcinių vietų tipus. Jei reikia, spustelėkite mygtuką **Filtruoti** ir pasirinkite.

- Dėl priežiūros planų planavimo funkcinėse vietose: jei suplanavę priežiūros planus atnaujinsite „FastTab“ **Visos funkcinės vietos** > **Priežiūros planai** esančių priežiūros planų turto tipų, gamintojų ir modelių sąranką, su ta funkcine vieta susiję esami priežiūros grafiko įrašai bus automatiškai ištrinti. Norėdami kurti naujus kalendoriaus įrašus, kurie atitinka atnaujintą priežiūros plano sąranką funkcinėje vietoje, turite paleisti naują tos funkcinės vietos priežiūros plano grafiką. Norėdami gauti daugiau informacijos apie funkcinių vietų turto tipų, gamintojų ir modelių sąranką, žr. [Funkcinių vietų kūrimas](../functional-locations/create-functional-locations.md).

>*Pavyzdys:* norite sukurti konkrečios funkcinės vietos priežiūros planą, o tai reiškia, kad planuojant priežiūros planą bus įtrauktas visas turtas, nustatytas toje funkcinėje vietoje bet kuriuo metu. Tokiu atveju, sukuriate priežiūros planą ir pasirenkate konkrečią funkcinę vietą, tačiau į priežiūros planą NEĮTRAUKIATE jokio turto. Rezultatas – suplanavus tą priežiūros planą, bus sukurtos viso turto, tuo metu susijusio su funkcine vieta, priežiūros grafiko eilutės.

- Jei srityje **Turto tipai** atlikite turto tipų, gamintojų ir modelių pakeitimus, tie pakeitimai turės įtakos tik naujam turtui, kuriame naudojamas atnaujintas turto tipas. Norėdami gauti daugiau informacijos apie turto tipų sąranką žr. [Turto tipai](../setup-for-objects/object-types.md).  

5. Spustelėkite **Gerai**, kad būtų pradėti generuoti turto priežiūros grafiko įrašai. Sugeneruoti įrašai bus rodomi sąrašo puslapyje **Visas priežiūros grafikas**. Toliau pateikiamame paveikslėlyje pavaizduotas dialogo lango **Planuoti priežiūros planus** pavyzdys.

![1 pav.](media/09-preventive-maintenance.png)

- Dialogo lange **Planuoti priežiūros planus**, „FastTab“ **Vykdyti fone** galite nustatyti paketines užduotis, kad kalendoriaus įrašai būtų automatiškai generuojami reguliariais intervalais.  
- Planuojant prevencinę priežiūrą priežiūros nebus sukurta grafiko eilučių, kurių numatoma pradžios data ir laikas yra ankstesni už sistemos datą ir laiką.  

Toliau pateiktame paveikslėlyje pavaizduotas priežiūros plano pagal laiką apskaičiavimas.  

![2 paveikslėlis](media/10-preventive-maintenance.jpg)

Dėl priežiūros planų pagal skaitiklį: toliau pateiktuose paveikslėliuose, rodomi du skirtingi skaitiklio registravimo ciklai. Jie pagrįsti nustatytu turto „V0001“ priežiūros planu numatant, kad turtas (automobilis) kiekvieną mėnesį nuvažiuos apie 2 000 km.

Pirmame pavyzdyje kiekvieną mėnesį nėra nuvažiuojama numatytų 2 000 km. Pagal priežiūros planą pagal skaitiklį riba yra 2 000 km, o tai reiškia, kad paleidus priežiūros plano planavimą kiekvieną kartą, kai pasiekiama 2 000 km riba, turėtų būti sukuriama priežiūros grafiko eilutė. 1 pavyzdyje yra 4 registravimo eilutės, tačiau 2 000 riba pasiekta tik vieną kartą. Tai reiškia, kad vykdant šio turto priežiūros planų planavimą, pavyzdžiui, 3 mėnesių laikotarpiu, bus sukurta tik viena priežiūros plano eilutė.

Kitame paveikslėlyje kiekvieną mėnesį užregistruojami 2 000 km arba daugiau. Todėl, jei planuosite šio turto priežiūros planus 3 mėnesių laikotarpiu, bus sukurtos tris priežiūros eilutės. 

Iš aprašytų pavyzdžių matyti, kad visose skaitiklio turto registracijose matoma tendencija apibūdinti turto nusidėvėjimą. Ši tendencija naudojama kaip skaičiavimo pagrindas priežiūros plano planavimo metu.

![3 paveikslėlis](media/11-preventive-maintenance.png)

![4 paveikslėlis](media/12-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]