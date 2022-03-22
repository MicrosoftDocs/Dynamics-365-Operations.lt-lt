---
title: Nustatykite TDS parametrus
description: Šioje temoje paaiškinama, kaip nustatyti parametrus, siekiant suaktyvinti išskaitytų mokesčių (TDS) funkciją nurodytose operacijose. Tai yra būtinas žingsnis norint naudoti iš šaltinio TDS priemonę atskaityti mokesčius.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e0c0c830391b790f3bc066e319a855b44f7e243f4e086144bbafaa6bb2fa1df3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781712"
---
# <a name="set-the-tds-parameters"></a>Nustatykite TDS parametrus

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti parametrus, siekiant suaktyvinti išskaitytų mokesčių (TDS) funkciją nurodytose operacijose. Tai yra būtinas žingsnis norint naudoti iš šaltinio TDS priemonę atskaityti mokesčius.

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
