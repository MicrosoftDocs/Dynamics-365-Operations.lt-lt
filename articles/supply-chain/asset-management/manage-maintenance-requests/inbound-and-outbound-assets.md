---
title: Gaunamas ir siunčiamas turtas
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas užregistruoti gaunamą ir siunčiamą turtą.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6dfadf6824c6a3df7be9b3b6f3d9f5dd2749e34
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018076"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="b5f7f-103">Gaunamas ir siunčiamas turtas</span><span class="sxs-lookup"><span data-stu-id="b5f7f-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b5f7f-104">Jei jūsų įmonė vykdo iš kitų vietų ar klientų gauto turto remonto darbus ar priežiūros užduotis, modulyje Turto valdymas galima sekti ir gaunamą turtą, kuris yra pakeliui į jūsų įmonę, ir siunčiamą turtą, kuris yra grąžinamas.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="b5f7f-105">Jei norite naudoti gaunamas ir siunčiamas ciklo būsenas gaunamam ir grąžinamam turtui valdyti, turite nustatyti priežiūros užklausų ciklo būsenas ir ciklo modelius, kad šie veiksmai būtų palaikomi.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="b5f7f-106">Daugiau informacijos žr. [Priežiūros užklausos](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="b5f7f-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="b5f7f-107">Turto valdymo konfigūracija nulemia, ar galite dirbti su gaunamu ir siunčiamu turtu.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="b5f7f-108">Gaunamo turto registravimas</span><span class="sxs-lookup"><span data-stu-id="b5f7f-108">Register assets as inbound</span></span>

1. <span data-ttu-id="b5f7f-109">Pasirinkite **Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="b5f7f-110">Pasirinkite priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="b5f7f-111">Pasirinkite **Atnaujinti priežiūros užklausos būseną**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="b5f7f-112">Pasirinkite **Gaunamas** (arba kitą sukurtą gaunamo turto ciklo būseną), tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Gaunamo turto registravimas](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="b5f7f-114">Gaunamo turto kaip gauto registravimas</span><span class="sxs-lookup"><span data-stu-id="b5f7f-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="b5f7f-115">Pasirinkite **Turto valdymas** \> **Dažnas** \> **Pirmyn atgal** \> **Atvykstamasis turtas**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="b5f7f-116">Pasirinkite turtą arba priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="b5f7f-117">Pasirinkite **Gauti turtą**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="b5f7f-118">Lauke **Gauta** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="b5f7f-119">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-119">Then select **OK**.</span></span> <span data-ttu-id="b5f7f-120">Įrašas pašalinamas iš **Gaunamas turtas** sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-120">The record is removed from the **Inbound assets** list page.</span></span>

![Gaunamo turto kaip gauto registravimas](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="b5f7f-122">Siunčiamo turto registravimas</span><span class="sxs-lookup"><span data-stu-id="b5f7f-122">Register assets as outbound</span></span>

<span data-ttu-id="b5f7f-123">Atlikę priežiūros arba remonto užduotį, galite užregistruoti turtą kaip grąžintą.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="b5f7f-124">Pasirinkite **Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="b5f7f-125">Pasirinkite priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="b5f7f-126">Pasirinkite **Atnaujinti priežiūros užklausos būseną**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="b5f7f-127">Pasirinkite **Siunčiamas** (arba kitą sukurtą siunčiamo turto ciklo būseną), tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="b5f7f-128">Siunčiamo turto kaip pristatyto registravimas</span><span class="sxs-lookup"><span data-stu-id="b5f7f-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="b5f7f-129">Pasirinkite **Turto valdymas** \> **Dažnas** \> **Pirmyn atgal** \> **Siunčiamas turtas**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="b5f7f-130">Pasirinkite turtą arba priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="b5f7f-131">Pasirinkite **Pristatyti turtą**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="b5f7f-132">Lauke **Pristatyta** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="b5f7f-133">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-133">Then select **OK**.</span></span> <span data-ttu-id="b5f7f-134">Įrašas pašalinamas iš **Siunčiamas turtas** sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="b5f7f-134">The record is removed from the **Outbound assets** list page.</span></span>
