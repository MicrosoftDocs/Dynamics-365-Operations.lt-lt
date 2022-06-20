---
title: Tiekėjo mokėjimo sąlygų apibrėžimas
description: Šiame straipsnyje paaiškinama, kaip nustatyti tiekėjo SF mokėjimo sąlygas.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a676856ed43bf1b78684eac0682e0fdef9c84083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906477"
---
# <a name="define-vendor-payment-terms"></a>Tiekėjo mokėjimo sąlygų apibrėžimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti tiekėjo SF mokėjimo sąlygas. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite **Naršymo sritis > Moduliai > Mokėtinos sumos > Mokėjimo konfigūracija > Mokėjimo sąlygos**.
2. Pasirinkite **Naujas**. Mokėjimo **sąlygų puslapis** naudojamas nurodyti, kaip bus skaičiuojamas terminas. Ji nenaudojamas apibrėžti, kaip bus skaičiuojama mokėjimo nuolaidos data.  
3. Lauke **Mokėjimo sąlygos** surinkite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke **Dienos** įveskite skaičių. Čia įvestas numeris bus naudojamas pridėti prie termino arba prie laikotarpio pabaigos, nurodytos mokėjimo **metode**. Pvz., pasirinkus **Grynoji**, skaičius bus pridėtas prie termino. Jei pasirinksite **Dabartinis mėnesis**, skaičius bus pridedamas prie dabartinio mėnesio paskutinės dienos, kad būtų apskaičiuota termino pabaigos data.  
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį.
8. Pasirinkit **Mokėtinos sumos > Mokėjimo konfigūracija > Mokėjimo nuolaida**.
9. Pasirinkite **Naujas**.
10. Lauke **Mokėjimo nuolaida** įveskite ID.
11. Lauke **Aprašymas įveskite** surinkite reikšmę.
12. Jei tiekėjas siūlo pakopinę nuolaidą, baigus galioti dabartinei nuolaidai, pasirinkite kitą mokėjimo nuolaidą.
13. Uždarykite puslapį.
14. Lauke **Dienos** įveskite skaičių. Lauke Dienos įvestas kiekis **bus** **naudojamas** mokėjimo nuolaidos datai skaičiuoti, remiantis tuo, **kokia pasirinktis pasirinkta lauke Net/Current**. Jei buvo pasirinkta **Grynoji**, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie SF datos. Jei buvo pasirinktas **Dabartinis mėnesis**, norint nustatyti mokėjimo nuolaidos datą, kiekis bus pridėtas prie dabartinio mėnesio pabaigos.  
15. Lauke **Nuolaida** įveskite mokėjimo nuolaidos procentą. 
16. Įveskite pagrindinę sąskaitą, į kurią bus registruojamos kliento SF taikoma mokėjimo nuolaida, tada įveskite pagrindinę sąskaitą, į kurią bus registruojamos tiekėjo SF taikoma mokėjimo nuolaida. Jei **Taikyti nuolaidą korespondentinėms sąskaitoms** nustatyta kaip **Naudoti pagrindinę sąskaitą, skirtą tiekėjo nuolaidoms**, bus naudojama pagrindinė sąskaita. Jei parinktis nustatyta į **Sąskaitos faktūros eilutėse esančios sąskaitos**, mokėjimo nuolaida bus registruojama turto / išlaidų sąskaitose, esančiose SF eilutėse.  
17. Pasirinkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
