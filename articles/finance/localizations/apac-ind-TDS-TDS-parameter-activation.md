---
title: Nustatykite TDS parametrus
description: Šiame straipsnyje paaiškinama, kaip nustatyti parametrus, kad nurodytų operacijų metu būtų galima suaktyvinti išskaitytų mokesčių (TDS) funkciją. Tai yra būtinas žingsnis norint naudoti iš šaltinio TDS priemonę atskaityti mokesčius.
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
ms.openlocfilehash: 3390cad6979858fbff73769d0d25132ba18a2157
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865619"
---
# <a name="set-the-tds-parameters"></a>Nustatykite TDS parametrus

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti parametrus, kad nurodytų operacijų metu būtų galima suaktyvinti išskaitytų mokesčių (TDS) funkciją. Tai yra būtinas žingsnis norint naudoti iš šaltinio TDS priemonę atskaityti mokesčius.

1. Eikite į **Didžioji knyga \> Didžiosios knygos nustatymas \> DK parametrai**.
2. Skirtuko **Tiesioginiai mokesčiai** dalyje **Šaltinio atskaityti mokesčiai** nustatykite **Suaktyvinti TDS** parinktį į **Taip** norėdami suaktyvinti TDS funkciją, ir jai naudojamus puslapius ir laukus.
3. Nustatykite **SF** parinktį į **Taip** norėdami suaktyvinti laukus, kurie naudojami TDS apskaičiuoti ir atskaityti SF lygiu.
4. Nustatykite **Mokėjimas** parinktį į **Taip** norėdami suaktyvinti laukus, kurie naudojami TDS apskaičiuoti ir atskaityti mokėjimo lygiu.

    [![Skirtukas Tiesioginiai mokesčiai.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. Numeracijų **skirtuke raskite** eilutę, kurioje **nuorodos** lauke nustatyta **išskaitomo mokesčio mokėjimas**. Lauke **Numerio sekos kodas** eilutei, pasirinkite numerio sekos kodą. Numeracijos kodas naudojamas periodinio TDS sudengimo proceso kvitų numeriams generuoti.

    > [!NOTE]
    > Norėdami vykdyti periodinio TDS sudengimo procesą, eikite į **Mokesčių \> Deklaracijos \> Išskaitomas mokestis \> Išskaitomo mokesčio mokėjimas**.

    [![Numeracijų skirtukas.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Uždarykite puslapį.
