---
title: Mažinimo dienų pavyzdys
description: Mažinimo dienų pavyzdys.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46b38579e8a6246476d0893e1a047ad434f6d399
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564513"
---
# <a name="reduction-days-example"></a><span data-ttu-id="6fbd1-103">Mažinimo dienų pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6fbd1-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6fbd1-104">Sukūrėte abonementinę operaciją kliento abonementui tvarkyti, kaip aprašyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="6fbd1-105">Nuo datos</span><span class="sxs-lookup"><span data-stu-id="6fbd1-105">From date</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-106">Iki datos</span><span class="sxs-lookup"><span data-stu-id="6fbd1-106">To date</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-107">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="6fbd1-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-108">Abonemento tipas</span><span class="sxs-lookup"><span data-stu-id="6fbd1-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-109">Project</span><span class="sxs-lookup"><span data-stu-id="6fbd1-109">Project</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-110">Kategorija</span><span class="sxs-lookup"><span data-stu-id="6fbd1-110">Category</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-111">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="6fbd1-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-112">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="6fbd1-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fbd1-113">2011 m. kovo 01 d.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-114">2011 m. kovo 31 d.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="6fbd1-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-116"><strong>Reguliarus</strong></span><span class="sxs-lookup"><span data-stu-id="6fbd1-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="6fbd1-117">9013</span><span class="sxs-lookup"><span data-stu-id="6fbd1-117">9013</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-118">SubKat2</span><span class="sxs-lookup"><span data-stu-id="6fbd1-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-119">EUR</span><span class="sxs-lookup"><span data-stu-id="6fbd1-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-120">200,00</span><span class="sxs-lookup"><span data-stu-id="6fbd1-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6fbd1-121">Klientas praneša, kad jam dvi dienas (kovo 10 d. ir kovo 11 d.) nereikės aptarnavimo.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="6fbd1-122">Sutinkate sutrumpinti abonementą šiomis dviejomis dienomis.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="6fbd1-123">Sukuriate naują **Mažinimo dienų** tipo operaciją, kaip aprašyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="6fbd1-124">Nuo datos</span><span class="sxs-lookup"><span data-stu-id="6fbd1-124">From date</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-125">Iki datos</span><span class="sxs-lookup"><span data-stu-id="6fbd1-125">To date</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-126">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="6fbd1-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-127">Abonemento tipas</span><span class="sxs-lookup"><span data-stu-id="6fbd1-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-128">Project</span><span class="sxs-lookup"><span data-stu-id="6fbd1-128">Project</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-129">Kategorija</span><span class="sxs-lookup"><span data-stu-id="6fbd1-129">Category</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-130">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="6fbd1-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="6fbd1-131">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="6fbd1-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6fbd1-132">2011 m. kovo 10 d.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-133">2011 m. kovo 11 d.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="6fbd1-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-135"><strong>Sumažinimo dienos</strong></span><span class="sxs-lookup"><span data-stu-id="6fbd1-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="6fbd1-136">9013</span><span class="sxs-lookup"><span data-stu-id="6fbd1-136">9013</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-137">SubKat2</span><span class="sxs-lookup"><span data-stu-id="6fbd1-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-138">EUR</span><span class="sxs-lookup"><span data-stu-id="6fbd1-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="6fbd1-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="6fbd1-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6fbd1-140">Kai išrašoma SF už 2011 m. kovo mėn. operacijas, 200 EUR pardavimo kaina yra sumažinama 12,90 EUR.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="6fbd1-141">Todėl mokėtina abonementinės operacijos suma yra 187,10 EUR, tad bendra SF suma už dvi operacijas yra 187,10 EUR.</span><span class="sxs-lookup"><span data-stu-id="6fbd1-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="6fbd1-142">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="6fbd1-142">See also</span></span>

[<span data-ttu-id="6fbd1-143">Abonementinio mokesčio dienų sumažinimas</span><span class="sxs-lookup"><span data-stu-id="6fbd1-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


