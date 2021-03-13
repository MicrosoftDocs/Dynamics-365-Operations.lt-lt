---
title: 'ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (4 dalis – Ataskaitos vykdymas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos (ER) modelį, kad būtų galima naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. (4 dalis)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fe332de84339d3369ba495ca13f50c4901f366
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092280"
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
![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run1.png)
5. Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.
    * Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run2.png)
6. Išplėskite dalį Įtrauktini įrašai.
7. Spustelėkite Filtras.
8. Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.
9. Lauke Kriterijai įveskite 00057.
10. Spustelėkite Gerai.
11. Spustelėkite Gerai.
![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run3.png)
    * Peržiūrėkite sugeneruotą išvestį. Rodomos kiekvienos pasirinkto paketo operacijos finansinės dimensijos iš atitinkamo dimensijų rinkinio. Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio egzemplioriaus dimensijų skaičiaus.  
![ER konfigūracijų puslapis](../media/er-financial-dimensions-guides-run4.png)
