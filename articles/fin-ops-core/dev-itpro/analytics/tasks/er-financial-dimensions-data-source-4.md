---
title: 'ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos (ER) modelį, kad būtų galima naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. (4 dalis)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3bf58ec746fedb046b6014f5343d4ac92c2e6aba72882dec5b1f737aa1aaae46
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743218"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4---run-the-report"></a>ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)

[!include [banner](../../includes/banner.md)]

Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis. Ataskaitos kūrimas)“. Taip pat turite sukonfigūruoti numatytuosius dokumentų tipus puslapyje Elektroninių ataskaitų parametrai. Numatytieji dokumentų tipai taip pat nustatomi, kai jūs atsisiunčiate ir importuojate ER konfigūraciją. 


## <a name="run-report"></a>Ataskaitos vykdymas
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite Finansinių dimensijų modelio pavyzdys.
3. Medyje pasirinkite Financial dimensions sample model\Ledger journal report.
4. Spustelėkite Vykdyti.
![ER konfigūracijų puslapis.](../media/er-financial-dimensions-guides-run1.png)
5. Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.
    * Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![ER konfigūracijų puslapis.](../media/er-financial-dimensions-guides-run2.png)
6. Išplėskite dalį Įtrauktini įrašai.
7. Spustelėkite Filtras.
8. Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.
9. Lauke Kriterijai įveskite 00057.
10. Spustelėkite Gerai.
11. Spustelėkite Gerai.
![ER konfigūracijų puslapis.](../media/er-financial-dimensions-guides-run3.png)
    * Peržiūrėkite sugeneruotą išvestį. Rodomos kiekvienos pasirinkto paketo operacijos finansinės dimensijos iš atitinkamo dimensijų rinkinio. Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio egzemplioriaus dimensijų skaičiaus.  
![ER konfigūracijų puslapis.](../media/er-financial-dimensions-guides-run4.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]