---
title: Skaidyti SF funkcijas
description: Šiame straipsnyje aprašomos SF skaidymo pagal pristatymo adresą ir mokesčių sąskaitos numerį (TAN) funkcijos.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7bbeb94429c2c69b7b8ea3089390db676a021b80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874438"
---
# <a name="split-invoice-functionality"></a>Skaidyti SF funkcijas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos SF skaidymo pagal pristatymo adresą ir mokesčių sąskaitos numerį (TAN) funkcijos.

Puslapyje **Mokėtinų sąskaitų parametrai** skirtuke **Bendri** rinkitės **Produkto gavimo kvitas** ar **SF** žymimą laukelį, kad publikuotumėte ir išskirstytumėte produkto gavimo kvitą ir SF, kurių pirstatymo adresai ir TAN skiriasi **Pirkimo užsakymo** puslapyje. Užregistruota SF bus padalinta pagal pristatymo adresą ir TAN.

Skirtuke **Suminis atnaujinimas** „FastTab“ **Skaidymas pagrįstas pagal** eilutėje **Pristatymo informacija** nustatykite **Patvirtinimas**, **Paėmimo sąrašas**, **Važtaraštis**, ar **SF** parinktį į **Taip** norėdami publikuoti ir išskaidyti patvirtinimą, paėmimo sąrašą, važtaraštį ar sąskaitą, turinčius kitus pristatymo adresus ir TAN nei nustatyta kitose sąskaitų eilutėse **Pardavimo užsakymas** puslapyje. Užregistruota SF bus padalinta pirma pagal pristatymo adresą ir TAN.

> [!IMPORTANT]
> - Jei **pristatymo informacijos** pasirinktys nėra nustatytos kaip **Taip**, SF bus registruojama kaip viena SF. SF nebus padalyta.
> - Norėdami suskaidyti ir užregistruoti važtaraštį, kuriame SF eilučių pristatymo adresai ir TAN skiriasi, turite nustatyti **pristatymo informacijos** parinkties **Važtaraštis funkciją** į **Taip**.
> - Norėdami suskaidyti ir užregistruoti sąskaitą, kuriame SF eilučių pristatymo adresai ir TAN skiriasi, turite nustatyti **Sąskaita** parinkties **Važtaraštis funkciją** į **Taip**.
> - Norėdami suskaidyti ir užregistruoti sąskaitą, kuriame SF eilučių pristatymo adresai ir TAN tas pats, turite nustatyti **Sąskaita** parinkties **Važtaraštis funkciją** į **Ne**. Užregistruota SF bus padalinta pirma pagal pristatymo adresą ir TAN.

## <a name="example"></a>Pavyzdys

Šiame pavyzdyje **Sąskaita** parinktis **Pristatymo informacijai** yra nustatyta į **Taip** skirtuke **Santraukos naujinimas** puslapyje **Mokėtinų sąskaitų parametrai**. Užregistruojama pirkimo SF, kurios eilutėse nustatyti šie pristatymo adresai ir TAN:

- **1 prekės eilutė 1:** pristatymo adresas, TAN-ABCD12345A
- **2 prekės eilutė 1:** pristatymo adresas, TAN-ABCD12345A
- **3 prekės eilutė 2:** pristatymo adresas, TAN-ABCE12345B
- **4 prekės eilutė 3:** pristatymo adresas, TAN-ABCD12345A

Tokiu atveju originali SF suskaidoma į dvi SF ir registruojama tokiu būdu:

- Registruojama 1 prekės eilutės ir 2 prekės eilutės SF, nes abiejų eilučių pristatymo adresas ir TAN yra vienodi.
- Užregistruota 3 prekės eilutės 2 SF.
- Užregistruota 4 prekės eilutės 3 SF.
