--- 
title: "Kurti pristatymo grafiką"
description: "Ši procedūra parodo, kaip kurti pardavimo užsakymo pristatymo grafiką."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d99dfae5e045262d34daf3529a6a3f4716b4afe3
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="create-delivery-schedule"></a>Kurti pristatymo grafiką

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip kurti pardavimo užsakymo pristatymo grafiką. Pristatymo grafikas naudojamas, kai užsakymo arba pasiūlymo kiekį pageidaujama pristatyti keliomis siuntomis. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.


## <a name="create-delivery-schedule"></a>Kurti pristatymo grafiką
1. Eikite į Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
4. Spustelėkite Gerai.
5. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
6. Lauke Kiekis įveskite skaičių, kuris yra didesnis nei 1.
7. Spustelėkite eilutę Pardavimo užsakymas.
8. Spustelėkite Pristatymo grafikas.
    * Puslapis Pristatymo grafikas – tai vieta, kurioje galite nurodyti siuntų, kurių visas užsakymo eilutės kiekis bus pristatytas klientui, skaičių.    
    * Pagal numatytąsias nuostatas sistema visą pradinės pardavimo eilutės kiekį ir kitą pristatymo informaciją kopijuoja į pirmąją pristatymo grafiko eilutę. Šiame pavyzdyje sukursime dviejų siuntų grafiką, antrosios siuntos datą paslinkdami per savaitę nuo pirmosios.  
9. Lauke Kiekis įveskite skaičių, kuris yra viso kiekio dalis.
10. Spustelėkite Naujas.
11. Lauke Kiekis įveskite likusį kiekį.
12. Lauke Pageidaujama siuntimo data įveskite datą, kuri yra viena savaite į priekį nuo pirmosios pristatymo eilutės datos.
    * Dvi „FastTab‟ Išlaidų konvertavimas parinktys kontroliuoja, kaip išlaidas paskirstyti pristatymo grafiko eilutėse, kai jos priskirtos pradinei užsakymo eilutei. Jei pasirenkate Kopijuoti bendras sumas, ta pati išlaidų suma kopijuojama į kiekvieną eilutę. Parinktis Paskirstyti į pristatymo eilutes išlaidas vienodai padalija visose pristatymo eilutėse.  
    * Skirstyti galima tik fiksuotas išlaidas, o kintamosios išlaidos vis tiek bus kopijuojamos į eilutes.  
13. Perkėlę žymeklį nuo antrosios pristatymo eilutės, atnaujinsite puslapį.
    * Sekti visą kiekį, paskirstytą pristatymo grafiko eilutėms, galite pažvelgę į laukus Iš viso ir Liko. Kai likęs kiekis yra nulis, grafikui paskirstytas visas pradinės eilutės kiekis.   
14. Spustelėkite GERAI.
    * Pristatymo grafikas dabar nukopijuotas į užsakymo eilutes.   
    * Pradinė užsakymo eilutė, vadinama komercine eilute, konvertuota į užsakymo eilutę, kurioje yra keli pristatymai. Ji pažymėta atskira piktograma ir veikia kaip pristatymo eilučių antraštė.  
    * Dvi naujosios eilutės, vadinamos pristatymo eilutėmis, sudaro vieną pristatymo grafiką. Užsakymas bus vykdomas pagal šias eilutes, o ne pradinę eilutę. Jei spausdinami tokie dokumentai kaip patvirtinimo važtaraščiai, išrinkimo dokumentai, važtaraščiai ar SF, rodomos tik pristatymo eilutės.   
    * Pristatymo eilutėse gali skirtis pristatymo datos, kiekiai, pristatymo būdai ir saugojimo dimensijos, pvz., teritorija ir sandėlis. Tačiau produkto dimensijos visada turi atitikti dimensijas komercinėje eilutėje, ir jų keisti negalima.  
15. Lauke Kiekis įveskite skaičių, kuris yra didesnis nei dabartinis.
16. Norėdami pamatyti kiekio perskaičiavimo poveikį, pasirinkite komercinę eilutę.
17. Veiksmų srityje spustelėkite Paimti ir pakuoti.
18. Spustelėkite Registruoti važtaraštį.
19. Išplėskite skyrių Parametrai.
20. Lauke Kiekis pasirinkite Visi.
    * Atkreipkite dėmesį, kad važtaraštis bus sukurtas dviem pristatymo grafiko eilutėms, o ne pradinei užsakymo eilutei.  
21. Lauke Spausdinti važtaraštį pasirinkite Taip.
22. Spustelėkite GERAI.
23. Spustelėkite Taip.
24. Uždarykite puslapį.


