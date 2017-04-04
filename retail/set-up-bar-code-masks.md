---
title: "Brūkšninių kodų skaičių sekų nustatymas"
description: "Šioje temoje aprašoma, kaip nustatyti brūkšninio kodo skaičių sekos simboliai, brūkšninių kodų skaičių sekos, ir kaip priskirti brūkšniniam kodui kaukes su brūkšniniais kodais."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fe598799d52cacd84da775ac7ace8cf9a30ae5fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-code-masks"></a>Brūkšninių kodų skaičių sekų nustatymas

Šioje temoje aprašoma, kaip nustatyti brūkšninio kodo skaičių sekos simboliai, brūkšninių kodų skaičių sekos, ir kaip priskirti brūkšniniam kodui kaukes su brūkšniniais kodais.

<a name="set-up-bar-code-mask-characters"></a>Brūkšninio kodo skaičių sekos simbolių nustatymas
-------------------------------

Brūkšninių kodų skaičių sekos yra naudojami sukurti brūkšninių kodų ir greitai identifikuoti brūkšninių kodų, kurie yra nuskaitomi į pardavimo (POS). Kaukės susideda iš simbolių, kurie veikia kaip vietos rezervavimo ženklus, kurie nurodo brūkšninių kodų, kurie bus sukurtas formatas. Norėdami sukonfigūruoti brūkšninio kodo skaičių, jums reikia sukurti brūkšninio kodo skaičių sekos simboliai. Eikite į **mažmeninės prekybos ir prekybos**&gt;**atsargų valdymo**&gt;**brūkšniniai kodai ir etiketės**&gt;**kaukė simbolius**. Spustelėkite **naujas** sukurti brūkšninio kodo skaičių sekos simboliai. Skaičių sekos simbolius galima sukurti nurodyti šiuos brūkšninio kodo duomenis.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Field**            | **Description**                                                                                                 |
| **Product**          | Vietos rezervavimo ženklo produkto ID.                                                                                     |
| **Any number**       | Naudojama norint nurodyti skaičių, kuris bus sunkiai koduojami brūkšninius kodus.                                                  |
| **Check digit**      | Nurodo, kad brūkšninio kodo brūkšninio kodo skaičių formatas naudoja kontrolinis skaitmuo patvirtinti brūkšninio kodo galiojimą. |
| **Size digit**       | Rodo dydžio sukurtas produktas variantas, kuris apima dydžio brūkšninį kodą.                                 |
| **Color digit**      | Nurodo spalvą sukurtas produktas variantas, kuris apima spalva brūkšninį kodą.                               |
| **Style digit**      | Rodo stilius sukurtas produktas variantas, kuris apima stilių brūkšninį kodą.                             |
| **EAN license code** | Vietos rezervavimo ženklo EAN licencijai išduoti EAN licencijos kodus.                                                       |
| **Kaina**            | Nurodo kainą, nes kaina įterpti brūkšninius kodus.                                                                   |
| **Quantity**         | Rodo kiekis kiekis/atsitiktinai svorio įterpti brūkšninius kodus.                                                |
| **Employee**         | Rodo brūkšninio kodo segmento darbuotojo ID numerio, brūkšninio kodo POS prisijungiant.                                  |
| **Customer**         | Nurodo kliento ID segmente.                                                                                  |
| **Duomenų įvedimas**       | *Dar neįdiegta.*                                                                                          |
| **Discount code**    | Nuolaida kodas brūkšniniam kodui, kad buvo įtraukti su nuolaida – į pardavimo sandoris             |
| **Dovanų kortelė**        | Rodo dovanų kortelės numerį, kai išduodant arba mokėjimo ir dovanų kortelės.                                               |
| **Loyalty card**     | Prideda lojalų klientą į operaciją, ir gali būti naudojamas, kai mokėjimas lojalumo.                             |

## <a name="define-bar-code-masks"></a>Apibrėžti brūkšninių kodų skaičių sekos
Po to, kai brūkšninio kodo skaičių sekos simboliai yra nurodyta reikia brūkšninių kodų skaičių sekos, eikite į **mažmeninės prekybos ir komercijos**&gt;**atsargų valdymo**&gt;**brūkšniniai kodai ir etiketės**&gt;**brūkšninio kodo šablono nustatymą**. Šiame puslapyje galite nurodyti brūkšninių kodų skaičių sekos, naudodami anksčiau nurodytus simbolius. Šie brūkšninių kodų skaičių sekos bus naudojamas generuoti brūkšninius kodus ir bus taip pat padeda nustatyti brūkšninius kodus nuskaityti EKA.

1.  Spustelėkite **naujas** sukurti naujus brūkšninio kodo skaičių.
2.  Įveskite reikšmes į **šablono ID** ir **Aprašymas** laukus, o tada pasirinkite brūkšninį kodą kaukė tipo su **tipo** srityje.
3.  – Į **bendrojo** reikšmę, skyriuje, **brūkšninio kodo standartinio** srityje, ir tada nurodykite brūkšninio kodo priešdėlis, jeigu jis yra būtinas.
4.  – Į **brūkšninis kodas kaukė segmento** skyriaus, pridėti brūkšninio kodo segmentų, kuris bus naudojamas brūkšninis kodas turi būti sukurta.

Kaip, pavyzdžiui, sukurti brūkšninio kodo skaičių su šablono ID "Gaminys", jums bus atlikite nurodytus veiksmus.

1.  Sukurti naują brūkšninio kodo skaičių ir pasirinkite tipą "Produktas".
2.  Pasirinkite brūkšninį kodą standartą, pvz., "kodekso 39".
3.  Teikti lengvai nustatyti brūkšninį kodą naudoti priešdėlį. Pvz., "22".
4.  Pridėti kaukės segmentą. Bus pasirinktas "Produkto" kaukė segmente.
5.  Būti trumpesni produktų segmento, pvz., "10". Ilgis turi atitikti produkto ID dažniausiai naudojamas parduotuvėje ilgį. Kaukė bus rodomi kaip peržiūra – į **bendrojo** skyriuje pagal **kaukė**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Priskirti brūkšniniai kodai brūkšninių kodų skaičių sekos
Brūkšninių kodų skaičių sekos turi būti priskirti brūkšninius kodus, kol jie gali būti naudojami. Toliau su ankstesniame pavyzdyje, priskirti brūkšninio kodo skaičių brūkšniniu kodu, atlikite šiuos veiksmus:

1.  Eikite į **organizacijos administracijos**&gt;**sąrankos**&gt;**kodų**. Spustelėkite **naujas** sukurti naują brūkšninį kodą.
2.  Įveskite reikšmes į **brūkšninio kodo****nustatymo** ir ** sąrankos ** laukus.
3.  – Į **bendrojo** skyriuje, visų į **brūkšninio kodo tipas** pasirinkite "39 kodas". – Į **kaukė****ID** pasirinkite anksčiau sukurtą "Produktas" kaukė.
4.  Pagal **dydis**, įveskite "12".
5.  Click **Save**.

Brūkšninio kodo skaičių dabar galima sukurti brūkšninių kodų produktams. Aukščiau nurodytus veiksmus, kaip sukurti brūkšninių kodų skaičių sekos produktų pavyzdžiai, tačiau jie taip pat iliustruoja, kaip sukurti brūkšninių kodų skaičių sekos, bet kitų palaikomų brūkšninio kodo tipus. Brūkšninių kodų skaičių sekos, tipai ir ilgiai turi būti pritaikyti naudoti jūsų aplinkoje.


