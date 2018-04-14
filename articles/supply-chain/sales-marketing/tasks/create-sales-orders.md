--- 
title: "Pardavimo užsakymų kūrimas"
description: "Šioje procedūroje parodoma, kaip kurti pardavimo užsakymą."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4ccd2c4ace41f07dce14498031e3cc29ecb61b1c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-sales-orders"></a>Pardavimo užsakymų kūrimas

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti pardavimo užsakymą. Šią procedūrą galite naudoti demonstracinėje duomenų įmonėje USMF. Pardavimo užsakymus paprastai kuria pardavimo užsakymų procesorius. 




## <a name="enter-sales-order-header-details"></a>Įvesti pardavimo užsakymo antraštės informaciją
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite kliento įrašą.
    * Šiame pavyzdyje kliento numerį pasirinkite US-004.  
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite GERAI.

## <a name="enter-sales-order-line-details"></a>Įvesti pardavimo užsakymo eilutės informaciją
    * Jūsų organizacijos parduodami produktai gali būti kelių variantų, kuriuos skiria dimensijos, pavyzdžiui, konfigūracija, spalva, dydis ir stilius. Taip pat gali būti nustatyta, kad su produktais būtų naudojamos saugojimo dimensijos, pavyzdžiui, teritorija, sandėlis ir padėklas, bei sekimo dimensijos, pavyzdžiui, paketo ir serijos numeriai. Priskyrus šias dimensijas, užsakymo eilutėje reikia pasirinkti tų dimensijų reikšmes. Norint pagerinti užsakymo įvedimo efektyvumą, rekomenduojama į užsakymo tinklelį įtraukti atitinkamus dimensijų laukus.  
1. Spustelėkite eilutę Pardavimo užsakymas.
2. Spustelėkite Dimensijos.
    * Šiame pavyzdyje pasirinkite dimensijas Spalva, Teritorija ir Sandėlis. Čia pasirinktos dimensijos atsiras pardavimo užsakymo tinklelyje. Jei norite, kad jūsų pasirinktys išliktų, parinktį Įrašyti sąranką nustatykite į Taip.   
3. Spustelėkite GERAI.
4. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Šiame pavyzdyje spustelėkite prekės numerį T0004.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Jei prekė yra pardavimo kategorijos dalis, prekės pavadinimas automatiškai atsiras lauke Pardavimo kategorija.  
    * Jei produkto dimensijų laukuose jau yra reikšmė, taip yra todėl, kad ši reikšmė buvo nukopijuota iš produkto įrašo, kuriame ji apibrėžta kaip numatytoji produkto dimensija. Numatytąją reikšmę galima pakeisti bet kuriuo metu.   
7. Lauke Spalva spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše raskite ir pasirinkite norimą įrašą.
9. Sąraše spustelėkite saitą pasirinktoje eilutėje.
10. Lauke Kiekis įveskite skaičių.
    * Jei prekė parduodama skirtingais vienetais, nei kad ji buvo pirkta, gaminama ir saugoma, ir produkto įraše nustatytas pardavimo matavimo vienetas, ši reikšmė bus rodoma lauke Vienetas. Reikšmę galima bet kada keisti.   
    * Jei lauke Teritorija reikšmė jau yra, ji buvo nukopijuota iš užsakymo antraštės arba iš užsakymo nuostatų, kurios yra susietos su produktu. Reikšmę galima bet kada keisti. Jei laukas tuščias, pasirinkite reikšmę.   
    * Jei lauke Vieneto kaina reikšmė jau yra, ji buvo nukopijuota iš galiojančios prekybos sutarties arba iš produkto įrašo. (Vieneto kaina taip pat gali būti iš pardavimo sutarties, tačiau pardavimo užsakymų kūrimo iš pardavimo sutarčių procesas skiriasi nuo to, kuris rodomas čia.) Jei laukas tuščias, įveskite reikšmę.   
    * Lauke Nuolaida pateikiama produkto vieneto nuolaidos suma. Norint apskaičiuoti visą eilutės nuolaidos sumą, nuolaidos reikšmė dauginama iš eilučių kiekio.    Jei lauke Nuolaida reikšmė jau yra, ji buvo nukopijuota iš galiojančios prekybos sutarties. Jei laukas tuščias, o klientui norite suteikti eilutės nuolaidą, įveskite reikšmę.  
    * Lauke Nuolaidos procentas yra procentinė reikšmė, kuria reikia sumažinti visą bendrą eilučių sumą.  Jei lauke Nuolaidos procentas reikšmė jau yra, ji buvo nukopijuota iš galiojančios prekybos sutarties. Jei laukas tuščias, o klientui norite suteikti eilutės nuolaidą, įveskite reikšmę.  
    * Lauke Grynoji suma yra reikšmė, kuri apskaičiuojama pagal eilutės kiekį ir vieneto kainą, pakoreguotą nuolaidų.  Apskaičiuotąją reikšmę galite pakeisti kita.  

## <a name="review-the-order-totals"></a>Peržiūrėti bendrąsias užsakymo sumas
1. Veiksmų srityje spustelėkite Pardavimo užsakymas.
2. Spustelėkite Sumos.
    * Puslapyje Sumos rodoma išsami informacija apie visą užsakymą. Ji apima tarpinę sumą, kuri yra visų eilučių grynųjų sumų, pakoreguotų atsižvelgiant į galimas eilučių nuolaidas, suma, visą SF sumą, kuri yra tarpinė suma, pakoreguota atsižvelgiant į galimą užsakymo lygio nuolaidą, išlaidas ir PVM, kliento kredito limito situaciją ir kt.  SF suma – tai suma, kuri bus rodoma kliento SF dokumente.  
3. Spustelėkite GERAI.


