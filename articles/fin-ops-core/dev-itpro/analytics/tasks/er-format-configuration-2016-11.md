---
title: 'ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)'
description: Šioje temoje paaiškinama, kaip sukurti elektroninių ataskaitų (ER) formato konfigūraciją.
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9404d1e242c83d2103d1f24c42589c33b9f57f02
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092255"
---
# <a name="er-create-a-format-configuration-november-2016"></a>ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenį turintis vartotojas gali kurti formato konfigūraciją elektroninėms ataskaitoms (ER). Ši formato konfigūracija apibrėš mokėjimų apdorojimui naudojamų elektroninių dokumentų formatą. Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ formato konfigūraciją. Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti procedūros „Modelio susiejimas su duomenų šaltiniais“ veiksmus.


## <a name="create-a-new-format-configuration"></a>Kurti naują formato konfigūraciją
1. Pasirinkite **Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**.
2. Spustelėkite **Ataskaitų konfigūracijos**.
3. Medyje pasirinkite **„Mokėjimai (supaprastintas modelis)“**.
4. Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą.

 > [!NOTE]
 > Jei nematote **Kurti konfigūraciją**, turite įgalinti dizaino režimą puslapyje **Elektroninės ataskaitos parametrai**. 
 
5. Lauke **Naujas** įveskite **Formatas pagal duomenų modelį PaymentModel**.
6. Lauke **Pavadinimas**, įveskite **BACS (JK fiktyvus)**.
7. Lauke **Aprašas** įveskite **BACS mokėjimo tiekėjui formatas (JK fiktyvus)**.
    * Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas. Šis teikėjas galės prižiūrėti šią konfigūraciją. Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.  
    * Galima apibrėžti konkretų elektroninio dokumento formatą. Palikite šį lauką tuščią, jei norite pasirinkti formatą vykdymo metu.  
8. Lauke **Duomenų modelio aprašas** įveskite arba pasirinkite reikšmę.
9. Spustelėkite **Sukurti konfigūraciją**. Sukurta nauja konfigūracija. Juodraščio versijoje galima laikyti elektroninių dokumentų valdymui skirtą dizaino formatą.  

## <a name="design-the-format-of-an-electronic-document"></a>Kurti elektroninio dokumento formatą
1. Spustelėkite **Konstruktorius**.
2. Spustelėdami **Įtraukti šakninį elementą** atidarykite išplečiamąjį dialogo langą.
3. Medyje pasirinkite **Bendra \ Failas**.
4. Lauke **Pavadinimas** įveskite **XML**.
5. Lauke **Kodavimas** įveskite **UTF-8**.
6. Spustelėkite **Gerai**.
7. Spustelėkite **Įtraukti**.
8. Medyje pasirinkite **XML \ Elementas**.
9. Lauke **Pavadinimas** įveskite **Pranešimas**.
10. Spustelėkite **Gerai**.
11. Medyje pasirinkite **Xml \ Pranešimas**.
12. Spustelėkite **Įtraukti elementą**.
13. Lauke **Pavadinimas** įveskite **ProcessingDate**.
14. Spustelėkite **Gerai**.
15. Spustelėkite **Įtraukti elementą**.
16. Lauke „Pavadinimas“ įveskite **MessageId**.
17. Spustelėkite **Gerai**.
18. Spustelėkite **Įtraukti elementą**.
19. Lauke **Pavadinimas**, įveskite **Mokėjimai**.
20. Spustelėkite **Gerai**.
21. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai**.
22. Spustelėkite **Įtraukti elementą**.
23. Lauke **Pavadinimas** įveskite **Prekė**.
24. Spustelėkite **Gerai**.
25. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.
26. Spustelėkite **Įtraukti**.
27. Medyje pasirinkite **XML \ Atributas**.
28. Lauke „Pavadinimas“ įveskite **Id**.
29. Spustelėkite **Gerai**.
30. Spustelėkite **Įtraukti**.
31. Medyje pasirinkite **XML \ Elementas**.
32. Lauke „Pavadinimas“ įveskite **Tiekėjas**.
33. Spustelėkite **Gerai**.
34. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas**.
35. Spustelėkite **Įtraukti elementą**.
36. Lauke „Pavadinimas“ įveskite **Agentas**.
37. Spustelėkite **Gerai**.
38. Spustelėkite **Įtraukti elementą**.
39. Lauke **Pavadinimas** įveskite **Bankas**.
40. Spustelėkite **Gerai**.
41. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas**.
42. Spustelėkite **Įtraukti elementą**.
43. Lauke **Pavadinimas** įveskite **RoutingNumber**.
44. Spustelėkite **Gerai**.
45. Spustelėkite **Įtraukti elementą**.
46. Lauke **Pavadinimas** įveskite **AccountNumber**.
47. Spustelėkite **Gerai**.
48. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas**.
49. Spustelėkite **Kopijuoti**.
50. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.
51. Spustelėkite **Įklijuoti**.
52. Lauke **Pavadinimas** įveskite **Mokėtojas**.
53. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė**.
54. Spustelėkite **Įtraukti elementą**.
55. Lauke **Pavadinimas** įveskite **Valiuta**.
56. Spustelėkite **Gerai**.
57. Spustelėkite **Įtraukti elementą**.
58. Lauke **Pavadinimas**, įveskite **Aprašas**.
59. Spustelėkite **Gerai**.
60. Spustelėkite **Įtraukti elementą**.
61. Lauke Pavadinimas įveskite **TransDate**.
62. Spustelėkite **Gerai**.
63. Spustelėkite **Įtraukti elementą**.
64. Lauke Pavadinimas įveskite **Suma**.
65. Spustelėkite **Gerai**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Parengti formato komponentus susiejimui su duomenų modelio elementais
1. Medyje pasirinkite **Xml \ Pranešimas \ ProcessingDate**.
2. Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.
3. Medyje pasirinkite **Tekstas \ DateTime**.
4. Lauke **Formatas** įveskite **mmmm-MM-dd**.
5. Spustelėkite **Gerai**.
6. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ TransDate**.
7. Spustelėkite **Įtraukti DateTime**.
8. Lauke **Formatas** įveskite **mmmm-MM-dd**.
9. Lauke **DateTime tipas** pasirinkite **Data**.
10. Spustelėkite **Gerai**.
11. Medyje pasirinkite **Xml \ Pranešimas \ MessageId**.
12. Spustelėdami **Įtraukti** atidarykite išplečiamąjį dialogo langą.
13. Medyje pasirinkite **Tekstas \ Eilutė**.
14. Spustelėkite **Gerai**.
15. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas**.
16. Spustelėkite **Įtraukti eilutę**.
17. Spustelėkite **Gerai**.
18. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ RoutingNumber**.
19. Spustelėkite **Įtraukti eilutę**.
20. Spustelėkite **Gerai**.
21. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ AccountNumber**.
22. Spustelėkite **Įtraukti eilutę**.
23. Spustelėkite **Gerai**.
24. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Pavadinimas**.
25. Spustelėkite **Įtraukti eilutę**.
26. Spustelėkite **Gerai**.
27. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ RoutingNumber**.
28. Spustelėkite **Įtraukti eilutę**.
29. Spustelėkite **Gerai**.
30. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ AccountNumber**.
31. Spustelėkite **Įtraukti eilutę**.
32. Spustelėkite **Gerai**.
33. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Valiuta**.
34. Spustelėkite **Įtraukti eilutę**.
35. Spustelėkite **Gerai**.
36. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Aprašas**.
37. Spustelėkite **Įtraukti eilutę**.
38. Spustelėkite **Gerai**.
39. Medyje pasirinkite **Xml \ Pranešimas \ Mokėjimai \ Prekė \ Suma**.
40. Spustelėkite **Įtraukti eilutę**.
41. Spustelėkite **Gerai**.
42. Spustelėkite **Įrašyti**.
43. Uždarykite puslapį.

