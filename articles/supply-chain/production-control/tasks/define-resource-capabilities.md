---
title: Apibrėžkite išteklių galimybės
description: Išteklių pajėgumai apibūdina, ką gali atlikti operacijų ištekliai.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42451da0bd465ce3a18ecf18570f3331847474c1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579117"
---
# <a name="define-resource-capabilities"></a>Apibrėžkite išteklių galimybės

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]