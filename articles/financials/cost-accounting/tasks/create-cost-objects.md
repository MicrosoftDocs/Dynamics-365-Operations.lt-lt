--- 
title: "Išlaidų objektų kūrimas  "
description: "Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo išlaidų centro finansinę dimensiją į savikainos apskaitą per duomenų jungtį."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d43274aed2edbb91fd4e399cb8d45e91646b055
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-objects"></a><span data-ttu-id="0eeb4-103">Išlaidų objektų kūrimas  </span><span class="sxs-lookup"><span data-stu-id="0eeb4-103">Create cost objects</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0eeb4-104">Šioje procedūroje parodoma, kaip kurti išlaidų objektus importuojant „Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo išlaidų centro finansinę dimensiją į savikainos apskaitą per duomenų jungtį.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="0eeb4-105">Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="0eeb4-106">Ši procedūra yra skirta kaštų apskaitos funkcijai, įtrauktai į „Microsoft Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="0eeb4-107">Naujų išlaidų objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="0eeb4-107">Create new cost objects</span></span>
1. <span data-ttu-id="0eeb4-108">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų objekto dimensijos.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="0eeb4-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-109">Click New.</span></span>
3. <span data-ttu-id="0eeb4-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0eeb4-111">Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="0eeb4-112">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="0eeb4-113">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="0eeb4-114">Duomenų jungties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0eeb4-114">Configure the data connector</span></span>
1. <span data-ttu-id="0eeb4-115">Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="0eeb4-116">Pasirinkite CostCenter, norėdami importuoti CostCenter dimensiją į kaštų apskaitą.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="0eeb4-117">Lauke Dimensijos pavadinimas pasirinkite Išlaidų centras.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="0eeb4-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="0eeb4-119">Importuoti išlaidų centrus</span><span class="sxs-lookup"><span data-stu-id="0eeb4-119">Import cost centers</span></span>
1. <span data-ttu-id="0eeb4-120">Spustelėkite Importuoti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="0eeb4-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="0eeb4-122">Importuotų išlaidų centrų peržiūra</span><span class="sxs-lookup"><span data-stu-id="0eeb4-122">View the imported cost centers</span></span>
1. <span data-ttu-id="0eeb4-123">Spustelėkite Peržiūrėti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="0eeb4-123">Click View dimension members.</span></span>


