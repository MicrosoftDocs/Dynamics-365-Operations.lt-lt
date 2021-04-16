---
title: Kurti pirkimo užsakymus pagal biudžetą
description: Šią procedūrą naudokite norėdami kurti pirkimo užsakymą, kuriam tikrinama, ar pakankamas biudžetas.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a79b19ce4ff35ecc1f691edea1bdc5e30010b433
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821374"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Kurti pirkimo užsakymus pagal biudžetą

[!include [banner](../../includes/banner.md)]

Šią procedūrą naudokite norėdami kurti pirkimo užsakymą, kuriam tikrinama, ar pakankamas biudžetas. Šiame įraše naudojama demonstracinių duomenų įmonė USMF.


## <a name="review-the-budget-control-configuration"></a>Peržiūrėkite biudžeto kontrolės konfigūraciją
1. Eikite į Biudžetas > Sąranka > Biudžeto tikrinimas > Biudžeto tikrinimo konfigūracija.
2. Spustelėkite skirtuką Prieinami biudžeto fondai.
3. Spustelėkite skirtuką Dokumentai ir žurnalai.
4. Spustelėkite skirtuką Apibrėžti biudžeto kontrolės taisykles.
5. Spustelėkite skirtuką Apibrėžti biudžeto grupes.
6. Uždarykite puslapį.

## <a name="create-the-purchase-order-header"></a>Pirkimo užsakymo antraštės kūrimas
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Tiekėjo sąskaita įveskite arba pasirinkite vertę.
4. Išplėskite skyrių Bendra.
5. Lauke Apskaitos data, nustatykite datą „2016-01-01“.
6. Spustelėkite GERAI.

## <a name="add-a-purchase-order-line"></a>Pirkimo užsakymo eilutės įtraukimas
1. Lauke Įsigijimo kategorija įveskite arba pasirinkite reikšmę.
2. Kiekį nustatykite „2‟.
3. Lauke Vienetas įveskite arba pasirinkite reikšmę.
4. Nustatykite Vieneto kainą „10000“.
5. Spustelėkite Finansai.
6. Spustelėkite „Paskirstyti sumas“.
7. Lauke DK sąskaita nurodykite reikšmę „601300-001-023--“.
8. Uždarykite puslapį.

## <a name="perform-budget-checking"></a>Patikrinti biudžetą
1. Spustelėkite Finansai.
2. Spustelėkite Atlikti biudžeto tikrinimą.
3. Spustelėkite Finansai.
4. Spustelėkite Biudžeto tikrinimo klaidos arba įspėjimai.
5. Spustelėkite Uždaryti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]