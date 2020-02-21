---
title: Kelių klientų užsakymų ir SF grąžinamos prekės
description: Šioje temoje aprašomos funkcijos, padedančios atlikti kelių klientų užsakymų ir SF grąžinimus „Dynamics 365 Commerce“.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004463"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="e346d-103">Kelių klientų užsakymų ir SF grąžinamos prekės</span><span class="sxs-lookup"><span data-stu-id="e346d-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e346d-104">Gali būti atliekami kelių užsakymų ir SF grąžinimai.</span><span class="sxs-lookup"><span data-stu-id="e346d-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="e346d-105">„Commercel“ sukonfigūravimas, kad būtų palaikomi kelių kliento užsakymų ir SF grąžinimai</span><span class="sxs-lookup"><span data-stu-id="e346d-105">Configure Commerce to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="e346d-106">Eikite į **Prekybos parametrai \> Klientų užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="e346d-106">Go to **Commerce parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="e346d-107">Įjunkite parametrą **Įjungti kelių užsakymų grąžinimus**.</span><span class="sxs-lookup"><span data-stu-id="e346d-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="e346d-108">Grąžinimų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="e346d-108">Process returns</span></span>

<span data-ttu-id="e346d-109">Įjungus šį parametrą ir pakeitimus sinchronizavus su parduotuvėmis, parduotuvės kasininkas gali pasirinkti kelis kliento pardavimo užsakymus dėl grąžinimo.</span><span class="sxs-lookup"><span data-stu-id="e346d-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="e346d-110">Pasirinkus užsakymus, bus parodytas visų grąžintinų produktų iš visų užsakymų SF sąrašas.</span><span class="sxs-lookup"><span data-stu-id="e346d-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="e346d-111">Tada kasininkas gali pasirinkti grąžintinus produktus.</span><span class="sxs-lookup"><span data-stu-id="e346d-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="e346d-112">Sukuriamas vienas grąžinimo užsakymas visiems pasirinktiems produktams.</span><span class="sxs-lookup"><span data-stu-id="e346d-112">A single return order will be created for all the selected products.</span></span>
