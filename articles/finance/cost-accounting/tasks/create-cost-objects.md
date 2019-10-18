---
title: 'Išlaidų objektų kūrimas  '
description: Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2616e5275f9f59b962d4e456684073aea2c654ea
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249683"
---
# <a name="create-cost-objects"></a><span data-ttu-id="90c24-103">Išlaidų objektų kūrimas  </span><span class="sxs-lookup"><span data-stu-id="90c24-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90c24-104">Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.</span><span class="sxs-lookup"><span data-stu-id="90c24-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="90c24-105">Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="90c24-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="90c24-106">Naujų išlaidų objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="90c24-106">Create new cost objects</span></span>
1. <span data-ttu-id="90c24-107">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų objekto dimensijos.</span><span class="sxs-lookup"><span data-stu-id="90c24-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="90c24-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="90c24-108">Click New.</span></span>
3. <span data-ttu-id="90c24-109">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="90c24-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="90c24-110">Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="90c24-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="90c24-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="90c24-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="90c24-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="90c24-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="90c24-113">Duomenų jungties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="90c24-113">Configure the data connector</span></span>
1. <span data-ttu-id="90c24-114">Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="90c24-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="90c24-115">Pasirinkite CostCenter, norėdami importuoti CostCenter dimensiją į kaštų apskaitą.</span><span class="sxs-lookup"><span data-stu-id="90c24-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="90c24-116">Lauke Dimensijos pavadinimas pasirinkite Išlaidų centras.</span><span class="sxs-lookup"><span data-stu-id="90c24-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="90c24-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="90c24-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="90c24-118">Importuoti išlaidų centrus</span><span class="sxs-lookup"><span data-stu-id="90c24-118">Import cost centers</span></span>
1. <span data-ttu-id="90c24-119">Spustelėkite Importuoti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="90c24-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="90c24-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="90c24-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="90c24-121">Importuotų išlaidų centrų peržiūra</span><span class="sxs-lookup"><span data-stu-id="90c24-121">View the imported cost centers</span></span>
1. <span data-ttu-id="90c24-122">Spustelėkite Peržiūrėti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="90c24-122">Click View dimension members.</span></span>

