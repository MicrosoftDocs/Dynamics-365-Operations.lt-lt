---
title: "Finansinių dimensijų įtraukimas į CFO darbo sritį"
description: "Šioje temoje paaiškinama, kaip įtraukti finansines dimensijas į CFO darbo sritį, kad būtų galima jas naudoti DK ir biudžeto ataskaitose."
author: aprilolson
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
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e674948f642ab7525f96092a9a1f3adaae66974
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="82815-103">Finansinių dimensijų įtraukimas į CFO darbo sritį</span><span class="sxs-lookup"><span data-stu-id="82815-103">Add financial dimensions to the CFO workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82815-104">Šioje temoje paaiškinama, kaip įtraukti finansines dimensijas į vyriausiojo finansininko (CFO) darbo sritį, kad būtų galima jas naudoti DK ir biudžeto ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="82815-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="82815-105">CFO darbo srityje yra skirtukai **Apžvalga** ir **Finansin.**. Ataskaitos šiuose dviejuose skirtukuose pagrįstos dviem priemonėmis: LedgerActivityMeasure ir BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="82815-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="82815-106">Naudojant „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.), yra sąsaja tarp tų dviejų priemonių ir objekto DimensionCombinationEntity.</span><span class="sxs-lookup"><span data-stu-id="82815-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="82815-107">Todėl galima pasirinkti dimensijas.</span><span class="sxs-lookup"><span data-stu-id="82815-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="82815-108">Naudojant „Finance and Operations“, puslapyje **Objekto parduotuvė** atnaujinkite priemonę **LedgerActivityMeasure** ir **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="82815-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="82815-109">Naudojant „Microsoft Visual Studio“, atidarykite programų naršymo priemonę ir ieškokite **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="82815-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="82815-110">Srityje **Ištekliai** atidarykite **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="82815-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="82815-111">Kai bus atidarytas išteklius „Microsoft Power BI“ darbalaukyje, pasirinkite **Gauti duomenis**, pasirinkite **SQL serverio duomenų bazė** tada pasirinkite **Jungtis**.</span><span class="sxs-lookup"><span data-stu-id="82815-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="82815-112">Įveskite serverio vardą, tada įveskite **AxDW** kaip duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="82815-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="82815-113">Pasirinkite **DirectQuery**, tada pasirinkite **OK**.</span><span class="sxs-lookup"><span data-stu-id="82815-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="82815-114">Raskite ir pasirinkite **LedgerActivityMeasure\_DimensionCombination**, tada pasirinkite **Load**.</span><span class="sxs-lookup"><span data-stu-id="82815-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="82815-115">Sąraše **Laukai** pakeiskite lentelės **Finansinės dimensijos** pavadinimą, kad ją būtų paprasta identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="82815-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="82815-116">Pasirinkite **Valdyti ryšius**, tada pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="82815-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="82815-117">Pirmame lauke pasirinkite **Didžiosios knygos veiklos**, tada pasirinkite **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="82815-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="82815-118">Antrame lauke pasirinkite **LedgerActivityMeasure\_DimensionCombination** (arba **Finansinės dimensijos**, jei pervardijote lentelę).</span><span class="sxs-lookup"><span data-stu-id="82815-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="82815-119">Pasirinkite antraštę **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="82815-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="82815-120">Lauke **Svarba** pasirinkite **Daugelis su vienu**.</span><span class="sxs-lookup"><span data-stu-id="82815-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="82815-121">Pakeiskite reikšmę **Kelių filtrų kryptys** į **Viena**.</span><span class="sxs-lookup"><span data-stu-id="82815-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="82815-122">Pasirinkite **Suaktyvinti šį ryšį** ir **Naudoti nurodomąjį integralumą**, pasirinkite **Gerai**, tada pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="82815-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="82815-123">[![Ryšio kūrimas](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="82815-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="82815-124">Sąraše **Laukai** turėtų būti rodoma lentelė ir pasiekiamos finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="82815-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="82815-125">Vilkite norimas finansines dimensijas į ataskaitų lygio filtrus.</span><span class="sxs-lookup"><span data-stu-id="82815-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="82815-126">Įrašykite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="82815-126">Save your changes.</span></span>
15. <span data-ttu-id="82815-127">Programos objektų medyje (AOT) dešiniuoju pelės mygtuku spustelėkite projektą, tada pasirinkite **Sinchronizuoti**.</span><span class="sxs-lookup"><span data-stu-id="82815-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="82815-128">Sukurkite projektą, tada atidarykite programą, kad peržiūrėtumėte rezultatus.</span><span class="sxs-lookup"><span data-stu-id="82815-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="82815-129">[![Baigta darbo sritis](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="82815-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

