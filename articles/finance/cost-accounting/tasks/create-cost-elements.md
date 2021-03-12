---
title: 'Išlaidų elementų kūrimas  '
description: Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f58b6896dd5b9e257bf6066e56142dcd2d8fb45
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990797"
---
# <a name="create-cost-elements"></a><span data-ttu-id="2116a-103">Išlaidų elementų kūrimas  </span><span class="sxs-lookup"><span data-stu-id="2116a-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2116a-104">Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="2116a-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="2116a-105">Šioje procedūroje parodoma, kaip kurti išlaidų elementus importuojant pagrindines sąskaitas per duomenų jungtį.</span><span class="sxs-lookup"><span data-stu-id="2116a-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="2116a-106">Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="2116a-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="2116a-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai kaštų apskaitos funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="2116a-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="2116a-108">Naujų išlaidų elementų kūrimas</span><span class="sxs-lookup"><span data-stu-id="2116a-108">Create new cost elements</span></span>
1. <span data-ttu-id="2116a-109">Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų elemento dimensijos.</span><span class="sxs-lookup"><span data-stu-id="2116a-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="2116a-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2116a-110">Click New.</span></span>
3. <span data-ttu-id="2116a-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2116a-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2116a-112">Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2116a-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="2116a-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2116a-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="2116a-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2116a-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="2116a-115">Duomenų jungties konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="2116a-115">Configure the data connector</span></span>
1. <span data-ttu-id="2116a-116">Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="2116a-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="2116a-117">Lauke Sąskaitų planas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2116a-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="2116a-118">Pasirinkite Bendrai naudojamas, norėdami naudoti bendrai naudojamą sąskaitų planą.</span><span class="sxs-lookup"><span data-stu-id="2116a-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="2116a-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2116a-119">Click New.</span></span>
4. <span data-ttu-id="2116a-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="2116a-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2116a-121">Taikydami sąskaitų filtrus galite nustatyti savo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="2116a-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="2116a-122">Lauke Iš pagrindinės sąskaitos įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2116a-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="2116a-123">Lauke Į pagrindinę sąskaitą įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2116a-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="2116a-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="2116a-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="2116a-125">Importuoti pagrindines sąskaitas</span><span class="sxs-lookup"><span data-stu-id="2116a-125">Import main accounts</span></span>
1. <span data-ttu-id="2116a-126">Spustelėkite Importuoti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="2116a-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="2116a-127">Pagrindinės sąskaitos bus importuotos į savikainos apskaitą ir naudojamos kaip savikainos elementai.</span><span class="sxs-lookup"><span data-stu-id="2116a-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="2116a-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="2116a-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="2116a-129">Peržiūrėkite importuotas sąskaitas kaip išlaidų elementus</span><span class="sxs-lookup"><span data-stu-id="2116a-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="2116a-130">Spustelėkite Peržiūrėti dimensijos narius.</span><span class="sxs-lookup"><span data-stu-id="2116a-130">Click View dimension members.</span></span>
    * <span data-ttu-id="2116a-131">Peržiūrėkite importuotas DK sąskaitas kaip savo verslo išlaidų elementus, į kuriuos galima perkelti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="2116a-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

