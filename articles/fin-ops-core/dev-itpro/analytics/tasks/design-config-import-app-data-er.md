---
title: ER konfigūracijų kūrimas siekiant išanalizuoti gaunamus dokumentus
description: Šioje procedūroje parodoma, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint analizuoti gaunamą elektroninį dokumentą.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 446a4676ad00c93d691d3048408c32d7ad373d2d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682098"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>ER konfigūracijų kūrimas siekiant išanalizuoti gaunamus dokumentus

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint analizuoti gaunamą elektroninį dokumentą. Šios procedūros metu importuosite reikiamas ER formato konfigūracijas, sukurtas pavyzdinei įmonei „Litware, Inc.“, ir jas panaudosite gaunamų elektroninių dokumentų analizei. Norėdami baigti šios procedūros veiksmus, pirmiausia turite atlikti procedūrą „ER sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“.

Ši procedūra sukurta vartotojams, kuriems priskirtas vaidmuo Sistemos administratorius arba Elektroninių ataskaitų teikimo programuotojas.

Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį. Prieš pradėdami atsisiųskite ir išsaugokite failus, pateiktus temoje „Gaunamų dokumentų analizė siekiant atnaujinti prašymų duomenis“ ([Gaunamų dokumentų analizė](../parse-incoming-electronic-documents.md)). Turimi omenyje šie failai: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros „Kurkite konfigūracijos teikėją ir pažymėkite kaip aktyvų” veiksmus.
2. Pasirinkite Ataskaitų konfigūracijos.
    * Toliau pateikiamas scenarijus bus naudojamas norint nurodyti XML formatu pateiktų gaunamų elektroninių dokumentų analizavimo galimybes: ERP programa reikalauja duomenų iš žiniatinklio tarnybos (pvz., [eftsa](http://efsta.org/) finansų tarnybos) ir analizuoja gaunamus atsakymus, kad būtų galima atitinkamai atnaujinti programos duomenis. Siekiant, kad analizavimas būtų efektyviausias naudojamas vienas ER formatas, nepaisant to, kad laukiamų gaunamų XML formatu pateikiamų dokumentų struktūra skiriasi.

## <a name="import-and-review-er-configurations"></a>Importuoti ir peržiūrėti ER konfigūracijas

Importuokite ER modelio konfigūraciją, kurioje yra duomenų modelio pavyzdys, skirtas saugoti informaciją apie gaunamą failą.

1. Pasirinkite Keitimas.
2. Pasirinkite Įkelti iš XML failo.
    * Pasirinkite Naršyti ir pasirinkite failą EFSTA model.xml.
3. Pasirinkite Gerai.
4. Medyje pasirinkite „EFSTA model“ (EFSTA modelis).
5. Pasirinkite Dizaino įrankis.
    * Peržiūrėkite importuoto duomenų modelio struktūrą. Nurodoma, jog išvardijimas „enumType“ turėtų atpažinti šių tipų aptarnavimo atsakymus: gauti patvirtinimą apie operacijos pateikimą, gauti informacijos apie paskutinę pateiktą operaciją ir atpažinti nepalaikomo tipo atsakymus.
6. Medyje išplėskite „Response“ (atsakymas).
    * Nurodoma, jog šakninis elementas „Atsakymas“ turėtų nurodyti, kokio tipo duomenys turi būti paimami iš palaikomo aptarnavimo atsakymo, kad būtų galima atitinkamai atnaujinti programos duomenis.
7. Uždarykite puslapį.
    * Importuosite ER formato konfigūraciją, kurioje nurodoma, kaip bus išanalizuoti gaunami dokumentai, kad būtų galima saugoti duomenis ER duomenų modelyje.
8. Pasirinkite Keitimas.
9. Pasirinkite Įkelti iš XML failo.
    * Pasirinkite Naršyti ir pasirinkite failą EFSTA format.xml.
10. Pasirinkite Gerai.
11. Medyje išplėskite „EFSTA model“ (EFSTA modelis).
12. Medyje pasirinkite „EFSTA modelis\EFSTA formatas“.
13. Pasirinkite Dizaino įrankis.
14. Pasirinkite Išplėsti / sutraukti.
    * Formato CASE (atvejis) elementas naudojamas kaip šaknis ir apima tris įdėtuosius FILE (failo) elementus, o tai reiškia, kad šis formatas buvo sukurtas kelių formatų gaunamiems failams analizuoti.
15. Medyje pasirinkite „Atsakymai\Operacijos užbaigimas\TraC“.
    * Atsakymas į užklausą apie pateiktą operaciją prasideda šakniniu elementu „TraC“.
16. Medyje pasirinkite „Atsakymai\Paskutinės operacijos užklausa\Tra“.
    * Atsakymas į užklausą apie paskutinę pateiktą operaciją prasideda šakniniu elementu „Era“.
17. Medyje pasirinkite „Atsakymai\Netikėtas atsakymas\Tekstas“.
    * Įtrauktas trečiasis FILE (failo) elementas su įdėtuoju TEXT (teksto) elementu, kad būtų galima atpažinti kitų tipų atsakymus, kurie skiriasi nuo anksčiau minėto atsakymo.
18. Pasirinkite Susieti formatą su modeliu.
    * Šis modelis susiejimas apima duomenų srauto apibrėžimą, kad būtų galima saugoti informaciją apie gaunamą išanalizuotą dokumentą naudojant duomenų modelio elementus.
19. Pasirinkite Dizaino įrankis.
20. Medyje išplėskite „format“.
21. Medyje išplėskite „formatas\Atsakymai: atvejis(atsakymai)“.
    * Peržiūrėkite „formato“ duomenų šaltinio struktūrą. Visi trys atsakymų tipai pateikiami atskirai.
22. Medyje pasirinkite „formatas\Atsakymai: atvejis(atsakymai)\aTipas“.
    * Įtrauktas duomenų šaltinio elementas „aType“, kuriame būtų galima nurodyti atsakymo tipą ir kuris susietas su duomenų modelio elementu „Type“ (tipas).
23. Pasirinkite skirtuką Tikrinimai.
24. Medyje pasirinkite „Type = format.Responses.aType“ (tipas = formatas, atsakymai, a tipas).
    * Sukonfigūruota, jog ER tikrinimas informuotų vartotoją apie situaciją, kai atsakymo struktūra neatitinka patvirtinimo apie operacijos pateikimą arba informacijos apie paskutinę pateiktą operaciją (nepalaikomo atsakymo atvejis).
25. Uždarykite puslapį.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Paleisti ER formato, sukonfigūruoto analizuoti gaunamus failus, modelio susiejimą

Vykdysite sukurto modelio susiejimą, kad galėtumėte jį patikrinti ir pamatyti, kaip sukonfigūruotas ER formatas išanalizuos gaunamus aptarnavimo atsakymus. Šis veiksmas naudoja skirtingus XML failus, kad būtų galima imituoti skirtingų tipų žiniatinklio tarnybos atsakymus.

1. Atidarykite failą Response1.xml naudodami bet kurį xml skaitytuvą, pvz., interneto naršyklę. Šiame faile nurodoma patvirtinimo informacija apie užbaigtą operaciją („TraC“ yra šakninis elementas).
2. Pasirinkite Vykdyti.
    * Pasirinkite Naršyti ir pasirinkite failą Response1.xml.
3. Pasirinkite Gerai.
    * Peržiūrėkite sugeneruotą išvestį. Atsakymo tipas tinkamai atpažintas ir išanalizuotas (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` reiškia operacijos užbaigimo atvejį).
    * Atidarykite failą Response2.xml naudodami XML skaitytuvą. Šiame faile nurodoma informacija apie paskutinę pateiktą operaciją („`Tra`“ yra šakninis elementas).
4. Pasirinkite Vykdyti.
    * Pasirinkite Naršyti ir pasirinkite failą Response2.xml.
5. Pasirinkite Gerai.
    * Peržiūrėkite sugeneruotą išvestį. Atsakymo tipas tinkamai atpažintas ir išanalizuotas (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` reiškia sistemos paleidimo iš naujo atvejį).
    * Atidarykite failą Response3.xml naudodami XML skaitytuvą. Šis failas prasideda TraZ šakniniu elementu ir ši struktūra nėra sukonfigūruota naudoti ER formatą.
6. Pasirinkite Vykdyti.
    * Pasirinkite Naršyti ir pasirinkite failą Response3.xml.
7. Pasirinkite Gerai.
    * Peržiūrėkite sugeneruotą išvestį. Atsakymo tipas tinkamai pripažintas kaip nepalaikomas (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Sistemos pranešime pateiktas atitinkamas pranešimas (pagal ER tikrinimo nustatymą) ir didžioji duomenų modelio dalis nenurodyta.
    * Atidarykite failą Response4.xml naudodami XML skaitytuvą. Šio failo struktūra beveik tokia pati kaip sėkmingai išanalizuoto failo Response1.xml, skiriasi tik šakninio elemento „TraC“ įdėtųjų elementų seka.
8. Pasirinkite Vykdyti.
    * Pasirinkite Naršyti ir pasirinkite failą Response4.xml.
9. Pasirinkite Gerai.
    * Peržiūrėkite sugeneruotą išvestį. Atsakymo tipas tinkamai pripažintas kaip nepalaikomas (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Sistemos pranešime pateiktas atitinkamas pranešimas ir didžioji duomenų modelio dalis nenurodyta. Taip yra todėl, kad naudojant dabartinį šio ER formato nustatymą manoma, kad naudojama tam tikra gaunamo failo šakninio elemento įdėtųjų elementų seka.
10. Uždarykite puslapį.
11. Medyje pasirinkite „Atsakymai\Operacijos užbaigimas\TraC“.
12. Lauke Įdėtųjų elementų analizavimo tvarka pasirinkite „Any“ (bet kuri).
    * Lauke „Įdėtųjų elementų analizavimo tvarka“ pasirinkite Bet kuri, kad šiam šakniniam XML elementui būtų galima naudoti bet kokią įdėtųjų elementų seką.
13. Pasirinkite Įrašyti.
14. Pasirinkite Susieti formatą su modeliu.
15. Pasirinkite Vykdyti.
    * Pasirinkite Naršyti ir pasirinkite failą Response4.xml.
16. Pasirinkite Gerai.
    * Peržiūrėkite sugeneruotą išvestį. Atsakymo tipas dabar tinkamai pripažintas kaip lygus failo Response1.xml tipui.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]