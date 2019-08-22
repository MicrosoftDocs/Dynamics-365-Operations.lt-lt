---
title: Apibrėžkite išteklių galimybės
description: Išteklių pajėgumai apibūdina, ką gali atlikti operacijų ištekliai.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ee6bfd06d7a38418812c2663695ab31701ef1ab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843678"
---
# <a name="define-resource-capabilities"></a>Apibrėžkite išteklių galimybės

[!include [task guide banner](../../includes/task-guide-banner.md)]

Išteklių pajėgumai apibūdina, ką gali atlikti operacijų ištekliai. Planuojant, kiekvienos užduoties ir operacijos reikalavimai lyginami su turimų išteklių pajėgumais. Šis užduočių vadovas jums padės sukurti išteklių pajėgumą ir jį priskirti ištekliui. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-a-resource-capability"></a>Kurti ištekliaus pajėgumą
1. Eikite į Išteklių pajėgumai.
2. Spustelėkite Naujas.
3. Lauke Pajėgumas surinkite ištekliaus pajėgumo ID.
    * Atliekant konkrečią operaciją, naudojamas pajėgumų ID, siekiant nurodyti, kad ištekliai turi šių pajėgumų operacijai atlikti.  
4. Lauke Aprašas įveskite pajėgumo aprašą.

## <a name="assign-capability-to-a-resource"></a>Priskirti pajėgumą ištekliui
1. Spustelėkite Pridėti.
2. Lauke Išteklius surinkite ištekliaus ID.
    * Išteklių pajėgumus galima priskirti vienam ar keliems ištekliams.  
3. Lauke Galiojimo pabaiga įveskite datą.
    * Šį lauką galite naudoti norėdami nurodyti, kad pajėgumų išteklius turi tik ribotą laiką.  
4. Lauke Prioritetas įveskite skaičių.
    * Kai planuojate užduotis ir operacijas, galite nurodyti, ar išteklius pasirinkti pagal prioritetą. Jei pasirenkate daryti taip, ir užduotį arba operaciją iki pageidaujamos datos gali atlikti daugiau nei vienas išteklius, pasirenkamas išteklius, kurio prioritetas reikiamų pajėgumų atžvilgiu yra žemiausias.  
5. Lauke Lygis įveskite skaičių.
    * Kai nurodote, kad užduočiai arba operacijai atlikti reikia konkrečių pajėgumų, taip pat galite nurodyti minimalų reikiamą lygį. Pajėgumų lygį naudokite norėdami diferencijuoti išteklius, kurie gali atlikti tą pačią užduotį, tik skirtingu greičiu, pajėgumu, mastu ir t. t.  

