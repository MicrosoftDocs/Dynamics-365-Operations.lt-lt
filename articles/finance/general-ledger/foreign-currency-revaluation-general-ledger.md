---
title: DK užsienio valiutos kurso pasikeitimas
description: Šiame straipsnyje pateikiama DK užsienio valiutos kurso pasikeitimo proceso – nustatymo, proceso skaičiavimo ir, jei reikia, perkainojimo operacijų anuliavimo peržiūra.
author: kweekley
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: twheeloc
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96ae50e339c63687a4c8114d3c965123fd5e37ab
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779994"
---
# <a name="foreign-currency-revaluation-for-general-ledger"></a>DK užsienio valiutos kurso pasikeitimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama DK užsienio valiutos kurso pasikeitimo proceso – nustatymo, proceso skaičiavimo ir, jei reikia, perkainojimo operacijų anuliavimo peržiūra. 

Laikotarpio pabaigoje tvarkant apskaitos konvencijas būtina DK sąskaitų balansus užsienio valiuta perkainoti naudojant skirtingus valiutų kursų tipus (dabartinis, retrospektyvinis, vidurkio, ir t. t.). Pavyzdžiui, tvarkant tam tikrą apskaitos konvenciją, turtą ir įsipareigojimus būtina perkainoti pagal esamą valiutos kursą, ilgalaikį turtą – pagal retrospektyvinį valiutos kursą, o pelną ir nuostolį – pagal mėnesio vidurkį. Galima naudoti DK užsienio valiutos kurso pasikeitimo funkciją, norint perkainoti balansą ir pelno bei nuostolio sąskaitas. 

> [!NOTE]
> Užsienio valiutos kurso pasikeitimo funkciją galima taip pat naudoti moduliuose Gautinos sumos (AR) ir Mokėtinos sumos (AP). Jei naudojate šiuos modulius, neapmokėtos operacijos turėtų būti perkainojamos naudojant užsienio valiutos kurso pasikeitimo funkciją šiuose moduliuose. AR ir AP užsienio valiutos kurso pasikeitimo funkcija DK sukurs apskaitos įrašą, kuriame bus nurodyti nerealizuotas pelnas arba nuostolis, ir užtikrins, kad papildomas knygas ir DK galima suderinti. Kadangi AR ir AP užsienio valiutos kurso pasikeitimo funkcijos apskaitos įrašus kuria DK, gautinų ir mokėtinų sumų pagrindinės sąskaitos turi būti neįtrauktos į DK užsienio valiutos kurso pasikeitimą. 

Kai paleidžiate perkainojimo procesą, kiekvienos pagrindinės sąskaitos balansas, užregistruotas užsienio valiuta, bus perkainotas. Perkainojimo metu sukurtas negauto pelno arba nuostolio operacijas sugeneruoja sistema. Bus sukurtos dvi operacijos: viena skirta apskaitos valiutai, o kita – ataskaitų valiutai, jei to reikia. Kiekvienas apskaitos įrašas bus registruojamas negautame pelne arba nuostolyje ir pagrindinėje sąskaitoje, kurie yra perkainojami.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Pasiruošimas paleisti užsienio valiutos kurso pasikeitimą
Prieš vykdant perkainojimo procesą reikalinga tolesnė sąranka.

Puslapyje **Pagrindinės sąskaita**
 - Jei pagrindinė sąskaita turi būti perkainota DK, pasirinkite **Užsienio valiutos kurso pasikeitimas**. Jei pagrindinė sąskaita neturėtų būti perkainota (pavyzdžiui, AR ir AP, jei perkainojama papildomose knygose), atžymėkite šią parinktį.
 - Jei pagrindinė sąskaita pažymėta perkainoti, įveskite **Valiutos kurso tipas**. Šis valiutos kurso tipas bus naudojamas perkainojant pagrindinę sąskaitą. Finansinėse ataskaitose galima naudoti atskirą lauką **Finansinių ataskaitų valiutos kurso tipas**. Du laukai nėra sinchronizuojami, todėl perkainojant ir kuriant finansines ataskaitas galima naudoti skirtingus valiutų kursų tipus.

Puslapyje **DK**
 - Nurodykite **valiutos kurso tipą**. Jei valiutos kurso tipas nenurodytas pagrindinėje sąskaitoje, šis valiutos kurso tipas bus naudojamas vykdant užsienio valiutos kurso pasikeitimo funkciją.
 - Nurodykite valiutos kurso pasikeitimo gauto pelno, patirtų nuostolių, negauto pelno ir nepatirtų nuostolių sąskaitas. Gauto pelno ir patirtų nuostolių sąskaitos naudojamos sudengiant AR ir AP operacijas, o negauto pelno ir nepatirtų nuostolių sąskaitos naudojamos perkainojant atviras operacijas ir DK pagrindines sąskaitas.

Puslapyje **Valiutos kurso pasikeitimo sąskaitos**
 - Pasirinkite skirtingas kiekvienos valiutos ir įmonės valiutos kurso pasikeitimo sąskaitas. Nenurodžius jokios sąskaitos naudojamos sąskaitos iš puslapio **Didžioji knyga**.

## <a name="process-foreign-currency-revaluation"></a>Užsienio valiutos kurso pasikeitimo apdorojimas
Baigę atlikti sąranką naudodamiesi puslapiu **Užsienio valiutos kurso pasikeitimas** perkainokite pagrindinių sąskaitų balansus. Galite paleisti procesą realiuoju laiku arba suplanuoti, kad jis būtų paleistas naudojant paketą. 

Puslapyje **Užsienio valiutos kurso pasikeitimas** bus rodoma kiekvieno perkainojimo proceso retrospektyva, įskaitant tai, kada procesas buvo vykdytas ir kokie kriterijai nustatyti, saitą į sukurtą perkainojimo kvitą ir įrašą apie tai, ar ankstesnis perkainojimas buvo atšauktas. Norėdami vykdyti perkainojimo procesą, pasirinkite mygtuką **Užsienio valiutos kurso pasikeitimas**. 

Reikšmės **Pradžios data** ir **Pabaigos data** nurodo perkainojamo užsienio valiutos balanso skaičiavimo datų intervalą. Kai perkainojate pelno ir nuostolio sąskaitas, perkainojamos visos tuo datos intervalu vykstančios operacijos. Kai perkainojate balanso sąskaitas, **pradžios datos** nepaisoma. Vietoj to perkainojamas balansas nustatomas nueidami nuo finansinių metų pradžios iki pabaigos **datos**. 

Naudojant parinktį **Kurso data** galima nurodyti datą, kurią turi būti nustatytas numatytasis valiutos kursas. Pvz., galite perkainoti balansus nuo sausio 1 d. iki sausio 31 d., bet naudoti valiutos kursą, nustatytą vasario 1 d. 

Pasirinkite, kurias pagrindines sąskaitas perkainoti: visas, balanso arba pelno ir nuostolio. Perkainoti bus tik tos pagrindinės sąskaitos **, kurios pažymėtos perkainoti** (pagrindinės sąskaitos puslapyje). Norėdami dar labiau apriboti pagrindinių sąskaitų diapazoną, naudokite skirtuką Įtraukti įrašai, **kad** nurodykite pagrindinių sąskaitų diapazoną arba atskiras pagrindines sąskaitas. 

Perkainojimo procesą galima taikyti vienam arba daugiau juridinių subjektų. Peržiūroje bus rodomos tik juridiniai subjektai, prie kurių turite prieigą. Pasirinkite juridinius subjektus, kuriems norite taikyti perkainojimo procesą. 

Perkainojimo procesą galima taikyti vienai arba daugiau užsienio valiutų. Peržvalgoje bus rodomos visos pasirinktos perkainoti juridinių subjektų valiutos, kurios buvo registruotos atitinkamo pagrindinės sąskaitos tipo (Balansas arba Pelnas ir nuostolis) laikotarpiu. Apskaitos valiuta bus įtraukta į sąrašą, bet niekas nebus perkainojama pasirinkus apskaitos valiutą. 

Nustatykite parinktį **Peržiūrėti prieš registruojant** į **Taip**, jei norite peržiūrėti DK perkainojimo rezultatą. DK peržiūra skiriasi nuo AR ir AP užsienio valiutos kurso pasikeitimo modeliavimo. AR ir AP modeliavimas yra ataskaita, o DK pateikiama peržiūra, kurią galima registruoti nepaleidus perkainojimo proceso dar kartą. Peržiūros rezultatus galima eksportuoti į „Microsoft Excel“, norint išsaugoti sumų skaičiavimo retrospektyvą. Jei norite peržiūrėti perkainojimo rezultatus, naudoti paketinio vykdymo negalėsite. Naudodamas peržiūrą vartotojas turi galimybę registruoti visų juridinių subjektų rezultatus, naudodamas mygtuką **Registruoti**. Jei kilo problema dėl juridinio subjekto rezultatų, vartotojas taip pat gali registruoti juridinių subjektų pogrupį, naudodamas mygtuką **Pasirinkti registruotinus juridinius subjektus**.

Jei norite neįtraukti koregavimų, užregistruotų naudojant ataskaitų **valiutos** koregavimo žurnalą iš perkainojimo proceso, **nustatykite Neįtraukti ataskaitų valiutos koregavimų** į **Taip**. Numatyta, kad ataskaitų valiutos koregavimai įtraukiami į perkainojimą. 

Kai užsienio valiutos kurso pasikeitimo procesas baigtas, bus sukurtas įrašas, skirtas sekti kiekvieno vykdymo retrospektyvą. Bus sukurtas atskiras kiekvieno juridinio subjekto ir registravimo sluoksnio įrašas.

## <a name="calculate-unrealized-gainloss"></a>Negauto pelno / nuostolio skaičiavimas
Neauto pelno / nuostolio operacijos DK perkainojimo bei AR ir AP perkainojimo procesuose kuriamos skirtingai. AR ir AP ankstesnis perkainojimas yra visiškai atšaukiamas (darant prielaidą, kad operacija dar nesudengta) ir nauja negauto pelno / nuostolio perkainojimo operacija sukuriama pagal naują valiutos kursą. Taip yra todėl, kad AR ir AP perkainojama kiekviena atskira operacija. DK ankstesnis perkainojimas nėra atšaukiamas. Operacija, skirta pokyčiui tarp pagrindinės sąskaitos balanso, įskaitant visas ankstesnio perkainojimo sumas, ir naujos vertės registruoti, sukuriama pagal lauke Kurso data nurodytos datos valiutos kursą. 

**Pavyzdys** Toliau pateikiami pagrindinės sąskaitos 110110 balansai.

| Data   | DK sąskaita| Operacijos suma | Apskaitos suma |
|------------|--------------------|------------------------|-----------------------|
| Sausio 20 | 110110 (grynieji pinigai)      | 500 EUR (debetas)        | 1000 USD (debetas)      |

Pagrindinė sąskaita perkainojama sausio 31 d.  Negautas pelnas / nuostolis skaičiuojamas toliau nurodytu būdu.

| Dabartinis balansas operacijos valiuta | Dabartinis balansas apskaitos valiuta | Valiutos kursas perkainojimo metu | Nauja apskaitos valiutos suma | Negautas pelnas / nuostolis    |
|--------------------|---------------------------|----------------------------------|------------------------------------|-----------------------------|
| 500 EUR            | 1000 USD                  | 166.6667                         | 833,33 USD (500 x 1,666667)        | 166,67 nuostolis (833,33 – 1000) |

Sukuriamas toliau nurodytas apskaitos įrašas.

| Data   | DK sąskaita       | Debetas | Kreditas |
|------------|--------------------------|-----------|------------|
| Sausio 31 | 110110 (grynieji pinigai)            |           | 166.67     |
| Sausio 31 | 801400 (nepatirtas nuostolis) | 166.67    |            |

Naujų vasario mėn. operacijų neregistruojama.  Pagrindinė sąskaita yra perkainojama vasario 28 d.

| Dabartinis balansas operacijos valiuta | Dabartinis balansas apskaitos valiuta | Valiutos kursas perkainojimo metu | Nauja apskaitos valiutos suma | Negautas pelnas / nuostolis    |
|---------------------------------------|-----------------------------------|-------------------------------|--------------------|-----------------------------|
| 500 EUR                 | 833,33 USD (1000 – 166,67)       | 250.0000              | 1250 USD (500 x 2,5)               | 416,67 pelnas (1250 – 833,33) |

Sukuriamas toliau nurodytas apskaitos įrašas.

| Data    | DK sąskaita       | Debetas | Kreditas |
|-------------|--------------------------|-----------|------------|
| Vasario 28 | 110110 (grynieji pinigai)            | 416.67    |            |
| Vasario 28 | 801600 (negautas pelnas) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Užsienio valiutos kurso pasikeitimo atšaukimas
Jei norite atšaukti perkainojimo operaciją, pasirinkite puslapio **Užsienio valiutos kurso pasikeitimas** mygtuką **Atšaukti operaciją**. Bus sukurtas naujas užsienio valiutos kurso pasikeitimo retrospektyvos įrašas, skirtas tvarkyti audito retrospektyvą ir sekti, kada buvo vykdytas arba atšauktas perkainojimas. 

Galite atšaukti perkainojimo, įvykdyto neatsižvelgiant į datų tvarką, rezultatus, tačiau gali reikėti taip pat atšaukti dabartinį perkainojimą, norint užtikrinti, kad kiekvienos perkainotos pagrindinės sąskaitos balansai yra teisingi. Atšaukimai gali būti vykdomi neatsižvelgiant į datų tvarką, nes nėra jokių būdų kontroliuoti, kaip dažnai ir kurios pagrindinės sąskaitos yra perkainojamos. Pvz., organizacija gali pasirinkti perkainoti grynųjų pinigų pagrindines sąskaitas kas ketvirtį, o visas kitas pagrindines sąskaitas – kas mėnesį.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
