---
title: Mažinimo dienų pavyzdys
description: Mažinimo dienų pavyzdys.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 509d1a9e2abd79938376209d8feab1b935394833
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010527"
---
# <a name="reduction-days-example"></a><span data-ttu-id="073dd-103">Mažinimo dienų pavyzdys</span><span class="sxs-lookup"><span data-stu-id="073dd-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="073dd-104">Sukūrėte abonementinę operaciją kliento abonementui tvarkyti, kaip aprašyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="073dd-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="073dd-105">Nuo datos</span><span class="sxs-lookup"><span data-stu-id="073dd-105">From date</span></span></p></th>
<th><p><span data-ttu-id="073dd-106">Iki datos</span><span class="sxs-lookup"><span data-stu-id="073dd-106">To date</span></span></p></th>
<th><p><span data-ttu-id="073dd-107">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="073dd-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="073dd-108">Abonemento tipas</span><span class="sxs-lookup"><span data-stu-id="073dd-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="073dd-109">Project</span><span class="sxs-lookup"><span data-stu-id="073dd-109">Project</span></span></p></th>
<th><p><span data-ttu-id="073dd-110">Kategorija</span><span class="sxs-lookup"><span data-stu-id="073dd-110">Category</span></span></p></th>
<th><p><span data-ttu-id="073dd-111">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="073dd-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="073dd-112">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="073dd-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="073dd-113">2011 m. kovo 01 d.</span><span class="sxs-lookup"><span data-stu-id="073dd-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="073dd-114">2011 m. kovo 31 d.</span><span class="sxs-lookup"><span data-stu-id="073dd-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="073dd-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="073dd-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="073dd-116"><strong>Reguliarus</strong></span><span class="sxs-lookup"><span data-stu-id="073dd-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="073dd-117">9013</span><span class="sxs-lookup"><span data-stu-id="073dd-117">9013</span></span></p></td>
<td><p><span data-ttu-id="073dd-118">SubKat2</span><span class="sxs-lookup"><span data-stu-id="073dd-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="073dd-119">EUR</span><span class="sxs-lookup"><span data-stu-id="073dd-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="073dd-120">200,00</span><span class="sxs-lookup"><span data-stu-id="073dd-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="073dd-121">Klientas praneša, kad jam dvi dienas (kovo 10 d. ir kovo 11 d.) nereikės aptarnavimo.</span><span class="sxs-lookup"><span data-stu-id="073dd-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="073dd-122">Sutinkate sutrumpinti abonementą šiomis dviejomis dienomis.</span><span class="sxs-lookup"><span data-stu-id="073dd-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="073dd-123">Sukuriate naują **Mažinimo dienų** tipo operaciją, kaip aprašyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="073dd-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="073dd-124">Nuo datos</span><span class="sxs-lookup"><span data-stu-id="073dd-124">From date</span></span></p></th>
<th><p><span data-ttu-id="073dd-125">Iki datos</span><span class="sxs-lookup"><span data-stu-id="073dd-125">To date</span></span></p></th>
<th><p><span data-ttu-id="073dd-126">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="073dd-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="073dd-127">Abonemento tipas</span><span class="sxs-lookup"><span data-stu-id="073dd-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="073dd-128">Project</span><span class="sxs-lookup"><span data-stu-id="073dd-128">Project</span></span></p></th>
<th><p><span data-ttu-id="073dd-129">Kategorija</span><span class="sxs-lookup"><span data-stu-id="073dd-129">Category</span></span></p></th>
<th><p><span data-ttu-id="073dd-130">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="073dd-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="073dd-131">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="073dd-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="073dd-132">2011 m. kovo 10 d.</span><span class="sxs-lookup"><span data-stu-id="073dd-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="073dd-133">2011 m. kovo 11 d.</span><span class="sxs-lookup"><span data-stu-id="073dd-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="073dd-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="073dd-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="073dd-135"><strong>Sumažinimo dienos</strong></span><span class="sxs-lookup"><span data-stu-id="073dd-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="073dd-136">9013</span><span class="sxs-lookup"><span data-stu-id="073dd-136">9013</span></span></p></td>
<td><p><span data-ttu-id="073dd-137">SubKat2</span><span class="sxs-lookup"><span data-stu-id="073dd-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="073dd-138">EUR</span><span class="sxs-lookup"><span data-stu-id="073dd-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="073dd-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="073dd-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="073dd-140">Kai išrašoma SF už 2011 m. kovo mėn. operacijas, 200 EUR pardavimo kaina yra sumažinama 12,90 EUR.</span><span class="sxs-lookup"><span data-stu-id="073dd-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="073dd-141">Todėl mokėtina abonementinės operacijos suma yra 187,10 EUR, tad bendra SF suma už dvi operacijas yra 187,10 EUR.</span><span class="sxs-lookup"><span data-stu-id="073dd-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="073dd-142">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="073dd-142">See also</span></span>

[<span data-ttu-id="073dd-143">Abonementinio mokesčio dienų sumažinimas</span><span class="sxs-lookup"><span data-stu-id="073dd-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


