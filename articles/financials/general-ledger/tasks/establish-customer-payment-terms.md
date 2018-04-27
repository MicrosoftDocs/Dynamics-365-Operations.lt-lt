--- 
title: "Nustatyti kliento mokėjimo sąlygas"
description: "Ši procedūra apibrėžia mokėjimo nuolaidą ir termino sąranką."
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 04b45508047d26ef7c08ede5862be75835783ef5
ms.contentlocale: lt-lt
ms.lasthandoff: 10/26/2017

---
# <a name="establish-customer-payment-terms"></a>Nustatyti kliento mokėjimo sąlygas

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra apibrėžia mokėjimo nuolaidą ir termino sąranką. Šiame užduočių vadove naudojama demonstracinė įmonė USMF.

1. Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų dienos.
    * Mokėjimo sąlygų sąranka bendrinama su gautinomis sumomis ir mokėtinomis sumomis. Jei ją nurodysite modulyje, ji bus prieinama ir kitame modulyje. Šiame užduočių vadove visas mokėjimo sąlygas nustatau srityje Gautinos sumos.  
2. Spustelėkite Naujas.
    * Sukurkite mokėjimo dieną, jeigu mokėjimo sąlygose reikalaujama konkrečios savaitės dienos (pirmadienio, antradienio ir t. t) arba konkrečios mėnesio dienos (5 d., 10 d., ir t. t).  
3. Lauke Mokėjimų diena įveskite mokėjimo dienos, nurodytos mokėjimo dienos lauke, ID.
4. Lauke Aprašas įveskite mokėjimų dienos aprašą.
5. Lauke Savaitė / Mėnuo pasirinkite arba Savaitė, arba Mėnuo.
    * Jei norite įvesti savaitės dieną, pvz., pirmadienį, pasirinkite Savaitė. Jei norite įvesti mėnesio dieną, pvz., 10 d., pasirinkite Mėnuo. Šiame pavyzdyje pasirinkite Mėnuo.  
6. Lauke Mėnesio diena įveskite datą.
    * Dieną reikėtų įvesti kaip skaičių, pvz., „10‟, o ne kaip „10 d.‟.  
7. Spustelėkite Įrašyti.
8. Uždarykite puslapį.
9. Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo sąlygos.
10. Spustelėkite Naujas.
    * Mokėjimo sąlygos naudojamos apibrėžti, kaip bus skaičiuojami terminai. Mokėjimo nuolaidos datos sąranka apibrėžiama atskirame puslapyje.  
11. Lauke Mokėjimo sąlygos įveskite ID, esantį lauke Mokėjimo sąlygos.
12. Lauke Aprašas įveskite aprašą.
13. Pasirinkite mokėjimo būdą, pvz., COD, Grynasis, Dabartinis mėnuo ir t. t.
    * Mokėjimo būdas naudojamas apibrėžti, kaip bus pradedami skaičiuoti terminai.  Pvz., Grynasis naudojamas, jei terminas visada yra nustatytas mėnesių ar dienų skaičius po SF datos. COD galima naudoti, kai mokėti reikia gavus SF, todėl terminas nebūtų skaičiuojamas. Pasirinkite Dabartinis mėnuo, kuris bus naudojamas šiame užduočių vadove.  
14. Pasirinkite mokėjimo dieną, jei skaičiuojant įtraukiama konkreti savaitės diena ar data.
    * Atsižvelgiant į mokėjimo sąlygas, kiekį galite įvesti mėnesiais arba dienomis. Arba galite naudoti mokėjimų grafiką ar mokėjimo dieną, kuriuos „pridėtumėte‟ prie mokėjimo būdo pabaigos. Jei terminas visada bus kito mėnesio 10 d., mokėjimo dieną pasirinkite 10 d.  
15. Spustelėkite Įrašyti.
16. Uždarykite puslapį.
17. Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimo nuolaidos.
18. Spustelėkite Naujas.
    * Šis puslapis naudojamas apibrėžti, kaip bus skaičiuojama mokėjimo nuolaidos data.  
19. Lauke Mokėjimo nuolaida įveskite ID, esantį lauke Mokėjimo nuolaida.
20. Lauke Aprašas įveskite aprašą.
21. Jei galima pakopinė mokėjimo nuolaida, pasirinkite kitą nuolaidos kodą, kuris yra aktualus po šios naujos mokėjimo nuolaidos.
22. Įveskite dienų, naudojamų skaičiuoti mokėjimo nuolaidos datai, skaičių.
    * Jei pasirinktas grynasis principas, norint apskaičiuoti mokėjimo nuolaidos datą, dienų skaičius bus pridėtas prie SF datos.  
23. Įveskite mokėjimo nuolaidos procentą.
24. Įveskite pagrindinę sąskaitą, kurioje bus registruojama klientų SF mokėjimo nuolaida.
25. Lauke Taikyti nuolaidą korespondentinėms sąskaitoms pasirinkite parinktį.
    * Jei pasirinksite „Sąskaitos SF eilutėse‟, mokėjimo nuolaida bus registruojama toje pačioje turto / išlaidų pagrindinėje sąskaitoje, esančioje tiekėjo SF eilutėse. Jei pasirinksite „Tiekėjo SF naudoti pagrindinę sąskaitą‟, mokėjimo nuolaida bus registruojama pagrindinėje sąskaitoje, apibrėžtoje srityje „Pagrindinė tiekėjų SF sąskaita‟. Šiame pavyzdyje pasirinkite „Tiekėjų SF naudoti pagrindinę sąskaitą‟.  
26. Įveskite pagrindinę sąskaitą, kurioje bus registruojama tiekėjų SF mokėjimo nuolaida.
27. Spustelėkite Įrašyti.


