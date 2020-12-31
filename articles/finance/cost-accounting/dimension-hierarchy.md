---
title: Dimensijų hierarchija
description: Šioje temoje pateikiama informacijos apie dimensijų hierarchijas. Dimensijų hierarchija naudojama kaštų apskaitoje norint nurodyti ataskaitų struktūrą, išlaidų strategijas ir saugos nustatymus.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71ba02fc6be4ab9a7871c10a9f95c474e52ae765
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445910"
---
# <a name="dimension-hierarchy"></a>Dimensijų hierarchija

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacijos apie dimensijų hierarchijas. Dimensijų hierarchija naudojama kaštų apskaitoje norint nurodyti ataskaitų struktūrą, išlaidų strategijas ir saugos nustatymus.  

## <a name="overview"></a>Apžvalga

Dimensijų hierarchijos naudojamos įvairiose kaštų apskaitos vietose. Naudodami dimensijų hierarchiją galite nurodyti šią informaciją:

-  Organizacijos reikalavimus atitinkančią ataskaitų struktūrą
-  Savikainos strategijos
-  Saugos nustatymai

Čia pateikiamas dimensijų hierarchijos pavyzdys.

![Dimensijų hierarchijos pavyzdys](./media/dimension-hierarchy.png)

Dimensijų hierarchiją galima sukurti šių tipų dimensijoms:

-  Savikainos elemento dimensijos
-  Savikainos objekto dimensijos
-  Statistinės dimensijos

> [!NOTE]
> - Jeigu reikalingos skirtingos perspektyvos, galite sukurti kelias tos pačios dimensijos dimensijų hierarchijas.
> - Dimensijų hierarchija gali būti susieta tik su viena dimensija.
> - Dimensijų hierarchijos struktūros lygiai gali būti neriboti. Visi lygiai nurodomi darbo srityje **Išlaidų kontrolė**. Kai „Microsoft Excel“ arba „Microsoft Power BI“ naudojate ataskaitų rengimo tikslais, eksportuojami tik pirmi 15 dimensijų hierarchijos lygių. Šis apribojimas nustatomas todėl, kad naudojant „Excel“ ir „Power BI“ reikalinga ilgalaikė schema.
> - Dimensijų hierarchija nėra įsigaliojanti nuo tam tikros datos. Todėl bet kokie dimensijų hierarchijai atlikti pakeitimai iš karto įrašomi į įrašą ir negalima palyginti datos prieš su data po.

## <a name="dimension-hierarchy-type"></a>Dimensijų hierarchijos tipas

Kai sukuriate naują dimenijų hierarchiją, turite pasirinkti hierarchijos tipą. Eikite į **Kaštų apskaita** > **Dimensijos** > **Dimensijų hierarchijos**. Spustelėkite **Naujas** ir pasirinkite dimensijų hierarchijos tipą. Galite pasirinkti **Dimensijų kategorizavimo hierarchija** arba **Dimensijų klasifikavimo hierarchija**.

### <a name="dimension-categorization-hierarchy"></a>Dimensijų klasifikavimo hierarchija

Tipas **Dimensijų kategorizavimo hierarchija** naudojamas ataskaitų rengimo tikslais. Jis palaiko tik išlaidų elemento dimensijas. Pasirinkus šį tipą taikomos šios taisyklės:

-  Dimensijos narys hierarchijos struktūroje gali būti susietas daugiau nei vieną kartą.
-  Lapo mazgui priskirdami išlaidų veikimo būdą išlaidų elemento dimensijos narį galite įdėti į įvairius mazgus.

### <a name="dimension-classification-hierarchy"></a>Dimensijų klasifikavimo hierarchija

Tipas **Dimensijų klasifikacijos hierarchija** naudojamas norint apibrėžti taisykles ir ataskaitų rengimo tikslais. Jis palaiko visas dimensijas, pavyzdžiui, išlaidų objektus, išlaidų elementus ir statistines dimensijas. Pasirinkus šį tipą dimensijos narys hierarchijos struktūroje gali būti susietas tik vieną kartą.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Dimensijų hierarchijos kūrimas ir priežiūra

Dimensijų hierarchija sukuriama kaip mazgą turinti ir lapo mazgo ryšiais pasižyminti medžio struktūra.

-  Mazge gali būti antrinių mazgų – 1:_n_.
-  Mazgui negali būti priskirta antrinių mazgų ir lapų mazgų.
-  Lapo mazgas gali būti priskirtas tik žemiausiame hierarchijos lygmenyje.

### <a name="example"></a>Pavyzdys

Mažai įmonei būdinga tokia organizacijos struktūra, kai finansų ir žmogiškųjų išteklių skyriai yra administraciniai, o surinkimo ir pakavimo skyriai yra gamybos skyriai.

![Organizacijos struktūros pavyzdys](./media/dimension-hierarchy-org.png)

Savikainos objekto dimensija apima visus organizacijos išlaidų centrus.

- Savikainos objekto dimensija
    - Išlaidų centrai

Savikainos objekto dimensiją, kurią sudaro visi išlaidos centrai, galima nustatyti kaip parodyta čia.

| Išlaidų centrai | aprašymas |
|--------------|-------------|
| CC001        | Personalas          |
| CC002        | Finansai     |
| CC003        | Mokesčiai         |
| CC007        | AR/AP       |
| CC005        | Surinkimas    |
| CC006        | Pakuotės   |

Savikainos elemento dimensija apima visus organizacijos savikainos elementus.

- Savikainos elemento dimensija
    - Savikainos elementai

Savikainos elemento dimensiją, kurią sudaro visi savikainos elementai, galima nustatyti kaip parodyta čia.

| Savikainos elementai | aprašymas |
|---------------|-------------|
| 10001         | Elektros energija |
| 10010         | Valymas    |
| 10011         | Šildymas     |
| 40001         | PPK        |

Organizacijos ataskaitoms keliamus reikalavimus atitinkančią dimensijos hierarchiją galima nustatyti kaip parodyta čia.

**Dimensijų hierarchijos informacija**

| Dimensijų hierarchijos pavadinimas | Dimensija    | Dimensijų hierarchijos tipo pavadinimas      | Prieigos sąrašo hierarchija |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizacija             | Išlaidų centrai | Dimensijų klasifikavimo hierarchija | Nr.                    |

Ataskaitų rengimui skirtą dimensijų hierarchiją galima nustatyti kaip parodyta čia.

|                   | Dimensijos narių intervalai   |                         |
|-------------------|---------------------------|-------------------------|
| **Mazgai**         | **Iš dimensijos nario** | **Į dimensijos narį** |
| Organizacija      |                           |                         |
| &nbsp;&nbsp;Administratorius         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Finansai   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personalas        | CC001                     | CC001                   |
| &nbsp;&nbsp;Gamyba    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakuotės | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Surinkimas  | CC006                     | CC006                   |

Strategijai keliamus reikalavimus atitinkančią dimensijos hierarchiją galima nustatyti kaip parodyta čia.

**Dimensijų hierarchijos informacija**

| Dimensijų hierarchijos pavadinimas | Dimensija     | Dimensijų hierarchijos tipo pavadinimas      |
|--------------------------|---------------|------------------------------------|
| Savikainos veikimo būdas            | Savikainos elementai | Dimensijų klasifikavimo hierarchija |

Strategijos dimensijų hierarchiją galima nustatyti kaip parodyta čia.

|                   | Dimensijos narių intervalai   |                         |
|-------------------|---------------------------|-------------------------|
| **Mazgai**         | **Iš dimensijos nario** | **Į dimensijos narį** |
| Savikainos veikimo būdas     |                           |                         |
| &nbsp;&nbsp;Fiksuotos išlaidos    | 10001                     | 10011                   |
|&nbsp;&nbsp;Kintamos išlaidos | 40001                     | 40010                   |

> [!NOTE]
> Dalies **Dimensijos narių intervalai** mazge gali būti dimensijos narių intervalų – 1:_n_. Galite įvesti dimensijos nariais dar netapusių dimensijos narių ID. Taikant šį metodą hierarchija tampa atsparesnė ateities pokyčiams.  

### <a name="copy-a-hierarchy"></a>Hierarchijos kopijavimas

Galite nukopijuoti dabartinę dimensijų hierarchiją kaip naujos dimensijų hierarchijos pradžios tašką. Šis metodas gali būti naudingas, jei norite palyginti ankstesnę dimensijų hierarchiją su naująja dimensijų hierarchija.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Pakeiskite mazgų išdėstymo tvarką hierarchijoje

Kiekvieno struktūros lygmens mazgą galite patraukti į viršų ir į apačią. Tokiu būdu darbo srityje **Išlaidų kontrolė** galite pakeisti ataskaitų mazgų išdėstymo tvarką.

Į naują vietą hierarchijoje mazgas perkeliamas pasirinkus tikslinį mazgą. Yra du mazgo perkėlimo būdai:

- **Perkelti žemiau** – perkelti pasirinktą mazgą iš dabartinės vietos hierarchijoje ir įterpti jį **po** pasirinktu tiksliniu mazgu.
- **Perkelti po** – perkelti pasirinktą mazgą iš dabartinės vietos hierarchijoje ir įterpti jį **po** pasirinktu tiksliniu mazgu jo hierarchijos lygyje.

> [!NOTE] 
> Eksportuojant duomenis į „Excel“ arba „Power BI“mazgų išdėstymo tvarka nėra išlaikoma, nes tie įrankiai naudoja išdėstymo pagal raidinius ir skaitinius simbolius tvarką. Turėtumėte pakeisti išdėstymo tvarką rankiniu būdu.

## <a name="define-dimension-hierarchies-for-reporting"></a>Ataskaitų dimensijų hierarchijų apibrėžimas

Dimensijų hierarchijos svarbios ataskaitoms. Naudodami jas galite nurodyti konkrečią atskirai organizacijai tinkančią struktūrą. Pasinaudodamos dimensijos hierarchijos mazgo lygyje atliktais telkimais suinteresuotosios šalys gali bet kuriame organizacijos lygyje matyti bet kokio lygio duomenis.

Dimensijų hierarchijas galima rasti toliau nurodytuose ataskaitų įrankiuose. Šis metodas padeda užtikrinti ataskaitų struktūros vientisumą.

- **Savikainos kontrolės** darbo sritis (klientas):

    - Kontroliuojama atliekant konfigūravimą.

- **Savikainos kontrolės** darbo sritis (mobilioji programa):

    - Kontroliuojama atliekant konfigūravimą.

- „Excel“

    - Suteikia galimybę pasirinkti konkrečias dimensijų hierarchijas pagal eksporto apibrėžimą:

        - Viena savikainos elemento dimensijų hierarchija (privaloma)
        - Viena savikainos objekto dimensijų hierarchija (pasirinktinai)
        - Viena statistinė dimensijų hierarchija (pasirinktinai)

- Power BI:

    - Galimos visos dimensijų hierarchijos.
    
Jei ataskaitas kuriate naudodami „Excel“ arba „Power BI“, eksportuojami tik pirmi 15 dimensijų hierarchijų lygių. Šis apribojimas nustatomas todėl, kad naudojant „Excel“ ir „Power BI“ reikalinga ilgalaikė schema. Jei hierarchija sudaryta iš daugiau nei 15 lygių, pertekliniai lygiai neeksportuojami. Normalizuotoje lentelėje pateikiamas kiekvieno hierarchijos dimensijos nario įrašas. Todėl įvyksta automatinis telkimas. Taikant šį metodą lengviau užtikrinti, kad visų galimų 15 hierarchijos lygių likučiai būtų teisingi.

Toliau pateiktame pavyzdyje nurodoma, kaip dimensijų hierarchija gali atrodyti ataskaitų struktūroje.

| Savikainos objekto dimensijų hierarchija – 1 lygis | Savikainos objekto dimensijų hierarchija – 2 lygis | Savikainos objekto dimensijų hierarchija – 3 lygis | Savikainos objekto dimensijų hierarchija – 4 lygis | Savikainos objekto dimensijų hierarchija – 15 lygis |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organizacija                              | Administratorius                                     | Finansai                                   | CC002                                     |                                            |
| Organizacija                              | Administratorius                                     | Finansai                                   | CC003                                     |                                            |
| Organizacija                              | Administratorius                                     | Finansai                                   | CC007                                     |                                            |
| Organizacija                              | Administratorius                                     | Personalas                                        | CC001                                     |                                            |
| Organizacija                              | Gamyba                                | Pakuotės                                 | CC005                                     |                                            |
| Organizacija                              | Gamyba                                | Surinkimas                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Ataskaitoms naudojamų dimensijų hierarchijų atnaujinimas 

Laikui bėgant pirmiau minėtuose ataskaitų rengimo įrankiuose naudojamos dimensijų hierarchijos turi būti atnaujinamos. Atnaujinti dimensijų hierarchijas galite atnaujindami klientą.

- **Savikainos kontrolės** darbo sritis (klientas)
- **Savikainos kontrolės** darbo sritis (mobilioji programa)

Dimensijų hierarchijų atnaujinimai pasirenkami kas 24 valandas pagal iš anksto į talpyklą perkeltas užduotis. Atnaujinus eksportuotus duomenis atnaujintas dimensijų hierarchijas galima rasti šiuose įrankiuose:

- „Excel“
- „Power BI‟

> [!NOTE] 
> Norėdami rankiniu būdu suaktyvinti dimensijų hierarchijos talpyklos naujinimą, galite sukurti naują dimensijų hierarchijos arba turimų atnaujinti hierarchijų eksportavimą į „Excel“.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Savikainos strategijų dimensijų hierarchijų apibrėžimas

Kaštų apskaitą sudaro keletas strategijų, kuriose nurodomos išsamios taisyklės. Turite nustatyti vieną ar kelias toliau nurodytų strategijų dimensijų hierarchijas.

- Savikainos veikimo būdas
- Išlaidų paskirstymas
- Išlaidų paskirstymas
- Išlaidų sumavimas

Naudojant dimensijų hierarchijas lengva kurti taisykles. Norėdami, kad nereikėtų kurti taisyklių kiekvienam dimensijos nariui, galite pasinaudoti pagal dimensijų hierarchijos lygius pateiktų dimensijos narių telkimo funkcija. Jeigu yra sutampančių taisyklių, turite nurodyti specialias taisykles, kurių sistema laikysis atlikdama pridėtinių išlaidų skaičiavimą.

### <a name="example-define-a-cost-behavior-policy"></a>Pavyzdys: savikainos veikimo būdo strategijos nustatymas

Sukuriama nauja savikainos veikimo būdo strategija ir jai priskiriamos atitinkamos dimensijų hierarchijos, kaip parodyta čia.

**Savikainos veikimo būdo strategija**

| Strategijos pavadinimas   | Savikainos elemento dimensijų hierarchija | Savikainos objekto dimensijų hierarchija | Apskaitos valiuta |
|---------------|----------------------------------|---------------------------------|---------------------|
| Savikainos veikimo būdas | Savikainos veikimo būdas                    | Organizacija                    | USD                 |

**Taisyklės**

| Savikainos elemento dimensijų hierarchijos mazgas | Savikainos objekto dimensijų hierarchijos mazgas | Fiksuotas procentas | Fiksuota suma | Galioja nuo | Galioja iki |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Fiksuotos išlaidos                            | Organizacija                         | 100,00           | 0,00         | 1/1/2017   | Niekada    |
| 10001                                 | Organizacija                         | 0,00             | 150,00       | 1/1/2017   | Niekada    |
| 10001 (\*)                             | Finansai                              |                  | 50,00        | 1/1/2017   | Niekada    |
| Savikainos veikimo būdas arba kintamos išlaidos (\*\*)   | Organizacija                         | 0,00             | 0,00         | 1/1/2017   | Niekada    |

\* Kintamų išlaidų mazgas nėra būtinas. Jei išlaidos nepriskiriamos prie fiksuotų išlaidų, turbūt jos kintamos išlaidos.

\*\* Sukuriama išsami taisyklė, kuri taikoma savikainos elemento nario 10001 ir visų finansų hierarchijos lygyje susietų savikainos objekto narių (CC002, CC003, CC007) deriniui.

Pirmiau pateiktose taisyklėse nurodomas lankstumas, kurį suteikia dimensijų hierarchijos. Nurodydami aukšto lygio taisykles galite sumažinti priežiūros darbų apimtis. Po to galite nurodyti specialiems verslo tikslams pasiekti pritaikytas išsamias taisykles.

Jeigu taisyklėse naudojamos dimensijų hierarchijos atnaujinamos, sistema automatiškai pasiūlo pritaikyti atnaujinimus.

Jei taisyklėse detalumo lygis nebereikalingas, galima nutraukti taisyklės galiojimą.

Pavyzdžiui, speciali savikainos objekto dimensijų hierarchijos mazgui Finansai taikoma savikainos veikimo būdo taisyklė nebereikalinga. Tokiu atveju spustelėjus **Taisyklės galiojimo pabaiga** baigiasi taisyklės galiojimas.

| Savikainos elemento dimensijų hierarchijos mazgas | Savikainos objekto dimensijų hierarchijos mazgas | Fiksuotas procentas | Fiksuota suma | Galioja nuo | Galioja iki  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Fiksuotos išlaidos                            | Organizacija                         | 100,00           | 0,00         | 1/1/2017   | Niekada     |
| 10001                                 | Organizacija                         | 0,00             | 150,00       | 1/1/2017   | Niekada     |
| 10001                                 | Finansai                              |                  | 50,00        | 1/1/2017   | 20/1/2017 |
| Savikainos veikimo būdas arba kintamos išlaidos        | Organizacija                         | 0,00             | 0,00         | 1/1/2017   | Niekada     |

Atliekant pridėtinių išlaidų skaičiavimą, jei jis atliekamas po 2017 m. sausio 20 d., į šią taisyklę neatsižvelgiama.

> [!NOTE] 
> Laukuose **Galioja nuo** ir **Galioja iki** nurodoma data ir laikas. Galite nutraukti taisyklės galiojimą ir tą pačią dieną atlikti naują pridėtinių išlaidų skaičiavimą.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Saugos nustatymo dimensijų hierarchijų apibrėžimas

Kaštų apskaitos duomenys turėtų būti prieinami visiems už ataskaitinį vienetą atsakingiems vadovams. Kaštų apskaitos terminologijoje ataskaitinis vienetas vaizduojamas kaip savikainos objektas arba savikainos objektų rinkinys.

Gali būti, kad visi vadovai galės pasiekti itin slaptus verslo duomenis, pvz., įplaukas ir maržas. Todėl svarbu nustatyti saugą, kad vadovai galėtų matyti tik su jais susijusius ir jiems reikiamus duomenis. Norėdami padėti kontroliuoti duomenų saugumą, nurodote dimensijų hierarchijas.

- Dimensijų hierarchijos naudojamos tik tada, kai dimensijų hierarchijos nuorodoje pasirinkta dimensijos reikšmė yra savikainos objekto dimensija.
- Vienai prieigos sąrašo hierarchijos savikainos objekto dimensijai galima įjungti tik vieną dimensijų hierrchiją.

**Dimensijų hierarchijos informacija**

| Dimensijų hierarchijos pavadinimas | Dimensija    | Dimensijų hierarchijos tipo pavadinimas      | Prieigos sąrašo hierarchija |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizacija             | Išlaidų centrai | Dimensijų klasifikavimo hierarchija | **Taip**               |

Hierarchijos kūrimo įrankyje galima naudoti naują „FastTab“ skirtuką **Vartotojai**. Čia kiekviename hierarchijos mazge galite įterpti vieną ar kelis vartotojų ID.

|                 | Vartotojai            | Dimensijos narių intervalai   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Mazgai**       | **Vartotojo ID**      | **Iš dimensijos nario** | **Į dimensijos narį** |
| Organizacija    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Administratorius         | Balandžio            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finansai   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personalas        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Gamyba    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakuotės | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Surinkimas  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Išlaidų buhalteriai turi būti priskirti aukščiausiam hierarchijos lygiui, kad galėtų matyti visus kaštų apskaitos įrašus.

Norėdami įgalinti prieigos sąrašo hierarchiją ir jos saugos parametrus, eikite į **Kaštų apskaita** > **Sąranka** > **Parametrai** > **Bendra**. Pasirinkite parametrą **Įgalinti savikainos objekto dimensijos narių peržiūros prieigą**.

Prieigos sąrašo hierarchijos parametrai naudojami norint valdyti toliau nurodytose srityse rodomus duomenis.

- **Savikainos kontrolės** darbo sritis (klientas):

    - Duomenys formose, kurios naudojamos detalizuojant scenarijus

- **Savikainos kontrolės** darbo sritis (mobilioji programa):

    - Likučiai kortelėse

- Power BI:

    - Atliekant „Power BI“ vizualizavimą rodomi duomenys
    - Į „Dynamics 365 Finance“ klientą įtrauktų duomenų „Power BI“ vizualizavimai

> [!NOTE] 
> - Tam, kad prieigos sąrašo hierarchija galėtų turėti įtakos „Power BI“, turi būti susieta prieigos sąrašo hierarchija ir „Power BI“ eilučių lygio sauga. Daugiau informacijos rasite dalyje [Kaštų apskaitos turinio paketo saugos nustatymas](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Prieigos sąrašo hierarchija negali padėti užtikrinti, kad duomenys bus eksportuoti į „Excel“. Todėl tą ataskaitų įrankį turi naudoti tik išlaidų buhalteriai ir vadovai, kuriems suteikiama neribota prieiga peržiūrėti duomenis.
