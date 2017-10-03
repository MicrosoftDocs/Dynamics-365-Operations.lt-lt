--- 
title: "Kurti pakeitimo „kanban“ taisyklę"
description: "Šioje procedūroje parodoma, kaip konkrečią datą esamą „kanban“ taisyklę pakeisti nauja „kanban“ taisykle."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 58b12edbbdcf77429c32193dfd850bc53f4c26a8
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-replacement-kanban-rule"></a>Kurti pakeitimo „kanban“ taisyklę

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip konkrečią datą esamą „kanban“ taisyklę pakeisti nauja „kanban“ taisykle. Tai naudinga, kai reikia koordinuoti ir planuoti gamybos eigos ar papildymo taisyklių pakeitimus. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta proceso inžinieriui arba vertės srauto vadybininkui, kai jie parengia pakeistos gamybos eigos arba naujos papildymo taisyklės gamybą. Atliekant šią užduotį, „kanban“ taisyklė 000022 pakeičiama nauja taisykle ir naujosios taisyklės kiekis nuo 48 padidinamas iki 100.


## <a name="select-a-kanban-rule-to-replace"></a>Keistinos „kanban“ taisyklės pasirinkimas
1. Eikite į „Kanban“ taisyklės.
2. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite „kanban“ taisyklę 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Kurti pakeitimo „kanban“ taisyklę
1. Spustelėkite Pakeisti „kanban“ taisyklę.
2. Lauke Įsigaliojimo data įveskite datą ir laiką.
    * Pasirinkite datą ateityje, pvz., viena savaitė nuo dabar. Tai yra data ir laikas, kada naujoji „kanban“ taisyklė tampa aktyvi ir pakeičia senąją „kanban“ taisyklę.  
    * Jei „kanban“ taisyklė pakeičią kelią gamybos eigoje, galima pasirinkti kitą veiklą.  Atlikdami šią procedūrą, veiklos nekeisime.  
3. Spustelėkite GERAI.
    * Atkreipkite dėmesį, kad sukuriama nauja „kanban“ taisyklė, kuri pakeičia „kanban“ taisyklę 000022.  
    * Galiojimo data nustatoma pagal datą, pasirinktą pakeičiant „kanban“ taisyklę.  
4. Sąraše raskite ir pasirinkite norimą įrašą.
    * Pasirinkite pakeistą „kanban“ taisyklę 000022.  
    * Atkreipkite dėmesį, kad pakeistos „kanban“ taisyklės data yra tokia pati, kaip Galiojimo data, nes ji yra galiojimo pabaigos data.  
5. Sąraše pasirinkite 1 eilutę.
    * Sąrašo viršuje pasirinkite naująją „kanban“ taisyklę. Tai yra „kanban“ taisyklė, kurios numeris didžiausias.  
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Spustelėkite „kanban“ taisyklės numerį, kad atidarytumėte „kanban“ taisyklę.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Senąją pakeičiančios „kanban“ taisyklės didžiausio kiekio modifikavimas
1. Didžiausias kiekis nustatykite į 100.
    * Išplėskite „FastTab‟ skirtuką Kiekiai, kad matytumėte lauką Didžiausias kiekis. Didžiausią kiekį pakeitus į 100, bus galima apdoroti iki 100 „kanban“.    Tai yra paskutinis šios užduoties veiksmas.  


