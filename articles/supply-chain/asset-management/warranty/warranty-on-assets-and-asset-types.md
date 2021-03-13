---
title: Turto ir jo tipų garantijos
description: Šioje temoje paaiškinama, kaip modulyje Turto valdymas nustatyti turto ir jo tipų garantijas.
author: josaw1
manager: tfehr
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c0359bfe31b3d01f28028bb17d5d30af39a1db9
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021609"
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
    > ![Darbo užsakymo puslapis](media/02-warranty.png)

> [!NOTE]
> Jei, kuriant turto, kuriam taikoma tiekėjo garantija, darbo užsakymą, yra numatyta darbo užsakymo garantijos laikotarpio pradžios data, gaunate pranešimą apie garantijos sutartį. Tada, jei reikia, darbo užsakymą galite atšaukti.
