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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f5f6e5048f70e744cb3dc82a2a279aae69b4af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446128"
---
# <a name="create-cost-objects"></a><span data-ttu-id="e3e2b-103">Išlaidų objektų kūrimas  </span><span class="sxs-lookup"><span data-stu-id="e3e2b-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3e2b-104">Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="e3e2b-105">Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="e3e2b-106">Naujų išlaidų objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="e3e2b-106">Create new cost objects</span></span>
1. <span data-ttu-id="e3e2b-107">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų objekto dimensijos.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="e3e2b-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-108">Click New.</span></span>
3. <span data-ttu-id="e3e2b-109">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e3e2b-110">Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="e3e2b-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e3e2b-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="e3e2b-113">Duomenų jungties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e3e2b-113">Configure the data connector</span></span>
1. <span data-ttu-id="e3e2b-114">Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="e3e2b-115">Pasirinkite CostCenter, norėdami importuoti CostCenter dimensiją į kaštų apskaitą.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="e3e2b-116">Lauke Dimensijos pavadinimas pasirinkite Išlaidų centras.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="e3e2b-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="e3e2b-118">Importuoti išlaidų centrus</span><span class="sxs-lookup"><span data-stu-id="e3e2b-118">Import cost centers</span></span>
1. <span data-ttu-id="e3e2b-119">Spustelėkite Importuoti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="e3e2b-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="e3e2b-121">Importuotų išlaidų centrų peržiūra</span><span class="sxs-lookup"><span data-stu-id="e3e2b-121">View the imported cost centers</span></span>
1. <span data-ttu-id="e3e2b-122">Spustelėkite Peržiūrėti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="e3e2b-122">Click View dimension members.</span></span>

