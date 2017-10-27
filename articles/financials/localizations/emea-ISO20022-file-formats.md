---
title: "ISO20022 failų importavimas"
description: "Šioje temoje paaiškinama, kaip importuoti ISO 20022 mokėjimo failų camt.054 ir pain.002 formatų failus į „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimą)."
author: neserovleo
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: fcab30f03aebf7dbe76d5b3b64260f726f291fb8
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

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

## <a name="additional-details"></a>Papildoma informacija

Importuodami formato konfigūraciją iš LCS, jūs importuojate visą konfigūracijos medį, o tai reiškia, kad įtraukiamos modelio ir modelio susiejimo konfigūracijos. Mokėjimo modelyje pradedant nuo 8 versijos susiejimai yra atskirose ER konfigūracijose sprendimų medyje (mokėjimo modelio susiejimas 1611, mokėjimo modelio susiejimas su paskirtimi ISO20022 ir t.t.). Yra daug skirtingų mokėjimo formatų viename modelyje (mokėjimo modelis), todėl atskiras susiejimo tvarkymas yra labai svarbus siekiant nesudėtingai tvarkyti sprendimus. Išnagrinėkime šį scenarijų: galite naudoti ISO20022 mokėjimus norėdami generuoti kredito perkėlimo failus, tada importuoti iš banko gautus pranešimus. Tokiu atveju reikėtų naudoti tokias konfigūracijas:

 - **Mokėjimo modelis**
 - **Mokėjimo modelio susiejimas 1611** – šis susiejimas bus naudojamas generuoti eksportavimo failą
 - **Mokėjimo modelio susiejimas su paskirtimi ISO20022** – ši konfigūracija apima visus susiejimus, kurie bus naudojami importuoti duomenis („į paskirties vietą“ susiejimo kryptis)
 - **ISO20022 kredito pervedimas** – ši konfigūracija apima formato komponentą, kuris atsakingas už eksportavimo failo generavimą (pain.001) pagal mokėjimo modelio susiejimą 1611, taip pat modelio susiejimo komponento formatą, kuris bus naudojamas kartu su mokėjimo modelio susiejimu su paskirtimi ISO20022, kad būtų galima registruoti eksportuotus mokėjimus sistemoje tolesniais importavimo tikslais (importavimas į „CustVendProcessedPayments“ techninę lentelę)
 - **ISO20022 kredito pervedimas (CE)**, kur CE atitinka šalies plėtinį – išvestinis ISO20022 kredito pervedimos formatas su ta pačia struktūra ir tam tikrais kiekvienai šaliai būdingais skirtumais
 - **Pain.002** – šis formatas bus naudojamas kartu su mokėjimo modelio susiejimu su paskirtimi ISO20022, kad būtų galima importuoti pain.002 failą į tiekėjo mokėjimų perkėlimų žurnalą
 - **Camt.054** – šis formatas bus naudojamas kartu su mokėjimo modelio susiejimu su paskirtimi ISO20022, kad būtų galima importuoti camt.054 failą į tiekėjo mokėjimų perkėlimų žurnalą Ta pati formato konfigūracija bus naudojama kliento mokėjimų importavimo funkcijoms, tačiau skirtingų susiejimas bus naudojamas mokėjimo modelio susiejime su paskirties ISO20022 konfigūracija.

Daugiau informacijos apie elektronines ataskaitas žr. [Elektroninių ataskaitų apžvalga](../../dev-itpro/analytics/general-electronic-reporting.md).

## <a name="additional-resources"></a>Papildomi ištekliai
- [Tiekėjo mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą](./tasks/create-export-vendor-payments-iso20022-payment-format.md)
- [Importuoti ISO20022 kredito pervedimo konfigūraciją](./tasks/import-iso20022-credit-transfer-configuration.md)
- [Importuoti ISO20022 tiesioginio debeto konfigūraciją](./tasks/import-iso20022-direct-debit-configuration.md)
- [Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas](./tasks/set-up-company-bank-accounts-iso20022-credit-transfers.md)
- [Nustatyti ISO20022 tiesioginio debeto įmonės banko sąskaitas](./tasks/set-up-company-bank-accounts-iso20022-direct-debits.md)
- [Nustatyti ISO20022 tiesioginio debeto klientus ir klientų banko sąskaitas](./tasks/set-up-bank-accounts-iso20022-direct-debits.md)
- [Nustatyti ISO20022 kredito pervedimo mokėjimo būdą](./tasks/set-up-method-payment-iso20022-credit-transfer.md)
- [ISO20022 tiesioginio debeto mokėjimo būdo nustatymas](./tasks/setup-method-payment-iso20022-direct-debit.md)
- [Nustatyti ISO20022 kredito pervedimų tiekėjus ir tiekėjų banko sąskaitas](./tasks/set-up-vendor-iso20022-credit-transfers.md)

