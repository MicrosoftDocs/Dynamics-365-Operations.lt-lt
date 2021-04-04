---
title: Mobiliojo įrenginio meniu elemento gautoms prekėms registruoti nustatymas
description: Šioje temoje aprašyta mobiliojo įrenginio meniu elemento sąranka.
author: ShylaThompson
manager: tfehr
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFMenu, WHSRFDefaultData
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81282e8db199c0d81e4f10de964b2fd09a5734fe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255996"
---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Mobiliojo įrenginio meniu elemento gautoms prekėms registruoti nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašyta mobiliojo įrenginio meniu elemento sąranka. Šis meniu elementas naudojamas registruojant naudojantis pirkimo užsakymais užsakytų prekių gavimą. 

Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra skirta sandėlio vadovui.


## <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas
1. Naršymo srityje eikite į **Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai**.
2. Pasirinkite **Naujas**.
3. Lauke **Meniu elemento pavadinimas** įveskite reikšmę. Tai šio mobiliojo įrenginio meniu elemento unikalus identifikatorius. Pavyzdžiui, galite įvesti `My PO registration`.  
4. Lauke **Pavadinimas** įveskite reikšmę. Tai yra pavadinimas, kuris bus rodomas vartotojui mobiliajame įrenginyje. Pavyzdžiui, galite įvesti `PO registration`.  
5. Lauke **Režimas** pasirinkite **Darbas**. Užregistravus turimus kiekius, gautus pirkimo užsakymo eilutei, bus sukuriamas darbas, kad būtų galima perkelti prekes iš gavimo skyriaus į atsargas. Darbas sukuriamas tik tada, kai prekės užregistruotos. Todėl palikite parinkties **Naudoti esamą darbą** nuostatą **Ne**.
6. Skyriaus **Bendra** lauke **Darbo kūrimo procesas** pasirinkite **Pirkimo užsakymo prekės gavimas**.
    - Norint užregistruoti turimą kiekį sandėlyje, pirkimo užsakymo eilutė turi būti unikaliai identifikuota. Šiuo atveju mobilusis įrenginys užregistruos pirkimo užsakymo numerį ir prekės numerį ir taip sistema galės identifikuoti PO eilutę. Bus sukurtas atidėjimo laikas ir galės išrinkti kitas darbuotojas. Nuo pasirinkto darbo kūrimo metodo priklauso, kurie laukai bus pasiekiami „FastTab“ **Bendra**.  
    - Jei pažymėsite parinktį **Naudoti numatytuosius duomenis**, bus įjungtas mygtukas **Numatytieji duomenys**. Čia galite pasirinkti laukus, kuriuose bus rodomi duomenys, paprastai reikalingi darbuotojui kasdieniame jo darbe, kad šios reikšmės būtų rodomos mobiliajame įrenginyje.  
    - **Numerio lentelės grupavimo** parametras veikia kartu su vienetų sekų grupe, kuri priskiriama gaunamai prekei. Galite nurodyti, ar gavimus, mažesnius arba didesnius nei vienas padėklas, reikia grupuoti į vieną numerio lentelę, ar skaidyti į atskiras numerio lenteles kiekvienam vienetui.  
    - Jei pažymėsite parinktį **Generuoti numerio lentelę**, remiantis pasirinkta numeracija bus sugeneruotas unikalus numerio lentelės numeris.  
    - Galite pasirinkti šabloną, kuris bus naudojamas kuriant darbą. Pavyzdžiui, jei registruojate pirkimo užsakymo prekę, atidėjimo darbas bus sugeneruotas remiantis darbo šablonu. Jei čia nepasirinksite darbo šablono, sistema paskirs šabloną pagal užklausos kriterijus, kurie yra susieti su šablonais.  
    - Jei perdavimo kodai rodomi mobiliajame įrenginyje, darbuotojai gali įvertinti prekių būseną arba kokybę ir pasirinkti tinkamą kodą. Perdavimo kodo taisyklėse nurodoma, ar prekės bus pasiekiamos kitiems sandėlio procesams. Taisyklėse taip pat nurodoma, kuris vietos nustatymas naudojamas sukurtam darbui.   
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]