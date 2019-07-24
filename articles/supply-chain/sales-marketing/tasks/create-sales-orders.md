---
title: Pardavimo užsakymų kūrimas
description: Šioje procedūroje parodoma, kaip kurti pardavimo užsakymą.
author: omulvad
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0c27126e688b5b8972dae3542973ed73c5e9153
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711183"
---
# <a name="create-sales-orders"></a>Pardavimo užsakymų kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti pardavimo užsakymą. Šią procedūrą galite naudoti demonstracinėje duomenų įmonėje USMF. Pardavimo užsakymus paprastai kuria pardavimo užsakymų procesorius. 

## <a name="enter-sales-order-header-details"></a>Įvesti pardavimo užsakymo antraštės informaciją
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento kodas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite kliento įrašą.
    - Šiame pavyzdyje kliento numerį pasirinkite US-004.  
5. Pasirinkite **Gerai**.

## <a name="enter-sales-order-line-details"></a>Įvesti pardavimo užsakymo eilutės informaciją
    
Jūsų organizacijos parduodami produktai gali būti kelių variantų, kuriuos skiria dimensijos, pavyzdžiui, konfigūracija, spalva, dydis ir stilius. Taip pat gali būti nustatyta, kad su produktais būtų naudojamos saugojimo dimensijos, pavyzdžiui, teritorija, sandėlis ir padėklas, bei sekimo dimensijos, pavyzdžiui, paketo ir serijos numeriai. Priskyrus šias dimensijas, užsakymo eilutėje reikia pasirinkti tų dimensijų reikšmes. Norint pagerinti užsakymo įvedimo efektyvumą, rekomenduojama į užsakymo tinklelį įtraukti atitinkamus dimensijų laukus.
    
1. Skyriuje **Pardavimo užsakymo eilutės** pasirinkite **Pardavimo užsakymo eilutė**.
2. Pasirinkite **Dimensijos**.
    
    Šiame pavyzdyje pasirinkite dimensijas Spalva, Teritorija ir Sandėlis. Čia pasirinktos dimensijos atsiras pardavimo užsakymo tinklelyje. Jei norite, kad jūsų pasirinktys išliktų, parinktį **Įrašyti nustatymus** nustatykite į Taip.
    
3. Pasirinkite **Gerai**.
4. Lauke **Prekės numeris** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Šiame pavyzdyje spustelėkite prekės numerį T0004.
    - Jei prekė yra pardavimo kategorijos dalis, prekės pavadinimas automatiškai atsiras lauke Pardavimo kategorija.  
    - Jei produkto dimensijų laukuose jau yra reikšmė, taip yra todėl, kad ši reikšmė buvo nukopijuota iš produkto įrašo, kuriame ji apibrėžta kaip numatytoji produkto dimensija. Numatytąją reikšmę galima pakeisti bet kuriuo metu.   
6. Lauke **Spalva** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Lauke **Kiekis** įveskite skaičių.
    - Jei prekė parduodama skirtingais vienetais, nei kad ji buvo pirkta, gaminama ir saugoma, ir produkto įraše nustatytas pardavimo matavimo vienetas, ši reikšmė bus rodoma lauke **Vienetas**. Reikšmę galima bet kada keisti.   
    - Jei lauke **Vieta** reikšmė jau yra, ji buvo nukopijuota iš užsakymo antraštės arba iš užsakymo nuostatų, kurios yra susietos su produktu. Reikšmę galima bet kada keisti. Jei laukas tuščias, pasirinkite reikšmę.   
    - Jei lauke **Vieneto kaina** reikšmė jau yra, ji buvo nukopijuota iš galiojančios prekybos sutarties arba iš produkto įrašo. (Vieneto kaina taip pat gali būti iš pardavimo sutarties, tačiau pardavimo užsakymų kūrimo iš pardavimo sutarčių procesas skiriasi nuo to, kuris rodomas čia.) Jei laukas tuščias, įveskite reikšmę.   
    - Lauke **Nuolaida** pateikiama produkto vieneto nuolaidos suma. Norint apskaičiuoti visą eilutės nuolaidos sumą, nuolaidos reikšmė dauginama iš eilučių kiekio. Jei lauke **Nuolaida** reikšmė jau yra, ji buvo nukopijuota iš galiojančios prekybos sutarties. Jei laukas tuščias, o klientui norite suteikti eilutės nuolaidą, įveskite reikšmę.  
    - Lauke **Nuolaidos procentas** yra procentinė reikšmė, kuria reikia sumažinti visą bendrą eilučių sumą.  Jei lauke **Nuolaidos procentas** reikšmė jau yra, ji buvo nukopijuota iš galiojančios prekybos sutarties. Jei laukas tuščias, o klientui norite suteikti eilutės nuolaidą, įveskite reikšmę. 
    - Lauke **Grynoji** yra reikšmė, kuri apskaičiuojama pagal eilutės kiekį ir vieneto kainą, pakoreguotą nuolaidų.  Apskaičiuotąją reikšmę galite pakeisti kita.  

## <a name="review-the-order-totals"></a>Peržiūrėti bendrąsias užsakymo sumas
1. **Veiksmų srityje** pasirinkite **Pardavimo užsakymas**.
2. Pasirinkite **Bendrosios sumos**.
    
    Puslapyje **Bendrosios sumos** rodoma išsami informacija apie visą užsakymą. Ji apima tarpinę sumą, kuri yra visų eilučių grynųjų sumų, pakoreguotų atsižvelgiant į galimas eilučių nuolaidas, suma, visą SF sumą, kuri yra tarpinė suma, pakoreguota atsižvelgiant į galimą užsakymo lygio nuolaidą, išlaidas ir PVM, kliento kredito limito situaciją ir kt. SF suma – tai suma, kuri bus rodoma kliento SF dokumente.  
    
3. Pasirinkite **Gerai**.
