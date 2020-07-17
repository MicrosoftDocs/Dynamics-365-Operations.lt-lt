---
title: Papildomos vietos zonos
description: Šioje temoje apžvelgiamos naujos vietos zonos, kurios pridėtos į „Microsoft Dynamics 365 Supply Chain Management”.
author: Mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9727187ad555f9e3d09beed3f3447a22c29ed22a
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530172"
---
# <a name="additional-location-zones"></a><span data-ttu-id="eaeed-103">Papildomos vietos zonos</span><span class="sxs-lookup"><span data-stu-id="eaeed-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaeed-104">Galimi trys nauji zonų laukai „Microsoft Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="eaeed-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="eaeed-105">Sandėlio valdytojai gali naudoti juos papildomoms sandėlio organizacijoms arba maketams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="eaeed-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="eaeed-106">Naujus zonos laukus galima nustatyti neautomatiniu būdu arba naudojant **Vietos parametras** vedlį.</span><span class="sxs-lookup"><span data-stu-id="eaeed-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="eaeed-107">Jie gali būti naudojami bet kurioje užklausoje ar filtruojant, naudojant Vietos lentelę.</span><span class="sxs-lookup"><span data-stu-id="eaeed-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="eaeed-108">Norint naudoti zonos laukus, papildomų nustatymų nereikia.</span><span class="sxs-lookup"><span data-stu-id="eaeed-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="eaeed-109">Papildomos vietos zonos įjungimo funkcija</span><span class="sxs-lookup"><span data-stu-id="eaeed-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="eaeed-110">Norint naudoti *Papildomos vietos zona* funkciją, įjunkite ją savo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="eaeed-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="eaeed-111">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="eaeed-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="eaeed-112">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="eaeed-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="eaeed-113">**Modulis:** *sandėlio valdymas*</span><span class="sxs-lookup"><span data-stu-id="eaeed-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="eaeed-114">**Funkcijos pavadinimas:** *Papildomos vietos zona*</span><span class="sxs-lookup"><span data-stu-id="eaeed-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="eaeed-115">Vietos zonų naudojimas</span><span class="sxs-lookup"><span data-stu-id="eaeed-115">Use location zones</span></span>

1. <span data-ttu-id="eaeed-116">Eikite į **Sandėlio tvarkymas \> Sąranka \>Sandėlis \> Vietos nustatymo vedlys**.</span><span class="sxs-lookup"><span data-stu-id="eaeed-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="eaeed-117">Nustatykite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="eaeed-117">Set the following values:</span></span>

    - <span data-ttu-id="eaeed-118">Lauke **Sandėlis** pasirinkite _62_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="eaeed-119">**Zonos ID** lauke pasirinkite _AUKŠTAS_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="eaeed-120">**Papildoma zona 1** lauke pasirinkite _PASIRINKTIZONĄ1_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="eaeed-121">**Papildoma zona 2** lauke pasirinkite _INTERNETINĖPARDUOTUVĖ1_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="eaeed-122">**Vietos profilio ID** lauke pasirinkite _AUKŠTAS_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="eaeed-123">Pasirinkite **Aukštas** eilutę.</span><span class="sxs-lookup"><span data-stu-id="eaeed-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="eaeed-124">**Nuo numeris** įveskite _1_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="eaeed-125">**Iki numeris** lauke įveskite _3_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="eaeed-126">Pasirinkite **Perėjimas** eilutę.</span><span class="sxs-lookup"><span data-stu-id="eaeed-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="eaeed-127">**Nuo numeris** įveskite _1_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="eaeed-128">**Iki numeris** lauke įveskite _5_.</span><span class="sxs-lookup"><span data-stu-id="eaeed-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="eaeed-129">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="eaeed-129">Select **Create**.</span></span>
8. <span data-ttu-id="eaeed-130">Gaunate pranešimus, kuriuose nurodoma, kad buvo pridėtos naujos vietos.</span><span class="sxs-lookup"><span data-stu-id="eaeed-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="eaeed-131">Pasirinkite **Rodyti pranešimus** mygtuką, kada peržiūrėtumėte pranešimus.</span><span class="sxs-lookup"><span data-stu-id="eaeed-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="eaeed-132">Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos**.</span><span class="sxs-lookup"><span data-stu-id="eaeed-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="eaeed-133">Naujos vietos rodomos sąraše, o visi zonų laukai yra galimi (t. y. esamos zonos laukas ir naujos papildomos zonos laukai).</span><span class="sxs-lookup"><span data-stu-id="eaeed-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
