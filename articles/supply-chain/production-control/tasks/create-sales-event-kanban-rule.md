---
title: Kurti pardavimo įvykio „kanban“ taisyklę
description: Šia procedūra sutelkiamas dėmesys į nustatymus, reikalingus norint sukurti „kanban“ taisyklę, kuri veikia kuriant pardavimo užsakymą.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2bee6e81acd029406c95237f0b4ba4ab2565ea1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "342022"
---
# <a name="create-a-sales-event-kanban-rule"></a>Kurti pardavimo įvykio „kanban“ taisyklę

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra sutelkiamas dėmesys į nustatymus, reikalingus norint sukurti „kanban“ taisyklę, kuri veikia kuriant pardavimo užsakymą. Įvykio „kanban“ taisyklė papildo reikalavimus, kylančius iš pardavimo užsakymo eilučių. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ji skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia naujos arba pakeistos prekės gamybą.




## <a name="create-a-new-kanban-rule"></a>Kurti naują „kanban“ taisyklę
1. Eikite į „Kanban“ taisyklės.
2. Spustelėkite Naujas.
3. Lauke Papildymo strategija pasirinkite „Įvykis“.
    * Pasirinkus Įvykis reiškia, kad „kanban“ taisyklę nulemia įvykis, pvz., pardavimo užsakymo eilutės kūrimas.   Tai taikoma toms sritims, kuriose kiekvienas „kanban“ turėtų patenkinti tam tikrus poreikius.  
4. Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.
    * Pasirinkite Galutinis surinkimas.  
5. Išplėskite skyrių Išsami informacija.
6. Lauke Produktas įveskite arba pasirinkite reikšmę.
    * Pažymėkite L0050.  

## <a name="define-an-event"></a>Įvykio apibrėžimas
1. Išplėskite skyrių Įvykiai.
2. Lauke Pardavimo įvykis pasirinkite „Automatinis“.
    * Pasirinkus pardavimo įvykį Automatinis, kai pardavimo eilutė sutaps su produkto ir gavimo vieta, ši „kanban“ taisyklė bus paleidžiama automatiškai. Šioje procedūroje tai produktas L0050 13 sandėlyje.  
3. Nustatykite pasirinkties Mažiausias įvykio kiekis reikšmę „50“.
    * Kai Mažiausias įvykio kiekis yra 50, „kanban“ taisyklę naudos tik tie įvykiai, kurių kiekis yra 50 arba didesnis.  
4. Išplėskite skyrių Gamybos eiga.
    * Atkreipkite dėmesį, kad Gavimo vieta yra 13 sandėlis. Tai reiškia, kad ši „kanban“ taisyklė bus taikoma šiai vietai.  
    * Šiame pavyzdyje šią „kanban“ taisyklę paleis produkto pardavimo eilutė L0050, kurioje nurodytas 13 sandėlio kiekis yra 50 arba didesnis.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Pardavimo eilutės kūrimas ir įvykio „kanban“ taisyklės paleidimas
1. Eikite į Visi pardavimo užsakymai.
    * Įrašius „kanban“ taisyklę rodomas įspėjimas, o tai reiškia, kad „kanbans“ bus sukurti realiuoju laiku kuriant pardavimo užsakymą.  
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite US-003.  
4. Spustelėkite GERAI.
5. Lauke „Prekės numeris“ įveskite „L0050“.
6. Lauke Vieta įveskite „1“.
    * Pasirinkite 1 vietą, nes 13 sandėlis yra 1 vietoje.  
7. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
    * Nustatykite pasirinkties Sandėlis reikšmę 13.  
8. Nustatykite kiekį – 75.
    * Įveskite kiekį 50 arba didesnį, kad paleistumėte „kanban“ taisyklę.  

## <a name="verify-that-kanban-is-created"></a>Patikrinkite, ar „kanban“ sukurtas
1. Spustelėkite Produktas ir tiekimas.
2. Spustelėkite Peržiūrėti iškvietimo medį.
    * Atkreipkite dėmesį, kad sukuriamas „kanban“, kurio kiekis toks pat, kaip pardavimo eilutė. Taip pat galite matyti, kokios medžiagos turi būti išduotos norint pagaminti L0050. Tai yra paskutinis šios procedūros veiksmas.  

