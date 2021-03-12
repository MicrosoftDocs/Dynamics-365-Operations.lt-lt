---
title: Trikties šalinimo išvesties sandėlio operacijos
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio operacijomis „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993983"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="f8acb-103">Trikties šalinimo išvesties sandėlio operacijos</span><span class="sxs-lookup"><span data-stu-id="f8acb-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8acb-104">Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite susidurti dirbdami su išvesties sandėlio operacijomis „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="f8acb-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="f8acb-105">Gaunu tolesnį klaidos pranešimą: „Pardavimo užsakymo nepavyko išleisti"</span><span class="sxs-lookup"><span data-stu-id="f8acb-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f8acb-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="f8acb-106">Issue description</span></span>

<span data-ttu-id="f8acb-107">Ši problema gali įvykti dėl kelių priežasčių.</span><span class="sxs-lookup"><span data-stu-id="f8acb-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="f8acb-108">Pavyzdžiui, užsakymą sustabdė kredito valdyba ir jokių siuntimų negalima sukurti kol patvirtinimo pašto adresas yra įvestas pardavimo eilutėms susietoms su pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="f8acb-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="f8acb-109">Kitu atveju, užsakymas yra sustabdytas ir turi būti įvertintas prieš tai, kai jis bus išleistas į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f8acb-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="f8acb-110">Šis sulaikymas gali būti konkretus užsakymui arba būti kliento paskyroje.</span><span class="sxs-lookup"><span data-stu-id="f8acb-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f8acb-111">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="f8acb-111">Issue resolution</span></span>

<span data-ttu-id="f8acb-112">Įtraukite ar naujinkite adresą pardavimo užsakyme ir užsakymo eilutėse ir tuomet paleiskite užsakymą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f8acb-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="f8acb-113">Užsakymai gali būti išleisti į sandėlį tik jei jie turi galiojantį pristatymo adresą (adreso formato nustatymuose **Organizacijos adminstracijos** modulyje).</span><span class="sxs-lookup"><span data-stu-id="f8acb-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="f8acb-114">Tirkite sustabdytą užsakymą ir adreso problemas.</span><span class="sxs-lookup"><span data-stu-id="f8acb-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="f8acb-115">Tuomet pašalinkite sustabdytą užsakymą ar klientą ir išleiskite užsakymą į sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f8acb-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="f8acb-116">Gaunu tolesnį pranešimą: „Siuntimas 1% apkrovai buvo patvirtintas."</span><span class="sxs-lookup"><span data-stu-id="f8acb-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="f8acb-117">Nepaisant, nėra jokių publikuotų eilučių.</span><span class="sxs-lookup"><span data-stu-id="f8acb-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f8acb-118">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="f8acb-118">Issue description</span></span>

<span data-ttu-id="f8acb-119">Krovinio siuntimas buvo patvirtintas, bet neįvyko jokio tolesnio publikavimo.</span><span class="sxs-lookup"><span data-stu-id="f8acb-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f8acb-120">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="f8acb-120">Issue resolution</span></span>

<span data-ttu-id="f8acb-121">Siuntimo patvirtinimas neveikia publikavimo.</span><span class="sxs-lookup"><span data-stu-id="f8acb-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="f8acb-122">Jis tik naujina siuntimą ir krovinio būseną.</span><span class="sxs-lookup"><span data-stu-id="f8acb-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="f8acb-123">Publikavimas turi vykti kaip atskiras procesas.</span><span class="sxs-lookup"><span data-stu-id="f8acb-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="f8acb-124">Gaunu tolesnį klaidos pranešimą: „Tiesioginis pristatymas negali apdoroti sandėlio 1%, nes jam įjungtas sandėlio valdymas.</span><span class="sxs-lookup"><span data-stu-id="f8acb-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="f8acb-125">Prašome nurodyti kitą sandelį, kuris nėra įjungtas sandėlio valdymui."</span><span class="sxs-lookup"><span data-stu-id="f8acb-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f8acb-126">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="f8acb-126">Issue description</span></span>

<span data-ttu-id="f8acb-127">Prekė yra įtraukta į pardavimo eilutę tiesioginiam pristatymui iš sandėlio, kuris yra įjungtas sandėlio valdyme (WMS).</span><span class="sxs-lookup"><span data-stu-id="f8acb-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="f8acb-128">Gausite šį klaidos pranešimą, kai pardavimo eilutės bus naujinta.</span><span class="sxs-lookup"><span data-stu-id="f8acb-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="f8acb-129">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="f8acb-129">Issue resolution</span></span>

<span data-ttu-id="f8acb-130">„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą.</span><span class="sxs-lookup"><span data-stu-id="f8acb-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="f8acb-131">Šiuo metu, WMS nepalaiko tiesioginio pristatymo.</span><span class="sxs-lookup"><span data-stu-id="f8acb-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="f8acb-132">Dėl to, norėdami naudoti tiesioginį pristatymą, turite pasirinkti ne WMS prekę ir sandėlį.</span><span class="sxs-lookup"><span data-stu-id="f8acb-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
