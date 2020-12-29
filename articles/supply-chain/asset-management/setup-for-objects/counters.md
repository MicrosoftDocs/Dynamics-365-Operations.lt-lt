---
title: Turto matai
description: Šioje temoje paaiškinta, kaip kurti turto matus turto valdyme.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433701"
---
# <a name="counters"></a><span data-ttu-id="5f90f-103">Skaitikliai</span><span class="sxs-lookup"><span data-stu-id="5f90f-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f90f-104">Šioje temoje paaiškinta, kaip kurti skaitiklio tipus turto valdyme.</span><span class="sxs-lookup"><span data-stu-id="5f90f-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="5f90f-105">Skaitiklio tipai naudojami norint atlikti turto skaitiklių registracijas, pvz., gamybos valandų skaičių arba pagaminto turto kiekį.</span><span class="sxs-lookup"><span data-stu-id="5f90f-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="5f90f-106">Turto tipai yra susiję su skaitiklio tipais.</span><span class="sxs-lookup"><span data-stu-id="5f90f-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="5f90f-107">Tai reiškia, kad skaitiklis gali būti naudojamas turtui tik tuo atveju, jei skaitiklis yra nustatytas naudojamam turto tipui.</span><span class="sxs-lookup"><span data-stu-id="5f90f-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="5f90f-108">Prieš atliekant turto skaitiklio registracijas, būtina sukurti skaitiklio tipus, kuriuos norite naudoti **Skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="5f90f-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="5f90f-109">Tada **Skaitikliai** galima kurti skaitiklio registracijas.</span><span class="sxs-lookup"><span data-stu-id="5f90f-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="5f90f-110">Skaitikliai gali būti naudojami priežiūros planuose.</span><span class="sxs-lookup"><span data-stu-id="5f90f-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="5f90f-111">Priežiūros plano eilutė gali būti tipo „Skaitiklis“, pavyzdžiui, susijusi su gamybos valandų skaičiumi arba pagamintu kiekiu.</span><span class="sxs-lookup"><span data-stu-id="5f90f-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="5f90f-112">Skaitiklio registraciją galima atnaujinti rankiniu būdu arba automatiškai, atsižvelgiant į gamybos valandas arba pagamintą kiekį.</span><span class="sxs-lookup"><span data-stu-id="5f90f-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="5f90f-113">Skaitiklis gali būti nustatytas naudoti vieną iš trijų naujinimo metodų (pasirinktų lauke **Naujinti**, dalyje **Skaitikliai**):</span><span class="sxs-lookup"><span data-stu-id="5f90f-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="5f90f-114">Rankinis – skaitiklio reikšmes būtina užregistruoti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="5f90f-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="5f90f-115">Gamybos valandos – skaitiklis automatiškai atnaujinamas pagal gamybos valandų skaičių.</span><span class="sxs-lookup"><span data-stu-id="5f90f-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="5f90f-116">Gamybos kiekis – skaitiklis automatiškai atnaujinamas pagal pagamintą kiekį.</span><span class="sxs-lookup"><span data-stu-id="5f90f-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="5f90f-117">Jei naudojamas pagamintas kiekis, *visi* užregistruoti elementai įtraukiami į skaitiklio registraciją, t. y. tiek tinkamas kiekis, tiek kiekis su klaidomis.</span><span class="sxs-lookup"><span data-stu-id="5f90f-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="5f90f-118">Jei reikia, skaitiklio registraciją visada galima atlikti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="5f90f-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="5f90f-119">Turto skaitiklio registravimų skaitiklio tipų kūrimas</span><span class="sxs-lookup"><span data-stu-id="5f90f-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="5f90f-120">Pasirinkite **Turto valdymas** > **Sąranka** > **Turto tipai** > **Skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="5f90f-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="5f90f-121">Pasirinkite **Naujas**, kad sukurtumėte naują skaitiklio tipą.</span><span class="sxs-lookup"><span data-stu-id="5f90f-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="5f90f-122">Lauke **Skaitiklis** įterpkite ID, o lauke **Pavadinimas** – skaitiklio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5f90f-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="5f90f-123">„FastTab“ **Bendra** pasirinkite skaitiklio vienetą lauke **Vienetas**.</span><span class="sxs-lookup"><span data-stu-id="5f90f-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="5f90f-124">Lauke **Naujinti** pasirinkite skaitikliui naudojamą naujinimo metodą.</span><span class="sxs-lookup"><span data-stu-id="5f90f-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="5f90f-125">Perjungimo mygtuke **Paveldėti skaitiklio reikšmes** pasirinkite „Taip“, jei antrinis turtas turto struktūroje turi automatiškai paveldėti skaitiklio registracijas, atliktas pagrindiniame turte.</span><span class="sxs-lookup"><span data-stu-id="5f90f-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="5f90f-126">Lauke **Bendroji agreguota reikšmė** pasirinkite skaitikliui naudojamą sumavimo metodą naudojant šį skaitiklio tipą.</span><span class="sxs-lookup"><span data-stu-id="5f90f-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="5f90f-127">„Sum“ yra standartinis pasirinkimas, naudojamas norint nuolat įtraukti užregistruotas reikšmes į bendrąją reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5f90f-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="5f90f-128">„Average“ gali būti naudojamas, jei skaitiklis nustatytas stebėti ribines reikšmes, pvz., temperatūrą, vibraciją ar turto nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="5f90f-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="5f90f-129">Lauke **Nuokrypis virš** įveskite viršutinę procentinę reikšmę tikrinant, ar rankiniu būdu atliktos skaitiklio registracijos patenka į numatytą intervalą.</span><span class="sxs-lookup"><span data-stu-id="5f90f-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="5f90f-130">Tikrinimas pagrįstas esamų skaitiklio registracijų tiesiniu padidėjimu.</span><span class="sxs-lookup"><span data-stu-id="5f90f-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="5f90f-131">Lauke **Nuokrypis iki** įveskite apatinę procentinę reikšmę tikrinant, ar rankiniu būdu atliktos skaitiklio registracijos patenka į numatytą intervalą.</span><span class="sxs-lookup"><span data-stu-id="5f90f-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="5f90f-132">Tikrinimas pagrįstas esamų skaitiklio registracijų tiesiniu sumažėjimu.</span><span class="sxs-lookup"><span data-stu-id="5f90f-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="5f90f-133">Lauke **Tipas** pasirinkite pranešimo tipą (informacija, įspėjimas, klaida), kuris bus rodomas, jei rankiniu būdu atliekamų skaitiklio registravimų metu atsiranda nuokrypių už apibrėžto intervalo.</span><span class="sxs-lookup"><span data-stu-id="5f90f-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="5f90f-134">„FastTab“ **Turto tipai** įtraukite turto tipus, kurie turėtų galėti naudoti skaitiklį.</span><span class="sxs-lookup"><span data-stu-id="5f90f-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="5f90f-135">„FastTab“ **Susijusio turto skaitikliai** įtraukite skaitiklį, kuris bus automatiškai atnaujinamas atnaujinus šį skaitiklį.</span><span class="sxs-lookup"><span data-stu-id="5f90f-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="5f90f-136">Susijęs skaitiklis automatiškai atnaujinamas tik tuo atveju, jei skaitiklio nustatymuose susijęs skaitiklis yra turto tipo.</span><span class="sxs-lookup"><span data-stu-id="5f90f-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="5f90f-137">Pavyzdžiui, skaitiklį galima nustatyti „Gamybos valandoms“ ir įtraukti turto tipą „Sunkvežimio variklis“.</span><span class="sxs-lookup"><span data-stu-id="5f90f-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="5f90f-138">Kai šis skaitiklis atnaujinamas, susijęs skaitiklis „Alyva“ taip pat atnaujinamas pagal tas pačias skaitiklio reikšmes.</span><span class="sxs-lookup"><span data-stu-id="5f90f-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="5f90f-139">Nustatymai dalyje **Skaitikliai** apima nustatymus „Valandos“.</span><span class="sxs-lookup"><span data-stu-id="5f90f-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="5f90f-140">Be to, skatiklyje „Alyva“ turto tipas „Sunkvežimio variklis“ turi būti įtrauktas į „FastTab“ **Turto tipai**, kad būtų užtikrintas skaitiklio ryšys.</span><span class="sxs-lookup"><span data-stu-id="5f90f-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="5f90f-141">Žr. toliau esančias ekrano kopijas, kuriose pateiktas valandų ir alyvos skaitiklių nustatymo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="5f90f-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="5f90f-142">Kai turto tipai įtraukiami į skaitiklio tipą dalyje **Skaitikliai**, šis skaitiklis automatiškai įtraukiamas į turto tipus „FastTab“ **Skaitikliai**, dalyje [Turto tipai](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="5f90f-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![1 pav.](media/071-setup-for-objects.png)

