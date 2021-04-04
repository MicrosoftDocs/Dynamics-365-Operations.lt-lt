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
ms.openlocfilehash: df528bf7e95ee7ea74a792894b5e1c2f50c57730
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234758"
---
# <a name="reduction-days-example"></a><span data-ttu-id="57552-103">Mažinimo dienų pavyzdys</span><span class="sxs-lookup"><span data-stu-id="57552-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="57552-104">Sukūrėte abonementinę operaciją kliento abonementui tvarkyti, kaip aprašyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="57552-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="57552-105">Nuo datos</span><span class="sxs-lookup"><span data-stu-id="57552-105">From date</span></span></p></th>
<th><p><span data-ttu-id="57552-106">Iki datos</span><span class="sxs-lookup"><span data-stu-id="57552-106">To date</span></span></p></th>
<th><p><span data-ttu-id="57552-107">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="57552-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="57552-108">Abonemento tipas</span><span class="sxs-lookup"><span data-stu-id="57552-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="57552-109">Project</span><span class="sxs-lookup"><span data-stu-id="57552-109">Project</span></span></p></th>
<th><p><span data-ttu-id="57552-110">Kategorija</span><span class="sxs-lookup"><span data-stu-id="57552-110">Category</span></span></p></th>
<th><p><span data-ttu-id="57552-111">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="57552-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="57552-112">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="57552-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57552-113">2011 m. kovo 01 d.</span><span class="sxs-lookup"><span data-stu-id="57552-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="57552-114">2011 m. kovo 31 d.</span><span class="sxs-lookup"><span data-stu-id="57552-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="57552-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="57552-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="57552-116"><strong>Reguliarus</strong></span><span class="sxs-lookup"><span data-stu-id="57552-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="57552-117">9013</span><span class="sxs-lookup"><span data-stu-id="57552-117">9013</span></span></p></td>
<td><p><span data-ttu-id="57552-118">SubKat2</span><span class="sxs-lookup"><span data-stu-id="57552-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="57552-119">EUR</span><span class="sxs-lookup"><span data-stu-id="57552-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="57552-120">200,00</span><span class="sxs-lookup"><span data-stu-id="57552-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57552-121">Klientas praneša, kad jam dvi dienas (kovo 10 d. ir kovo 11 d.) nereikės aptarnavimo.</span><span class="sxs-lookup"><span data-stu-id="57552-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="57552-122">Sutinkate sutrumpinti abonementą šiomis dviejomis dienomis.</span><span class="sxs-lookup"><span data-stu-id="57552-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="57552-123">Sukuriate naują **Mažinimo dienų** tipo operaciją, kaip aprašyta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="57552-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="57552-124">Nuo datos</span><span class="sxs-lookup"><span data-stu-id="57552-124">From date</span></span></p></th>
<th><p><span data-ttu-id="57552-125">Iki datos</span><span class="sxs-lookup"><span data-stu-id="57552-125">To date</span></span></p></th>
<th><p><span data-ttu-id="57552-126">Prenumerata</span><span class="sxs-lookup"><span data-stu-id="57552-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="57552-127">Abonemento tipas</span><span class="sxs-lookup"><span data-stu-id="57552-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="57552-128">Project</span><span class="sxs-lookup"><span data-stu-id="57552-128">Project</span></span></p></th>
<th><p><span data-ttu-id="57552-129">Kategorija</span><span class="sxs-lookup"><span data-stu-id="57552-129">Category</span></span></p></th>
<th><p><span data-ttu-id="57552-130">Pardav. valiuta</span><span class="sxs-lookup"><span data-stu-id="57552-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="57552-131">Pardavimo kaina</span><span class="sxs-lookup"><span data-stu-id="57552-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57552-132">2011 m. kovo 10 d.</span><span class="sxs-lookup"><span data-stu-id="57552-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="57552-133">2011 m. kovo 11 d.</span><span class="sxs-lookup"><span data-stu-id="57552-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="57552-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="57552-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="57552-135"><strong>Sumažinimo dienos</strong></span><span class="sxs-lookup"><span data-stu-id="57552-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="57552-136">9013</span><span class="sxs-lookup"><span data-stu-id="57552-136">9013</span></span></p></td>
<td><p><span data-ttu-id="57552-137">SubKat2</span><span class="sxs-lookup"><span data-stu-id="57552-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="57552-138">EUR</span><span class="sxs-lookup"><span data-stu-id="57552-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="57552-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="57552-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57552-140">Kai išrašoma SF už 2011 m. kovo mėn. operacijas, 200 EUR pardavimo kaina yra sumažinama 12,90 EUR.</span><span class="sxs-lookup"><span data-stu-id="57552-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="57552-141">Todėl mokėtina abonementinės operacijos suma yra 187,10 EUR, tad bendra SF suma už dvi operacijas yra 187,10 EUR.</span><span class="sxs-lookup"><span data-stu-id="57552-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="57552-142">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="57552-142">See also</span></span>

[<span data-ttu-id="57552-143">Abonementinio mokesčio dienų sumažinimas</span><span class="sxs-lookup"><span data-stu-id="57552-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]