--- 
title: "„Kanban“ užduočių planavimas"
description: "Šia procedūra dėmesys skiriamas konkretaus darbo elemento „kanban‟ apdorojimo užduočių planavimui."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f36544993a9280ae10489a19252bc105abd40ac9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="schedule-kanban-jobs"></a>„Kanban“ užduočių planavimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra dėmesys skiriamas konkretaus darbo elemento „kanban‟ apdorojimo užduočių planavimui. Būtina šios procedūros sukūrimo sąlyga yra procedūra „Parengti „kanban“ užduoties procesą, kai nėra reikiamų medžiagų“. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši užduotis yra skirta darbo laiko prižiūrėtojui ir gamybos planuotojui, dirbančiam su „kanban‟.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Pasirinkti darbo elemento „kanban‟ užduotis
1. Pasirinkite Gamybos kontrolė > „Kanban“ > „Kanban“ užduočių planavimas.
2. Išplėsti „FactBox“ Laikotarpio pajėgumas
    * Išplėskite „FactBox“ „Kanban“.  
3. Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite 1250 darbo elementą. Rodinys bus filtruojamas, kad būtų rodomos tik 1250 darbo elemento užduotys.  
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite Pažymėti.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>„Kanban‟ užduotį planuoti pirmajam galimam laikotarpiui
1. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite pirmąją eilutę sąraše, kurios būsena yra Nesuplanuota. Taškinė piktograma lauke Užduoties būsena nurodo nesuplanuotą būseną.  
2. Spustelėkite Planuoti.
    * „Kanban‟ užduotis bus suplanuota pirmajam galimam laikotarpiui.  
    * Atkreipkite dėmesį, kad „kanban“ užduotis perkelta į sąrašo pabaigą, nes ji pridėta į laikotarpį, prasidedantį šiandien.  
    * Jei laikotarpis, prasidedantis šiandien, yra visiškai rezervuotas, užduotis bus perkelta į pirmąjį galimą laikotarpį.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Konkrečiai dienai suplanuoti dvi „kanban‟ užduotis
1. Sąraše pasirinkite 1 eilutę.
    * Turėtumėte matyti, kad pirmosios eilutės lauke Užduoties būsena būsena yra Nesuplanuota.  
2. Sąraše pasirinkite 2 eilutę.
    * Turėtumėte matyti, kad antrosios eilutės lauke Užduoties būsena būsena yra Nesuplanuota. Dabar pasirinktos pirmosios dvi užduotys.  
3. Spustelėdami Grafikas nuo datos, atidarykite išplečiamąjį dialogo langą.
4. Pažymėkite arba atžymėkite langelį Perrašyti pajėgumo trūkumo reakciją.
    * Ši parinktis leidžia nepaisyti numatytosios pajėgumo trūkumo reakcijos.  
5. Lauke Pajėgumo trūkumo reakcija pasirinkite „Įtraukti į reikalaujamą laikotarpį‟.
    * Ši parinktis užtikrins, kad užduotis būtų pridėta į reikiamą laikotarpį, neatsižvelgiant į tai, kad darbo elementas gali būti perkrautas.  
6. Spustelėkite Planuoti.
    * Atkreipkite dėmesį, kad abi užduotys pridėtos į norimą laikotarpį.  
    * Dalyje Laikotarpio pajėgumas galite matyti kiekvieno laikotarpio apkrovą. Lauke Suvartojimas rodomas suplanuotas suvartojimas šiuo laikotarpiu. Jei suplanuotas suvartojimas yra didesnis nei galimas pajėgumas per šį laikotarpį, bus pasirinktas perkrautas suvartojimas.  


