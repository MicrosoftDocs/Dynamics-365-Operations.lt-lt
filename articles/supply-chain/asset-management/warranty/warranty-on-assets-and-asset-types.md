---
title: Turto ir jo tipų garantijos
description: Šioje temoje paaiškinama, kaip modulyje Turto valdymas nustatyti turto ir jo tipų garantijas.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 27a079e0fdc0fe1644e59a454659d77ec0eb416b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354209"
---
# <a name="warranties-on-assets-and-asset-types"></a>Turto ir jo tipų garantijos

[!include [banner](../../includes/banner.md)]

 


Šioje temoje paaiškinama, kaip modulyje Turto valdymas nustatyti turto ir jo tipų garantijas.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Turto tipo garantijos nustatymas

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Turto tipai** \> **Turto tipai**.
2. Kairiojoje srityje pasirinkite turto tipą, prie kurio norite pridėti tiekėjo garantijos sutartį, tada pasirinkite **Numatytosios turto tipo reikšmės**.
3. „FastTab“ konteinerio **Bendra** lauke **Tiekėjo garantija** pasirinkite sutartį.

## <a name="set-up-a-warranty-on-an-asset"></a>Turto garantijos nustatymas

1. Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Visas turtas**.
2. Pasirinkite turtą, tada – **Redaguoti**.
3. „FastTab“ konteinerio **Tiekėjas** skyriaus **Tiekėjo garantija** lauke **Garantija** pasirinkite garantijos sutartį.
4. Laukuose **Garantijos pradžia** ir **Garantijos pabaiga** pasirinkite pradžios bei pabaigos datas.

    > [!IMPORTANT]
    > Jei darbo užsakymo lauke **Garantijos pradžia** yra pasirinkta data, darbo užsakymo garantija pradeda galioti tą dieną. Kuriant darbo užsakymą, laukas **Garantijos pradžia** automatiškai nustatomas kaip sukūrimo data. Tačiau šią datą galite pakeisti, kad jį atitiktų, pavyzdžiui, garantijos sutarties pradžios datą.
    >
    > ![Darbo užsakymo puslapis.](media/02-warranty.png)

> [!NOTE]
> Jei, kuriant turto, kuriam taikoma tiekėjo garantija, darbo užsakymą, yra numatyta darbo užsakymo garantijos laikotarpio pradžios data, gaunate pranešimą apie garantijos sutartį. Tada, jei reikia, darbo užsakymą galite atšaukti.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]