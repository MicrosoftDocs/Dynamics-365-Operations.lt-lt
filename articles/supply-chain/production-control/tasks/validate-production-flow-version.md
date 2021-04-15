---
title: Patikrinti gamybos eigą ir versiją
description: Ši procedūra nurodo, kaip sukurti naują gamybos eigą ir pirmąją „lean manufacturing“ versiją.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b46e3983cc95062e1c2073bb649f60df64807b99
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810988"
---
# <a name="validate-a-production-flow-and-version"></a>Patikrinti gamybos eigą ir versiją

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip sukurti naują gamybos eigą ir pirmąją „lean manufacturing“ versiją. Būtinos sąlygos: turi būti nurodyti „lean manufacturing“ parametrai ir klasės laiko matavimo vienetai. Būtina nurodyti vertės srautą ir gamybos grupę. Žr. „Lean manufacturing“ techninę dokumentaciją, kad susipažintumėte su gamybos eigos koncepcijomis ir veiklomis. Ši procedūra taikoma juridiniams subjektui USMF ir demonstraciniams duomenims. Tačiau jeigu juridinis subjektas sukonfigūruotas „Lean manufacturing“, gali būti naudojami kiti juridiniai subjektai.


## <a name="create-a-production-flow"></a>Gamybos eigos kūrimas
1. Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Vertės srautas yra valdymo vienetas, kuris apima visas veiklas ir vertės srauto eigas.   Šiame etape valdymo vienetai yra tik juridinis subjektas ir jiems nepriskirta jokia kita funkcija.  
7. Lauke Gamybos grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Gamybos grupės leidžia apibrėžti gamybos proceso medžiagą, darbą ir NG sąskaitas. Norint susieti apskaitos kontekstą su gamybos eiga, reikia pasirinkti gamybos grupę.  
9. Spustelėkite Įrašyti.

## <a name="create-a-production-flow-version"></a>Kurti gamybos eigos versiją
1. Spustelėkite Pridėti.
2. Lauke Galiojimo data įveskite datą ir laiką.
    * Galite atnaujinti versijos galiojimo datą bet kuriuo metu, net ir aktyvioms versijoms. Naudokite versijos galiojimo datą planuodami palaipsniui ją pašalinti.  
3. Spustelėkite GERAI.
4. Sąraše pažymėkite pasirinktą eilutę.
5. Lauke „Vienetas“ įveskite reikšmę.
6. Pasirinkite Vieneto gamybos laiko vienetas.
7. Lauke Vidutinis vieneto gamybos laikas įveskite skaičių.
    * Nurodykite gamybos eigos versijos vieneto gamybos kontrolės numatomą vidutinį vieneto gamybos laiką.   Vieneto gamybos laikas yra apibrėžiamas kaip kiekis per laikotarpį.  Pateiktame pavyzdyje vieneto gamybos laikas yra 10 vienetų per 0,2 valandos. Kai darbo laikas yra 8 valandos, našumo pajėgumas yra 400 vienetų per dieną.  
8. Lauke Ciklo kiekis įveskite skaičių.
9. Išplėskite arba sutraukite skyrių Versijos informacija.
10. Lauke Trumpiausias vieneto gamybos laikas įveskite skaičių.
    * Trumpiausias vieneto gamybos laikas turi būti trumpesnis negu vidutinis vieneto gamybos laikas arba jam lygus.  
11. Lauke Ilgiausias vieneto gamybos laikas įveskite skaičių.
    * Ilgiausias vieneto gamybos laikas turi būti ilgesnis negu vidutinis vieneto gamybos laikas arba jam lygus.  
12. Dalyje Faktinio ciklo laiko laikotarpis įveskite dienų skaičių.
    * Faktinio ciklo laiko laikotarpis yra dienų skaičius, per kurias sujungiamos užduotys nuo faktinės minutės atgal, kad būtų galima apskaičiuoti faktinį ciklo laiką. Reikšmę galima pakeisti bet kuriuo metu ir ji naudojama tik skaičiuojant faktinius ciklo laikus.  
13. Spustelėkite Įrašyti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]