---
title: ER konfigūracijų priklausomybės nuo kitų komponentų apibrėžimas
description: Šiame straipsnyje aprašoma, kaip sukurti elektroninių ataskaitų (ER) konfigūraciją ir nurodyti jos priklausomybę nuo kitų programinės įrangos komponentų.
author: NickSelin
ms.date: 07/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aceb883e9182090a336c4c91aa0022a79495ce40
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111701"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>ER konfigūracijų priklausomybės nuo kitų komponentų apibrėžimas

[!include [banner](../../includes/banner.md)]

Norėdami atlikti šiuos veiksmus, turite užbaigti veiksmus užduočių vedlyje, ER valdymo modelio susiejimo konfigūracijos, ir jūs turite turėti prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS).

Ši procedūra nurodo, kaip sukurti elektroninių ataskaitų (ER) konfigūraciją ir nurodo jos priklausomybę nuo kitų programinės įrangos komponentų, kad jūs galite padėti užtikrinti, kad konfigūracija tinkamai bus atsisiųsta į konkrečią finansų ir operacijų versiją. Šiame pavyzdyje kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. 

Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas įmonės naudoja bendrai. 

1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
    * Įsitikinkite, kad konfigūracijos medyje yra konfigūracija „Duomenų pavyzdžio modelis“ ir antriniai elementai. Kitu atveju atlikite veiksmus užduočių vedlyje, ER valdyti modelio susiejimo konfigūracijas, ir tada dar kartą paleiskite šį vedlį.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>Apibrėžkite ER konfigūracijų priklausomybę nuo kitų komponentų
1. Medyje išplėskite „Duomenų pavyzdžio modelis“.
2. Medyje pasirinkite „Sample data model\Sample mapping“.
    * Mes pasirinkome modelio susiejimo konfigūracijos „Susiejimo pavyzdys“ projekto versiją. Dabar apibrėšime jos priklausomybę nuo kitų programinės įrangos komponentų. Šis veiksmas yra laikomas išankstine sąlyga, norint kontroliuoti šios konfigūracijos versijos atsisiuntimą iš ER saugyklos ir toliau naudoti šią versiją.   
3. Išplėskite sekciją Išankstiniai reikalavimai.
    * Žinokite, kad išankstinių reikalavimų grupė „Įgyvendinimas“ automatiškai įtraukta šiame etape. Šioje grupėje yra būtinas komponentas, kuris nurodo duomenų modelio konfigūraciją ir kurio vėliavėlė Įgyvendinimas įjungta. Ši vėliavėlė rodo, kad naudojama susiejimo konfigūracija „Susiejimo pavyzdys“ duomenų modeliui „Duomenų modelio pavyzdys“ įgyvendinimui. Šis komponentas privers ER atsisiųsti susiejimo konfigūraciją „Susiejimo pavyzdys“ iš ER saugyklos kai bus atsisiunčiama modelio konfigūracija „Duomenų modelio pavyzdys“.   
4. Spustelėkite Redaguoti.
    * Vieną dabartinės konfigūracijos versijos priklausomybę nuo programinės įrangos komponento galima nurodyti naudojant komponento tipo apibrėžtį ir arba komponento versiją, arba komponento versijų diapazoną.  
    * Galima sugrupuoti norimas priklausomybes. Pasirinkus grupavimo tipą „Visi“, šios grupės priklausomybės sąlyga laikoma patenkinta, kai patenkinta kiekviena šios grupės ir antrinės grupės priklausomybės sąlyga. Pasirinkus grupavimo tipą „Vienas iš“, šios grupės priklausomybės sąlyga laikoma patenkinta, kai patenkinta bent viena šios grupės priklausomybės sąlyga.   
5. Spustelėkite Naujas.
6. Pasirinkite Produkto būtinasis komponentas.
7. Pasirinkite Microsoft Dynamics 365 for Operations (1611).
8. Lauke Versija įrašykite „[7.1.1541.3036,8)“.
    * [7.1.1541.3036,8)  
    * Įvedamos priklausomybės įvertinamos atsisiunčiant šią konfigūraciją iš ER saugyklos. Ši konfigūracijos versija bus atsisiųsta iš ER saugyklos, kai „Duomenų pavyzdžio modelio“ 1 versijos konfigūracija jau bus reikiamoje vietoje arba iš anksto atsisiųsta. Jei jis atsisiųstas iš anksto, jis turi būti įdiegtas į finansų ir operacijų versiją 7.1.1541.3036 arba vėlesnę versiją, bet neturi viršyti 8 pagrindinės versijos.   
9. Spustelėkite Įrašyti.
10. Uždarykite puslapį.
11. Spustelėkite keisti būseną.
12. Spustelėkite Baigti.
13. Spustelėkite GERAI.
14. Medyje pasirinkite „Sample data model\Sample mapping (alternative)“.
15. Spustelėkite Redaguoti.
16. Spustelėkite Naujas.
17. Pasirinkite Produkto būtinasis komponentas.
18. Pasirinkite „Microsoft Dynamics AX 7.0 RTW“.
19. Lauke Versija įrašykite „[7.0.1265.3015,7.1)“.
    * [7.0.1265.3015,7.1)  
    * Priklausomybės įvertinamos atsisiunčiant konfigūraciją iš ER saugyklos. Ši konfigūracijos versija bus atsisiųsta iš ER saugyklos, kai „Duomenų pavyzdžio modelio“ 1 versijos konfigūracija jau bus reikiamoje vietoje arba iš anksto atsisiųsta. Jei jis atsisiųstas iš anksto, Microsoft Dynamics jis turi būti įdiegtas 365 finansų, įmonės leidime, kurio versija turi būti 7.0.1265.3015 arba vėlesnė, bet neturi viršyti 1 versijos.   
20. Spustelėkite Įrašyti.
21. Uždarykite puslapį.
22. Spustelėkite keisti būseną.
23. Spustelėkite Baigti.
24. Spustelėkite GERAI.

## <a name="configure-the-er-repository"></a>Konfigūruokite ER saugyklą
1. Uždarykite puslapį.
2. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Atidarykite ER saugyklų sąrašą dabartiniam ER teikėjui, „Litware, Inc.‟  
3. Sąraše pažymėkite pasirinktą eilutę.
4. Spustelėkite Saugyklos.
5. Spustelėkite Rodyti filtrus.
6. Įveskite filtro reikšmę „LCS“ lauke „Tipo pavadinimas“ naudodami filtro operatorių „yra“.
    * Jei LCS saugykla jau užregistruota dabartiniam ER teikėjui, galite praleisti likusius šios antrinės užduoties veiksmus. Jei LCS saugykla dar neužregistruota, atlikite likusius veiksmus.   
7. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
8. Lauke Konfigūracijų saugyklos tipas įveskite „LCS“.
9. Spustelėkite Kurti saugyklą.
10. Lauke Projektas įveskite arba pasirinkite vertę.
    * Pasirinkite norimą LCS projektą iš lauko „Projektas“ peržvalgos.  
11. Spustelėkite Gerai.
12. Uždarykite puslapį.

## <a name="upload-configurations-to-lcs"></a>Nusiųskite konfigūracijas į LCS
1. Spustelėkite Ataskaitų konfigūracijos.
2. Medyje pasirinkite „Sample data model“.
3. Pasirinkite baigtą šios konfigūracijos versiją.
4. Spustelėkite keisti būseną.
5. Spustelėkite Bendrinti.
6. Spustelėkite GERAI.
    * 1 šios modelio konfigūracijos versija nusiųsta į LCS, naudojant LCS projektą ER saugyklai, kuri anksčiau buvo sukonfigūruota.   
7. Medyje išplėskite „Duomenų pavyzdžio modelis“.
8. Medyje pasirinkite „Sample data model\Sample mapping“.
9. Pasirinkite baigtą šios konfigūracijos versiją.
10. Spustelėkite keisti būseną.
11. Spustelėkite Bendrinti.
12. Spustelėkite GERAI.
    * 1.1 šios modelio susiejimo konfigūracijos versija nusiųsta į LCS, naudojant LCS projektą ER saugyklai, kuri anksčiau buvo sukonfigūruota.   
13. Medyje pasirinkite „Sample data model\Sample mapping (alternative)“.
14. Pasirinkite baigtą šios konfigūracijos versiją.
15. Spustelėkite keisti būseną.
16. Spustelėkite Bendrinti.
17. Spustelėkite GERAI.
    * 1.1 šios modelio susiejimo konfigūracijos versija nusiųsta į LCS, naudojant LCS projektą ER saugyklai, kuri anksčiau buvo sukonfigūruota.   

## <a name="evaluate-er-configuration-dependencies"></a>Įvertinkite ER konfigūracijos priklausomybes
Mes panaikinsime iš sistemos sukurtas konfigūracijas ir vėl atsisiųsime jas iš LCS saugyklos.  
1. Medyje pasirinkite „Sample data model\Sample mapping“.
2. Spustelėkite Naikinti.
3. Spustelėkite Taip.
4. Medyje pasirinkite „Sample data model\Sample mapping (alternative)“.
5. Spustelėkite Naikinti.
6. Spustelėkite Taip.
7. Medyje pasirinkite „Sample data model\Sample format“.
8. Spustelėkite Naikinti.
9. Spustelėkite Taip.
10. Medyje pasirinkite „Sample data model“.
11. Spustelėkite Naikinti.
12. Spustelėkite Taip.
13. Uždarykite puslapį.
    * Atidarykite ER saugyklų sąrašą dabartiniam ER teikėjui, „Litware, Inc.‟  
14. Spustelėkite Saugyklos.
15. Spustelėkite Rodyti filtrus.
16. Įveskite filtro reikšmę „LCS“ lauke „Tipo pavadinimas“ naudodami filtro operatorių „yra“.
17. Spustelėkite Atidaryti.
18. Medyje pasirinkite „Sample data model“.
    * Atkreipkite dėmesį, kad galite peržiūrėti įvertinimą, ar patenkintos išankstinės sąlygos kiekvienai ER konfigūracijų versijai dabartinei saugyklai. Norėdami peržiūrėti šį įvertinimą, spustelėkite Tikrinti išankstines sąlygas.   
19. Spustelėkite Tikrinti išankstinius reikalavimus.
20. Spustelėkite Importuoti.
21. Spustelėkite Taip.
22. Uždarykite puslapį.
23. Uždarykite puslapį.
24. Uždarykite puslapį.
25. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
26. Medyje išplėskite „Duomenų pavyzdžio modelis“.
    * Atkreipkite dėmesį, kad modelio „Susiejimo pavyzdys“ susiejimo konfigūracija buvo atsisiųsta kartu su pasirinkta duomenų modelio konfigūracija. Du failai atsisiunčiami kartu, kadangi „Susiejimo pavyzdys“ apibrėžtas kaip pasirinkto duomenų modelio įgyvendinimas, ir todėl, kad jis taikomas programoms. Konfigūracija „Susiejimo pavyzdys (alternatyvus)“ dar neatsisiųsta, nes reikiamos programos versijos sąlyga nėra patenkinta.   
    * Jei prisiregistruojate prie finansų ir operacijų, užregistruokite tą patį teikėją, kreipkitės į tą patį LCS projektą ir atsisiųskite tą pačią duomenų modelio konfigūraciją, konfigūracija "Pavyzdžio konvertavimas (alternatyvi)" bus atsisiųsta, o "Pavyzdžio susiejimo" konfigūracija bus praleista.  

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) konfigūracijų ciklo valdymas](../general-electronic-reporting-manage-configuration-lifecycle.md)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

