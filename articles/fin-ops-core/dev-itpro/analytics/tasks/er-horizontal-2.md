---
title: 'ER: horizontaliai išplečiamų diapazonų naudojimas norint dinamiškai įtraukti stulpelius į „Excel“ ataskaitas (2 dalis – Formato paleidimas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninių ataskaitų (ER) formatą generuoti ataskaitoms, tokioms kaip OPENXML darbalapių („Excel”) failai. (2 dalis)
author: NickSelin
ms.date: 08/29/2018
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
ms.openlocfilehash: a62bad6ca241a2372a72e312ec5a707008a5fc09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744992"
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]