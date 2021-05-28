---
title: Naudojant prekių grąžinimo grupes, klientų grąžinimų kaupti nepavyko
description: Kai kliento grąžinimo sutartis naudojate kartu su prekių grąžinimo grupėmis, grąžinimai apskaičiuojami, bet kaupimo nepavyksta.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026735"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="6ac5b-103">Naudojant prekių grąžinimo grupes, klientų grąžinimų kaupti nepavyko</span><span class="sxs-lookup"><span data-stu-id="6ac5b-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="6ac5b-104">KB numeris: 4611372</span><span class="sxs-lookup"><span data-stu-id="6ac5b-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="6ac5b-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="6ac5b-105">Symptoms</span></span>

<span data-ttu-id="6ac5b-106">Kai kliento grąžinimo sutartis naudojate kartu su ( *kiekio* tipu) ir prekių grąžinimo grupėmis, grąžinimai apskaičiuojami, bet kaupimo nepavyksta.</span><span class="sxs-lookup"><span data-stu-id="6ac5b-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="6ac5b-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="6ac5b-107">Resolution</span></span>

<span data-ttu-id="6ac5b-108">Sistema veikia kaip sukurta.</span><span class="sxs-lookup"><span data-stu-id="6ac5b-108">The system is behaving as designed.</span></span> <span data-ttu-id="6ac5b-109">Prekių grupių grupė tik tos prekės, kurių ribinės vertės sąlyga tokia pati.</span><span class="sxs-lookup"><span data-stu-id="6ac5b-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="6ac5b-110">Grąžinimo sąlyga (ribinė vertė) nustatoma pagal kiekvienos prekės sumą, o ne pagal kiekvienos prekių grupės prekės kaupimo sumą.</span><span class="sxs-lookup"><span data-stu-id="6ac5b-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
