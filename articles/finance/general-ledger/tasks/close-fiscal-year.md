---
title: Uždaryti finansinius metus
description: Šios procedūros veiksmai padeda atlikti metų pabaigos uždarymo procesą, kuriuo balansai perkeliami į kitus finansinius metus.
author: aprilolson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 013a5b1ac5b99c6a8ac75885e6d65067d5ed4c2ffd5cc5f625a73963666c0a81
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779511"
---
# <a name="close-the-fiscal-year"></a>Uždaryti finansinius metus

[!include [banner](../../includes/banner.md)]

Šios procedūros veiksmai padeda atlikti metų pabaigos uždarymo procesą, kuriuo balansai perkeliami į kitus finansinius metus.


## <a name="validate-year-end-close-parameters"></a>Uždarymo metų pabaigoje parametrų tikrinimas
1. Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Didžiosios knygos nustatymas > Didžiosios knygos parametrai**.
2. Išplėskite skyrių **Finansinių metų uždarymas**.
3. Nustatykite parinktį **Perkėlimo metu naikinti metų uždarymo operacijas** į Taip arba Ne.
    
    Jei finansiniai metai jau uždaryti ir vėl uždarymas metų pabaigoje atliekamas iš naujo, šis parametras yra svarbus. Jei nustatyta parinktis Taip, ankstesnio uždarymo metų pabaigoje kvitas bus panaikintas ir bus sukurtas naujas visų sąskaitų pradžios balansų kvitas. Jei nustatyta parinktis Ne, ankstesnis kvitas panaikintas nebus ir naujas kvitas bus sukurtas tik tiems įrašams, kurie buvo registruoti po paskutinio uždarymo metų pabaigoje, koreguoti.

4. Nustatykite parinktį **Kurti uždarymo operacijas perkėlimo metu** į Taip arba Ne.

    Jei nustatyta parinktis Taip, sukuriamos dvi operacijos. Sukuriamas vienas kvitas, skirtas uždaromiems finansiniams metams, kad pelno ir nuostolių DK sąskaitų balansai būtų lygūs nuliui, ir sukuriamas kitas kvitas, skirtas kitų finansinių metų pradžios balansams. Jei nustatyta parinktis Ne, sukuriamas vienas kvitas, skirtas kitų finansinių metų pradžios balansams.  

5. Nustatykite parinktį **Nustatyti finansinių metų būseną kaip Uždaryta visam laikui** į Taip arba Ne.

    Jei nustatyta parinktis Taip, finansinių metų būsena bus nustatyta kaip Uždaryta visam laikui.  Kadangi visam laikui uždaryti metai negali būti iš naujo atidaryti, geriausia būtų nustatyti parinktį Ne.  

6. Nustatykite parinktį **Kvito numeris turi būti įvestas vykdant uždarymo metų pabaigoje procesą** į Taip arba Ne.

    Jei nustatyta parinktis Taip, kvito numeris turi būti įvestas neautomatiniu būdu vykdant uždarymo metų pabaigoje procesą. Numeracija nėra naudojama generuojant šį kvito numerį. Geriausia šią parinktį nustatyti į Taip.  

7. Uždarykite puslapį.
8. Pasirinkite **Didžioji knyga > Laikotarpio uždarymas > Uždarymas metų pabaigoje**.
9. Spustelėkite **Naujas**, kad sukurtumėte uždarymo metų pabaigoje šabloną.

    Galima kurti šabloną, skirtą juridinių subjektų, kuriems reikia taikyti uždarymo metų pabaigoje procesą, grupėms. Šį šabloną galima naudoti pakartotinai daugelį metų.  

10. Lauke **Grupės pavadinimas** įveskite uždarymo metų pabaigoje šablono pavadinimą.
11. Lauke **Finansinis kalendorius** pasirinkite finansinius metus, kuriems bus sukurtas šablonas.

    Tik tie juridiniai subjektai, kurie naudoja tuos pačius finansinius metus, gali būti sugrupuoti į uždarymo metų pabaigoje šabloną. Taip yra todėl, kad uždarymas metų pabaigoje atliekamas pasirenkant finansinius metus, o ne datą.  

12. Dalyje **Veiksmų sritis** spustelėkite **Įrašyti**.
13. Skyriuje **Juridiniai subjektai** spustelėkite **Įtraukti**, kad pasirinktumėte šio šablono juridinius subjektus.
    
    Juridiniai subjektai gali būti įtraukti pasirenkant juridinių subjektus arba pasirenkant organizacijos hierarchiją.  Bus įtraukti tik tie juridiniai asmenys, kurių organizacijos hierarchijoje pasirinktas tas pats finansinis kalendorius.  

14. Pasirinkite juridinius subjektus arba organizacijos hierarchiją.
15. Spustelėkite **Gerai**.
16. Pasirinkite Taip arba Ne dalyje **Perkelti balanso dimensiją**.

    Geriausia nustatyti šią parinktį į Taip, jei naudojate balanso sąskaitas. Tokiu būdu finansinės dimensijos liks užregistruotose operacijose, kai kuriami balanso sąskaitų pradžios balansai. Naudodami pelno ir nuostolio sąskaitas galite pasirinkti išsaugoti finansines dimensijas (uždaryti viską), kai balansai perkeliami į nepaskirstytą pelną, arba galite pasirinkti finansines dimensijas pakeisti kita dimensijos reikšme (uždaryti vieną). Jei pasirinksite Uždaryti vieną, galite nurodyti konkrečią kiekvienos dimensijos reikšmę ar net palikti ją tuščią.  

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