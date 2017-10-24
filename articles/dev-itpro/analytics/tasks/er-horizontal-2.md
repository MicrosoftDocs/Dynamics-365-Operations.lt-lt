--- 
title: "Formato, naudojančio horizontaliai išplečiamus diapazonus, kad elektroninėse ataskaitose (ER) stulpeliai į „Excel“ ataskaitas būtų įtraukiami dinamiškai, paleidimas"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8e5c53905b903bc5242625283f3b093144243cf9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-format-that-uses-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-for-electronic-reporting-er"></a>Formato, naudojančio horizontaliai išplečiamus diapazonus, kad elektroninėse ataskaitose (ER) stulpeliai į „Excel“ ataskaitas būtų įtraukiami dinamiškai, paleidimas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas ataskaitas generuoti kaip OPENXML darbalapių („Excel“) failus, kuriuose būtinus stulpelius galima dinamiškai kurti kaip horizontaliai išplečiamus diapazonus. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite veiksmus, nurodytus procedūroje „ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (1 dalis: formato kūrimas)“.

Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


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
    * Peržiūrėkite sugeneruotą išvestį. Atkreipkite dėmesį, kad naujai sukurtame „Excel“ faile yra tiek pat stulpelių, kiek jų pasirinkta finansinėms dimensijoms. Tų stulpelių ataskaitos antraštė nurodo finansinių dimensijų pavadinimus. Tų stulpelių operacijų eilutės nurodo finansines dimensijas. Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo egzemplioriaus dimensijų skaičiaus.  


