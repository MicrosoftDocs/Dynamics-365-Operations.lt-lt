---
title: Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas
description: Šioje procedūroje parodoma, kaip nustatyti konkrečios įmonės banko kodo informaciją, kurios reikia norint generuoti mokėjimo failą.
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
ms.openlocfilehash: 2bbbf55ed28ad2131d7e1253dd44842d85d39315
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174970"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip nustatyti konkrečios įmonės banko kodo informaciją, kurios reikia norint generuoti mokėjimo failą. Galite nustatyti informaciją, kurios reikia norint generuoti ISO 20022 kredito pervedimo formatą, tačiau, atsižvelgiant į formatą, gali būti reikalinga kita informacija, pvz., įmonės ID arba rūšiavimo kodas. 

Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.

Tai yra antroji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="set-up-iban-and-swift-code"></a>IBAN ir SWIFT kodo nustatymas
1. Eikite į Grynųjų pinigų ir banko valdymas > Banko sąskaitos.
2. Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „DEMF OPER‟.
3. Spustelėkite DEMF OPER, kad atidarytumėte banko kodo informaciją.
4. Spustelėkite Redaguoti.
5. Išplėskite skyrių Papildoma identifikacija.
6. Lauke IBAN surinkite „DE89370400440532013000‟.
7. Lauke SWIFT kodas surinkite „DEUTDEFF‟.
    * Atkreipkite dėmesį, kad SWIFT / BIC nereikalingas naudojant daugelį mokėjimo formatų, tačiau vis tiek rekomenduojama užregistruoti banko kodo SWIFT / BIC.  
8. Spustelėkite Įrašyti.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Juridinio subjekto banko kodo nustatymas
1. Pasirinkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai.
2. Spustelėkite Redaguoti.
3. Išplėskite skyrių Banko sąskaitos informacija.
4. Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.
5. Spustelėkite Įrašyti.

