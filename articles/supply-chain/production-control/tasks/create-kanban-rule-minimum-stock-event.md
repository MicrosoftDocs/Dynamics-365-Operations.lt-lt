---
title: Kurti „kanban“ taisyklę naudojant minimalių atsargų įvykį
description: Šioje procedūroje dėmesys skiriamas sąrankai, kuri reikalinga siekiant „kanban“ taisyklę kurti pagal minimalių atsargų įvykį ir užtikrinti, kad konkrečioje vietoje visada turima konkretaus produkto.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3213fac9875a1fd7824be71236cc0d2efb3274a81b33335756a0dd7391fcbfdb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745531"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Kurti „kanban“ taisyklę naudojant minimalių atsargų įvykį

[!include [banner](../../includes/banner.md)]

Šioje procedūroje dėmesys skiriamas sąrankai, kuri reikalinga siekiant „kanban“ taisyklę kurti pagal minimalių atsargų įvykį ir užtikrinti, kad konkrečioje vietoje visada turima konkretaus produkto. „Kanban“ taisyklė sukuriama, siekiant medžiagą perkelti į vietą, kai atsargų lygis būna mažesnis nei 200 vienetų. Vykdant iškvietimo įvykių apdorojimą, sukuriami reikiami „kanban“. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši užduotis skirta proceso inžinieriui arba vertės srauto vadovui, nes jie parengia naujos arba pakeistos prekės gamybą „lean“ aplinkoje.


## <a name="create-a-new-kanban-rule"></a>Kurti naują „kanban“ taisyklę
1. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
2. Spustelėkite Naujas.
3. Lauke Tipas pasirinkite Išėmimas.
    * Šis tipas naudojamas perkėlimo „kanban‟ kurti.  
4. Lauke Papildymo strategija pasirinkite „Įvykis“.
    * Įvykio strategija naudojama, kad pagal įvykį būtų sukurti perkėlimo „kanban‟. Vėliau procedūros metu perkėlimo „kanban“ suaktyvinsite naudodami atsargų papildymą.  
5. Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.
    * Įveskite arba pasirinkite ReplenishSpeakerComponents. Šios perkėlimo veiklos gavimo (išeigos) sandėlis ir vieta yra 12 – tai reiškia, kad medžiagos bus perkeltos į 12-ojo sandėlio 12-ąją vietą.  
6. Išplėskite skyrių Išsami informacija.
7. Lauke Produktas įveskite arba pasirinkite reikšmę.
    * Pažymėkite M0007.  
8. Išplėskite skyrių Įvykiai.
9. Lauke Atsargų papildymo įvykis pasirinkite Paketas.
    * Taip sukuriamas „kanban“, siekiant medžiagų poreikius susijusioje vietoje patenkinti iškvietimo įvykių apdorojimo metu.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Nustatyti mažiausią galimą prekės kiekį
1. Lauke Produktas spustelėkite saitą.
2. Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Prekės numeris.
3. Išplėskite „FactBox“ Produkto vaizdas.
4. Veiksmų srityje spustelėkite Planuoti.
5. Spustelėkite Prekės padengimas.
6. Spustelėkite Naujas.
7. Sąraše pažymėkite pasirinktą eilutę.
8. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
    * Nustatykite pasirinkties Sandėlis reikšmę 12.  
9. Nustatyti lauko Mažiausias kiekis reikšmę į 200.

## <a name="run-the-batch-event-creation-job"></a>Paleisti paketinę įvykio kūrimo užduotį
1. Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ užduoties paketinis apdorojimas > Iškvietimo įvykių apdorojimas.
2. Spustelėkite GERAI.
3. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite anksčiau sukurtą „kanban“ taisyklę.  
5. Išplėskite skyrių „Kanbans“.
    * Atkreipkite dėmesį, kad „kanban“ buvo sukurtas, siekiant reikiamą medžiagą perkelti į 12-ąjį sandėlį.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]