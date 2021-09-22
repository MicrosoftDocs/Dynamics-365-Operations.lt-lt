---
title: Bendro prekių kiekio klaida mėginant baigti užsakymą
description: Bandant užbaigti gamybos užsakymą ir pranešti, kad baigta, galite gauti bendrą prekių kiekio klaidą. Šiame puslapyje paaiškinama, kodėl ir kaip sumažinti fiksuotą išdavimą.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477082"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Bendro prekių kiekio klaida mėginant baigti gamybos užsakymą

## <a name="symptoms"></a>Požymiai

Jums bandant publikuoti ataskaitą kaip baigtą žurnalą gamybos užsakyme, gausite tolesnį klaidos pranešimą:

> Bendras prekių kiekis, kuris yra paskelbtas baigtas gamybai, bus %1. Paskutinės operacijos atsiliepimas yra 0,00 bendrai.

## <a name="cause"></a>Priežastis

Ši problema atsitinka, jei publikuoti kiekiai paskutinėse operacijose nebuvo teisingi. Pavyzdžiui, jei gamyba yra pradėta, bet nurodytas kiekis negali būti priskirtas, maršruto kortelės žurnalas bus publikuotas be jokių eilučių. Norėdami patvirtinti situaciją, atverkite gamybos užsakymą ir tada veiksmų juostoje, **Peržiūros** skirtuke pasirinkite **Nukreipti kortelę**.

## <a name="resolution"></a>Sprendimas

Galite ištaisyti šią klaidą publikuodami papildomus žurnalus operacijoms, kurioms žurnalai nebuvo tinkamai publikuoti. Paleiskite iš naujo gamybos užsakymą ir rinkitės papildomų žurnalų publikavimą. Šis veiksmas nepradės gamybos užsakymo, bet publikuos žurnalus. Maršruto kortelė tuomet turi rodyti publikuotus kiekius ir jūs tūrėtumėte galėti užbaigti gamybos užsakymus sėkmingai.
