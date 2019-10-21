---
title: Modelio modifikavimas ir susiejimas siekiant generuoti dokumentus, kuriuose yra prašymų duomenys
description: 'Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (2 dalis: generuoti dokumentus)“.'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5df6128228b9ff620c606c550c5eb7a6039b915
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182306"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>Modelio modifikavimas ir susiejimas siekiant generuoti dokumentus, kuriuose yra prašymų duomenys

[!include [task guide banner](../../includes/task-guide-banner.md)]

Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (2 dalis: generuoti dokumentus)“. 

Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis. Taikydami šią procedūrą modifikuosite ER konfigūracijas, kad jas pradėtumėte naudoti elektroniniams dokumentams generuoti ir programos duomenims atnaujinti. Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį.


## <a name="modify-data-model"></a>Keiskite duomenų modelį
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje pasirinkite „Intrastat (model)“.
    * Jūs išplėsite, kaip naudojate duomenų modelį. Be jo naudojimo kaip duomenų šaltinio Intrastat ataskaitai generuoti, duomenų modelis bus naudojamas informacijai apie Intrastat ataskaitų teikimo procesą rinkti. Informacija paskui bus naudojama programos duomenims atnaujinti.   
3. Spustelėkite Konstruktorius.
4. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
5. Lauke „Naujas mazgas kaip” įveskite „Modelio šaknis”.
6. Lauke Pavadinimas įrašykite „Programos duomenų atnaujinimui“.
    * Programos duomenų atnaujinimui  
7. Spustelėkite Pridėti.
8. Medyje pasirinkite „Programos duomenų atnaujinimui“.
    * Šis naujas šakninis elementas įtraukiamas, norint nurodyti duomenų srautą duomenims iš Intrastat ataskaitos perkelti (naudojamas kaip duomenų šaltinis) į programos lenteles (atnaujinimo paskirtis). Atkreipkite dėmesį, kad skirtingi šakniniai elementai turi būti naudojami, norint gauti duomenis, kurie yra registruojami siunčiamam dokumentui, ir gaunant duomenis iš dokumento, kuris naudojamas norint atnaujinti programos duomenis.   
9. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
10. Lauke Pavadinimas įrašykite „Archyvo antraštė“.
    * Archyvo antraštė  
11. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
12. Spustelėkite Pridėti.
    * Kadangi jūs kursite kiekvienos sugeneruotos Intrastat ataskaitos įrašą, turite tam sukurti naują elementą.  
13. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
14. Lauke Pavadinimas įveskite Failo vardas.
    * Failo vardas  
15. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
16. Spustelėkite Pridėti.
17. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
18. Lauke „Pavadinimas“ įrašykite „Eilučių skaičius“.
    * Eilučių skaičius  
19. Lauke „Prekės tipas“ pasirinkite „Sveikasis skaičius“.
20. Spustelėkite Pridėti.
    * Įtraukite šį elementą, norėdami pateikti Intrastat operacijų, kurios paskelbtos per dabartinį ataskaitų teikimo procesą, skaičių.  
21. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
22. Lauke Pavadinimas įrašykite „Archyvuoti eilutes“.
    * Archyvo eilutės  
23. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
24. Spustelėkite Pridėti.
    * Įtraukite šį elementą, norėdami pateikti Intrastat operacijų, kurios paskelbtos per dabartinį ataskaitų teikimo procesą, sąrašą.  
25. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
26. Lauke „Pavadinimas“ įveskite „Suma“.
    * Suma  
27. Lauke „Prekės tipas“ pasirinkite „Realusis skaičius“.
28. Spustelėkite Pridėti.
29. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
30. Lauke Pavadinimas įrašykite „Prekės įr. ID“.
    * Prekės įr. ID  
31. Lauke „Prekės tipas“ pasirinkite „Int64“.
32. Spustelėkite Pridėti.
33. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
34. Lauke „Pavadinimas“ įrašykite „Prekės numeris“.
    * Prekės Nr.  
35. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
36. Spustelėkite Pridėti.
37. Spustelėkite Įrašyti.
38. Uždarykite puslapį.

## <a name="modify-model-mapping"></a>Keiskite modelio susiejimą
1. Medyje išplėskite „Intrastat (model)“.
2. Medyje pasirinkite „Intrastat (model)\Intrastat (mapping)“.
    * Keiskite esamą modelio susiejimą, norėdami pradėti jį naudoti programos duomenų atnaujinimui ir Intrastat ataskaitų teikimo informacijai archyvuoti.  
3. Spustelėkite Konstruktorius.
4. Spustelėkite Naujas.
5. Lauke Pavadinimas įrašykite „Atnaujinti archyvą“.
    * Atnaujinti archyvą  
6. Lauke Kryptis pasirinkite „Į paskirtį“.
7. Spustelėkite Įrašyti.
    * Šis naujas susiejimas nurodo duomenų srautą duomenims perkelti (Intrastat ataskaitų teikimo informacija) į programos lenteles (atnaujinimo paskirtis). Atkreipkite dėmesį, kad kitokio modelio šakniniai elementai turi būti naudojami, norint gauti duomenis iš programos ataskaitų teikimo procesui, o tada naudokite duomenis iš duomenų modelio programos duomenų atnaujinimui.   
8. Spustelėkite Konstruktorius.
9. Medyje pasirinkite „Data model\Data model“.
    * Pridėkite reikiamą duomenų šaltinį. Tai yra duomenų modelis, kuriame yra informacija apie Intrastat operacijas, apie kurias pateikta ataskaita, kurios turi būti archyvuojamos.  
10. Spustelėkite „Įtraukti šaknį“.
11. Lauke Pavadinimas įrašykite „modelis“.
    * modelis  
12. Lauke Apibrėžtis įveskite arba pasirinkite reikšmę „Programos duomenų atnaujinimui“.
    * Programos duomenų atnaujinimui  
13. Spustelėkite GERAI.
14. Medyje išplėskite „modelis‟.
15. Medyje pasirinkite „Funkcijos \ Apskaičiuotas laukas“.
16. Medyje pasirinkite „model\Archive header“.
17. Spustelėkite Pridėti.
    * Kadangi norite sunumeruoti Intrastat operacijas, apie kurias pateikta ataskaita, archyvavimui, turi būti pridėtas tinkamas duomenų šaltinis.  
18. Lauke Pavadinimas įrašykite „Sunumeruotos eilutės“.
    * Sunumeruotos eilutės  
19. Spustelėkite „Redaguoti formulę“.
20. Medyje pasirinkite „List\ENUMERATE“.
21. Spustelėkite „Įtraukti funkciją“.
22. Medyje išplėskite „modelis‟.
23. Medyje išplėskite „model\Archive header“.
24. Medyje pasirinkite „model\Archive header\Archive lines“.
25. Spustelėkite „Įtraukti duomenų šaltinį“.
26. Lauke Formulė įveskite „ENUMERATE(model.'Archive header'.'Archive lines')“.
    * ENUMERATE(model.'Archive header'.'Archive lines')  
27. Spustelėkite Įrašyti.
28. Uždarykite puslapį.
29. Spustelėkite GERAI.
30. Spustelėkite Pridėti paskirties vietą.
    * Pridėkite programos lentelių kaip privalomų paskirčių, kurias reikia naujinti, norint archyvuoti Intrastat operacijų, apie kurias pateikta ataskaita, informaciją.  
31. Lauke Pavadinimas įrašykite „Archyvas“.
    * Archyvuoti  
32. Lauke Lentelės pavadinimas įrašykite „IntrastatArchiveGeneral“.
    * IntrastatArchiveGeneral  
    * Išlaikykite įrašo veiksmą „Įterpti“, kad galėtumėte pridėti įrašų per kiekvieno Intrastat ataskaitų kūrimo proceso informacijos archyvavimą.  
33. Lauke Įrašo inform. žurnalas pasirinkite Taip.
    * Pasirinkite Taip, kad gautumėte informaciją apie programos duomenų atnaujinimo problemas.  
34. Lauke Praleisti įrašo veiksmo tikrinimą pasirinkite Taip.
    * Pasirinkite Taip, jei norite nerodyti tikrinimo klaidų apie tuščią lauką „Intrastat archyvo ID“. Tai bus padaryta pridėjus įrašus, pagal eilės numerio parametrus, kurie konfigūruojami šiai lentelei užsienio prekybos parametrų formoje.  
35. Spustelėkite GERAI.
    * Susiekite įtraukto duomenų šaltinio elementus (filtruotas modelis, pagrįstas pasirinktu šakniniu elementu) su elementais iš pridėtos paskirties.  
36. Medyje išplėskite „Archyvas“
37. Medyje išplėskite „Archive\<Relations“.
38. Medyje išplėskite „Archive\<Relations\IntrastatArchiveDetail“.
39. Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)“.
40. Medyje išplėskite „model\Archive header\Enumerated lines“.
41. Medyje išplėskite „model\Archive header\Enumerated lines\Value“.
42. Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Amount“.
43. Spustelėkite Susieti.
44. Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)“.
45. Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Commodity rec id“.
46. Spustelėkite Susieti.
47. Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)“.
48. Medyje pasirinkite „model\Archive header\Enumerated lines\Value\Item number“.
49. Spustelėkite Susieti.
50. Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)“.
51. Medyje pasirinkite „model\Archive header\Enumerated lines\Number“.
52. Spustelėkite Susieti.
53. Medyje pasirinkite „Archive\<Relations\IntrastatArchiveDetail“.
54. Medyje pasirinkite „model\Archive header\Enumerated lines“.
55. Spustelėkite Susieti.
56. Medyje pasirinkite „Archive\File name(FileName)“.
57. Medyje pasirinkite „model\Archive header\File name“.
58. Spustelėkite Susieti.
59. Medyje pasirinkite „Archive\Number of lines(NumberOfLines)“.
60. Medyje pasirinkite „model\Archive header\Number of lines“.
61. Spustelėkite Susieti.
62. Medyje pasirinkite „Archive“.
63. Medyje pasirinkite „model\Archive header“.
64. Spustelėkite Susieti.
65. Spustelėkite Įrašyti.
66. Uždarykite puslapį.
67. Uždarykite puslapį.
