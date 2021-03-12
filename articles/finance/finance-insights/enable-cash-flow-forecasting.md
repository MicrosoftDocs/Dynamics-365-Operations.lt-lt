---
title: Grynųjų pinigų srautų prognozavimo įjungimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 1977dac4a3ab66cca2248dc0124d3a06d6963f40
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978769"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Grynųjų pinigų srautų prognozavimo įjungimas (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.

> [!NOTE]
> Norėdami grynųjų pinigų sraute naudoti mokėjimo prognozes, turite nustatyti funkciją Kliento mokėjimo prognozės, kaip aprašyta temoje [Kliento mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md).

1. Naudokite informaciją iš aplinkos puslapio portale „Microsoft Dynamics Lifecycle Services“ (LCS), kad prisijungtumėte prie pirminio „Azure SQL“ tos aplinkos egzemplioriaus. Norėdami įjungti smėlio dėžės aplinkos testus, vykdykite tolesnę Transact-SQL (T-SQL) komandą. (Gali reikėti įjungti prieigą prie savo IP adreso portale LCS, kad galėtumėte nuotoliniu būdu prisijungti prie programos objektų serverio \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Jei jūsų „Microsoft Dynamics 365 Finance“ įdiegtis yra „Service Fabric“ įdiegtis, galite praleisti šį veiksmą. Modulio Finansinės įžvalgos komanda jums jau turėjo įjungti testą. Jei nematote funkcijų darbo srityje **Funkcijų valdymas** arba jei kyla problemų bandant jas įjungti, kreipkitės adresu <fiap@microsoft.com>.
  
2. Atidarykite darbo sritį **Funkcijų valdymas** ir atlikite tolesnius veiksmus.

    1. Pasirinkite **Tikrinti, ar yra naujinimų**.
    2. Įjunkite tolesnes funkcijas.

        - Naujas tinklelio valdiklis
        - Grupavimas tinklelyje (peržiūros versija) 
        - Klientų mokėjimų numatymai (peržiūros versija)
        - Grynųjų pinigų srauto prognozės (peržiūros versija)

3. Eikite į **Grynųjų pinigų ir banko valdymas \> Grynųjų pinigų srautų prognozių sąranka** ir įtraukite likvidumo sąskaitas, kurios turi būti įtrauktos į prognozes.

    > [!NOTE]
    > Jei likvidumo sąskaitos nenustatytos, grynųjų pinigų srauto sugeneruoti negalima.

4. Eikite į **Grynųjų pinigų ir banko valdymas \> Sąranka \> Finansinės įžvalgos (peržiūros versija) \> Grynųjų pinigų srautų prognozes (peržiūros versija)** ir atlikite tolesnius veiksmus.

    1. Skirtuke **Grynųjų pinigų srautų prognozė** pasirinkite **Įjungti funkciją**.
    2. Pasirinkite **Sukurti prognozavimo modelį**.

Daugiau informacijos apie grynųjų pinigų srautų prognozavimo galimybę žr. [Grynųjų pinigų srautų prognozavimas](cash-flow-forecast-intro.md).

## <a name="privacy-notice"></a>Privatumo pranešimas

Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.
