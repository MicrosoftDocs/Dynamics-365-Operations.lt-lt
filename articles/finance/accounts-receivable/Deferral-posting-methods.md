---
title: Atidėjimų registravimo metodai
description: Šiame straipsnyje aprašomi skirtumai tarp atidėjimo registravimo metodų įplaukoms ir išlaidų atidėjimams abonemento sąskaitose pateikiamose sąskaitose.
author: JodiChristiansen
ms.date: 6/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: c66ed1c38251140dd798c39797873ceb5f7121a4
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017477"
---
# <a name="deferral-posting-methods"></a>Atidėjimų registravimo metodai

Šiame straipsnyje aprašomi skirtumai tarp atidėjimo registravimo metodų įplaukoms ir išlaidų atidėjimams abonemento sąskaitose pateikiamose sąskaitose.

Puslapyje Įplaukų **ir išlaidų atidėjimo parametrai** atidėjimo registravimo metodų pasirinktys yra Balansas **ir Pelnas** **ir nuostolis**. Šiame straipsnyje pateiktas pavyzdys padės paaiškinti skirtumus tarp šių dviejų metodų ir priežastis, dėl kurių galite naudoti vieną ar kitą metodą.

**Balanso metodas** naudoja tik dvi sąskaitas. Todėl įtrauktas mažesnis nustatymas. Pelno **ir nuostolio metodas** turi dvi papildomas sąskaitas– **·** **Pradinio** pripažinimo ir Pripažinimo korespondentinę sąskaitą, įplaukoms, nuolaidoms ir išlaidoms, atsižvelgiant į operacijos tipą. Šios sąskaitos yra nustatytos atidėjimų numatytųjų nustatymų puslapyje (Abonemento **įplaukų** ir išlaidų atidėjimų nustatymas **\>).\>** Nors pavyzdys skirtas atidėtoms įplaukoms, ta pati sąvoka gali būti taikoma ir atidėtoms nuolaidoms, ir atidėtoms išlaidoms.

## <a name="example"></a>Pavyzdys

1 pardavimo SF bendra suma yra $3,000, ji turi atidėtų įplaukų. Toliau pateikiamose lentelėse rodomi paskirstymai, kai užregistruojama ši pardavimo SF.

**Balanso metodas**

| Tipas | Sąskaita | Debetas | Kreditas|
|---|---|---|---|
| Debetas | Gautinos sumos | 3,000.00 | |
| Kreditas | Atidėtos įplaukos | | 3,000.00 |

**Pelno ir nuostolio metodas**

| Tipas | Sąskaita | Debetas | Kreditas |
|---|---|---|---|
| Debetas | Gautinos sumos | 3,000.00 | |
| Debetas | Įplaukų pripažinimo korespondentinė sąskaita | 3,000.00 | |
| Kreditas | Atidėtos įplaukos | | 3,000.00 |
| Kreditas | Pradinis įplaukų pripažinimas | | 3,000.00 |

2 pardavimo SF suma yra $2,000, todėl ji neturi atidėtų įplaukų.

| Tipas | Sąskaita | Suma |
|---|---|---|
| Debetas | Gautinos sumos | 3,000.00 |
| Kreditas | Įplaukos | 3,000.00 |

**Balanso metodo bendrosios sumos, 1 ir 2 pardavimo SF sujungtos**

| Sąskaita | Debetas | Kreditas |
|---|---|---|
| Gautinos sumos | 5,000.00 | |
| Įplaukos | | 2 000,00 |
| Atidėtos įplaukos | | 3,000.00 |

**Naudojant balanso** metodą, balanso įplaukos nesudėtingos. Kai kurios įplaukos registruojamos atidėtų įplaukų **sąskaitoje**. Atkreipkite dėmesį, kad, kaip įplaukos pripažįstamos kiekvieną laikotarpį, atidėtų įplaukų sąskaitoje yra keletas debetų **ir kreditų**. Bruto įplaukos per tam tikrą laikotarpį bus sumaišytos su įplaukų pripažinimo ins / out.

**Sujungtos pardavimo SF 1 ir 2 pelno ir nuostolio metodo bendrosios sumos**

| Sąskaita | Debetas | Kreditas |
|---|---|---|
| Gautinos sumos | 5,000.00 | |
| Įplaukos | | 5,000.00 |
| Įplaukų korespondentinė sąskaita | 3,000.00 | |
| Atidėtos įplaukos | | 3,000.00 |

Visos įplaukos eina į pelno ir nuostolio įplaukų **sąskaitą**. Tada atidėtos įplaukos perkeliamos iš pelno ir nuostolio išrašo į balansą. Galite lengvai matyti bendras įplaukas, nes viskas užregistruota Įplaukų **sąskaitoje**. Tačiau kai kurios iš šių bendrųjų įplaukų atidėtos. Todėl jis perkeliamas į atidėtų įplaukų sąskaitą **ir** atpažįstamas vėliau.

Pelno ir **nuostolio** metodo metu galite peržiūrėti įplaukų ir įplaukų korespondentinę sąskaitą, **·** **kad** pamatytumėte $5,000 įplaukų ir grynųjų įplaukų (atidėtų) $2,000. Nors pelno **ir nuostolio** metodas gali palengvinti ataskaitų rengimo procesą, yra daugiau sąskaitų, kurios turi būti nustatytos.
