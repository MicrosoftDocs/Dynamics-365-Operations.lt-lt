---
title: Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų peržiūra
description: Šioje temoje aprašoma, kaip kurti elektroninių ataskaitų konfigūraciją, norint generuoti elektroninius dokumentus su įdėtaisiais vaizdais. (1 dalis – Parametrų nustatymas).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eee6300350dd96c34f2eab44704d1895e6171ff
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093650"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų peržiūra

[!include [banner](../../includes/banner.md)]

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus užduočių vedlyje „ER: ataskaitų kūrimas „MS Office“ formatais su įdėtaisiais vaizdais (1 dalis. Parametrų nustatymas)“.

Ši procedūra parodo, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, norint generuoti elektroninius dokumentus, kuriuose yra įdėtųjų vaizdų „Microsoft Excel“ ir „Microsoft Word“. Šiame pavyzdyje peržiūrėsite pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. 

Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį.


## <a name="review-the-imported-data-model"></a>Peržiūrėkite importuotų duomenų modelį
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje pasirinkite „Model for cheques“.
3. Spustelėkite Konstruktorius.
    * Šis modelis skirtas nurodyti, kokius mokėjimo čekius naudoja įmonė, ir parodyti šio modelio susiejimą su programos duomenų šaltiniais. Peržiūrėkite šį modelį naudodami ER operacijų kūrimo priemonę. Atkreipkite dėmesį į pateiktus modelio elementų atributus: struktūrą, pavadinimą, aprašymą, duomenų tipą ir t.t.   
4. Medyje išplėskite „root“.
5. Medyje pasirinkite „root\cheques“.
6. Medyje išplėskite „root\cheques“.
7. Medyje išplėskite „root\cheques\attributes“.
8. Medyje išplėskite „root\payer“.
9. Medyje pasirinkite „root\istestrun“.
10. Medyje pasirinkite „root\layout“.
    * Šio modelio išdėstymo elementą sudaro pasirinktos banko sąskaitos čekio formos maketo spausdinimo informacija. Taip pat apima du konteinerio duomenų tipo mazgus vaizdams saugoti.   
11. Medyje išplėskite „root\layout“.
12. Medyje pasirinkite „root\layout\company logo“.
13. Medyje išplėskite „root\layout\company logo“.
14. Medyje pasirinkite „root\layout\company logo\image“.
15. Medyje pasirinkite „root\layout\company logo\isprinted“.
16. Medyje pasirinkite „root\layout\signature“.
17. Medyje išplėskite „root\layout\signature“.
18. Medyje pasirinkite „root\layout\signature\image“.
19. Medyje pasirinkite „root\layout\signature\isprinted“.
    * Atkreipkite dėmesį, kad du vaizdo duomenų modelio elementai susieti su lentelių laukais, kuriuose yra įmonės logotipas ir įgaliotojo asmens parašas dvejetainiu formatu.  
20. Medyje išplėskite „root\layout\watermark“.
21. Spustelėkite „Susieti modelį su duomenų šaltiniu“.
22. Spustelėkite Konstruktorius.
23. Medyje išplėskite „chequesselected“.
24. Medyje išplėskite „layout“.
25. Medyje išplėskite „layout\company logo“.
26. Medyje išplėskite „layout\signature“.
27. Medyje išplėskite „layout\watermark“.
28. Įjunkite „Rodyti išsamią informaciją”.
    * Atkreipkite dėmesį, kad čekių duomenų modelio elementas yra susietas su TmpChequePrintout lentele, kurioje vykdant bus čekių įrašai, kuriuos vartotojas pasirinko spausdinti.   
29. Uždarykite puslapį.
30. Uždarykite puslapį.
31. Uždarykite puslapį.

## <a name="review-the-imported-format"></a>Peržiūrėkite importuotą formatą
1. Medyje išplėskite „Model for cheques“.
2. Medyje pasirinkite „Model for cheques\Cheques printing format“.
3. Spustelėkite Konstruktorius.
4. Spustelėkite Priedai.
5. Spustelėkite Atidaryti.
    * Atidarykite pridėtą ataskaitos šabloną „Excel“.  
    * Peržiūrėkite pridėtos ataskaitos „Excel“ šabloną, kuris bus naudojamas čekiams spausdinti. Šablone yra du čekiai puslapyje, jis skirtas čekiams spausdinti iš anksto išspausdintoje formoje. Atkreipkite dėmesį, kad yra įdėti du tušti vaizdai. Šie tušti vaizdai skirti įmonės logotipui ir parašui asmens, kuris autorizuoja mokėjimą. Patikrinkite, ar vaizdai pavadinti CompLogo ir SignatureImage, atitinkamai, „Excel“.   
6. Uždarykite puslapį.
7. Medyje išplėskite „Report“.
8. Medyje išplėskite „Report\ChequeLines“.
9. Medyje pasirinkite „Report\ChequeLines\CompLogo“.
10. Įjunkite „Rodyti išsamią informaciją”.
    * Atkreipkite dėmesį, kad „CompLogo“ formato langelio elementas rodo „Excel“ elementą, naudojamą įmonės logotipo vaizdui įtraukti į ataskaitą. Šis formato elementas yra susietas su vaizdo duomenų modelio elementu, vykdant jame yra įmonės logotipo vaizdas dvejetainiu formatu.   
11. Spustelėkite skirtuką „Susiejimas“.
12. Spustelėkite Redagavimas įgalintas
    * Atkreipkite dėmesį, kad galite nustatyti „CompLogo“ formato langelio elementą taip, kad jis daugiau nebūtų įjungtas. Šiuo atveju susietas „Excel“ vaizdo elementas paslėps įmonės logotipą sugeneruotoje ataskaitoje. Jei įgalintos išraiškos rezultatas TRUE ir apibrėžtas susiejimas neteikia vaizdo, susietas „Excel“ vaizdo elementas rodys vaizdą, kuris buvo įrašytas „Excel“ šablone.   
13. Uždarykite puslapį.
14. Medyje išplėskite „labels: Container“.
    * Kai kurios etiketės, kurios pateikiamos iš anksto išspausdintoje čekio formoje, bus įtrauktos į ataskaitą, kai ji sukuriama bandymo tikslu. Tačiau tos etiketės nebus išspausdintos spausdinant tinkamas etiketes, nes iš anksto išspausdintoje formoje jos jau yra.  
15. Uždarykite puslapį.

