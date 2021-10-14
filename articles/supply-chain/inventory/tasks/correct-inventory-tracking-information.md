---
title: Taisyti atsargų sekimo informaciją
description: Ši procedūra padės kūrimo ir atsargų perkėlimo žurnalo registravimo proceso metu, kad pakoreguotumėte atsargų sekimo informaciją.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69921651ecd0969e9cdd3cdd3740db212a1953e1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573806"
---
# <a name="correct-inventory-tracking-information"></a>Taisyti atsargų sekimo informaciją

[!include [banner](../../includes/banner.md)]

Ši procedūra padės kūrimo ir atsargų perkėlimo žurnalo registravimo proceso metu, kad pakoreguotumėte atsargų sekimo informaciją. Šiame pavyzdyje atnaujinsime paketo valdomos prekės informaciją, pakeitę neteisingai užregistruotą paketą į kitą paketą. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonės USPI arba savo duomenis. Jei naudojate savo duomenis, jums reikia turėti prekę, kurios paketas įgalintas ir jis neturi būti kontroliuojamas pagal vietą. Be to, norint atlikti atsargų perkėlimą, turi būti nustatytas atsargų žurnalo pavadinimas. Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.


## <a name="create-an-inventory-transfer-journal"></a>Kurkite atsargų perkėlimo žurnalą
1. Eikite į Perkėlimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
4. Spustelėkite GERAI.

## <a name="create-journal-lines"></a>Žurnalo eilučių kūrimas
1. Spustelėkite Naujas.
2. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Jei naudojate USPI, pasirinkite M5003.  
3. Lauke Kiekis įveskite skaičių.
4. Spustelėkite skirtuką Atsargų dimensijos.
5. Lauke Paketo numeris įveskite arba pasirinkite vertę.
6. Lauke Teritorija įveskite arba pasirinkite reikšmę.
7. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
8. Lauke Paketo numeris įveskite arba pasirinkite vertę.

## <a name="post-the-journal"></a>Registruoti žurnalą
1. Spustelėkite Registruoti.
2. Spustelėkite GERAI.

## <a name="check-tracing-information"></a>Tikrinti sekimo informaciją
1. Spustelėkite Atsargos.
2. Spustelėkite Sekti.
3. Spustelėkite GERAI.
    * Naudodami šią sekimo informaciją galite sekti pagal paketą, pagal kurį ištaisėte atsargas.  Taip pat galite naudoti Prekės sekimo puslapį norėdami pamatyti šią informaciją.  
4. Uždarykite puslapį.

## <a name="check-inventory-transactions"></a>Tikrinti atsargų operacijas
1. Spustelėkite Atsargos.
2. Spustelėkite Operacijos.
    * Čia galite pamatyti operacijas, kurios buvo sukurtos užregistravus jūsų žurnalą.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]