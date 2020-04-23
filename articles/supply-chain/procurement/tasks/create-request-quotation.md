---
title: Kurti pasiūlymo patvirtinimą
description: Šia procedūra parodoma, kaip kurti pasiūlymo patvirtinimą.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2c13ed20ec86108bcb9edc0d20d53ff98732b9d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204751"
---
# <a name="create-a-request-for-quotation"></a>Kurti pasiūlymo patvirtinimą

[!include [banner](../../includes/banner.md)]

Šia procedūra parodoma, kaip kurti pasiūlymo patvirtinimą. Paprastai tai atlieka pirkimo agentas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis. Prieš pradėdami turite nustatyti siūlymų tipus. Atlikę šią užduotį ir sukūrę bei išsiuntę RFQ, galite įvesti atsakymus pagal tiekėją, juos palyginti ir pasirinkti sutartį.


## <a name="prepare-a-new-rfq"></a>Naujo RFQ parengimas
1. Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Visi pasiūlymų patvirtinimai**.
2. Spustelėkite **Naujas**.
    Galimi tolesni pirkimo tipai. Pirkimo užsakymas (numatytasis tipas): dokumentas, kuriuo patvirtinamas siūlymas pirkti produktų arba priimamas siūlymas parduoti produktų už užmokestį. Pirkimo paraiška: šis tipas pasirenkamas automatiškai, jei RFQ kuriate tiesiai iš pirkimo paraiškos. Jei šią parinktį pasirinksite rankiniu būdu, gausite klaidą. Pirkimo sutartis: susitarimas per tam tikrą laikotarpį nupirkti tam tikrą produktų kiekį arba tam tikros vertės produktų. Jei pasirenkate šią parinktį, turite pasirinkti datų intervalą, taikomą pirkimo sutarčiai.  
3. Lauke **Dokumento antraštė** įveskite reikšmę.
4. Lauke **Siūlymo tipas** įveskite arba pasirinkite reikšmę.
    + Jei vertinimo būdas susietas su siūlymo tipu, jis bus numatytasis jūsų kuriamo RFQ vertinimo būdas. Vertinimo būdą vėliau galima pakeisti.  
    + Lauke **Pristatymo data** įveskite datą.  
    + Pasirinkite datą, iki kurios norite gauti prekes.  
    + Lauke **Galiojimo data ir laikas** įveskite datą ir laiką.  
    + Nurodykite datą ir laiką, iki kurių tiekėjai turi atsakyti į RFQ.  
5. **Sandėlio lauke** įveskite arba pasirinkite reikšmę. Numatytasis pristatymo adresas bus sandėlio adresas.  
6. Spustelėkite **Gerai**.

## <a name="add-lines"></a>Pridėti eilutes

Nurodę pagrindinę informaciją apie RFQ, galite nurodyti prekes arba paslaugas, kurių kainos pasiūlymus turi teikti tiekėjai. Numatytasis eilutės tipas yra Prekė.

1. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę. Jei naudojate USMF, galite pasirinkti T0020.  
2. Lauke **Kiekis** įveskite skaičių.
3. Spustelėkite **Pridėti eilutę**.
4. Lauke **Eilutės tipas** pasirinkite Kategorija. Naudodami tipą Kategorijos eilutė, galite kurti ne atsargų prekių ar paslaugų RFQ. Tada iš įsigijimo kategorijų hierarchijos turite pasirinkti prekių ar paslaugų tipą.  
5. Lauke **Įsigijimo kategorija** įveskite arba pasirinkite reikšmę.
6. Lauke **Produkto gavimo kvitas** įveskite vertę.
7. Lauke **Kiekis** įveskite skaičių.
8. Lauke **Vienetas** įveskite arba pasirinkite reikšmę.

## <a name="add-vendors"></a>Įtraukti tiekėjų
1. Spustelėdami **Antraštė**, rodinį Eilutės pakeisite į rodinį Antraštė. 
2. Išplėskite sekciją **Tiekėjas**.
3. Spustelėkite **Automatiškai įtraukti tiekėjų**. Tiekėjų į RFQ galite įtraukti automatiškai pagal pageidaujamų prekių įsigijimo kategoriją. Jei nėra patvirtintų eilutėse įtrauktų kategorijų tiekėjų, jų įtraukti galite rankiniu būdu.  
4. Spustelėkite **Pridėti**.
5. Lauke **Tiekėjo paskyra** įveskite arba pasirinkite reikšmę.
6. Spustelėkite **Pridėti**.
7. Lauke **Tiekėjo paskyra** įveskite arba pasirinkite reikšmę. Kai pasirenkate tiekėją, būsena yra Sukurtas. Tai reiškia, kad tiekėjo informacija buvo įrašyta į RFQ, tačiau RFQ nebuvo išsiųstas tiekėjui. Galite pridėti tiekėją prie RFQ, nepriklausomai nuo jo statuso.  

## <a name="send-the-rfq-to-vendors"></a>Siųsti RFQ tiekėjams
1. **Veiksmų srityje** spustelėkite **Siųsti**. Puslapyje Pasiūlymo patvirtinimo siuntimas patikrinkite, ar sąraše esantys tiekėjai yra tie, kurie turi gauti RFQ.  
2. Spustelėkite **Spausdinti**. Naudodami šį dialogo langą galite spausdinti RFQ. Jei pasirinksite spausdinti atsakymų lapą, jo turinys apibrėžtas įsigijimo ir šaltinio pasirinkimo parametruose. Norėdami pasirinkti, kaip spausdinti atsakymų lapus, atidarę dialogo langą Spausdinti, spustelėkite Papildomos spausdinimo parinktys. Kiekvienam tiekėjui bus išspausdintas vienas RFQ su eilutėmis, kurių būsena – Sukurta arba Išsiųsta. Atšauktos eilutės ir eilutės su registruotas atsakymais nebus išspausdintos.   
3. Spustelėkite **Atšaukti**.
4. Spustelėkite **Gerai**.
5. Uždarykite puslapį.
6. Uždarykite puslapį.

## <a name="view-the-rfq-journal"></a>RFQ žurnalo peržiūra
1. Eikite į **Įsigijimas ir šaltinio pasirinkimas > Pasiūlymų patvirtinimai > Pasiūlymo patvirtinimų sekimas > Pasiūlymo patvirtinimų žurnalai**.
2. Spustelėkite **Peržiūrėti / spausdinti**.
3. Spustelėkite **Originalo peržiūra**.
4. Uždarykite puslapį.
5. Uždarykite puslapį.

