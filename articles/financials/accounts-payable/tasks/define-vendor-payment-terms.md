---
title: Nustatyti tiekėjo mokėjimo sąlygas
description: Nustatykite tiekėjų SF mokėjimo sąlygas.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68c69d5be5ccbdfb17fea7c61121cbf26fee48d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569037"
---
# <a name="define-vendor-payment-terms"></a>Nustatyti tiekėjo mokėjimo sąlygas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nustatykite tiekėjų SF mokėjimo sąlygas. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo sąlygos.
2. Spustelėkite Naujas.
    * Mokėjimo sąlygų puslapis naudojamas apibrėžti, kaip bus skaičiuojamas terminas. Ji nenaudojamas apibrėžti, kaip bus skaičiuojama mokėjimo nuolaidos data.  
3. Lauke Mokėjimo sąlygos surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Dienos įveskite skaičių.
    * Čia įvestas skaičius bus pridedamas prie termino arba prie laikotarpio, nurodyto srityje Mokėjimo būdas. Pvz., pasirinkus Grynasis, skaičius bus pridėtas prie termino. Jei pasirinksite Dabartinis mėnuo, skaičius bus pridedamas prie dabartinio mėnesio paskutinės dienos, kad būtų apskaičiuota termino pabaigos data.  
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.
8. Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo nuolaidos.
9. Spustelėkite Naujas.
10. Lauke Mokėjimo nuolaida įveskite ID.
11. Lauke Aprašas įveskite reikšmę.
12. Jei tiekėjas siūlo pakopinę nuolaidą, baigus galioti dabartinei nuolaidai, pasirinkite kitą mokėjimo nuolaidą.
13. Uždarykite puslapį.
14. Lauke Dienos įveskite skaičių.
    * Kiekis, įvestas lauke Dienos, pagal tai, kokia parinktis buvo pasirinkta lauke Grynasis / dabartinis, bus naudojamas skaičiuoti mokėjimo nuolaidos datai. Jei buvo pasirinktas Grynasis, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie SF datos. Jei buvo pasirinktas Dabartinis mėnuo, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie dabartinio mėnesio pabaigos.  
15. Lauke Nuolaida įveskite mokėjimo nuolaidos procentą. 
16. Įveskite pagrindinę sąskaitą, kurioje bus registruojama klientų SF mokėjimo nuolaida.
17. Įveskite pagrindinę sąskaitą, kurioje bus registruojama tiekėjų SF mokėjimo nuolaida.
    * Jei srityje Taikyti nuolaidą korespondentinėms sąskaitoms nustatyta Tiekėjo SF naudoti pagrindinę sąskaitą, bus naudojama pagrindinė sąskaita.  Jei parinktis nustatyta į Sąskaitos SF eilutėse, mokėjimo nuolaida bus registruojama turto / išlaidų sąskaitose, esančiose SF eilutėse.  
18. Spustelėkite Įrašyti.

