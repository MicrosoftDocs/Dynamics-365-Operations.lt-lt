---
title: Darbo užsakymo išsiuntimas
description: Šioje temoje aiškinama, kaip išsiųsti darbo užsakymą turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887210"
---
# <a name="dispatch-work-order"></a>Darbo užsakymo išsiuntimas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Naudodami funkciją **Išsiųsti** galite suplanuoti vieną darbo užsakymą arba darbo užsakymo užduotis vienam darbuotojui.

1. Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.

2. Sąraše pasirinkite darbo užsakymą.

3. Skirtuke **Bendra** spustelėkite **Išsiųsti**.

4. Dialogo lange **Suplanuoti darbo užsakymą** pasirinkite darbuotoją lauke**Darbuotojas**.

5. Lauke **Suplanuoti valandas** galite įvesti numatomas darbo valandas tokiu atveju, kai numatomos darbo valandos skiriasi nuo prognozuojamų valandų.

6. Jei reikia, lauke **Suplanuota pradžia** galite redaguoti pradžios datą ir laiką.

7. Jei planavimo proceso metu reikia atsižvelgti į pajėgumo apribojimus, susijusius su jau suplanuotais kitų užduočių ištekliais, įsitikinkite, kad perjungimo mygtukai **Turtas** **Įrankis** **Darbuotojas** yra nustatyti į Taip. Jei norite peržiūrėti išsamią informaciją apie planavimo procesą, perjungimo mygtuke **Daugiažodis** pasirinkite Taip. Tai reiškia, kad išsami informacija apie darbo užsakymo apskaičiuotą rezultatą rodoma sistemos pranešime.

8. Perjungimo mygtuke **Nepaisyti grafiko** pasirinkite Taip, kad nepaisytumėte uždarytų dienų kalendoriuje (taikoma turtui, darbuotojui ir įrankiams). Perjungimo mygtuke **Nepaisyti suplanuoto vykdymo** pasirinkite Taip, kad nepaisytumėte apribojimų, kurie gali būti pasirinkti darbo užsakyme dėl planavimo. Daugiau informacijos apie suplanuoto vykdymo sąranką ieškokite skyriuje [Suplanuotas vykdymas](../setup-for-work-orders/scheduled-execution.md).

9. Spustelėkite **Gerai**. Darbo užsakymo ciklo būsena automatiškai atnaujinama į nurodytą ciklo būseną Suplanuota **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Ciklo modeliai**

Žemiau pateiktame paveikslėlyje rodomas išsiuntimo žymėjimų pavyzdys dialogo lange **Suplanuoti darbo užsakymą**.

![1 pav.](media/04-work-order-scheduling.png)

>[!NOTE]
>Jei norite panaikinti darbo užsakymo grafiką, tai galite padaryti pasirinkdami darbo užsakymą parinktyje **Visi darbo užsakymai** ir spustelėdami **Panaikinti grafiką** skirtuke **Bendra**. Jei ištrinate grafiką, nepamirškite atnaujinti darbo užsakymo ciklo būseną rankiniu būdu.

