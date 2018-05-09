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
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ebe2766976f2c7a88f9b919c8c13e05e36576e45
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="a6747-103">Finansinių dimensijų įtraukimas į CFO darbo sritį</span><span class="sxs-lookup"><span data-stu-id="a6747-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6747-104">Šioje temoje paaiškinama, kaip įtraukti finansines dimensijas į vyriausiojo finansininko (CFO) darbo sritį, kad būtų galima jas naudoti DK ir biudžeto ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="a6747-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="a6747-105">CFO darbo srityje yra skirtukai **Apžvalga** ir **Finansin.**. Ataskaitos šiuose dviejuose skirtukuose pagrįstos dviem priemonėmis: LedgerActivityMeasure ir BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="a6747-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="a6747-106">Naudojant „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.), yra sąsaja tarp tų dviejų priemonių ir objekto DimensionCombinationEntity.</span><span class="sxs-lookup"><span data-stu-id="a6747-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="a6747-107">Todėl galima pasirinkti dimensijas.</span><span class="sxs-lookup"><span data-stu-id="a6747-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="a6747-108">Naudojant „Finance and Operations“, puslapyje **Objekto parduotuvė** atnaujinkite priemonę **LedgerActivityMeasure** ir **BudgetActivityMeasure**.</span><span class="sxs-lookup"><span data-stu-id="a6747-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="a6747-109">Naudojant „Microsoft Visual Studio“, atidarykite programų naršymo priemonę ir ieškokite **LedgerCFO**.</span><span class="sxs-lookup"><span data-stu-id="a6747-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="a6747-110">Srityje **Ištekliai** atidarykite **LedgerCFOWorkspacePBIX**.</span><span class="sxs-lookup"><span data-stu-id="a6747-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="a6747-111">Kai bus atidarytas išteklius „Microsoft Power BI“ darbalaukyje, pasirinkite **Gauti duomenis**, pasirinkite **SQL serverio duomenų bazė** tada pasirinkite **Jungtis**.</span><span class="sxs-lookup"><span data-stu-id="a6747-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="a6747-112">Įveskite serverio vardą, tada įveskite **AxDW** kaip duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="a6747-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="a6747-113">Pasirinkite **DirectQuery**, tada pasirinkite **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6747-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="a6747-114">Raskite ir pasirinkite **LedgerActivityMeasure\_DimensionCombination**, tada pasirinkite **Load**.</span><span class="sxs-lookup"><span data-stu-id="a6747-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="a6747-115">Sąraše **Laukai** pakeiskite lentelės **Finansinės dimensijos** pavadinimą, kad ją būtų paprasta identifikuoti.</span><span class="sxs-lookup"><span data-stu-id="a6747-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="a6747-116">Pasirinkite **Valdyti ryšius**, tada pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a6747-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="a6747-117">Pirmame lauke pasirinkite **Didžiosios knygos veiklos**, tada pasirinkite **LedgerDimension**.</span><span class="sxs-lookup"><span data-stu-id="a6747-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="a6747-118">Antrame lauke pasirinkite **LedgerActivityMeasure\_DimensionCombination** (arba **Finansinės dimensijos**, jei pervardijote lentelę).</span><span class="sxs-lookup"><span data-stu-id="a6747-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="a6747-119">Pasirinkite antraštę **DimensionCombinationRECID**.</span><span class="sxs-lookup"><span data-stu-id="a6747-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="a6747-120">Lauke **Svarba** pasirinkite **Daugelis su vienu**.</span><span class="sxs-lookup"><span data-stu-id="a6747-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="a6747-121">Pakeiskite reikšmę **Kelių filtrų kryptys** į **Viena**.</span><span class="sxs-lookup"><span data-stu-id="a6747-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="a6747-122">Pasirinkite **Suaktyvinti šį ryšį** ir **Naudoti nurodomąjį integralumą**, pasirinkite **Gerai**, tada pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="a6747-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="a6747-123">[![Ryšio kūrimas](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="a6747-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="a6747-124">Sąraše **Laukai** turėtų būti rodoma lentelė ir pasiekiamos finansinės dimensijos.</span><span class="sxs-lookup"><span data-stu-id="a6747-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="a6747-125">Vilkite norimas finansines dimensijas į ataskaitų lygio filtrus.</span><span class="sxs-lookup"><span data-stu-id="a6747-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="a6747-126">Įrašykite pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="a6747-126">Save your changes.</span></span>
15. <span data-ttu-id="a6747-127">Programos objektų medyje (AOT) dešiniuoju pelės mygtuku spustelėkite projektą, tada pasirinkite **Sinchronizuoti**.</span><span class="sxs-lookup"><span data-stu-id="a6747-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="a6747-128">Sukurkite projektą, tada atidarykite programą, kad peržiūrėtumėte rezultatus.</span><span class="sxs-lookup"><span data-stu-id="a6747-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="a6747-129">[![Baigta darbo sritis](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="a6747-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>

