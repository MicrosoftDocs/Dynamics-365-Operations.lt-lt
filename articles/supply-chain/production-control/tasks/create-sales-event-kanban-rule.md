---
title: Kurti pardavimo įvykio „kanban“ taisyklę
description: Šia procedūra sutelkiamas dėmesys į nustatymus, reikalingus norint sukurti „kanban“ taisyklę, kuri veikia kuriant pardavimo užsakymą.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cd2b579e542b9f905fc51b63f2120e5a5c883ae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566652"
---
# <a name="create-a-sales-event-kanban-rule"></a>Kurti pardavimo įvykio „kanban“ taisyklę

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]