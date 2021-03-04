---
title: Kompensavimo proceso nustatymas ir rezultatų skaičiavimas
description: Kompensacijos procesai naudojami nustatyti naujas kompensacijų ir premijų sumas darbuotojams, užregistruotiems pastoviosios ir kintamosios atlyginimo dalies planuose.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompProcess, HRMCompProcessLine, HRMCompEvent, HRMCompEventEmpl, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 254eb4f83cc734e43920b912e81c7a9230ca82dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419747"
---
# <a name="define-compensation-process-and-calculate-results"></a>Kompensavimo proceso nustatymas ir rezultatų skaičiavimas

Kompensacijos procesai naudojami nustatyti naujas kompensacijų ir premijų sumas darbuotojams, užregistruotiems pastoviosios ir kintamosios atlyginimo dalies planuose. Kompensacijos procesą galima vykdyti kelis kartus, norint atlikti sąlyginę analizę siekiant patikrinti, ar visi pakeitimai ir parametrai yra teisingi. Šios procedūros metu bus sukurtas kompensacijos procesas, vykdomas procesas ir peržiūrėti rezultatai. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-a-compensation-process"></a>Kurti kompensacijos apdorojimą
1. Eikite į Personalas > Kompensacija > Procesas > Kompensacijos procesai.
2. Spustelėkite Naujas.
3. Lauke Procesas įveskite vertę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Proceso tipas pasirinkite pasirinktį.
    * Ciklas nurodo laikotarpį, įvertintą kompensacijai nustatyti. Įvertinant apsvarstoma, kurias pareigas darbuotojai užėmė, kuriuos našumo vertinimus įtraukti, laiko, kiek darbuotojas buvo įdarbintas ciklo metu, apskaičiavimas ir kt. Ciklo pradžios datos pavyzdys gali būti pirma praėjusių finansinių metų diena.  
6. Lauke Ciklo pradžia įveskite datą.
    * Ciklo pabaigos data svarbi dėl to, kad tai yra data, naudojama nustatyti, kurie darbuotojai buvo aktyviai įdarbinti ir įtraukti į vieną ar daugiau kompensacijų planų.  
7. Lauke Ciklo pabaiga įveskite datą.
    * Aktyvios operacijos data yra tokia data, kada turėtų įsigalioti nauji kompensacijų tarifai. Daugelis įmonių įtraukia kelis mėnesius tarp ciklo pabaigos ir naujo kompensacijų tarifų įsigaliojimo. Papildomas laikas naudojamas apdoroti ir peržiūrėti naują kompensaciją.  
8. Lauke Aktyvios operacijos data įveskite datą.
    * Tam tikra data naudojama kintamų kompensacijų planams, nustatantiems darbuotojo premijos sumą pagal kompensacijos tarifą šiuo momentu.  
    * Fiksuotas užmokestis pagal samdos datą naudojamas su fiksuotų kompensacijų planais su Procentine samdos taisykle.  Darbuotojai, kurie yra pasamdyti tarp ciklo pradžios ir fiksuoto užmokesčio pagal samdos datą laikotarpio, gaus 100 % jų apskaičiuotos kompensacijos padidėjimo, o ne proporcingai paskirstytą procentą.  
9. Lauke Fiksuotas užmokestis pagal samdos datą įveskite datą.
    * Peržiūrėjimo terminas yra data, pagal kurią visi proceso rezultatai turėtų būti peržiūrėti, kad juos būtų galima įkelti į darbuotojo kompensacijos įrašą prieš aktyvios operacijos datą. Šis laukas skirtas tik informacijai.  
10. Lauke Peržiūrėti terminą įveskite datą.
11. Spustelėkite Įrašyti.

## <a name="setup-the-compensation-plans-and-actions-for-a-compensation-process"></a>Nustatyti kompensacijos proceso kompensacijos planus ir veiksmus
1. Spustelėkite Nustatymas.
    * Nustatymo puslapis naudojamas pasirinkti, kuriuos planus apdoroti kaip šio kompensacijos proceso dalį, ir kuriuos veiksmus reikia atlikti pagal kiekvieną planą.  
2. Lauke Planas įveskite arba pasirinkite vertę.
3. Spustelėkite Įrašyti.
4. Spustelėkite Pridėti.
5. Lauke Veiksmas pasirinkite Kapitalo tipo veiksmą.
6. Spustelėkite Pridėti.
7. Lauke Veiksmas pasirinkite Nuopelno tipo veiksmą.
    * Kompensacijos veiksmai gali būti sujungti į „grandinę“ naudojant lauką Naudoti ankstesnį rezultatą siekiant nurodyti, ar šio veiksmo skaičiavimo pradžios tašku pasirinktam veiksmui turėtų būti naudojamas darbuotojų pagrindinis užmokestis ar ankstesnio veiksmo rezultatas.  
8. Lauke Naudoti ankstesnį rezultatą pasirinkite Taip.
9. Spustelėkite Pridėti.
10. Lauke Veiksmas pasirinkite Bendro tipo Veiksmą.
    * Skirtingi kompensacijos veiksmų tipai įgalina skirtingus laukus. Bendram kompensacijos veiksmo tipui, galima nurodyti padidinimo procentą arba padidinimo sumą.  
11. Pasirinkite pasirinktį Pasirinkti padidinimo sumą.
12. Lauke Padidinti sumą įveskite skaičių.
13. Spustelėkite Pridėti.
14. Lauke Veiksmas pasirinkite Paaukštinimo tipo Veiksmą.
    * Lygio pakeitimo veiksmo tipai Skatinimas ir Kita leidžia vartotojams rankiniu būdu koreguoti darbuotojų kompensacijas. Rekomendacijas galima įgalinti šių veiksmų tipams ir kitiems veiksmų tipams, kad galėtumėte įvesti naują rekomenduojamą kompensacijos vertę darbuotojui.  
15. Spustelėkite Pridėti.
16. Lauke „Tipas“ pasirinkite parinktį.
    * Pastoviosios ir kintamosios atlyginimo dalies planus galima vykdyti tuo pačiu kompensacijos procesu.  
17. Lauke Planas įveskite arba pasirinkite vertę.
    * Naudokite žymės langelį Įgalinti užmokestį už veiklą norėdami nustatyti, ar pagal darbuotojo našumo vertinimą koreguoti reikia pastoviosios ir kintamosios atlyginimo dalies sumą.  
    * Svertų galima nepaisyti kintamosios atlyginimo dalies planuose.  
18. Spustelėkite Įrašyti.
19. Spustelėkite Pridėti.
20. Uždarykite puslapį.

## <a name="run-the-compensation-process"></a>Vykdyti kompensacijos procesą
1. Spustelėkite Vykdyti procesą.
    * Valdiklis Rodyti apdorojimo kontrolės rezultatus leidžia peržiūrėti viso kompensacijos proceso apdorojimo pranešimus, kai apdorojimas baigtas.  
2. Lauke Rodyti vykdymo rezultatus pasirinkite Taip.
3. Spustelėkite GERAI.

## <a name="view-the-results"></a>Peržiūrėti rezultatus
1. Spustelėkite Proceso rezultatai.
2. Spustelėkite Darbuotojo rezultatai.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Išplėskite skyrių Pastovioji atlyginimo dalis.
    * Išplėskite „FastTabs“ norėdami peržiūrėti proceso rezultatus. Jei kompensacijos veiksmui buvo pažymėta Įgalinti rekomendacijas, tam veiksmui bus įgalinti Rekomendacijų laukai.  
5. Sąraše raskite ir pasirinkite norimą įrašą.
    * Vieno darbuotojo rezultatus galima peržiūrėti spustelėjus mygtuką Peržiūrėti rezultatus.  
    * Apskaičiuotą kompensacijos sumą galite perrašyti koreguodami procentą arba padidinimo sumą laukuose Rekomendacija.  
6. Lauke Rekomenduojamas procentas įveskite skaičių.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Lauke Rekomenduojamas procentas įveskite skaičių.
    * Norint nepaisyti esamam įrašui atliktų pakeitimų ir generuoti naują kompensavimo rezultatą pasirinktam darbuotojui, galima naudoti Perskaičiuoti.  
    * Kai visi pakeitimai darbuotojui atlikti, pakeiskite būseną į Patvirtinta.  
9. Spustelėkite keisti būseną.
10. Spustelėkite Patvirtinti.
    * Patvirtinus įrašą, jį galima įkelti į darbuotojo oficialų kompensacijos įrašą. Nauja kompensacija įsigalios nuo operacijos datos, nustatytos kompensacijos procese.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]