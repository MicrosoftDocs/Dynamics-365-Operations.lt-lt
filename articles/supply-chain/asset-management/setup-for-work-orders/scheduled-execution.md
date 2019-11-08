---
title: Numatytas vykdymas
description: Šioje temoje paaiškintas numatytas vykdymas modulyje Turto valdymas.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 89e13179e17b7cf075d631bc65d82da5f24da624
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569851"
---
# <a name="scheduled-execution"></a>Numatytas vykdymas

[!include [banner](../../includes/banner.md)]

 

Galite nustatyti numatytą vykdymą naudodami darbo užsakymo aptarnavimo lygius. (Norėdami gauti daugiau informacijos apie darbo užsakymų aptarnavimo lygius, žr. [Aptarnavimo lygis ir aprašas](service-level-and-description.md).) Numatytas vykdymas suteikia lankstumo planuojant priežiūros darbuotojų darbą, nes galite nustatyti išsamesnius arba mažiau išsamius intervalo, per kurį turėtų būti baigtas darbo užsakymas, reikalavimus. Pavyzdžiui, priežiūros darbuotojas, kuris gamybos patalpoje užduotį atlieka greičiau, nei planuota, gali pereiti prie kitos netoliese esančios užduoties, kuri buvo suplanuota dabartinę savaitę, bet nebūtinai tą pačią dieną. Šis metodas leidžia optimizuoti darbuotojų planavimą ir užduočių vykdymą.

Numatyto vykdymo sąranka, kuri yra susijusi su darbo užsakymais, gali būti bendra arba konkreti. Galite nustatyti bendrų eilučių, kurios taikomos ne tik konkretiems darbo užsakymų tipams, turto tipams ir pan. Arba galite sukurti numatyto vykdymo eilučių, kurios taikomos konkrečiam darbo užsakymo tipui, turto tipui, priežiūros užduoties tipui ir pan.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Numatytas vykdymas**.
2. Pasirinkite **Naujas**, kad sukurtumėte numatyto vykdymo eilutę.
3. Laukuose **Funkcinė vieta**, **Darbo užsakymo tipas**, **Turto tipas**, **Gamintojas**, **Modelis**, **Priežiūros užduoties tipo kategorija**, **Priežiūros užduoties tipas**, **Priežiūros užduoties tipo variantas** ir **Prekyba** pasirinkite reikiamas reikšmes.
4. Lauke **Aptarnavimo lygis** pasirinkite darbo užsakymo aptarnavimo lygį. Jei šį lauką paliksite tuščią, bus sukurta bendriausio tipo numatyto vykdymo eilutė. Norėdami pamatyti bendrosios eilutės pavyzdį, žr. pirmąjį įrašą toliau pateiktoje iliustracijoje. Ši eilutė leidžia konkrečiai datai ir laikui suplanuoti visus darbo užsakymus, kurių darbo užsakymo aptarnavimo lygis nenustatytas.
5. Lauke **Numatytas vykdymas** pasirinkite laiko intervalą.
6. Pasirinkite **Įrašyti**.

![Numatytas vykdymas](media/20-setup-for-work-orders.png)
