--- 
title: "Garantinio rašto operacija"
description: "Ši procedūra padeda apdoroti garantinius raštus."
author: kweekley
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c2e215f1ae16f907c8b64ea1f05cf67bfb0a04b6
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="letter-of-guarantee-transaction"></a>Garantinio rašto operacija

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padeda apdoroti garantinius raštus.



Prieš baigdami šitą procedūrą, turite įvykdyti toliau nurodytas užduotis:

- Nustatyti garantinio rašto banko priemones ir registravimo šablonus.

- Kurti garantinio rašto banko priemonės sutartį.



Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Kurti pardavimo užsakymą su garantiniu raštu
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
4. Išplėskite skyrių Bendra.
5. Lauke Teritorija įveskite arba pasirinkite reikšmę.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke Banko dokumento tipas pasirinkite „Garantinis raštas“.
10. Spustelėkite Gerai.
11. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
12. Lauke Vieneto kaina įveskite skaičių.
13. Išplėskite skyrių Eilutės informacija.
14. Spustelėkite skirtuką Pristatymas.
    * Pastaba: pristatymo datos valdymo pasirinkimas = nėra  
15. Lauke Pageidaujama siuntimo data įveskite datą.
16. Lauke Patvirtinta siuntimo data įveskite datą.

## <a name="process-letter-of-guaranteerequest"></a>Apdoroti garantinį raštą Užklausa
1. Veiksmų srityje spustelėkite Valdyti.
2. Spustelėkite Garantinis raštas.
3. Veiksmų srityje spustelėkite Garantinis raštas.
4. Spustelėdami Užklausa atidarykite išplečiamąjį dialogo langą.
5. Lauke Tipas įveskite arba pasirinkite reikšmę.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Lauke Vertė įveskite skaičių.
8. Lauke Galiojimo data įveskite datą ir laiką.
9. Spustelėkite GERAI.
10. Uždarykite puslapį.

## <a name="process-letter-of-guaranteesubmit-to-bank"></a>Apdoroti garantinį raštą Pateikti bankui
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Spustelėdami Pateikti bankui atidarykite išplečiamąjį dialogo langą.
4. Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite GERAI.

## <a name="process-letter-of-guaranteereceive-from-bank"></a>Apdoroti garantinį raštą Gauti iš banko
1. Spustelėdami Gauti iš banko, atidarykite išplečiamąjį dialogo langą.
2. Lauke Banko numeris įveskite reikšmę.
    * Patikrinkite apskaičiuotų laukų Marža ir Išlaidos reikšmes.  
3. Spustelėkite GERAI.
4. Išplėskite sekciją Veiksmai.
    * Patikrinkite įrašą „Gauti iš banko“.  
5. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.
6. Spustelėkite Eilutės.
    * Patikrinkite žurnalo įrašų registravimą.  
7. Uždarykite puslapį.

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a>Apdoroti garantinį raštą Duoti gavėjui
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Veiksmų srityje spustelėkite Valdyti.
4. Spustelėkite Garantinis raštas.
5. Veiksmų srityje spustelėkite Garantinis raštas.
6. Spustelėdami Duoti gavėjui, atidarykite išplečiamąjį dialogo langą.
7. Spustelėkite GERAI.
8. Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Spustelėdami Duoti gavėjui, atidarykite išplečiamąjį dialogo langą.
11. Spustelėkite GERAI.
12. Išplėskite sekciją Veiksmai.
    * Patikrinkite įrašą „Duoti gavėjui“.  

## <a name="process-letter-of-guaranteeincrease-value"></a>Apdoroti garantinį raštą Didinti vertę
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Veiksmų srityje spustelėkite Valdyti.
4. Spustelėkite Garantinis raštas.
5. Veiksmų srityje spustelėkite Garantinis raštas.
6. Spustelėdami Didinti vertę, atidarykite išplečiamąjį dialogo langą.
7. Lauke Įtrauktina vertė įveskite skaičių.
8. Spustelėkite GERAI.
9. Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.
10. Sąraše raskite ir pasirinkite norimą įrašą.
11. Spustelėdami Didinti vertę, atidarykite išplečiamąjį dialogo langą.
12. Spustelėkite GERAI.
13. Išplėskite sekciją Veiksmai.
    * Patikrinkite įrašą „Didinti vertę“.  
14. Sąraše raskite ir pasirinkite norimą įrašą.
15. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.
16. Spustelėkite Eilutės.
    * Patikrinkite užregistruotus žurnalo įrašus.  

## <a name="process-letter-of-guaranteeliquidate"></a>Apdoroti garantinį raštą Likviduoti
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Sąraše spustelėkite saitą pasirinktoje eilutėje.
3. Veiksmų srityje spustelėkite Valdyti.
4. Spustelėkite Garantinis raštas.
5. Veiksmų srityje spustelėkite Garantinis raštas.
6. Spustelėdami Likviduoti, atidarykite išplečiamąjį dialogo langą.
7. Spustelėkite GERAI.
8. Pasirinkite Grynųjų pinigų ir banko valdymas > Garantiniai raštai > Garantiniai raštai.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Spustelėdami Likviduoti, atidarykite išplečiamąjį dialogo langą.
11. Spustelėkite GERAI.
12. Išplėskite sekciją Veiksmai.
    * Patikrinkite įrašą „Likviduoti“.  
13. Sąraše raskite ir pasirinkite norimą įrašą.
14. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Žurnalo paketo numeris.
15. Spustelėkite Eilutės.
    * Patikrinkite užregistruotus žurnalo įrašus.  
16. Uždarykite puslapį.


