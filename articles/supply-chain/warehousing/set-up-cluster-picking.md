---
title: Klasterio paėmimo nustatymas
description: Šioje temoje aprašoma, kaip nustatyti klasterio paėmimą ir kaip taikyti prekės patvirtinimą naudojant klasterio paėmimą.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da11a474e1bb031fac26e04c91cbdbab5f62eb0b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977358"
---
# <a name="set-up-cluster-picking"></a><span data-ttu-id="9efc2-103">Klasterio paėmimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="9efc2-103">Set up cluster picking</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9efc2-104">Šioje temoje aprašoma, kaip leisti darbuotojams naudotis savo mobiliaisiais įrenginiais norint grupuoti paėmimo darbą, kad vienu metu iš vienos vietos būtų galima paimti keleto darbo užsakymų prekes.</span><span class="sxs-lookup"><span data-stu-id="9efc2-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="9efc2-105">Tai vadinama *klasterio paėmimu*.</span><span class="sxs-lookup"><span data-stu-id="9efc2-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="9efc2-106">Apie klasterio paėmimą</span><span class="sxs-lookup"><span data-stu-id="9efc2-106">About cluster picking</span></span>

<span data-ttu-id="9efc2-107">Pateikus darbo užsakymus į sandėlį, darbuotojas gali naudoti mobilųjį įrenginį norėdamas priskirti užsakymus klasteriui.</span><span class="sxs-lookup"><span data-stu-id="9efc2-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="9efc2-108">Klasteris darbuotojui suorganizuos paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="9efc2-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="9efc2-109">Kai darbo užsakymas priskiriamas klasteriui, darbuotojas turi naudoti klasterio paėmimą, kad atliktų užsakymo paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="9efc2-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="9efc2-110">Darbuotas negali naudoti kitų paėmimo būdų.</span><span class="sxs-lookup"><span data-stu-id="9efc2-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="9efc2-111">Jei darbo užsakymas klasteriui priskiriamas per klaidą, darbuotojas turi išskaidyti klasterį ir perkurti.</span><span class="sxs-lookup"><span data-stu-id="9efc2-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="9efc2-112">Jei reikia, darbuotojas gali perduoti klasterį kitam darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="9efc2-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="9efc2-113">Tada klasterio būsena pakeičiama į Perduota.</span><span class="sxs-lookup"><span data-stu-id="9efc2-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="9efc2-114">Kai darbuotojas naudoja mobilųjį įrenginį norėdamas nurodyti, kad paėmimo ir atidėjimo darbas baigtas, siuntą arba krovinį reikia patvirtinti kliente.</span><span class="sxs-lookup"><span data-stu-id="9efc2-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the client.</span></span>

## <a name="enable-cluster-picking"></a><span data-ttu-id="9efc2-115">Klasterio paėmimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="9efc2-115">Enable cluster picking</span></span>

<span data-ttu-id="9efc2-116">Norėdami įgalinti klasterio paėmimą, turite nustatyti taip:</span><span class="sxs-lookup"><span data-stu-id="9efc2-116">To enable cluster picking, you must set up the following:</span></span>

- <span data-ttu-id="9efc2-117">**Klasterio šablonai** – nurodykite, ar norite automatiškai sugeneruoti klasterio ID, naudotinų padėčių skaičių, kada klasterius skaidyti ir kaip nuosekliai išdėstyti bei patikrinti paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="9efc2-117">**Cluster profiles** – Specify whether to automatically generate cluster   IDs, the number of positions to use, when to break clusters, and how to   sequence and verify the picking work.</span></span>

- <span data-ttu-id="9efc2-118">**Darbo šablonai** – apibrėžkite, kaip sukurti klasterio paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="9efc2-118">**Work templates** – Define how to create the picking work for cluster   picking.</span></span>

- <span data-ttu-id="9efc2-119">**Vietos nurodymai** – nurodykite, iš kur prekes paimti ir kur jas padėti.</span><span class="sxs-lookup"><span data-stu-id="9efc2-119">**Location directives** – Specify where to pick items from, and where to put   them.</span></span>

- <span data-ttu-id="9efc2-120">**Mobiliojo įrenginio meniu elementai** – sukonfigūruokite mobiliojo įrenginio meniu elementą norėdami naudoti esamą darbą, kurį nurodo klasterio paėmimas.</span><span class="sxs-lookup"><span data-stu-id="9efc2-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="9efc2-121">Tada turite įtraukti meniu elementą į mobiliojo įrenginio meniu, kad jis būtų rodomas mobiliuosiuose įrenginiuose.</span><span class="sxs-lookup"><span data-stu-id="9efc2-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

- <span data-ttu-id="9efc2-122">**Sandėlio valdymo parametrai** – nurodykite numeraciją, naudotiną norint sugeneruoti klasterių identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="9efc2-122">**Warehouse management parameters** – Specify the number sequence to use if   you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="9efc2-123">Klasterio šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="9efc2-123">Set up a cluster profile</span></span>

<span data-ttu-id="9efc2-124">Norėdami nustatyti klasterio šabloną atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="9efc2-124">To set up a cluster profile, follow these steps:</span></span>

1. <span data-ttu-id="9efc2-125">Spustelėkite **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Klasterio šablonai**.</span><span class="sxs-lookup"><span data-stu-id="9efc2-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \>  **Cluster profiles**.</span></span>

1. <span data-ttu-id="9efc2-126">Norėdami sukurti naują šabloną spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="9efc2-126">Click **New** to create a new profile.</span></span>

1. <span data-ttu-id="9efc2-127">Spustelėję **Sukurti klasterį**, o po to srityje **Klasterio rūšiavimas** spustelėję **Naujas** nustatykite klasterio rūšiavimo kriterijus.</span><span class="sxs-lookup"><span data-stu-id="9efc2-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="9efc2-128">Rūšiavimo kriterijai valdo tvarką, kuria darbuotojas atliks paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="9efc2-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="9efc2-129">Galite įtraukti tiek kriterijų, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="9efc2-129">You can add as many criteria as needed.</span></span>

1. <span data-ttu-id="9efc2-130">Lauke **Eilės numeris** įveskite skaičių norėdami apibrėžti rūšiavimo kriterijų apdorojimo tvarką.</span><span class="sxs-lookup"><span data-stu-id="9efc2-130">In the **Sequence number** field, enter a number to define the order in  which the sorting criteria are processed.</span></span>

1. <span data-ttu-id="9efc2-131">Lauke **Lauko pavadinimas** pasirinkite lauką, kuris nustatys rūšiavimą.</span><span class="sxs-lookup"><span data-stu-id="9efc2-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="9efc2-132">Pavyzdžiui, jei pasirenkate lauką **WMSLocationId**, darbas bus rūšiuojamas pagal vietą.</span><span class="sxs-lookup"><span data-stu-id="9efc2-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

1. <span data-ttu-id="9efc2-133">Lauke **Rūšiavimas** pasirinkite vieną iš toliau nurodytų pasirinkčių.</span><span class="sxs-lookup"><span data-stu-id="9efc2-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="9efc2-134">**Parinktis**</span><span class="sxs-lookup"><span data-stu-id="9efc2-134">**Option**</span></span>     | <span data-ttu-id="9efc2-135">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="9efc2-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9efc2-136">**Didėjančiai**</span><span class="sxs-lookup"><span data-stu-id="9efc2-136">**Ascending**</span></span>  | <span data-ttu-id="9efc2-137">Paėmimo darbo seka nustatoma didėjimo tvarka remiantis rūšiavimo kriterijais.</span><span class="sxs-lookup"><span data-stu-id="9efc2-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="9efc2-138">Pavyzdžiui, jei kaip rūšiavimo kriterijus naudojate lauką **WMSLocationId**, o jūsų vietos ID yra 1, 2, 3 ir 4, pirmiausia bus imama iš 4 vietos.</span><span class="sxs-lookup"><span data-stu-id="9efc2-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="9efc2-139">**Mažėjančiai**</span><span class="sxs-lookup"><span data-stu-id="9efc2-139">**Descending**</span></span> | <span data-ttu-id="9efc2-140">Paėmimo darbo seka nustatoma mažėjimo tvarka remiantis rūšiavimo kriterijais.</span><span class="sxs-lookup"><span data-stu-id="9efc2-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="9efc2-141">Pavyzdžiui, jei kaip rūšiavimo kriterijus naudojate lauką **WMSLocationId**, o jūsų vietos ID yra 1, 2, 3 ir 4, pirmiausia bus imama iš 1 vietos.</span><span class="sxs-lookup"><span data-stu-id="9efc2-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="9efc2-142">Prekės patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="9efc2-142">Item confirmation</span></span>

<span data-ttu-id="9efc2-143">Kai taikomas klasterio pasirinkimas, būtina patvirtinti prekes, kad būtų galima patikrinti į klasterius įtraukiamas prekes.</span><span class="sxs-lookup"><span data-stu-id="9efc2-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="9efc2-144">Galite patikrinti prekes atlikdami klasterių pasirinkimą, vykstant klasterio parinkimo procesui.</span><span class="sxs-lookup"><span data-stu-id="9efc2-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="9efc2-145">Sąranka pagrįsta produkto brūkšninio kodo sąranka.</span><span class="sxs-lookup"><span data-stu-id="9efc2-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="9efc2-146">Prekės patikrinimo nustatymas atliekant klasterio parinkimą</span><span class="sxs-lookup"><span data-stu-id="9efc2-146">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="9efc2-147">Mobiliojo įrenginio meniu elemente atidarykite darbo patvirtinimo sąrankos formą: **Sandėlio valdymas** \> **Sandėlio valdymas** \> **Sąranka** \> **Mobilusis įrenginys** \> **Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="9efc2-147">On a mobile device menu item, open the setup form for work confirmation:  **Warehouse management** \> **Warehouse management** \> **Setup** \>  **Mobile device** \> **Mobile device menu items**.</span></span>

1. <span data-ttu-id="9efc2-148">Mobiliojo įrenginio meniu elemente atidarykite **Darbo patvirtinimo sąranka**.</span><span class="sxs-lookup"><span data-stu-id="9efc2-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="9efc2-149">Naudodamiesi parinktimi **Produkto patvirtinimas** mobiliuoju įrenginiu nuskaitydami galite patikrinti kiekvieną atsargų dalį.</span><span class="sxs-lookup"><span data-stu-id="9efc2-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
