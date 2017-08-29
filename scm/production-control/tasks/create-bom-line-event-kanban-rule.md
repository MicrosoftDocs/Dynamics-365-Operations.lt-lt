--- 
title: "KS eilutės „kanban“ taisyklės kūrimas"
description: "Šioje užduotyje parodoma, ką ir kaip reikia nustatyti, norint sukurti įvykio „kanban“ taisyklę, siekiant užtikrinti gamybos KS eilučių tiekimą mišrioje „lean‟ ir klasikinėje gamybos aplinkoje."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
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
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 97fab2f372221cd6757531088d88b28571f07ab8
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a>KS eilutės „kanban“ taisyklės kūrimas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje užduotyje parodoma, ką ir kaip reikia nustatyti, norint sukurti įvykio „kanban“ taisyklę, siekiant užtikrinti gamybos KS eilučių tiekimą mišrioje „lean‟ ir klasikinėje gamybos aplinkoje. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF. Ši užduotis skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia naujos arba pakeistos prekės gamybą.


## <a name="create-a-new-kanban-rule"></a>Kurti naują „kanban“ taisyklę
1. Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ kiekio skaičiavimas > „Kanban“ taisyklės.
2. Spustelėkite Naujas.
3. Lauke Tipas pasirinkite Išėmimas.
    * Tipas Išėmimas naudojamas kurti perkėlimo „kanban‟ signalams.  
4. Lauke Papildymo strategija pasirinkite „Įvykis“.
    * Įvykio strategija pasirenkama, kad pagal įvykį būtų sukurtas „kanban‟ signalų perkėlimas. Vėliau šiame užduoties vadove ją paleisime įvertindami gamybos užsakymą.  
5. Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.
    * Įveskite arba pasirinkite ReplenishSpeakerComponents. Šios perkėlimo veiklos gavimo (išeigos) sandėlis ir vieta yra 12 – tai reiškia, kad medžiaga bus perkelta į 12-ojo sandėlio 12-ąją vietą.  
6. Išplėskite skyrių Išsami informacija.
7. Lauke Produktas įveskite arba pasirinkite M0001.
8. Išplėskite skyrių Įvykiai.
9. Lauke KS eilutės įvykis pasirinkite Automatinis.
    * Kai laukas KS eilutės įvykis nustatytas į Automatinis, tenkinti gamybos užsakymo KS eilučių medžiagų poreikiams bus sukurtas „kanban“.  
10. Uždarykite puslapį.

## <a name="create-and-modify-a-new-production-order"></a>Naujo gamybos užsakymo kūrimas ir modifikavimas
1. Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.
2. Spustelėkite Naujas gamybos užsakymas.
3. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Įveskite arba pasirinkite L0001. Naudojame prekę L0001, nes prekė M0001 yra įtraukta į prekės L0001 KS.  
4. Spustelėkite Kurti.
5. Sąraše spustelėkite saitą L0001 eilutėje.
6. Spustelėkite KS.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Spustelėkite Redaguoti.
9. Lauke Eilutės tipas pasirinkite Iškviestas tiekimas.
    * Pasirenkamas iškviestas tiekimas, kad būtų suaktyvintas „kanban‟ tiekimo kūrimas.  
10. Lauke Išteklių suvartojimas pasirinkite Ne.
    * Išvalius žymės langelį Išteklių suvartojimas, galima pakeisti sandėlį  
11. Išplėskite dalį Atsargų dimensijos.
12. Lauke „Sandėlis“ įveskite „12“.
    * Sandėlis nustatytas į 12, nes jis yra išėmimo veiklos išeigos sandėlis.  
13. Lauke Vieta įveskite „12“.
    * Vieta nustatyta į 12, nes ji yra išėmimo veiklos išeigos vieta.  
14. Uždarykite puslapį.
15. Uždarykite puslapį.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Gamybos užsakymo įvertinimas ir sukurto „kanban“ peržiūra
1. Spustelėkite Įvertinti.
    * Įvertinus gamybos užsakymą bus suaktyvintas susijusio „kanban‟ kūrimas, kad būtų galima tiekti prekę M0001.  
2. Spustelėkite GERAI.
3. Uždarykite puslapį.
4. Uždarykite puslapį.
5. Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite sukurtą prekės M0001 įvykio „kanban“ taisyklę.  
7. Išplėskite skyrių „Kanbans“.
8. Sąraše pažymėkite pasirinktą eilutę.
    * Atkreipkite dėmesį į „kanban‟, sukurtą, kad būtų galima tiekti M0001 įvertintam gamybos užsakymui.  
    * Tai paskutinis veiksmas!  


