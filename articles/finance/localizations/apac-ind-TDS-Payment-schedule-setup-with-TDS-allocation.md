---
title: Nustatyti mokėjimo grafikus su TDS paskirstymu
description: Šioje temoje paaiškinama, kaip nustatyti mokėjimo grafikus (TDS) priemonės išskaitomo mokesčio paskirstymui.
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023456"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>Nustatyti mokėjimo grafikus su TDS paskirstymu

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti mokėjimo grafikus (TDS) priemonės išskaitomo mokesčio paskirstymui.

1. Pasirinkite **Mokėtinos sumos \> Mokėjimų sąranka \> Mokėjimo grafikas**.

    [![Mokėjimo grafikų puslapis](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

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
