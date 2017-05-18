---
title: "Brūkšninių kodų skaičių sekų nustatymas"
description: "Šioje temoje aprašoma, kaip nustatyti brūkšninio kodo skaičių sekos simbolius ir kaip brūkšninio kodo skaičių seką susieti su brūkšniniu kodu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 4c80cfdaee2c797f0f57460c88e9ebb1c8156737
ms.contentlocale: lt-lt
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-bar-code-masks"></a>Brūkšninių kodų skaičių sekų nustatymas

[!include[banner](includes/banner.md)]


Šioje temoje aprašoma, kaip nustatyti brūkšninio kodo skaičių sekos simbolius ir kaip brūkšninio kodo skaičių seką susieti su brūkšniniu kodu.

<a name="set-up-bar-code-mask-characters"></a>Brūkšninio kodo skaičių sekos simbolių nustatymas
-------------------------------

Brūkšninio kodo skaičių sekos naudojamos brūkšniniams kodams kurti ir greitai identifikuoti brūkšninius kodus, nuskaitytus elektroniniame kasos aparatą (EKA). Skaičių sekos sudaromos iš simbolių, kurie veikia kaip vietos rezervavimo ženklai, nurodantys brūkšninių kodų, kurie bus sukurti, formatą. Norėdami sukonfigūruoti brūkšninio kodo skaičių seką, turite nustatyti brūkšninių kodų skaičių sekų simbolius. Eikite į **Mažmeninė prekyba ir prekyba** &gt; **Atsargų valdymas** &gt; **Brūkšniniai kodai ir etiketės** &gt; **Skaičių sekos simboliai**. Spustelėkite **Naujas** ir sukurkite brūkšninio kodo skaičių sekos simbolius. Skaičių sekos simboliai gali būti sukurti nurodyti šiuos brūkšninių kodų duomenis.

|                      |                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------|
| **Laukas**            | **Aprašas**                                                                                                 |
| **Produktas**          | Produkto ID vietos rezervavimo ženklas.                                                                                     |
| **Bet koks skaičius**       | Naudojamas nurodyti numerį, kuris bus užprogramuotas brūkšniniuose koduose.                                                  |
| **Tikrinti skaitmenį**      | Nurodo, kad brūkšninio kodo formatas brūkšninio kodo skaičių sekoje naudoja tikrinimo skaitmenį, brūkšninio kodo tinkamumui patvirtinti. |
| **Dydžio skaitmuo**       | Nurodo dydį brūkšniniame kode sukurtame produkto variante, kuris apima dydį.                                 |
| **Spalvos skaitmuo**      | Nurodo spalvą brūkšniniame kode sukurtame produkto variante, kuris apima spalva.                               |
| **Spalvos skaitmuo**      | Nurodo stilių brūkšniniame kode sukurtame produkto variante, kuris apima stilių.                             |
| **EAN licencijos kodas** | Vietos rezervavimo ženklas EAN licencijai, išduotai EAN licencijos kodams.                                                       |
| **Kaina**            | Kainos įdėtiesiems brūkšniniams kodams nurodo kainą.                                                                   |
| **Kiekis**         | Kiekio / atsitiktinio svorio įdėtiesiems brūkšniniams kodams nurodo kiekį.                                                |
| **Darbuotojas**         | Nurodo brūkšninio kodo segmentą darbuotojo ID numeriui, naudojamam EKA prisijungimui brūkšniniu kodu.                                  |
| **Klientas**         | Nurodo kliento ID segmentą.                                                                                  |
| **Duomenų įrašas**       | *Dar neįdiegta.*                                                                                          |
| **Nuolaidos kodas**    | Nurodo brūkšninio kodo, kuris naudojamas nuolaidai elektroniniame kasos aparate pridėti, nuolaidos kodą             |
| **Dovanų kortelė**        | Nurodo dovanų kortelės numerį, išduodant arba mokant dovanų kortele.                                               |
| **Lojalumo kortelė**     | Įtraukia lojalų klientą į operaciją, gali būti naudojama mokant lojalumo kortele.                             |

## <a name="define-bar-code-masks"></a>Brūkšninio kodo skaičių sekų nustatymas
Brūkšninio kodo skaičių sekos simboliai nurodyti reikalingoms brūkšninio kodo skaičių sekoms, eikite į **Mažmeninė prekyba ir prekyba** &gt; **Atsargų valdymas** &gt; **Brūkšniniai kodai ir etiketės** &gt; **Brūkšninio kodo skaičių sekos nustatymas**. Šiame puslapyje galite nustatyti brūkšninių kodų skaičių sekas, kuriose naudojami anksčiau nurodyti simboliai. Šios brūkšninio kodo skaičių sekos bus naudojamos generuojant brūkšninius kodus ir padės identifikuoti EKA nuskaitytus brūkšninius kodus.

1.  Spustelėkite **Naujas** ir sukurkite naują brūkšninio kodo skaičių seką.
2.  Įveskite vertes laukuose **Skaičių sekos ID** ir **Aprašas**, tada pasirinkite brūkšninio kodo skaičių sekos tipą lauke **Tipas**.
3.  Skyriuje **Bendra** pasirinkite vertę lauke **Standartinis brūkšninis kodas**, tada nurodykite brūkšninio kodo prefiksą, jeigu jo reikalaujama.
4.  Skyriuje **Brūkšninio kodo skaičių sekos segmentas** įtraukite brūkšninio kodo segmentus, kurie bus naudojami kuriamame brūkšniniame kode.

Pavyzdžiui, norėdami sukurti brūkšninio kodo skaičių seką su skaičių sekos ID „Produktas“, darytumėte štai ką:

1.  Sukurkite naują brūkšninio kodo skaičių seką ir pasirinkite tipą „Produktas“.
2.  Pasirinkite brūkšninio kodo standartą, pvz., „Kodas 39“.
3.  Pateikite prefiksą, kuris bus naudojamas brūkšniniams kodui lengvai identifikuoti. Pvz., „22“.
4.  Įtraukite brūkšninio kodo skaičių seką. Bus pasirinktas skaičių sekos segmentas „Produktas“.
5.  Pateikite produkto segmento ilgį, pvz., „10“. Ilgis turi atitikti paprastai parduotuvėje naudojamo produkto ID ilgį. Skaičių seka bus rodoma kaip peržiūra skyriuje **Bendra**, dalyje **Skaičių seka**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Brūkšninio kodo skaičių sekų priskyrimas brūkšniniams kodams
Brūkšninių kodų skaičių sekos prieš naudojant turi būti priskirtos brūkšniniams kodams. Tęsiant ankstesnį pavyzdį, norint brūkšnini kodo skaičių seką priskirti brūkšniniam kodui, atlikite šiuos veiksmus:

1.  Eikite į **Organizacijos administravimas** &gt; **Sąranka** &gt; **Brūkšniniai kodai**. Spustelėkite **Naujas**, kad sukurtumėte naują brūkšninį kodą.
2.  Įveskite vertes laukuose **Brūkšninis kodas** **nustatymas** ir **Nustatymas **.
3.  Skyriaus **Bendra** lauke **Brūkšninių kodų tipai** pasirinkite „Kodas 39’. Laukuose **Skaičių seka** **ID** pasirinkite anksčiau sukurtą „Produkto“ skaičių seka.
4.  Lauke **Dydis** įveskite „12“.
5.  Spustelėkite **Įrašyti**.

Brūkšninio kodo skaičių seką dabar galima naudoti produktams kuriant brūkšninius kodus. Aukščiau nurodyti veiksmai yra pavyzdžiai, kaip sukurti produktų brūkšninių kodų skaičių sekas, bet jie iliustruoja ir tai, kaip kurti brūkšninio kodo sekas bet kuriems kitiems palaikomiems brūkšninių kodų tipams. Brūkšninių kodų skaičių sekos, tipai ir ilgiai turi būti koreguojami naudoti jūsų konkrečioje aplinkoje.




