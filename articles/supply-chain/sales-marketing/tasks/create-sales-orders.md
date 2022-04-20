---
title: Pardavimo užsakymų kūrimas
description: Šioje procedūroje parodoma, kaip kurti pardavimo užsakymą.
author: Henrikan
ms.date: 04/06/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, InventDimParmFixed, InventProductDimensionLookup, SalesTotals
audience: Application User, SalesTableDelete, SalesTableListPagePreviewPage, SalesUpdateRemain
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462f47ab5d85665ed8132e5bfb6dd945c537c1ef
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551730"
---
# <a name="create-sales-orders"></a>Pardavimo užsakymų kūrimas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti pardavimo užsakymą. Šią procedūrą galite naudoti demonstracinėje duomenų įmonėje USMF. Pardavimo užsakymus paprastai kuria pardavimo užsakymų procesorius. 

## <a name="enter-sales-order-header-details"></a>Įvesti pardavimo užsakymo antraštės informaciją
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento kodas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite kliento įrašą.
    - Šiame pavyzdyje kliento numerį pasirinkite US-004.  
5. Pasirinkite **Gerai**.

## <a name="enter-sales-order-line-details"></a>Įvesti pardavimo užsakymo eilutės informaciją
    
Jūsų organizacijos parduodami produktai gali būti kelių variantų, kuriuos skiria dimensijos, pavyzdžiui, konfigūracija, spalva, dydis ir stilius. Be to, gali būti nustatyta, kad su produktais būtų naudojamos saugojimo dimensijos, pavyzdžiui, teritorija, sandėlis ir padėklas, taip pat sekimo dimensijos, pavyzdžiui, paketo ir serijos numeriai. Priskyrus šias dimensijas, užsakymo eilutėje reikia pasirinkti tų dimensijų reikšmes. Norint pagerinti užsakymo įvedimo efektyvumą, rekomenduojama į užsakymo tinklelį įtraukti atitinkamus dimensijų laukus.
    
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
    
    Puslapyje **Bendrosios sumos** rodoma išsami informacija apie visą užsakymą. Ji apima tarpinę sumą, kuri yra visų eilučių grynųjų sumų, pakoreguotų atsižvelgiant į galimas eilučių nuolaidas, suma, visą SF sumą, kuri yra tarpinė suma, pakoreguota atsižvelgiant į galimą užsakymo lygio nuolaidą, išlaidas ir PVM, kliento kredito limito situaciją ir kita. SF suma – tai suma, kuri bus rodoma kliento SF dokumente.  
    
3. Pasirinkite **Gerai**.

## <a name="sales-order-creation-performance-enhancement"></a>Pardavimo užsakymo kūrimo našumo gerinimas
Nauja priemonė, įdiegta su programos 10.0.26 **versija, sumažina papildomą lentelių SourceDocumentHeader** ir **SourceDocumentLine įrašų kūrimą**. Našumas pagerėja, o saugojimo dydis sumažėja, nes šie įrašai nesukurti. Šios pagrindinio šaltinio dokumento sistemos lentelės šiuo metu nėra naudojamos produkto pardavimo užsakymams ir nėra suplanuotų planų, kuriuos būtų galima naudoti. Įgalinus šią funkciją, laikoma saugiais pokyčiais, siekiant padidinti našumą. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
