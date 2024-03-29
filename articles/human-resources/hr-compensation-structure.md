---
title: Kompensacijos struktūros kūrimas
description: Šiame straipsnyje paaiškinama, kaip sukurti pastoviosios atlyginimo dalies planą ir įtraukti darbuotojus į planą, naudojant tinkamumo taisykles.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86953e6d54843f17d0d6090a9def8bc256624f21
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902982"
---
# <a name="develop-a-compensation-structure"></a>Kompensacijos struktūros kūrimas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašoma, kaip kurti pastoviosios atlyginimo dalies planą ir įtraukti darbuotojus į planą taikant tinkamumo taisykles. Šiame straipsnyje naudojami JAVMF demonstraciniai duomenys ir jis taikomas kompensacijų ir išmokų vadovams.

## <a name="create-a-fixed-compensation-plan"></a>Pastoviosios atlyginimo dalies plano kūrimas

1. Pasirinkite **Kompensacijų valdymas**.

2. Pasirinkite **Pastoviosios kompensacijos planai**.

3. Pasirinkite **Naujas**.

4. Lauke **Planas** įveskite reikšmę.

5. Lauke **Aprašas** įveskite reikšmę.

6. Lauke **Įsigaliojimo data** įveskite datą.

7. Lauke **Tipas** pasirinkite, ar pastoviosios kompensacijos planas yra **Intervalo**, **Kategorijos** ar **Veiksmo**.

8. Žymės langelis **Leistina rekomendacija** bus visų veiksmų, įtrauktų į šį planą apdorojimo įvykyje, numatytoji reikšmė. Leidę rekomendacijas galėsite nepaisyti paskaičiuotos siūlomos sumos apdorodami kompensaciją.

9. Laukas **Leistinas nepatekimas į intervalą** leidžia nurodyti, kaip norite elgtis su kompensacijų sumomis, kurios nepatenka į nurodytą pateikto lygio kompensavimo struktūros diapazoną. Lauką **Leistinas nepatekimas į intervalą** nustačius kaip **Joks**, galima naudoti bet kokią kompensacijos sumą. Pasirinkus parinktį **Negriežtas nuokrypis**, vartotojas įspėjamas, jei kompensacijos suma yra mažesnė, nei minimali to lygio atskaitos taško suma, arba didesnė, nei maksimali to lygio suma. Vartotojai gali įspėjimo nepaisyti ir tęsti veiklą. Pasirinkus parinktį **Griežtas nuokrypis**, sugeneruojama klaida, jei darbuotojo kompensacija nustatyta ne tarp minimalių ir maksimalių to lygio atskaitos taškų, ir darbuotojo kompensacija automatiškai pakoreguojama, kad ji patektų į šį intervalą.

10. Laukas **Samdos taisyklė** apskaičiuoja darbuotojo kompensaciją apdorojimo įvykio metu. **Procentinė** **samdos taisyklė** apskaičiuoja padidėjimą, proporcingą laiko trukmei, kurią darbuotojas dirba cikle.

11. Lauke **Valiuta** įveskite reikšmę.

12. Lauke **Užmokesčio tarifo konvertavimas** įveskite arba pasirinkite reikšmę.

13. Išplėskite dalį **Intervalo realizavimo matrica**. Papildomai galite įtraukti diapazono realizavimo įrašų, kad darbuotojai greičiau pasiektų vidurio tašką ir kad sulėtintumėte spartą, kuria jie juda link savo diapazono maksimumo.

14. Pasirinkite **Įrašyti**. Taip įjungiamas mygtukas **Nustatyti kompensaciją** ir toliau nustatoma kompensacijos plano struktūra.

15. Pasirinkite **Nustatyti kompensaciją**. Kompensacijos struktūrą galite sukurti vienu iš toliau nurodytų trijų būdų.

    - Sukurti visiškai naują struktūrą, pasirenkant atskaitos taškų rinkinį ir įtraukiant lygių bei sukuriant savą struktūrą.
    - Kompensacijos struktūrą kopijuoti iš esamo plano kaip pradžios tašką ir ją modifikuoti naujajam planui.
    - Pasirinkti esamą kompensacijų tinklelį. Jei kompensacijų tinklelį jau naudoja kitas planas, visi atlikti tinklelio pakeitimai taip pat atsispindi kitame plane.

16. Pasirinkite **Pagal esamą kompensavimo matricą sukurti naują**.

17. Lauke **Kopijuoti iš tinklelio** įveskite arba pasirinkite reikšmę. Jei norite, galite keisti naujojo kompensacijų tinklelio, kurį sukuriate nukopijuodami pasirinktą tinklelį, pavadinimą.

18. Pasirinkite **Gerai**.

19. Pasirinkite **Masinis keitimas**. **Masinis keitimas** leidžia išlaikyti kompensacijų matricos sumas, vieną ar kelis lygius ir (arba) atskaitos taškus padidinant procentine dalimi arba standartine suma.

20. Lauke **Koregavimo suma** įveskite skaičių.

21. Pažymėkite arba atžymėkite visas sąrašo eilutes.

22. Spustelėkite **Taikyti tinkleliui**.

23. Uždarykite puslapį. Sukūrę kompensavimo struktūrą, galite pasirinkti, kurie atskaitos taškai turėtų būti naudojami kaip pastoviosios kompensacijos plano kontrolinis taškas. Kontrolinis taškas naudojamas darbuotojo lyginamajam koeficientui skaičiuoti.

24. Lauke **Kontrolinis taškas** įveskite arba pasirinkite reikšmę.

25. Uždarykite puslapį.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Pastoviosios kompensacijos plano tinkamumo taisyklės kūrimas

Pastoviosios kompensacijos plano darbuotojui priskirti negalite tol, kol nenustatote plano tinkamumo taisyklių.  

1. Pasirinkite **Tinkamumo taisyklės**.

2. Pasirinkite **Naujas**.

3. Lauke **Tinkamumas** įveskite reikšmę.

4. Lauke **Aprašas** įveskite reikšmę.

5. Lauke **Įsigaliojimo data** įveskite datą. Tinkamumo taisyklės naudojamos tiek pastoviosios, tiek kintamosios kompensacijos planuose. Lauke **Tipas** pasirinkite plano tipą.

6. Lauke **Planas** įveskite arba pasirinkite reikšmę. Pasirinkite kriterijus, kuriuos turi atitikti darbuotojas, kad turėtų teisę į kompensavimo planą. Toliau nurodyti galimi kriterijai.

    - **Skyrius**
    - **Profesinė sąjunga**
    - **Vieta** (**Kompensacijų regionas**)
    - **Užduotis**
    - **Funkcija**
    - **Užduoties tipas**
    - **Kompensavimo lygis**
    
    Kad turėtų teisę į kompensavimo planą, darbuotojas turi atitikti visus nurodytus kriterijus. Jei nenurodote jokių kriterijų, į kompensacijos planą teisę turi visi darbuotojai. Jei darbuotojas neatitinka tinkamumo taisyklėje nurodytų kriterijų, arba jei kompensavimo plano tinkamumo taisyklė nenurodyta, kuriant darbuotojo pastoviosios kompensacijos įrašą, peržvalgoje kompensavimo planas nebus rodomas.

7. Uždarykite puslapį.

8. Uždarykite puslapį.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
