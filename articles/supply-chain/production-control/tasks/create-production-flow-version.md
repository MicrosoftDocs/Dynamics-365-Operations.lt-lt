---
title: Kurti gamybos eigos versiją
description: Šioje procedūroje dėmesys skiriamas naujos gamybos eigos versijos kūrimui.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b72d6162edd0ae6ccbfdcfe3e63ecff30528454
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569265"
---
# <a name="create-a-production-flow-version"></a>Kurti gamybos eigos versiją

[!include [banner](../../includes/banner.md)]

Šioje procedūroje dėmesys skiriamas naujos gamybos eigos versijos kūrimui. Šiai procedūrai turi būti nurodyti „lean manufacturing“ parametrai ir klasės laiko matavimo vienetai. Taip pat būtina nurodyti vertės srautą ir gamybos grupę. Norėdami sužinoti daugiau apie gamybos eigas ir „lean manufacturing“ veiklas, žr. „Microsoft Dynamics AX“ „Lean Manufacturing“ techninę dokumentaciją. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="create-a-production-flow"></a>Gamybos eigos kūrimas
1. Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite vertės srauto tipo valdymo vienetą. Vertės srautas yra valdymo vienetas, kuris apima visas veiklas ir vertės srauto srautus. Šiame etape valdymo vienetai yra tik juridinis subjektas ir jiems nepriskirta jokia kita funkcija.  
7. Lauke Gamybos grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite gamybos eigos gamybos grupę. Gamybos grupės leidžia apibrėžti gamybos proceso medžiagą, darbą ir NG sąskaitas. Norint susieti apskaitos kontekstą su gamybos eiga, reikia pasirinkti gamybos grupę.  
9. Spustelėkite Įrašyti.

## <a name="create-a-production-flow-version"></a>Kurti gamybos eigos versiją
1. Spustelėkite Pridėti.
2. Lauke Galiojimo data įveskite datą ir laiką.
    * Jei reikia, nurodykite versijos galiojimo datą. Galite atnaujinti ją bet kuriuo metu, net ir aktyvioms versijoms. Galite naudoti ją planuodami palaipsniui pašalinti versiją.  
3. Spustelėkite GERAI.
4. Sąraše pažymėkite pasirinktą eilutę.
5. Lauke „Vienetas“ įveskite reikšmę.
6. Nustačius keičiasi vienetas.
7. Lauke Vidutinis vieneto gamybos laikas įveskite skaičių.
    * Nurodykite vidutinį versijos vieneto gamybos laiką. Nurodykite gamybos eigos versijos vieneto gamybos kontrolės numatomą vidutinį vieneto gamybos laiką. Vieneto gamybos laikas yra apibrėžiamas kaip kiekis per laikotarpį. Pateiktame pavyzdyje vieneto gamybos laikas yra 10 vienetų per 0,2 valandos. Kai darbo laikas yra 8 valandos, našumo pajėgumas yra 400 vienetų per dieną.  
8. Lauke Ciklo kiekis įveskite skaičių.
    * Nurodykite kiekį per ciklą, susijusį su vidutiniu vieneto gamybos laiku.  
9. Perjunkite skyriaus Versijos informacija išplėtimą.
10. Lauke Trumpiausias vieneto gamybos laikas įveskite skaičių.
    * Nurodykite trumpiausią vieneto gamybos laiką. Trumpiausias vieneto gamybos laikas turi būti trumpesnis negu vidutinis vieneto gamybos laikas arba jam lygus.  
11. Lauke Ilgiausias vieneto gamybos laikas įveskite skaičių.
    * Ilgiausias vieneto gamybos laikas turi būti ilgesnis negu vidutinis vieneto gamybos laikas arba jam lygus.  
12. Dalyje Faktinio ciklo laiko laikotarpis (dienomis) įveskite skaičių.
    * Dalyje Faktinio ciklo laiko laikotarpis įveskite dienų skaičių. Faktinio ciklo laiko laikotarpis yra dienų skaičius, per kurias sujungiamos užduotys nuo faktinės minutės atgal, kad būtų galima apskaičiuoti faktinį ciklo laiką. Reikšmę galima pakeisti bet kuriuo metu ir ji naudojama tik skaičiuojant faktinius ciklo laikus.  
13. Spustelėkite Įrašyti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]