--- 
title: "Kurti „kanban“ taisyklę naudojant minimalių atsargų įvykį"
description: "Šioje procedūroje dėmesys skiriamas sąrankai, kuri reikalinga siekiant „kanban“ taisyklę kurti pagal minimalių atsargų įvykį ir užtikrinti, kad konkrečioje vietoje visada turima konkretaus produkto."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c480b518925a8536ebb77d60fcf1f1a548b097f
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# Kurti „kanban“ taisyklę naudojant minimalių atsargų įvykį

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje dėmesys skiriamas sąrankai, kuri reikalinga siekiant „kanban“ taisyklę kurti pagal minimalių atsargų įvykį ir užtikrinti, kad konkrečioje vietoje visada turima konkretaus produkto. „Kanban“ taisyklė sukuriama, siekiant medžiagą perkelti į vietą, kai atsargų lygis būna mažesnis nei 200 vienetų. Vykdant iškvietimo įvykių apdorojimą, sukuriami reikiami „kanban“. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši užduotis skirta proceso inžinieriui arba vertės srauto vadovui, nes jie parengia naujos arba pakeistos prekės gamybą „lean“ aplinkoje.


## Kurti naują „kanban“ taisyklę
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

## Nustatyti mažiausią galimą prekės kiekį
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

## Paleisti paketinę įvykio kūrimo užduotį
1. Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ užduoties paketinis apdorojimas > Iškvietimo įvykių apdorojimas.
2. Spustelėkite GERAI.
3. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite anksčiau sukurtą „kanban“ taisyklę.  
5. Išplėskite skyrių „Kanbans“.
    * Atkreipkite dėmesį, kad „kanban“ buvo sukurtas, siekiant reikiamą medžiagą perkelti į 12-ąjį sandėlį.  


