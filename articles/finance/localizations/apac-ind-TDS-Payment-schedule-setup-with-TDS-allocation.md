---
title: Nustatyti mokėjimo grafikus su TDS paskirstymu
description: Šiame straipsnyje paaiškinama, kaip nustatyti mokėjimo grafikus naudojant šaltinio (TDS) paskirstyme išskaityus mokesčius.
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
ms.openlocfilehash: 48891c32f39b743ce26e265c5682dab28ecb4b27
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868318"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Nustatyti mokėjimo grafikus su TDS paskirstymu

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti mokėjimo grafikus naudojant šaltinio (TDS) paskirstyme išskaityus mokesčius.

1. Pasirinkite **Mokėtinos sumos \> Mokėjimų sąranka \> Mokėjimo grafikas**.

    [![Mokėjimo grafikų puslapis.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Veiksmų juostoje rinkitės **Naujas** norėdami sukurti mokėjimo grafiką ir įveskite reikiamą informaciją.
3. Lauke **Paskirstymas** pasirinkite metodą, kurį naudosite paskirstyti mokėjimą mokėjimo grafikui:

    - Bendroji suma
    - Fiksuota suma
    - Fiksuotas kiekis
    - Nurodyta

    **Išskaitomo mokesčio paskirstymo** lauke rodomas TDS paskirstymo metodas, skirtas mokėjimo grafikui. Jei lauke **Paskirstymas** pasirenkate **Bendroji** suma, **išskaitomo mokesčio paskirstymo** laukas automatiškai nustatomas kaip Bendroji **suma**. Jei lauke **Paskirstymas pasirenkate**, **Fiksuota suma** arba **Fiksuotas kiekis** esantis **Paskirstymo** lauke, **išskaitomo mokesčio paskirstymo** lauke automatiškai nustatomas **proporcingai**.

    > [!NOTE]
    > Jei išskaitomo mokesčio paskirstymo laukas nustatytas kaip Bendroji suma, mokėjimo mokėjimai apskaičiuojami remiantis bendra suma, į **kurią** įtraukta TDS **suma**. Jei išskaitomo mokesčio paskirstymo laukas nustatytas kaip Proporcinga suma, mokėjimo mokėjimai apskaičiuojami remiantis grynoji suma, į **po** atskaičiuotos TDS **sumos**.

4. Formoje įveskite kitą reikalingą informaciją ir tada užverkite puslapį.
