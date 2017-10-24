--- 
title: "Išlaidų elementų kūrimas  "
description: "Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais."
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
ms.openlocfilehash: 1e665fc53455e457a2488f4ec28ebb5b715d90eb
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-cost-elements"></a><span data-ttu-id="94c2a-103">Išlaidų elementų kūrimas  </span><span class="sxs-lookup"><span data-stu-id="94c2a-103">Create cost elements</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="94c2a-104">Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="94c2a-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="94c2a-105">Šioje procedūroje parodoma, kaip kurti išlaidų elementus importuojant pagrindines sąskaitas per duomenų jungtį.</span><span class="sxs-lookup"><span data-stu-id="94c2a-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="94c2a-106">Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="94c2a-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="94c2a-107">Ši procedūra yra skirta kaštų apskaitos funkcijai, įtrauktai į „Microsoft Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="94c2a-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="94c2a-108">Naujų išlaidų elementų kūrimas</span><span class="sxs-lookup"><span data-stu-id="94c2a-108">Create new cost elements</span></span>
1. <span data-ttu-id="94c2a-109">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų elemento dimensijos.</span><span class="sxs-lookup"><span data-stu-id="94c2a-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="94c2a-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="94c2a-110">Click New.</span></span>
3. <span data-ttu-id="94c2a-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94c2a-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="94c2a-112">Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94c2a-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="94c2a-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94c2a-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="94c2a-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="94c2a-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="94c2a-115">Duomenų jungties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="94c2a-115">Configure the data connector</span></span>
1. <span data-ttu-id="94c2a-116">Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="94c2a-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="94c2a-117">Lauke Sąskaitų planas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94c2a-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="94c2a-118">Pasirinkite Bendrai naudojamas, norėdami naudoti bendrai naudojamą sąskaitų planą.</span><span class="sxs-lookup"><span data-stu-id="94c2a-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="94c2a-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="94c2a-119">Click New.</span></span>
4. <span data-ttu-id="94c2a-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="94c2a-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="94c2a-121">Taikydami sąskaitų filtrus galite nustatyti savo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="94c2a-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="94c2a-122">Lauke Iš pagrindinės sąskaitos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94c2a-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="94c2a-123">Lauke Į pagrindinę sąskaitą įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="94c2a-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="94c2a-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="94c2a-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="94c2a-125">Importuoti pagrindines sąskaitas</span><span class="sxs-lookup"><span data-stu-id="94c2a-125">Import main accounts</span></span>
1. <span data-ttu-id="94c2a-126">Spustelėkite Importuoti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="94c2a-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="94c2a-127">Pagrindinės sąskaitos bus importuotos į savikainos apskaitą ir naudojamos kaip savikainos elementai.</span><span class="sxs-lookup"><span data-stu-id="94c2a-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="94c2a-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="94c2a-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="94c2a-129">Peržiūrėkite importuotas sąskaitas kaip išlaidų elementus</span><span class="sxs-lookup"><span data-stu-id="94c2a-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="94c2a-130">Spustelėkite Peržiūrėti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="94c2a-130">Click View dimension members.</span></span>
    * <span data-ttu-id="94c2a-131">Peržiūrėkite importuotas DK sąskaitas kaip savo verslo išlaidų elementus, į kuriuos galima perkelti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="94c2a-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  


