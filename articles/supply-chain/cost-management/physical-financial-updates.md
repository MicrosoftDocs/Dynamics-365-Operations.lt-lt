---
title: Faktiniai ir finansiniai atnaujinimai
description: Šioje temoje apžvelgiama, kokių tipų operacijos didina arba mažina atsargų kiekius.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4360f9132d31c9d0038f51c68c1f6c3fcaaa2025
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250876"
---
# <a name="physical-and-financial-updates"></a>Faktiniai ir finansiniai atnaujinimai

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiama, kokių tipų operacijos didina arba mažina atsargų kiekius. 

Atsargų operacijas galima faktiškai ir finansiškai naujinti „Dynamics 365 Supply Chain Management“. Kai kurių tipų faktinėse ir finansinėse operacijose atsargų kiekiai yra padidinami, o kitose – sumažinami.

## <a name="physical-increases"></a>Faktinis didėjimas
Kai užregistruota faktinė operacija, operacijos įrašo būsena yra **Gauta**. Toliau pateiktos operacijos laikomos faktiniais padidėjimais:

-   Pirkimo užsakymo gavimas
-   Pardavimo užsakymo važtaraščio grąžinimas
-   Gamybos užsakymo skelbimas baigtu
-   Šalutinis produktas gamybos užsakymo išrinkimo dokumente

## <a name="financial-increases"></a>Finansiniai padidėjimai
Kai užregistruojama finansinė gavimo operacija, operacijos įrašo būsena, didinanti kiekį, yra **Nupirkta**. Toliau pateiktos operacijos laikomos finansiniais padidėjimais:

-   Tiekėjo SF
-   Pardavimo užsakymo grąžinimo SF
-   Gamybos užsakymo įkainojimas
-   Teigiamo kiekio atsargų žurnalai, pvz., judėjimo, pelno ir nuostolio, inventorizacijos, KS, ir perkėlimo

## <a name="transactions-that-increase-quantity"></a>Kiekį didinančios operacijos
Operacijos, kuriose kiekis padidinamas, registruojamos vykdoma vidutine savikaina. Apskaičiuota naudojama vidutinė savikaina pagrįsta kiekvienos iš šių operacijų išlaidomis kiekvienai atsargų dimensijai, kuri sekama finansiškai. Daugiau informacijos apie naudojamą vidutinę savikainą rasite dalyje [Naudojama vidutinė savikaina](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Kiekį mažinančios operacijos
Apskaičiuota vykdoma vidutinė savikaina naudojama, kai užregistruojama kiekį mažinanti operacija, nepaisant, koks atsargų modelis yra susietas su tomis atsargomis. Kiekį mažinanti operacijos negali būti pažymėta kitai operacijai prieš registruojant. Jei faktinės turimos atsargos tampa neigiamos, naudojama atsargų savikaina, nustatyta prekei puslapyje **Prekė**. 

> [!NOTE]
> Jei įgalinta kelių teritorijų funkcija, ši savikaina bus atsargų savikaina, nustatyta teritorijai puslapyje **Numatytieji užsakymo parametrai**.

## <a name="physical-issues-vs-financial-issues"></a>Faktinis išdavimas ir finansinis išdavimas
Kai užregistruota faktinė išdavimo operacija, operacijos įrašo būsena yra **Paimta**. Toliau pateiktos operacijos laikomos faktiniais išdavimais:

-   Gamybos užsakymo išrinkimo dokumentų žurnalas
-   Pardavimo užsakymo važtaraštis
-   Pirkimo užsakymo važtaraščio grąžinimas

Kai užregistruota finansinė operacija, operacijos įrašo būsena yra **Parduota**. Toliau pateiktos operacijos laikomos finansiniais išdavimais:

-   Gamybos užsakymo baigimas
-   Pardavimo užsakymo SF
-   Tiekėjo SF grąžinimas
-   Neigiamo kiekio atsargų žurnalai, pvz., judėjimo, pelno ir nuostolio, inventorizacijos, KS, ir perkėlimo

Operacijos, kurios mažina kiekį, registruojamos vykdoma vidutine savikaina. Todėl norint sudengti išdavimo operacijas su gavimo operacijomis pagal kiekvienai prekei priskirtą atsargų modelį, reikia atlikti atsargų uždarymo procedūrą.
