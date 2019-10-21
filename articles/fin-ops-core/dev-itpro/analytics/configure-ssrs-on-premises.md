---
title: „SQL Server Reporting Services“ konfigūravimas vietiniams diegimams
description: Šioje temoje pateikiama informacija apie „SQL Server Reporting Services“ (SSRS) konfigūravimą vietiniam diegimui.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: bb6e8a55c9bee4e60c3a627409d2fbe3b8915196
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174241"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>„SQL Server Reporting Services“ konfigūravimas vietiniams diegimams

[!include [banner](../includes/banner.md)]

Atlikę šioje temoje nurodytus veiksmus, konfigūruokite „SQL Server Reporting Services“ (SSRS), skirtas „Microsoft Dynamics 365 Finance“ ir „Operations” (vietinė versija) diegti.

1. Atidarykite ataskaitų serverio konfigūravimo tvarkytuvo programą.
2. Palikite numatytąjį **serverio pavadinimą**, kuris turėtų būti dabartinio įrenginio pavadinimas, taip pat **ataskaitų serverio egzempliorių**, **MSSQLSERVER**.
3. Spustelėkite **Prisijungti**.

    [![Prisijungimas prie ataskaitų serverio konfigūravimo](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Spustelėkite skirtuką **Tarnybos sąskaita** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.

    [![Skirtukas Tarnybos sąskaitos](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Spustelėkite skirtuką **Tinklo tarnybos URL** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.

    [![Skirtukas Žiniatinklio tarnybos URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Spustelėkite skirtuką **Duomenų bazė** ir patikrinkite, ar **Duomenų bazės pavadinimas** ir **Kredencialų parametrai** atitinka toliau pateiktą grafinį vaizdą.

    > [!NOTE]
    > Turėsite susikurti naują duomenų bazę. Norėdami tai atlikti, spustelėkite **Keisti duomenų bazę**, tada patikrinkite, ar naujos duomenų bazės pavadinimas yra **DynamicsAxReportServer**.

    [![duomenų bazės skirtukas](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Spustelėkite skirtuką **Tinklo portalo URL** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.

    > [!NOTE]
    > Norėdami sukurti ir tinkamai sukonfigūruoti portalą, turite spustelėti **Taikyti**.

    [![skirtukas tinklo portalo url](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Sukonfigūravus portalą skirtuko **Tinklo portalas** vaizdas atitiks toliau pateiktą grafinį vaizdą.

    [![skirtukas tinklo portalas](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Norėdami peržiūrėti „SQL Server Reporting Services“ tinklo portalą, spustelėkite ataskaitų URL.
9. Įėję į portalą sukurkite naują aplanką, pavadinimu **Dynamics**.

    [![aplankas „Dynamics“](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. Srityje **Ataskaitų serverio konfigūravimo tvarkytuvas** spustelėkite skirtuką **El. pašto parametrai** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.

    [![skirtukas el. pašto parametrai](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Spustelėkite skirtuką **Vykdymo sąskaita** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.

    [![skirtukas vykdymo sąskaita](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Nekeiskite numatytųjų parametrų skirtuke **Šifravimo raktai**.

    [![skirtukas šifravimo raktai](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Spustelėkite skirtuką **Abonemento parametrai** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.

    [![skirtukas abonementų parametrai](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Nekeiskite numatytųjų parametrų skirtuke **Skalės sudarymas**.

    [![skirtukas skalės sudarymas](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Nekeiskite numatytųjų parametrų skirtuke **„Power BI“ integravimas**.

    [![skirtukas „Power BI“ integravimas](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Spustelėkite **Išeiti**, kad uždarytumėte **ataskaitų serverio konfigūravimo tvarkytuvą**.

    [![ataskaitų serverio konfigūravimo tvarkytuvo uždarymas](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)