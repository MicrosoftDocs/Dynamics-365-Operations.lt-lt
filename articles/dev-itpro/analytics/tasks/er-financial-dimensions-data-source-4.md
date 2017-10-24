--- 
title: "Ataskaitos, kuri finansines dimensijas naudoja kaip duomenų šaltinį, vykdymas elektroninėse ataskaitose (ER)"
description: "Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.openlocfilehash: cdecf5fb3f3047a56353ee6d4a8f94957f508e4b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="run-a-report-that-uses-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Ataskaitos, kuri finansines dimensijas naudoja kaip duomenų šaltinį, vykdymas elektroninėse ataskaitose (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (3 dalis: ataskaitos kūrimas)“. Taip pat turite sukonfigūruoti numatytuosius dokumentų tipus puslapyje Elektroninių ataskaitų parametrai. Numatytieji dokumentų tipai taip pat nustatomi, kai jūs atsisiunčiate ir importuojate ER konfigūraciją. 


## <a name="run-report"></a>Ataskaitos vykdymas
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite Finansinių dimensijų modelio pavyzdys.
3. Medyje pasirinkite Financial dimensions sample model\Ledger journal report.
4. Spustelėkite Vykdyti.
5. Lauke Dimensijos pavadinimas įveskite arba pasirinkite reikšmę.
    * Norėdami pasirinkti visas dabartinės įmonės dimensijas, įveskite toliau nurodytą informaciją: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project:  
6. Išplėskite dalį Įtrauktini įrašai.
7. Spustelėkite Filtras.
8. Pasirinkite eilutę DK žurnalo lentelės ir lauko Žurnalo paketo numeris eilutę.
9. Lauke Kriterijai įveskite 00057.
10. Spustelėkite GERAI.
11. Spustelėkite GERAI.
    * Peržiūrėkite sugeneruotą išvestį. Atkreipkite dėmesį, kad rodomos kiekvienos pasirinkto paketo operacijos finansinės dimensijos iš atitinkamo dimensijų rinkinio. Vykdykite šią ataskaitą ir pasirinkite skirtingas dimensijas, norėdami pamatyti, ar ataskaita nepriklauso nuo pasirinktų dimensijų skaičiaus arba sukonfigūruotų šio „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo egzemplioriaus dimensijų skaičiaus.  


