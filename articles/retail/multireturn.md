---
title: Kelių klientų užsakymų ir SF grąžinamos prekės
description: Šioje temoje aprašomos funkcijos, kurios leidžia atlikti kelių klientų užsakymų ir SF „Microsoft Dynamics 365 for Retail“ grąžinimus.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2019
ms.locfileid: "373073"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="488a6-103">Kelių klientų užsakymų ir SF grąžinamos prekės</span><span class="sxs-lookup"><span data-stu-id="488a6-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="488a6-104">„Dynamics 365 for Finance and Operations“ 10.0 versijoje galima atlikti kelių užsakymų ir SF grąžinimus, kai senesnėse nei 10.0 versijose vienu metu galima apdoroti tik vienos SF grąžinimus.</span><span class="sxs-lookup"><span data-stu-id="488a6-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="488a6-105">Konfigūruokite „Retail“, kad būtų palaikomi kelių kliento užsakymų ir SF grąžinimai</span><span class="sxs-lookup"><span data-stu-id="488a6-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="488a6-106">Eikite į **„Retail“ parametrai \> Klientų užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="488a6-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="488a6-107">Įjunkite parametrą **Įjungti kelių užsakymų grąžinimus**.</span><span class="sxs-lookup"><span data-stu-id="488a6-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="488a6-108">Grąžinimų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="488a6-108">Process returns</span></span>

<span data-ttu-id="488a6-109">Įjungus šį parametrą ir pakeitimus sinchronizavus su parduotuvėmis, parduotuvės kasininkas gali pasirinkti kelis kliento pardavimo užsakymus dėl grąžinimo.</span><span class="sxs-lookup"><span data-stu-id="488a6-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="488a6-110">Pasirinkus užsakymus, bus parodytas visų grąžintinų produktų iš visų užsakymų SF sąrašas.</span><span class="sxs-lookup"><span data-stu-id="488a6-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="488a6-111">Tada kasininkas gali pasirinkti grąžintinus produktus.</span><span class="sxs-lookup"><span data-stu-id="488a6-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="488a6-112">Sukuriamas vienas grąžinimo užsakymas visiems pasirinktiems produktams.</span><span class="sxs-lookup"><span data-stu-id="488a6-112">A single return order will be created for all the selected products.</span></span>