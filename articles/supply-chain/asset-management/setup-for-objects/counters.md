---
title: Turto matai
description: Šioje temoje paaiškinta, kaip kurti turto matus turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783469"
---
# <a name="asset-measures"></a><span data-ttu-id="2cc9b-103">Turto matai</span><span class="sxs-lookup"><span data-stu-id="2cc9b-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="2cc9b-104">Šioje temoje paaiškinta, kaip kurti turto matus turto valdyme.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="2cc9b-105">Turto matų tipai naudojami norint atlikti turto matavimo vienetų registravimus, pvz., gamybos valandų skaičių arba pagaminto turto kiekį.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="2cc9b-106">Turto tipai susiję su turto matų tipais.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="2cc9b-107">Tai reiškia, kad turto matas gali būti naudojamas turtui tik tuo atveju, jei turto matas nustatomas naudojamo turto tipui.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="2cc9b-108">Prieš atliekant turto matavimo vienetų registravimus būtina sukurti turto matų tipus, kuriuos norite naudoti dalyje **Skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="2cc9b-109">Tada galima kurti turto matavimo vienetų registravimus dalyje **Turto matai**.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="2cc9b-110">Turto matai gali būti naudojami priežiūros planuose.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="2cc9b-111">Priežiūros plano eilutė gali būti tipo „Skaitiklis“, pavyzdžiui, susijusi su gamybos valandų skaičiumi arba pagamintu kiekiu.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="2cc9b-112">Turto matavimo vienetų registravimus galima atnaujinti rankiniu būdu arba automatiškai, atsižvelgiant į gamybos valandas arba pagamintą kiekį.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="2cc9b-113">Turto matas gali būti nustatytas naudoti vieną iš trijų naujinimo metodų (pasirinktų lauke **Naujinti** dalyje **Skaitikliai**):</span><span class="sxs-lookup"><span data-stu-id="2cc9b-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="2cc9b-114">Rankinis – būtina užregistruoti turto matavimo vienetų reikšmes rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="2cc9b-115">Gamybos valandos – skaitiklis automatiškai atnaujinamas pagal gamybos valandų skaičių.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="2cc9b-116">Gamybos kiekis – skaitiklis automatiškai atnaujinamas pagal pagamintą kiekį.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="2cc9b-117">Jei naudojamas pagamintas kiekis, *visi* užregistruoti elementai įtraukiami į matavimo vienetų registravimą, tiek tinkamas, tiek netinkamas kiekis.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="2cc9b-118">Jei reikia, visada galima rankiniu būdu atlikti turto matavimo vienetų registravimus.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="2cc9b-119">Turto skaitiklio registravimų skaitiklio tipų kūrimas</span><span class="sxs-lookup"><span data-stu-id="2cc9b-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="2cc9b-120">Pasirinkite **Turto valdymas** > **Sąranka** > **Turto tipai** > **Skaitikliai**.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="2cc9b-121">Pasirinkite **Naujas**, kad sukurtumėte naują turto matavimo vieneto tipą.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="2cc9b-122">Lauke **Skaitiklis** įterpkite ID, o lauke **Pavadinimas** – skaitiklio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="2cc9b-123">„FastTab“ **Bendra** pasirinkite matavimo vienetą lauke **Vienetas**.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="2cc9b-124">Lauke **Naujinti** pasirinkite turto matui naudojamą naujinimo metodą.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="2cc9b-125">Perjungimo mygtuke **Paveldėti skaitiklio reikšmes** pasirinkite „Taip“, jei antrinis turtas turto struktūroje turėtų automatiškai paveldėti turto matų registravimus, atliktus pagrindiniame turte.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="2cc9b-126">Lauke **Bendroji agreguota reikšmė** pasirinkite turto matų sumavimo metodą naudojant šį turto mato tipą.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="2cc9b-127">„Sum“ yra standartinis pasirinkimas, naudojamas norint nuolat įtraukti užregistruotas reikšmes į bendrąją reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="2cc9b-128">„Average“ gali būti naudojama, jei turto matas nustatytas stebėti ribines reikšmes, pvz., temperatūrą, vibraciją ar turto nusidėvėjimą.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="2cc9b-129">Lauke **Nuokrypis virš** įterpkite viršutinę procentinę reikšmę tikrinant, ar rankiniai turto matų registravimai patenka į numatytą diapazoną.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="2cc9b-130">Tikrinimas pagrįstas esamo turto mato registravimų linijiniu padidėjimu.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="2cc9b-131">Lauke **Nuokrypis po** įterpkite apatinę procentinę reikšmę tikrinant, ar rankiniai turto matų registravimai patenka į numatytą diapazoną.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="2cc9b-132">Tikrinimas pagrįstas esamo turto mato registravimų linijiniu sumažėjimu.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="2cc9b-133">Lauke **Tipas** pasirinkite pranešimo tipą (informacija, įspėjimas, klaida), kuris bus rodomas, jei rankinio turto mato registravimų metu atsiranda nuokrypių už apibrėžto diapazono.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="2cc9b-134">„FastTab“ **Turto tipai** įtraukite turto tipus, kurie turėtų naudoti turto matą.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="2cc9b-135">„FastTab“ **Susijusio turto matai** įtraukite turto matus, kurie bus automatiškai atnaujinti atnaujinus šį turto matą.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="2cc9b-136">Susijęs turto matas automatiškai atnaujinamas tik tuo atveju, jei turto mato nustatymuose susijęs turto matas yra turto tipo, su kuriuo jis yra susijęs.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="2cc9b-137">Pavyzdžiui: galima nustatyti turto matą „Gamybos valandoms“ ir įtraukti turto tipą „Sunkvežimio variklis“.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="2cc9b-138">Kai šis turto matas atnaujinamas, susijęs skaitiklis „Nafta“ taip pat atnaujinamas pagal tas pačias turto matų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="2cc9b-139">Nustatymai dalyje **Skaitikliai** apima nustatymus „Valandos“.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="2cc9b-140">Be to, „Nafta“ turto mate turto tipas „Sunkvežimio variklis“ turi būti įtrauktas į „FastTab“ **Turto tipai**, kad būtų užtikrintas turto mato ryšys.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="2cc9b-141">Žr. toliau pateiktus ekrano vaizdus, kus pateiktas Valandų ir Naftos turto matų nustatymo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="2cc9b-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="2cc9b-142">Kai turto tipai įtraukiami į turto mato tipą dalyje **Skaitikliai**, tas turto matas automatiškai įtraukiamas į turto tipus „FastTab“ **Skaitikliai** dalyje [Turto tipai](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="2cc9b-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![1 pav.](media/071-setup-for-objects.png)


