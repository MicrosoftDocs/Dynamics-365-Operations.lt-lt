--- 
title: "ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti elektroninių ataskaitų (ER) formato konfigūraciją."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a>ER: formato konfigūracijos kūrimas (2016 m. lapkričio mėn.)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali sukurti elektroninių ataskaitų (ER) formato konfigūraciją. Ši formato konfigūracija apibrėš mokėjimų apdorojimui naudojamų elektroninių dokumentų formatą. Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ formato konfigūraciją. Norėdami užbaigti šiuos veiksmus, pirmiausia turite užbaigti procedūros „Susieti modelį su duomenų šaltiniais“ veiksmus.


## <a name="create-a-new-format-configuration"></a>Kurti naują formato konfigūraciją
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Ataskaitų konfigūracijos.
3. Medyje pasirinkite „Mokėjimai (supaprastintas modelis)“.
4. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
5. Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį PaymentModel“.
6. Lauke „Pavadinimas“, įveskite „BACS (JK fiktyvus)“.
    * BACS (JK fiktyvus)  
7. Lauke „Aprašas“ įveskite „BACS mokėjimo tiekėjui formatas (JK fiktyvus)“.
    * BACS mokėjimo tiekėjui formatas (JK fiktyvus)  
    * Čia automatiškai įvedamas aktyvios konfigūracijos teikėjas. Šis teikėjas galės prižiūrėti šią konfigūraciją. Kiti teikėjai šią konfigūraciją galės naudoti, bet negalės jos prižiūrėti.  
    * Galima apibrėžti konkretų elektroninio dokumento formatą. Palikite šį lauką tuščią, jei norite pasirinkti formatą vykdymo metu.  
8. Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.
9. Spustelėkite Sukurti konfigūraciją.
    * Sukurta nauja konfigūracija. Juodraščio versijoje galima laikyti elektroninių dokumentų valdymui skirtą dizaino formatą.  

## <a name="design-format-of-electronic-document"></a>Kurti elektroninių dokumentų formatą
1. Spustelėkite Konstruktorius.
2. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
3. Medyje pasirinkite „Bendra \ Failas“.
4. Lauke „Pavadinimas“ įveskite „XML“.
    * Xml  
5. Lauke „Kodavimas“ įveskite „UTF-8“.
    * UTF-8  
6. Spustelėkite GERAI.
7. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
8. Medyje pasirinkite „XML \ Elementas“.
9. Lauke „Pavadinimas“ įveskite „Pranešimas“.
    * Pranešimas  
10. Spustelėkite GERAI.
11. Medyje pasirinkite „Xml \ Pranešimas“.
12. Spustelėkite Įtraukti elementą.
13. Lauke „Pavadinimas“ įveskite „ProcessingDate“.
    * ProcessingDate  
14. Spustelėkite GERAI.
15. Spustelėkite Įtraukti elementą.
16. Lauke „Pavadinimas“ įveskite „MessageId“.
    * MessageId  
17. Spustelėkite GERAI.
18. Spustelėkite Įtraukti elementą.
19. Lauke „Pavadinimas“, įveskite „Mokėjimai“.
    * Mokėjimai  
20. Spustelėkite GERAI.
21. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai“.
22. Spustelėkite Įtraukti elementą.
23. Lauke „Pavadinimas“ įveskite „Prekė“.
    * Produktas  
24. Spustelėkite GERAI.
25. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė“.
26. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
27. Medyje pasirinkite „XML \ Atributas“.
28. Lauke „Pavadinimas“ įveskite „Id“.
    * ID  
29. Spustelėkite GERAI.
30. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
31. Medyje pasirinkite „XML \ Elementas“.
32. Lauke „Pavadinimas“ įveskite „Tiekėjas“.
    * Tiekėjas  
33. Spustelėkite GERAI.
34. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas“.
35. Spustelėkite Įtraukti elementą.
36. Lauke „Pavadinimas“ įveskite „Agentas“.
    * Vardas  
37. Spustelėkite GERAI.
38. Spustelėkite Įtraukti elementą.
39. Lauke „Pavadinimas“ įveskite „Bankas“.
    * Bankas  
40. Spustelėkite GERAI.
41. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas“.
42. Spustelėkite Įtraukti elementą.
43. Lauke „Pavadinimas“ įveskite „RoutingNumber“.
    * RoutingNumber  
44. Spustelėkite GERAI.
45. Spustelėkite Įtraukti elementą.
46. Lauke „Pavadinimas“ įveskite „AccountNumber“.
    * AccountNumber  
47. Spustelėkite GERAI.
48. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas“.
49. Spustelėkite Kopijuoti.
50. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė“.
51. Spustelėkite Įklijuoti.
52. Lauke „Pavadinimas“ įveskite „Mokėtojas“.
    * Mokėtojas  
53. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė“.
54. Spustelėkite Įtraukti elementą.
55. Lauke „Pavadinimas“ suveskite „Valiuta“.
    * Valiuta  
56. Spustelėkite GERAI.
57. Spustelėkite Įtraukti elementą.
58. Lauke „Pavadinimas“, įveskite „Aprašas“.
    * aprašymas  
59. Spustelėkite GERAI.
60. Spustelėkite Įtraukti elementą.
61. Lauke „Pavadinimas“ įveskite „TransDate“.
    * TransDate  
62. Spustelėkite GERAI.
63. Spustelėkite Įtraukti elementą.
64. Lauke „Pavadinimas“ įveskite „Suma“.
    * Suma  
65. Spustelėkite GERAI.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Parengti formato komponentus susiejimui su duomenų modelio elementais
1. Medyje pasirinkite „Xml \ Pranešimas \ ProcessingDate“.
2. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
3. Medyje pasirinkite „Tekstas \ DateTime“.
4. Lauke „Formatas“ įveskite „mmmm-MM-dd“.
    * mmmm-MM-dd  
5. Spustelėkite GERAI.
6. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ TransDate“.
7. Spustelėkite Įtraukti DateTime.
8. Lauke „Formatas“ įveskite „mmmm-MM-dd“.
    * mmmm-MM-dd  
9. Lauke „DateTime tipas” pasirinkite „Data”.
10. Spustelėkite GERAI.
11. Medyje pasirinkite „Xml \ Pranešimas \ MessageId“.
12. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
13. Medyje pasirinkite „Tekstas \ Eilutė‟.
14. Spustelėkite Gerai.
15. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Pavadinimas“.
16. Spustelėkite Įtraukti eilutę.
17. Spustelėkite Gerai.
18. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ RoutingNumber“.
19. Spustelėkite Įtraukti eilutę.
20. Spustelėkite Gerai.
21. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Tiekėjas \ Bankas \ AccountNumber“.
22. Spustelėkite Įtraukti eilutę.
23. Spustelėkite Gerai.
24. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Pavadinimas“.
25. Spustelėkite Įtraukti eilutę.
26. Spustelėkite Gerai.
27. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ RoutingNumber“.
28. Spustelėkite Įtraukti eilutę.
29. Spustelėkite Gerai.
30. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Mokėtojas \ Bankas \ AccountNumber“.
31. Spustelėkite Įtraukti eilutę.
32. Spustelėkite Gerai.
33. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Valiuta“.
34. Spustelėkite Įtraukti eilutę.
35. Spustelėkite Gerai.
36. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Aprašas“.
37. Spustelėkite Įtraukti eilutę.
38. Spustelėkite Gerai.
39. Medyje pasirinkite „Xml \ Pranešimas \ Mokėjimai \ Prekė \ Suma“.
40. Spustelėkite Įtraukti eilutę.
41. Spustelėkite Gerai.
42. Spustelėkite Įrašyti.
43. Uždarykite puslapį.


