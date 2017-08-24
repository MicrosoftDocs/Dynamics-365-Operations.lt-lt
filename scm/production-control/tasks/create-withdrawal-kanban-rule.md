--- 
title: "Kurti išėmimo „kanban“ taisyklę"
description: "Šioje procedūroje parodyta, ką ir kaip reikia nustatyti, norint sukurti medžiagos perkėlimo „lean‟ aplinkoje išėmimo „kanban“ taisyklę."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c3172f5c932b94b2a9e442286eb61159286297fb
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a>Kurti išėmimo „kanban“ taisyklę

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodyta, ką ir kaip reikia nustatyti, norint sukurti medžiagos perkėlimo „lean‟ aplinkoje išėmimo „kanban“ taisyklę. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia naujos arba pakeistos medžiagos papildymą.


## <a name="create-new-kanban-rule"></a>Naujos „kanban“ taisyklės kūrimas
1. Eikite į „Kanban“ taisyklės.
2. Spustelėkite Naujas.
3. Lauke Tipas pasirinkite Išėmimas.
    * „Kanban‟ taisyklių tipas Išėmimas naudojamas perkelti medžiagai ar prekėms.  
4. Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.
    * Pasirinkite ReplenishSpeakerComponents.   Ši veikla nustatyta perkelti komponentus iš 11-ojo sandėlio, 11-osios vietos į 12-ąjį sandėlį ir 12-ąją vietą.  
5. Lauke Produktas įveskite arba pasirinkite reikšmę.
    * Pažymėkite M0007.  
6. Lauke Gamybos laikas įveskite skaičių.
    * Pavyzdžiui, 60.  
7. Lauke Matavimo vienetas įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, Minutės.  

## <a name="set-quantities-for-kanban"></a>„Kanban‟ kiekių nustatymas
1. Nustatykite pasirinkties Numatytasis kiekis reikšmę „5“.
    * Tai kiekis, kuris bus perduotas kiekvienam „kanban“.  
2. Lauke Fiksuotas „kanban“ kiekis įveskite 2.
    * Tai yra „kanbans“, kurie turi būti aktyvūs, suma. Šiuo atveju 2 „kanban“ signalai, iš kurių kiekvienas perkelia 5.  
3. Lauke Žemiausia įspėjimo riba įveskite „1“.
    * Naudojama norint sekti minimalią visų paskirties vietoje turinčių būti „kanbans“ sumą. Pavyzdžiui, tai naudojama „kanban“ kiekio apžvalgoje.  
4. Lauke Aukščiausia įspėjimo riba įveskite „2“.
    * Naudojama norint sekti maksimalią visų paskirties vietoje turinčių būti „kanbans“ sumą. Pavyzdžiui, tai naudojama „kanban“ kiekio apžvalgoje.  

## <a name="create-kanbans"></a>Kurti „kanban“
1. Spustelėkite Įrašyti.
    * Tam, kad būtų galima kurti „kanbans“, turi būti įrašyta „kanban“ taisyklė.  
2. Spustelėkite Pridėti.
    * Atkreipkite dėmesį, kad nėra jokių aktyvių „kanban“ signalų, nes siūlomas Naujų „kanban“ signalų skaičius yra 2, lygus fiksuotam „kanban“ kiekiui.  
3. Spustelėkite Kurti.
    * Taip sukursite du „kanban“ signalus.  
    * Atkreipkite dėmesį, kad 2 „kanban“ signalai, kiekvienas po 5, buvo sukurti šiai išėmimo „kanban“ taisyklei.  Tai yra paskutinis šios procedūros veiksmas.  

