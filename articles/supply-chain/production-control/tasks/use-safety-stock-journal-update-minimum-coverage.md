--- 
title: "Pakankamų atsargų žurnalo naudojimas mažiausiam padengimui atnaujinti"
description: "Šioje procedūroje nurodoma, kaip mažiausio padengimo pasiūlymus apskaičiuoti pagal praeities operacijas ir tada atnaujinti prekės padengimą naudojant pasiūlymus."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 72b873faaee7bc86bd98f90ca2fb12a216d2f06b
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# Pakankamų atsargų žurnalo naudojimas mažiausiam padengimui atnaujinti

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje nurodoma, kaip mažiausio padengimo pasiūlymus apskaičiuoti pagal praeities operacijas ir tada atnaujinti prekės padengimą naudojant pasiūlymus. Tai atliekama naudojant pakankamų atsargų žurnalą. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši užduotis skirta gamybos planuotojui, kad būtų lengviau tvarkyti mažiausią padengimą.


## Kurti naują pakankamų atsargų žurnalo pavadinimą
1. Pasirinkite Pakankamų atsargų žurnalų pavadinimai.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas įveskite „Medžiagos“.
4. Lauke Aprašas įveskite „Medžiagos“.
5. Uždarykite puslapį.

## Kurti pakankamų atsargų žurnalą
1. Pasirinkite Pakankamų atsargų skaičiavimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
    * Pasirinkite sukurto pakankamų atsargų žurnalo pavadinimą, pvz., Medžiagos.  
4. Spustelėkite Kurti eilutes.
5. Lauke Pradžios data įveskite datą.
    * Nustatykite datą į „2015-01-02“.  
6. Lauke Pabaigos data įveskite datą.
    * Nustatykite datą į „2015-12-30“.  
7. Spustelėkite GERAI.
    * Taip sukursite dimensijų, kuriose yra atsargų operacijų, eilutes.  

## Apskaičiuoti pasiūlymą
1. Spustelėkite Apskaičiuoti pasiūlymą.
2. Pasirinkite parinktį Naudoti išdavimo vidurkį per gamybos laiką.
3. Nustatykite dauginimo koeficientą į 10.
    * Dauginimo koeficientas naudojamas pasiūlymui koreguoti. Kadangi demonstraciniuose duomenyse yra tik kelios operacijos, turėsite nustatyti koeficientą, gautumėte realų pasiūlymą.  
4. Spustelėkite GERAI.
    * Slinkite žemyn ir raskite M0002 bei M0003. Peržiūrėkite stulpelį Apskaičiuotas mažiausias kiekis.   

## Naujinti mažiausią kiekį
1. Lauke Naujas mažiausias kiekis įveskite skaičių.
    * Atnaujinkite lauko Naujas mažiausias kiekis reikšmę, kad ji atitiktų lauko Apskaičiuotas mažiausias kiekis reikšmę. Jei apskaičiuotas mažiausias kiekis yra lygus nuliui, galite įvesti norimą būsimąją reikšmę. Pavyzdžiui, šiame lauke galite įvesti M0002, kurio sandėlis yra 12-asis, apskaičiuotą mažiausią kiekį.  
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pavyzdžiui, galite pasirinkti M0002, kurio sandėlis yra 12-asis.  
3. Lauke Naujas mažiausias kiekis įveskite skaičių.
    * Atnaujinkite lauko Naujas mažiausias kiekis reikšmę, kad ji atitiktų lauko Apskaičiuotas mažiausias kiekis reikšmę. Jei apskaičiuotas mažiausias kiekis yra lygus nuliui, galite įvesti norimą būsimąją reikšmę.  

## Registruoti naują mažiausią kiekį ir patikrinti rezultatą
1. Spustelėkite Registruoti.
2. Spustelėkite GERAI.
3. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Prekės numeris.
4. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Prekės numeris.
5. Veiksmų srityje spustelėkite Planuoti.
6. Spustelėkite Prekės padengimas.
    * Atkreipkite dėmesį, kad mažiausias kiekis buvo atnaujintas, įvedus naują mažiausią kiekį iš pakankamų atsargų žurnalo.  


