---
title: ER sukurto formato komponentų susiejimas su duomenų modelio elementais (2016 m. lapkričio mėn.)
description: Šiame straipsnyje aprašoma, kaip susieti duomenų modelio elementus su sukurtos elektroninės ataskaitos (ER) konfigūracijos komponentais.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc201832c10d9432f478d5d411c8ffe010807a70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895311"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>ER sukurto formato komponentų susiejimas su duomenų modelio elementais (2016 m. lapkričio mėn.)

[!include [banner](../../includes/banner.md)]

Tolesnėje procedūroje parodoma, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmens vartotojas gali susieti duomenų modelio elementus su sukurtos elektroninių ataskaitų (ER) konfigūracijos, nustatančios verslo mokėjimų srities elektroninio dokumento formatą, komponentais. Šį formatą bus galima naudoti vėliau norint generuoti elektroninius mokėjimų apdorojimo dokumentus. Šiame pavyzdyje sukursite kaip pavyzdys pateiktos įmonės „Litware, Inc.“ formato konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijos bendrinamos visoms įmonėms. Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti užduočių vedlio „Konfigūracijos formato kūrimas“ veiksmus.


## <a name="select-a-format-configuration"></a>Pasirinkti formato konfigūraciją
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Ataskaitų konfigūracijos.
3. Medyje išskleiskite „Mokėjimai (supaprastintasis modelis)“.
4. Medyje pasirinkite „Mokėjimai (supaprastintas modelis) \ BACS (JK fiktyvus)“.
5. Spustelėkite Konstruktorius.

## <a name="map-format-components-to-data-model-elements"></a>Susieti formato komponentus su duomenų modelio elementais
1. Spustelėkite Išplėsti / sutraukti.
2. Spustelėkite skirtuką „Susiejimas“.
3. Medyje išplėskite „modelis‟.
4. Medyje pasirinkite „Xml \ Pranešimas \ ProcessingDate \ DateTime“.
5. Medyje pasirinkite „modelis \ ProcessingDateTime”.
6. Spustelėkite Susieti.
7. Medyje pasirinkite „Xml \ Pranešimas \ MessageId \ Eilutė“.
8. Medyje pasirinkite „modelis \ MessageIdentification”.
9. Spustelėkite Susieti.
10. Medyje išplėskite „modelis \ Mokėjimai‟.
11. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Suma \ Eilutė“.
12. Medyje pasirinkite „modelis \ Mokėjimai \ InstructedAmount“.
13. Spustelėkite Susieti.
14. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ TransDate \ DateTime“.
15. Medyje pasirinkite „modelis \ Mokėjimai \ TransactionDate“.
16. Spustelėkite Susieti.
17. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Aprašas \ Eilutė“.
18. Medyje pasirinkite „modelis \ Mokėjimai \ Aprašas“.
19. Spustelėkite Susieti.
20. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Valiuta \ Eilutė“.
21. Medyje pasirinkite „modelis \ Mokėjimai \ Valiuta“.
22. Spustelėkite Susieti.
23. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Id“.
24. Medyje pasirinkite „modelis \ Mokėjimai \ End2EndID“.
25. Spustelėkite Susieti.
26. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius‟.
27. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Sąskaita‟.
28. Medyje išplėskite „modelis \ Mokėjimai \ Kreditorius \ Agentas‟.
29. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas \ Eilutė“.
30. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Pavadinimas“.
31. Spustelėkite Susieti.
32. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ RoutingNumber \ Eilutė“.
33. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Agentas \ RoutingNumber“.
34. Spustelėkite Susieti.
35. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ AccountNumber \ Eilutė“.
36. Medyje pasirinkite „modelis \ Mokėjimai \ Kreditorius \ Sąskaita \ Numeris“.
37. Spustelėkite Susieti.
38. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Pavadinimas \ Eilutė“.
39. Medyje išplėskite „modelis \ Mokėjimai \ Skolininkas‟.
40. Medyje išplėskite „modelis \ Mokėjimai \ Skolininkas \ Sąskaita‟.
41. Medyje išplėskite „modelis \ Mokėjimai \ Skolininkas \ Agentas“.
42. Medyje pasirinkite „modelis \ Mokėjimai \ Skolininkas \ Pavadinimas“.
43. Spustelėkite Susieti.
44. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ RoutingNumber \ Eilutė“.
45. Medyje pasirinkite „modelis \ Mokėjimai \ Debitorius \ Agentas \ RoutingNumber“.
46. Spustelėkite Susieti.
47. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ AccountNumber \ Eilutė“.
48. Medyje pasirinkite „modelis \ Mokėjimai \ Skolininkas \ Sąskaita \ Numeris“.
49. Spustelėkite Susieti.
50. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė“.
51. Medyje pasirinkite „modelis \ Mokėjimai“.
52. Spustelėkite Susieti.
53. Spustelėkite Įrašyti.

## <a name="validate-format-mapping"></a>Tikrinti formato susiejimą
1. Spustelėkite Tikrinti.
    * Norėdami įsitikinti, kad visi susiejimai veikia gerai, patikrinkite naują susiejimą.  
2. Uždarykite puslapį.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Pakeisti esamos formato konfigūracijos versijos būseną
Atlikdami kitus veiksmus, pakeisite formato konfigūracijos būseną iš Juodraštis į Baigta, kad ją būtų galima naudoti generuojant mokėjimo dokumentus.  
1. Spustelėkite keisti būseną.
2. Spustelėkite Baigti.
3. Lauke Aprašas įveskite reikšmę.
    * Pavyzdžiui, „1 versija“.  
4. Spustelėkite GERAI.
5. Pasirinkite baigtą esamos konfigūracijos versiją.
    * Atkreipkite dėmesį, kad konfigūracija įrašoma kaip 1.1 baigta versija: formato 1 versija, paremta duomenų modelio 1 versija.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Nustatyti baigtos formato versijos įsigaliojimo datą
Kiekvieną formato versiją galima sukonfigūruoti taip,kad ji būtų parengta naudoti nuo tam tikros datos. Kai pasirinktą dieną veikia daugiau nei viena formato versija, bus naudojamas naujausias formatas (pagal versijos numerį). Tinkame versija parenkama naudojant seanso datos reikšmę.  

## <a name="restrict-access-to-created-format-from-companies"></a>Apriboti įmonių prieigą prie sukurto formato
1. Išplėskite dalį ISO šalies / regiono kodai.
    * Kiekvieną formato prieigą galima apriboti nustatant konkrečias šalis / regionus, kuriuose veiks šis formatas. Kai konkretaus formato šalių / regionų sąrašas yra tuščias, šį formatą galima naudoti bet kurioje įmonėje. Į šalių / regionų sąrašą įterpus ISO šalių / regionų kodus, formatą bus galima naudoti tik įmonėse, kurių pagrindinis adresas yra šalyje / regione.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]