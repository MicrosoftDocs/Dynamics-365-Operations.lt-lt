---
title: Uždaryti finansinius metus
description: Šios procedūros veiksmai padeda atlikti metų pabaigos uždarymo procesą, kuriuo balansai perkeliami į kitus finansinius metus.
author: aprilolson
ms.date: 11/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d52e6789a96defaf1d0132fe97fc183a05af207
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779818"
---
# <a name="close-the-fiscal-year"></a>Uždaryti finansinius metus

[!include [banner](../../includes/banner.md)]

Šios procedūros veiksmai padeda atlikti metų pabaigos uždarymo procesą, kuriuo balansai perkeliami į kitus finansinius metus.


## <a name="validate-year-end-close-parameters"></a>Uždarymo metų pabaigoje parametrų tikrinimas
1. Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Didžiosios knygos nustatymas > Didžiosios knygos parametrai**.
2. Išplėskite skyrių **Finansinių metų uždarymas**.
3. Pasirinkite **Taip** arba **Ne** norėdami **perkėlimo pasirinkties metu naikinti metų uždarymo operacijas**.
    
Jei finansiniai metai jau uždaryti ir vėl uždarymas metų pabaigoje atliekamas iš naujo, šis parametras yra svarbus. Jei nustatyta **Taip**, ankstesnio metų pabaigos uždarymo kvitas bus panaikintas ir bus sukurtas naujas visų sąskaitų pradžios balansų kvitas. Jei nustatyta **Ne**, ankstesnis kvitas liks, o naujas kvitas bus sukurtas tik įrašų, užregistruotų po paskutinių metų pabaigos uždarymo, koregavimams.

4. Pasirinkti **Taip** arba **Ne,** jei norite kurti **uždarymo operacijas perkėlimo metu**.

Jei nustatyta **Taip**, sukuriamos dvi operacijos. Finansiniais metais sukuriamas vienas kvitas, skirtas visų DK sąskaitų balansams suskurti iki nulio, o kitais finansiniais metais pradžios balansų kvitas sukuriamas antras kvitas. Jei nustatyta **Ne**, per kitus pradžios balansų finansinius metus sukuriamas vienas kvitas.  

5. Pasirinkite **Taip** arba **Ne, norėdami** nustatyti **finansinių metų būseną kaip visiškai uždarytą**.

Jei nustatyta **Taip**, finansinių metų būsena bus nustatyta visam laikui **uždaryta.** Kadangi visam laikui uždarytų metų negalima atidaryti iš naujo, geriausia nustatyti šią pasirinktį kaip **Ne**.  

6. Pasirinkite **Taip** arba **Ne**, jei **norite nurodyti kvito numerį, kuris turi būti užpildytas metų pabaigos uždarymo pasirinkties** metu.

Jei nustatyta **Taip**, kvito numeris turi būti įvestas rankiniu būdu metų pabaigos uždarymo proceso metu. Numeracija nėra naudojama generuojant šį kvito numerį. Geriausia tai nustatyti kaip **Taip**.  

7. Uždarykite puslapį.
8. Pasirinkite **Didžioji knyga > Laikotarpio uždarymas > Uždarymas metų pabaigoje**.
9. Spustelėkite **Naujas**, kad sukurtumėte uždarymo metų pabaigoje šabloną.

Galima kurti šabloną, skirtą juridinių subjektų, kuriems reikia taikyti uždarymo metų pabaigoje procesą, grupėms. Šį šabloną galima naudoti pakartotinai daugelį metų.  

10. **Lauke Grupės pavadinimas** įveskite metų pabaigos uždarymo šablono pavadinimą.
11. Lauke **Finansinis kalendorius** pasirinkite finansinius metus, kuriems bus sukurtas šablonas.

Tik tie juridiniai subjektai, kurie naudoja tuos pačius finansinius metus, gali būti sugrupuoti į uždarymo metų pabaigoje šabloną. Taip yra todėl, kad uždarymas metų pabaigoje atliekamas pasirenkant finansinius metus, o ne datą.  

12. Dalyje **Veiksmų sritis** spustelėkite **Įrašyti**.
13. Skyriuje **Juridiniai subjektai** spustelėkite **Įtraukti**, kad pasirinktumėte šio šablono juridinius subjektus.
    
Juridiniai subjektai gali būti įtraukti pasirenkant juridinių subjektus arba pasirenkant organizacijos hierarchiją. Bus įtraukti tik tie juridiniai asmenys, kurių organizacijos hierarchijoje pasirinktas tas pats finansinis kalendorius.  

14. Pasirinkite juridinius subjektus arba organizacijos hierarchiją.
15. Spustelėkite **Gerai**.
16. Balanso **dimensijos** balanse **pasirinkite** **Taip arba Ne**.

Geriausia nustatyti šią pasirinktį kaip Taip balanso **sąskaitose**. Tokiu būdu finansinės dimensijos liks užregistruotose operacijose, kai kuriami balanso sąskaitų pradžios balansai. Pelno ir nuostolio sąskaitose galite pasirinkti prižiūrėti finansines dimensijas (**Uždaryti** viską), kai balansai perkeliami į nepaskirstytas pelnas, arba galite pasirinkti, kad finansinės dimensijos būtų pakeistos kita dimensijos reikšme (**uždaryti vieną**). Jei pasirinksite Uždaryti **vieną**, galėsite nurodyti konkrečią kiekvienos dimensijos vertę arba net pasirinkti, kad ji būtų tuščia.  

17. Spustelėkite **Įrašyti**.
18. Pradėkite uždarymo metų pabaigos procesą, dalyje **Veiksmų sritis** pasirinkdami **Uždaryti finansinį laikotarpį**. Bus vykdomas pasirinkto šablono uždarymo metų pabaigoje procesas.  
19. Pasirinkite visus arba dalį šablone pateiktų juridinių subjektų, kuriems norite taikyti uždarymo metų pabaigoje procesą.

Pirmą kartą vykdant uždarymo metų pabaigoje procesą, organizacijos gali vykdyti visų šablono juridinių subjektų uždarymo metų pabaigoje procesą, kad gautų pradžios balansus. Jei po to sukuriami koregavimo įrašai, galite vykdyti tik pakoreguotų juridinių subjektų uždarymo metų pabaigoje procesą.  

20. Spustelėkite **Gerai**.
21. Pasirinkite finansinius metus, kuriems norite taikyti uždarymo metų pabaigoje procesą.
22. Dalyje **Kvito laukas** įveskite reikšmę. Geriausia finansinius metus įtraukti į kvito numerį, kad būtų lengviau rasti uždarymo metų pabaigoje kvitą, kuris buvo sukurtas.  
23. Pagal numatytuosius parametrus uždarymo metų pabaigoje procesas vykdomas paketiniu režimu. Geriausia ilgai trunkančius procesus vykdyti paketiniu režimu. Paprastai tai yra vienas iš tokių procesų, todėl įprasta naudoti paketinį režimą.  
24. Spustelėkite **Gerai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
