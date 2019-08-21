---
title: Pakankamų atsargų žurnalo naudojimas mažiausiam padengimui atnaujinti
description: Šioje procedūroje nurodoma, kaip mažiausio padengimo pasiūlymus apskaičiuoti pagal praeities operacijas ir tada atnaujinti prekės padengimą naudojant pasiūlymus.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3b2916d6d2f24579fd9795c0e0bc548b6c2b747
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835789"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a>Pakankamų atsargų žurnalo naudojimas mažiausiam padengimui atnaujinti

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje nurodoma, kaip mažiausio padengimo pasiūlymus apskaičiuoti pagal praeities operacijas ir tada atnaujinti prekės padengimą naudojant pasiūlymus. Tai atliekama naudojant pakankamų atsargų žurnalą. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši užduotis skirta gamybos planuotojui, kad būtų lengviau tvarkyti mažiausią padengimą.


## <a name="create-a-new-safety-stock-journal-name"></a>Kurti naują pakankamų atsargų žurnalo pavadinimą
1. Pasirinkite Pakankamų atsargų žurnalų pavadinimai.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas įveskite „Medžiagos“.
4. Lauke Aprašas įveskite „Medžiagos“.
5. Uždarykite puslapį.

## <a name="create-a-safety-stock-journal"></a>Kurti pakankamų atsargų žurnalą
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

## <a name="calculate-proposal"></a>Apskaičiuoti pasiūlymą
1. Spustelėkite Apskaičiuoti pasiūlymą.
2. Pasirinkite parinktį Naudoti išdavimo vidurkį per gamybos laiką.
3. Nustatykite dauginimo koeficientą į 10.
    * Dauginimo koeficientas naudojamas pasiūlymui koreguoti. Kadangi demonstraciniuose duomenyse yra tik kelios operacijos, turėsite nustatyti koeficientą, gautumėte realų pasiūlymą.  
4. Spustelėkite GERAI.
    * Slinkite žemyn ir raskite M0002 bei M0003. Peržiūrėkite stulpelį Apskaičiuotas mažiausias kiekis.   

## <a name="update-minimum-quantity"></a>Naujinti mažiausią kiekį
1. Lauke Naujas mažiausias kiekis įveskite skaičių.
    * Atnaujinkite lauko Naujas mažiausias kiekis reikšmę, kad ji atitiktų lauko Apskaičiuotas mažiausias kiekis reikšmę. Jei apskaičiuotas mažiausias kiekis yra lygus nuliui, galite įvesti norimą būsimąją reikšmę. Pavyzdžiui, šiame lauke galite įvesti M0002, kurio sandėlis yra 12-asis, apskaičiuotą mažiausią kiekį.  
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pavyzdžiui, galite pasirinkti M0002, kurio sandėlis yra 12-asis.  
3. Lauke Naujas mažiausias kiekis įveskite skaičių.
    * Atnaujinkite lauko Naujas mažiausias kiekis reikšmę, kad ji atitiktų lauko Apskaičiuotas mažiausias kiekis reikšmę. Jei apskaičiuotas mažiausias kiekis yra lygus nuliui, galite įvesti norimą būsimąją reikšmę.  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Registruoti naują mažiausią kiekį ir patikrinti rezultatą
1. Spustelėkite Registruoti.
2. Spustelėkite GERAI.
3. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Prekės numeris.
4. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Prekės numeris.
5. Veiksmų srityje spustelėkite Planuoti.
6. Spustelėkite Prekės padengimas.
    * Atkreipkite dėmesį, kad mažiausias kiekis buvo atnaujintas, įvedus naują mažiausią kiekį iš pakankamų atsargų žurnalo.  

