---
title: Negalima pakeisti patvirtinto tiekėjo įsigaliojimo datos
description: Patvirtintų tiekėjų sąrašas pagal produkto objektą neleidžia pakeisti įsigaliojimo datos
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477048"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Negalima pakeisti patvirtinto tiekėjo įsigaliojimo datos


## <a name="symptoms"></a>Požymiai

Produktas turi patvirtintą tiekėją, kurio įsigaliojimo data, pavyzdžiui, yra 2018 m. sausio mėn. 11 d. (*11/01/2018*) ir galiojimo data yra *Niekada*. Jeigu bandysite pakeisti įsigaliojimo datą iki 2018 m. sausio mėn. 10 d. (*10/01/2018*) arba 2018 m. sausio mėn. 12 d., (*12/01/2018*), gausite šią klaidą:

> Negalima sukurti įrašo patvirtintame tiekėjų sąraše (PdsApproveVendorList). Vertė „Galiojimas” turi būti didesnė arba lygi vertei „Įsigaliojimas”.

## <a name="resolution"></a>Sprendimas

Galite pratęsti tik tokį laikotarpį, kuriam tiekėjas yra patvirtintas. Galioja šios taisyklės:

- Norėdami pakeisti įsigaliojimo datą taip, kad ji būtų ankstesnė nei bet kuris esamas faktinis prekės tiekėjo įrašas (laikotarpiai), naujo laikotarpio galiojimo pabaigos data turi būti ankstesnė už visas esamų įrašų galiojimo datas.
- Norėdami pakeisti galiojimo datą taip, kad ji būtų vėlesnė nei bet kuris iš esamų laikotarpių, galiojimo data turi būti vėlesnė nei vėliausia data iš esamų įrašų.
- Norėdami sumažinti bendrą laikotarpį, kuriam tiekėjas buvo patvirtintas, turite panaikinti arba modifikuoti esamus įrašus. Taip pat galite naudoti jungiklį **Sutrumpinti** importavimo metu. Šis jungiklis panaikina visus esamus įrašus, esančius patvirtintų tiekėjų pagal prekę lentelėje.

Scenarijaus pavyzdyje, kuris aprašytas problemos aprašyme, kur įrašo įsigaliojimo data yra *11/01/2018* ir galiojimo pabaigos data yra *Niekada* galite importuoti naują įrašą, kurio įsigaliojimo data yra *10/01/2018* ir galiojimo pabaigos data yra *Niekada*. Tačiau negalite sutrumpinti laikotarpio taip, kad įsigaliojimo data būtų atnaujinta į *12/01/2018* per duomenų valdymą. Turite atlikti šį keitimą per vartotojo sąsają.
