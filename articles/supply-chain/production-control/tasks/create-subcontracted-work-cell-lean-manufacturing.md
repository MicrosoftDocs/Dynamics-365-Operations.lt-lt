---
title: Kurti „lean manufacturing“ subrangovo darbo elementą
description: Norėdami modeliuoti subrangovo darbą „lean manufacturing“, turite sukurti darbo elementą, susietą su tiekėju, atliekančiu darbą.
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86838eb81f42b0f930f3989f7edfa5ee724bd05e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006896"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Kurti „lean manufacturing“ subrangovo darbo elementą

[!include [banner](../../includes/banner.md)]

Norėdami modeliuoti subrangovo darbą „lean manufacturing“, turite sukurti darbo elementą, susietą su tiekėju, atliekančiu darbą. Subrangovo darbo elementas yra susietas su tiekėju, susiejant tiekėjo tipo išteklių. Jei leidžiate šį įrašą naudodami USMF demonstracinę įmonę, galite pasirinkti tiekėjo kodo ID 1002 ir 1 svetainę.


## <a name="create-a-vendor-resource"></a>Sukurkite tiekėjo išteklių
1. Eikite į Ištekliai.
2. Spustelėkite Naujas.
3. Lauke Išteklius surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Tipas pasirinkite „Tiekėjas“.
6. Lauke „Tiekėjas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.

## <a name="create-the-resource-group"></a>Sukurkite išteklių grupę
1. Eikite į Išteklių grupės.
2. Spustelėkite Naujas.
3. Lauke Išteklių grupės surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkti svetainę, kuriai turi būti priskirtas darbo elementas. Teoriškai svetainė gali vaizduoti vieną svetainę, kurią valdo tiekėjas. Tačiau dauguma atvejų subrangos ištekliai yra tik paskirti svetainei, kuri užsako subrangos darbą. Atkreipkite dėmesį, kad subrangovo darbo elementų įvesties ir išvesties sandėliai turi būti toje pačioje svetainėje.  
6. Lauke Teritorija surinkite reikšmę.
7. @SysTaskRecorder:_RequestClose
8. Pažymėkite arba išvalykite žymės langelį „Darbo elementas“.
9. Lauke Įeigos sandėlis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
    * Pasirinkite sandėlį ir vietą, kurios naudojamos medžiagai organizuoti tiekėjo valdomam darbo elementui. Daugeliu atvejų sandėlis ir vieta modeliuojami naudojant atskirą kiekvieno tiekėjo sandėlį ir vieną vietą darbo elementui.  
10. Lauke Įeigos vieta spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
11. Lauke Išeigos sandėlis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
    * Apibrėžkite sandėlį ir vietą, kur medžiaga užregistruota užregistravus darbo elemento subrangos veiklą. Sandėlis ir vieta gali būti tiekėjo svetainėje, jei tiekėjas praneša apie „kanban“ užduotis. Taip pat sandėlis ir vieta gali būti gavimo vieta, susieta su kitu gamybos eigos veiksmu.  
12. Lauke Išeigos vieta spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
13. Išplėskite arba sutraukite skyrių Kalendoriai.
14. Spustelėkite Pridėti.
15. Lauke Kalendorius spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Susiekite darbo elemento darbo laiko kalendorių išteklių grupe. Kritiniams ištekliams rekomenduojame apibrėžti konkrečius kalendorius, nurodančius tikslų darbo laiką ir susijusius darbo elemento arba tiekėjo svetainės pajėgumus.  
16. Išplėskite arba sutraukite sekciją Ištekliai.
17. Spustelėkite Pridėti.
    * Subrangos išteklių grupė turi turėti susietą tiekėjo tipo išteklių, kuris susieja išteklių grupę su tiekėjo sąskaita.  
18. Lauke Ištekliai spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite arba įveskite tiekėjo strategiją, kurią sukūrėte ankstesnėje papildomoje užduotyje.  
19. Išplėskite arba sutraukite skyrių Darbo elemento pajėgumas.
20. Spustelėkite Pridėti.
    * Darbo elementas turi turėti apibrėžtą pajėgumą. Šiame pavyzdyje mes kuriame 100 vienetų per standartinę darbo dieną gamybos pajėgumą.  
21. Lauke Gamybos eigos modelis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
22. Lauke Pajėgumo laikotarpis pasirinkite pasirinktį.
23. Lauke Vidutinis našumo kiekis įveskite skaičių.
24. Lauke Vienetas spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
25. „ResolveChanges“ Vienetas.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]