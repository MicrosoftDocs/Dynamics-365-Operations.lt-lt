---
title: "DK užsienio valiutos kurso pasikeitimas"
description: "Šioje temoje apžvelgiami šie DK užsienio valiutos kurso pasikeitimo proceso aspektai: sąranka, proceso paleidimas, procesas skaičiavimas ir tai, kaip atšaukti perkainojimo operacijas, jei reikia."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8031f5b4be79b0642134898db60188311d1ca6d2
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017

---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>DK užsienio valiutos kurso pasikeitimas

[!include[banner](../includes/banner.md)]


Šioje temoje apžvelgiami šie DK užsienio valiutos kurso pasikeitimo proceso aspektai: sąranka, proceso paleidimas, procesas skaičiavimas ir tai, kaip atšaukti perkainojimo operacijas, jei reikia. 

Laikotarpio pabaigoje tvarkant apskaitos konvencijas būtina DK sąskaitų balansus užsienio valiuta perkainoti naudojant skirtingus valiutų kursų tipus (dabartinis, retrospektyvinis, vidurkio, ir t. t.). Pavyzdžiui, tvarkant tam tikrą apskaitos konvenciją, turtą ir įsipareigojimus būtina perkainoti pagal esamą valiutos kursą, ilgalaikį turtą – pagal retrospektyvinį valiutos kursą, o pelną ir nuostolį – pagal mėnesio vidurkį. Galima naudoti DK užsienio valiutos kurso pasikeitimo funkciją, norint perkainoti balansą ir pelno bei nuostolio sąskaitas. 

> [!NOTE]
> Užsienio valiutos kurso pasikeitimo funkciją galima taip pat naudoti moduliuose Gautinos sumos (AR) ir Mokėtinos sumos (AP). Jei naudojate šiuos modulius, neapmokėtos operacijos turėtų būti perkainojamos naudojant užsienio valiutos kurso pasikeitimo funkciją šiuose moduliuose. AR ir AP užsienio valiutos kurso pasikeitimo funkcija DK sukurs apskaitos įrašą, kuriame bus nurodyti nerealizuotas pelnas arba nuostolis, ir užtikrins, kad papildomas knygas ir DK galima suderinti. Kadangi AR ir AP užsienio valiutos kurso pasikeitimo funkcijos apskaitos įrašus kuria DK, gautinų ir mokėtinų sumų pagrindinės sąskaitos turi būti neįtrauktos į DK užsienio valiutos kurso pasikeitimą. 

Kai paleidžiate perkainojimo procesą, kiekvienos pagrindinės sąskaitos balansas, užregistruotas užsienio valiuta, bus perkainotas. Perkainojimo metu sukurtas negauto pelno arba nuostolio operacijas sugeneruoja sistema. Bus sukurtos dvi operacijos: viena skirta apskaitos valiutai, o kita – ataskaitų valiutai, jei to reikia. Kiekvienas apskaitos įrašas bus registruojamas negautame pelne arba nuostolyje ir pagrindinėje sąskaitoje, kurie yra perkainojami.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Pasiruošimas paleisti užsienio valiutos kurso pasikeitimą
Prieš vykdant perkainojimo procesą reikalinga tolesnė sąranka.

-   Puslapyje **Pagrindinės sąskaita**
-   Jei pagrindinė sąskaita turi būti perkainota DK, pasirinkite **Užsienio valiutos kurso pasikeitimas**. Jei pagrindinė sąskaita neturėtų būti perkainota (pavyzdžiui, AR ir AP, jei perkainojama papildomose knygose), atžymėkite šią parinktį.
-   Jei pagrindinė sąskaita pažymėta perkainoti, įveskite **Valiutos kurso tipas**. Šis valiutos kurso tipas bus naudojamas perkainojant pagrindinę sąskaitą. Finansinėse ataskaitose galima naudoti atskirą lauką **Finansinių ataskaitų valiutos kurso tipas**. Du laukai nėra sinchronizuojami, todėl perkainojant ir kuriant finansines ataskaitas galima naudoti skirtingus valiutų kursų tipus.

-   Puslapyje **DK**
-   Nurodykite **valiutos kurso tipą**. Jei valiutos kurso tipas nenurodytas pagrindinėje sąskaitoje, šis valiutos kurso tipas bus naudojamas vykdant užsienio valiutos kurso pasikeitimo funkciją.
-   Nurodykite valiutos kurso pasikeitimo gauto pelno, patirtų nuostolių, negauto pelno ir nepatirtų nuostolių sąskaitas. Gauto pelno ir patirtų nuostolių sąskaitos naudojamos sudengiant AR ir AP operacijas, o negauto pelno ir nepatirtų nuostolių sąskaitos naudojamos perkainojant atviras operacijas ir DK pagrindines sąskaitas.

-   Puslapyje **Valiutos kurso pasikeitimo sąskaitos**
-   Pasirinkite skirtingas kiekvienos valiutos ir įmonės valiutos kurso pasikeitimo sąskaitas. Nenurodžius jokios sąskaitos naudojamos sąskaitos iš puslapio **Didžioji knyga**.

## <a name="process-foreign-currency-revaluation"></a>Užsienio valiutos kurso pasikeitimo apdorojimas
Baigę atlikti sąranką naudodamiesi puslapiu **Užsienio valiutos kurso pasikeitimas** perkainokite pagrindinių sąskaitų balansus. Galite paleisti procesą realiuoju laiku arba suplanuoti, kad jis būtų paleistas naudojant paketą. 

Puslapyje **Užsienio valiutos kurso pasikeitimas** bus rodoma kiekvieno perkainojimo proceso retrospektyva, įskaitant tai, kada procesas buvo vykdytas ir kokie kriterijai nustatyti, saitą į sukurtą perkainojimo kvitą ir įrašą apie tai, ar ankstesnis perkainojimas buvo atšauktas. Norėdami vykdyti perkainojimo procesą, pasirinkite mygtuką **Užsienio valiutos kurso pasikeitimas**. 

Reikšmės **Pradžios data** ir **Pabaigos data** nurodo perkainojamo užsienio valiutos balanso skaičiavimo datų intervalą. Kai perkainojate pelno ir nuostolio sąskaitas, perkainojamos visos tuo datos intervalu vykstančios operacijos. Kai perkainojate balanso sąskaitas, Pradžios data yra ignoruojama. Perkainotinas balansas nustatomas skaičiuojant nuo finansinių metų pradžios iki lauke Pabaigos data nurodytos datos. 

Naudojant parinktį **Kurso data** galima nurodyti datą, kurią turi būti nustatytas numatytasis valiutos kursas. Pvz., galite perkainoti balansus nuo sausio 1 d. iki sausio 31 d., bet naudoti valiutos kursą, nustatytą vasario 1 d. 

Pasirinkite, kurias pagrindines sąskaitas perkainoti: visas, balanso arba pelno ir nuostolio. Bus perkainojamos tik pažymėtos perkainoti (puslapyje Pagrindinės sąskaitos) pagrindinės sąskaitos. Jei norite dar labiau sumažinti pagrindinių sąskaitų diapazoną, naudokite skirtuką **Įtrauktini įrašai**, norėdami nustatyti pagrindinių sąskaitų diapazoną arba atskiras pagrindines sąskaitas. 

Perkainojimo procesą galima taikyti vienam arba daugiau juridinių subjektų. Peržiūroje bus rodomos tik juridiniai subjektai, prie kurių turite prieigą. Pasirinkite juridinius subjektus, kuriems norite taikyti perkainojimo procesą. 

Perkainojimo procesą galima taikyti vienai arba daugiau užsienio valiutų. Peržvalgoje bus rodomos visos pasirinktos perkainoti juridinių subjektų valiutos, kurios buvo registruotos atitinkamo pagrindinės sąskaitos tipo (Balansas arba Pelnas ir nuostolis) laikotarpiu. Apskaitos valiuta bus įtraukta į sąrašą, bet niekas nebus perkainojama pasirinkus apskaitos valiutą. 

Nustatykite parinktį **Peržiūrėti prieš registruojant** į **Taip**, jei norite peržiūrėti DK perkainojimo rezultatą. DK peržiūra skiriasi nuo AR ir AP užsienio valiutos kurso pasikeitimo modeliavimo. AR ir AP modeliavimas yra ataskaita, o DK pateikiama peržiūra, kurią galima registruoti nepaleidus perkainojimo proceso dar kartą. Peržiūros rezultatus galima eksportuoti į „Microsoft Excel“, norint išsaugoti sumų skaičiavimo retrospektyvą. Negalite naudoti paketinio apdorojimo, jei norite peržiūrėti perkainojimo rezultatus. Naudodamas peržiūrą vartotojas turi galimybę registruoti visų juridinių subjektų rezultatus, naudodamas mygtuką **Registruoti**. Jei kilo problema dėl juridinio subjekto rezultatų, vartotojas taip pat gali registruoti juridinių subjektų pogrupį, naudodamas mygtuką **Pasirinkti registruotinus juridinius subjektus**. 

Kai užsienio valiutos kurso pasikeitimo procesas baigtas, bus sukurtas įrašas, skirtas sekti kiekvieno vykdymo retrospektyvą.  Bus sukurtas atskiras kiekvieno juridinio subjekto ir registravimo sluoksnio įrašas.

## <a name="calculate-unrealized-gainloss"></a>Negauto pelno / nuostolio skaičiavimas
Neauto pelno / nuostolio operacijos DK perkainojimo bei AR ir AP perkainojimo procesuose kuriamos skirtingai. AR ir AP ankstesnis perkainojimas yra visiškai atšaukiamas (darant prielaidą, kad operacija dar nesudengta) ir nauja negauto pelno / nuostolio perkainojimo operacija sukuriama pagal naują valiutos kursą. Taip yra todėl, kad AR ir AP perkainojama kiekviena atskira operacija. DK ankstesnis perkainojimas nėra atšaukiamas. Operacija, skirta pokyčiui tarp pagrindinės sąskaitos balanso, įskaitant visas ankstesnio perkainojimo sumas, ir naujos vertės registruoti, sukuriama pagal lauke Kurso data nurodytos datos valiutos kursą. 

**Pavyzdys** Toliau pateikiami pagrindinės sąskaitos 110110 balansai.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Data**   | **DK sąskaita** | **Operacijos suma** | **Apskaitos suma** |
| Sausio 20 | 110110 (grynieji pinigai)      | 500 EUR (debetas)        | 1000 USD (debetas)      |

Pagrindinė sąskaita perkainojama sausio 31 d.  Negautas pelnas / nuostolis skaičiuojamas toliau nurodytu būdu.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Dabartinis balansas operacijos valiuta** | **Dabartinis balansas apskaitos valiuta** | **Valiutos kursas perkainojimo metu** | **Nauja apskaitos valiutos suma** | **Negautas pelnas / nuostolis**    |
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833,33 EUR (500 x 1,666667)        | 166,67 nuostolis (833,33 – 1000) |

Sukuriamas toliau nurodytas apskaitos įrašas.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Data**   | **DK sąskaita**       | **Debetas** | **Kreditas** |
| Sausio 31 | 110110 (grynieji pinigai)            |           | 166.67     |
| Sausio 31 | 801400 (nepatirtas nuostolis) | 166.67    |            |

Naujų vasario mėn. operacijų neregistruojama.  Pagrindinė sąskaita yra perkainojama vasario 28 d.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Dabartinis balansas operacijos valiuta** | **Dabartinis balansas apskaitos valiuta** | **Valiutos kursas perkainojimo metu** | **Nauja apskaitos valiutos suma** | **Negautas pelnas / nuostolis**    |
| 500 EUR                                     | 833,33 USD (1000 – 166,67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | 416,67 pelnas (1250 – 833,33) |

Sukuriamas toliau nurodytas apskaitos įrašas.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Data**    | **DK sąskaita**       | **Debetas** | **Kreditas** |
| Vasario 28 | 110110 (grynieji pinigai)            | 416.67    |            |
| Vasario 28 | 801600 (negautas pelnas) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Užsienio valiutos kurso pasikeitimo atšaukimas
Jei norite atšaukti perkainojimo operaciją, pasirinkite puslapio **Užsienio valiutos kurso pasikeitimas** mygtuką **Atšaukti operaciją**. Bus sukurtas naujas užsienio valiutos kurso pasikeitimo retrospektyvos įrašas, skirtas tvarkyti audito retrospektyvą ir sekti, kada buvo vykdytas arba atšauktas perkainojimas. 

Galite atšaukti perkainojimo, įvykdyto neatsižvelgiant į datų tvarką, rezultatus, tačiau gali reikėti taip pat atšaukti dabartinį perkainojimą, norint užtikrinti, kad kiekvienos perkainotos pagrindinės sąskaitos balansai yra teisingi. Atšaukimai gali būti vykdomi neatsižvelgiant į datų tvarką, nes nėra jokių būdų kontroliuoti, kaip dažnai ir kurios pagrindinės sąskaitos yra perkainojamos. Pvz., organizacija gali pasirinkti perkainoti grynųjų pinigų pagrindines sąskaitas kas ketvirtį, o visas kitas pagrindines sąskaitas – kas mėnesį.




