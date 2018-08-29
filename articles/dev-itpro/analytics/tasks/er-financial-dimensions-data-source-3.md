--- 
title: "Ataskaitų, pagal kurias finansinės dimensijos būtų naudojamos kaip duomenų šaltiniai, kūrimas"
description: "Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 055401104ae62c75694dff0b2ee64d12b2621686
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="design-reports-to-use-financial-dimensions-as-data-sources"></a>Ataskaitų, pagal kurias finansinės dimensijos būtų naudojamos kaip duomenų šaltiniai, kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šie veiksmai paaiškina, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) modelį, norėdamas naudoti finansines dimensijas kaip ER ataskaitų duomenų šaltinį. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti atlikti veiksmus, nurodytus procedūroje „ER: finansinių dimensijų kaip duomenų šaltinio naudojimas (2 dalis: modelio susiejimas)“.


## <a name="design-a-report-to-present-financial-dimensions"></a>Ataskaitos kūrimas finansinėms dimensijoms pateikti
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje pasirinkite Finansinių dimensijų modelio pavyzdys.
3. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
4. Lauke Naujas įveskite Formatas, pagrįstas duomenų modeliu Finansinių dimensijų modelio pavyzdys.
    * Naudokite modelį, kuris buvo iš anksto sukurtas kaip naujos ataskaitos duomenų šaltinis.  
5. Lauke Pavadinimas, įveskite DK žurnalo ataskaita.
6. Lauke Duomenų modelio aprašas pasirinkite Įrašas.
7. Spustelėkite Sukurti konfigūraciją.
8. Spustelėkite Konstruktorius.
9. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
10. Medyje pasirinkite „XML \ Elementas“.
11. Lauke Pavadinimas įveskite Šaknis.
12. Spustelėkite Gerai.
13. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
14. Medyje pasirinkite „XML \ Atributas“.
15. Lauke „Pavadinimas“ įveskite „Įmonė“.
16. Spustelėkite Gerai.
17. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
18. Medyje pasirinkite „XML \ Elementas“.
19. Lauke Pavadinimas įveskite Žurnalas.
20. Spustelėkite Gerai.
21. Medyje pasirinkite Root: XML Element\Journal: XML Element.
22. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
23. Medyje pasirinkite „XML \ Atributas“.
24. Lauke Pavadinimas įveskite Paketas.
25. Spustelėkite Gerai.
26. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
27. Medyje pasirinkite „XML \ Elementas“.
28. Lauke Pavadinimas įveskite Operacija.
29. Spustelėkite Gerai.
30. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.
31. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
32. Medyje pasirinkite „XML \ Atributas“.
33. Lauke Pavadinimas įveskite Kvitas.
34. Spustelėkite GERAI.
35. Spustelėkite Įtraukti atributą.
36. Lauke Pavadinimas įveskite Data.
37. Spustelėkite GERAI.
38. Spustelėkite Įtraukti atributą.
39. Lauke „Pavadinimas“ suveskite „Valiuta“.
40. Spustelėkite GERAI.
41. Spustelėkite Įtraukti atributą.
42. Lauke Pavadinimas Dt.
43. Spustelėkite GERAI.
44. Spustelėkite Įtraukti atributą.
45. Lauke Pavadinimas įveskite Ct.
46. Spustelėkite GERAI.
47. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
48. Medyje pasirinkite „XML \ Elementas“.
49. Lauke Pavadinimas įveskite Dimensijos.
50. Spustelėkite Gerai.
51. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.
52. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
53. Medyje pasirinkite „XML \ Atributas“.
54. Lauke Pavadinimas įveskite Kodas.
55. Spustelėkite GERAI.
56. Spustelėkite Įtraukti atributą.
57. Lauke Pavadinimas įveskite Reikšmė.
58. Spustelėkite GERAI.
59. Spustelėkite Įtraukti atributą.
60. Lauke Pavadinimas įveskite Aprašas.
61. Spustelėkite GERAI.

## <a name="map-report-elements-to-data-sources"></a>Ataskaitos elementų susiejimas su duomenų šaltiniais
1. Spustelėkite skirtuką „Susiejimas“.
2. Medyje išplėskite dalį model: Data model Financial dimensions sample model.
3. Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list.
4. Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.
5. Medyje išplėskite dalį model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.
6. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute.
7. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String.
8. Spustelėkite Susieti.
9. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute.
10. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String.
11. Spustelėkite Susieti.
12. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute.
13. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String.
14. Spustelėkite Susieti.
15. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list.
16. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element.
17. Spustelėkite Susieti.
18. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute.
19. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real.
20. Spustelėkite Susieti.
21. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute.
22. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real.
23. Spustelėkite Susieti.
24. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute.
25. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String.
26. Spustelėkite Susieti.
27. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute.
28. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date.
29. Spustelėkite Susieti.
30. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute.
31. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String.
32. Spustelėkite Susieti.
33. Medyje pasirinkite Root: XML Element\Journal: XML Element\Transaction: XML Element.
34. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list.
35. Spustelėkite Susieti.
36. Medyje pasirinkite Root: XML Element\Journal: XML Element\Batch: XML Attribute.
37. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list\Batch: String.
38. Spustelėkite Susieti.
39. Medyje pasirinkite Root: XML Element\Journal: XML Element.
40. Medyje pasirinkite model: Data model Financial dimensions sample model\Journal: Record list.
41. Spustelėkite Susieti.
42. Medyje pasirinkite Root: XML Element\Company: XML Attribute.
43. Medyje pasirinkite model: Data model Financial dimensions sample model\Company: String.
44. Spustelėkite Susieti.
45. Spustelėkite Įrašyti.
46. Uždarykite puslapį.


