---
title: Fiktyvios prekės
description: Šioje temoje išsamiai aprašoma, kaip eilutės tipą Fiktyvi galima naudoti komplektavimo specifikacijos (KS) ir formulės eilutėms programoje „Dynamics 365 Supply Chain Management“.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 02c4994fe6df192937f92f0167a3127ff2a8a588
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966334"
---
# <a name="phantom-items"></a>Fiktyvios prekės

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, išsamiai, kaip eilutės tipą Fiktyvi galima naudoti komplektavimo specifikacijos (KS) ir formulės eilutėms. Toliau pateiktoje iliustracijoje (a) yra produkto H (F ir G dalių) KS, o (b) yra produkto H (F dalies) maršruto lapas.

![Produktas H, F dalis](media/product-H-part-F.png)


Šioje iliustracijoje rodomas dviejų lygių KS struktūros pavyzdys. Užbaigtas produktas H atitinka mašinos rinkinio produktą. Mašinos rinkinys sudarytas iš dviejų dalių: elektros įrenginio (F), kuris turi dvi medžiagas (A ir B), ir pakavimo medžiagų grupės (G), kuri taip pat turi dvi medžiagas (C ir D). Kita medžiaga (E) naudojama atliekant bendrąjį mašinos surinkimą.

![Produktas H, F dalis](media/product-H-part-B.png)

Pirmesnėje iliustracijoje vaizduojama produkto H inžinerinė KS. Ši struktūra suteikia galimybę peržiūrėti viso mašinos rinkinio dalis ir komponentus. Tačiau, nors produkto kūrėjams toks KS atvaizdavimas gali pasirodyti priimtinesnis, kuriant šią struktūrą gali būti nepakankamai atsižvelgta į tai, kaip mašina stovi ant parduotuvės grindų. 

Pavyzdžiui, pirmesnėje iliustracijoje vaizduojamoje inžinerinėje KS matoma, kad elektrinis įrenginys F surinktas kaip atskira dalis atskirame darbo užsakyme. Tačiau renkant elektrinį įrenginį ant parduotuvės grindų gali būti tikslingiau jį surinkti kaip bendro mašinos rinkinio dalį, ne kaip atskirą darbo užsakymą.

Šioje inžinerinėje KS taip pat vaizduojama, kad G dalis yra atskira dalis. Tačiau šioje struktūroje G dalis yra ne fizinė dals, o pakavimo medžiagų rinkinys. 

Todėl, nors inžinerinė KS yra itin naudinga kuriant produktą ir jį plėtojant, tai gali būti ne pats logiškiausias būdas produkto gamybos vykdymo procesui palaikyti. Priešingai, gamybos KS yra geriausias būdas sukurti produktą.

Toliau pateiktoje iliustracijoje vaizduojama, kaip inžinerinė KS perkeliama į gamybos KS. Šioje iliustracijoje (a) yra produkto H KS, o b yra produkto H maršruto lapas.

Šioje struktūroje galite matyti, kad visiškai neliko F ir G dalių, o medžiagos, iš kurių šios dalys sudarytos, perkeltos į kitą KS lygį. 

Priešingai negu inžinerinėje KS, kurioje buvo du operacijų lapai, gamybos KS yra tik vienas operacijų lapas. Su G dalimi susieta pakuotės operacija taip pat perkelta ir dabar yra produkto H operacijų lapo dalis. Elektros įrenginio surinkimas yra pirmoji operacija. Ši tvarka racionali, nes šis įrenginys naudojamas kitoje operacijoje, kuri yra mašinos surinkimas. Paskutinė operacija yra pakavimo operacija, kurią atliekant naudojamos dvi pakavimo medžiagos (C ir D).

Perėjimą nuo inžinerinės KS prie gamybos KS galima atlikti naudojant fiktyvios KS eilutės tipą. Kaip galima spręsti iš termino „fiktyvi“ reikšmės, pereinant nuo vieno KS tipo prie kito, F ir G dalių neliko. Šiame pavyzdyje fiktyvios eilutės tipas taikomas inžinerinės KS F ir G dalių KS eilutėms. Sukūrus gamybos arba paketo užsakymą inžinerinė KS nukopijuojama į gamybos arba paketo užsakymą. Tada, kai nustatoma apytikslė užsakymo vertė, įvyksta perėjimas iš inžinerinės KS į gamybos KS, kaip pavaizduota pirmesnėse iliustracijose. Antroje iliustracijoje vaizduojamame operacijų lape pakavimo medžiagos C ir D yra operacijos įvestis. 

## <a name="multilevel-phantom-bom-structures"></a>Kelių lygių fiktyvios KS struktūros
Fiktyvios eilutės tipą galima naudoti kelių lygių KS struktūrose, kaip vaizduojama toliau pateiktoje iliustracijoje. Šioje iliustracijoje (a) yra produkto G KS, o (b) yra E ir F dalių ir produkto G maršruto lapas. 

![Produktas G, F dalis su maršruto lapais](media/product-G-route-sheet-G.png)


Toliau pateiktoje iliustracijoje vaizduojama gamybos KS ir maršruto lapas, jei E ir F dalių KS eilutės sukonfigūruotos taip, kad eilutės tipas yra Fiktyvi. Šioje iliustracijoje (a) yra produkto G KS, o (b) yra produkto G maršruto lapas.

![Produktas G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Fiktyvus elementas ir maršruto tinklas
Fiktyvi KS taip pat gali būti naudojama maršruto tinklą turinčiai KS. Maršruto tinkle viena ar kelios operacijos vykdomos lygiagrečiai. Toliau pateiktoje iliustracijoje vaizduojamas kelių lygių KS naudojamo maršruto tinklo pavyzdys. Šioje iliustracijoje (a) yra produkto G ir F dalies KS, o (b) yra produkto G ir F dalies, kurioje yra maršruto tinklas, maršruto lapas.

![Produktas G, F dalis](media/product-G-part-F.png)


Toliau pateiktoje iliustracijoje (a) yra produkto G ir F dalies KS, o (b) yra produkto G ir F dalies maršruto lapas.

![Produktas G, F dalis su maršruto lapais](media/product-G-part-F-with-route-sheet.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]