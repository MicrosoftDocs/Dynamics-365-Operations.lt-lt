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
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="1c4b4-103">„SQL Server Reporting Services“ konfigūravimas vietiniams diegimams</span><span class="sxs-lookup"><span data-stu-id="1c4b4-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c4b4-104">Atlikę šioje temoje nurodytus veiksmus, konfigūruokite „SQL Server Reporting Services“ (SSRS), skirtas „Microsoft Dynamics 365 Finance“ ir „Operations” (vietinė versija) diegti.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="1c4b4-105">Atidarykite ataskaitų serverio konfigūravimo tvarkytuvo programą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="1c4b4-106">Palikite numatytąjį **serverio pavadinimą**, kuris turėtų būti dabartinio įrenginio pavadinimas, taip pat **ataskaitų serverio egzempliorių**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="1c4b4-107">Spustelėkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-107">Click **Connect**.</span></span>

    <span data-ttu-id="1c4b4-108">[![Prisijungimas prie ataskaitų serverio konfigūravimo](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="1c4b4-109">Spustelėkite skirtuką **Tarnybos sąskaita** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="1c4b4-110">[![Skirtukas Tarnybos sąskaitos](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="1c4b4-111">Spustelėkite skirtuką **Tinklo tarnybos URL** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="1c4b4-112">[![Skirtukas Žiniatinklio tarnybos URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="1c4b4-113">Spustelėkite skirtuką **Duomenų bazė** ir patikrinkite, ar **Duomenų bazės pavadinimas** ir **Kredencialų parametrai** atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1c4b4-114">Turėsite susikurti naują duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-114">You will need to create a new database.</span></span> <span data-ttu-id="1c4b4-115">Norėdami tai atlikti, spustelėkite **Keisti duomenų bazę**, tada patikrinkite, ar naujos duomenų bazės pavadinimas yra **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="1c4b4-116">[![duomenų bazės skirtukas](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="1c4b4-117">Spustelėkite skirtuką **Tinklo portalo URL** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1c4b4-118">Norėdami sukurti ir tinkamai sukonfigūruoti portalą, turite spustelėti **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="1c4b4-119">[![skirtukas tinklo portalo url](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="1c4b4-120">Sukonfigūravus portalą skirtuko **Tinklo portalas** vaizdas atitiks toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="1c4b4-121">[![skirtukas tinklo portalas](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="1c4b4-122">Norėdami peržiūrėti „SQL Server Reporting Services“ tinklo portalą, spustelėkite ataskaitų URL.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="1c4b4-123">Įėję į portalą sukurkite naują aplanką, pavadinimu **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="1c4b4-124">[![aplankas „Dynamics“](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="1c4b4-125">Srityje **Ataskaitų serverio konfigūravimo tvarkytuvas** spustelėkite skirtuką **El. pašto parametrai** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="1c4b4-126">[![skirtukas el. pašto parametrai](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="1c4b4-127">Spustelėkite skirtuką **Vykdymo sąskaita** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="1c4b4-128">[![skirtukas vykdymo sąskaita](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="1c4b4-129">Nekeiskite numatytųjų parametrų skirtuke **Šifravimo raktai**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="1c4b4-130">[![skirtukas šifravimo raktai](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="1c4b4-131">Spustelėkite skirtuką **Abonemento parametrai** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="1c4b4-132">[![skirtukas abonementų parametrai](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="1c4b4-133">Nekeiskite numatytųjų parametrų skirtuke **Skalės sudarymas**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="1c4b4-134">[![skirtukas skalės sudarymas](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="1c4b4-135">Nekeiskite numatytųjų parametrų skirtuke **„Power BI“ integravimas**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="1c4b4-136">[![skirtukas „Power BI“ integravimas](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="1c4b4-137">Spustelėkite **Išeiti**, kad uždarytumėte **ataskaitų serverio konfigūravimo tvarkytuvą**.</span><span class="sxs-lookup"><span data-stu-id="1c4b4-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="1c4b4-138">[![ataskaitų serverio konfigūravimo tvarkytuvo uždarymas](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="1c4b4-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
