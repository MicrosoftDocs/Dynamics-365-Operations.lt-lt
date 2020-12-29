---
title: Suplanuotų užsakymų tvirtinimas
description: Šioje temoje aprašomas suplanuotų užsakymų, palaikomų „Planning Optimization“, tvirtinimas.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433566"
---
# <a name="approve-planned-orders"></a>Suplanuotų užsakymų tvirtinimas

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip atnaujinti suplanuotų užsakymų būseną „Planning Optimization“.

Atkreipkite dėmesį, kad suplanuotų užsakymų tvirtinimas yra pasirinktinis veiksmas, skirtas sukurti patvirtintą suplanuotą užsakymą. Rekomenduojama patvirtinti modifikuotus suplanuotus užsakymus, kitu atveju pakeitimų bus nepaisoma ir jie bus perrašyti kito planavimo vykdymo metu.

![Suplanuoto užsakymo srautas](media/approved-planned-orders-1.png)

Laukas **Būsena** padeda sekti jūsų procesą naudojant toliau pateiktas reikšmes.

- **Neapdorota:** kai bendrasis planavimas sugeneruoja suplanuotus užsakymus, suplanuotų užsakymų būsena yra *Neapdorota*. Šios būsenos suplanuoti užsakymai bus panaikinti kito planavimo vykdymo metu.
- **Baigta:** jei nusprendžiate netvirtinti suplanuoto užsakymo, galite pakeisti būseną į *Baigta*, kad nurodytumėte, jog baigėte šio suplanuoto užsakymo vertinimą. Atkreipkite dėmesį, kad būsenas *Neapdorota* ir *Baigta* sistema valdo vienodai.
- **Patvirtinta:** jei norite palikti pakeitimus arba planuojate tvirtinti suplanuotą užsakymą, pakeiskite būseną į *Patvirtinta*. Suplanuoti užsakymai, kurių būsena yra *Patvirtinta*, laikomi fiksuotais ir numatyto tiekimo bendrojo planavimo metu, kad nebūtų modifikuojami ar panaikinami vėlesnių pagrindinio planavimo vykdymų metu. Norint tai pasiekti, planavimo logika kopijuoja *patvirtintus* suplanuotus užsakymus iš senosios plano versijos į naująją plano versiją bendrojo planavimo metu. Atkreipkite dėmesį, kad suplanuoti užsakymai, kurių būsena *Patvirtinta*, laikomi numatyto tiekimo tik konkrečiame pagrindiniame plane.

Suplanuotus užsakymus galite valdyti naudodami darbo sritį **Bendrasis planavimas**, sąrašą **Suplanuoti užsakymai** arba sąrašus **Suplanuoti gamybos užsakymai**, **Suplanuoti pirkimo užsakymai** ir **Suplanuotas perkėlimas**.
