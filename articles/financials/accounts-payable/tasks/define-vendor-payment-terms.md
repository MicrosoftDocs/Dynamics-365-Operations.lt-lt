---
title: Tiekėjo mokėjimo sąlygų apibrėžimas
description: Šioje temoje aiškinama kaip nustatyti tiekėjo SF mokėjimo sąlygas.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6432d04aa821e76d67e2c430e514f4b9056d8228
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843199"
---
# <a name="define-vendor-payment-terms"></a>Tiekėjo mokėjimo sąlygų apibrėžimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje aiškinama kaip nustatyti tiekėjo SF mokėjimo sąlygas. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite **Naršymo sritis > Moduliai > Mokėtinos sumos > Mokėjimo konfigūracija > Mokėjimo sąlygos**.
2. Pasirinkite **Naujas**. Mokėjimo sąlygų puslapis naudojamas apibrėžti, kaip bus skaičiuojamas terminas. Ji nenaudojamas apibrėžti, kaip bus skaičiuojama mokėjimo nuolaidos data.  
3. Lauke **Terms of payment** surinkite reikšmę.
4. Lauke **Description field**surinkite reikšmę.
5. Lauke **Days** įveskite skaičių. Čia įvestas skaičius bus pridedamas prie termino arba prie laikotarpio, nurodyto srityje Mokėjimo būdas. Pvz., pasirinkus **Net**, skaičius bus pridėtas prie termino. Jei pasirinksite **Current month**, skaičius bus pridedamas prie dabartinio mėnesio paskutinės dienos, kad būtų apskaičiuota termino pabaigos data.  
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį.
8. Pasirinkit **Accounts payable > Payment setup > Cash discounts**.
9. Pasirinkite **Naujas**.
10. Lauke **Cash discount** įveskite ID.
11. Lauke **Description field**surinkite reikšmę.
12. Jei tiekėjas siūlo pakopinę nuolaidą, baigus galioti dabartinei nuolaidai, pasirinkite kitą mokėjimo nuolaidą.
13. Uždarykite puslapį.
14. Lauke **Days** įveskite skaičių. Kiekis, įvestas lauke **Days**, pagal tai, kokia parinktis buvo pasirinkta lauke **Net/Current**, bus naudojamas skaičiuoti mokėjimo nuolaidos datai. Jei buvo pasirinktas **Net**, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie SF datos. Jei buvo pasirinktas **Current month**, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie dabartinio mėnesio pabaigos.  
15. Lauke **Discount** įveskite mokėjimo nuolaidos procentą. 
16. Įveskite pagrindinę sąskaitą, į kurią bus registruojamos kliento SF taikoma mokėjimo nuolaida, tada įveskite pagrindinę sąskaitą, į kurią bus registruojamos tiekėjo SF taikoma mokėjimo nuolaida. Jei srityje **Discount offset accounts** nustatyta **Use main account for vendor discount**, bus naudojama pagrindinė sąskaita. Jei parinktis nustatyta į **Accounts on the invoice lines**, mokėjimo nuolaida bus registruojama turto / išlaidų sąskaitose, esančiose SF eilutėse.  
17. Pasirinkite **Įrašyti**.

