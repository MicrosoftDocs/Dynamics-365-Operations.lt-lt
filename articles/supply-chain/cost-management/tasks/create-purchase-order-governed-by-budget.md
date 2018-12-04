--- 
title: "Kurti pirkimo užsakymus pagal biudžetą"
description: "Šią procedūrą naudokite norėdami kurti pirkimo užsakymą, kuriam tikrinama, ar pakankamas biudžetas."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc024caa54db6629a1e573df295fe8333996647
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-governed-by-budget"></a>Kurti pirkimo užsakymus pagal biudžetą

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


