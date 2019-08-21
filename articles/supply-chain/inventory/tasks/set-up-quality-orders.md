---
title: Nustatyti kokybės užsakymus
description: Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos.
author: perlynne
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0119ae07e490f048dbb021983e25889cb1cb42b3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845359"
---
# <a name="set-up-quality-orders"></a>Nustatyti kokybės užsakymus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos. Procedūrą paprastai atlieka kokybės vadovas. Šis procesas apima kokybės grupės kūrimą apibrėžti prekėms, iš kurių bus imami pavyzdžiai, ir bandymo grupės kūrimą grupuoti bandymams, kuriuos reikia atlikti su prekėmis kokybės grupėje. Šį vedlį galite vykdyti demonstracinių duomenų įmonėje USMF.


## <a name="enable-quality-management"></a>Kokybės valdymo įgalinimas
1. Eikite į **Valdymo skiltį > Moduliai > Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai**.
2. Spustelėkite skirtuką **Quality management** tab.
3. Nustatykite **Use quality management option** reikšmę Taip.
4. Spustelėkit **Report setup**. USMF kokybės valdymo ataskaitos sąranka jau yra nurodyta. Jei tai buvo atlikta, čia galite įtraukti naujas skirtingų ataskaitų tipų eilutes ir pasirinkti kiekvienos ataskaitos dokumento tipą.  
5. Uždarykite puslapį.
6. Uždarykite puslapį.

## <a name="create-a-test"></a>Kurti bandymą
1. Pasirinkite **Inventory management > Setup > Quality control > Tests**.
2. Spustelėkite **Naujas**.
3. Lauke **Test** surinkite reikšmę.
4. Lauke **Description field**surinkite reikšmę.
5. Lauke **Type** pasirinkite „Parinktis‟. Šiame pavyzdyje pasirinksime „Parinktis‟ – bus galima priskirti tikrinimo rezultatus pagal iš anksto apibrėžtas reikšmes.  
6. Spustelėkite **Įrašyti**.
7. Uždarykite puslapį.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Kurti bandymų kintamuosius, kad būtų galima apibrėžti, kaip įrašomi bandymų rezultatai
1. Pasirinkit **Inventory management > Setup > Quality control > Test variables**.
2. Spustelėkite **Naujas**.
3. Lauke **Variable** surinkite reikšmę.
4. Lauke **Description field**surinkite reikšmę.
5. Spustelėkite **Įrašyti**.
6. Spustelėkite **Outcomes**.
7. Spustelėkite **Naujas**.
8. Lauke **Outcome** surinkite reikšmę.
9. Lauke **Description field**surinkite reikšmę.
10. Lauke **Outcome status** pasirinkite „Sėkmingai‟.
11. Spustelėkite **Įrašyti**.
12. Spustelėkite **Naujas**.
13. Lauke **Outcome** surinkite reikšmę.
14. Lauke **Description field**surinkite reikšmę.
15. Spustelėkite **Įrašyti**.
16. Uždarykite puslapį.
17. Uždarykite puslapį.

## <a name="set-up-item-sampling"></a>Nustatyti prekių pavyzdžių ėmimą
1. Pasirinkit **Inventory management > Setup > Quality control > Item sampling**.
2. Spustelėkite **Naujas**.
3. Lauke **Item sampling**surinkite reikšmę.
4. Lauke **Description field**surinkite reikšmę.
5. Lauke **Value** įveskite skaičių. Ši reikšmė susijusi su kiekio specifikacija, pasirinkta gretimame lauke.  
6. Išplėskite arba sutraukite sekciją **Process** section.
7. Pažymėkite arba panaikinkite žymės langelio **Full blocking** žymėjimą. Jei pasirenkate šią parinktį ir jei tikrinti nepavyksta, užblokuojama visa partija ar užsakymo eilutės kiekis. Jei jos nepasirenkate, blokuojamos tik kokybės užsakymo prekės.  
8. Spustelėkite **Įrašyti**.
9. Uždarykite puslapį.

## <a name="create-a-quality-group"></a>Kurti kokybės grupę
1. Pasirinkit **Inventory management > Setup > Quality control > Quality groups**.
2. Spustelėkite **Naujas**.
3. Lauke **Quality group** surinkite reikšmę. Naudokite aprašomąjį pavadinimą, kad būtų lengviau identifikuoti, kokios rūšies prekės bus grupėje (pavyzdžių ėmimo kriterijai).  
4. Lauke **Description field**surinkite reikšmę.
5. Spustelėkite **Įrašyti**.
6. Spustelėkite **Įtraukti prekes**.
7. Pasirinkti eilutę **Item number**. Šiame pavyzdyje filtravimas bus vykdomas pagal prekės numerį.  
8. Lauke **Criteria**surinkite reikšmę. Pavyzdžiui, įveskite T*, kad filtruotumėte tuos prekių numerius, kurie prasideda T.  
9. Spustelėkite **Gerai**.
10. Spustelėkite **Gerai**.
11. Spustelėkit **Item quality groups**.
12. Uždarykite puslapį.
13. Uždarykite puslapį.

## <a name="create-a-test-group"></a>Kurti bandymų grupę
1. Pasirinkite **Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymų grupės**.
2. Spustelėkite **Naujas**.
3. Lauke **Test group** surinkite reikšmę. Suteikite **Test group** pavadinimą, kuris padės prisiminti, kokie bandymai vykdomi ir su kuria kokybės grupe ji turėtų būti susieta. Pavyzdžiui, jei ji bus naudojama su kokybės grupe, kuri pasirenka prekes, prasidedančias „T‟, galite ją pavadinti „T prekių bandymai‟.  
4. Lauke **Description field**surinkite reikšmę.
5. Lauke **Item sampling** pasirinkite prekių pavyzdžių ėmimo eilutę, kurią sukūrėte anksčiau.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Spustelėkite **Pridėti**.
8. Lauke **Sequence number**įveskite skaičių.
9. Lauke **Test** pasirinkite bandymą, kurį sukūrėte anksčiau.
10. Sąraše raskite ir pasirinkite norimą įrašą.
11. Spustelėkite skirtuką **Tikrinti**.
12. Lauke **Variable** pasirinkite bandymo kintamąjį, kurį sukūrėte prieš tai.
13. Sąraše raskite ir pasirinkite norimą įrašą.
14. Lauke **Default outcome** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
15. Sąraše spustelėkite saitą pasirinktoje eilutėje.
16. Spustelėkite **Įrašyti**.
17. Uždarykite puslapį.

## <a name="define-when-quality-orders-will-be-created"></a>Apibrėžti, kada bus kuriami kokybės užsakymai
1. Pasirinkit **Inventory management > Setup > Quality control > Quality associations**.
2. Spustelėkite **Naujas**.
3. Lauke **Reference type**pasirinkite parinktį.
4. Lauke **Item code** pasirinkite „Grupė‟. Šiame pavyzdyje pasirinksime „Grupė‟ ir naudosime anksčiau savo sukurtą kokybės grupę. Taip pat galite nustatyti „Lentelė‟, kad prekes nurodytumėte rankiniu būdu, arba pasirinkti „Visi‟, kad visos prekės būtų pridėtos į kokybės užsakymą.  
5. Lauke **Item** pasirinkite kokybės grupę, kurią sukūrėte prieš tai. Galimos parinktys lauke Prekė priklauso nuo to, ką nustatote lauke Prekės kodas.  
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Išplėskite arba sutraukite sekciją Procesas.
8. Lauke **Event type** pasirinkite parinktį. Tai yra įvykis, kuris suaktyvina bandymą. Čia galimos parinktys priklauso nuo to, kokį procesą pasirinkote lauke Nuorodos tipas.  
9. Lauke **Execution**pasirinkite parinktį.
10. Išplėskite arba sutraukite **Quality order process** sekcijąf
11. Lauke **Event blocking** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Šiame lauke rodomas procesų, kuriuos galima blokuoti, jei kokybės užsakymas vis dar atidarytas, sąrašas. Parinktys priklauso nuo to, ką pasirinkote lauke Įvykio tipas.  
12. Sąraše spustelėkite saitą pasirinktoje eilutėje. Tai priklausys nuo ankstesnių pasirinktų reikšmių. Pasirinkite, are reikia blokuoti šiuos procesus, o atidarytus kokybės užsakymus susieti su šaltinio dokumento eilute.  
13. Išplėskite arba sutraukite sekciją **Specifications**.
14. Lauke **Test group** pasirinkite bandymų grupę, kurią sukūrėte prieš tai.
15. Sąraše raskite ir pasirinkite norimą įrašą.
16. Spustelėkite **Įrašyti**.
17. Uždarykite puslapį.

