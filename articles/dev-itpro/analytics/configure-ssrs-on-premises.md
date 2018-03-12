---
title: "„SQL Server Reporting Services“ konfigūravimas vietiniam diegimui"
description: "Šioje temoje pateikiama informacija apie „SQL Server Reporting Services“ (SSRS) konfigūravimą vietiniam diegimui."
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: 2b5abc98f5788c5091e5be61688cfd0d4076a510
ms.contentlocale: lt-lt
ms.lasthandoff: 03/09/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="f573e-103">„SQL Server Reporting Services“ konfigūravimas vietiniam diegimui</span><span class="sxs-lookup"><span data-stu-id="f573e-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f573e-104">Atlikę šioje temoje nurodytus veiksmus, konfigūruokite „SQL Server Reporting Services“ (SSRS), skirtas „Microsoft Dynamics 365 for Finance and Operations“, („Enterprise“ leidimo (vietinės versijos)) diegimui.</span><span class="sxs-lookup"><span data-stu-id="f573e-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) deployment.</span></span>

1. <span data-ttu-id="f573e-105">Atidarykite ataskaitų serverio konfigūravimo tvarkytuvo programą.</span><span class="sxs-lookup"><span data-stu-id="f573e-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="f573e-106">Palikite numatytąjį **serverio pavadinimą**, kuris turėtų būti dabartinio įrenginio pavadinimas, taip pat **ataskaitų serverio egzempliorių**, **MSSQLSERVER**.</span><span class="sxs-lookup"><span data-stu-id="f573e-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="f573e-107">Spustelėkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="f573e-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="f573e-108">[![Prisijungimas prie ataskaitų serverio konfigūravimo](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="f573e-109">Spustelėkite skirtuką **Tarnybos sąskaita** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f573e-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="f573e-110">[![Skirtukas Tarnybos sąskaitos](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="f573e-111">Spustelėkite skirtuką **Tinklo tarnybos URL** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f573e-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="f573e-112">[![Skirtukas Žiniatinklio tarnybos URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="f573e-113">Spustelėkite skirtuką **Duomenų bazė** ir patikrinkite, ar **Duomenų bazės pavadinimas** ir **Kredencialų parametrai** atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f573e-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="f573e-114">**Pastaba:** Turėsite susikurti naują duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="f573e-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="f573e-115">Norėdami tai atlikti, spustelėkite **Keisti duomenų bazę**, tada patikrinkite, ar naujos duomenų bazės pavadinimas yra **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="f573e-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="f573e-116">[![duomenų bazės skirtukas](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="f573e-117">Spustelėkite skirtuką **Tinklo portalo URL** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f573e-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="f573e-118">**Pastaba.** Norėdami sukurti ir tinkamai sukonfigūruoti portalą, turite spustelėti **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="f573e-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="f573e-119">[![skirtukas tinklo portalo url](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
  <span data-ttu-id="f573e-120">Sukonfigūravus portalą skirtuko **Tinklo portalas** vaizdas atitiks toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f573e-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="f573e-121">[![skirtukas tinklo portalas](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="f573e-122">Norėdami peržiūrėti „SQL Server Reporting Services“ tinklo portalą, spustelėkite ataskaitų URL.</span><span class="sxs-lookup"><span data-stu-id="f573e-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9.  <span data-ttu-id="f573e-123">Įėję į portalą sukurkite naują aplanką, pavadinimu **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="f573e-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="f573e-124">[![aplankas „Dynamics“](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="f573e-125">Srityje **Ataskaitų serverio konfigūravimo tvarkytuvas** spustelėkite skirtuką **El. pašto parametrai** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f573e-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="f573e-126">[![skirtukas el. pašto parametrai](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="f573e-127">Spustelėkite skirtuką **Vykdymo sąskaita** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f573e-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="f573e-128">[![skirtukas vykdymo sąskaita](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
  <span data-ttu-id="f573e-129">Nekeiskite numatytųjų parametrų skirtuke **Šifravimo raktai**. [![šifravimo raktų skirtukas](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="f573e-130">Spustelėkite skirtuką **Abonemento parametrai** ir patikrinkite, ar parametrai atitinka toliau pateiktą grafinį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="f573e-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="f573e-131">[![skirtukas abonementų parametrai](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
  <span data-ttu-id="f573e-132">Nekeiskite numatytųjų parametrų skirtuke **Skalės sudarymas**. [![skalės sudarymo skirtukas](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
  <span data-ttu-id="f573e-133">Nekeiskite numatytųjų parametrų skirtuke **„Power BI“ integravimas**. [![„power bi“ integravimo skirtukas](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="f573e-134">Spustelėkite **Išeiti**, kad uždarytumėte **ataskaitų serverio konfigūravimo tvarkytuvą**.</span><span class="sxs-lookup"><span data-stu-id="f573e-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="f573e-135">[![ataskaitų serverio konfigūravimo tvarkytuvo uždarymas](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="f573e-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


