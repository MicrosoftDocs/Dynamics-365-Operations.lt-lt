--- 
title: "Siųsti užsakymus kaip tiesioginius pristatymus"
description: "Ši procedūra parodo, kaip kurti pardavimo užsakymo tiesioginį pristatymą."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f674de4877dd2d6e6f1ff02f16a68cb4805d9864
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="ship-orders-as-direct-deliveries"></a>Siųsti užsakymus kaip tiesioginius pristatymus

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip kurti pardavimo užsakymo tiesioginį pristatymą. Tiesioginį pristatymą naudojate, kai norite siųsti prekes klientui tiesiogiai iš tiekėjo, vietoj to, kad pirma jas siųstumėte į savo sandėlį. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Norėdami sėkmingai baigti antrąją antrinę užduotį „Kurti tiesioginius pristatymus iš darbastalio“, įsitikinkite, kad, pasirinktos pardavimo užsakymo prekės numatytasis Tiekėjas nurodytas Patvirtintų pagrindinių produktų Pirkimo „FastTab“.


## <a name="set-an-individual-order-for-direct-delivery"></a>Nustatyti atskirą tiesioginio pristatymo užsakymą
1. Eikite į Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti sąskaitą US-001.  
4. Spustelėkite GERAI.
5. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Jei naudojate USMF, galite pasirinkti prekę T0020.  
6. Spustelėkite Įrašyti.
7. Veiksmų srityje spustelėkite Pardavimo užsakymas.
8. Spustelėkite Tiesioginis pristatymas.
    * Puslapyje Kurti pristatymą išvardytos visos atvirų pardavimo užsakymų eilutės taip, kaip nukopijuota iš pardavimo užsakymo. Galite peržiūrėti užsakymo informaciją ir, jei reikia, galite modifikuoti informaciją, pvz., pirkimo kiekį ir kainų nustatymo sąlygas, prieš kurdami tiesioginį pristatymą.  
9. Lauke Įtraukti viską pasirinkite Taip.
    * Jei tiesioginį pristatymą norite sugeneruoti tik pardavimo užsakymo eilučių pogrupiui, pažymėkite jas atskirai.  
    * Lauke Tiekėjo sąskaita gali būti įvestas arba dar nebūti įvestas tiekėjo numeris. Jei yra nustatytas produkto numatytasis tiekėjas (susietame Prekės padengime), šis tiekėjas bus nukopijuotas į eilutę. Priešingu atveju, tiekėją turite įvesti rankiniu būdu. Šiame pavyzdyje pasirinksime naują tiekėją kitame veiksme, net jei jis jau įvestas.   
10. Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.
    * Jei naudojate USMF, galite pasirinkti sąskaitą 1001.  
11. Spustelėkite GERAI.
    * Pranešimas informuoja, kad pirkimo užsakymas sukurtas.   
12. Išplėskite skyrių Eilutės informacija.
13. Spustelėkite skirtuką Pristatymas.
    * Laukas Tiesioginis pristatymas dabar nustatytas į Taip.  
    * Tiesioginio pristatymo būsena rodo sukurtą pirkimo užsakymą.   
14. Veiksmų srityje spustelėkite Bendra.
15. Spustelėkite Susiję užsakymai.
16. Spustelėkite, jei norite atidaryti lauke Pirkimo užsakymas esantį saitą.
17. Išplėskite skyrių Eilutės informacija.
18. Spustelėkite skirtuką Adresas.
    * Atkreipkite dėmesį, kad šios pirkimo užsakymo eilutės pristatymo adresas yra kliento pristatymo adresas, o ne jūsų įmonės adresas.  
    * Jeigu pakeisite pristatymo adresą pardavimo užsakymo eilutėje arba pradinio pardavimo užsakymo eilutėje, pristatymo adresas atitinkamoje užsakymo eilutėje bus automatiškai atnaujintas.  
19. Spustelėkite skirtuką Pristatymas.
    * Kaip ir pardavimo užsakymo eilutės, taip ir susieto pirkimo užsakymo eilutės tipas irgi nustatytas į Tiesioginis pristatymas.  
    * Pirkimo užsakymo eilutės Pristatymo data ir Patvirtinta pristatymo data yra nustatytos į Pageidaujama gavimo data ir Patvirtinta gavimo data iš atitinkamos pradinio pardavimo užsakymo eilutės.   
    * Jei atnaujinsite bet kurią iš šių datų arba pirkimo eilutėje, arba pardavimo eilutėje, atitinkamo užsakymo datos bus automatiškai atnaujintos.     
    * Pirkimo užsakymas, kuriame nustatyta prekes pristatyti tiesiogiai klientui, yra specialiu būdu susietas su pradiniu pardavimo užsakymu. Šis susiejimas nustato taisyklę, kad pardavimo užsakymo važtaraščio atnaujinimo negalima atlikti iš paties pardavimo užsakymo, jis turi būti atliekamas naudojant pirkimo užsakymą. Tačiau kliento SF išrašymas atliekamas pagal pardavimo užsakymą.  
20. Veiksmų srityje spustelėkite Pirkti.
21. Spustelėkite „Patvirtinimas“.
22. Spustelėkite GERAI.
23. Veiksmų srityje spustelėkite Gauti.
24. Spustelėkite Produkto gavimo kvitas.
25. Lauke Produkto gavimo kvitas surinkite reikšmę.
26. Spustelėkite GERAI.
27. Veiksmų srityje spustelėkite Bendra.
28. Spustelėkite Susiję užsakymai.
29. Sąraše pažymėkite pasirinktą eilutę.
    * Po to, kai pirkimo užsakymas buvo atnaujintas kaip gautas, arba, kitaip tariant, po to, kai tiekėjas išsiuntė prekes jūsų kliento adresu, pradinio pardavimo užsakymo būsena automatiškai atnaujinama į Pristatyta.  
    * Dabar galima išrašyti pardavimo užsakymo SF.    
30. Spustelėkite GERAI.
31. Uždarykite puslapį.
32. Spustelėkite GERAI.

## <a name="create-direct-deliveries-from-the-workbench"></a>Kurti tiesioginius pristatymus iš darbastalio
1. Uždarykite puslapį.
2. Uždarykite puslapį.
3. Eikite į Visi pardavimo užsakymai.
4. Spustelėkite Naujas.
5. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
6. Spustelėkite Gerai.
7. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
8. Išplėskite skyrių Eilutės informacija.
9. Spustelėkite skirtuką Pristatymas.
    * Užuot tiesioginį pristatymą kūrę kaip pardavimo užsakymo apdorojimo dalį, kaip ankstesnėje procedūroje, galite perduoti šią užduotį pirkimo specialistui. Norint pardavimo užsakymo eilutę įtraukti į tiesioginio pristatymo tvarkymo procesą, turite eilutėje pažymėti tiesioginį pristatymą.  
10. Lauke Tiesioginis pristatymas pasirinkite Taip.
    *   Jei prekei jau nustatytas tiesioginis pristatymas pagal numatytuosius nustatymus, užsakymo eilutės įraše laukas bus automatiškai nustatytas į Taip. Galite nustatyti prekės tiesioginį pristatymą Patvirtinto produkto pagrindiniame rodinyje, nustatydami tiesioginio pristatymo pasirinktį į Taip ir pasirinkę numatytąjį Tiesioginio pristatymo sandėlį.  
    * Kadangi dar nesukurtas pirkimo užsakymas, Tiesioginio pristatymo būsena nustatyta į Turi būti pristatyta tiesiogiai.   
11. Uždarykite puslapį.
12. Uždarykite puslapį.
13. Eikite į Tiesioginis pristatymas.
    * Tiesioginio pristatymo puslapis veikia kaip darbastalis, teikiantis pirkimo agentui visų pardavimo užsakymo eilučių, kurios turi būti tiesiogiai pristatytos, apžvalgą ir tai leidžia jiems kurti atitinkamus pirkimo užsakymus. Be to, jie gali peržiūrėti atidarytus tiesioginio pristatymo užsakymus ir patvirtintus užsakymus skirtukuose Patvirtinimas ir Pristatymas.   
14. Spustelėkite Kurti tiesioginį pristatymą.
15. Spustelėkite skirtuką Patvirtinimas.
    * Sukūrus tiesioginio pristatymo užsakymą, jis automatiškai perkeliamas į skirtuką Patvirtinimas. Galite patvirtinti užsakymą tiesiogiai iš šio puslapio. Kai pirkimas patvirtintas, jis bus automatiškai perkeltas į skirtuką Pristatymas, iš kurio galite registruoti jo gavimą.  


