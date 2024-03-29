---
title: Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas
description: Šioje procedūroje parodoma, kaip nustatyti konkrečios įmonės banko kodo informaciją, kurios reikia norint generuoti mokėjimo failą.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3b3b5ce9d7e24b2b7d3f76e4d770968df897b546df507ba9e3bde5aeac91715
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780775"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Nustatyti ISO20022 kredito pervedimų įmonės banko sąskaitas

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]