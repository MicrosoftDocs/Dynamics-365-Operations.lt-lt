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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a7239bf5f8e53e61c4259abbcbf2ff740f4cef55
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433652"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="28a27-103">Gaunamas ir siunčiamas turtas</span><span class="sxs-lookup"><span data-stu-id="28a27-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="28a27-104">Jei jūsų įmonė vykdo iš kitų vietų ar klientų gauto turto remonto darbus ar priežiūros užduotis, modulyje Turto valdymas galima sekti ir gaunamą turtą, kuris yra pakeliui į jūsų įmonę, ir siunčiamą turtą, kuris yra grąžinamas.</span><span class="sxs-lookup"><span data-stu-id="28a27-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="28a27-105">Jei norite naudoti gaunamas ir siunčiamas ciklo būsenas gaunamam ir grąžinamam turtui valdyti, turite nustatyti priežiūros užklausų ciklo būsenas ir ciklo modelius, kad šie veiksmai būtų palaikomi.</span><span class="sxs-lookup"><span data-stu-id="28a27-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="28a27-106">Daugiau informacijos žr. [Priežiūros užklausos](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="28a27-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="28a27-107">Turto valdymo konfigūracija nulemia, ar galite dirbti su gaunamu ir siunčiamu turtu.</span><span class="sxs-lookup"><span data-stu-id="28a27-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="28a27-108">Gaunamo turto registravimas</span><span class="sxs-lookup"><span data-stu-id="28a27-108">Register assets as inbound</span></span>

1. <span data-ttu-id="28a27-109">Pasirinkite **Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="28a27-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="28a27-110">Pasirinkite priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="28a27-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="28a27-111">Pasirinkite **Atnaujinti priežiūros užklausos būseną**.</span><span class="sxs-lookup"><span data-stu-id="28a27-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="28a27-112">Pasirinkite **Gaunamas** (arba kitą sukurtą gaunamo turto ciklo būseną), tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="28a27-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Gaunamo turto registravimas](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="28a27-114">Gaunamo turto kaip gauto registravimas</span><span class="sxs-lookup"><span data-stu-id="28a27-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="28a27-115">Pasirinkite **Turto valdymas** \> **Dažnas** \> **Pirmyn atgal** \> **Atvykstamasis turtas**.</span><span class="sxs-lookup"><span data-stu-id="28a27-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="28a27-116">Pasirinkite turtą arba priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="28a27-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="28a27-117">Pasirinkite **Gauti turtą**.</span><span class="sxs-lookup"><span data-stu-id="28a27-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="28a27-118">Lauke **Gauta** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="28a27-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="28a27-119">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="28a27-119">Then select **OK**.</span></span> <span data-ttu-id="28a27-120">Įrašas pašalinamas iš **Gaunamas turtas** sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="28a27-120">The record is removed from the **Inbound assets** list page.</span></span>

![Gaunamo turto kaip gauto registravimas](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="28a27-122">Siunčiamo turto registravimas</span><span class="sxs-lookup"><span data-stu-id="28a27-122">Register assets as outbound</span></span>

<span data-ttu-id="28a27-123">Atlikę priežiūros arba remonto užduotį, galite užregistruoti turtą kaip grąžintą.</span><span class="sxs-lookup"><span data-stu-id="28a27-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="28a27-124">Pasirinkite **Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Aktyvios priežiūros užklausos**.</span><span class="sxs-lookup"><span data-stu-id="28a27-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="28a27-125">Pasirinkite priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="28a27-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="28a27-126">Pasirinkite **Atnaujinti priežiūros užklausos būseną**.</span><span class="sxs-lookup"><span data-stu-id="28a27-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="28a27-127">Pasirinkite **Siunčiamas** (arba kitą sukurtą siunčiamo turto ciklo būseną), tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="28a27-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="28a27-128">Siunčiamo turto kaip pristatyto registravimas</span><span class="sxs-lookup"><span data-stu-id="28a27-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="28a27-129">Pasirinkite **Turto valdymas** \> **Dažnas** \> **Pirmyn atgal** \> **Siunčiamas turtas**.</span><span class="sxs-lookup"><span data-stu-id="28a27-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="28a27-130">Pasirinkite turtą arba priežiūros užklausą.</span><span class="sxs-lookup"><span data-stu-id="28a27-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="28a27-131">Pasirinkite **Pristatyti turtą**.</span><span class="sxs-lookup"><span data-stu-id="28a27-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="28a27-132">Lauke **Pristatyta** įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="28a27-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="28a27-133">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="28a27-133">Then select **OK**.</span></span> <span data-ttu-id="28a27-134">Įrašas pašalinamas iš **Siunčiamas turtas** sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="28a27-134">The record is removed from the **Outbound assets** list page.</span></span>
