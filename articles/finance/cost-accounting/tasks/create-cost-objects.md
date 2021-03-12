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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990772"
---
# <a name="create-cost-objects"></a><span data-ttu-id="a1b1d-103">Išlaidų objektų kūrimas  </span><span class="sxs-lookup"><span data-stu-id="a1b1d-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1b1d-104">Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="a1b1d-105">Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="a1b1d-106">Naujų išlaidų objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="a1b1d-106">Create new cost objects</span></span>
1. <span data-ttu-id="a1b1d-107">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų objekto dimensijos.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="a1b1d-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-108">Click New.</span></span>
3. <span data-ttu-id="a1b1d-109">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a1b1d-110">Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="a1b1d-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a1b1d-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="a1b1d-113">Duomenų jungties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a1b1d-113">Configure the data connector</span></span>
1. <span data-ttu-id="a1b1d-114">Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="a1b1d-115">Pasirinkite CostCenter, norėdami importuoti CostCenter dimensiją į kaštų apskaitą.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="a1b1d-116">Lauke Dimensijos pavadinimas pasirinkite Išlaidų centras.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="a1b1d-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="a1b1d-118">Importuoti išlaidų centrus</span><span class="sxs-lookup"><span data-stu-id="a1b1d-118">Import cost centers</span></span>
1. <span data-ttu-id="a1b1d-119">Spustelėkite Importuoti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="a1b1d-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="a1b1d-121">Importuotų išlaidų centrų peržiūra</span><span class="sxs-lookup"><span data-stu-id="a1b1d-121">View the imported cost centers</span></span>
1. <span data-ttu-id="a1b1d-122">Spustelėkite Peržiūrėti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="a1b1d-122">Click View dimension members.</span></span>

