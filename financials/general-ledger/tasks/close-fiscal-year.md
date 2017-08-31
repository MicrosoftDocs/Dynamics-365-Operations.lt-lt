--- 
title: "Uždaryti finansinius metus"
description: "Šios procedūros veiksmai padeda atlikti metų pabaigos uždarymo procesą, kuriuo balansai perkeliami į kitus finansinius metus."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 83ea19e11596374c3e3ceb051db0b483f4b58583
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="close-the-fiscal-year"></a>Uždaryti finansinius metus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šios procedūros veiksmai padeda atlikti metų pabaigos uždarymo procesą, kuriuo balansai perkeliami į kitus finansinius metus.


## <a name="validate-year-end-close-parameters"></a>Uždarymo metų pabaigoje parametrų tikrinimas
1. Eikite į Didžioji knyga > DK nustatymas > DK parametrai.
2. Išplėskite skyrių Finansinių metų uždarymas.
3. Nustatykite parinktį Perkėlimo metu naikinti metų uždarymo operacijas į Taip arba Ne.
    * Jei finansiniai metai jau uždaryti ir vėl uždarymas metų pabaigoje atliekamas iš naujo, šis parametras yra svarbus. Jei nustatyta parinktis Taip, ankstesnio uždarymo metų pabaigoje kvitas bus panaikintas ir bus sukurtas naujas visų sąskaitų pradžios balansų kvitas. Jei nustatyta parinktis Ne, ankstesnis kvitas panaikintas nebus ir naujas kvitas bus sukurtas tik tiems įrašams, kurie buvo registruoti po paskutinio uždarymo metų pabaigoje, koreguoti.  
4. Nustatykite parinktį Kurti uždarymo operacijas perkėlimo metu į Taip arba Ne.
    * Jei nustatyta parinktis Taip, sukuriamos dvi operacijos. Sukuriamas vienas kvitas, skirtas uždaromiems finansiniams metams, kad pelno ir nuostolių DK sąskaitų balansai būtų lygūs nuliui, ir sukuriamas kitas kvitas, skirtas kitų finansinių metų pradžios balansams. Jei nustatyta parinktis Ne, sukuriamas vienas kvitas, skirtas kitų finansinių metų pradžios balansams.  
5. Nustatykite parinktį Nustatyti finansinių metų būseną kaip Uždaryta visam laikui į Taip arba Ne.
    * Jei nustatyta parinktis Taip, finansinių metų būsena bus nustatyta kaip Uždaryta visam laikui.  Kadangi visam laikui uždaryti metai negali būti iš naujo atidaryti, geriausia būtų nustatyti parinktį Ne.  
6. Nustatykite parinktį Kvito numeris turi būti įvestas vykdant uždarymo metų pabaigoje procesą į Taip arba Ne.
    * Jei nustatyta parinktis Taip, kvito numeris turi būti įvestas neautomatiniu būdu vykdant uždarymo metų pabaigoje procesą. Numeracija nėra naudojama generuojant šį kvito numerį. Geriausia šią parinktį nustatyti į Taip.  
7. Uždarykite puslapį.
8. Pasirinkite Didžioji knyga > Laikotarpio uždarymas > Uždarymas metų pabaigoje.
9. Spustelėkite Naujas, kad sukurtumėte uždarymo metų pabaigoje šabloną.
    * Galima kurti šabloną, skirtą juridinių subjektų, kuriems reikia taikyti uždarymo metų pabaigoje procesą, grupėms. Šį šabloną galima naudoti pakartotinai daugelį metų.  
10. Lauke Grupės pavadinimas įveskite uždarymo metų pabaigoje šablono pavadinimą.
11. Pasirinkti finansinius metus, kuriems kuriamas šablonas bus taikomas.
    * Tik tie juridiniai subjektai, kurie naudoja tuos pačius finansinius metus, gali būti sugrupuoti į uždarymo metų pabaigoje šabloną. Taip yra todėl, kad uždarymas metų pabaigoje atliekamas pasirenkant finansinius metus, o ne datą.  
12. Norėdami įrašyti įrašą, naudokite nuorodą.
13. Spustelėkite Įtraukti ir pasirinkite šio šablono juridinius subjektus.
    * Juridiniai subjektai gali būti įtraukti pasirenkant juridinių subjektus arba pasirenkant organizacijos hierarchiją.  Bus įtraukti tik tie juridiniai asmenys, kurių organizacijos hierarchijoje pasirinktas tas pats finansinis kalendorius.  
14. Pasirinkite juridinius subjektus arba organizacijos hierarchiją.
15. Spustelėkite GERAI.
16. Pasirinkite, ar finansinės dimensijos bus perkeltos į kitus finansinius metus.
    * Geriausia nustatyti šią parinktį į Taip, jei naudojate balanso sąskaitas.  Tokiu būdu finansinės dimensijos liks užregistruotose operacijose, kai kuriami balanso sąskaitų pradžios balansai.  Naudodami pelno ir nuostolio sąskaitas galite pasirinkti išsaugoti finansines dimensijas (uždaryti viską), kai balansai perkeliami į nepaskirstytą pelną, arba galite pasirinkti finansines dimensijas pakeisti kita dimensijos reikšme (uždaryti vieną). Jei pasirinksite Uždaryti vieną, galite nurodyti konkrečią kiekvienos dimensijos reikšmę ar net palikti ją tuščią.  
17. Spustelėkite Įrašyti.
18. Pradėkite uždarymo metų pabaigoje procesą, veiksmų srityje pasirinkdami Uždaryti finansinį laikotarpį.
    * Bus vykdomas pasirinkto šablono uždarymo metų pabaigoje procesas.  
19. Pasirinkite visus arba dalį šablone pateiktų juridinių subjektų, kuriems norite taikyti uždarymo metų pabaigoje procesą.
    * Pirmą kartą vykdant uždarymo metų pabaigoje procesą, organizacijos gali vykdyti visų šablono juridinių subjektų uždarymo metų pabaigoje procesą, kad gautų pradžios balansus. Jei po to sukuriami koregavimo įrašai, galite vykdyti tik pakoreguotų juridinių subjektų uždarymo metų pabaigoje procesą.  
20. Spustelėkite GERAI.
21. Pasirinkite finansinius metus, kuriems norite taikyti uždarymo metų pabaigoje procesą.
22. Lauke Kvitas įveskite reikšmę.
    * Geriausia finansinius metus įtraukti į kvito numerį, kad būtų lengviau rasti uždarymo metų pabaigoje kvitą, kuris buvo sukurtas.  
23. Pagal numatytuosius parametrus uždarymo metų pabaigoje procesas vykdomas paketiniu režimu.
    * Geriausia ilgai trunkančius procesus vykdyti paketiniu režimu. Paprastai tai yra vienas iš tokių procesų, todėl įprasta naudoti paketinį režimą.  
24. Spustelėkite GERAI.


