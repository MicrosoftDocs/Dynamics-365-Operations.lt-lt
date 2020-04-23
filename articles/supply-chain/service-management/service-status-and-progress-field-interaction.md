---
title: Aptarnavimo būsenos ir eigos lauko sąveika
description: Formoje Aptarnavimo užsakymai antraštės lauke Eiga nurodoma viso aptarnavimo užsakymo būsena, o lauke Būsena nurodoma atskirų aptarnavimo užsakymo eilučių būsena.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd70d00f7ce531b225362065dfd9f1f5c1adc754
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207329"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="b5be3-103">Aptarnavimo būsenos ir eigos lauko sąveika</span><span class="sxs-lookup"><span data-stu-id="b5be3-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b5be3-104">Formoje **Aptarnavimo užsakymai** aptarnavimo užsakymo lauke **Eiga** nurodoma viso aptarnavimo užsakymo būsena, o lauke **Būsena** nurodoma atskirų aptarnavimo užsakymo eilučių būsena.</span><span class="sxs-lookup"><span data-stu-id="b5be3-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5be3-105">Eiga</span><span class="sxs-lookup"><span data-stu-id="b5be3-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="b5be3-106">1 eilutės būsena</span><span class="sxs-lookup"><span data-stu-id="b5be3-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="b5be3-107">2 eilutės būsena</span><span class="sxs-lookup"><span data-stu-id="b5be3-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="b5be3-108">3 eilutės būsena</span><span class="sxs-lookup"><span data-stu-id="b5be3-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5be3-109"><strong>Vykdoma</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-110"><strong>Sukurta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-111"><strong>Sukurta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-112"><strong>Sukurta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5be3-113"><strong>Vykdoma</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-114"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-115"><strong>Sukurta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-116"><strong>Sukurta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5be3-117"><strong>Vykdoma</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-118"><strong>Sukurta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-119"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-120"><strong>Užregistruota</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5be3-121"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-122"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-123"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-124"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5be3-125"><strong>Užregistruota</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-126"><strong>Užregistruota</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-127"><strong>Užregistruota</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-128"><strong>Užregistruota</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5be3-129"><strong>Užregistruota</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-130"><strong>Užregistruota</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-131"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="b5be3-132"><strong>Atšaukta</strong></span><span class="sxs-lookup"><span data-stu-id="b5be3-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b5be3-133">Aptarnavimo užsakymo eiga vykdoma, jei visų eilučių būsena **Sukurta**; taip pat ji vykdoma, jei kai kurių eilučių būsena yra **Atšaukta** arba **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="b5be3-134">Jei visos aptarnavimo užsakymo eilutės yra pažymėtos nurodant būseną **Užregistruota**, būsenos užsakymo eiga yra **Užregistruota**..</span><span class="sxs-lookup"><span data-stu-id="b5be3-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="b5be3-135">Jei kai kurios eilutės pažymėtos nurodant būseną **Užregistruota**, o kai kurios – nurodant būseną **Atšaukta**, eigos būsena vis dar **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="b5be3-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


