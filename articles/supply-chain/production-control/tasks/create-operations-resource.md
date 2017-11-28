--- 
title: "Kurti operacijų išteklių"
description: "Operacijų išteklius atlieka projekto arba gamybos proceso veiklas."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aa80e4b22d116c8f580c9aefe7c114cfe1d19cc8
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="create-an-operations-resource"></a>Kurti operacijų išteklių

[!include[task guide banner](../../includes/task-guide-banner.md)]

Operacijų išteklius atlieka projekto arba gamybos proceso veiklas. Šioje procedūroje rodoma, kaip apibrėžti operacijų išteklių. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.

1. Eikite į Ištekliai.
2. Spustelėkite Naujas.
3. Lauke Išteklius surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.

## <a name="define-capacity-and-consumption-parameters"></a>Apibrėžti pajėgumų ir suvartojimo parametrus
1. Išplėskite skyrių Operacija.
2. Lauke Atliekų procentinė dalis įveskite skaičių.
3. Lauke Nustatymų kategorija įveskite arba pasirinkite reikšmę.
    * Nurodykite išlaidų kategoriją, kuri apibrėžia, kaip paaiškinti nustatymo išlaidas.  
4. Lauke Apdorojimo laiko kategorija įveskite arba pasirinkite reikšmę.
    * Nurodykite išlaidų kategoriją, kuri apibrėžia, kaip paaiškinti vykdymo laiko išlaidas.  
5. Lauke Kiekio kategorija įveskite arba pasirinkite reikšmę.
    * Nurodykite išlaidų kategoriją, kuri apibrėžia, kaip paaiškinti išteklių išlaidas pagal išeigos kiekį.  
6. Lauke Pajėgumo vienetas pasirinkite parinktį.
    * Nurodykite vienetą, kuriuo išreikšti operacijų ištekliaus pajėgumą.  
7. Lauke Pajėgumas įveskite skaičių.
8. Lauke Efektyvumo procentas įveskite skaičių.
    * Nurodykite efektyvumą, kurio tikitės iš operacijų ištekliaus. Efektyvumo procentas reguliuoja operacijų ištekliaus našumą ir veikia ištekliui rezervuotą laiką.  
9. Lauke Operacijų planavimo procentas įveskite skaičių.
    * Nurodykite maksimalų operacijos ištekliaus pajėgumo procentą, kurį norite naudoti planuodami operacijas.  
10. Lauke Ribotas pajėgumas pasirinkite Taip.
    * Jei operacijos išteklius turėtų būti planuojamas pagal faktinį turimą pajėgumą ir jei reikia atsižvelgti į esamų pajėgumų rezervavimus, šią parinktį nustatykite į Taip. Jei ši parinktis nustatyta į Ne, daroma prielaida, kad operacijos ištekliaus pajėgumas yra neribotas, ir šis išteklius gali būti perpildytas.  
11. Lauke Ribotosios spartos išteklius pasirinkite Taip.

## <a name="define-working-times"></a>Apibrėžti darbo laikus
1. Išplėskite skyrių Kalendoriai.
2. Spustelėkite Pridėti.
3. Lauke Kalendorius įveskite arba pasirinkite reikšmę.
    * Nurodykite darbo laiko kalendorių, apibrėžiantį ištekliaus pajėgumą (valandomis).  
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="define-resource-capabilities"></a>Apibrėžkite išteklių galimybės
1. Išplėskite dalį Pajėgumai.
2. Spustelėkite Pridėti.
    * Pajėgumas yra operacijų ištekliaus gebėjimas atlikti tam tikrą veiklą. Planavimo mechanizmas išteklius paskirsto derindamas kiekvienos veiklos išteklių poreikius ir turimų operacijų išteklių pajėgumus.  
3. Lauke Pajėgumas įveskite arba pasirinkite reikšmę.
4. Lauke Lygis įveskite skaičių.
    * Nurodykite įgudimo lygį, kuriuo išteklius apdoroja pajėgumą.  
5. Lauke Prioritetas įveskite skaičių.
    * Nurodykite operacijų ištekliaus prioritetą pajėgumo atžvilgiu. Planuojant pagal prioritetą, pirmiausia pasirenkamas operacijų išteklius, kurio prioritetas aukščiausias (mažiausia skaitinė reikšmė).  

## <a name="assign-resource-to-resource-group"></a>Priskirti išteklių išteklių grupei
1. Išplėskite dalį Išteklių grupės.
2. Spustelėkite Pridėti.
    * Išteklių grupė apibrėžia operacijų ištekliaus teritoriją, gamybos vienetą ir sandėlio kontekstą. Operacijų išteklių planuoti galima tik kai jis priskirtas išteklių grupei ir tik toje teritorijoje, kurioje išteklių grupė yra.  
3. Lauke Išteklių grupė įveskite arba pasirinkite reikšmę.
4. Lauke Įvesties vieta įveskite arba pasirinkite reikšmę.
    * Nurodykite sandėlio vietą, iš kurios operacijų išteklius vartoja medžiagas.  


