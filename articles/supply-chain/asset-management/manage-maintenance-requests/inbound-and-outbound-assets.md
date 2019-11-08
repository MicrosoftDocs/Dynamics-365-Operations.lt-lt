---
title: Gaunamas ir siunčiamas turtas
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas užregistruoti gaunamą ir siunčiamą turtą.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb318c24424c291f08ba7527b2258c0da4cba9a8
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571673"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="8c3ab-103">Gaunamas ir siunčiamas turtas</span><span class="sxs-lookup"><span data-stu-id="8c3ab-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8c3ab-104">Jei jūsų įmonė vykdo iš kitų vietų ar klientų gauto turto remonto darbus ar priežiūros užduotis, modulyje Turto valdymas galima sekti ir gaunamą turtą, kuris yra pakeliui į jūsų įmonę, ir siunčiamą turtą, kuris yra grąžinamas.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="8c3ab-105">Jei norite naudoti gaunamas ir siunčiamas ciklo būsenas gaunamam ir grąžinamam turtui valdyti, turite nustatyti priežiūros užklausų ciklo būsenas ir ciklo modelius, kad šie veiksmai būtų palaikomi.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="8c3ab-106">Daugiau informacijos žr. skyriuje [Priežiūros užklausų konfigūracija](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="8c3ab-106">For more information, see [Setup for maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="8c3ab-107">Turto valdymo konfigūracija nulemia, ar galite dirbti su gaunamu ir siunčiamu turtu.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="8c3ab-108">Gaunamo turto registravimas</span><span class="sxs-lookup"><span data-stu-id="8c3ab-108">Register assets as inbound</span></span>

1. <span data-ttu-id="8c3ab-109">Pasirinkite**Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="8c3ab-110">Pasirinkite priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="8c3ab-111">Pasirinkite **Atnaujinti priežiūros užklausos būseną**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="8c3ab-112">Pasirinkite **Gaunamas** (arba kitą sukurtą gaunamo turto ciklo būseną), tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Gaunamo turto registravimas](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="8c3ab-114">Gaunamo turto kaip gauto registravimas</span><span class="sxs-lookup"><span data-stu-id="8c3ab-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="8c3ab-115">Pasirinkite **Turto valdymas** \> **Dažnas** \> **Pirmyn atgal** \> **Atvykstamasis turtas**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="8c3ab-116">Pasirinkite turtą arba priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="8c3ab-117">Pasirinkite **Gauti turtą**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="8c3ab-118">Lauke **Gauta** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="8c3ab-119">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-119">Then select **OK**.</span></span> <span data-ttu-id="8c3ab-120">Įrašas pašalinamas iš **Gaunamas turtas** sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-120">The record is removed from the **Inbound assets** list page.</span></span>

![Gaunamo turto kaip gauto registravimas](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="8c3ab-122">Siunčiamo turto registravimas</span><span class="sxs-lookup"><span data-stu-id="8c3ab-122">Register assets as outbound</span></span>

<span data-ttu-id="8c3ab-123">Atlikę priežiūros arba remonto užduotį, galite užregistruoti turtą kaip grąžintą.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="8c3ab-124">Pasirinkite**Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="8c3ab-125">Pasirinkite priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="8c3ab-126">Pasirinkite **Atnaujinti priežiūros užklausos būseną**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="8c3ab-127">Pasirinkite **Siunčiamas** (arba kitą sukurtą siunčiamo turto ciklo būseną), tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="8c3ab-128">Siunčiamo turto kaip pristatyto registravimas</span><span class="sxs-lookup"><span data-stu-id="8c3ab-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="8c3ab-129">Pasirinkite **Turto valdymas** \> **Dažnas** \> **Pirmyn atgal** \> **Siunčiamas turtas**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="8c3ab-130">Pasirinkite turtą arba priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="8c3ab-131">Pasirinkite **Pristatyti turtą**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="8c3ab-132">Lauke **Pristatyta** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="8c3ab-133">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-133">Then select **OK**.</span></span> <span data-ttu-id="8c3ab-134">Įrašas pašalinamas iš **Siunčiamas turtas** sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="8c3ab-134">The record is removed from the **Outbound assets** list page.</span></span>
