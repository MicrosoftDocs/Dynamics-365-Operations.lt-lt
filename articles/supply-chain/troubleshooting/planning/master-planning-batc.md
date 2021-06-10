---
title: Negalite filtruoti bendrojo planavimo prekių pagal jų susijusias padengimo grupės reikšmes
description: Negalite filtruoti bendrojo planavimo prekių pagal jų susijusias padengimo grupės reikšmes.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049481"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a>Negalite filtruoti bendrojo planavimo prekių pagal jų susijusias padengimo grupės reikšmes

KB numeris: 4612572

## <a name="symptoms"></a>Požymiai

Norite filtruoti prekes, kurios bus įtrauktos į bendrojo planavimo paketinę užduotį, remiantis susijusių įrašų reikšmėmis iš prekių padengimo lentelės. (Pavyzdžiui, norite filtruoti prekes pagal jų **Tiekėjo** ir (arba) **Padengimo grupės** reikšmę). Paketinės užduoties filtro nustatymas leidžia jums sukurti jungtį iš **Prekių** lentelės į **Prekių padengimo** lentelę, o tada nurodyti laukų reikšmės iš prekių padengimo lentelės jūsų užklausoje. Tačiau, jums užbaigus šį nustatymą, sistema vis tiek kuria suplanuotus užsakymus visam prekių padengimui, o ne tik prekėms, kurios atitinka nurodytas laukų reikšmes iš prekių padengimo lentelės.

## <a name="resolution"></a>Paaiškinimas

Paketinių užduočių filtras gali filtruoti tik prekes. Nors galite įtraukti sujungimą į **Prekės padengimo** lentelę, filtravimo parametrai, kuriuos taikote tai lentelei, nepaveiks užklausos išeigos. Vykdymo metu sistema vykdo visų padengimo grupių ir visų filtruotų prekių variantų planavimą. Kai prekė jau yra įtraukta į vykdymą, visos į prekės filtrą įtrauktos padengimo grupės nebus paveiktos planavimo išeigos.
