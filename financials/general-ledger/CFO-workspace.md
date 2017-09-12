---
title: "Finansinių dimensijų įtraukimas į CFO darbo sritį"
description: "Šioje temoje paaiškinama, kaip įtraukti finansines dimensijas į CFO darbo sritį, kad būtų galima jas naudoti DK ir biudžeto ataskaitose."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: lt-lt
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="f9741-103">Finansinių dimensijų įtraukimas į CFO darbo sritį</span><span class="sxs-lookup"><span data-stu-id="f9741-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f9741-104">Šioje temoje paaiškinama, kaip įtraukti finansines dimensijas į vyriausiojo finansininko (CFO) darbo sritį, kad būtų galima jas naudoti DK ir biudžeto ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="f9741-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="f9741-105">CFO darbo sritis turi skirtuką **Peržiūra** ir skirtuką **Finansinis**.</span><span class="sxs-lookup"><span data-stu-id="f9741-105">The CFO workspace has an **Overview** tab and a **Financial** tab.</span></span> <span data-ttu-id="f9741-106">Ataskaitos šiuose dviejuose skirtukuose pagrįstos dviem priemonėm: LedgerActivityMeasure ir BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="f9741-106">The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="f9741-107">Naudojant „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo 2017 liepos mėn. naujinimą, yra sąsaja tarp tų dviejų priemonių ir „DimensionCombinationEntity“ objekto.</span><span class="sxs-lookup"><span data-stu-id="f9741-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="f9741-108">Todėl galima pasirinkti dimensijas.</span><span class="sxs-lookup"><span data-stu-id="f9741-108">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="f9741-109">Naudojant „Finance and Operations“, puslapyje **Objekto parduotuvė** atnaujinkite priemonę **LedgerActivityMeasure** ir **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="f9741-109">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="f9741-110">Naudojant „Microsoft Visual Studio“, atidarykite programų naršymo priemonę ir ieškokite **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="f9741-110">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="f9741-111">Srityje **Ištekliai** atidarykite **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="f9741-111">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="f9741-112">Kai bus atidarytas išteklius „Microsoft Power BI“ darbalaukyje, pasirinkite **Gauti duomenis**, pasirinkite **SQL serverio duomenų bazė** tada pasirinkite **Jungtis**.</span><span class="sxs-lookup"><span data-stu-id="f9741-112">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="f9741-113">Įveskite serverio vardą, tada įveskite **AxDW** kaip duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="f9741-113">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="f9741-114">Pasirinkite **DirectQuery**, tada pasirinkite **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9741-114">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="f9741-115">Raskite ir pasirinkite **LedgerActivityMeasure\_DimensionCombination**, tada pasirinkite **Load**.</span><span class="sxs-lookup"><span data-stu-id="f9741-115">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="f9741-116">Sąraše **Laukai** pakeiskite lentelės **Finansinės dimensijos** pavadinimą, kad ją būtų paprasta identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="f9741-116">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="f9741-117">Pasirinkite **Valdyti ryšius**, tada pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f9741-117">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="f9741-118">Pirmame lauke pasirinkite **Didžiosios knygos veiklos**, tada pasirinkite **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="f9741-118">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="f9741-119">Antrame lauke pasirinkite **LedgerActivityMeasure\_DimensionCombination** (arba **Finansinės dimensijos**, jei pervardijote lentelę).</span><span class="sxs-lookup"><span data-stu-id="f9741-119">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="f9741-120">Pasirinkite antraštę **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="f9741-120">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="f9741-121">Lauke **Svarba** pasirinkite **Daugelis su vienu**.</span><span class="sxs-lookup"><span data-stu-id="f9741-121">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="f9741-122">Pakeiskite reikšmę **Kelių filtrų kryptys** į **Viena**.</span><span class="sxs-lookup"><span data-stu-id="f9741-122">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="f9741-123">Pasirinkite **Suaktyvinti šį ryšį** ir **Naudoti nurodomąjį integralumą**, pasirinkite **Gerai**, tada pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="f9741-123">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="f9741-124">[![Ryšio kūrimas](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="f9741-124">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="f9741-125">Sąraše **Laukai** turėtų būti rodoma lentelė ir pasiekiamos finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="f9741-125">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="f9741-126">Vilkite norimas finansines dimensijas į ataskaitų lygio filtrus.</span><span class="sxs-lookup"><span data-stu-id="f9741-126">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="f9741-127">Įrašykite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="f9741-127">Save your changes.</span></span>
15. <span data-ttu-id="f9741-128">Programos objektų medyje (AOT) dešiniuoju pelės mygtuku spustelėkite projektą, tada pasirinkite **Sinchronizuoti**.</span><span class="sxs-lookup"><span data-stu-id="f9741-128">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="f9741-129">Sukurkite projektą, tada atidarykite programą, kad peržiūrėtumėte rezultatus.</span><span class="sxs-lookup"><span data-stu-id="f9741-129">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="f9741-130">[![Baigta darbo sritis](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="f9741-130">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

