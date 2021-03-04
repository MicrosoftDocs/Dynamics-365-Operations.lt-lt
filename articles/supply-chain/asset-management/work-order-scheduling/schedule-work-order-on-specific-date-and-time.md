---
title: Darbo užsakymo planavimas konkrečią dieną ir konkrečiu laiku
description: Šioje temoje paaiškinta, kaip konkrečią dieną ir konkrečiu laiku suplanuoti darbo užsakymą naudojant modulį Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e81ea13a3463965c6e4785dac32f536d2e94a7ba
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433495"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Darbo užsakymo planavimas konkrečią dieną ir konkrečiu laiku

[!include [banner](../../includes/banner.md)]

 

Jei darbo užsakymas turi būti suplanuotas konkrečią dieną *ir* konkrečiu laiku, galite perrašyti įprastą planavimo procesą modulyje Turto valdymas ir sukurti specialų darbo užsakymo grafiką.

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Darbo užsakymų sąraše, stulpelyje **Darbo užsakymas**, spustelėkite darbo užsakymo ID.

3. Spustelėkite **Redaguoti**.

4. „FastTab“ **Darbo užsakymo antraštė** laukuose **Numatoma pradžia** ir **Numatoma pabaiga** įveskite pradžios ir pabaigos datas ir laiką.

    ![1 pav.](media/05-work-order-scheduling.png)

5. Skirtuke **Bendra** spustelėkite **Grafikas**, kad naudotumėte įprastą planavimo procesą, arba spustelėkite **Išsiųsti**, jei darbo užsakymą norite priskirti konkrečiam darbuotojui.

6. Norėdami perrašyti bet kokius esamus pajėgumo rezervavimus siekiant užtikrinti, kad darbo užsakymas bus suplanuotas numatomu laikotarpiu, dialogo lango **Planuoti darbo užsakymą** > skyriuje **Ribotas pajėgumas** pažymėkite parinktis, kaip parodyta toliau pateiktame paveikslėlyje. Tai reiškia, kad planavimo proceso metu bus nepaisoma esamų pajėgumo rezervavimų, nes darbo užsakymas turi būti pradėtas numatomu pradžios laiku.

    ![2 paveikslėlis](media/06-work-order-scheduling.png)

7. Spustelėkite **Gerai**, kad pradėtumėte planavimą.

8. Jei planavimo proceso metu sukuriama dvigubų rezervavimų, ekrane matysite pranešimą ir galėsite koreguoti susijusius darbo užsakymus.

>[!NOTE]
>Kad būtų galima suplanuoti darbo užsakymo priežiūros darbuotoją, tas priežiūros darbuotojas turi būti pasiekiamas numatomą pradžios datą ir numatomu pradžios laiku. Darbuotojų pasiekiamumas nustatomas [darbuotojų kalendoriuje](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]