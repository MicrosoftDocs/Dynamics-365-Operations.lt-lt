--- 
title: "RFQ kainos pasiūlymų įvedimas bei lyginimas ir sutarčių pasirinkimas"
description: "Šia procedūra rodoma, kaip į RFQ įvesti atsakymų, vertinti bei lyginti kainos pasiūlymus ir tada pasirinkti vieno iš tiekėjo kainos pasiūlymą."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7cd4876acfebcc9595abb358cfc9b355e93041d6
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>RFQ kainos pasiūlymų įvedimas bei lyginimas ir sutarčių pasirinkimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra rodoma, kaip į RFQ įvesti atsakymų, vertinti bei lyginti kainos pasiūlymus ir tada pasirinkti vieno iš tiekėjo kainos pasiūlymą. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Prieš pradedant reikia turėti RFQ su dviem eilutėmis, išsiųstą bent dviem tiekėjams. Norėdami tokį sukurti, kaip būtinąjį komponentą galite vykdyti procedūrą „Pasiūlymo patvirtinimo kūrimas“. Šios procedūros vykdyti negalėsite tol, kol nenustatysite vertinimo kriterijų.


## <a name="enter-a-reply-from-a-vendor"></a>Atsakymo iš tiekėjo įvedimas
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Visi pasiūlymų patvirtinimai.
2. Pasirinkite RFQ, kurio būsena yra Išsiųstas ir spustelėkite saitą ant pasiūlymo patvirtinimo atvejo numerio.
    * RFQ turėjo būti išsiųstas bent 2 tiekėjams.  
3. Spustelėdami antraštę, pereikite į tiekėjų sąrašą.
4. Pasirinkite tiekėją, kuriam RFQ dokumente norite įvesti atsakymą.
5. Spustelėkite Įvesti atsakymą.
6. Veiksmų srityje spustelėkite Atsakymas.
7. Spustelėkite Kopijuoti duomenis į atsakymą.
    * Šiuo veiksmu bus kopijuojami pasirinkti duomenys, pvz., kiekis iš RFQ atvejo į RFQ atsakymą. Taip pat šį veiksmą galite praleisti ir visus atsakymo laukus užpildyti rankiniu būdu, redaguodami atsakymą.  
8. Spustelėkite Redaguoti.
9. Lauke Vieneto kaina įveskite skaičių.
10. Pasirinkite kitą pasiūlymo eilutę.
11. Lauke Vieneto kaina įveskite skaičių.

## <a name="score-the-bid"></a>Kainos pasiūlymo vertinimas
1. Spustelėdami antraštę, pereikite prie kainos pasiūlymo vertinimo.
2. Išplėskite dalį Kainos pasiūlymo vertinimas.
3. Lauke Rezultatas įveskite vieno iš vertinimo kriterijų skaičių.
    * Jei ant vieno iš vertinimo kriterijų užvedate pele, patariama, kokiame intervale turi būti jūsų rezultatas. Šioje demonstracijoje į bet kurį iš kriterijų galite įtraukti skaičių nuo 1 iki 5.  
4. Pasirinkite kitą vertinimo kriterijų.
5. Lauke Rezultatas įveskite skaičių.
6. Išplėskite dalį Klausimynai.
    * Jei RFQ atvejyje yra tiekėjams išsiųstas klausimynas, jų atsakymus galite įvesti klausimyno skyriuje.  
7. Uždarykite puslapį.

## <a name="enter-a-reply-for-another-vendor"></a>Kito tiekėjo atsakymo įvedimas
1. Pasirinkite kitą tiekėją – išvalykite tiekėją, kuriam ką tik įvedėte atsakymą ir pasirinkite kito tiekėjo eilutę.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Spustelėkite Įvesti atsakymą.
4. Spustelėkite Kopijuoti duomenis į atsakymą.
5. Spustelėkite Redaguoti.
6. Lauke Vieneto kaina įveskite skaičių.
7. Pasirinkite kitą pasiūlymo eilutę.
8. Lauke Vieneto kaina įveskite skaičių.

## <a name="score-the-second-bid"></a>Antro kainos pasiūlymo vertinimas
1. Spustelėdami antraštę, pereikite prie kainos pasiūlymo vertinimo.
2. Lauke Rezultatas įveskite skaičių.
3. Sąraše raskite ir pasirinkite norimą įrašą.
4. Lauke Rezultatas įveskite skaičių.

## <a name="compare-the-replies"></a>Atsakymų palyginimas
1. Veiksmų srityje spustelėkite Bendra.
2. Spustelėkite Palyginti atsakymus.
3. Lauke Reitingas įveskite skaičių.
    * Šiame puslapyje rodomi kainų pasiūlymai su antrašte ir eilutėmis bei bendras rezultatas antraštės lygyje. Eilutes galite palyginti jas rūšiuodami tinklelyje, kad palyginamos eilutės būtų viena šalia kitos. Taip pat pateikiama tolesnė informacija. Kiekis: tiekėjo pasiūlytas kiekis. Jis gali skirtis nuo RFQ nurodyto kiekio.   Grynoji suma – atėmus visas nuolaidas tiekėjo siūloma kaina už eilutėje nurodytas prekes.   Nuokrypis: dienų skaičius, kuriuo kainos pasiūlymo antraštėje arba eilutėje nurodyta pristatymo data skiriasi nuo pageidaujamos RFQ antraštėje arba RFQ eilutėje nurodytos pristatymo datos.   Galite įvesti kiekvieno kainos pasiūlymo reitingą.  
4. Pasirinkite kito norimo reitinguoti kainos pasiūlymo antraštės eilutę.
5. Lauke Reitingas įveskite skaičių.
6. Spustelėkite Įrašyti.

## <a name="reject-a-bid"></a>Kainos pasiūlymo atmetimas
1. Pasirinkite norimo atmesti kainos pasiūlymo antraštės eilutę.
    * Vienu metu vieną kainos pasiūlymą ar vieno kainos pasiūlymo eilutes galite tik priimti, atmesti arba grąžinti.  
2. Pažymėkite žymės langelį Žymėti.
    * Jei kainos pasiūlymo antraštėje pažymėsite žymės langelį Žymėti, taip pat bus pažymėtos visos eilutės. Taip pat galite pasirinkti pažymėti kainos pasiūlymo eilučių subrinkinį ir taip jas atmesti arba priimti. Galima dėl kai kurių RFQ eilučių priimti vieno tiekėjo kainos pasiūlymą, o kitas RFQ eilutes paskirti kitam tiekėjui, tačiau tai atlikti reikia 2 veiksmais, vienu metu dirbant su vienu kainos pasiūlymu. Jei yra pakaitinių eilučių, galite priimti tik pradinę pasiūlymo eilutę arba jos pakaitą, bet ne abu.  
3. Spustelėkite Atmesti.
4. Spustelėdami Parametrai atidarykite išplečiamąjį dialogo langą.
5. Lauke Atmetimo priežastis įveskite arba pasirinkite reikšmę.
    * Atmetimo priežastis bus išsaugota atsakyme.  
6. Spustelėkite GERAI.
7. Spustelėkite GERAI.
8. Uždarykite puslapį.
9. Uždarykite puslapį.
10. Atnaujinkite puslapį.

## <a name="accept-a-bid"></a>Kainos pasiūlymo priėmimas
1. Pasirinkite pasiūlymą, kurį norite priimti ir spustelėkite lauke Pasiūlymo patvirtinimas esantį saitą.
2. Veiksmų srityje spustelėkite Atsakymas.
3. Spustelėkite Priimti.
    * Jei pažymėjote konkrečias eilutes, į priėmimo veiksmą bus įtrauktos tik pažymėtos eilutės. Jei norite priimti visas kainos pasiūlymo eilutes, tada eilučių žymėti nereikia.  
4. Spustelėdami Parametrai atidarykite išplečiamąjį dialogo langą.
    * Taip galite įrašyti kainos pasiūlymo priėmimo priežastį. Priežastis bus išsaugota kainos pasiūlyme.  
5. Lauke Priėmimo priežastis įveskite arba pasirinkite reikšmę.
6. Spustelėkite GERAI.
7. Spustelėkite GERAI.
    * Spustelėjus Gerai, pagal eilutes, įtrauktas į RFQ priėmimą, sugeneruojamas pirkimo užsakymas. Jei yra kitų neapdorotų (priimtų, atmestų ar grąžintų) kainos pasiūlymų, sistema jus paragins likusius kainos pasiūlymus atmesti.  

## <a name="view-the-purchase-order-thats-been-generated"></a>Sugeneruoto pirkimo užsakymo peržiūra
1. Veiksmų srityje spustelėkite Bendra.
2. Spustelėkite Pirkimo užsakymas.
    * Čia galite peržiūrėti pirkimo užsakymą, kuris buvo sugeneruotas, kai priėmėte kainos pasiūlymą.  
3. Uždarykite puslapį.
4. Uždarykite puslapį.
5. Uždarykite puslapį.
6. Uždarykite puslapį.


