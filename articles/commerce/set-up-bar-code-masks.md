---
title: Brūkšninių kodų skaičių sekų nustatymas
description: Šioje temoje aprašoma, kaip nustatyti brūkšninio kodo skaičių sekos simbolius ir kaip brūkšninio kodo skaičių seką susieti su brūkšniniu kodu.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 265994
ms.assetid: 5831c74d-d2a1-4fa5-9a9a-a5aba8848381
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7bc66b9d6586650dc7b1477ac02260a480d46596
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264581"
---
# <a name="set-up-bar-code-masks"></a>Brūkšninių kodų skaičių sekų nustatymas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti brūkšninio kodo skaičių sekos simbolius ir kaip brūkšninio kodo skaičių seką susieti su brūkšniniu kodu.

## <a name="set-up-bar-code-mask-characters"></a>Brūkšninio kodo skaičių sekos simbolių nustatymas

Brūkšninio kodo skaičių sekos naudojamos brūkšniniams kodams kurti ir greitai identifikuoti brūkšninius kodus, nuskaitytus elektroniniame kasos aparatą (EKA). Skaičių sekos sudaromos iš simbolių, kurie veikia kaip vietos rezervavimo ženklai, nurodantys brūkšninių kodų, kurie bus sukurti, formatą. Norėdami sukonfigūruoti brūkšninio kodo skaičių seką, turite nustatyti brūkšninių kodų skaičių sekų simbolius. Eikite į **Mažmeninė prekyba ir prekyba** &gt; **Atsargų valdymas** &gt; **Brūkšniniai kodai ir etiketės** &gt; **Skaičių sekos simboliai**. Spustelėkite **Naujas** ir sukurkite brūkšninio kodo skaičių sekos simbolius. Skaičių sekos simboliai gali būti sukurti nurodyti šiuos brūkšninių kodų duomenis.

| Laukas            | aprašymas |
|------------------|-------------|
| Produktas          | Produkto ID vietos rezervavimo ženklas. |
| Bet koks skaičius       | Naudojamas nurodyti numerį, kuris bus užprogramuotas brūkšniniuose koduose. |
| Tikrinti skaitmenį      | Nurodo, kad brūkšninio kodo formatas brūkšninio kodo skaičių sekoje naudoja tikrinimo skaitmenį, brūkšninio kodo tinkamumui patvirtinti. |
| Dydžio skaitmuo       | Nurodo dydį brūkšniniame kode sukurtame produkto variante, kuris apima dydį. |
| Spalvos skaitmuo      | Nurodo spalvą brūkšniniame kode sukurtame produkto variante, kuris apima spalva. |
| Spalvos skaitmuo      | Nurodo stilių brūkšniniame kode sukurtame produkto variante, kuris apima stilių. |
| EAN licencijos kodas | Vietos rezervavimo ženklas EAN licencijai, išduotai EAN licencijos kodams. |
| Kaina            | Kainos įdėtiesiems brūkšniniams kodams nurodo kainą. |
| Kiekis         | Kiekio / atsitiktinio svorio įdėtiesiems brūkšniniams kodams nurodo kiekį. |
| Darbuotojas         | Nurodo brūkšninio kodo segmentą darbuotojo ID numeriui, naudojamam EKA prisijungimui brūkšniniu kodu. |
| Klientas         | Nurodo kliento ID segmentą. |
| Duomenų įrašas       | *Dar neįdiegta.* |
| Nuolaidos kodas    | *Nebenaudojama* nuo „Dynamics 365 for Retail“ 2017 m. pavasario leidimo. Anksčiau: nurodo brūkšninio kodo, kuris naudojamas nuolaidai elektroniniame kasos aparate įtraukti, nuolaidos kodą. |
| Kupono kodas      | Nurodo brūkšninio kodo, naudojamo nuolaidai į užsakymą įtraukti, kupono kodą. Jis pakeitė nuolaidos kodą. |
| Dovanų kortelė        | Nurodo dovanų kortelės numerį, išduodant arba mokant dovanų kortele. |
| Lojalumo kortelė     | Įtraukia lojalų klientą į operaciją, gali būti naudojama mokant lojalumo kortele. |

## <a name="define-bar-code-masks"></a>Brūkšninio kodo skaičių sekų nustatymas

Kai brūkšninio kodo skaičių sekos simboliai nurodyti reikalingoms brūkšninio kodo skaičių sekoms, eikite į **Mažmeninė prekyba ir prekyba** &gt; **Atsargų valdymas** &gt; **Brūkšniniai kodai ir etiketės** &gt; **Brūkšninio kodo skaičių sekos nustatymas**. Šiame puslapyje galite nustatyti brūkšninių kodų skaičių sekas, kuriose naudojami anksčiau nurodyti simboliai. Šios brūkšninio kodo skaičių sekos bus naudojamos generuojant brūkšninius kodus ir padės identifikuoti EKA nuskaitytus brūkšninius kodus.

1. Spustelėkite **Naujas** ir sukurkite naują brūkšninio kodo skaičių seką.
2. Įveskite vertes laukuose **Skaičių sekos ID** ir **Aprašas**, tada pasirinkite brūkšninio kodo skaičių sekos tipą lauke **Tipas**.
3. Skyriuje **Bendra** pasirinkite vertę lauke **Standartinis brūkšninis kodas**, tada nurodykite brūkšninio kodo prefiksą, jeigu jo reikalaujama.
4. Skyriuje **Brūkšninio kodo skaičių sekos segmentas** įtraukite brūkšninio kodo segmentus, kurie bus naudojami kuriamame brūkšniniame kode.

Pavyzdžiui, norėdami sukurti brūkšninio kodo skaičių seką su skaičių sekos ID „Produktas“, darytumėte štai ką:

1. Sukurkite naują brūkšninio kodo skaičių seką ir pasirinkite tipą „Produktas“.
2. Pasirinkite brūkšninio kodo standartą, pvz., „Kodas 39“.
3. Pateikite prefiksą, kuris bus naudojamas brūkšniniams kodui lengvai identifikuoti. Pavyzdžiui, „22“.
4. Įtraukite brūkšninio kodo skaičių seką. Bus pasirinktas skaičių sekos segmentas „Produktas“.
5. Pateikite produkto segmento ilgį, pvz., „10“. Ilgis turi atitikti paprastai parduotuvėje naudojamo produkto ID ilgį. Skaičių seka bus rodoma kaip peržiūra skyriuje **Bendra**, dalyje **Skaičių seka**.

## <a name="assign-bar-code-masks-to-bar-codes"></a>Brūkšninio kodo skaičių sekų priskyrimas brūkšniniams kodams

Brūkšninių kodų skaičių sekos prieš naudojant turi būti priskirtos brūkšniniams kodams. Tęsiant ankstesnį pavyzdį, norint brūkšnini kodo skaičių seką priskirti brūkšniniam kodui, atlikite šiuos veiksmus:

1. Eikite į **Organizacijos administravimas** &gt; **Sąranka** &gt; **Brūkšniniai kodai**. Spustelėkite **Naujas**, kad sukurtumėte naują brūkšninį kodą.
2. Įveskite vertes laukuose **Brūkšninis kodas** **nustatymas** ir **Sąranka**.
3. Dalies **Bendra** lauke **Brūkšninio kodo tipas** pasirinkite „Kodas 39“. Lauke **Skaičių sekos** **ID** pasirinkite anksčiau sukurtą „Produkto“ skaičių seką.
4. Lauke **Dydis** įveskite „12“.
5. Spustelėkite **Įrašyti**.

Brūkšninio kodo skaičių seką dabar galima naudoti produktams kuriant brūkšninius kodus. Aukščiau nurodyti veiksmai yra pavyzdžiai, kaip sukurti produktų brūkšninių kodų skaičių sekas, bet jie iliustruoja ir tai, kaip kurti brūkšninio kodo sekas bet kuriems kitiems palaikomiems brūkšninių kodų tipams. Brūkšninių kodų skaičių sekos, tipai ir ilgiai turi būti koreguojami naudoti jūsų konkrečioje aplinkoje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]