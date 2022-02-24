---
title: EUR-00002 ES Intrastat deklaracijos generavimas
description: Šia procedūra rodomi veiksmai, kuriuos reikia atlikti norint elektroniniu failo formatu eksportuoti Intrastat deklaraciją ir „Excel‟ formatu peržiūrėti deklaracijos duomenis.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2aba5caaaf0fbee511e1a293b09fa8301bb6831
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408244"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a>EUR-00002 ES Intrastat deklaracijos generavimas

[!include [banner](../../includes/banner.md)]

Šia procedūra rodomi veiksmai, kuriuos reikia atlikti norint elektroniniu failo formatu eksportuoti Intrastat deklaraciją ir „Excel‟ formatu peržiūrėti deklaracijos duomenis. 

Kol operacijų neperkelsite į Intrastat, tol negalėsite atlikti šios procedūros. 

Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.


## <a name="import-configurations-with-settings"></a>Konfigūracijų su parametrais importavimas
1. Pasirinkite Darbo sritys > Elektroninės ataskaitos
2. Spustelėkite Nustatyti kaip aktyvų.
3. Spustelėkite Saugyklos.
4. Spustelėkite Atidaryti.
5. Atidarykite stulpelio filtrą Konfigūracijos pavadinimas.
6. Lauke Konfigūracijos pavadinimas pritaikykite filtrą, naudodami reikšmę „Intrastat (DE)‟ ir filtro operatorių „prasideda‟.
    * Turėtumėte pasirinkti tinkamą jūsų juridinio subjekto šalies konfigūracijos pavadinimą. Šioje procedūroje kaip pavyzdys naudojamas Vokietijos juridinis subjektas (DEMF), todėl reikėtų pasirinkti „Intrastat (DE)".  
    * Spustelėkite Importuoti, tada spustelėkite Taip.  
7. Atidarykite stulpelio filtrą Konfigūracijos pavadinimas.
8. Lauke Konfigūracijos pavadinimas pritaikykite filtrą, naudodami reikšmę „Intrastat ataskaita‟ ir filtro operatorių „prasideda‟.
    * Spustelėkite Importuoti, tada spustelėkite Taip.  

## <a name="set-up-foreign-trade-parameters"></a>Užsienio prekybos parametrų nustatymas
1. Pasirinkite Mokesčiai > Nustatymai > Užsienio prekyba > Užsienio prekybos parametrai.
2. Išplėskite skyrių Elektroninės ataskaitos.
3. Lauke Failo formato susiejimas įveskite arba pasirinkite reikšmę Intrastat (DE).
4. Lauke Ataskaitos formato susiejimas įveskite arba pasirinkite reikšmę Intrastat ataskaita.
5. Išplėskite skyrių Apvalinimo taisyklės.
    * Turėtumėte nustatyti Intrastat ataskaitų apvalinimo taisykles, taikomas jūsų šalyje / regione.  
6. Lauke Apvalinimo taisyklė įveskite skaičių.
    * Įveskite apvalinimo tikslumą, pavyzdžiui, įveskite „0,01‟.  
7. Lauke Sumos skaitmenų po kablelio skaičius įveskite skaičių.
    * Pvz., įveskite „2‟.  
8. Lauke Apvalinimas žemiau 1 kg pasirinkite parinktį.
    * Pavyzdžiui, pasirinkite Apvalinimas iki 1 kg.  
9. Lauke Apvalinimo taisyklė įveskite skaičių.
    * Pavyzdžiui, įveskite „1‟, kad svorį apvalintumėte iki sveikojo skaičiaus.  
10. Išplėskite dalį Mažiausia riba.
11. Lauke Svoris įveskite skaičių.
    * Pavyzdžiui, kaip mažiausią svorį įveskite „10‟.  
12. Lauke Suma įveskite skaičių.
    * Pavyzdžiui, kaip mažiausią sumą įveskite „200‟.  
13. Lauke Prekė įveskite arba pasirinkite reikšmę.

## <a name="set-up-compression-of-intrastat"></a>Intrastat glaudinimo nustatymas
1. Pasirinkite Mokesčiai > Nustatymas > Užsienio prekyba > Intrastat glaudinimas.
2. Spustelėkite Šalinti.
3. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pavyzdžiui, dalyje Yra pasirinkite Prekė.  
4. Spustelėkite Pridėti.

## <a name="generate-intrastat-declaration"></a>Intrastat deklaracijos generavimas
1. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat
2. Spustelėkite Tikrinti.
    * Tikrinama pagal puslapio Užsienio prekybos parametrai lauką Tikrinti nustatymus.  
3. Spustelėkite GERAI.
4. Spustelėkite Naujinti.
5. Spustelėkite Mažiausia riba.
6. Lauke Pradžios data įveskite datą.
    * Pvz., įveskite 2015 m. sausio 1 d.  
7. Lauke Glaudinti pasirinkite Taip.
8. Lauke Pabaigos data įveskite datą.
    * Pvz., įveskite 2015 m. sausio 31 d.  
9. Spustelėkite GERAI.
10. Spustelėkite Naujinti.
11. Spustelėkite Glaudinti.
    * Šis glaudinimas vyksta atsižvelgiant į tai, kaip nustatėte Intrastat glaudinimo parametrus.  
12. Lauke Pradžios data įveskite datą.
    * Pvz., įveskite 2015 m. sausio 1 d.  
13. Lauke Pabaigos data įveskite datą.
    * Pvz., įveskite 2015 m. sausio 31 d.  
14. Spustelėkite GERAI.
15. Spustelėkite Naujinti.
16. Spustelėkite Regeneruoti eilės numerius.
17. Spustelėkite GERAI.
18. Spustelėkite Išvestis.
19. Spustelėkite Ataskaita.
20. Lauke Pradžios data įveskite pirmąją ataskaitinio laikotarpio datą.
    * Pavyzdžiui, nustatykite datą 2015 m. sausio 1 d.  
21. Lauke Pabaigos data įveskite datą.
    * Pvz., įveskite 2015 m. sausio 31 d.  
22. Lauke Generuoti failą pasirinkite Taip.
23. Lauke „Failo pavadinimas“ suveskite reikšmę.
24. Lauke Generuoti ataskaitą pasirinkite Taip.
25. Lauke Ataskaitos failo pavadinimas įveskite reikšmę.
26. Lauke Kryptis pasirinkite parinktį.
    * Pavyzdžiui, pasirinkite Išsiuntimai.  
27. Spustelėkite GERAI.

