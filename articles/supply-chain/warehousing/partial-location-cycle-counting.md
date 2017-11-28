---
title: "Dalinis vietos ciklų skaičiavimas"
description: "Faktinės skaičiavimo operacijos valdomos pagal ciklo skaičiavimo planus. Galite reikalauti, kad būtų skaičiuojamos ne visos vietoje turimos atsargos, o tik konkretūs produktai ir produkto variantai."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0e0f9d81f4d5943a89d8ac87776e05acb32cb8d9
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="partial-location-cycle-counting"></a>Dalinis vietos ciklų skaičiavimas

[!include[banner](../includes/banner.md)]


Faktinės skaičiavimo operacijos valdomos pagal ciklo skaičiavimo planus. Galite reikalauti, kad būtų skaičiuojamos ne visos vietoje turimos atsargos, o tik konkretūs produktai ir produkto variantai.

Naudodami ciklo skaičiavimo planus skaičiavimo darbui sukurti, galite valdyti faktines skaičiavimo operacijas. Galite reikalauti, kad būtų skaičiuojamos ne visos vietoje turimos atsargos, o tik konkretūs produktai ir produkto variantai. Filtruodamas konkrečius produktus, sandėlio vadovas gali sumažinti peržiūros pridėtines išlaidas, išvengti konsolidavimo klaidų ir sutaupyti laiko.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Kaip konfigūruoti dalinį vietos ciklo skaičiavimą
Skaičiavimo operacijoms naudojant sandėlio darbo procesą, kiekvienai vietai sukuriama darbo antraštė. Kai nustatote ciklo skaičiavimo planą, galite naudoti užklausą **Pasirinkti vietas**, kad apribotumėte sukurtą ciklo skaičiavimo darbą. Kai pasirenkate ciklo skaičiavimo plano produktus, galite pasirinkti produkto ir produkto varianto užklausas, kad patikslintumėte, kas yra skaičiuojama. 

**Darbo šabloną** galite susieti su ciklo skaičiavimo planu, kad nurodytumėte, kaip turi būti sukurtas ciklo skaičiavimo darbas. Tiesioginė nuoroda į skaičiavimo operacijoms skirtą darbo šabloną pateikta ciklo skaičiavimo plane. 

Kai apibrėžiate darbo šablono informaciją, galite naudoti parinktį **Darbo eilučių lūžiai**, kad nurodytumėte, ar skaičiavimo darbo eilutės turi būti grupuojamos pagal prekės numerį ar produkto varianto numerį. Ši sąranka būtina, jei norite skaičiuoti tik vietoje turimas konkrečių produktų atsargas. Sukurtos ciklo skaičiavimo darbo eilutės turės čia nustatytą informacijos lygį, ir valdomos skaičiavimo operacijos bus vykdomos pagal šį lygį. 

Jei susiesite ciklo skaičiavimo planus su darbo šablonais naudodami parinktį **Darbo eilučių lūžiai**, sukurtam ciklo skaičiavimo darbui bus pasirinktas laukas **Dalinis ciklo skaičiavimas**, ir bus sukurtos kelios ciklo skaičiavimo darbo eilutės pagal darbo šablono aprašą. 

Prieš apdorojant dalinį ciklo skaičiavimo darbą, turite bent jau pasirinkti **Rodyti prekės numerį** mobiliojo įrenginio meniu elementui skaičiavimo sąrankos metu. Sandėlio operatorius bus paprašytas įrašyti tik skaičiavimo informaciją, susijusią su inventorizacijos eilutėmis (prekių numeriai ir produkto dimensijos). Šio skaičiavimo proceso metu visų kitų turimų atsargų bus nepaisoma. 

Dalinio ciklo skaičiavimo proceso atveju vietos **paskutinio ciklo skaičiavimo** data / laikas nebus atnaujinami.

## <a name="example"></a>Pavyzdys
Pavyzdžiui, 61 sandėlyje turi būti skaičiuojamas tik prekės numeris A0001.

1.  Sukuriamas naujas ciklo skaičiavimo darbo šablonas. Parinktis **Darbo eilučių lūžiai** naudojama skaičiavimo darbo eilutėms grupuoti pagal prekės numerį. Todėl sukurtas ciklo skaičiavimo darbas turės eilutes pagal prekės numerį. Eilutes taip pat galite grupuoti pagal produkto varianto numerį.
2.  Sukuriamas naujo ciklo skaičiavimo planas, kuriame pateikiama nuoroda į naujai sukurtą darbo šabloną. Ciklo skaičiavimo planas apima visas 61 sandėlyje esančias vietas (užklausa **Pasirinkti vietas**), kuriose yra atsargų pagal prekės numerį A0001. Konkrečių produktų pasirinkimas nurodytas skyriuje **Ciklo skaičiavimo produktų pasirinkimas**.
3.  Galite pasirinkti ciklo skaičiavimo planų produktus, nustatydami lauką **Tuščios vietos** į **Neįtraukti tuščių**. Apdorojus ciklo skaičiavimo planą, sukuriamas dalinis ciklo skaičiavimo darbas prekės numeriui A0001. Faktinis skaičiavimo procesas gali būti atliekamas naudojant mobiliojo įrenginio meniu elementą, skirtą valdomam ciklo skaičiavimui.



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Ciklų skaičiavimas](cycle-counting.md)


