---
title: Darbo užsakymų iš priežiūros užklausų kūrimas
description: Šioje temoje paaiškinama, kaip sukurti darbo užsakymą iš priežiūros užklausos turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f7af87f359cfe3a606c8be857dd905bfef75e97
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847464"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Darbo užsakymų iš priežiūros užklausų kūrimas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Sukūrę priežiūros užklausas, galite lengvai jas konvertuoti į darbo užsakymus. Šioje temoje aprašomas greičiausias būdas dirbti su priežiūros užklausomis, atnaujinti kelias priežiūros užklausas vienu metu, o tada sukurti darbo užsakymą kelioms priežiūros užklausoms tuo pačiu metu. Puslapiuose **Active maintenance requests** arba **My functional location maintenance requests** galite vienu metu dirbti su viena priežiūros užklausa ir konvertuoti vieną priežiūros užklausą į darbo užsakymą.

> [!NOTE]
> Kiekviena priežiūros užklausa gali būti susijusi tik su vienu darbo užsakymu. Tačiau kelias priežiūros užklausas galima įtraukti į vieną darbo užsakymą, net jei priežiūros užklausos turi skirtingas lėšas.

1. Pasirinkite **Asset management**\>**Common**\>**maintenance requests**\>**All maintenance requests**.
2. Prieš kurdami darbo užsakymą pagal priežiūros užklausas, turite pasirinkti bent priežiūros užklausų priežiūros užduoties tipą, taip pat priežiūros užduoties tipo variantą ir prekybą, jei ši informacija yra aktuali. Tinklelio rodinyje galite lengvai atnaujinti informaciją apie priežiūros užklausą.
3. Kai būsite pasirengę kurti darbo užsakymą, pasirinkite priežiūros užklausas, kurias į jį įtrauksite.

    - Jei pasirenkate kelias priežiūros užklausas, kurias konvertuosite į darbo užsakymą, prieš kurdami darbo užsakymą, turite nustatyti laukus **„Turtas“** ir **„Priežiūros užduoties tipas“**.
    - Jei pasirenkate vieną priežiūros užklausą, kurią konvertuosite į darbo užsakymą, prieš kurdami darbo užsakymą, turite nustatyti tik lauką **Asset**. Tačiau kurdami darbo užsakymą, dialogo lange **„Kurti darbo užsakymą“** galite pasirinkti priežiūros užduoties tipą (ir susijusį priežiūros užduoties tipo variantą ir prekybą, jei ši informacija yra aktuali).

4. Pasirinkite **„Darbo užsakymas“**.
5. Dialogo lange **„Kurti darbo užsakymą“** nustatykite laukus ir pasirinkite **„Gerai“**.

    Pranešimo juosta gali įspėti, kad sukurtas naujas darbo užsakymas.

    Be to, kai sukuriate darbo užsakymą, pagrįstą priežiūros užklausa, jei su priežiūros užklausa susijęs turtas yra įtrauktas į garantijos sutartį, pranešimo juosta įspėja apie garantijos sutartį.

6. Pasirinkite **Asset management** \> **Common** \> **Work orders** \> **All work orders** ir atidarykite naują darbo užsakymą.

    ![1 paveikslėlis](media/05-manage-maintenance-requests.png)

