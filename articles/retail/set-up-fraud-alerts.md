---
title: "Įspėjimų dėl apgaulės nustatymas"
description: "Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją. Galite apibrėžti konkrečius kodus, kurie būtų naudojami norint automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="bc5f1-104">Įspėjimų dėl apgaulės nustatymas</span><span class="sxs-lookup"><span data-stu-id="bc5f1-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="bc5f1-105">Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="bc5f1-106">Galite apibrėžti konkrečius kodus, kurie būtų naudojami norint automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="bc5f1-107">Prieš nustatydami ir naudodami apgaulės patikros taisykles, turite įgalinti apgaulės patikrą ir apibrėžti pagrindines apgaulės patikros reikšmes skambučių centro parametruose.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="bc5f1-108">Naudojami du toliau nurodyti apgaulės taisyklių tipai.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="bc5f1-109">**Statinės taisyklės** naudoja konkrečią reikšmę, pvz., telefono numerį, kuris buvo įtrauktas į juodąjį sąrašą.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="bc5f1-110">**Dinaminės taisyklės** gali būti sudarytos iš kintamųjų ir sąlygų.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="bc5f1-111">Prieš kurdami dinaminę taisyklę, turite sukurti kintamuosius ir sąlygas, apibrėžiančias, kam taisyklė yra taikoma ir kada ji turėtų būti taikoma.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="bc5f1-112">Pavyzdžiui, norite sukurti taisyklę, pagal kurią klientui 1202 pateikus 1 000,00 arba didesnės vertės užsakymą, pardavimo užsakymas turėtų būti sulaikomas, kol bus patikrintas kliento mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="bc5f1-113">Šiuo atveju kintamieji yra klientas 1202 ir užsakymo bendroji suma 1 000,00.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="bc5f1-114">Sąlyga nurodo, kad klientui 1202 pateikus užsakymą, kurio bendra suma yra lygi arba didesnė nei 1 000,00, pardavimo užsakymas turi būti sulaikytas, kol bus patikrintas kliento mokėjimas.</span><span class="sxs-lookup"><span data-stu-id="bc5f1-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




