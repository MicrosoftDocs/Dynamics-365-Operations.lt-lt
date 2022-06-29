---
title: Darbo užsakymo išsiuntimas
description: Šiame straipsnyje paaiškinama, kaip išsiųsti darbo užsakymą turto valdymo skyriuje.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f78e8642715b0c3fd3d01e8072645ccd9c58d685
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016861"
---
# <a name="dispatch-work-order"></a>Darbo užsakymo išsiuntimas

[!include [banner](../../includes/banner.md)]

 

Naudodami funkciją **Išsiųsti** galite suplanuoti vieną darbo užsakymą arba darbo užsakymo užduotis vienam darbuotojui.

1. Spustelėkite **Turto valdymo darbo** > **užsakymai Visi** > **darbo užsakymai arba** Aktyvūs **darbo užsakymai**.

2. Sąraše pasirinkite darbo užsakymą.

3. Skirtuke **Bendra** spustelėkite **Išsiųsti**.

4. Dialogo lange **Suplanuoti darbo užsakymą** pasirinkite darbuotoją lauke **Darbuotojas**.

5. Lauke **Suplanuoti valandas** galite įvesti numatomas darbo valandas tokiu atveju, kai numatomos darbo valandos skiriasi nuo prognozuojamų valandų.

6. Jei reikia, lauke **Suplanuota pradžia** galite redaguoti pradžios datą ir laiką.

7. Jei planavimo proceso metu reikia atsižvelgti į pajėgumo apribojimus, susijusius su jau suplanuotais kitų užduočių ištekliais, įsitikinkite, kad nustatytos perjungimo mygtukų **Turtas**, **Įrankis** ir **Darbuotojas** reikšmės **Taip**. Jei norite peržiūrėti išsamią informaciją apie planavimo procesą, pasirinkite perjungimo mygtuko **Daugiažodis** reikšmę **Taip**. Tai reiškia, kad išsami informacija apie darbo užsakymo apskaičiuotą rezultatą rodoma sistemos pranešime.

8. Pasirinkite perjungimo mygtuko **Nepaisyti grafiko** reikšmę **Taip**, kad nepaisytumėte uždarytų dienų kalendoriuje (taikoma turtui, darbuotojui ir įrankiams). Pasirinkite perjungimo mygtuko **Nepaisyti suplanuoto vykdymo** reikšmę **Taip**, kad nepaisytumėte apribojimų, kurie gali būti pasirinkti darbo užsakyme dėl planavimo. 

    Informacijos apie suplanuoto vykdymo sąranką ieškokite skyriuje [Suplanuotas vykdymas](../setup-for-work-orders/scheduled-execution.md).

9. Spustelėkite **Gerai**. Darbo užsakymo ciklo būsena automatiškai atnaujinama į ciklo būseną **Suplanuota**, nurodyta **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Ciklo modeliai**.

Žemiau pateiktame paveikslėlyje rodomas išsiuntimo žymėjimų pavyzdys dialogo lange **Suplanuoti darbo užsakymą**.

![1 iliustracija.](media/04-work-order-scheduling.png)

[!NOTE]
Jei norite panaikinti darbo užsakymo grafiką, pasirinkite darbo užsakymą **Visi darbo užsakymai**, o tada spustelėkite **Panaikinti grafiką** skirtuke **Bendra**. Jei ištrinate grafiką, nepamirškite atnaujinti darbo užsakymo ciklo būsenos rankiniu būdu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]