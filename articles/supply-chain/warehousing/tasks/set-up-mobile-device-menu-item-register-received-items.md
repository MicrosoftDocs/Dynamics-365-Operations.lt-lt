---
title: Mobiliojo įrenginio meniu elemento gautoms prekėms registruoti nustatymas
description: Šioje temoje aprašyta mobiliojo įrenginio meniu elemento sąranka.
author: ShylaThompson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 599a533c90b0346637221fecc78ddd688410fb3c
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914750"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Mobiliojo įrenginio meniu elemento gautoms prekėms registruoti nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje aprašyta mobiliojo įrenginio meniu elemento sąranka. Šis meniu elementas naudojamas registruojant naudojantis pirkimo užsakymais užsakytų prekių gavimą. 

Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra skirta sandėlio vadovui.


## <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai**.
2. Pasirinkite **Naujas**.
3. Lauke **Meniu elemento pavadinimas** įveskite reikšmę. Tai šio mobiliojo įrenginio meniu elemento unikalus identifikatorius. Pavyzdžiui, galite įvesti `My PO registration`.  
4. Lauke **Pavadinimas** įveskite reikšmę. Tai yra pavadinimas, kuris bus rodomas vartotojui mobiliajame įrenginyje. Pavyzdžiui, galite įvesti `PO registration`.  
5. Lauke **Režimas** pasirinkite **Darbas**. Užregistravus turimus kiekius, gautus pirkimo užsakymo eilutei, bus sukuriamas darbas, kad būtų galima perkelti prekes iš gavimo skyriaus į atsargas. Darbo nesukuriamas, kol prekės neužregistruojamos. Todėl palikite parinkties **Naudoti esamą darbą** nuostatą **Ne**. 
6. Skyriaus **Bendra** lauke **Darbo kūrimo procesas** pasirinkite **Pirkimo užsakymo prekės gavimas**.
    - Norint užregistruoti turimą kiekį sandėlyje, pirkimo užsakymo eilutė turi būti unikaliai identifikuota. Šiuo atveju mobilusis įrenginys užregistruos pirkimo užsakymo numerį ir prekės numerį ir taip sistema galės identifikuoti PO eilutę. Bus sukurtas atidėjimo laikas ir galės išrinkti kitas darbuotojas. Nuo pasirinkto darbo kūrimo metodo priklauso, kurie laukai bus pasiekiami „FastTab“ **Bendra**.  
    - Jei pažymėsite parinktį **Naudoti numatytuosius duomenis**, bus įjungtas mygtukas **Numatytieji duomenys**. Čia galite pasirinkti laukus, kuriuose bus rodomi duomenys, paprastai reikalingi darbuotojui kasdieniame jo darbe, kad šios reikšmės būtų rodomos mobiliajame įrenginyje.  
    - Parametras **Numerio lentelių grupavimas** veikia kartu su vienetų sekų grupe, priskirta gaunamai prekei. Galite nurodyti, ar gavimus, mažesnius arba didesnius nei vienas padėklas, reikia grupuoti į vieną numerio lentelę, ar skaidyti į atskiras numerio lenteles kiekvienam vienetui.  
    - Jei pažymėsite parinktį **Generuoti numerio lentelę**, remiantis pasirinkta numeracija bus sugeneruotas unikalus numerio lentelės numeris.  
    - Galite pasirinkti šabloną, kuris bus naudojamas kuriant darbą. Pavyzdžiui, jei registruojate pirkimo užsakymo prekę, atidėjimo darbas bus sugeneruotas remiantis darbo šablonu. Jei čia nepasirinksite darbo šablono, sistema priskirs šabloną pagal užklausos kriterijus, kurie yra susieti su šablonais.  
    - Jei perdavimo kodai rodomi mobiliajame įrenginyje, darbuotojai gali įvertinti prekių būseną arba kokybę ir pasirinkti tinkamą kodą. Perdavimo kodo taisyklėse nurodoma, ar prekės bus pasiekiamos kitiems sandėlio procesams. Taisyklėse taip pat nurodoma, kuris sukurto darbo vietos nurodymas naudojamas.   
    - Jei pažymėsite parinktį **Paketo perdavimo kodai**, darbuotojai gali įvertinti paketo būseną arba kokybę ir pasirinkti tinkamą perdavimo kodą. Nustatytos paketo perdavimo kodo taisyklės lemia, ar paketas bus pasiekiamas kitiems sandėlio procesams.  
    - Jei pažymėsite parinktį **Spausdinti žymes**, gavus prekes automatiškai bus atspausdinta numerio lentelės žymė.  
7. Pasirinkite **Įrašyti**.
8. Uždarykite puslapį.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Meniu elemento įtraukimas į mobiliojo įrenginio meniu
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu**.
2. Naudokite **spartųjį filtrą**, kad filtruotumėte lauką **Pavadinimas** pagal reikšmę `inbound`.
3. Pasirinkite **Redaguoti**.
4. Galimų meniu ir elementų medyje pasirinkite anksčiau sukurtą meniu elementą.
5. Pasirinkite rodyklę, kuri rodo į dešinę.
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį.

