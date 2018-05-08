--- 
title: "Konfigūracijų importavimas dokumentams su programos duomenimis generuoti"
description: "Norėdami baigti šios procedūros veiksmus, pirmiausia turite atlikti procedūrą „ER sukurti konfigūracijos teikėją“ ir pažymėti jį kaip aktyvų."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 87352293a78d6a356db49deffb930016a1bf836c
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="import-configurations-to-generate-documents-with-application-data"></a>Konfigūracijų importavimas dokumentams su programos duomenimis generuoti

[!include [task guide banner](../../includes/task-guide-banner.md)]

Norėdami baigti šios procedūros veiksmus, pirmiausia turite atlikti procedūrą „ER sukurti konfigūracijos teikėją“ ir pažymėti jį kaip aktyvų.

Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą. Šios procedūros metu importuosite reikiamas ER formato konfigūracijas, sukurtas pavyzdinei įmonei „Litware, Inc.“, tada generuosite elektroninius dokumentus. Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį. Prieš pradėdami, atsisiųskite ir įrašykite failus, išvardytus žinyno temoje „Elektroninių dokumentų generavimas ir programų duomenų naujinimas naudojant ER įrankį“ (generate-electronic-documents-update-application-data/). Failai yra Intrastat (modelis).xml, Intrastat (susiejimas).xml ir Intrastat (formatas).xml

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros „Kurkite konfigūracijos teikėją ir pažymėkite kaip aktyvų” veiksmus.  
    * Šios procedūros veiksmuose rodoma, kaip naudoti ER galimybes, norint atlikti programos duomenų naujinimą ir kaip generuoti Intrastat ataskaitą. Išsamią informaciją apie ataskaitų teikimo procesą archyvuojama programos lentelėse. Dabar, kai Intrastat ataskaitų kūrimo procesas aktyvintas iš Intrastat formos, archyvavimas daromas remiantis logika, užprogramuota esamame šaltinio kode. Taikydami šią procedūrą, konfigūruosite panašią dar supaprastintą programos duomenų logiką, naudojant tik ER sistemą. Šaltinio kodo pakeitimai nebus daromi.   

## <a name="import-er-configurations"></a>Importuokite ER konfigūracijas
1. Spustelėkite Ataskaitų konfigūracijos.
2. Spustelėkite Keitimas.
3. Spustelėkite Įkelti iš XML failo.
    * Importuokite ER modelio konfigūraciją, kurioje yra duomenų modelis, skirtas naudoti kaip duomenų šaltinis Intrastat ataskaitai generuoti. Vėliau išplėsite šio duomenų modelio apibrėžtį naudoti jį programos duomenų atnaujinimui, informacijai apie Intrastat ataskaitų procesą archyvuoti.   
    * Spustelėkite Naršyti ir pasirinkite Intrastat (modelis).xml failą.  
4. Spustelėkite GERAI.
5. Medyje pasirinkite „Intrastat (model)“.
6. Spustelėkite Konstruktorius.
7. Medyje išplėskite „For outgoing document“.
8. Medyje išplėskite „For outgoing document\Transactions“.
    * Peržiūrėkite importuoto duomenų modelio struktūrą. Žinokite, kad šakninis elementas „Išeinančiam dokumentui“ apibrėžtas, kad nurodytų srautą duomenims gauti iš programos ir naudoti kaip duomenų šaltinį Intrastat ataskaitai generuoti. „Operacijos (įrašų sąrašas)“ naudojamas parodyti Intrastat operacijas, apie kurias turi būti pateikta ataskaita. Kadangi archyvuosite paskelbtus prekių kodus, unikalus vieno prekės kodo „Prekės įr. ID (Int64)“ identifikatorius reikalingas šiame duomenų sraute.   
9. Uždarykite puslapį.
10. Spustelėkite Keitimas.
11. Spustelėkite Įkelti iš XML failo.
    * Importuokite ER susiejimo konfigūraciją, kuri nurodo duomenų srautą, skirtą gauti duomenis iš programos, ir tada naudoja jį Intrastat ataskaitai generuoti. Vėliau išplėsite šio modelio susiejimo apibrėžtį duomenims iš Intrastat ataskaitos gauti ir naudoti jį programos duomenų atnaujinimui, informacijai apie Intrastat ataskaitų procesą archyvuoti.   
    * Spustelėkite Naršyti ir pasirinkite Intrastat (susiejimas).xml failą.  
12. Spustelėkite GERAI.
13. Medyje išplėskite „Intrastat (model)“.
14. Medyje pasirinkite „Intrastat (model)\Intrastat (mapping)“.
15. Spustelėkite Konstruktorius.
    * Atkreipkite dėmesį, kad dabartinio modelio susiejime lauke Kryptis yra reikšmė „Į modelį“. Tai reiškia, kad šis modelio susiejimas buvo sukurtas duomenims iš programos gauti ir jiems saugoti duomenų modelyje.  
16. Spustelėkite Konstruktorius.
17. Medyje išplėskite „List“.
18. Medyje išplėskite „Transactions= List“.
    * Peržiūrėkite modelio susiejimo struktūrą, kuriai naudojamas duomenų modelis, išfiltruotas pagal šakninį elementą „Siunčiamam dokumentui“. Atkreipkite dėmesį, kad įtrauktas duomenų šaltinis, „Sąrašas“, suteikia prieigą prie reikalingų programos duomenų, kurie yra įrašų sąrašas iš Intrastat lentelės.  
19. Uždarykite puslapį.
20. Uždarykite puslapį.
21. Spustelėkite Keitimas.
22. Spustelėkite Įkelti iš XML failo.
    * Importuokite ER formato konfigūraciją, nurodančią Intrastat ataskaitos išdėstymą ir duomenų pateikimo į ataskaitą procesą. Vėliau išplėsite šią formato apibrėžtį duomenims iš Intrastat ataskaitos siųsti į duomenų modelį ir paskui naudoti programos duomenų atnaujinimui, informacijai apie Intrastat ataskaitų procesą archyvuoti.   
    * Spustelėkite Naršyti ir pasirinkite Intrastat (formatas).xml failą.  
23. Spustelėkite GERAI.
24. Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.
25. Spustelėkite Konstruktorius.
26. Spustelėkite Išplėsti / sutraukti.
27. Medyje pasirinkite „File\Declaration“.
28. Spustelėkite skirtuką „Susiejimas“.
29. Medyje pasirinkite „File“.
    * Peržiūrėkite formato, naudojamo Intrastat ataskaitai generuoti, struktūrą. Atkreipkite dėmesį, kad jis skirtas XML failui generuoti užpildant duomenis iš duomenų modelio, kuris grindžiamas šakniniu elementu „Siunčiamam dokumentui“. Patikrinkite, ar sugeneruoto failo pavadinimas apibrėžtas vartotojo dialogo formoje (tam naudojamas „fn“ duomenų šaltinis).   
30. Uždarykite puslapį.


