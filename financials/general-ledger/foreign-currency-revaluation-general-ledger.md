---
title: "DK užsienio valiutos kurso pasikeitimas"
description: "Šioje temoje pateikiama apžvalga šių Didžiosios knygos užsienio valiutos perkainojimo procesui - nustatymas, veikia procesas, skaičiavimo procesą, ir kaip pakeisti perkainojimo operacijų, jei reikia."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>DK užsienio valiutos kurso pasikeitimas

Šioje temoje pateikiama apžvalga šių Didžiosios knygos užsienio valiutos perkainojimo procesui - nustatymas, veikia procesas, skaičiavimo procesą, ir kaip pakeisti perkainojimo operacijų, jei reikia. 

Laikotarpio pabaigoje tvarkant apskaitos konvencijas būtina DK sąskaitų balansus užsienio valiuta perkainoti naudojant skirtingus valiutų kursų tipus (dabartinis, retrospektyvinis, vidurkio, ir t. t.). Pavyzdžiui, tvarkant tam tikrą apskaitos konvenciją, turtą ir įsipareigojimus būtina perkainoti pagal esamą valiutos kursą, ilgalaikį turtą – pagal retrospektyvinį valiutos kursą, o pelną ir nuostolį – pagal mėnesio vidurkį. Galima naudoti DK užsienio valiutos kurso pasikeitimo funkciją, norint perkainoti balansą ir pelno bei nuostolio sąskaitas. 

> [!NOTE]
> Užsienio valiutos perkainojimo taip pat yra (AR) gautinos ir mokėtinos sąskaitos (AP). Jei naudojate tuos modulius, nebaigtus sandorius turi būti perkainotas naudojant valiutos kurso šiuose moduliuose. AR ir AP užsienio valiutos kurso pasikeitimo funkcija DK sukurs apskaitos įrašą, kuriame bus nurodyti nerealizuotas pelnas arba nuostolis, ir užtikrins, kad papildomas knygas ir DK galima suderinti. Kadangi AR ir AP užsienio valiutos kurso pasikeitimo funkcijos apskaitos įrašus kuria DK, gautinų ir mokėtinų sumų pagrindinės sąskaitos turi būti neįtrauktos į DK užsienio valiutos kurso pasikeitimą. 

Kai paleidžiate perkainojimo procesą, kiekvienos pagrindinės sąskaitos balansas, užregistruotas užsienio valiuta, bus perkainotas. Perkainojimo metu sukurtas negauto pelno arba nuostolio operacijas sugeneruoja sistema. Dvi operacijos gali būti sukurta, vieną numatytąja valiuta ir antrąją – finansinės atskaitomybės valiuta, jei tinka. Kiekvienas apskaitos įrašas bus rašyti nerealizuotas pelnas ar nuostolis ir sąskaita buvo perkainotas.

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

Į **dienos normos** būtų galima nustatyti, kuriam turėtų numatytosios valiutos kurso datą. Pvz., galite suteikti balansą tarp dienos diapazonas nuo sausio 1 iki sausio 31 d., bet naudoti valiutos kursas, nustatytas už vasario 1. 

Pasirinkite, kurias pagrindines sąskaitas perkainoti: visas, balanso arba pelno ir nuostolio. Perkainojama tik pagrindinės sąskaitos pažymėtus kaip perkainojimo (Main abonemento puslapyje). Jei norite toliau riboti pagrindinių sąskaitų, naudoti įrašus **įtraukti** tab Norėdami nurodyti diapazoną, sąskaitų, ar atskiros pagrindinės sąskaitos. 

Perkainojimo procesas gali būti vykdoma vienas ar keli juridiniai asmenys. Peržvalgos rodys tik juridiniai asmenys, prie kurių turite prieigą. Pasirinkite juridinių asmenų, kuriems norite paleisti perkainojimo procesą. 

Perkainojimo procesą galima taikyti vienai arba daugiau užsienio valiutų. Peržvalgos apims visas valiutas, užregistruotos datų diapazone pagrindinės sąskaitos (balanso ar pelno ir nuostolio), juridiniams asmenims, pasirinktas perkainoti rūšį. Numatytąja valiuta bus įtraukta į sąrašą, bet nieko perkainojama pasirinkus numatytąja valiuta. 

Nustatyti **peržiūros prieš registruojant** į **taip** jei norite peržiūrėti DK perkainojimo rezultatas. Peržiūra paprastai knygos skiriasi nuo AR ir AP valiutos kurso modeliavimą. Modeliavimo AR ir AP ataskaitą, tačiau DK turi peržiūrą, kuri gali būti įregistruota, jums nereikės dar kartą paleisti perkainojimo procesas. Peržiūros rezultatus galima eksportuoti į „Microsoft Excel“, norint išsaugoti sumų skaičiavimo retrospektyvą. Negalite naudoti paketinio apdorojimo, jei norite peržiūrėti perkainojimo rezultatus. Naudodamas peržiūrą vartotojas turi galimybę registruoti visų juridinių subjektų rezultatus, naudodamas mygtuką **Registruoti**. Jei kilo problema dėl juridinio subjekto rezultatų, vartotojas taip pat gali registruoti juridinių subjektų pogrupį, naudodamas mygtuką **Pasirinkti registruotinus juridinius subjektus**. 

Po užsienio valiuta perkainojimo procesas bus baigtas, įrašas bus sukurta stebėti kiekvieną run istorija.  Atskirus įrašus bus sukurtas juridinis asmuo ir registravimo sluoksniui.

## <a name="calculate-unrealized-gainloss"></a>Negauto pelno / nuostolio skaičiavimas
Neauto pelno / nuostolio operacijos DK perkainojimo bei AR ir AP perkainojimo procesuose kuriamos skirtingai. AR ir AP ankstesnis perkainojimas yra visiškai atšaukiamas (darant prielaidą, kad operacija dar nesudengta) ir nauja negauto pelno / nuostolio perkainojimo operacija sukuriama pagal naują valiutos kursą. Taip yra todėl, kad AR ir AP perkainojama kiekviena atskira operacija. DK, praėjusių laikotarpių perkainojimo nepanaikinamas. Vietoj to, kad operacija bus sukurtas Delta tarp balanso sąskaita, įskaitant ankstesnius perkainojimo sumas, ir nauja reikšmė pagal valiutų kursą kursą data. 

**Pavyzdys** žemiau pateikti likučiai yra pagrindinės sąskaitos 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Data**   | **DK sąskaita** | **Operacijos suma** | **Apskaitos suma** |
| Sausio 20 | 110110 (grynieji pinigai)      | 500 EUR (debetas)        | 1000 USD (debetas)      |

Pagrindinės sąskaitos perkainojamas m. sausio 31 d.  Nerealizuotas pelnas/nuostolis apskaičiuojama toliau nurodytu būdu.

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

Naujos operacijos neregistruojamos vasario mėnesį.  Vasario 28 d. perkainojamas sąskaita.

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

Galite atšaukti rezultatus perkainojimo datą pažeistas, bet reikia taip pat pakeisti dabartinį perkainojimo užtikrinti kiekvienos perkainoto pagrindinės sąskaitos likučius. Ir atstatymas gali atsirasti pasibaigusio galiojimo tvarka, todėl, kad yra ne taip, kaip valdyti, kurios pagrindinės sąskaitos perkainojamas ir dažnis, kada jie perkainojamas. Pvz., organizacijoje gali rinktis perkainoti savo pinigų pagrindinės sąskaitos kas ketvirtį, tačiau visos kitos pagrindinės sąskaitos kas mėnesį.


