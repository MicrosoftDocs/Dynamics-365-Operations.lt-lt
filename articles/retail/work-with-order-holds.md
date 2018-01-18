---
title: "Užsakymo sulaikymas"
description: "Šioje temoje aprašomi užsakymų sulaikymai naudojant „Dynamics 365 for Retail“."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: c543a1538a83d88eaebce203e14cf8b0e10e2ad3
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="order-holds"></a><span data-ttu-id="1185e-103">Užsakymo sulaikymas</span><span class="sxs-lookup"><span data-stu-id="1185e-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="1185e-104">Šioje temoje aprašomi užsakymų sulaikymai naudojant „Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="1185e-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1185e-105">Užsakymą galima sulaikyti dėl įvairių priežasčių.</span><span class="sxs-lookup"><span data-stu-id="1185e-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="1185e-106">Pavyzdžiui, galima sulaikyti užsakymą, kol bus patikrintas kliento adresas ar mokėjimo būdas arba kol vadybininkas peržiūrės kliento kredito limitą.</span><span class="sxs-lookup"><span data-stu-id="1185e-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="1185e-107">Pardavimo proceso metu kartais privalu pardavimo užsakymą sulaikyti.</span><span class="sxs-lookup"><span data-stu-id="1185e-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="1185e-108">Pvz., pardavimo užsakymas gali būti sulaikytas dėl kliento mokėjimo problemų, įtariamos apgaulės arba laukiant, kol užsakymą peržiūrės vadovas.</span><span class="sxs-lookup"><span data-stu-id="1185e-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="1185e-109">Kai pardavimo užsakymas sulaikomas, jam priskiriamas užsakymo sulaikymo kodas, kad parodytų sulaikymo priežastį.</span><span class="sxs-lookup"><span data-stu-id="1185e-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="1185e-110">Pardavimo užsakymų sulaikymo kodus konfigūruoti galima pasirinkus **Pardavimas ir rinkodara** &gt; **Sąranka** &gt; **Pardavimo užsakymai** &gt; **Užsakymų sulaikymo kodai**.</span><span class="sxs-lookup"><span data-stu-id="1185e-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="1185e-111">Pardavimo užsakymą galima sulaikyti neautomatiniu būdu tuo metu, užsakymas kuriamas, arba vėliau.</span><span class="sxs-lookup"><span data-stu-id="1185e-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="1185e-112">Be to, užsakymą galima sulaikyti automatiškai pagal apgaulės taisykles.</span><span class="sxs-lookup"><span data-stu-id="1185e-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="1185e-113">Kai pardavimo užsakymas yra sulaikytas, gali reikėti atnaujinti jo informaciją.</span><span class="sxs-lookup"><span data-stu-id="1185e-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="1185e-114">Taip pat tęsdami darbą su pardavimo užsakymu galite jį išregistruoti.</span><span class="sxs-lookup"><span data-stu-id="1185e-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="1185e-115">Pardavimo užsakymą galite išregistruoti, vėl įregistruoti ir net perrašyti kito vartotojo išregistravimą, naudodami užsakymo sulaikymo darbo sritį (**„Retail“** &gt; **Klientai** &gt; **Užsakymo sulaikymas**).</span><span class="sxs-lookup"><span data-stu-id="1185e-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="1185e-116">Kai užsakymas paruoštas baigti, prieš baigiant užsakymo procesą būtina pašalinti sulaikymą.</span><span class="sxs-lookup"><span data-stu-id="1185e-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




