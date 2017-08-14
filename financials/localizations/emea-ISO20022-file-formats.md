---
title: "ISO20022 failų importavimas"
description: "Šioje temoje paaiškinama, kaip importuoti ISO 20022 mokėjimo failų camt.054 ir pain.002 formatų failus į „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimą)."
author: neserovleo
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01T00:00:00.000Z
ms.dyn365.ops.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 48e280bf0a6c5db237bd389fe448c9d698d3ae12
ms.openlocfilehash: acf6ed5f503d77f372d802a51a71cec062c2b24b
ms.contentlocale: lt-lt
ms.lasthandoff: 07/25/2017

---

# <a name="import-iso20022-files"></a>Importuoti ISO20022 failus

## <a name="overview"></a>Apžvalga
Mokėjimo failus galite importuoti toliau nurodytais formatais.

 - **ISO20022 camt.054 kredito pažyma** – šiuo failų formatu gaunamus mokėjimus importuokite į kliento mokėjimų žurnalą.
 - **ISO20022 pain.002 būsenos grąžinimas** ir **ISO20022 camt.054 debeto pažyma** – importuokite šių failų formatų grąžinamo failus į AP mokėjimų perkėlimų žurnalą.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Būtinosios sąlygos importuojant camt.054 kredito pažymos failą
Norėdami importuoti banko pranešimus į camt.054.001.002 formatą kliento mokėjimų žurnale, turite įvykdyti toliau nurodytas būtinąsias sąlygas.

1. Importuokite **ISO20022 camt.054** elektroninių ataskaitų (ER) konfigūraciją iš „Microsoft Dynamics Lifecycle Services“ (LCS). Tada puslapio **Kliento mokėjimo būdas** lauke **Formato konfigūracijos importavimas** pasirinkite reikiamą konfigūraciją. Daugiau informacijos ieškokite [Mokėjimo būdų failo formatai](emea-select-file-formats-for-the-method-of-payments.md).
2. Puslapyje **Visi klientai** įveskite kiekvieno kliento pavadinimą ir organizacijos numerį.
3. Puslapyje **Kliento banko sąskaita** sukurkite kliento banko sąskaitos įrašą, įvesdami šią informaciją: IBAN arba banko sąskaitos numerį, SWIFT arba banko kodą.
4. Puslapyje **Banko sąskaitos** nustatykite juridinio subjekto banko sąskaitas, įvesdami šią informaciją: IBAN arba banko sąskaitos numerį, SWIFT arba banko kodą, valiutą ir adresą.

    > [!NOTE]
    > Jei planuojate naudoti pažangaus banko derinimą, „FastTab“ srityje **Derinimas** parinktį **Pažangus banko suderinimas** nustatykite į **Taip**. Jei planuojate derinti neužregistruotus importuotus mokėjimus, parinktį **Naudoti banko išrašus kaip elektroninių mokėjimų patvirtinimus** nustatykite į **Taip**.

5. Pasirinktina: puslapyje **Operacijos kodo susiejimas** susiejimą faile nustatykite tarp banko operacijos kodų ir banko operacijos tipų.
6. Jei faile yra operacijos išlaidų, kurias norite registruoti kartu su gaunamais mokėjimais, puslapyje **Kliento mokėjimo mokestis** sukurkite mokėjimo mokestį. Tada puslapyje **Mokėjimo būdai** esančiame mokėjimo mokesčio nustatyme susiekite mokėjimo mokestį su banko sąskaita.
7. Jei bus importuoti ESR mokėjimai ir pateiktos ISR nuorodos (taikoma juridiniams subjektams Šveicarijoje), atlikite toliau nurodytą nustatymą.

    - Lauke **Kliento mokėjimai, sąskaitos ilgis** įveskite kliento kodo, naudojamo ISR nuorodose arba norint automatiškai identifikuoti klientą, ilgį.
    - Įsitikinkite, kad kliento ir SF numeriai (numeracijos) sudaryti tik iš skaičių. Šiuose numeriuose negali būti jokių kitų simbolių. SF numeryje negali būti priekinių nulių.
    - Juridinio subjekto banko sąskaitoje įveskite ESR, BESR ir banko kodą. Daugiau informacijos ieškokite [senesnėje ESR funkcijoje](emea-che-esr-customer-payments-import.md), nes joje pateikti panašūs būtini parametrai.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>camt.054 kredito pažymos failo importavimas į kliento mokėjimų žurnalą
1. Puslapyje **Kliento mokėjimų žurnalo eilutės** spustelėkite **Funkcijos** > **Importuoti mokėjimus**.
2. Pasirinkite mokėjimo būdą su reikiamais ISO20022 camt.054 formatui parametrais.
3. Nurodykite reikiamus parametrus ir failo maršrutą, tada spustelėkite **Gerai**.

Failas importuotas.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Būtinosios sąlygos norint importuoti pain.002 būsenos grąžinimo ir camt.054 debeto pažymos formatų failus į AP mokėjimų perkėlimų žurnalą.
Norėdami importuoti toliau nurodytų ISO20022 formatų banko pranešimus į puslapį **Tiekėjo mokėjimo perkėlimas**, turite įvykdyti toliau nurodytas sąlygas.

1. Importuokite į **ISO20022 camt.054** ir **ISO20022 pain.002** ER konfigūracijas iš LCS.
2. Puslapyje **Tiekėjo mokėjimo būdas** esančiuose laukuose **Grąžinimo formato konfigūracija** ir **Grąžinimo formato antrinė konfigūracija** pasirinkite norimas importuoti ER konfigūracijas. Turėsite suaktyvinti bendrą pasirinktų mokėjimo būdų elektroninio grąžinimo formatą.
3. Puslapyje **Grąžinimo formato būsenos susiejimas** nustatykite būsenos kodų susiejimą tarp pain.002 ir tiekėjo mokėjimo žurnalo būsenų.

    Toliau pateikiamas būsenos nustatymo pavyzdys.

    Grąžinimo būsena | Mokėjimo būsena
    --------------|---------------
    RJCT          | Atmestas
    ACCP          | Priimta
    ACSP          | Gauta

4. Puslapyje **Grąžinimo formato klaidų kodai** nustatykite pain.002 klaidų kodus ir aprašus su išorinės ISO20022 būsenos priežasties kodais.

    Toliau pateikiamas klaidos kodo nustatymo dalies pavyzdys.

    Kodas | Vardas
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Jei camt.054 faile yra operacijos išlaidų, kurias norite registruoti kartu su gaunamais mokėjimais, puslapyje **Tiekėjo mokėjimo mokestis** sukurkite mokėjimo mokestį. Tada puslapyje **Mokėjimo būdai** esančiame mokėjimo mokesčio nustatyme susiekite mokėjimo mokestį su banko sąskaita.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>pain.002 būsenos grąžinimo arba camt.054 debeto pažymos failų importavimas į tiekėjo mokėjimų žurnalą
1. Atidarykite puslapį **Mokėjimo perkėlimai**, esantį mokėtinų sumų meniu.
2. Puslapyje **Mokėjimo perkėlimai** spustelėkite **Grąžinimo failas – tiekėjas**.
3. Pasirinkite mokėjimo būdą su reikiamais ISO20022 failų parametrais, tada spustelėkite **Gerai**.
4. Pasirinkite planuojamą importuoti failo formatą, tada spustelėkite **Gerai**.
5. Nurodykite reikiamus parametrus ir failo maršrutą, tada spustelėkite **Gerai**.

Jei importuojate pain.002 failą, tiekėjo mokėjimo eilučių būsena atnaujinama pagal importuotame faile esančią informaciją.

Jei importuojate camt.054 failą, turite nurodyti toliau pateiktus papildomus parametrus.

- **Mokesčio ID** – įveskite mokesčio ID, pagal kurį bus apibrėžtos naujo mokėjimo mokesčio eilutės, kurios bus sukurtos tiekėjo mokėjimo žurnalo eilutėje, jei camt.054 faile bus nurodyta išlaidų suma.
- **Naujas žurnalo pavadinimas** ir **Naujas žurnalo aprašas** – įveskite žurnalo, į kurį bus perkeltos apdorotos operacijos, pavadinimą ir aprašą. Po perkėlimo naujame žurnale turėtų būti priskirti nauji kvitų numeriai.
- **Importuoti tiesioginio debeto operacijas** – nustatykite šią parinktį į **Taip**, jei į tiekėjo mokėjimų žurnalą reikia importuoti siunčiamą tiesioginį debetą.
- **Žurnalo pavadinimas** – nurodykite naują importuotų tiesioginio debeto operacijų žurnalo pavadinimą.
- **Sudengti operacijas** – nustatykite šią parinktį į **Taip**, jei importuotus tiekėjo mokėjimus reikia sudengti naudojant sistemoje randamas SF.

Importuotą informaciją galite peržiūrėti puslapyje **Mokėjimo perkėlimai**. 

