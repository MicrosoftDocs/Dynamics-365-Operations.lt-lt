---
title: Fiktyvios prekės
description: Šiame straipsnyje aprašoma, kaip naudojant KS eilutes ir formulę galima naudotiphantom eilutės tipą Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 64139873216decd8ecb2fcaf1f284e726c53c332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893329"
---
# <a name="phantom-items"></a>Fiktyvios prekės

[!include [banner](../includes/banner.md)]

Šiame straipsnyje išsamiai aprašoma, kaip KS ir formulės eilutėse gali būti naudojamas vienišos eilutės tipas.

1 pav. yra produkto H KS, o F ir G dalys– produktų H ir F dalies maršruto lapas.

![1 pav.: Inžinerinė KS.](media/product-H-part-F.png)
*1 pav.: Inžinerinė KS*

1 pav. rodo dviejų lygių KS struktūros pavyzdį. Užbaigtas produktas H atitinka mašinos rinkinio produktą. Mašinos rinkinys sudarytas iš dviejų dalių: elektros įrenginio (F), kuris turi dvi medžiagas (A ir B), ir pakavimo medžiagų grupės (G), kuri taip pat turi dvi medžiagas (C ir D). Kita medžiaga (E) naudojama atliekant bendrąjį mašinos surinkimą.

1 pav. rodo produkto H inžinerinę KS. Ši struktūra leidžia gerai peržiūrėti visos mašinos surinkimo dalis ir komponentus. Tačiau, nors produkto kūrėjams toks KS atvaizdavimas gali pasirodyti priimtinesnis, kuriant šią struktūrą gali būti nepakankamai atsižvelgta į tai, kaip mašina stovi ant parduotuvės grindų.

Pavyzdžiui, gamybos KS 1 paveikslėlyje nurodo, kad elektros vienetas F surenkamas kaip atskira dalis atskirame darbo užsakyme. Tačiau renkant elektrinį įrenginį ant parduotuvės grindų gali būti tikslingiau jį surinkti kaip bendro mašinos rinkinio dalį, ne kaip atskirą darbo užsakymą.

Šioje inžinerinėje KS taip pat vaizduojama, kad G dalis yra atskira dalis. Tačiau šioje struktūroje G dalis yra ne fizinė dalis, o pakavimo medžiagų rinkinys.

Todėl, nors inžinerinė KS yra itin naudinga kuriant produktą ir jį plėtojant, tai gali būti ne pats logiškiausias būdas produkto gamybos vykdymo procesui palaikyti. Priešingai, gamybos KS yra geriausias būdas sukurti produktą.

2 pav. rodo, kaip ankstesnė inžinerijos KS pereiti į gamybos KS. 2 pav. yra produkto H KS, o b – produkto H maršruto lapas.

![2 pav.: gamybos KS.](media/product-H-part-B.png)
*2 pav.: gamybos KS*

Šioje struktūroje galite matyti, kad visiškai neliko F ir G dalių, o medžiagos, iš kurių šios dalys sudarytos, perkeltos į kitą KS lygį.

Priešingai negu inžinerinėje KS, kurioje buvo du operacijų lapai, gamybos KS yra tik vienas operacijų lapas. Su G dalimi susieta pakuotės operacija taip pat perkelta ir dabar yra produkto H operacijų lapo dalis. Elektros įrenginio surinkimas yra pirmoji operacija. Ši tvarka racionali, nes šis įrenginys naudojamas kitoje operacijoje, kuri yra mašinos surinkimas. Paskutinė operacija yra pakavimo operacija, kurią atliekant naudojamos dvi pakavimo medžiagos (C ir D).

Perėjimą nuo inžinerinės KS prie gamybos KS galima atlikti naudojant fiktyvios KS eilutės tipą. Kaip galima spręsti iš termino „fiktyvi“ reikšmės, pereinant nuo vieno KS tipo prie kito, F ir G dalių neliko. Šiame pavyzdyje fiktyvios eilutės tipas taikomas inžinerinės KS F ir G dalių KS eilutėms. Sukūrus gamybos arba paketo užsakymą inžinerinė KS nukopijuojama į gamybos arba paketo užsakymą. Tada, kai užsakymas įvertintas, įvyksta perėjimas iš inžinerijos KS į gamybos KS, kaip parodyta 2 pav. Iš 2 pav. operacijų lapo į operaciją įvedamos pakavimo medžiagos C ir D.

## <a name="multilevel-phantom-bom-structures"></a>Kelių lygių fiktyvios KS struktūros

Phantom eilutės tipas gali būti naudojamas kelių lygių KS struktūrose, kaip parodyta 3 pav. 3 pav. yra G produkto KS, o (b) yra E ir F dalių ir produkto G maršruto lapas.

![3 pav.: inžinerijos KS dalis G.](media/product-G.png)
*3 pav.: gamybos KS dalis G*

4 pav. rodo gautą gamybos KS ir maršruto lapą, jei KS eilutės E ir F dalims sukonfigūruotos taip, kad eilutės tipas būtų fiktyvus. 4 pav. yra G produkto KS, o (b) yra produkto G maršruto lapas.

![4 pav.: gamybos KS dalis G.](media/product-G-route-sheet-G.png)
*4 pav.: gamybos KS dalis G*

## <a name="phantom-and-route-network"></a>Fiktyvus elementas ir maršruto tinklas

Fiktyvi KS taip pat gali būti naudojama maršruto tinklą turinčiai KS. Maršruto tinkle viena ar kelios operacijos vykdomos lygiagrečiai. 5 pav. rodo maršruto tinklo, kuris naudojamas kelių lygių KS, pavyzdį. 5 pav. (a) yra produkto G ir F dalies KS, (b) yra produkto G maršruto lapas ir F dalis, kuri turi maršruto tinklą.

![5 pav.: inžinerijos KS dalis G, maršruto tinklas.](media/product-G-part-F.png)
*5 pav.: inžinerijos KS dalis G, maršruto tinklas*

6 pav. yra produkto G ir F dalies KS, o (b) yra produkto G ir F dalies maršruto lapas.

![6 pav.: gamybos KS dalis G, maršruto tinklas.](media/product-G-part-F-with-route-sheet.png)
*6 pav.: gamybos KS dalis G, maršruto tinklas*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]