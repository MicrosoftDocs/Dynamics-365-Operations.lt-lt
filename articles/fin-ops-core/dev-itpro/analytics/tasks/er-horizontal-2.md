---
title: 'ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (2 dalis – Formato paleidimas)'
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 4596f7d7789ea44d49d7e7f273e4a52ee38dd90f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684528"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-2---run-format"></a>ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (2 dalis – Formato paleidimas)

[!include [banner](../../includes/banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (1 dalis. Formato kūrimas)“.

Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="find-created-format"></a>Sukurto formato radimas
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite Finansinių dimensijų modelio pavyzdys.
3. Medyje pasirinkite Financial dimensions sample model\Sample report with horizontally expandable ranges.

## <a name="execute-format-to-create-excel-output"></a>Formato paleidimas norint kurti „Excel“ išvestį
1. Spustelėkite Vykdyti.
2. Lauke Dimensijos pavadinimas įveskite BusinessUnit;CostCenter;Department.
    * Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.  Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project:  
3. Išplėskite dalį Įtrauktini įrašai.
4. Spustelėkite Filtras.
5. Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.
6. Lauke Kriterijai įveskite 00057..00058.
    * 00057..00058  
7. Spustelėkite GERAI.
8. Spustelėkite GERAI.
    * Peržiūrėkite sugeneruotą išvestį. Atkreipkite dėmesį, kad naujai sukurtame „Excel“ faile yra tiek pat stulpelių, kiek jų pasirinkta finansinėms dimensijoms. Tų stulpelių ataskaitos antraštė nurodo finansinių dimensijų pavadinimus. Tų stulpelių operacijų eilutės nurodo finansines dimensijas. Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio egzemplioriaus dimensijų skaičiaus.  

