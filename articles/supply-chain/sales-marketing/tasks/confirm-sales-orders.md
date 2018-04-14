--- 
title: "Patvirtinti pardavimo užsakymus"
description: "Ši procedūra parodo, kaip patvirtinti pardavimo užsakymus."
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="confirm-sales-orders"></a>Patvirtinti pardavimo užsakymus

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip patvirtinti pardavimo užsakymus. Jums bus parodyta, kaip patvirtinti vieną užsakymą, ir kaip patvirtinti kelis užsakymus vienu kartu. Šias užduotis paprastai atlieka pardavimo užsakymų tvarkytojas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis. Prieš pradėdami įsitikinkite, kad yra keletas atvirų to paties kliento pardavimo užsakymų. Jei naudojate USMF, galite naudoti klientą US-027.


## <a name="confirm-a-single-sales-order"></a>Patvirtinti vieną pardavimo užsakymą
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
2. Sąraše raskite ir pasirinkite užsakymą, kurį norite patvirtinti.
3. Spustelėkite pardavimo užsakymo numerio nuorodą, kad atidarytumėte pasirinktą užsakymą.
4. Veiksmų srityje spustelėkite Parduoti.
5. Spustelėkite „Patvirtinti pardavimo užsakymą“.
6. Išplėskite arba sutraukite skyrių Parametrai.
    * Įsitikinkite, kad aktyvintas registravimo laukas „Taip“.  
7. Nustatykite spausdinimo patvirtinimo parinktį „Taip“.
    * Lauke „Patikrinti kredito limitą“ nurodomas metodas, naudojamas skaičiuojant kliento kredito likutį. Jis numatytuoju būdu kopijuojamas iš puslapio „Gautinų sumų parametrai“. Jei norite praleisti kredito limito tikrinimą, kai tvirtinate konkretų pardavimo užsakymą, nustatykite „Patikrinti kredito limitą“ reikšmę „Nėra“. Tačiau visada reikėtų žinoti, kad net ir nustačius šiam laukui reikšmę „Nėra“, kredito limitas vis tiek bus tikrinamas, jei kliento bendruosiuose duomenyse bus pasirinkta parinktis „Privalomas kredito limitas“.  
8. Spustelėkite GERAI.
9. Spustelėkite Taip.
10. Uždarykite puslapį.
11. Veiksmų srityje spustelėkite Parinktys.
12. Spustelėkite Keisti rodinį.
13. Spustelėkite antraštės rodinį.
    * Kai užsakymas patvirtinamas, dokumento būsena pakeičiama į „Patvirtinimas“.  
14. Veiksmų srityje spustelėkite Parduoti.
15. Spustelėkite „Pardavimo užsakymo patvirtinimas“.
16. Uždarykite puslapį.

## <a name="confirm-multiple-sales-orders-at-once"></a>Patvirtinti keletą pardavimo užsakymų vienu kartu
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Užsakymo patvirtinimas > Patvirtinti pardavimo užsakymą.
2. Spustelėkite Pažymėti.
3. Skirtuko „Diapazonas“ sąraše pasirinkite įrašą su nuoroda į lauką „Kliento sąskaitą“.
4. Lauke Kriterijai spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše raskite ir pasirinkite kliento sąskaitą, turinčią keletą užsakymų, kuriuos norite masiškai patvirtinti.
    * Jei naudojate USMF, galite pasirinkti sąskaitą US-027.  
6. Spustelėkite GERAI.
    * Skirtuke „Apžvalga“ rodomas užsakymų, kurie atitinka užklausos kriterijus, sąrašas. Jie bus įtraukti į patvirtinimą.  
    * Lauke „Suvestinės atnaujinimas“ rodomas parametras, pagal kurį reikia suvesti keletą užsakymų į vieną patvirtinimo dokumentą. Pagal numatytuosius nustatymus parinktis kopijuojama iš nustatymo „Suvestinio atnaujinimo numatytosios reikšmės“, esančio puslapyje „Mokėtinų sumų parametrai“.  
7. Lauke „Suminis atnaujinimas“ pasirinkite „Užsakymas“.
    * Norint sukurti suminį atnaujinimą, būtini parametrai SF sąskaita ir valiuta. Tai reiškia, kad neleidžiama atlikti suminių atnaujinimų, kurių SF sąskaitos ir valiutos skirtingos. Papildomus parametrus galima nustatyti puslapyje „Suminio atnaujinimo parametrai“, kurį galima pasiekti iš puslapio „Gautinų sumų parametrai“.  
8. Lauke „Pardavimo užsakymas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše pasirinkite numerį užsakymo, kurį norite padaryti suminiu užsakymu.
10. Spustelėkite „Išdėstyti“.
11. Spustelėkite GERAI.
12. Spustelėkite GERAI.


