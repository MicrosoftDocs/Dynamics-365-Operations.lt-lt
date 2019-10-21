---
title: Banko užsienio valiutos kurso pasikeitimas
description: Šioje temoje pateikta banko užsienio valiutos kurso pasikeitimo proceso apžvalga. Temoje pateikiama informacija apie sąranką, proceso vykdymą, proceso apskaičiavimą ir kurso keitimo operacijų atšaukimą.
author: mikefalkner
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: d7e7006679757d7e779b86c58649cd3869e1c7d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188446"
---
# <a name="bank-foreign-currency-revaluation"></a>Banko užsienio valiutos kurso pasikeitimas

[!include [banner](../includes/banner.md)]


Šioje temoje pateikta banko užsienio valiutos kurso pasikeitimo proceso apžvalga. Temoje aiškinama, kaip nustatyti ir vykdyti procesą, bei pateikiama informacija apie proceso apskaičiavimą. Temoje taip pat aiškinama, kaip atšaukti kurso keitimo operacijas, jei to prireiktų.

Laikotarpio pabaigoje tvarkant apskaitos konvencijas būtina banko sąskaitų balansus užsienio valiuta perkainoti naudojant skirtingus valiutų kursų tipus (dabartinis, retrospektyvinis, vidurkio ir t. t.). Banko užsienio valiutos kurso pasikeitimo funkciją galima naudoti norint perkainoti vieną ar kelias banko sąskaitas. Be to, ši funkcija taip pat yra visuotinė. Tai reiškia, kad lankydamiesi viename puslapyje gali perkainoti visų juridinių subjektų, prie kurių turite prieigą, bankus.

> [!NOTE]
> Kai paleidžiate kurso keitimo procesą, kiekvienos banko sąskaitos, registruotos užsienio valiuta, balansas bus perkainotas. Perkainojimo metu sukurtas negauto pelno arba nuostolio operacijas sugeneruoja sistema. Bus sukurtos dvi operacijos: viena, skirta apskaitos valiutai, o kita – ataskaitų valiutai, jei naudojama ataskaitų valiuta. Kiekvienas apskaitos įrašas bus užregistruotas negauto pelno arba patirto nuostolio sąskaitose ir pagrindinėje sąskaitoje, kurie atliekamas perkainojimas.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Pasiruošimas paleisti užsienio valiutos kurso pasikeitimą

Prieš vykdant perkainojimo procesą reikalinga tolesnė sąranka.

- Puslapyje **Didžioji knyga** nurodykite valiutos kurso tipą. Jei valiutos kurso tipas pagrindinėje sąskaitoje nenurodytas, šis valiutos kurso tipas bus naudojamas atliekant užsienio valiutos kurso keitimą.
- Puslapyje **Didžioji knyga** nurodykite valiutos kurso pasikeitimo gauto pelno, patirtų nuostolių, negauto pelno ir nepatirtų nuostolių sąskaitas. Gauto pelno ir patirto nuostolio sąskaitos naudojamos sudengiant gautinų sumų ir mokėtinų sumų operacijas. Negauto pelno ir nepatirto nuostolio sąskaitos naudojamos norint atlikti atvirų operacijų ir pagrindinių DK sąskaitų perkainojimą.
- Puslapyje **Valiutos kurso pasikeitimo sąskaitos** kiekvienai valiutai ir įmonei parinkite skirtingą valiutos kurso pasikeitimo sąskaitą. Nenurodžius jokios sąskaitos naudojamos sąskaitos iš puslapio **Didžioji knyga**.

## <a name="enable-foreign-currency-revaluation"></a>Užsienio valiutos kurso pasikeitimo įgalinimas

Užsienio valiutos kurso pasikeitimo funkciją turite įjungti prieš vykdydami užsienio valiutos kurso pasikeitimus.

1. Eikite į **Grynųjų pinigų ir banko valdymas \> Sąranka \> Grynųjų pinigų ir banko valdymo parametrai**.
2. Skirtuke **Bendra**, pateiktame srityje **Užsienio valiutos kurso pasikeitimas**, parinktį **Įgalinti banko perkainojimą** nustatykite į **Taip** ir įjunkite šią funkciją dabartiniam juridiniam subjektui. 
3. Skirtuke **Numeracijos** įtraukite užsienio valiutos kurso pasikeitimo numeraciją.
4. Norėdami, kad skiltis **Užsienio valiutos kurso pasikeitimas** būtų rodoma vietos puslapio srityje **Periodinės užduotys**, atnaujinkite naršyklę.

Šią funkciją turite įjungti kiekvienam juridiniam subjektui, kuriame bus naudojama užsienio valiutos kurso pasikeitimo funkcija. Jei jums priskirtas sistemos administratoriaus arba funkcijų valdytojo vaidmuo, galite praleisti šį veiksmą, įgalindami funkciją **Įgalinti pakartotinį banko įvertinimą be parametro** darbo srityje **Funckijų valdymas**.

> [!NOTE]
> Jei jūsų juridiname subjekte naudojamas Rusijos, Lenkijos arba Vengrijos šalies / regiono kodas, banko užsienio valiutos kurso pasikeitimo procedūrą jau galite atlikti. Užsienio valiutos kurso pasikeitimo funkcijos, kuri naudojama kitose šalyse arba regionuose, naudoti negalėsite.

## <a name="process-foreign-currency-revaluation"></a>Užsienio valiutos kurso pasikeitimo apdorojimas

Baigę sąranką ir norėdami perkainoti visų juridinių subjektų vienos ar kelių banko sąskaitų balansus, pasinaudokite puslapiu **Užsienio valiutos kurso pasikeitimas**, pateiktu srityje Grynųjų pinigų ir banko paslaugų valdymas. Galite paleisti procesą realiuoju laiku arba suplanuoti, kad jis būtų paleistas naudojant paketą.

Puslapyje **Užsienio valiutos kurso pasikeitimas** pateikiama kiekvieno perkainojimo proceso retrospektyva. Jame nurodoma, kada procesas buvo vykdytas bei kokie kriterijai nurodyti, ir pateikiamas saitas į kvitą, sukurtą perkainojimo procesui. Puslapyje taip pat nurodoma, ar ankstesnis perkainojimas buvo atšauktas. Norėdami vykdyti perkainojimo procesą, pasirinkite parinktį **Užsienio valiutos kurso pasikeitimas**, pateiktą veiksmų srityje, ir atidarykite dialogo langą **Bankas – užsienio valiutos kurso pasikeitimas**.

Lauke **Perkainojimo data** nurodoma galutinė užsienio valiutos balanso, kuris bus perkainotas, apskaičiavimo data. Perkainojama visa banko operacijų, įvykdytų iki šios datos, suma.

Lauke **Valiutos kurso data** nurodoma valiutos kurso, kuris bus naudojamas valiutos balansams perkainoti, data. Pavyzdžiui, galite perkainoti sausio 31 d. balansus, tačiau taikyti vasario 1 d. nurodytą valiutos kursą.

Perkainojimo procesą galima taikyti vienam arba daugiau juridinių subjektų. Peržiūroje rodomi tik tie juridiniai subjektai, prie kurių turite prieigą. Pasirinkite juridinius subjektus, kuriems norite parinkti užsienio valiutos kurso pasikeitimo procesui tinkamas banko sąskaitas. Visos šių juridinių subjektų banko sąskaitos bus rodomos tinklelyje.

Jei perkainojimo rezultatus norite peržiūrėti prieš juos registruodami, parinktį **Peržiūrėti prieš registruojant** nustatykite į **Taip**. Užsienio valiutos kurso pasikeitimo procedūrai būdinga peržiūra, kurią galima registruoti. Dar kartą vykdyti perkainojimo proceso nereikia. Peržiūros lange pateiktus rezultatus galite eksportuoti į „Microsoft Excel“ ir tokiu būdu kaupti sumų skaičiavimo retrospektyvą. Jei norite peržiūrėti perkainojimo rezultatus, naudoti paketinio vykdymo negalėsite.

Pasirinkite **Gerai** ir vykdykite užsienio valiutos kurso pasikeitimą. Bus sukurtas įrašas, kad galėtumėte sekti kiekvieno vykdymo retrospektyvą. Sukuriamas atskiras kiekvieno juridinio subjekto ir registravimo sluoksnio įrašas.

## <a name="calculate-unrealized-gainloss"></a>Negauto pelno / nuostolio skaičiavimas

Srityje Grynųjų pinigų ir banko valdymas bazome valiuta laikoma banko valiuta, todėl ji nėra perkainojama. Banko sąskaitos balansas apskaitos valiutos srityje perkainojamas naudojant valiutos kursus tarp banko valiutos ir apskaitos valiutos lauke **Valiutos kurso data**. Banko sąskaitos balansas ataskaitų valiutos srityje taip pat perkainojamas naudojant valiutos kursus tarp banko valiutos ir ataskaitų valiutos lauke **Valiutos kurso data**.

Skirtumui tarp banko sąskaitos balanso ir naujo balanso, apskaičiuoto apskaitos valiuta, apskaičiuoti sukuriama operacija. Skirtumui tarp banko sąskaitos balanso ir naujo balanso, apskaičiuoto ataskaitų valiuta, apskaičiuoti sukuriama dar viena operacija. Šių operacijų įrašai pažymimi kaip suderinti. 

Jei banko valiuta atitinka apskaitos valiutą, apskaitos valiutos įrašas nesukuriamas. Jei banko valiuta atitinka ataskaitų valiutą, ataskaitų valiutos įrašas taip pat nesukuriamas.

Be to, užsienio valiutos kurso pasikeitimo operacija išskaidoma po dimensijas, sutinkamas atliekant banko operacijas. Išskaidymas pagrįstas kiekvienos dimensijos balansu. Pvz., bendras banko balansas yra 10 000, tačiau 001 verslo struktūros vieneto balansas yra 4 000, o 002 verslo struktūros vieneto balansas – 6 000. Šiuo atveju 40 procentų perkainojimo sumos registruojama 001 verslo struktūros vieneto perkainojimo sąskaitoje, o 60 procentų – 002 verslo struktūros vieneto perkainojimo sąskaitoje. Jei sąskaitos struktūroje verslo struktūros vienetas neįtrauktas, visa suma registruojama perkainojimo sąskaitoje.

## <a name="reverse-foreign-currency-revaluation"></a>Atšaukti užsienio valiutos kurso pasikeitimą

Jei perkainojimo operaciją reikia atšaukti, pasirinkite puslapio **Užsienio valiutos kurso pasikeitimas** veiksmų srityje pateiktą mygtuką **Atšaukti operaciją**. Sukuriamas naujas užsienio valiutos kurso pasikeitimo retrospektyvos įrašas, skirtas audito retrospektyvai tvarkyti ir naudojamas norint sekti, kada perkainojimas buvo vykdytas arba atšauktas.

Norėdami atšaukti kelis perkainojimus, pirmiausia turite atšaukti naujausią perkainojimą. Tada datų tvarka toliau atšaukite senesnius perkainojimus. Tai atlikę galite vykdyti naujus perkainojimus, susijusius su laikotarpiais, kada atliktus perkainojimus atšaukėte.
