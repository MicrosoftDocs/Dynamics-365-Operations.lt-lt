---
title: Numatytieji didžiosios knygos aprašai
description: Numatytuosius aprašus galima naudoti laukeliui „Aprašas“ atnaujinti DK kvitų registracijose.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500385"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Numatytieji didžiosios knygos aprašai

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Numatytuosius aprašus galima naudoti laukeliui **Aprašas** atnaujinti DK kvitų registracijose. Ši funkcija patobulinta darbui su iškrovimo kaina.

Kad nustatytumėte DK registracijų numatytuosius aprašus, eikite į **Organizacijos administravimas \> Sąranka \> Numatytieji aprašai**.

Šioje lentelėje pateikiamas naujų verčių, kurios buvo pridėtos laukelyje **Aprašas**, vertės puslapyje **Numatytieji aprašai** iškrovimo kainai palaikyti.

| Aprašo tipas | Pastabos |
|---|---|
| Importavimo įkainojimas – savikainos kaupimas | Pirkimo užsakyme užregistravus SF, savikainos kaupimas apdorojimas vertinamai reiso savikainai. Galima nurodyti prie reiso numerio aprašo pridėti numatytuosius aprašus. Siuntos numeriui naudokite *%4*. |
| Importavimo įkainojimas – tranzito prekių užsakymas | Jei naudojate tranzitinį apdorojimą, užregistruojama pirkimo užsakymo SF, o prekės registruojamos tranzito prekių sąskaitoje. Galima nurodyti prie tranzito užsakymo numerio aprašo pridėti numatytuosius aprašus. Kaip tranzito užsakymo numerį naudokite *%4*. |
| Atsargos – Uždarymas – Koregavimas | Kai mokėtinų sumų (MS) SF apdorojama reiso savikainai, atsargų koregavimas apdorojamas reiso savikainai įvertinti. Galima nurodyti prie reiso numerio aprašo pridėti numatytuosius aprašus. Siuntos numeriui naudokite *%4*. |

Daugiau informacijos apie tai, kaip dirbti su puslapiu **Numatytieji aprašai**, žr. [Numatytųjų aprašų nustatymas automatiniam registravimui](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
