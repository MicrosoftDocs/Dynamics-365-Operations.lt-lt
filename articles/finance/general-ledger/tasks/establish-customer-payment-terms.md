---
title: Nustatyti kliento mokėjimo sąlygas
description: Ši procedūra apibrėžia mokėjimo nuolaidą ir termino sąranką.
author: aprilolson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6069d28d84ab1705fd62a33cea7e0b923f0e0705
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065715"
---
# <a name="establish-customer-payment-terms"></a>Nustatyti kliento mokėjimo sąlygas

[!include [banner](../../includes/banner.md)]

Ši procedūra apibrėžia mokėjimo nuolaidą ir termino sąranką. Šiame užduočių vadove naudojama demonstracinė įmonė USMF.

1. Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Mokėjimų sąranka > Mokėjimo dienos**. **Mokėjimo sąlygų** sąranka bendrinama su **Gautinos sumos** ir **Mokėtinos sumos**. Jei ją nurodysite modulyje, ji bus prieinama ir kitame modulyje. Šiame užduoties vadove nustatytos visos gautinų sumų **mokėjimo** sąlygos.
2. Spustelėkite **Naujas**. Sukurkite mokėjimo dieną, jeigu mokėjimo sąlygose reikalaujama konkrečios savaitės dienos (pirmadienio, antradienio ir t. t) arba konkrečios mėnesio dienos (5 d., 10 d., ir t. t). 
3. Lauke **Mokėjimo diena** įveskite ID.
4. Lauke **Aprašas** įveskite mokėjimų dienos aprašą.
5. Lauke **Savaitė/mėnuo** pasirinkite „Savaitė“ arba „Mėnuo“'. Jei norite įvesti savaitės dieną, pvz., pirmadienį, pasirinkite Savaitė. Jei norite įvesti mėnesio dieną, pvz., 10 d., pasirinkite Mėnuo. Šiame pavyzdyje pasirinkite Mėnuo. 
6. Lauke **Mėnesio diena** įveskite datą. Dieną reikėtų įvesti kaip skaičių, pvz., „10‟, o ne kaip „10 d.‟. 
7. Spustelėkite **Įrašyti**.
8. Uždarykite puslapį.
9. Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Mokėjimų sąranka > Mokėjimo sąlygos**.
10. Spustelėkite **Naujas**. **Mokėjimo sąlygos** naudojamos apibrėžti, kaip bus skaičiuojami terminai. Mokėjimo nuolaidos datos sąranka apibrėžiama atskirame puslapyje. 
11. Lauke **Mokėjimo sąlygos** įveskite ID.
12. Lauke **Aprašas** įveskite aprašą.
13. Pasirinkite mokėjimo būdą **, pvz** ., **COD**, **Net**, šį **mėnesį ir** t. t. Mokėjimo **būdas** naudojamas apibrėžti termino skaičiavimo pradžios nurodymą. Pavyzdžiui, grynasis **naudojamas**, jei terminas visada yra nustatytas mėnesių skaičius arba dienų skaičius po SF datos. **COD** gali būti naudojamas, kai apmokėjimas būtinas SF, todėl termino datos apskaičiuoti negalima. Pasirinkite **šį šio užduočių** vadovo mėnesį.  
14. Pasirinkite **Mokėjimo diena**, jei skaičiuojant įtraukiama konkreti savaitės diena ar data. Atsižvelgiant į mokėjimo sąlygas, kiekį galite įvesti mėnesiais arba dienomis. Arba mokėjimo grafiką arba mokėjimo dieną galite naudoti norėdami pridėti prie mokėjimo būdo **pabaigos**.**·** **·** Jei terminas visada bus kito mėnesio 10 d., pasirinkite 10 **mokėjimo dieną**. Jei naudojate mokėjimo **kalendorių**, galite nurodyti, kaip terminas nustatomas, kai apskaičiuota data nusileido ne darbo dienai. Pradinis terminas skaičiuojamas naudojant kalendorines dienas. Jei apskaičiuota data nusileido ne darbo dienai, apskaičiuotą terminą galite koreguoti pagal kitą darbo dieną arba pagal ankstesnę darbo dieną.
15. Spustelėkite **Įrašyti**.
16. Uždarykite puslapį.
17. Eikite į **Gautinos sumos > Mokėjimų sąranka > Mokėjimo nuolaidos**.
18. Spustelėkite **Naujas**. Šis puslapis naudojamas apibrėžti, kaip bus skaičiuojama mokėjimo nuolaidos data. 
19. Lauke **Mokėjimo nuolaida** įveskite ID.
20. Lauke **Aprašas** įveskite aprašą.
21. Jei galima pakopinė mokėjimo nuolaida, pasirinkite **kitą nuolaidos kodą**, kuris yra aktualus po šios naujos mokėjimo nuolaidos.
22. Lauke **Dienos** įveskite dienų, naudojamų skaičiuoti mokėjimo nuolaidos datai, skaičių. Jei pasirinktas **Grynasis** principas, norint apskaičiuoti mokėjimo nuolaidos datą, dienų skaičius bus pridėtas prie SF datos.  
23. Lauke **Nuolaida procentais** įveskite mokėjimo nuolaidos procentą.
24. **Pagrindinė sąskaita, skirta kliento nuolaidoms** įveskite pagrindinę sąskaitą, kuri bus naudojama pateikiant kliento SF su mokėjimo nuolaida.
25. Lauke **Taikyti nuolaidą korespondentinėms sąskaitoms** pasirinkite parinktį. Jei pasirinksite „Sąskaitos SF eilutėse‟, mokėjimo nuolaida bus registruojama toje pačioje turto / išlaidų pagrindinėje sąskaitoje, esančioje tiekėjo SF eilutėse. Jei pasirenkate **tiekėjo SF naudoti pagrindinę** sąskaitą, mokėjimo nuolaida bus užregistruojant pagrindinėje sąskaitoje, **kurią nurodote tiekėjo SF pagrindinėje sąskaitoje**. Šiame pavyzdyje pasirinkite **Naudoti pagrindinę sąskaitą tiekėjo SF**. 
26. Lauke **Pagrindinė sąskaita, skirta tiekėjo nuolaidoms** įveskite pagrindinę sąskaitą, kuri bus naudojama pateikiant tiekėjo SF su mokėjimo nuolaida.
27. Spustelėkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
