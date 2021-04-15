---
title: 'Išlaidų objektų kūrimas  '
description: Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810059"
---
# <a name="create-cost-objects"></a><span data-ttu-id="b40e7-103">Išlaidų objektų kūrimas  </span><span class="sxs-lookup"><span data-stu-id="b40e7-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b40e7-104">Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant išlaidų centro finansinę dimensiją į kaštų apskaitą per duomenų jungtį.</span><span class="sxs-lookup"><span data-stu-id="b40e7-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="b40e7-105">Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="b40e7-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="b40e7-106">Naujų išlaidų objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="b40e7-106">Create new cost objects</span></span>
1. <span data-ttu-id="b40e7-107">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų objekto dimensijos.</span><span class="sxs-lookup"><span data-stu-id="b40e7-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="b40e7-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b40e7-108">Click New.</span></span>
3. <span data-ttu-id="b40e7-109">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b40e7-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b40e7-110">Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b40e7-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="b40e7-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b40e7-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b40e7-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b40e7-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="b40e7-113">Duomenų jungties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b40e7-113">Configure the data connector</span></span>
1. <span data-ttu-id="b40e7-114">Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="b40e7-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="b40e7-115">Pasirinkite CostCenter, norėdami importuoti CostCenter dimensiją į kaštų apskaitą.</span><span class="sxs-lookup"><span data-stu-id="b40e7-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="b40e7-116">Lauke Dimensijos pavadinimas pasirinkite Išlaidų centras.</span><span class="sxs-lookup"><span data-stu-id="b40e7-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="b40e7-117">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b40e7-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="b40e7-118">Importuoti išlaidų centrus</span><span class="sxs-lookup"><span data-stu-id="b40e7-118">Import cost centers</span></span>
1. <span data-ttu-id="b40e7-119">Spustelėkite Importuoti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="b40e7-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="b40e7-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="b40e7-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="b40e7-121">Importuotų išlaidų centrų peržiūra</span><span class="sxs-lookup"><span data-stu-id="b40e7-121">View the imported cost centers</span></span>
1. <span data-ttu-id="b40e7-122">Spustelėkite Peržiūrėti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="b40e7-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]