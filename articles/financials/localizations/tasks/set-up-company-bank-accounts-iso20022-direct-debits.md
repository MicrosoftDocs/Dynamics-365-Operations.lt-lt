---
title: Nustatyti ISO20022 tiesioginio debeto įmonės banko sąskaitas
description: Ši užduotis apžvelgia, kaip nustatyti konkrečios įmonės banko sąskaitos informaciją, kurios reikia norint generuoti kliento mokėjimo failus.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89c4a8d3cb504df97bad5679bf12b3cdb5931d95
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852579"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Nustatyti ISO20022 tiesioginio debeto įmonės banko sąskaitas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši užduotis apžvelgia, kaip nustatyti konkrečios įmonės banko sąskaitos informaciją, kurios reikia norint generuoti kliento mokėjimo failus. Šioje procedūroje kaip pavyzdys naudojamas ISO 20022 tiesioginio debeto formatas. Naudojant kitus formatus gali reikėti papildomos sąrankos informacijos, pvz., įmonės ID arba rūšiavimo kodo.



Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF.



Tai yra antroji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.


## <a name="set-up-the-iban-and-swift-codes"></a>Nustatyti IBAN ir SWIFT kodus
1. Eikite į Grynųjų pinigų ir banko valdymas > Banko sąskaitos.
2. Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „DEMF OPER‟.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pavyzdžiui: spustelėkite DEMF OPER, kad atidarytumėte banko kodo informaciją.  
4. Spustelėkite Redaguoti.
5. Išplėskite arba sutraukite dalį Papildoma identifikacija.
6. Lauke IBAN surinkite reikšmę.
    * Pavyzdžiui, įveskite DE89370400440532013000.  
7. Lauke SWIFT kodas surinkite reikšmę.
    * Pavyzdžiui, įveskite DEUTDEFF.    Atkreipkite dėmesį, kad SWIFT / BIC nereikalingas naudojant daugelį mokėjimo formatų, tačiau vis tiek rekomenduojama užregistruoti banko kodo SWIFT / BIC.  
8. Spustelėkite Įrašyti.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Nustatyti juridinio subjekto banko sąskaitą
1. Pasirinkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai.
2. Spustelėkite Redaguoti.
3. Išplėskite arba sutraukite dalį Banko sąskaitos informacija.
4. Lauke Banko sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pavyzdžiui: pasirinkite DEMF OPER banko kodą.  
6. Spustelėkite Įrašyti.

