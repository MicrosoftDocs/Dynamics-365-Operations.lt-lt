---
title: Grynųjų pinigų srautų prognozavimo įjungimas
description: Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b5e54772b132b4098df8259e954a484a0838ee38
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386716"
---
# <a name="enable-cash-flow-forecasting"></a>Grynųjų pinigų srautų prognozavimo įjungimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.

> [!NOTE]
> Norėdami grynųjų pinigų sraute naudoti mokėjimo prognozes, turite nustatyti funkciją Kliento mokėjimo prognozės, kaip aprašyta temoje [Kliento mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md).

1. Naudokite informaciją iš aplinkos puslapio portale „Microsoft Dynamics Lifecycle Services“ (LCS), kad prisijungtumėte prie pirminio „Azure SQL“ tos aplinkos egzemplioriaus. Norėdami įjungti smėlio dėžės aplinkos testus, vykdykite tolesnę Transact-SQL (T-SQL) komandą. (Gali reikėti įjungti prieigą prie savo IP adreso portale LCS, kad galėtumėte nuotoliniu būdu prisijungti prie programos objektų serverio \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Praleiskite šį veiksmą, jei naudojate 10.0.20 ar vėlesnę versiją arba jei naudojate „Service Fabric“ diegimą. Modulio „Finance Insights” komanda jums jau turėjo įjungti testą. Jei nematote funkcijos darbo srityje **Funkcijų valdymas** arba jei kyla problemų bandant ją įjungti, kreipkitės adresu <fiap@microsoft.com>.
  
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
