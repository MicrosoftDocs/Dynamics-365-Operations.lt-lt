--- 
title: "Nustatyti mobiliojo įrenginio meniu elementą gautoms prekėms registruoti"
description: "Ši užduotis sutelkta į mobiliojo įrenginio meniu elemento nustatymą."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 642e2b05c9f9a59f6b47a22f3d92f2f6ae245039
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a>Nustatyti mobiliojo įrenginio meniu elementą gautoms prekėms registruoti

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši užduotis sutelkta į mobiliojo įrenginio meniu elemento nustatymą. Šis meniu elementas naudojamas registruojant naudojantis pirkimo užsakymais užsakytų prekių gavimą. 

Šį vadovą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra skirta sandėlio vadovui.


## <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.
2. Spustelėkite Naujas.
3. Lauke Meniu elemento pavadinimas surinkite reikšmę.
    * Tai šio mobiliojo įrenginio meniu elemento unikalus identifikatorius. Pavyzdžiui, galite įvesti „Mano PO registracija“.  
4. Lauke Pavadinimas surinkite reikšmę.
    * Tai yra pavadinimas, kuris bus rodomas vartotojui mobiliajame įrenginyje. Pavyzdžiui, galite įvesti „PO registracija“.  
5. Lauke Režimas pasirinkite „Darbas“.
    * Užregistravus turimus kiekius, gautus pirkimo užsakymo eilutei, bus sukuriamas darbas, kad būtų galima perkelti prekes iš gavimo skyriaus į atsargas. Darbo nesukuriamas, kol prekės neužregistruojamos.  Todėl palikite nustatytą parinkties Naudoti esamą darbą padėtį Ne.  
6. Išplėskite arba sutraukite dalį Bendra.
7. Lauke Darbo kūrimo procesas pasirinkite„Gaunama pirkimo užsakymo prekė“.
    * Norint užregistruoti turimą kiekį sandėlyje, pirkimo užsakymo eilutė turi būti unikaliai identifikuota. Šiuo atveju mobilusis įrenginys užregistruos pirkimo užsakymo numerį ir prekės numerį ir taip sistema galės identifikuoti PO eilutę. Bus sukurtas atidėjimo laikas ir galės išrinkti kitas darbuotojas.    Jūsų pasirinktas darbo kūrimo metodas nurodo, kurie laukai tampa pasiekiami skirtuke Bendra.  
    * Jei pasirinksite pasirinktį Naudoti numatytuosius duomenis, įgalinamas mygtukas Numatytieji duomenys. Čia galite pasirinkti laukus, kuriuose bus rodomi duomenys, paprastai reikalingi darbuotojui kasdieniame jo darbe, kad šios reikšmės būtų rodomos mobiliajame įrenginyje.  
    * Numerio lentelių grupavimo parametras veikia kartu su vienetų sekų grupe, priskirta prie gaunamos prekės. Galite nurodyti, ar gavimus, mažesnius arba didesnius nei vienas padėklas, reikia grupuoti į vieną numerio lentelę, ar skaidyti į atskiras numerio lenteles kiekvienam vienetui.  
    * Jei pasirinksite pasirinktį Generuoti numerio lentelę, pagal numeracijos pasirinkimą bus sugeneruotas unikalus numerio lentelės numeris.   
    * Galite pasirinkti šabloną, kuris bus naudojamas kuriant darbą. Pavyzdžiui, jei registruojate pirkimo užsakymo prekę, atidėjimo darbas bus sugeneruotas remiantis darbo šablonu. Jei čia nepasirinksite darbo šablono, sistema priskirs šabloną pagal užklausos kriterijus, kurie yra susieti su šablonais.  
    * Jei perdavimo kodai rodomi mobiliajame įrenginyje, darbuotojai gali įvertinti prekių būseną arba kokybę ir pasirinkti tinkamą kodą. Perdavimo kodo taisyklėse nurodoma, ar prekės bus pasiekiamos kitiems sandėlio procesams. Taisyklėse taip pat nurodoma, kuris sukurto darbo vietos nurodymas naudojamas.   
    * Jei pasirinksite parinktį Paketo perdavimo kodai, darbuotojai galės įvertinti paketo būseną arba kokybę ir pasirinkti tinkamą perdavimo kodą.  Nustatytos paketo perdavimo kodo taisyklės lemia, ar paketas bus pasiekiamas kitiems sandėlio procesams.  
    * Jei pasirinksite parinktį Spausdinti etiketes, numerio lentelės etiketė bus spausdinama automatiškai, kai gaunamos prekės.  
8. Spustelėkite Įrašyti.
9. Uždarykite puslapį.

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Meniu elemento įtraukimas į mobiliojo įrenginio meniu
1. Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu.
2. Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Pavadinimas pagal reikšmę „gaunami“.
3. Spustelėkite Redaguoti.
4. Medyje pasirinkite „Medyje Galimi meniu ir prekės pasirinkite anksčiau sukurtą meniu elementą.‟.
    * Pasirinkite meniu elementą, kurį sukūrėte anksčiau.  
5. Spustelėkite į dešinę pusę rodančią rodyklę.
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.


