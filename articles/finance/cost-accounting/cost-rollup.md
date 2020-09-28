---
title: Savikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas
description: Šioje temoje pateikiama informacija apie tai, kaip nustatyti teisingą antrinių išlaidų elementų lygį ir sukurti išlaidų sumavimo taisykles, kurios tiktų pagal organizacijos atskaitomybę ir išlaidų atsekamumą.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostRollupRule, CAMDimensionHierarchy, CAMOverheadRatePolicy
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f07483d0ccb8593f0e7ce8dbd3c83f63ce60d457
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759381"
---
# <a name="cost-rollup-policy-and-overhead-calculation"></a>Savikainos sumavimo strategija ir pridėtinių išlaidų skaičiavimas 

[!include [banner](../includes/banner.md)]

Naudodami kaštų apskaitą galite suprasti, kaip išlaidų srautas susijęs su organizacijoje pristatomais produktais ir paslaugomis. Norint peržiūrėti išlaidų skaidrumą svarbu pasiekti to, kad išlaidos būtų paskirstomos išlaidų objektams pagal atitinkamą paskirstymo pagrindą. Pagal numatytuosius nustatymus yra pasiekiama pirminio išlaidų elemento išlaidų paskirstymo, kurio norima kai kuriais atvejais, bet su juo susijusios keletas įžvalgų, į kurias reikėtų atsižvelgti.

-   Po pridėtinių išlaidų skaičiavimo pirminio išlaidų elemento išlaidų objektų likutis bus nulis.

-   Atlikus pridėtinių išlaidų skaičiavimą sugeneruotų išlaidų įrašų kiekis gali būti labai didelis.

-   Neįmanoma sekti išlaidų objektų išlaidų srauto.

Jeigu norite išvengti šių pasekmių, naudodamiesi kaštų apskaita galite nustatyti, kad išlaidos būtų paskirstomos taip, kad atitiktų jūsų organizacijos valdymo ataskaitų reikalavimus. Šioje temoje aptariama tai, kaip galite nustatyti teisingą antrinių išlaidų elementų lygį ir sukurti išlaidų sumavimo taisykles, kurios tiktų pagal organizacijos atskaitomybę ir išlaidų atsekamumą.

> [!NOTE]
> Pasikeitus ataskaitoms keliamiems reikalavimams konfigūracijas galite keisti.

## <a name="example-of-cost-rollup-policy-setup"></a>Savikainos sumavimo strategijos nustatymo pavyzdys

Įsivaizduokite, kad organizacija yra toliau nurodytos struktūros su 4 išlaidų centrais.

![Organizacijos struktūros pavyzdys](./media/dimension-hierarchy-org.png)

**Savikainos objekto dimensija**

| Išlaidų centrai | aprašymas          |
|--------------|-----------|
| CC001        | Personalas        |
| CC002        | Finansai   |
| CC003        | Surinkimas  |
| CC004        | Pakuotės |

**Savikainos elemento dimensija**

| Savikainos elementai | aprašymas | Tipas    |
|---------------|-------------|---------|
| 1001          | Elektros energija | Pagrindinis |
| 1002          | Atlyginimai    | Pagrindinis |
| 1003          | Reklama | Pagrindinis |

Organizacijos ataskaitoms keliamus reikalavimus atitinkančią dimensijos hierarchiją galima nustatyti toliau nurodytu būdu.

**Dimensijų hierarchijos informacija**

| Dimensijų hierarchijos pavadinimas | Dimensija    | Dimensijų hierarchijos tipo pavadinimas      | Prieigos sąrašo hierarchija |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizacija             | Išlaidų centrai | Dimensijų klasifikavimo hierarchija | Nr.                    |

**Dimensijų hierarchija**

|              | Dimensijos narių intervalai |                     |
|--------------|-------------------------|---------------------|
| **Mazgai**        | **Iš dimensijos nario**   | **Į dimensijos narį** |
| Organizacija |                         |                     |
| &nbsp;&nbsp;Administratorius             |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Finansai              | CC001                   | CC001               |
| &nbsp;&nbsp;&nbsp;&nbsp;Personalas               | CC002                   | CC002               |
| &nbsp;&nbsp;Gamyba               |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakuotės              | CC003                   | CC003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Surinkimas             | CC004                   | CC004               |

Strategijai keliamą reikalavimą atitinkančią dimensijos hierarchiją galima nustatyti toliau nurodytu būdu.

**Dimensijų hierarchijos informacija**

| Dimensijų hierarchijos pavadinimas | Dimensija     | Dimensijų hierarchijos tipo pavadinimas      |
|--------------------------|---------------|------------------------------------|
| Pelno ir nuostolio išrašas  | Savikainos elementai | Dimensijų klasifikavimo hierarchija |

**Dimensijų hierarchija**

|                         | Dimensijos narių intervalai |                     |
|-------------------------|-------------------------|---------------------|
| Mazgai                   | Iš dimensijos nario   | Į dimensijos narį |
| Pelno ir nuostolio išrašas |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Pirminės išlaidos                    | 10001                   | 10003               |

Apdorojus DK įrašus išlaidų įrašo likutis pagal išlaidų objektą atrodo taip.

|                      | **Išlaidų objektas** |           |           |           | **Bendroji suma**     |
|----------------------|-----------------|-----------|-----------|-----------|---------------|
| **Savikainos elementas**     | **CC001**       | **CC002** | **CC003** | **CC004** |               |
| **1001 Elektros energija** | 100,00          | 200,00    | 6.000,00  | 2.000,00  | **8.300,00**  |
| **1002 Atlyginimai**    | 10.000,00       | 10.000,00 | 8.000,00  | 6.500,00  | **34.500,00** |
| **1003 Reklama** | 0,00            | 4.000,00  | 0,00      | 0,00      | **4.000,00**  |
|                      | 10.100,00       | 14.200,00 | 14.000,00 | 8.500,00  | **46.800,00** |

**Statistinė dimensija**

| Statistiniai elementai |    aprašymas   |
|----------------------|------------------|
| SE-1                 | Personalo paslaugos      |
| SE-2                 | Finansų padalinio paslaugos |

Išlaidų objekto CC001 personalas teikia personalo paslaugas keliems išlaidų objektams.

Personalo teikiamomis paslaugomis naudojamasi pagal reikšmės paskirstymą.

| Išlaidų objektas | aprašymas |   Personalo paslaugos |
|-------------|-------------|----|
| CC002       | Finansai     | 35 |
| CC003       | Surinkimas    | 55 |
| CC004       | Pakuotės   | 10 |

Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų.

Finansų padalinio teikiamomis paslaugomis naudojamasi pagal reikšmės paskirstymą.

| Išlaidų objektas |   aprašymas    |  Finansų padalinio paslaugos   |
|-------------|------------------|----|
| CC003       | Surinkimas         | 65 |
| CC004       | Pakuotės        | 35 |

Išlaidų paskirstymo politiką galima nustatyti toliau nurodytu būdu.

| Strategijos pavadinimas | aprašymas     | Savikainos objekto dimensijų hierarchija | Statistinė dimensija | Savikainos elemento dimensija |
|-------------|-----------------|---------------------------------|-----------------------|------------------------|
| 2017        | Išlaidų paskirstymas | Organizacija                    | Statistiniai elementai  | Savikainos elementai          |

Išlaidų paskirstymo taisykles galima nustatyti toliau nurodytu būdu.

| Savikainos objekto dimensijų hierarchijos mazgas | Savikainos veikimo būdas | Paskirstymo bazė        |
|--------------------------------------|---------------|------------------------|
| CC001                                | Iš viso         | **Personalo paslaugos**        |
| CC002                                | Iš viso         | **Finansinės paslaugos** |

<a name="brhow-cost-flows-between-cost-centers"></a><br>Kaip vyksta išlaidų srautas tarp išlaidų centrų 
---------------------------------------------------

Jei norite sužinoti, kaip vyksta išlaidų srautas tarp organizacijos išlaidų centrų, kiekvienam išlaidų centrui galite sukurti išlaidų elementus, kurių tipas **Antrinis**. Po to šie išlaidų elementai bus naudojami perkeliant likučius iš vieno savikainos centro į kitą, kai atliekamas pridėtinių išlaidų skaičiavimas.

Išlaidų elemento dimensijos narius galima nustatyti toliau nurodytu būdu.

| Savikainos elementai | Tipas          |               |
|---------------|---------------|---------------|
| 1001          | Elektros energija   | Pagrindinis       |
| 1002          | Atlyginimai      | Pagrindinis       |
| 1003          | Reklama   | Pagrindinis       |
| **SC-CC001**  | **Personalas**        | **Antrinis** |
| **SC-CC002**  | **Finansai**   | **Antrinis** |
| **SC-CC003**  | **Surinkimas**  | **Antrinis** |
| **SC-CC004**  | **Pakuotės** | **Antrinis** |

Atsiradus nujiems dimensijos nariams dimensijų hierarchiją **Pelno ir nuostolio išrašas** reikia atnaujinti, kad joje būtų pateikti teisingi duomenys, kuriuos galima panaudoti apibrėžiant ataskaitas ir strategijas.

**Dimensijų hierarchijos informacija**

| Dimensijų hierarchijos pavadinimas | Dimensija     | Dimensijų hierarchijos tipo pavadinimas      |
|--------------------------|---------------|------------------------------------|
| Pelno ir nuostolio išrašas  | Savikainos elementai | Dimensijų klasifikavimo hierarchija |

**Dimensijų hierarchija**

|                         | Dimensijos narių intervalai |                     |
|-------------------------|-------------------------|---------------------|
| Mazgai                   | Iš dimensijos nario   | Į dimensijos narį |
| Pelno ir nuostolio išrašas |                         |                     |
| &nbsp;&nbsp;&nbsp;&nbsp;Pirminės išlaidos                        | 10001                   | 10003               |
| &nbsp;&nbsp;&nbsp;&nbsp;Antrinė savikaina                         | **SC-CC001**            | **SC-CC004**        |

Sukurkite **Savikainos sumavimo strategiją**, kurioje kiekvienas išlaidų centras susietas su atitinkamu išlaidų elementu, kurio tipas **Antrinis**.

**Savikainos sumavimo strategijos**

| Strategijos pavadinimas | aprašymas | Savikainos objekto dimensijų hierarchija | Savikainos elemento dimensijų hierarchija |
|-------------|-------------|---------------------------------|----------------------------------|
| 2017        | Išlaidų srautas   | Organizacija                    | Pelno ir nuostolio išrašas          |

**Išlaidų sumavimo taisyklės**

| Savikainos objekto dimensijų hierarchijos mazgas | Savikainos elemento dimensijų hierarchijos mazgas | Antrinis savikainos elementas |
|--------------------------------------|---------------------------------------|------------------------|
| CC001                                | Pelno ir nuostolio išrašas               | **SC-CC001**           |
| CC002                                | Pelno ir nuostolio išrašas               | **SC-CC002**           |
| CC003                                | Pelno ir nuostolio išrašas               | **SC-CC003**           |
| CC004                                | Pelno ir nuostolio išrašas               | **SC-CC004**           |

## <a name="perform-overhead-calculation"></a>Atlikti pridėtinių išlaidų skaičiavimą

**Žurnalas**

| Žurnalas | Žurnalo tipas            | Ataskaitinis kalendorinis laikotarpis | Metai | Laikotarpis | Versija       |
|---------|-------------------------|------------------------|------|--------|---------------|
| 00002   | Savikainos paskirstymo žurnalas | Finansiniai                 | 2017    | 1 laikotarpis | Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis |

Dabar sukūrusi **Išlaidų objekto likučio žurnalo įrašus** sistema taikys **Išlaidų sumavimo strategiją**.

**Savikainos objekto likučio žurnalo įrašai**

| Ataskaitinė data | Išlaidų objektas | aprašymas  | Savikainos elementas | aprašymas |  Suma |
|-----------------|-------------|--------------|----------|-----------|-----------|
| 2017-01-31      | CC001       | Personalas           | SC-CC001 | Personalas        | 10.100,00 |
| 2017-01-31      | CC002       | Finansai      | SC-CC002 | Finansai   | 17.735,00 |
| 2017-01-31      | CC003       | Surinkimas     | SC-CC003 | Surinkimas  | 31.082,75 |
| 2017-01-31      | CC004       | Pakuotės    | SC-CC004 | Pakuotės | 15.717,25 |

> [!NOTE]
> Jeigu esama strategijos, žurnalo įrašai sukuriami pagal **Išlaidų sumavimo strategijoje** nurodytas taisykles. Rodomas likutis yra pridėtinių išlaidų skaičiavimo likutis.

Puslapyje **Išlaidų objekto išlaidų likučio žurnalo įrašo informacija**, kuris pasiekiamas peržiūrint žurnalo įrašus, rodoma, kaip gaunamas likutis.

**Pavyzdys: išlaidų objekto CC002 Finansai žurnalo įrašas**

**Savikainos objekto išlaidų balanso žurnalo įrašo informacija**

| Savikainos elemento dimensijos narys | aprašymas |  Suma   |
|-------------------------------|-------------|-----------|
| 1001                          | Elektros energija | 200,00    |
| 1002                          | Atlyginimai    | 10.000,00 |
| 1003                          | Reklama | 4.000,00  |
| SC-CC001                      | Personalas          | 3.535,00  |

**Atliekant pridėtinių išlaidų skaičiavimą sugeneruoti išlaidų įrašai**

| Išlaidų objektas | aprašymas  | Savikainos elementas   | aprašymas  |        Suma     |       Ataskaitinė data     |
|-------------|--------------|----------|-----------------|-------------|------------|
| CC001       | Personalas           | SC-CC001 | Personalas              | \-10.100,00 | 2017-01-31 |
| CC002       | Finansai      | SC-CC001 | Personalas              | 3.535,00    | 2017-01-31 |
| CC003       | Surinkimas     | SC-CC001 | Personalas              | 5.555,00    | 2017-01-31 |
| CC004       | Pakuotės    | SC-CC001 | Personalas              | 1.010,00    | 2017-01-31 |
| CC002       | Finansai      | SC-CC002 | Finansai         | \-17.735,00 | 2017-01-31 |
| CC003       | Surinkimas     | SC-CC002 | Finansai         | 11.527,75   | 2017-01-31 |
| CC004       | Pakuotės    | SC-CC002 | Finansai         | 6.207,25    | 2017-01-31 |

Atlikę **Pridėtinių išlaidų skaičiavimą** galite pranešti rezultatus naudodami įrankius, pvz., „Microsoft SharePoint Workspace“, „Excel“ arba „Power BI“.

## <a name="view-reporting-in-excel"></a>Peržiūrėti ataskaitas naudojant „Excel“ 

Naudodami dimensijų hierarchijas galite peržiūrėti skirtingų telkimo lygių duomenis.

Toliau pateikiamas „Power Pivot“ ataskaitų kūrimo naudojant „Excel“ pavyzdys.

| **Pelno ir nuostolio išrašas** | **Išlaidų objektas** |                |               |               |  **Bendroji suma**    |
|-----------------------------|-----------------|----------------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002**      | **CC003**     | **CC004**     |               |
| **Pirminės išlaidos**            | **10.100,00**   | **14.200,00**  | **14.000,00** | **8.500,00**  | **46.800,00** |
| &nbsp;&nbsp;&nbsp;&nbsp;1001                            | 100,00          | 200,00         | 6.000,00      | 2.000,00      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                            | 10.000,00       | 10.000,00      | 8.000,00      | 6.500,00      | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                             | 0,00            | 4.000,00       | 0,00          | 0,00          | **4.000,00**  |
|**Antrinė savikaina**                            | **-10.100,00**  | **-14.200,00** | **17,082,75** | **7.217,25**  | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                            | \-10.100,00     | 3.535,00       | 5.555,00      | 1.010,00      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | \-17.735,00    | 11.527,75     | 6.207,25      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                            | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00           | 0,00          | 0,00          | 0,00          |
| **Bendroji suma**                   | **0,00**        | **0,00**       | **31.082,75** | **15.717,25** | **46.800,00** |

Naudodami **Išlaidų sumavimo strategiją** ir **Antrinio tipo išlaidų elementus** galite palikti kiekvieno vidinių ataskaitų išlaidų objekto pradines išlaidas kaip po **Pridėtinių išlaidų skaičiavimo** likusias pradines išlaidas.

Jeigu toks pats pavyzdys būtų buvęs atliktas nesukuriant **Išlaidų sumavimo strategijos,** ataskaitų rezultatas būtų parodytas toliau. Išlaidų srautas teisingas, bet atsekamumo ir įžvalgų, kaip vyksta išlaidų srautas iš vieno išlaidų centro į kitą, nebėra.

| **Pelno ir nuostolio išrašas** | **Išlaidų objektas** |           |               |               |          **Bendroji suma**  |
|-----------------------------|-----------------|-----------|---------------|---------------|---------------|
|                             | **CC001**       | **CC002** | **CC003**     | **CC004**     |               |
| **Pirminės išlaidos**            | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1001                              | 0,00            | 0,00      | 6.207,75      | 2.092,25      | **8.300,00**  |
| &nbsp;&nbsp;&nbsp;&nbsp;1002                             | 0,00            | 0,00      | 22.275,00     | 12.225,00     | **34.500,00** |
|&nbsp;&nbsp;&nbsp;&nbsp;1003                              | 0,00            | 0,00      | 2600,00       | 1.400,00      | **4.000,00**  |
|**Antrinė savikaina**                            | **0,00**        | **0,00**  | **0,00**      | **0,00**      | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC001                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC002                             | 0,00            | 0,00      | 0,00          | 0,00          | **0,00**      |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC003                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
|&nbsp;&nbsp;&nbsp;&nbsp;SC-CC004                             | 0,00            | 0,00      | 0,00          | 0,00          | 0,00          |
| **Bendroji suma**                   | **0,00**        | **0,00**  | **31.082,75** | **15.717,25** | **46.800,00** |

Priklausomai nuo jūsų organizacijoje ataskaitoms ir atsekamumui keliamų reikalavimų, galite nustatyti teisingą antrinių išlaidų elementų lygį ir sukurti išlaidų sumavimo taisykles, kurios atitiktų jūsų poreikius.

Aiškiai atskiriant **Išlaidų paskirstymo** ir **Išlaidų sumavimo strategijas** sukuriamas lankstumas atlikti nepertraukiamus naujinimus taip, kad nebūtų sukeliamas poveikis.



## <a name="additional-resources"></a>Papildomi ištekliai
-  [Savikainos objekto dimensijos](cost-objects.md)
-  [Savikainos elemento dimensijos](cost-elements.md)
-  [Dimensijų hierarchija](dimension-hierarchy.md)
-  [Pridėtinių išlaidų skaičiavimas](overhead-calculation.md)
