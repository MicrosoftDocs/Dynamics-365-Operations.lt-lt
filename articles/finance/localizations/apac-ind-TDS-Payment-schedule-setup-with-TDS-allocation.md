---
title: Nustatyti mokėjimo grafikus su TDS paskirstymu
description: Šioje temoje paaiškinama, kaip nustatyti mokėjimo grafikus (TDS) priemonės išskaitomo mokesčio paskirstymui.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 31ecf2e6fa4d3d37c3d5332dc1d5592bf1a99bad
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2022
ms.locfileid: "8408095"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Nustatyti mokėjimo grafikus su TDS paskirstymu

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti mokėjimo grafikus (TDS) priemonės išskaitomo mokesčio paskirstymui.

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
